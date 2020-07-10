+++
author = "mtorials"
date = 2020-07-09T22:00:00Z
description = "Web technologies are getting more and more complex.This is how I found my way to this blog."
draft = true
tags = ["hugo", "blog", "webdev"]
title = "The difficulty of making a simple blog"

+++
## The start of mt32.net

### Wordpress? No!

When I first had the idea of creating a website to share my ideas and problems related to programming, I already knew of the most important rule for programmers for a long time: Don't reinvent the wheel! Of course I had heard of wordpress but I already had tried it out and neither the fact that it uses PHP nor the idea of selecting a simple theme for my project was a plus point for me at the time.

### Headless CMS

Because I wanted to write my own frontend or at least my own layout and style, I searched for an headless content management system (headless CMS). I also wanted to use GraphQL instead of a standard RESTful API. In retrospect this was not a very smart requirement, because my idea of a blog does not really need the benefits of GraphQL. Also it was very hard to find a production ready headless CMS with GraphQL support. After trying various CMSs without ever being happy with one I decided that it can not be so hard to write my own backend.

### Reinventing the wheel

At this point I knew I was writing everything myself. This normally never is the best solution for any given problem that already has been solved thousands of times (in case of blog., But I thought I would maybe learn something along the way and have some fun writing my blog.

### Version 1

The first and finished version of this page was a overengineered website with login, comment section and menus. Written in JavaScript with Node and Prisma, a language and framework I do not know well, as well as Vue for the frontend, the software ran but the codebase was more than ugly. But I was using a GraphQL API!

Ok, I was not actually using it. After programming this for months I tried to deploy it and I failed.