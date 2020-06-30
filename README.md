# Dio Script Cheat Sheet
Cheet Sheet for Dio Script.

##  Hello World

Let's Start with something simple

```javascript
; This is a comment, comments do not affect the app. They are just for programmers to know what is going on
include dio ; this is a libary, you do not have to include dio but it will add more features

new command hello() {
  message send "Hello World!"
 }
 
 ```
 
 ## Cheat Sheet
 
 ### Commands
 ```javascript
 include dio
 
 new command Ping(dio.ping ;dio.ping is a part of the dio libary) {
        message send "Pong: {dio.ping}" replace "{dio.ping}" with dio.ping
 
}
```
### Events
#### onMemberJoin
```javascript
include dio

new event onMemberJoin(member as dio.Member) {
      message send "{member.mention} has joined!" replace "{member.mention}" with member.mention
      ;  Output: @Example#0000 has joined!
      member.add_role("TEST", member) ;Auto-Role
}
```
#### onMemberLeave
```javascript
include dio

new event onMemberLeave(member as dio.Member) {
      message send "Good bye {member.mention}... we will miss you" replace "{member.mention}" with member.mention
}
```
### Dio Libary

#### dio.ping
Returns the Ping of Dio in ms
```javascript
 include dio
 
 new command Ping(dio.ping ;dio.ping is a part of the dio libary) {
        message send "Pong: {dio.ping}" replace "{dio.ping}" with dio.ping
 
}
```
##### dio.ping.Seconds
Returns the ping of Dio in Seconds.
```javascript
 include dio
 
 new command Ping(dio.ping ;dio.ping is a part of the dio libary) {
        message send "Pong: {dio.ping.Seconds}" replace "{dio.ping.Seconds}" with dio.ping.Seconds
 
}
```

#### dio.Member
A member object
##### dio.Member.add_role()
PARMS: ROLE, MEMBER OBJECT
Adds a role to a member object
```javascript
include dio

new event onMemberJoin(member as dio.Member) {
      message send "{member.mention} has joined!" replace "{member.mention}" with member.mention
      ;  Output: @Example#0000 has joined!
      member.add_role("TEST", member) ;Auto-Role
}
```
##### dio.Member.GetDiscordTag()
PARMS: SPLIT
SPLIT is what character do you want to split it on. For Example if you do # on @Example#0000 you will get 0000. If left as None then it will send the entire thing. If set as <# it was only return the username.
Gives the ID of the user
```javascript
include dio

new event onMemberJoin(member as dio.Member) {
      member.GetDiscordTag('#')
}

```
