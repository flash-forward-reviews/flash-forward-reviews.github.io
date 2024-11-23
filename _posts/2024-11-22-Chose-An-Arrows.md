---
title: "Day 206 - Chose An Arrows"
layout: post
categories:
- No Music
- Educational
- REDACTED
feature_image: "/assets/banner-flash-forward.png"
permalink: /day-206
comments: true
---

{% include figure.html image="https://github.com/flash-forward-reviews/img2/blob/main/img/anarrows1.png?raw=true" caption="" alt="" %}{:target="_blank"}
 
## Skeeter's Take:

↑→←→→→↓↑←→
{% include figure.html image="https://github.com/flash-forward-reviews/img2/blob/main/img/anarrows2.png?raw=true" caption="" alt="" %}{:target="_blank"}

→→→→↓↓↑←→
{% include figure.html image="https://github.com/flash-forward-reviews/img2/blob/main/img/anarrows3.png?raw=true" caption="" alt="" %}{:target="_blank"}

→→↑←↓→↓↑←↑→↑
{% include figure.html image="https://github.com/flash-forward-reviews/img2/blob/main/img/anarrows4.png?raw=true" caption="" alt="" %}{:target="_blank"}

{% include figure.html image="https://github.com/flash-forward-reviews/img2/blob/main/img/anarrows5.png?raw=true" caption="" alt="" %}{:target="_blank"}

**Recommend: ↓↓↓↓↓↓↓**

**Replay Percentage Chance: ↓↓↓↓↓↓↓↓**

**Time Played: ↑→↑↓→** 

## Sam's Take:

You start Chose An Arrows with this top down screen, but don’t be fooled. The game is not a top down exploring type game, this is just the menu where you choose between two different game modes:

{% include figure.html image="https://github.com/flash-forward-reviews/img2/blob/main/img/anarrows6.png?raw=true" caption="" alt="" %}{:target="_blank"}

Now the entire game is in Spanish, and it took me a bit to figure it out, but I’m pretty sure I figured out the two game modes via pictures in the instructions and some trial and error. In one game mode, you choose a direction (up, down, left, right, center), hoping it does not match the computer’s choice. After ten rounds, if the computer only matched you two times or less, you win.

The second game mode is the opposite, you try to match the computer. Do it three or more ten rounds, you win!

{% include figure.html image="https://github.com/flash-forward-reviews/img2/blob/main/img/anarrows7.png?raw=true" caption="" alt="" %}{:target="_blank"}

It’s basically a simplified version of the Mario Party minigame “Look Away” if you are familiar.

{% include figure.html image="https://github.com/flash-forward-reviews/img2/blob/main/img/anarrows8.png?raw=true" caption="" alt="" %}{:target="_blank"}

So I’m sure everyone is thinking exactly what I’m thinking right now, doesn’t that seem a bit unbalanced? I feel the person trying to guess 3 is at a significant disadvantage, especially since the computer picks its directions randomly, so there is no way to play mind games. Now there is a way to calculate the probability, but it unfortunately involves binomial coefficients, which I absolutely do not remember and never will. Therefore we are left with only one other option: BRUTE FORCE:

{% include figure.html image="https://github.com/flash-forward-reviews/img2/blob/main/img/anarrows9.png?raw=true" caption="" alt="" %}{:target="_blank"}

What we have here is a Python script. We make a list of all the directions, and set functions for the robot to choose one at random, as well as the player. They are the same function really, I know, but it’s more fun to pretend they are different people. The last function is the game itself, player and robot each pick a random direction, if the directions match, a point is added.

{% include figure.html image="https://github.com/flash-forward-reviews/img2/blob/main/img/anarrows10.png?raw=true" caption="" alt="" %}{:target="_blank"}

Lastly, we have the main function. We choose the number of games we want to play, then play that many games, adding up each time we get a match three or more times (ie. every time the player correctly matches the directions 3 times or more in one match). Then we divide the number of matches won, by the number of games played, and we get a percentage of the games where the human successfully matched the robot’s directions 3 out of 10 rounds and won that minigame.

So now, we just set the desired attempts to some stupidly large number...

{% include figure.html image="https://github.com/flash-forward-reviews/img2/blob/main/img/anarrows11.png?raw=true" caption="" alt="" %}{:target="_blank"}

And after a million games, we get our percentage: 

{% include figure.html image="https://github.com/flash-forward-reviews/img2/blob/main/img/anarrows12.png?raw=true" caption="" alt="" %}{:target="_blank"}

Running it multiple times yields almost the same result, God bless the law of large numbers!

{% include figure.html image="https://github.com/flash-forward-reviews/img2/blob/main/img/anarrows13.png?raw=true" caption="" alt="" %}{:target="_blank"}

So we can conclude that whoever needs to match 3 is indeed at a significant disadvantage. They have only a 32% chance of winning, whereas the person that has to avoid their direction being matched has a 68% chance of winning. Okay great, so it’s a little imbalanced, why did I bother proving that?

BECAUSE THERE WAS A WAY TO BALANCE THIS GAME

{% include figure.html image="https://github.com/flash-forward-reviews/img2/blob/main/img/anarrows14.png?raw=true" caption="" alt="" %}{:target="_blank"}

What if you only needed to match two times out of ten instead of three?

Let’s run the simulation...

{% include figure.html image="https://github.com/flash-forward-reviews/img2/blob/main/img/anarrows15.png?raw=true" caption="" alt="" %}{:target="_blank"}

DEAR GOD

In this version of the game, the person trying to match has a 62% chance of winning, whereas the other player has a 38% chance! WE’VE IMPROVED THE DIFFERENCE BY 12 PERCENTAGE POINTS!

But we must go deeper...

Let’s bring it back up to 3 matches needed to win a round, but let’s increase the number of rounds from 10 to 13:

{% include figure.html image="https://github.com/flash-forward-reviews/img2/blob/main/img/anarrows16.png?raw=true" caption="" alt="" %}{:target="_blank"}

{% include figure.html image="https://github.com/flash-forward-reviews/img2/blob/main/img/anarrows17.png?raw=true" caption="" alt="" %}{:target="_blank"}

Let’s run it back...

{% include figure.html image="https://github.com/flash-forward-reviews/img2/blob/main/img/anarrows18.png?raw=true" caption="" alt="" %}{:target="_blank"}

Oh... I believe that rounds up to.. 50% BAYBEEE

WE DID IT BOYS, WE BALANCED CHOSE AN ARROWS!

Unfortunately, this would not make the game good. In fact I’m not even sure it’d make the game better. It’s a single player game, balance isn’t super important. It’s just two games and one of them is harder. I don’t really have a point to this one, I just enjoyed playing the game 1,000,000 times in Python. I certainly enjoyed it more than playing Chose An Arrows.

**Recommend: No**

**Game Mode 2 Win Percentage Chance: 32%**

**Time Played: 15 Minutes**

{% include button.html text="Link to Game" link="https://mata6414.itch.io/choose-an-arrow" %}