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
}
```
#### onMemberLeave
```javascript
include dio

new event onMemberLeave(member as dio.Member) {
      message send "Good bye {member.mention}... we will miss you" replace "{member.mention}" with member.mention
}
```
