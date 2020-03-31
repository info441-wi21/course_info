# INFO-441 Server-Side Development

This is the homepage for the [UW iSchool](https://ischool.uw.edu/) Spring 2020 Server-side development course.

Dive deeply into the world of server-side development. Build your own web application. Deploy it to the cloud. Authenticate users. Authorize and validate persistent data. Build retrieval indexes for fast searching. Notify clients of changes in real-time. Extend your system with a microservice architecture. Put it all together in a sophisticated web applications.

## Team

Instructor: [Kyle Thayer](http://kylethayer.com)

TA's: William Kwok, Chris Forbes

(The team wants to thank [Dave Stearns](https://www.linkedin.com/in/david-stearns-09a27319/) for making their material available as a base for this course and [Nigini Oliveira](http://nigini.me/) for his advice and version of the course repo.) 

### Office Hours
Office: Online!


Office Hours: 
Kyle: TBD Or email or message me to schedule separately
Will: TBD
Chris: Monday 2pm-4pm, Wednesday 2pm-4pm

## Communication

All communication should happen through [Canvas](https://canvas.uw.edu/courses/1373080 "Canvas page for the UW iSchool Autumn 2019 Server-side development course") and [Microsoft Teams](https://teams.microsoft.com/l/team/19%3a364e3e9961e3474b8d9a8f4877762e95%40thread.tacv2/conversations?groupId=8b1d0972-e0c2-45a1-88be-9aa0761aa34a&tenantId=f6b6dd5b-f02f-441a-99a0-162ac5060bd2)) (code 41h0qjp).

## Schedule

Below, are the contents for each class day.

| Date   | Material |
| :----: | -------- |
| 3/31 | Welcome to the Server-Side |
| |<a href="https://drstearns.github.io/tutorials/http/">The HyperText Transfer Protocol</a>|
| |<a href="https://drstearns.github.io/tutorials/env/">Environment Variables</a>|
| |<a href="https://drstearns.github.io/tutorials/gointro/">Introduction to Go</a>|
| |<a href="https://drstearns.github.io/tutorials/golang/">The Go Language</a>|
| |<a href="https://canvas.uw.edu/courses/1373080/assignments/5385825">Lecture Exercises</a>|
| 4/2 | Go Web Services 
| |<a href="https://drstearns.github.io/tutorials/goweb/">Go Web Servers</a>|
| |<a href="https://drstearns.github.io/tutorials/goslicemap/">Go Slices and Maps</a>|
| |<a href="https://drstearns.github.io/tutorials/gojson/">Go Structs and JSON</a>|
| |<a href="https://drstearns.github.io/tutorials/cors/">Cross-Origin Resource Sharing</a>|
| |<a href="https://drstearns.github.io/tutorials/tokenizing/">Tokenizing HTML Streams</a>|
| |[!! Assignment (summary branch)](https://classroom.github.com/a/W3AI9d2L))|
| |[!! Exercise](https://classroom.github.com/a/uvgSMH_5)|
| |[!! Exercise](https://classroom.github.com/a/uvgSMH_5)|
| 4/7 | Docker |
| |<a href="https://drstearns.github.io/tutorials/docker/">Containerizing with Docker</a>|
| |<a href="https://docs.docker.com/engine/userguide/eng-image/dockerfile_best-practices/">Dockerfile Best Practices</a>|
| |<a href="https://docs.docker.com/engine/admin/start-containers-automatically/#use-a-restart-policy">Docker restart policies</a>|
| |[!! Exercise (docker)](https://classroom.github.com/a/uvgSMH_5)|
| 4/9 | Deploying & Encrypting |
| |<a href="https://drstearns.github.io/tutorials/https/">Communicating Securely with HTTPS</a>|
| |<a href="https://drstearns.github.io/tutorials/deploy2do/">Deploying to Digital Ocean</a>|
| |<a href="https://drstearns.github.io/tutorials/deploy2aws/">Deploying to Amazon Web Services (AWS)</a>|
| |[!! Exercise (deploy)](https://github.com/info441/exercises/tree/master/deploy)
| 4/14 | Automated Tests |
| |<a href="https://drstearns.github.io/tutorials/testing/">Automated Testing in Go</a>| 
| |<a href="https://blog.golang.org/cover">The Cover Story</a>|
| |CORS slides: <a href="slides/lecture%20-%20CORS.pptx">pptx</a>, <a href="slides/lecture%20-%20CORS.pdf">pdf</a>|
| |[!!Exercise (testing)](https://github.com/info441/exercises/tree/master/testing)|
| 4/16 | Tracking Sessions |
| |<a href="https://drstearns.github.io/tutorials/sessions/">Tracking Sessions</a>|
| |<a href="https://redis.io/topics/data-types-intro">Redis Datatypes</a>|
| |<a href="https://docs.docker.com/engine/tutorials/networkingcontainers/">Docker Networks</a>|
| |Docker Network slides: <a href="slides/lecture%20-%20Docker%20Networks.pptx">pptx</a>, <a href="slides/lecture%20-%20Docker%20Networks.pdf">pdf</a>|
| |[!!Exercise (hmac)](https://github.com/info441/exercises/tree/master/hmac)|
| 4/21 | Persisting Data |
| |<a href="https://drstearns.github.io/tutorials/godb/">Talking to Databases from Go</a>|
| |<a href="https://drstearns.github.io/tutorials/gohandlerctx/">Sharing Values with Go Handlers</a>|
| |<a href="https://drstearns.github.io/tutorials/authentication/">Authenticating Users</a>|
| |[!!Exercise (postman)](https://github.com/info441/exercises/tree/master/postman)|
| 4/23 | REST APIs + Middleware |
| |<a href="https://drstearns.github.io/tutorials/gomiddleware/">Middleware Patterns in Go</a>|
| |<a href="https://drstearns.github.io/tutorials/rest/">REST APIs</a>|
| |[!!Exercise (middleware)](https://github.com/info441/exercises/tree/master/middleware)|
| 4/28 | Catch-Up + Project Bootstrap |
| 4/30 | Protecting Data Structures |			
| |<a href="https://drstearns.github.io/tutorials/mutexes/">Protecting Data Structures with Mutexes</a>|
| 5/5 | Node.js Microservices|
| |<a href="https://www.nginx.com/blog/introduction-to-microservices/">NGINX 7-Part article series on Microservices</a>|
| |<a class="inline_disabled"  href="https://youtu.be/5qJ_BibbMLw">Fast Delivery Talk</a> by Adrian Cockcroft|
| |<a class="inline_disabled"  href="https://youtu.be/1wiMLkXz26M">Migrating to Microservices Talk</a> by Adrian Cockcroft|
| |<a href="https://golang.org/pkg/net/http/httputil/#ReverseProxy">httputil.ReverseProxy</a>|
| |<a href="https://drstearns.github.io/tutorials/nodeweb/">Node.js Microservices</a>|
| |<a href="https://expressjs.com/en/starter/basic-routing.html">Express.js Basic Routing</a>|
| |<a href="https://github.com/mysqljs/mysql/blob/master/Readme.md">Node.js MySQL Driver Overview</a>|
| |[!!Exercise (microservices)](https://github.com/INFO441-19au-org/exercises-kylethayer/tree/master/microservices)|
| 5/7 | Message Queues |
| |<a href="https://www.rabbitmq.com/tutorials/tutorial-one-go.html">RabbitMQ Tutorial for Go</a>|
| |<a href="https://www.rabbitmq.com/tutorials/tutorial-one-javascript.html">RabbitMQ Tutorial for Node.js</a>|
| |[Use case: Asynchronous Tasks in Python with Celery and RabbitMQ](https://www.youtube.com/watch?v=fg-JfZBetpM)|
| 5/12 | Present / Review Proposals |
| 5/14 | Web Sockets |
| |[TALK: Real-life WebSocket Use Cases and Experiences](https://youtu.be/khULSvz_hdE)|
| |<a href="https://godoc.org/github.com/gorilla/websocket">Gorilla Web Socket Package</a>|
| |<a href="https://developer.mozilla.org/en-US/docs/Web/API/WebSockets_API/Writing_WebSocket_client_applications">Writing WebSocket Client Applications</a>|
| 5/19 | Concurrent Programming with Channels |
| |<a class="inline_disabled" href="https://www.youtube.com/watch?v=cN_DpYBzKso">Rob Pike on Concurrency is not Parallelism</a> (<a href="https://talks.golang.org/2012/waza.slide#1">slides from talk</a>)|
| |<a class="inline_disabled" href="https://www.youtube.com/watch?v=f6kdp27TYZs">Rob Pike on Go Concurrency Patterns</a> (<a href="https://talks.golang.org/2012/concurrency.slide#1">slides from talk</a>)|
| |<a href="https://www.golang-book.com/books/intro/10">Concurrency</a>|
| 5/21 | Homework Time ??? |
| 5/26 | Homework Time ??? |
| 5/29 | NO CLASS (day before Thanksgiving) |
| 6/2 | Homework Time ??? |
| 6/4 | Project Presentations!!! |-->


## Course Work

This course will be evaluated based on lecture exercises (10% of grade), 6 assignments (70% of grade), and a final project (20% of grade).

All assignments will be done individually or with one other person. You will turn in your own copy of the code.

The final project will be done in groups of 2-4 people. You will be graded on the code and on your role as a team member. We will evaluate your role as a team member based on the team's feedback and on our own observations. (If you are having any difficulty with your team, let us know early).

There is no final exam.


### Calculation of Final Grades

Canvas tracks grades on a percentage scale. To convert those to a 4.0 scale we will use [the standard iSchool conversion chart](https://faculty.washington.edu/dlsinfo/grading/grade-conversion-chart.pdf) (though we may curve up if grades in the course are too low). 

BTW: Canvas is already configured to calculate your final grade considering the previously described 90/10 grading weights and this conversion scale.

### Late Work / missing labs

To encourage you to keep on schedule with projects, we will deduct 10% of the possible points per 24-hour period that your submission is late, with a one hour initial grace period. For example, if the assignment is worth 100 points and your submission is between 1 and 24 hours late, the maximum you can receive on the assignment is 90 points. If your submission is between 24 and 48 hours late, the maximum you can receive is 80 points.

That said, we realize that sometimes life gets complicated and you might need a little extra time to finish a particular challenge. To give you a little flexibility you have 8 free late days that you can spend throughout the quarter. Each late day gives you a free 24-hour extension on the challenge. Unless you specify otherwise, we will use your late days for any work you submit late. After you exhaust all your late days, the normal late penalties will start to accrue.

Additionally we allow you to miss 2 of the lecture excersizes and still get full points on that portion of the grade.

If some additional difficulty occurs, please let us know and we can work out something.


## Course Rules

In addition to the standard [iSchool and UW academic policies](https://depts.washington.edu/infodocs/academic_policies/) that apply to all of our courses, the following rules also apply to this course.
