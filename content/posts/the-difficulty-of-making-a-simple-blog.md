+++
author = "mtorials"
date = 2020-07-10T22:00:00Z
description = "Web technologies are getting more and more complex. This is how I found my way to this blog."
tags = ["hugo", "blog", "webdev"]
title = "The difficulty of making a simple blog"
draft = false
+++
# The start of mt32.net

## Wordpress? No!

When I first had the idea of creating a website to share my ideas and problems related to programming, I already knew of the most important rule for programmers for a long time: Don't reinvent the wheel! Of course I had heard of wordpress but I already had tried it out and neither the fact that it uses PHP nor the idea of selecting a simple theme for my project was a plus point for me at the time.

## Headless CMSs

Because I wanted to write my own frontend or at least my own layout and style, I searched for an headless content management system (headless CMS). I also wanted to use GraphQL instead of a standard RESTful API. In retrospect this was not a very smart requirement, because my idea of a blog does not really need the benefits of GraphQL. Also it was very hard to find a production ready headless CMS with GraphQL support. After trying various CMSs without ever being happy with one I decided that it can not be so hard to write my own backend.

## Reinventing the Wheel

At this point I knew I was writing everything myself. This normally never is the best solution for any given problem that already has been solved thousands of times (in case of blog., But I thought I would maybe learn something along the way and have some fun writing my blog.

## Version One

The first and finished version of this page was a overengineered website with login, comment section and menus. Written in TypeScript with Node and Prisma, a language and framework I do not know well, as well as Vue for the frontend, the software ran but the codebase was more than ugly. But I was using a GraphQL API!

Ok, I was not actually using it. After programming this for months I tried to deploy it and I failed. I did not know how to use docker properly but I had to use it for Prisma and the database. Also setting up my node project for deployment on my virtual server (VPS) was harder then I thought it would be. The extra step from TypeScript to JavaScript did not help there either.

## Hugo

After too much frustration about not being able to easily deploy an already finished website I suspended this project. I never liked the idea of using the JavaScript ecosystem and my terrible code for the final website anyway. But I did not plan on giving up completely.

When I discovered Hugo by coincidence I was interested, because it neither is a CMS in the traditional way nor has it the need for an API and JavaScript/AJAX on the frontend to work. It instead is a static side generator. It renders the whole website before you deploy it. That does mean that static side generator are not suited for use cases in which you have to update your content regularly. But in case of a blog this not necessary. You only have to deploy the website when you post something new.

Also Hugo does not rely on the JavaScript ecosystem and to write my own theme I only had to learn a few lines of the Go HTML Templating Language and not a whole JavaScript framework.

## Continuous Deployment

Having to upload the newly rendered website via FTP every time you change something is a bit tedious and an argument against a solution like this. But when I learned Netlify has an integration for Hugo I decided to give it a try.

Netlify is a tool to deploy websites easily. You just have to connect it to a Git repository, done. After logging in with my already existing GitHub account I was able to deploy my Hugo website I made with exactly two commands a few minutes earlier. And on every commit Netlify builds and updates the website. Although I really like my VPS running Nginx I found this way of getting your own website up stunningly fast and easy.

> The fastes way to build the fastest sites

...was not an overstatement by Netlify in my case. Especially together with Hugo, the 

> The world’s fastest framework for building websites.

## Conculsion

Eventually I sticked to this method and I am very happy about it. The integration with GitHub is great and works like a universal interface to work together with other apps like [Forestry](https://forestry.io/). It is super convenient! I can write new articles with every device and the chages will be online only second later. There are definitely other solutions that can work better in other use cases, but for me this seems like the best one! 


## Update

I'm running this blog on my VPS now automaticly build and deployed with the Gitlab CI.