# What is DevOps?

Before we get started with Docker let’s lay the groundwork for learning the right mindset. Defining DevOps is not a trivial task but the term itself consists of two parts, Dev and Ops. Dev refers to the development of software and Ops to operations. Simple definition for DevOps would be that it means the release, configuring, and monitoring of software is in the hands of the very people who develop it.

A more formal definition is offered by Jabbari et al.: “DevOps is a development methodology aimed at bridging the gap between Development and Operations, emphasizing communication and collaboration, continuous integration, quality assurance and delivery with automated deployment utilizing a set of development practices”.

![DevOps](https://upload.wikimedia.org/wikipedia/commons/0/05/Devops-toolchain.svg)

Sometimes DevOps is regarded as a role that one person or a team can fill. Here’s some external motivation to learn DevOps skills: Salary by Developer Type in StackOverflow survey. You will not become a DevOps specialist solely from this course, but you will get the skills to help you navigate in the increasingly containerized world.

During this course we will focus mainly on the packaging, releasing and configuring of the applications. You will not be asked to plan or create new software. We will go over Docker and a few technologies that you may see in your daily life, these include e.g. Redis and Postgres. See StackOverflow survey on how closely they correlate these technologies.

## Exercises

### 1.1: Getting started
Since we already did “Hello, World!” in the material let’s do something else.
Start 3 containers from image that does not automatically exit, such as nginx, detached.
Stop 2 of the containers leaving 1 up.
Submit the output for docker ps -a which shows 2 stopped containers and one running.

### 1.2: Cleanup
We’ve left containers and a image that won’t be used anymore and are taking space, as docker ps -as and docker images will reveal.
Clean the docker daemon from all images and containers.
Submit the output for docker ps -a and docker images

### 1.3: Secret message
Now that we’ve warmed up it’s time to get inside a container while it’s running!
Image devopsdockeruh/simple-web-service:ubuntu will start a container that outputs logs into a file. Go inside the container and use tail -f ./text.log to follow the logs. Every 10 seconds the clock will send you a “secret message”.
Submit the secret message and command(s) given as your answer.

### 1.4: Missing dependencies
Start a ubuntu image with the process sh -c 'echo "Input website:"; read website; echo "Searching.."; sleep 1; curl http://$website;'

You will notice that a few things required for proper execution are missing. Be sure to remind yourself which flags to use so that the read actually waits for input.

> Note also that curl is NOT installed in the container yet. You will have to install it from inside of the container.
Test inputting helsinki.fi into the application. It should respond with something like

```<html>

<head>
  <title>301 Moved Permanently</title>
</head>

<body>
  <h1>Moved Permanently</h1>
  <p>The document has moved <a href="http://www.helsinki.fi/">here</a>.</p>
</body>

</html>
``` 
This time return the command you used to start process and the command(s) you used to fix the ensuing problems.

> This exercise has multiple solutions, if the curl for helsinki.fi works then it’s done. Can you figure out other (smart) solutions?



