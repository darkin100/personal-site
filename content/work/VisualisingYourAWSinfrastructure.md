---
title: "Visualising your AWS infrastructure"
date: 2016-05-30
tags: [ "aws", "architecture"]
draft: false
---

Building out an AWS infrastructure can get pretty complicated as there are many different elements and dependencies that need to be considered. Visualising the relationships is a great way to understand all the dependencies involved, however the existing tools may create results that were not exactly expected. The visualisations that I have been using are based on my Cloud Formation scripts. These are static JSON files that AWS uses to build out the architecture. The first tool that I used to help visualise the script was Cloud Formation Viz. Its a simple command line tool that can draw out the different components and relationships.
The below diagram is of a single EC2 instance.



This was a pretty simple Cloud Formation Script, but already you can see how complicated its starting to get!!!!
The second image is of a multi EC2 instance VPC.



Now we really start to see how complex architecture is!!! In reality though you need something like this to keep track of what you are building and how it all hangs together!!!

AWS CloudFormation has a builtin designer which visualises your cloud formation scripts, however this requires you to be editing your templates in the online designer. The benefits are you get template validation, however its difficult to tie the designer into a proper devops style workflow.

The below is the AWS visualisation of the single EC2 instance VPC taken as a screenshot.



The following is of the more complex multi instance VPC



What both of these solutions has in common is that they represent the architecture as a graph diagram rather than a what we would expect of a traditional architecture diagram. Typically people expect some thing like the below. (I used Lucid Chart)



The above is much more easily recognised as an Architecture diagram, but the reality is that its an abstraction and pov of an architecture. Its a much more digestible format for communicating your architecture.

Summary
Tooling is not great in this area and depending on your audience you will get very different results from handcrafting to auto-generating. At the moment for me I will be using both methods for tracking change and communicating my designs.



[go]: <http://golang.org/>
[gohtmltemplate]: <http://golang.org/pkg/html/template/>
