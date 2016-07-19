---
layout: post
title:  "parse-server and auth0 integration"
date:   2016-07-19 10:00:00 +0200
categories: "parse-server auth0"
author: "Adrian Brink"
---
At avogenie.com we are currently building an iOS client that rest on top of a combination of technologies such as firebase and the open-source parse-server. As such I had to figure out how to authenticate users in a way that allows for easy integration with external services such as firebase, parse-server and layer.com.

I decided to use auth0.com to handle the user management for now, because they have a very nice iOS SDK and have endpoints for issuing JWT tokens through an API call. However, the issue with the parse-server is that I didn’t want to write a custom oAuth integration but somehow needed a way to establish a user identity on our parse-server that can be referenced to from auth0.

After numerous days of scouring the internet for solutions I realised that there is no definitive guide on how to do this, but eventually I figured it out.

# The Guide

I am assuming that you have your parse-server running on heroku.com (I guess other providers should behave the same) and that you setup auth0.com to properly work with your iOS app (or other tech, they have pretty decent guides on most things). The important thing is that a user needs to be able to log in and show up in the auth0 dashboard.

Now the trick to get auth0 to work with parse-server is to create this rule.

Since I am converting my blog to jekyll the rest will follow later.
