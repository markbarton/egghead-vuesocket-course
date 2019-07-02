### Vue and Socket.io for Real-Time Communication

This repo is to support the [Egghead.io course - Vue and Socket.io](https://egghead.io/courses/vue-and-socket-io-for-real-time-communication)

#### How to use this repo

Each folder corresponds to a specific lesson in the course.  

Each lesson might have both a `server` and `client` folder.  The `server` folder holds the express server files and the `client` folder holds the Vue application.

You will need to do an ```npm install``` inside both the `client` and server `folders`.

*** You will also need to install the [Vue CLI](https://cli.vuejs.org/) ***

I recommend you have 2 terminals open when you have both a server and client folder as you will need to run them both together.

##### Express Server
To start the Express application, make sure you are in the server folder and after installing the dependencies use `node server` in the command line.

If you get an error in the console which looks like this:

```
Papertrail connection error:  { Error: getaddrinfo ENOTFOUND HOST_HERE HOST_HERE:111
    at GetAddrInfoReqWrap.onlookup [as oncomplete] (dns.js:58:26)
  errno: 'ENOTFOUND',
  code: 'ENOTFOUND',
  syscall: 'getaddrinfo',
  hostname: 'HOST_HERE',
  host: 'HOST_HERE',
  port: 111 }
```

Then you can either safely ignore it, or update the [logger.js](https://github.com/markbarton/egghead-vuesocket-course/blob/8ef5d14b4a30323c3615930b857aaa242d56fed0/lesson1/server/logger.js#L16) values with your own [free papertrail account](https://papertrailapp.com/plans).

I have a lesson about logging with Papertrail and NodeJS [here](https://egghead.io/lessons/javascript-nodejs-logging-using-winston-and-papertrail).

For some lessons the Express server will host a static HTML file and this can be accessed in your browser at [http://localhost:8500](http://localhost:8500)

#### VueJS

The Vue application lives inside the client folder.  After you have installed the dependencies with an `npm i` then you can use the `npm run serve` command to start the VueJS development server which allows you to open the URL [http://localhost:8080](http://localhost:8080) - I recommend you open multiple browsers which point to this URL so you can see the application broadcasting in realtime to multiple clients.  I recommend you do not duplicate your browser tab as this can copy the sessionStorage values which can interfere with some of the lessons. 
