# AWIZARDOFASCII

*********************
NB These are only rough notes. Just fleshing things out.
********************
## The World

The World is made of characters - specifically [ASCII](https://en.wikipedia.org/wiki/ASCII) characters. Each character has unit meaning that is dependent upon case - for instance, 'T' might mean a tree, while 't' a hand grabbing something. Characters can be put together (words?) to create new meanings.

We'll leave the concrete definition of each char until later. For now, consider the world as a large 2-D cartesian plane, with each point containing an ASCII character (including Null).

The player can move around the Space (not the Nulls) in the world, collecting, eating, using or otherwise interacting with other characters.

The player is the only character we have decided upon. The player is '.' (dot, `46.chr` in Ruby).

## The Player

The Player is called '.' - though the Player may have other use names.

The Player will have stats, both fluctuating (energy, hunger, _etc_) or persistent (Strength, Speed) - though there may be some interplay between the two (e.g low energy takes points off Speed).

The Player has an Inventory.

## Viewable Universe

For want of a better model, the player will be able to see up to 255 positions in each compass direction - what I'm calling "the fog of char". It's an arbitrary limitation, and one that will probably come back to bite us later, but for now the viewable area a player can see will be no more than a square made of all possible N-S/E-W pairs (from N255/W255 to S255/E255), ala:

```
N255/W255───    │
 │              │
 │              │
                │
                │
                │
                │
                │
 ───────────────┼──────────────────
                │
                │
                │
                │
                │                 │
                │                 │
                │                 │
                │      ────S255/E255
```

Obviously the World is bigger than this space. This also gives us an alternative way of referencing characters in the World - from the perspective of the Player. [Credit: thank you https://asciiflow.com/ for use of your diagramming tool].

## Other Goodies
### Scripts. 

Have to have scripts. As "texty" as we can get 'em. Leaning towards [Befunge](https://en.wikipedia.org/wiki/Befunge) at present, but happy to be steered elsewhere. No need to just have one scripting language.

Scripts are (potentially) the magic system. Maybe.

## Next Steps

I'll be building a World server in Ruby to start with, but not super stressed what language(s) get used. I will be sticking to Postgres for the back end. Sorry, but that's my jam.

We'll need to fill out the boilerplate stuff: LICENSE, CODE_OF_CONDUCT and the like. I'm not sure what needed, but it should become apparent. I'm thinking that at least the documenation (this site) should be Creative Commons, but code and other stuff might be licensed differently. License-agnostic for now, but leaning towards "more open" than not.

## Contributing

Early days, so not sure what to suggest. Ideas are welcome. Create a ticket or fork this and raise a PR. 





