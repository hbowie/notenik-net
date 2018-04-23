# Notenik-net

## Table of Contents

* Title
	- [Notenik](1-title-notenik)
* Rights
	- [Rights and Authorship](2-rights-rights-and-authorship)
* Introduction
	- [The Problem](3-introduction-the-problem)
	- [A Modest Proposal](4-introduction-a-modest-proposal)
	- [A Bit of Inspiration](5-introduction-a-bit-of-inspiration)
	- [Mission](6-introduction-mission)
	- [Technology](7-introduction-technology)
	- [The Notenik Name](8-introduction-the-notenik-name)
* Conceptual Model
	- [A Conceptual Object Model](9-conceptual-model-a-conceptual-object-model)
* Objects
	- [Provider](10-objects-provider)
	- [Realm](11-objects-realm)
	- [Collection](12-objects-collection)
	- [User](13-objects-user)
	- [Group](14-objects-group)
	- [Access Rule](15-objects-access-rule)
	- [Note](16-objects-note)
	- [Tag](17-objects-tag)
	- [Stream](18-objects-stream)
* Attributes
	- [Stage](19-attributes-stage)




## 1. Title: Notenik

This is a proposal for a new platform for publishing and reading content located on the World-Wide Web. It arises out of a growing sentiment that other available options are too limiting. 


## 2. Rights: Rights and Authorship

Copyright (c) 2018 [Herb Bowie][hb]

This program, including its documentation, is free software: you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation, either version 3 of the License, or (at your option) any later version.

This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the GNU General Public License for more details.

