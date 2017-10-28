# Aria_VS_Dragon

So this is both a little puzzle challenge I made and an interesting environment idea for evolution-based neural networks / models.

In this challenge, you play the role of Aria, a mage, and have to defeat the mighty Dragon, who is far more powerful than you,
but also doesn't think very hard!

You have 1 physical attack move with a sword, and 7 spells,
and with all of these you are allowed to target either yourself or the Dragon.

This means there are a total of 16 possible moves.

The solution is a bit of a trick, something that when you figure it out, you're like "Ohhhhhhhhhh..... I get it...."  and executing
this solution is very systematic, very exact, and so I wanted to see if some kind of evolving model could learn to beat it, and
honestly it looks like it's not only possible, but kind of a breeze.

Currently, my best approach has been to let the bot play 500 random games at first, take the best 50, have a RandomForest train
on those, and then have that model play 500 games, inject 10% random moves to ensure there's "innovation",
take the best 50 games, etc, until it is crushing the Dragon every time.

Right now it wins 25% of the time (if you play randomly you will basically never win) and the problem is that at a certain point,
the 10% randomness needs to be removed from its play.  Once the model has made all the innovations necessary, I need to give
itself a way of knowing that that is the case, and to shift gears, shore up on what it already knows, or maybe just
allow it to shift gears either way in regard to injecting randomness if its been stuck for a certain amount of time.

For now I just wanted to get the repo up cus I thought the idea was kinda cool.

Have a good day!
