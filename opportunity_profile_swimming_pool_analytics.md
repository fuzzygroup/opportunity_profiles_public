# Name: **PoolBot** / **PoolBoy**

# Domain: **tbd**

# Tag Lines: 

* A swimming pool is a horrible thing to let become soup
* A swimming pool is one missed maintenance opportunity from being ruined
* Swimming is better in the connected pool.
* The Connected Pool

## Concept: 

A swimming pool is simply one accident away from being a 30,000 gallon of cloudy soup.  A swimming pool is a uniquely wonderful way for an individual or family to beat the heat and enjoy life.  That said a swimming pool is a delicate fusion of:

* Water
* Chemicals
* Electricity
* Regular and Consistent Maintenance

Swimming pools very much remember mad scientists -- they are one lab accident (or maintenance error) away from becoming a super villain (or toxic puddle of cloudy soup).

## The Problem 

Swimming pools rely on humans to regularly perform chemical balance maintenance that looks a lot like this:

1. Test the water with a chemical test strip.
2. Compare the test strip to a color palette.
3. Calculate the amount of chemicals to add to a pool to maintain its correct ratio of chlorine / chloramine.
4. Notice when things go askew.

Steps 1 and 2 are problematic because:

* Humans are forgetful / lazy.
* Humans have poor color judgement at times and / or are color blind.

Step 3 is problematic because:

* Humans are bad at math because, well, **math**.
* People simply make mistakes

Step 4 is problematic because:

* Pools now have mechanical, opaque covers.
* As families age, the pool gets used less -- kids get busy with youth sports / video gaming / and the days of the pool being used constantly give way to holiday usage.
* People can be, ahem, unobservant

## Enter the Pool Company aka The Problem Not the Solution

Whenever a difficult problem exists, specialist firms come into being to take care of it.  However, the existence of specialist firms doesn't always mean that they are competent.  As this is beginning to sound particularly personal, let me assure you: it is.  I grew up with a pool and watched my mother struggle with testing kits that, today, are unchanged from the mid 1970s.  This has led to professional pool maintenance firms.

1. People are no more talented at math and calculating how much chorine to add than they were in the 1970s as I have now watched my own professional pool firm completely **fuck** up my pool.
2. Pool maintenance firms are now an industry unto themselves.  They have become a distribution agent to a large industry centered around service and support of these 20,000 to 30,000 gallon leviathans.
3. Pool maintenance firms are now so specialized that if you have a pool and a hot tub, that is two separate maintenance contracts as the pool guy is NOT the same as the spa guy -- despite **being the same damn thing**.

To draw an analogy from the world of high tech, the pool is a SAN or storage area network -- huge, complex and needing regular care and feeding.  The hot tub is an SSD that also requires care and feeding.  And despite there being the same maintenance requirements and underlying technologies, industry balkanization has led to different firms.

This is fundamentally:

* Irrational
* Inefficient
* Bad for the customer

## The Solution: Automate the Analytics And Generate Alerts

There are three key analytic issues:

* Chemical Analysis
* Flow state analysis

Each is discussed below.

### Chemical Analysis

For reasons of chemistry, there is not an easy way to measure the alkalinity of the water and its level of chlorine.  This is not a problem, it is an opportunity. The solution is to automate the traditional test kit in a controlled fashion using off the shelf hardware, image sensors and back end software.

Note: Based on research I did a few years back, there was one semiconductor to measuring chlorine levels.  It was a complex sensor element with a per unit cost of $300 and aimed at large commercial pools.

### Flow State Analysis

### The Proposed Product

The problem in question needs to be an inline box that is plumbed into a pool's water line.  By being plumbed into a water line, it can:

1. Measure water temperature.
2. Measure water movement.
3. Generate alerts if temperature moves outside of a threshold.
4. Generate alerts if a black swan event happens such as the pool motor stops due to a popped circuit breaker.
5. Generate chemical tests by a small electrically controlled drip valve that puts enough water onto a test strip that an image sensor can take a picture of the test strip and then send it to a server side process which looks up an account, compares the image of the test strip to a reference picture, calculates the amount of chemicals needed and sends an alert to a test message address (or an app).

That last item is likely the patentable IP as well as the recurring revenue element of the solution:

* The idea of automating a chlorine test via a picture and a server side process may be patentable ip
* A server side process means recurring revenue and feeds
* A proprietary test strip format is likely needed so it can be handled mechanically; there needs to be a hopper of these things, a robotic mechanism needs to insert them and so on 

### Sidebar: Reduce Energy Usage

Pool pumps are expensive and do not need to be run 24 hours a day but most pool owners do because knowing when to NOT run a pool motor is also conceptually difficult.  It should be possible to reduce pool operating costs by turn the motor off programmatically.

### Spas

And, of course, the same product can be used for spas.

## Why Doesn't This Already Exist

There are two problems:

1. There is an existing industry that thrives on the complexity NOT of pool cleaning but of pool chemistry.  My wife, for example, would be fine cleaning the pool but doesn't want to deal with the testing and the math.
2. The lack of a solid state sensor means that this is not a traditional analytics problem; it is a hybrid mechanical (move test strip) and visual (take a picture) problem.

## How Does It Make Money?

There are a number of opportunities:

1. Device sales.
2. Device installation; it does need to be plumbed into water lines, tied to power and then connected to wifi and calibrated.
3. Test strip sales.
4. SAAS fees.

## The Underlying Software

The back end software for this is a pretty classical analytics platform such as a time series DB for tracking measurements, a grafana dashboard and then an alerting api feeding into an app.  None of this is particularly novel in today's software development world.  The math is likely fairly easy and the color analysis of the test strip picture easy with something like the OpenCV toolkit.

## Competition

I have not seen this yet as a solution but the world is vast and mysterious.  Perhaps someone has started down this path.
