---
title: Week 2
date: "2018-11-16T10:46:37.121Z"
---

Second Sprint Journal for Labs8

(https://github.com/Lambda-School-Labs/Labs8-TeamComms/pulse)

Github handle: Flintbean

Back-End: https://teamcomm2.herokuapp.com/ 
Front-End: https://team-comm.netlify.com/landing

# Part 1

This week we implemented web sockets, stripe, and Oauth. Oauth was what I mainly worked on and it proved to be pretty difficult. Connecting the client request to our server, then hitting the google api, extracting the user information from google and redirecting that information to another endpoiint to pass the client the token was a dauntful task. When I was first trying to wrap my head around the order of the process, I was having a hard time. I had to watch some videos and go through a lot of trial and error. Eventually I figured it out and now everything makes a lot more sense. Another thing I had to do was create a end point on the server to retrieve user information by getting the id out of the token passed in through the end point. That was the final step to completion.

### Tasks Pulled

#### Front End

* Implement OAuth
    * Github: https://github.com/Lambda-School-Labs/Labs8-TeamComms/pull/32
    * Trello: https://trello.com/c/WPGQg8AE/51-oauth
  
* OAuth token put in storage and user info sent back to client:
    * Github: https://github.com/Lambda-School-Labs/Labs8-TeamComms/pull/41
    * Trello: https://trello.com/c/WPGQg8AE/51-oauth

#### Back End

* Userinfo retrieve
    * Github: https://github.com/Lambda-School-Labs/Labs8-TeamComms/pull/40
    * Trello: https://trello.com/c/WPGQg8AE/51-oauth

* OAuth implement
    * Github: https://github.com/Lambda-School-Labs/Labs8-TeamComms/pull/32
    * Trello: https://trello.com/c/WPGQg8AE/51-oauth

# Detailed Analysis

Using google Oauth was easy to do once playing around with it for a bit. The hardest part about it was finding out what to do with the user once they passed the google login. We needed to create a token for them and set it on their local storage. I tried to find a solution by strictly using the backend. This proved too difficult so we ended up just redirecting to our dashboard with the token in the URL and pulling that down into storage.

# Part 2- Milestone Reflections

Oauth was a great goal to push for. It was such a priority that I put in a lot of time getting it to work, because of that, I learned a lot about the process. After reaching the solution we did, I also notice other sites pulling tokens down from their url's into local storage after signing in through Oauth. That was interesting to see. We hit MVP pretty easily, though we didn't have sockets too fleshed out. That will be another challenge for us next week.