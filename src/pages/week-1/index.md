---
title: Week 1
date: "2018-11-09T10:46:37.121Z"
---

First Sprint Journal for Labs8

(https://github.com/Lambda-School-Labs/Labs8-TeamComms/pulse)

Github handle: Flintbean

Back-End: https://teamcomm2.herokuapp.com/ 
Front-End: https://team-comm.netlify.com/landing

# Part 1

The first week was a great experience. It was the first time I've had to work with a team on a project of this size. The first two days was spent coming up with ideas on how to implement the balsamic, and how we were going to build out the backend. The stack we were going to use was easy enough to all agree on. We all wanted to use a node backend with react and redux. The database is the only thing that we were up in the air about. We had only ever used a orm based db, so that seemed like the most likely choice. After a little research, however, mongo seemed like the best fit. It scales very well and allows us to be more flexible with the schema. Since none of us had used it before, it was a bit to learn but it ended up being a great choice. Boilerplating everything wasn't too bad. We had some problems with setting up dependencies, mainly eslint, that was causing merge conflicts. Our git workflow got a little jumbled in the first actual coding day, that was due in part to me. Establishing a structured gitflow is key, coordinating our pulls from master seems to work well. This is something I didn't do on the first day and I ran into some problems. All in all, a valuable learning experience. Deploying was rough for the back end. Deploying to heroku came with some extra challenges, since the repo has both the front and backend in it. With multiple package.jsons, we ran into problems very quickly while trying to deploy. After a bit of messing with it, we finally got it up and running. That was by far the hardest part(so far).

### Tasks Pulled

#### Front End

* Initialize React:
    * Github: https://github.com/Lambda-School-Labs/Labs8-TeamComms/pull/7
    * Trello: https://trello.com/c/UD5ceAgP/18-create-boilerplate-react-app
  
* Register User
    * Github: https://github.com/Lambda-School-Labs/Labs8-TeamComms/pull/14
    * Trello: https://trello.com/c/PkIsY6IH/35-register-user-function

#### Back End

* User CRUD routes
    * Github: https://github.com/Lambda-School-Labs/Labs8-TeamComms/pull/11
    * Trello: https://trello.com/c/Prc6FcQO/9-user-crud-routes

* Backend Initialize
    * Github: https://github.com/Lambda-School-Labs/Labs8-TeamComms/pull/4
    * Trello: https://trello.com/c/78Ot1Ajk/17-backend 


# Detailed Analysis

Deploying to heroku came with a heap of problems. It was running the wrong package.json so I had to only push the server directory up to the heroku master. After getting a merge conflict to the heroku master, I ended up getting rid of the deploy and starting a new one, where I only pushed the server directory up to it. Also configuring the port properly was something I forgot to do and I must have glanced over it in the heroku docs. Connecting the mlabs db was a breeze.


# Part 2- Milestone Reflections


We have a great group and everyone is willing to learn. We were all on the same page from the get go. I have a very specific interest in developing a solid back-end that is secure and reliable. This is my first tiem using mongo, and also my first time building a server of this scale, so im glad they deemed the backend responsibility to me. We had some back and fourth when it came to the user register and what kind of data we were going to require and send to the backend. While we spent a lot of time planning out the website in a broad scale, we didn't discuss the smaller details that were associated with some of the components. Was a small problem and easy to fix. Overall, a great learning experience