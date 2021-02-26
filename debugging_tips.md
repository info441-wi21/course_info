# Debugging Tips
## Setting up GO
### “Go install” vs “Go Build”
**Build vs compile vs executable:** When source code is compiled and built, it becomes an executable file. You cannot directly run the source code file(s) in Go (a la Javascript). Compile process ensures that source code can be turned into an executable. It is the build process that’s actually creating the final executable. 

**Note, not all Go files can be turned into an executable:** To create an executable file, you must invoke go install. go install succeeds only if there is a .go file inside your directory that contains 1) **a main() function**, and 2) **“package main”** declaration. (GOTCHA: package main must be the statement in the file) **This is how Go knows “where” to start the compilation process.**

**go install vs go build:** Both commands create an executable. The difference is that go install puts the executable in $GOPATH/bin, and go build puts it in the current working directory. 

**How to run the executable file:** Go executables do not have a file extension (like .exe in Windows, or .sh for shell script). Instead, they take on the name of the folder containing the .go file with the **main** function. To run your go executables from any directory, make sure to add $GOPATH to your $PATH (by editing your ~/.bash_profile)

_So how do you know if your code is valid Go code? If go install or go build finishes with no errors._

### I made a code change, and re-ran the executable, but nothing changed. Why? 
Always ‘go install’ before you re-run your code. Otherwise, you won’t see any changes. Many Go newcomers are baffled when they make some code changes, run their executable, and see nothing has changed. Typically, that’s because he/she has forgotten to compile the code and rebuild the executable via **‘go install’**. 

Remember, **Go is a compiled language.** That means, running code requires you to re-build / re-compile your entire source code, for you to see code changes take effect. 

### go build / go install did not create an executable

It might be because there’s no .go file with **a main function**, or a **package main** signature inside your folder. 

Also, remember that go install puts the executable in $GOPATH/bin. 

### I’m having issues with importing libraries
**Libraries vs non-libraries:** Simply put, packages that aren’t declared **package main** are libraries. But what does that mean? Typically, libraries contain code meant to be reused across different applications, like a library for parsing csv files. Also, libraries are places you put helper functions, models, etc, that get used by your executable.

**Custom vs standard libraries:** Standard libraries are things like “net/http” that come with your go installation. They are imported by the name, regardless of where your file is. Custom libraries are libraries that you downloaded from the web (through github, etc), or that you created. 

**Creating libraries:** When creating libraries, you must have “package &lt;library name&gt;” at the top of the file, for ALL Go files in that folder. They must all use the same library name. 

**Exporting variables and functions:** If you want something exported from a library, its name must be Capitalized. 

**Importing custom modules:** When importing custom modules, specify the full path to the folder containing the library, without the $GOPATH/src prefix.  

Say you want to use a library in /User/Go/src/custom/module/lib.go.  /User/Go is your $GOPATH. Then when you want to use, say, a function MyFunc in lib.go, you need to import it and use like this.

```
...
import custom/module/lib   // notice we don’t need .go extension
...
lib.MyFunc()     // notice I had to specify lib.MyFunc
```


**Variable visibility:** Say there’s files A, B, and C.   A and B are of the same package, and C is not.  In both A and B files, all variables and functions are visible to each other. No import necessary.  To use a function that resides in C, however, you’d need to import C library first. 

**Installing libraries from the web:** You browse Stackoverflow, and find a cool 3rd party library. You want to use it. In that case, don’t **git clone** &lt;git url&gt;, but **go get** &lt;git url&gt;. The difference is that go get actually installs the source code in addition to just download the source. But note, if you do go get &lt;git url&gt;, the code will be under $GOPATH/src/github.com/&lt;repo url&gt;.

If you install the golang tooling to VSCode or your preferred golang editor, it will provide auto importing functionalities.

### Bash Cheatsheet
```
pwd // get current working directory
echo $GOPATH  // see what $GOPATH is
vi ~/.bash_profile   // edit bash profile in VI text editor
source ~/.bash_profile //  reload bash profile 
export  VAR_NAME=VAL   // assign value VAL to variable VAR_NAME
PATH = ${GOPATH}/bin:${PATH}  // add $GOPATH to $PATH
```

## General

### My code is crashing
Sometimes when you are running your code, your code may crash and spit an output like this:

