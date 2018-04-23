Title:  Group

Type:   Objects

Seq:    14

Date Added: 2018-03-21 15:37:23

Body:   
 
A Group consists of a number of Users who all share a common set of access privileges. 

The Public Group implicitly consists of all possible users, whether authenticated or not.   

A Group is administered by one or more Users. An admin assigned to a Group is allowed to add Users to that Group and to remove Users from that Group.

Groups are created by Users, either explicitly or implicitly. An implicit Group is created whenever multiple Users are named as having access to a Note or a Collection. Implicit Groups are not assigned names. An explicit Group is created when a User assigns a new Group name. 

Each Group will exist within the context of a particular Realm. Each explicit Group's name must be unique within its Realm.  

A Group may optionally be identified as a subset of another Group. In this case, Users who are deleted from the larger Group will automatically be removed from the subset Group(s) as well. 

Users may be invited to join groups; however actual group membership is not created until a user consents to become a member of the group. 


