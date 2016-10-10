# Vim for the Impatient

Vim has some of the worst onboarding of any editor I have ever encountered.

This is unfortunate, because at the same time it is _one of the most powerful_
editors I have ever encountered.  My goal is twofold:

  1. to shorten the evaluation time.  I want you to hit the *informed* "I know whether I want this" point as fast as possible.
  2. to pave this very rocky road for people with a low tolerance for nonsense.

The "*informed*" qualifier is important.  I think there is an unexamined middle ground between "the 5 minute intro" and "goodbye weekend"; enough time to actually understand the tool without totally drinking the kool-aid.  That is my target, which is probably a couple of hours.

## Why Bother

Vim's power comes from three places: its composable command system, its configurability, and its ecosystem.

The latter two are more obvious: vim is extremely flexible, and easily integrates with running whatever you want on whatever keystroke you want, bringing the full power of your machine into your editor.  Even better, very talented people (much stronger developers than you or me) have built and shared their configurations for maximum productivity + custom commands.  Borrowing someone else's superpowers/solutions, especially from the best solvers of a problem, is at the heart of software.

The third is harder to express in words, though I will try anyway.  Basically, all of your experience navigating text has trained you into thinking things are Just "done a certain way".  Some people don't go very far down the shortcuts rabbit hole, and just click around with their mouse.  Others hold arrow keys, or consider themselves superusers for using `control` to skip around by words.  Each of these groups hits a limit of what can easily be done with a keyboard, and just accepts the friction of doing more complex manipulations.

Vim eliminates that friction, providing gestures for all of your intentions, not just tools to eventually manifest them.  It sounds like a small thing; holding control and arrow keys to move is not a big deal.  But Vim deletes the friction from even more complex actions: "go to the editable position at the end of this line".  "Paste my clipboard into the line above this one".  "Reindent this entire paragraph".  "Run this file".  "Shell out the execution of the tests for this file".  "Do this complex transform I define once on all of {these lines}".  All of these become about as low friction as hitting the arrow keys once.

This deep configurability is Vim's virtue and its vice.  We are going to explore the former while fighting the latter.

## The Problems

Let's enumerate some of the sources of trouble so we can better avoid them.

The vim experience has several categories of problem for new learners, and they
interact as comorbid conditions tend to: badly.

### Tinkerers

#### The Problem

Some people derive positive utility from tinkering with things, and so they seek
out and enjoy tools that require the maximum amount of tinkering possible.  This
is great for them, and I am happy they have found something they love!

Unfortunately, not all of us are tinkerers, and some of us even derive
_negative_ utility from having to tinker with things.  Because vim is such a
tinkerable tool, a nonzero fraction of the community will push tinkerer-oriented
perspectives and processes.  Further, orthogonal preferences can make
prioritization difficult: someone who enjoys Just Doing can have a hard time
telling you what is not important/can be ignored, because they love all of it.

Even worse, a small (but sometimes vocal) minority of the vim-using population
are, shall we say, lacking in basic empathy.  **They** love tinkering, and if
you don't, then "you must be doing something wrong" or "you might not be cut out
for this" or "maybe this is not for you."  Let's be clear: these people
**the very worst**, are not indicative of the broader vim using community, and
are the problem, not you.

#### The Solution

Compatibility with the people you learn from is extremely important.  If you are
not a tinkerer, you need a not-tinkerer teacher.  (Hello!)  If you are,
congratulations, vim will probably suit you nicely and you can read anything.

### Rampant Landmines

#### The Problem

Vim's potential control surface (think rocket dashboard) is tremendously
complicated, which means really small errors can produce wildly wrong results.
For example, `k` is up.  But `K` is "shell out to `man` and try to get guidance
for things under your cursor," which looks like total system failure when it
surprises you.  (Which it easily might if you, for example, actually tap the
capslock key.)

#### The Solution

We are going to do some risk management to start, and structure the learning
process to dodge the crazy stuff.  Skill trees are the best abstraction here: we
are going to put off the complex material that has dependencies, and focus on
building from the ground up.

### Exsanguination of Morale

#### The Problem

Some things, like Zelda games, are _extremely_ well designed to provide
continual feelings of progress and control.  Vim can be the total opposite
of that.  Landmines can breed a sense of helplessness/lack of control, as things blow up for unknown/seemingly irrational reasons, while tinkerers might gaslight you ("there are no problems at all!") or worse: blame you, the novice.

When I first heard of Vim, I dreaded its configurability as a potential fountain of frustration.  If I have to choose my keybindings myself, I am much more likely to choose badly (in a way that conflicts with some useful tool I "should have known" I would need to use/account for).  Giving voice to a feeling: "The best I can do choosing as a novice is match someone choosing as an expert, so why not just config the expert's advice by default?  Maybe I should go back to Sublime, which doesn't so obviously hate me."

This series is an attempt to mitigate this problem.  As I swing my machete through the thicket of Vim's problems, I'll try to leave behind a saner path for you.  Remember when you first really understood what Minecraft was all about?  That is the feeling we are going for here.

(If you don't remember, try [this](https://www.penny-arcade.com/comic/2010/09/17/mine-all-mine-part-one) and [this](https://www.penny-arcade.com/comic/2010/09/20/mine-all-mine-part-two).)

#### The Solution

Flow and feelings of empowerment/productivity are all about having expectations
and meeting them to build something.  So instead of throwing you into the deep
blue sea and trusting you to enjoy figuring it out, we'll build a useful IDE and companion workflows in pieces.

## Next time

We'll cover some safety practices, basic file management, and then add useful markdown features.
