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
take the best 50 games, etc, until it is crushing the Dragon every time.  After it hits a bit of a wall, you can remove the randomness and let it refine what it already knows.

Right now it wins 92% of the time.

At some point, I want to try making a general process where I run the function, walk away, come back, and the model automatically goes from total randomness to victory in 90%+ area.

This game is somewhat trivial once you know the trick, but the remarkable thing to me was that it didn't know any of the rules.  It only knew "lowering Dragon HP is good", "Killing the Dragon is really good", and "Killing the Dragon fast is a nice bonus".

Have a good day!
