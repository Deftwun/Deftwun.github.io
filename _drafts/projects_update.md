---
title: June Update
layout: post
date: {}
published: true
---
##Job
Time to fix up the resume and start the search. I'm determined to get a developer job. I'm sure it's not going to be easy but I'm feeling confident. Developing software is what I enjoy doing in my spare time so it just makes sense that I need to be doing this for a living. 

##Side-Projects
Lots of stuff I could potentially be working on but haven't been. There was a knitting app design tool I was making for the wife. Not sure where I left off on that but I remember it was coming together ok. Also want to try and develop some smaller simple apps for the android store using some type of html5/js framework. I want to see what type of result you can get when using web technologies instead of something like android studio. While I like Java, I've been spending a lot more time with javascript lately.

##Game
I've been working on this multiplayer game using node, socket.io, matterjs, and Pixijs. So far it's coming together pretty well. I'm trying to focus on just the game and not get carried away on 'engine' features.  [ZombieCopter](https://github.com/Deftwun/ZombieCopter) pretty much turned into a full on engine to that point that the game was a little lost. Now that I'm trying to live in Javascript land I'm trying to utilize the features of JS that let you just get things done. 

So far I think I'm only ~2-3 weeks in working on it here and there. Just finished getting sprites & rendering working. Eventually I'd like to put on heroku or something similar and see how it holds up. Lots of stuff to do first though.

![tankgame.jpg]({{site.baseurl}}/_drafts/tankgame.jpg)

It's pretty interesting to try and build a game like this. With the client/server model you need to have 2 seperate versions of the same physics world running at once. Then the client will periodically sync all body positions,angle,etc.. with the ones on the server. So lots of fun weird things to go wrong. I'm a little skeptical that my current setup will hold up in the real world but we'll see how it goes. Running the server locally 
seems to work surprisingly well.

###Things I'm thinking about
- Try and Keep entities data based
- Should I Scale sprites to fit physics object size?
	- Physics objects hava a bounds property that could define width/height
    - Allow for more flexibility with entity sizes
    - Some objects might need a tiled sprite instead of a scaled sprite.. where is this defined/set?
- Entities constructor should use an options object instead of regular args
	- This is where sprite scaled/tiled property exists
    	- This means Actor will need to be a member of Entity. Should be anyways really. Keep all entity setup/config in one file.

##FreecodeCamp
Need to get back on track and finish up back end development certification. I've finished all the api project a few months back and then took a break. I'll need to brush up on my express/passport knowledge though. [Things can get pretty hairy when you go the DIY route](https://www.youtube.com/watch?v=yvviEA1pOXw). I have a feeling there are preconfigured frameworks/templates available though that handle alot of the user authentication/authorization setup for you.

These are the apps I still need to build to get the certification. A bit daunting as a whole but I think they could all share a lot of the same code. I should focus on getting a basic app with authentication setup first though. That is one thing they all will definitely need. 

- [ ] [Voting app](https://www.freecodecamp.com/challenges/build-a-voting-app)
- [ ] [Nightlife coordination app](https://www.freecodecamp.com/challenges/build-a-nightlife-coordination-app)
- [ ] [Chart stock market](https://www.freecodecamp.com/challenges/chart-the-stock-market)
- [ ] [Manage a book trading club](https://www.freecodecamp.com/challenges/manage-a-book-trading-club)
- [ ] [Build a pinterest clone](https://www.freecodecamp.com/challenges/build-a-pinterest-clone)


