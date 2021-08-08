---
layout: post
title:  "Let's Make a Wireless Fencing System"
date:   2021-08-08 21:50:00 +0100
tags: fencing embedded
---
For some time I've been thinking about challenging myself to produce a complete (wireless) system. The project is meant to be a place for me to experiment with purpose, trying out some technologies with an end application, and to scratch a few mental itches. I'm hoping that along the way they'll be a few blog posts to try and explain a little more of my thought process along the way.

## Fencing - a brief introduction to a wired world

Fencing (the sword-fighting sport, not the things around a field) requires a lot of equipment for both competitors and clubs/venues. Recording hits on the opponent is based on detecting an electrical circuit between the one fencer's weapon and a conductive part of their clothing. Depending on the weapon, scoring points is dependent on which part of the weapon hits the opponent. This electrical circuit relies on the fencers connecting to a reel of cable at each end of the piste (the playing surface), which in turn is connected to the Scoring Box by yet more wires.

![A fencing match with the body cord connected to the wire spool](https://upload.wikimedia.org/wikipedia/commons/1/10/Final_Trophee_Monal_2012_n08.jpg "Two fencers")
The wire connecting the fencer on the right can be seen. Image [© Marie-Lan Nguyen / Wikimedia Commons / CC-BY 2.5](https://en.wikipedia.org/wiki/Fencing)

These wires provide a simple solution for sending electrical signals, but each part of the system requires maintenance, and for clubs hiring sports halls it takes time to setup and clear away this equipment.

## A wireless setup - main goals

This project has a few meta-goals that I want to achieve:
-   Have some fun.
    
    This is meant to be a hobby project. I'm not planning to leave `$DAY_JOB` to make my fortune on this.
-   Learn some new technologies.

    There's a few things (both hardware and software) that I'd like to try using. This seems like a good application.
-   Make something physical

    I really enjoy doing board bring up (and schematic review with an embedded engineer's hat on as well).

## Wait, what do you are you actually doing?

Oh yes, I haven't really got to that yet. I'd like to create a wireless scoring system for fencers that could be affordable for smaller clubs/societies. The 'system' comprises of just two logical components:
1.  The Fencer's Beltpack

    In a wired system each fencer's body cord is connected to the Scoring Box via a spool of wire. In a wireless system we can replace the spool (costing hundreds of pounds) with a beltpack. 

2.  Scoring Box

    This records the score during a match. Entry-level Scoring Boxes only indicate whether a hit has been made, whereas more advanced boxes display timings for a match, each players total points, and timing information on the match. Scoring Boxes often have a handheld remote used by the referee for control.
