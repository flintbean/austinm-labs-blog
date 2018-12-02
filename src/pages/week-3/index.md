---
title: Week 3
date: "2018-11-30T10:46:37.121Z"
---

Third Sprint Journal for Labs8

(https://github.com/Lambda-School-Labs/Labs8-TeamComms/pulse)

Github handle: Flintbean

Whiteboard: (https://youtu.be/_XIVk6Un0lc)

Back-End: https://teamcomm2.herokuapp.com/ 
Front-End: https://team-comm.netlify.com/landing

# Part 1

Third week went pretty well. This week was fully implementing socketio. JJ layed down a solid foundation with getting the core websocket functionality working. My job was to connect this to our mongodb. At the beginning of the week we were using two collections. Our user collection, which keeps all of the information about our user. Then we had our meeting collection, which held all of information about our meeting. My first run through with websockets consisted of connecting it to the "meeting" collection. This worked fine and I had it working within the first day. However, since data was constantly being updated with sockets and properties were constantly changing(questions, people in the meeting, notes), our collection was gigantic after the meeting. Which seemed like it would cause a lot of trouble down the road. In my mind, it seemed like adding another collection that held all the info from the meeting once it went live was going to be more maintanable and better for us down the road. 

### Tasks Pulled

#### Front End

* Create conversation data set up
    * Github: https://github.com/Lambda-School-Labs/Labs8-TeamComms/pull/63
    * Trello: https://trello.com/c/c3TE0iVk/57-create-conversation-function
  
* Socketio
    * Github: https://github.com/Lambda-School-Labs/Labs8-TeamComms/pull/69
    * Trello: https://trello.com/c/vhpBseQ7/56-socket-fix

#### Back End

* Convo retrieve
    * Github: https://github.com/Lambda-School-Labs/Labs8-TeamComms/pull/51
    * Trello: https://trello.com/c/hEuwfWLl/68-convo-retrieve

* Socketio
    * Github: https://github.com/Lambda-School-Labs/Labs8-TeamComms/pull/69
    * Trello: https://trello.com/c/vhpBseQ7/56-socket-fix


# Detailed Analysis

I refactored and ran into a few new challenges while connecting the db to my sockets. I realized that this new "livemeeting" collection needed to be connected with the meeting schema, and to do this properly, I had to create a livemeeting document on the creation of the meeting. My first idea, which was to create the livemeeting document when the meeting started. I quickly realized this was going to be a problem, because with each user connect, they were creating a new livemeeting document everytime. So once I created the livemeeting document properly, things went a lot smoother. There is still some bugs to work out and we are hoping to have those fleshed out by next week.

# Part 2- Milestone Reflections

Modularizing code is the key to success when working in groups. It allows people to work on the same component by using different files and connecting these files when it is finished. The websockets needed multiple parts to sync up to be able to get them working properly. The endpoint that created the meeting needed to have the right data being sent from the front end to be able to create our meeting and livemeeting documents. We also needed the models for each of these collections to be set up correcetly to recieve this information. Tristan set up the conversation create endpoint and tweaked the conversation model to allow the livemeeting(socket) collection to hook up with its paired meeting. Jameson set up the conversation create and set up all the information we were going to need for both of those. This was all happening while JJ was writing the websocket functionality then I was able to go in and connect it to the DB. There was some trial and error, especially after playing with sockets and seeing what was actually going to be needed. So that had to be communicated with the team so each person could make changes in accordance.