# communiteer-app
An app that brings together communities/community projects and volunteers behind a common goal. This repository is a work in progress mobile app that served as a final project at the Northcoders Bootcamp. Each member will continue to adapt the app as a personal project upon leaving the course.

Below is the original proposal and readMe which detailed some of the functionality we wanted to implement. This will be added to and edited as the project progresses.

The current deployed back end for the project can be found <a href="https://obscure-forest-52348.herokuapp.com/users/1">here</a>. A list of routes can be found in the readMe.

# Proposal

* The project is to create a mobile app tentatively titled "Communiteer"!. 

* It allows community groups (or people wanting to bring people together behind a common cause) to create a community of volunteers. 

* It should be just as applicable to a long running community group or as a quick set up reaction to an event that may require volunteers to offer something to the cause. 

## Basic Implementations
* User sign up.
* All Users will also volunteer.
* User will have a `Volunteer` section and a `Community Group Admin` section if they have created a group.
* User has a volunteer profile listing...
  * Skills/tasks they would volunteer for (could potentially include suggestions based on most common volunteering activities).
  * General location based on address.
  * Profile picture.
  * Ability to update this information at any time.
  * Track what community groups the User is a member of.
* User has the ability to create a `Community Group`. (this will make them the `Admin` of that community).
  * When User is an admin of a community they should have the ability to make other people admins.
    * User should be able to update the profile picture and banner of the community group
    * User should be able to create new `Projects/Events`.
    * Upon save the newly created project/event should notify each Volunteer that is matched to the project/event keywords supplied at creation of event
    * User should have the ability to update events and re-notify Volunteers who are signed up to the project/event.
* User as a Volunteer has the ability to search existing Community Groups and request to join.
* User notified when a project or task is listed that matches their skills.
* User has an "honour count" which tracks points they collect as they complete each project/task within the community.
  * This also updates if they recommend a friend to join up and that new volunteer goes on to participate.
* Admins will be able to recognise the work of the volunteers based on this honour system.
* Users as Volunteers can assign another Volunteer to a job if they can't fulfil their agreed role on a project/event.
* `Project/Event Page`
 * Once created the Project/Event Page will detail the event (timings/location/date), the skills required, show an event icon and background based on the community groups profile pic and banner.
 * Should be listed on the Community Group page so people can browse open Projects/Events.

## Extra Implementations
* Authentication and data privacy - log in passwords for Users
* The ability to message admins in real time. 
* Make suggestions to admins for activities the group could be undertaking. 

## Basic Routes/Requests

GET
api: '/areas' - Gets App areas
api: '/users' - Get all Users
api: '/skills' - Get app skills
api: '/users/:id' - Get Users by ID
api: '/groups/:id' - Get Groups by ID
api: '/groups/:id/events' - Get Group events by ID
api: '/areas/:id/groups' - Get Groups by Area
api: '/areas/:id/events' - Get Events by Area
api: '/events/:id' - Get Events by ID
api: '/users/:id/groups' - Get a Users Groups
api: '/groups/:id/users' - Get Users within Group
api: '/users/:id/events' - Get Users Events
api: '/events/:id/users' - Get Users within Event
api: '/users/:id/skills' - Get User Skills
api: '/events/:id/skills' - Get Event Skills
api: '/areas/:area_id/skills/:skill_id' - Get Users with particular Skill
api: '/users/:id/admin' - Get groups User is Admin of 

POST
api: '/users/:id/group' - Add Group
api: '/event' - Add Event
api: '/user' - Add User
api: '/users/:user_id/groups/:group_id' - Add User to Group
api: '/users/:user_id/events/:event_id' - Add User to Event

DELETE
api: '/user/:id' - Delete User
api: '/group/:id' - Delete Group
api: '/event/:id' - Delete Event

PUT
api: '/users/:id' - Update User 

## Extra Routes/Requests/Ideas

`Volunteer` -> `Community Group` (recommend a friend)

`Volunteer` -> `Live Message` -> `Community Group`

`Volunteer` -> `Community Group` -> `Activity/Project Suggestion`

`Volunteer` -> `Newsfeed (potentially drawing articles and data from other volunteering sources)` 

## Team

Leo, Kamran, Wasan and Ben.
