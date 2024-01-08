---
date: "2024-01-07"
description: "Ways to overcome weight anxiety and obsession."
paige:
  file_link:
    disable: false
  style: |
    #paige-authors,
    #paige-credit,
    #paige-date,
    #paige-keywords,
    #paige-reading-time,
    #paige-series,
    #paige-toc,
    .paige-authors,
    .paige-date,
    .paige-date-header,
    .paige-keywords,
    .paige-reading-time,
    .paige-series,
    .paige-summary {
        display: block;
    }
series: ["cycling"]
tags: ["zwift", "cycling"]
title: "Struggling with Zwift Weight"
---
<p>Just like in work, when you can automate something in life, you can eliminate some of the weirder ritualized neuroses.</p>

<p>In my case, it's about getting my weight right for each indoor ride. For whatever reason, I'm constantly obsessing about how the smallest of changes in my weight can impact my performance on a race or even just a short workout. In Zwift, it's pretty easy to manually do this, but by manually doing it before each ride, it's started to become a problem because now I'm putting too much mental energy into what I'm weighing. I don't do this for outdoor rides. Granted for indoor rides, you want to be fair and accurate when it comes to racing so that people aren't looking at your results skeptically, especially compared to your historical results. As a cyclist, I don't think that I'm a special case caring about the minute details of my data since the sport has a culture of shaving arms and legs, which I do not do. Although I have thought about the potential weight savings of shaving. Have I convinced you that I'm crazy yet?</p>

<p>I have a Fitbit Aria smart scale that helps me address this weight obsession. Instead, I can stand on the scale each day without really even looking at the result and then step off. What happens next is automagic. My Fitbit scale updates my Zwift weight without my manual input. How does this happen? APIs, baby! Some magical person created an opt-in application that runs whenever new weight data is logged into your Fitbit account. So, you step on your scale. The scale registers the new weight data and sends it from the scale to the cloud. Once the data is in the cloud, then there's likely some POST or PUT API sending the weight data to the Zwift account.</p>

<p>Okay? So, what? Well, my Fitbit scale doesn't update my Strava profile weight. I know, I'm a lil McLooney, but, c'mon, I'm a creature of habit and consistency. If I can't control the quality of my data, then how can I trust the data? Anyway, I did a little digging. Fitbit has a robust API and Strava has a robust API, but there's just not a free application for doing what Fitbit and Zwift are doing. I did some digging. Some people are using some paid apps as a third party to update their Strava profile weight with their Fitbit scales, but I want to know why. Can't this work directly? The answer is yes.</p>

<p>I set myself with a Fitbit developer account and a Strava developer account. I retrieved my weight from Fitbit using their API. Then I pushed my weight to Strava using their API. I've thought about developing this application myself, but I need to overcome a few roadblocks to move forward.</p>

- I need to understand token management. For instance, how can I renew access tokens so that the Strava and Fitbit application stays authenticated? How do I store/manage tokens as a developer pleeb?
- I need to script a conversion of the weight. I believe the weight data that I retrieved from Fitbit is different than what Strava accepts.

<p>I can't promise that I'll be less obsessed, but I can promise to post an update once I make some more progress.</p>