You should have received a copy of the GNU General Public License along with this program.  If not, see [http://www.gnu.org/licenses/][gpl].

You can find the source code for this program at [github.com/hbowie/notenik-net][github]. 

[github]: https://github.com/hbowie/notenik-net
[gpl]: http://www.gnu.org/licenses/
[hb]: http://www.herbbowie.com


## 3. Introduction: The Problem

Let's consider a very simple, generalized system scenario. 

1. An author wants to write something. Let's just call this piece of content a note.  
2. The author may want someone else to read what s/he has written.  
3. The note may be intended for specific people, or for a more general audience, or for the author's eyes only. 
4. The author wishes to file the note in such a way that it can be referenced later. 
5. Readers wish to read notes in which they are interested. 
6. Readers may wish to comment on notes. 

This doesn't sound that complicated, does it? And yet, today, all of the following platforms -- often with multiple services and apps to choose from -- simply provide numerous variations on this same simple scenario:

1. Email 
2. Text messages
3. Facebook
4. Twitter
5. Blogging
6. Micro-blogging
7. Slack
8. Wikis
9. Notes
10. Reminders 

Even worse, despite the multiplicity of tools we have available to perform such a simple job, we commonly run into all of the following problems:

1. Spam -- content we receive that doesn't really interest us;
2. Misfires -- Messages that are never read by their intended audience;
3. Lost and Never Found -- Useful content that is difficult or impossible to find at some later point when it is really needed. 

So why do we have so many different ways of handling a single, simple scenario? Is it because users benefit from having so many different ways to do the same thing? Nah. Not really. And why do we continue to suffer from the same problems over and over? Because these problems are so complex and difficult to solve? I don't think so. 

Instead, I would argue that we have so many different tools, and we suffer regularly from the same recurring problems, for these reasons:

1. Reliance on older standards that don't entirely suit our modern needs; 
2. Reliance on companies with proprietary software and services that profit by making us part of a captive audience. 


## 4. Introduction: A Modest Proposal

So how can we improve our situation?

My proposal consists of three parts:

1. A new set of standards that will handle all of the common, modern variations on the basic scenario identified above;

2. Open-source server software that adheres to these standards and implements all of the common use cases;

3. A nonprofit organization to host and run at least one instance  of this software, and to help sponsor and guide the continued development of the software. 


## 5. Introduction: A Bit of Inspiration

According to a recent [article in The Guardian](https://www.theguardian.com/technology/2018/mar/11/tim-berners-lee-tech-companies-regulations), [Tim Berners-Lee](https://en.wikipedia.org/wiki/Tim_Berners-Lee) warned of "two myths" that "limit our collective imagination" when looking for solutions to the problems facing the Web: "The myth that advertising is the only possible business model for online companies, and the myth that it’s too late to change the way platforms operate. On both points we need to be a little more creative," he said.

This proposal is intended to address both of these issues. 


## 6. Introduction: Mission

This new platform will be mission-driven, rather than being profit- or growth-driven.

Our mission will be:

* To empower users as both content creators and content consumers;
* To inform, educate, entertain and persuade, while avoiding manipulation and deceit;
* To maximize transparency into all aspects of the platform's operation;
* To "smarten up" the content and platform for a group of interested users, rather than dumbing things down to reach as broad an audience as possible. 

If we are successful in achieving our mission, then we will have created a platform characterized by high levels of trust, as opposed to the low trust environments we currently have today. 


## 7. Introduction: Technology

No firm decisions have been made, and no code has been written yet, but I'm leaning towards the following technology choices for the server software:

* [MongoDB][mdb] -- This popular NoSQL document-oriented database program seems well suited to my intentions. 

* [Ruby on Rails][ror] -- This seems like a suitable language and framework to use for the server software. 

Client software can be written in any language, and may be proprietary or open-source. 

[mdb]: https://en.wikipedia.org/wiki/MongoDB

[ror]: https://en.wikipedia.org/wiki/Ruby_on_Rails


## 8. Introduction: The Notenik Name

I've owned three 'Notenik' domain names (.com, .org and .net) since 2014, and have had a 'notenik' repo on GitHub starting in that same year. 

The name has also been used to describe a desktop application written in Java that is conceptually similar in some ways, but otherwise different from what I'm proposing here. 


## 9. Conceptual Model: A Conceptual Object Model

Let's start our journey towards a new set of standards by outlining a conceptual object/entity model that would support our starting problem scenario and its common variations. 


## 10. Objects: Provider

A Provider is an organization or person that hosts an instance of the Notenik software and makes it accessible on the Web through a domain name owned by the Provider. 

Notenik is intended to be available from any number of Providers. In this sense, it is similar to email, and dissimilar from Facebook and Twitter. 

Each provider is responsible for its own sustainable business model. A provider may be a for-profit or a nonprofit. The provider may charge users for use of content stored by the provider. It may also charge users a fee for reading some or all of its content. 


## 11. Objects: Realm

Within the context of Notenik, a Realm exercises stewardship over the content that exists within that Realm. 

Each Realm is hosted by a particular Provider. 

A single realm may correspond to a single individual or an organization composed of multiple individuals. 

The Realm establishes the rules for ownership and licensing  of content created within that Realm, and the general rules for accessing its content. 

Each Realm will have a name and a path, with the path typically being based on the name. Both name and path must be unique within a Provider. 

As an example, let's say that I create a realm for Herb Bowie within the provider at notenik.net. So the path for this realm might be hbowie, resulting in a URL of notenik.net/hbowie. 

The null realm represents the realm of the provider. So Herb Bowie might also have a Notenik realm at the url hbowie.com. 


## 12. Objects: Collection

A Collection contains a number of Notes and/or other other Collections. 

A Collection is conceptually similar to a folder. 

Each Realm may contain a number of Collections. 

Each Note within a Collection must have an ID that is unique within that Collection. 

The Collection specifies the rules for forming the unique ID for each Note within the Collection. 

For example, the title of each Note could become its unique ID. In a different Collection, the date and time of creation -- or of publication -- could become the unique ID for each  Note. 

The ID will typically be formed from one or more attributes of each Note. 

A unique path for each Note will also be derived from its unique ID. 


## 13. Objects: User

A User is a person who is using the system in some privileged fashion (other than simply reading public content). 

Users post Notes. 

Each User is assigned a username that is at least unique to its hosting Provider, and optionally unique across all known Providers. 

The username is also used as a path for that User's Realm. 

Every user must have a Note titled About, containing a brief biographical profile of the User. The About Note, along with the user's name and general location (state/province and country, at a minimum), will always be publicly accessible, or at least accessible to all other Users on the same Provider, and should be truthful.

There should be a 1:1 relationship between a user and a living, breathing person. The system should strike a reasonable balance between privacy and transparency. We don't want a user's data to be misused, but we also don't want to see user accounts that cannot be tied back, in a singular way, to a real person. 


## 14. Objects: Group

A Group consists of a number of Users who all share a common set of access privileges. 

The Public Group implicitly consists of all possible users, whether authenticated or not.   

A Group is administered by one or more Users. An admin assigned to a Group is allowed to add Users to that Group and to remove Users from that Group.

Groups are created by Users, either explicitly or implicitly. An implicit Group is created whenever multiple Users are named as having access to a Note or a Collection. Implicit Groups are not assigned names. An explicit Group is created when a User assigns a new Group name. 

Each Group will exist within the context of a particular Realm. Each explicit Group's name must be unique within its Realm.  

A Group may optionally be identified as a subset of another Group. In this case, Users who are deleted from the larger Group will automatically be removed from the subset Group(s) as well. 

Users may be invited to join groups; however actual group membership is not created until a user consents to become a member of the group. 


## 15. Objects: Access Rule

An Access Rule specifies how a particular User or Group may access a Note, or a Collection of Notes. 

| Rule 		| Permitted actions 								|
| -------------| -------------------------------------------------------- |
| Read 		| The User/Group may read the Note only. 				|
| Follow           | The User/Group may read the Note, and wishes to follow changes/additions to the Note/Collection. |
| Respond 	| The User/Group may read the Note and post a new Note that replies to or comments on the original Note. |
| Act			| The User/Group may read the Note, and is expected to Respond to it. |
| Edit 		| The User/Group may read the Note and edit the Note, but may not delete or re-identify the Note. |
| Own 		| The User/Group may edit the Note, and may Delete/Re-ID the Note, and may assign other Access Rules to other Users/Groups. |

Note that implementation of an Access Rule requires consent by both the content owner and the User/Group gaining access (except for the case of the Public group). 


## 16. Objects: Note

A Note is a single piece of content. It can be thought of as conceptually similar to a post or a tweet.

A Note will generally have a body, a teaser, and a title. The body is required. If not specified, the title and teaser will be algorithmically generated from the body. 

The body and teaser would generally be specified using a specialized variant of Markdown. 

A unique path for each Note will be generated algorithmically from some combination of the note's title, author, resident domain, realm, owning collection(s), and date and time of creation. 

Each Note will have its own unique URL. 

Each Note may be revised one or more times, and each Revision may be assigned a Revision/Version identifier. 

A Note may be associated with another Note, as a comment or response. 

A Note may optionally have a Date associated with it. This may indicate the date on which some event will occur, or the date when an item will be due.


## 17. Objects: Tag

A Tag represents a particular topic or category. One or more Tags may be assigned to each Note. 


## 18. Objects: Stream

A Stream is a selection of recent content that is updated on a more-or-less continuous basis. 

A Stream is conceptually similar to a feed. 

Every Collection has a corresponding Stream of newly published/modified Notes. 

Each Stream consists of: 

* One or more inputs (either a Stream of changes to a particular Collection, or another Stream);
* Selection criteria;
* Prioritization criteria;
* Sequencing criteria;
* Presentation critiera, specifying an arrangement of attributes to be shown in the Stream for each Note.  

Each User may create new Streams, may select Streams, and may choose which Streams(s) they wish to view at any particular time. 


## 19. Attributes: Stage

Each Note will go through a lifecycle consisting of the following stages. There are no restrictions on how a Note progresses through these stages, although there is obviously an implied progression. 

* Draft -- Out for review, but not yet finalized. 
* Published -- Ready for consumption. 
* Completed -- All required actions have been taken. 
* Archived -- Only of interest for historical purposes. 
* Deleted -- Ready for deletion, or already deleted. 



