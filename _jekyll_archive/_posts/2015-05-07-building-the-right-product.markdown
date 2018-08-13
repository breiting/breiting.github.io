---
layout: post
title:  "Are you building the right product?"
date:   2015-05-07
categories: testing
---

Software engineering is fun, no doubt. Developers - including me - often tend to build things from bottom up, because they feel save in their development environment and exactly know how to solve a problem or develop a certain feature. When it comes to product development, bottom up approaches partly make sense but have to be aligned with the bigger picture and the final product. How can you make sure that you build the right product which fits the customers’ needs and is inline with the general business goal? In an agile team, the product owner is responsible for collecting and identifying requirements together with stakeholders in order to let the team develop the right features. But how can you test high level features so they fit the needs of the customers?

I recently stumbled upon a methodology called behaviour-driven development
([BDD](http://guide.agilealliance.org/guide/bdd.html())). BDD emerged from
test-driven development ([TDD](http://guide.agilealliance.org/guide/tdd.html)) and tries to bring testing to a different
(business) level. By using natural language, features are defined and test
scenarios are created. This helps to write integration tests based on
stakeholders' needs. BDD is an outside-in approach putting the high level
feature first.

BDD Specification
=================

BDD tests are written in natural language being embedded into a certain syntax (GIVEN-WHEN-THEN). The following example demonstrates a simple BDD test specification.

{% highlight console %}
Feature: Get a single shot of my connected RGB camera
In order to display the image of my RGB camera in my visualisation application
As a developer I want to get the image data by a simple API call

Scenario: Read the image by calling the capture method
Given I have connected the camera
And the operating system detects my camera
When I call the capture method of the API
Then I should get the data via a uint8 pointer
{% endhighlight %}

In this example, the stakeholder is the application developer who is using the
to-be-developed framework. The goal is to read out the image from a given API
by one call. The scenario shows and example of how to access the data. The
GIVEN-WHEN-THEN clause helps to bring the natural language into a certain
syntax which can be picked up by a parser. This particular syntax above is
Gherkin compliant, and can be parsed by a tool called [cucumber](https://cucumber.io/). Cucumber can be
used to write code behind this specification, and actually call your library
directly. There are a number of cucumber implementations, but for native C++
code, [cucumber-cpp](https://github.com/cucumber/cucumber-cpp) is a good choice and allows easy integration into your C++
project.

While writing our BDD tests, top-level requirements are well covered and can give you a test regression for each sprint release. In addition, the features are also well documented and can serve as a “getting started”.
