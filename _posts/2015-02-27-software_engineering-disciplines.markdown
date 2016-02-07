---
layout: post
title:  "Software engineering disciplines"
date:   2015-02-27
categories: process, team
---

*Software development* is a creative process and requires discipline in various
topics in order to deliver great products. We can split the disciplines into
two different categories: developer-related and manager-related. The blue
topics are in charge of the management which needs to take care that those are
implemented properly. However, the orange topics need to be handled by the
individual developers. Both sides are required for a proper development
environment.

![]({{site.url}}/assets/disciplines.png)

# Management

## Development process and methodology

A solid development process is required to plan and execute a project plan.
Nowadays, agile and lean methodologies like Scrum or XP are common and help to
overcome difficulties by constant change of requirements during project
execution.

##  Source code guidelines

Yes - every developer has his/her coding style. However, a minimal set of
guidelines should be in place (at least for one product), which raises
readability of the code. There are some tools which help to keep the code in
good shape (e.g. astyle).

##  Requirements engineering

Every product has requirements. We should first start thinking of what does the
customer want before starting to code. If doing the other way around, lot of
code is produced, which may not be used later. Solid requirements engineering
is a must for delivering the right product.

##  Issue tracker

The simplest issue tracker is one which tracks your todos or bugs. However, in
agile development, complete requirements, and features are defined, and issue
tracker platforms are used for planning and tracking your complete work.

##  Content management system

Besides the source code itself, documentation of processes, guidelines and best
practices must find their place. The best solution is to setup a small WIKI or
CMS (content management system) which allows the team (and especially new
hires) to exchange information and knowledge.

##  IRC

If a team is not co-located, it may be necessary to provide an environment of
quick chats. In their daily work, developers quickly need to resolve issues by
talking to other team members. The most efficient way, in my opinion, is to
have an open chat window open and type the question in. Especially useful if
more developers are involved. For a peer-to-peer communication, a phone call
may be the preferred way to go.

# Development

##  Software architecture

Before getting into software design, a solid overall software architecture is
mandatory to lay out the foundation of your product. Flaws in the architecture
are hard to fix later.

##  Software design and patterns

Software design is one of the most creative tasks. A wide variety of design
patterns help to build your software system the right way. However, they can
only be a guide, and not a silver bullet.

##  Source code management

Your source code is your IP (intellectual property). For a software company,
the source code is - beside the team itself - its highest value. A good source
code must also be maintained and kept in good shape. This is not something
which is done automatically, but takes time and effort.

##  Build environment and configuration management

How can you make sure that your code is doing the right thing? Yes, having
tests in place. However, before that, you have to make sure that your code
builds and does not show any build breaks. Talking about cross-platform
development, a build environment which is able to produce cross platform build
scripts is inevitable. One popular environment is `cmake`.

##  Code reviews

In my opinion, code reviews are mandatory. Before checking in your code, at
least another developer needs to sign off. There are some good tools available
which also allow to perform code reviews for not co-located teams (e.g.
    web-based).

##  Software testing

Talking about software testing, a lot of developers are rolling eyes and think
that this is useless, and only distract from the "real" work. However, if you
understand the benefits of software testing, and lean about test driven
development (TDD) and its colleague behaviour-driven development (BDD), you
will soon experience that testing helps to build the right thing from the
beginning.

##  Continuous integration

Daily builds is the minimum a software development team should have. However,
we may also think of extending this by having continuous testing and
deployment. There are some continuous integration systems available, which help
to deliver your product to customers on a regular and structured basis.

This list should carefully be reviewed in order to identify blind spots. If you
need support, feel uncomfortable in one of those topics, or want to analyse the
health of your software development performance, do not hesitate and contact
us.
