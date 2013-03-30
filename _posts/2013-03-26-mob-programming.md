---
layout: post
title:  Mob Programming
---

Last Thursday evening at our monthly Ruby meet up in Edinburgh we had a mob programming session using Katrina's holiday refactoring code. The turn out was relatively small (only 7, with an 8th joining towards the end), a pattern we have seen when we have coding sessions rather than talks. However, as predicted by Woody, this seemed to be the ideal number once we were in our stride.

We started out by agreeing the rules for the evening:

* We were to sit in a circle around the pairing desk
* In any given turn there would be a driver typing at the keyboard and a navigator deciding the direction to be taken
* At the end of the turn the navigator would become the driver and the next person in line would become the navigator
* Turns would last 4 minutes
* We would start at 7pm and finish at 9pm

As it turned out we had a few late arrivals and so we didn't kick off until 7:30, for whatever that may be worth. I should also mention that we had quite a mix of skills in both Ruby and refactoring. Some had never used Ruby before and were not familiar with refactoring, some were dab hands at both, some were in between.

The evening started out well with all of us agreeing that the refactoring looked relatively simple and so we should just jump in and see how we got on. We agreed that only the navigator could decide the course of action although he or she could ask for help if they so desired. We also agreed that anyone wishing to offer advice had to say "Suggestion" first and only stump up their 2¢ if the navigator agreed first.

The first few iterations went well as we made some simple refactorings, however it soon became apparent that things were not as simple as we'd first thought (are they ever?). There were a couple of areas where complexity was hidden and a couple more where code was confusingly named or defined, thus masking its true intent. This led us to a few dead ends. In one particularly notable case a refactoring was made only to be rolled back … or so we thought. We'd actually only half undone the change though and it led to a few confusing turns as we tried to figure out why tests were failing.

We called time at 9 o'clock and started to do a retro on the evening, however we'd not completed the refactoring to our satisfaction (or at least we'd not reached a satisfactory cutting off point) and so, inevitably, we ended up gathered round the keyboard trying to solve it out. We quickly got to a better place and felt happier to leave it in that state.

At the end of the night I took the following notes:

* rules for communication helped at first so that there wasn't a free-for-all whilst people were trying to get their head around the code initially
* however there was a turning point where the rules stopped being helpful and started to hinder
* I suspect a short break in the middle to discuss the state of play might have helped
* the most change that was made came after the end of the official session when we all gathered round and group minded the rest :)

However, with hindsight I think that I somewhat disagree with these statements.

* I think the communication rules were a great constraint.
* The "turning point" that we experienced I now suspect to be the point where we were starting to find it hard to express ourselves adequately whilst we tried to hold all of the required context for the refactor in our heads. In other words, this was the point where the constraint started to work on us as intended.
* I do think that a short break half way through the evening would have been helpful so that we could all have taken a step back from the coal face. However, given that this was our first time I have no way of proving that out. I'd be interested to hear your experiences here.
* I now think that the reason we were so productive in those last few minutes was because we removed the constraint and reverted to type. In other words, the person typing was applying their solution in code rather than communicating verbally, which made it easier for them to intuit their way through (as many of us in the room would normally do). In turn the rest of us in the room were able to nudge and tweak the refactorings the "driver" was making. Therefore we resorted to the opposite of the intended setup with the "driver" leading and the "navigator" checking for typos and logic missteps.
* I have to admit that I find that fascinating! Whether this is actually what happened or not, it has been a bit of a lightbulb moment for me with regards to the way that I often approach pairing. Firstly, when I pair we more often than not assume the roles of leader (with keyboard) and tweaker (observing) rather than driver and navigator. I'm not sure if this is a good thing, bad thing or just a thing. :) Furthermore I often fall into the habit of what I call "painting with code", where I will pseudo a method, class or spec in order to explain to my pair what my intentions are, rather than taking the time to explain in plain english. I've justified this in the past by saying that code is more empirical than english, but I wonder now if it's more my inability to clearly express my intent otherwise.

Anyway, I digress. :) Everyone that attended the event found it valuable and most also found it enjoyable (I think that some found the typing/coding in front of others quite stressful, although I made an effort to assure everyone at the start that no judgement would be made).

The following were also some interesting takeaways from the evening:

* we often take our development environments for granted in how much they help and mould us (e.g. using someone else's workstation hampers muscle memory).
* the code we looked at initially seemed to be a reasonably straight forward refactor, but there was hidden complexity that we didn't understand until we got into the refactor.
* like a TV quiz show, it's much easier to spot issues/decide direction when you're not in the navigator's chair!
* a few times we had to roll back to a previous state
  * twice reset to previous commit
  * three times rolled back current direction to previous state to get a better grasp on big picture
