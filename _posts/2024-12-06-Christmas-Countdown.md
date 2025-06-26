---
title: "Day 220 - Christmas Countdown"
layout: post
categories:
- Christmas
- Not a Game
- Math
feature_image: "/assets/banner-flash-forward.png"
permalink: /day-220
comments: true
---

{% include figure.html image="https://raw.githubusercontent.com/flash-forward-reviews/img2/refs/heads/main/img/chriscount1.png" caption="" alt="" %}{:target="_blank"}
 
## Skeeter's Take:

It’s now December which means it’s time to start thinking about those gifts you are undoubtedly going to buy at the last minute! (Don’t mind me, that’s just me projecting). 

You probably have a rough estimate of days until christmas, but if you ever wanted to find out how many Miliseconds there are until Christmas, Christmas Countdown has got you covered!

Is what I would say if the countdown wasn’t WRONG: 

{% include figure.html image="https://raw.githubusercontent.com/flash-forward-reviews/img2/refs/heads/main/img/chriscount2.png" caption="" alt="" %}{:target="_blank"}

{% include figure.html image="https://raw.githubusercontent.com/flash-forward-reviews/img2/refs/heads/main/img/chriscount3.png" caption="" alt="" %}{:target="_blank"}

On top of that, I felt like the single guy saying “Christmas” was a little lack-luster visually, so I’ve contributed my own changes to make it more festive, and yet somehow less aesthetically pleasing. 

{% include figure.html image="https://raw.githubusercontent.com/flash-forward-reviews/img2/refs/heads/main/img/chriscount4.png" caption="" alt="" %}{:target="_blank"}

EDIT: MilkManIsSad is a legend. Sam went through to troubleshoot their rounding error and this crazy mo-fo took the advice and is actively working on fixing it. This is a simple little throwaway project that could have easily been ignored, but no - MilkManIsSad is actively working on improving this. I love that. I love the dedication. I love that they saw Sam’s message, took the feedback, and is implementing it. 

They also changed the background:

{% include figure.html image="https://raw.githubusercontent.com/flash-forward-reviews/img2/refs/heads/main/img/chriscount5.png" caption="In-Game Screenshot" alt="" %}{:target="_blank"}

Absolutely incredible. I’d like to formally apologize for my terrible art, MilkManIsSad. Had I known this would go on to contribute to your project, I would have spent way more time on this. Instead, I thought it was just going to be a dumb throwaway joke for this stupid blog, so I drew it with a mouse in MSPaint at the office today. You can even see where I gave up on the ornaments halfway through. This is the kind of drawing I would normally make fun of on any given day. Thanks for giving this MS Paint disaster an audience. 

MilkmanIsSad, I salute you my friend. Sorry I sort of made your game worse, but I’m glad I got to contribute in some way. I love how you rolled with the punches. Merry Christmas!

**Recommend: Christmas Countdown couldn’t even get the countdown to christmas right. EDIT: Changing to soft-recommend since MilkManIsSad is fixing it! And for the tenacity of fixing “Christmas Countdown”. We will have to check out more of your games in the future. Keep creating!**

**Replay Percentage Chance: 0% [Edit: 50% chance we come back to this to check if it’s fixed or just to reminisce.]**

**Time Played: 100598 milliseconds** 

## Sam's Take:

Okay there’s something very strange going on here, and I need to get to the bottom of it.

I thought it’s be funny to show up when this countdown ends and make a Merry Christmas post too late as a re-review call back. In order to get a video of the end of the countdown, I used the “hours” number to calculate roughly when the countdown would end...

{% include figure.html image="https://raw.githubusercontent.com/flash-forward-reviews/img2/refs/heads/main/img/chriscount6.png" caption="" alt="" %}{:target="_blank"}

Oh... that actually rounds into being correct...

So what’s going on here?

My theory is that the day is also rounding. Because it’s 11:36am as I type this, which is less than halfway through the day, I’m guessing it is not counting today yet. My evidence for this is that when I first checked the hours, it said there were 445 hours remaining until christmas, then when I went to get the above screenshot, I checked again and it had moved to 444 hours remaining. In that time, we crossed over 11:30am on my computer’s calendar (I changed time zones a few times to confirm the timer is based on my calendar). So before 11:30 (half way through the hour) it says 445 hours, after 11:30, 444. My guess is it will correct itself to “19 days” at noon. I will now wait for 20 minutes or so to confirm.

...

BINGO

{% include figure.html image="https://raw.githubusercontent.com/flash-forward-reviews/img2/refs/heads/main/img/chriscount7.png" caption="" alt="" %}{:target="_blank"}

{% include figure.html image="https://raw.githubusercontent.com/flash-forward-reviews/img2/refs/heads/main/img/chriscount11.png" caption="" alt="" %}{:target="_blank"}

While this explains the weird behavior, I think there’s still a problem. I’m pretty sure it will say that we are one day away from Christmas until noon on Christmas day. Basically, instead of rounding from the middle, the timers would make much more sense if they rounded down always (ie. 19 days, 23hrs, 59min away from Christmas should read as 19 days, not 20).

With all the information gathered, I alerted the developer:

{% include figure.html image="https://raw.githubusercontent.com/flash-forward-reviews/img2/refs/heads/main/img/chriscount8.png" caption="" alt="" %}{:target="_blank"}

And of course:

{% include figure.html image="https://raw.githubusercontent.com/flash-forward-reviews/img2/refs/heads/main/img/chriscount9.png" caption="" alt="" %}{:target="_blank"}

IT IS NOW MIDNIGHT, I AM ABOUT TO PUBLISH BUT WHEN I CLICK ON THE GAME:

{% include figure.html image="https://raw.githubusercontent.com/flash-forward-reviews/img2/refs/heads/main/img/chriscount10.png" caption="" alt="" %}{:target="_blank"}

Decimals to fix the rounding issues? Skeeter’s beautiful background? This guy saw my comments and fixed their game within a day. Great job MilkManIsSad, you filthy Chad.

**Recommend: I have to now**

**Replay Percentage Chance: 50%**

**Time Played: Depends what you mean** 

{% include button.html text="Link to Game" link="https://milkmanissad.itch.io/christmas-countdown" %}