```
panic: runtime error: index out of range [1] with length 1 [recovered]
    panic: runtime error: index out of range [1] with length 1
goroutine 7 [running]:
testing.tRunner.func1(0xc000100100)
    /usr/local/go/src/testing/testing.go:874 +0x3a3
panic(0x132f240, 0xc000016580)
    /usr/local/go/src/runtime/panic.go:679 +0x1b2
github.com/UW-Info-441-Winter-Quarter-2020/homework-username/servers/gateway/handlers.extractLinkAttribute(0x1740400000002, 0x136ebce, 0x4, 0xc00011e0c0, 0x3, 0x4, 0x4)

    /Users/username/go/src/github.com/UW-Info-441-Winter-Quarter-2020/homework-username/servers/gateway/handlers/summary.go:270 +0x293
github.com/UW-Info-441-Winter-Quarter-2020/homework-username/servers/gateway/handlers.extractSummary(0x1360f83, 0x19, 0x13c9500, 0xc000120030, 0xc000112601, 0x0, 0x0)

    /Users/username/go/src/github.com/UW-Info-441-Winter-Quarter-2020/homework-username/servers/gateway/handlers/summary.go:219 +0x22a
github.com/UW-Info-441-Winter-Quarter-2020/homework-username/servers/gateway/handlers.TestExtractSummary(0xc000100100)

    /Users/username/go/src/github.com/UW-Info-441-Winter-Quarter-2020/homework-username/servers/gateway/handlers/summary_test.go:320 +0x17fb
testing.tRunner(0xc000100100, 0x1374590)
    /usr/local/go/src/testing/testing.go:909 +0xc9
created by testing.(*T).Run
    /usr/local/go/src/testing/testing.go:960 +0x350
```

In order to debug easier, you will want to understand how to read this error. In this particular case, the very thing it crashed at was due to “index out of range”, meaning in a slice or array, the code tried to access something that didn’t exist. But where does this happen? We can see on the next line “/usr/local/go/src/testing/testing.go:874 +0x3a3” which indicates that this happened on line 874 of testing.go as seen by the “:874” at the end. We never created this file, so we want to look further in the call stack to see where it hits code we wrote so something can be fixed easily. 

The line 

“/Users/username/go/src/github.com/UW-Info-441-Winter-Quarter-2020/homework-username/servers/gateway/handlers/summary.go:270 +0x293” shows that there is an issue on line 270 of this file, so you can find and fix it. 

This is known as the call stack-- when an internal function or command is called, it will push it to the stack so when it outputs this to the user, the user knows what errors happened where. In addition, you should never display this data to the user whatsoever, through the API you may expose, because it reveals implementation details about your server and could potentially be used to hack into your server.

### How should we be reporting errors?
It is important to distinguish when errors should be reported, and how to respond to the user. Here is a few scenarios we want you to think about at a high level:

1. A user logs in on your front end, and sends data to your back end to log themselves in. The user sends this data as JSON, where your server has an error detecting they used a character you dont want to allow.
	1. If you crash the server using log.Fatal, the user will never receive a response back and your server will need to start back up all over again. This is the equivalent to something like Google crashing if you make a bad request to it.
	2. If you just print out the error using log.Print, the user will never receive a response back.
	3. When the user never receives a response back, they dont know what they did wrong and they just think your site is down.
	4. What you want to do in this case is return a message to the user saying that they had bad input, and you achieve this by sending data back to the user with http.Write or json.NewEncoder.
2. A user logs in on your front end, and sends data to your back end to log themselves in. The user sends data that looks fine, but your server crashes because of some small issue you never caught.
   1. Logging the error is fine, but crashing is NOT. log.Fatal should never be used in your code UNLESS it is part of the setup procedure before http.ListenAndServe is called.
   2. Logging the error as part of developer debugging is fine, but you should DELETE it in your final production build because log spam everywhere is annoying to other developers on your project.
   3. You would want to log your error in this case. However, you also want to log important metadata of the time this occurred, what the user’s input was, and maybe some other things about your server at that time. This might look clunky if you manually insert it in that function, and the logs would definitely look really full sometimes. That is why there are tools like SumoLogic which let you manage logs and outages with nice dashboard interfaces.
  
### I’m unsure where to start debugging issues
Server not running? Website not appearing? Docker container immediately exiting? There are a few useful commands you will want to use to determine where an issue lies.
1. docker ps -a
  1. This command will let you see what containers are actively running, and which have exited. Good to see what containers have failed and when they failed.
2. docker logs &lt;containername&gt;
  1. This command will let you see what the container actually logged when you do log.Print or a different logging command (I believe, it may be fmt.Printf I can’t remember)
  2. This way you can add log statements to where you THINK a server might crash and then see if it gets there and debug what might be crashing


## Assignment 3
### Redis issues
Make sure you run redis through docker, because that is how you will be doing so on the EC2 instance.

Try reading through Dr Stearns’s tutorial on using redis locally first to learn how to do this: https://drstearns.github.io/tutorials/sessions/#secredisasasessionstore

Keep in mind Dr Stearns’s tutorial has it running on a docker network, which may not work with tests unless you set your REDISADDR environment variable to match the hostname of that network and stuff. If you want to run it on localhost for now, because you don’t need to worry about docker networks just yet, do this following command

```
docker run -d -p 6379:6379 --name redisServer redis
```

## Assignment 4
### SQL Database is no longer starting correctly, and logs have a bunch of crap in them
If you changed nothing about how your database is deployed, it is possible that you have run out of storage in your EC2 instance due to all the redeployed containers caching themselves (Docker does this to run things faster, but it uses lots of storage space!) Your EC2 instances only have like 8 GB of storage, so it adds up fast. Prune these unused images and containers by doing the following command:

```
docker system prune --all
```
OR
```
docker volume prune
```

