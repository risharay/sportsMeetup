# sportsMeetup

## Table of Contents
1. [Overview](#Overview)
1. [Product Spec](#Product-Spec)
1. [Wireframes](#Wireframes)
2. [Schema](#Schema)

## Overview
### Description
This app lets you have fun with sports you enjoy, while also meeting new people. It allows you to choose a particular sport and team up with people nearby.

### App Evaluation
- **Category:** Social Networking
- **Mobile:** This is developed for mobile due to its efficiency and accessibility, but its functions can also be transfered over to a website application as well.
- **Story:** Allows users to select groups and meetup with people beased on location and sport specification. 
- **Market:** Any individual interested in sports can use this app.
- **Habit:** This app can be used anytime based on the user's liking and preference for a particular sport. 
- **Scope:** It will start off with a few people, but once the users grow it will allow for a better interaction/matching among users based on the type of sport and location. 

## Product Spec

### 1. User Stories (Required and Optional)

**Required Must-have Stories**

* User can sign up.
* User can login.
* User can choose sport.
* User can choose location.
* User can form/join a team.
* Profile pages for each user
* Settings (Accesibility, Notification, General, etc.)

**Optional Nice-to-have Stories**

* User can choose location from map.
* User can add friends.
* User can rate location.
* User can use app as a guest.

### 2. Screen Archetypes

* Login
* Register
* Profile Screen
* Start a Game Screen - User can choose their preferences/sport.
* Select a Team Screen - User sees a list of teams and choose one.
* Settings Screen

### 3. Navigation

**Tab Navigation** (Tab to Screen)

* Profile 
* Game
* Settings

**Flow Navigation** (Screen to Screen)

* Forced Log-in -> Account creation if no log in is available
* Profile -> Settings

## Wireframes
<img src = "Screen Shot 2020-04-16 at 1.43.44 PM.png">
<img src = "Screen Shot 2020-04-16 at 1.43.50 PM.png">
<img src = "Screen Shot 2020-04-16 at 1.45.46 PM.png">

* Story Board Preview
<img src="Screen Shot 2020-04-15 at 8.07.06 PM.png">


## Schema 

### Models
User
| Property  | Type    |Description |
| ------------- | ------------- | -------- |
|  userId | Number  | unique id for the user |
| username | String  | unique username for the user |
| profilePic | File | profile picture for the user |
| bio | String | profile description for the user  |

Game 
| Property  | Type    |Description |
| ------------- | ------------- | -------- |
| location | String | location of the meetup place |
| gameId | Number | unique id for game|

Team 
| Property  | Type    |Description |
| ------------- | ------------- | -------- |
| teamId | Number | unique id for team |
| noUsers | Number | number of users in the team |



### Networking
List of network requests by screen

Profile Screen
(Read/GET) Query logged in user object
(Update/PUT) Update user profile image

Base url: https://www.yelp.com/developers

| HTTP  | Endpoint  |Description |
| ------------- | ------------- | -------- |
| GET | /businesses/search | search businesses|
| GET | /location | The location of this business, including address, city, state, zip code and country.|
|GET |/photos | URLs of up to three photos of the business.|

