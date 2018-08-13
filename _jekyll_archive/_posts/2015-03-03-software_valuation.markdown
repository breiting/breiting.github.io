---
layout: post
title:  "Software valuation"
date:   2015-03-03
categories: value, estimation
---

Recently, Bob, a friend of mine, told me about an interesting conversation he
had with his colleague Henry (names have been changed). Henry was asking Bob to
give an estimate about the value (in cash) of their current code base. Not an
easy question, Bob thought, and had no simple answer. Henry said, this is an
easy task: "Yesterday, I counted the current lines of code of our master
branch. I was impressed that we almost reached 100k. Assuming a developer can
deliver about 500 lines of code per months (20 per day), this would result in
roughly 200 person months. If the developer costs 7k per month, then the code
base would be roughly worth 1.4 Mio Euros". This number really impressed me. Is
it really so simple to calculate the value of a software company's IP value?

After a quick research session in the web I found a model called <a
href="http://en.wikipedia.org/wiki/COCOMO">COCOMO</a> (Constructive Cost Model)
which is an algorithmic software cost estimation
model developed by Barry W. Boehm. The model uses a basic regression formula
with parameters that are derived from historical project data and current as
well as future project characteristics [taken from Wikipedia]. The COCOMO
formula is pretty simple:

$$E = a * KLOC^b * EAF$$

where E is the effort applied in person-months, KLOC is the estimated number of
thousands of delivered lines of code for the project, and EAF is the factor
calculated by a certain rating table (typical values range between 0.9 and
    1.4). The coefficient a and the exponent b are depending on the software
project class (organic, semi-attached, or embedded). Taking Henry's example
above, for an organic team this would even mean a value worth 2.3 Mio Euros.

Is it really so easy to get the value of your code repository (respectively
your company's IP)? Can each line be treated equally valuable? What about
maintenance cost, market value, bugs. Aren't those relevant for calculating the
value? I continued my research and found an interesting <a
href="http://infolab.stanford.edu/pub/gio/2006/worth40.pdf">paper</a> by Gio
Wiederhold (Professor (Emeritus) of Computer Science, Medicine, and Electrical
    Engineering
 at Stanford University). Professor Wiederhold discussed a method for valuing
software, based on the income that use of that software is expected to generate
in the future. This method can be used to estimate the value of a software
company. This is typically interesting during due diligence prior to an
acquisition. His approach not only takes into account the current status, but
also takes into account software maintenance costs, and product growth.

An interesting statement I found in his paper was that the value of the
purchaser of a software is independent of the cost and effort spent to create
it. A few brilliant lines of code can have a very high value, whereas a million
lines of code may have only little value. This statement already tells us that
the LOC is not a proper measure for the value of code. For proper estimation,
    maintenance must be taken into account. Wiederhold distinguishes between
    three different types:


1. *Bug fixing or corrective maintenance*: high cost immediately after a software release, will get less over time.
2. *Adaptive maintenance*: required to satisfy external constraints (e.g. new hardware, new OS, browser update, ...). Is typically constant over time.
3. *Perfective maintenance*: includes improvements such as performance upgrades assuring scalability as demands grow, improve interoperability with other vendors (e.g. other databases, services, ...). Typically grows over time.
