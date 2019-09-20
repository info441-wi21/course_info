# INFO-441 Server-Side Development

This is the homepage for the [UW iSchool](https://ischool.uw.edu/) Winter 2019 Server-side development course.

Dive deeply into the world of server-side development. Build your own web application. Deploy it to the cloud. Authenticate users. Authorize and validate persistent data. Build retrieval indexes for fast searching. Notify clients of changes in real-time. Extend your system with a microservice architecture. Put it all together in a sophisticated web applications.

## Team

Instructor: [Kyle Thayer](http://kylethayer.com)

TA's: William Kwok & Rico Wang

(The team wants to thank [Dave Stearns](https://www.linkedin.com/in/david-stearns-09a27319/) for making their material available as a base for this course and [Nigini Oliveira](http://nigini.me/) for his advice and version of the course repo. 

### Office Hours

TBD

## Communication

All communication should happen through [Canvas](https://canvas.uw.edu/courses/1321414 "Canvas page for the UW iSchool Autumn 2019 Server-side development course") and [Microsoft Teams](https://teams.microsoft.com/l/team/19%3aa670d1b210a14d4e8cc8beeafc70246a%40thread.skype/conversations?groupId=8f272ac9-f36a-4680-a82b-08b4c82b5e0e&tenantId=f6b6dd5b-f02f-441a-99a0-162ac5060bd2)).

## Schedule

Below, each day have a set of required sources that we want you to read/watch **before coming to class**. These will orient and prepare you for our in-class coding exercises. 
If you don't do this, you'll get lost rather quickly.

| Date   | Material |
| :----: | -------- |
| 1/8 | Welcome to the Server-Side |
| |<a href="https://drstearns.github.io/tutorials/http/">The HyperText Transfer Protocol</a>|
| |<a href="https://drstearns.github.io/tutorials/env/">Environment Variables</a>|
| |<a href="https://drstearns.github.io/tutorials/gointro/">Introduction to Go</a>|
| |<a href="https://drstearns.github.io/tutorials/golang/">The Go Language</a>|
| |<a href="https://drstearns.github.io/tutorials/goweb/">Go Web Servers</a>|
| |[!! Exercise](https://classroom.github.com/a/ZnYsYjMQ)|
| |[!! Week Assignment](https://classroom.github.com/a/ZMocr6oA)|
| LAB  | How to 411? |
| 1/10 | Go Web Services |
| |<a href="https://drstearns.github.io/tutorials/goslicemap/">Go Slices and Maps</a>|
| |<a href="https://drstearns.github.io/tutorials/gojson/">Go Structs and JSON</a>|
| |<a href="https://drstearns.github.io/tutorials/cors/">Cross-Origin Resource Sharing</a>|
| |[!! Exercise](https://github.com/info441/exercises/tree/master/zip)|
| 1/15 | Docker |
| |<a href="https://drstearns.github.io/tutorials/docker/">Containerizing with Docker</a>|
| |<a href="https://docs.docker.com/engine/userguide/eng-image/dockerfile_best-practices/">Dockerfile Best Practices</a>|
| |<a href="https://docs.docker.com/engine/admin/start-containers-automatically/#use-a-restart-policy">Docker restart policies</a>|
| |[!! Exercise](https://github.com/info441/exercises/tree/master/docker)|
| LAB | Docker Practice |
| 1/17 | Deploying & Encrypting |
| |<a href="https://drstearns.github.io/tutorials/https/">Communicating Securely with HTTPS</a>|
| |<a href="https://drstearns.github.io/tutorials/deploy2do/">Deploying to Digital Ocean</a>|
| |<a href="https://drstearns.github.io/tutorials/deploy2aws/">Deploying to Amazon Web Services (AWS)</a>|
| |[!! Exercise](https://github.com/info441/exercises/tree/master/deploy)
| 1/22 | Automated Tests |
| |<a href="https://drstearns.github.io/tutorials/testing/">Automated Testing in Go</a>| 
| |<a href="https://blog.golang.org/cover">The Cover Story</a>|
| |[!!Exercise](https://github.com/info441/exercises/tree/master/testing)|
| LAB | Automated Testing Practice |
| 1/24 | Tracking Sessions |
| |<a href="https://drstearns.github.io/tutorials/sessions/">Tracking Sessions</a>|
| |<a href="https://redis.io/topics/data-types-intro">Redis Datatypes</a>|
| |<a href="https://docs.docker.com/engine/tutorials/networkingcontainers/">Docker Networks</a>|
| |[!!Exercise](https://github.com/info441/exercises/tree/master/hmac)|
| 1/29 | Persisting Data |
| |<a href="https://drstearns.github.io/tutorials/godb/">Talking to Databases from Go</a>|
| |<a href="https://drstearns.github.io/tutorials/gohandlerctx/">Sharing Values with Go Handlers</a>|
| |<a href="https://drstearns.github.io/tutorials/authentication/">Authenticating Users</a>|
| |[!!Exercise](https://github.com/info441/exercises/tree/master/postman)|
| LAB | Postman Testing |
| 1/31 | Catch-Up + Project Bootstrap |
| 2/5 | REST APIs + Middleware |
| |<a href="https://drstearns.github.io/tutorials/gomiddleware/">Middleware Patterns in Go</a>|
| |<a href="https://drstearns.github.io/tutorials/rest/">REST APIs</a>|
| |[!!Exercise](https://github.com/info441/exercises/tree/master/middleware)|
| LAB | Middleware Practice |
| 2/7 | Trie Indexes |
| |<a href="https://drstearns.github.io/tutorials/trie/">The Trie Data Structure</a>|				
| |<a href="https://drstearns.github.io/tutorials/mutexes/">Protecting Data Structures with Mutexes</a>|
| |[!!Exercise](https://github.com/info441/exercises/tree/master/trie)|
| 2/12 | Microservices |
| |<a href="https://www.nginx.com/blog/introduction-to-microservices/">NGINX 7-Part article series on Microservices</a>|
| |<a class="inline_disabled"  href="https://youtu.be/5qJ_BibbMLw">Fast Delivery Talk</a> by Adrian Cockcroft|
| |<a class="inline_disabled"  href="https://youtu.be/1wiMLkXz26M">Migrating to Microservices Talk</a> by Adrian Cockcroft|
| |<a href="https://golang.org/pkg/net/http/httputil/#ReverseProxy">httputil.ReverseProxy</a>|
| |[!!Exercise](https://github.com/info441/exercises/tree/master/microservices)|
| LAB | Service Discovery |
| 2/14 | Node.js Microservices |
| |<a href="https://drstearns.github.io/tutorials/nodeweb/">Node.js Microservices</a>|
| |<a href="https://expressjs.com/en/starter/basic-routing.html">Express.js Basic Routing</a>|
| |<a href="https://github.com/mysqljs/mysql/blob/master/Readme.md">Node.js MySQL Driver Overview</a>|
| 2/19 | Microservices catchup + Project Ideas checkup |
| LAB | Microservices |
| 2/21 | Message Queues |
| |<a href="https://www.rabbitmq.com/tutorials/tutorial-one-go.html">RabbitMQ Tutorial for Go</a>|
| |<a href="https://www.rabbitmq.com/tutorials/tutorial-one-javascript.html">RabbitMQ Tutorial for Node.js</a>|
| |[Use case: Asynchronous Tasks in Python with Celery and RabbitMQ](https://www.youtube.com/watch?v=fg-JfZBetpM)|
| 2/26 | Web Sockets |
| |[TALK: Real-life WebSocket Use Cases and Experiences](https://youtu.be/khULSvz_hdE)|
| |<a href="https://godoc.org/github.com/gorilla/websocket">Gorilla Web Socket Package</a>|
| |<a href="https://developer.mozilla.org/en-US/docs/Web/API/WebSockets_API/Writing_WebSocket_client_applications">Writing WebSocket Client Applications</a>|
| LAB | Homework Time |
| 2/28 | Concurrent Programming with Channels |
| |<a class="inline_disabled" href="https://www.youtube.com/watch?v=cN_DpYBzKso">Rob Pike on Concurrency is not Parallelism</a> (<a href="https://talks.golang.org/2012/waza.slide#1">slides from talk</a>)|
| |<a class="inline_disabled" href="https://www.youtube.com/watch?v=f6kdp27TYZs">Rob Pike on Go Concurrency Patterns</a> (<a href="https://talks.golang.org/2012/concurrency.slide#1">slides from talk</a>)|
| |<a href="https://www.golang-book.com/books/intro/10">Concurrency</a>|
| 3/5 | Homework Time |
| LAB | Homework Time |
| 3/7 | Homework Time |
| 3/12 | Homework Time |
| 3/14 | Project Presentations??? |
| 3/19 | Project Presentations!!! |

## Grading

This course will be evaluated based on weekly assignments (10) and class+lab exercises (~18).

Assignments worth 90% of the grade and will be released every Tuesday morning. The submission deadline will be every Monday night (so you will have a week to work on each of those). 
Exercises compose the other 10% of the final grade and will be only doable by students present to classes. Because of that, you can miss up to 3 of those and still get full points.

In total, each week you will have an assignment that worths 100 points and two exercises worthing ten.

### Calculation of Final Grades

Canvas tracks grades on a percentage scale. To convert those to a 4.0 scale we will use [the standard iSchool conversion chart](https://faculty.washington.edu/dlsinfo/grading/grade-conversion-chart.pdf). 

BTW: Canvas is already configured to calculate your final grade considering the previously described 90/10 grading weights and this conversion scale.

### Late Work

Since each assignment builds upon your solution for the previous one, it's imperative that you keep up. To encourage you to keep on schedule, we will deduct 10% of the possible points per 24-hour period that your submission is late, with a one hour initial grace period. For example, if the assignment is worth 100 points and your submission is between 1 and 24 hours late, the maximum you can receive on the assignment is 90 points. If your submission is between 24 and 48 hours late, the maximum you can receive is 80 points.

That said, we realize that sometimes life gets complicated and you might need a little extra time to finish a particular challenge. To give you a little flexibility you have 5 free late days that you can spend throughout the quarter. Each late day gives you a free 24-hour extension on the challenge. Unless you specify otherwise, we will use your late days for any work you submit late. After you exhaust all your late days, the normal late penalties will start to accrue.

If something tragic occurs during the quarter, please let us know and we can work out something.


## Course Rules

In addition to the standard [iSchool and UW academic policies](https://depts.washington.edu/infodocs/academic_policies/) that apply to all of our courses, the following rules also apply to this course.

### Plagiarism

We encourage collaboration, but "collaboration" doesn't mean copying other people's code and trying to pass it off as your own. Collaboration means talking through your approach to a problem, or showing someone how you make something work. You can borrow approaches or techniques, but I want you to write your own implementation.

Although professional web developers often reuse code they find on the web, they also take the time to understand what that code is doing, customize it to their specific context, and cite the source so that they can find it again later. If you want to use code you find on the web, please include the source URL in a comment above the code, and take the time to understand why it works. Otherwise you won't learn anything.

If we receive multiple solutions with nearly identical code, we will notice. Remember that git records a log of every commit, so we can see exactly what you committed and when. If we see you commit code that is virtually identical to code a fellow student committed earlier, it's not too difficult to figure out who is copying from whom.

If we determine that you plagiarized code, you will get an automatic zero on the assignment, and we will file an academic misconduct report with the Associate Dean of Academics. We will also have a very unpleasant conversation about your future in the Information School, so just don't do it. If you've simply run out of time, use your late days.
