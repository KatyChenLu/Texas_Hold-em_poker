
# Texas Hold'em -- An Interview Question by Patreon

## Prompt

You start with a library of `Card`s, `Deck`s, and `Hand`s, and `XCTest` tests covering those classes. Example usage you can find below.

Your goal is to extend this library to support a variant of Poker called Texas Hold 'em.
This game will be made of a `TexasHoldemDealer`, `TexasHoldemPlayer`s, and their `PokerHand`s.
You do *not* need to make a Texas Hold 'em app, with any UI or controllers.
You *only* need to make the provided `XCTest`s pass, with clean and well-factored code.

You are given failing `XCTest` tests for each of these classes.
Run tests in XCode with Product -> Tests (⌘+U) to run all tests,
or click the test icon in the sidebar (fifth icon, looks like a yield sign) and hover over any individual test to run it.
You can also run individual tests from the test files themselves, which live under the `Texas Hold'emTests` folder in the project navigator.

These tests should encode all the knowledge of Poker and Texas Hold'em you need for this problem,
so don't worry if you're not a poker expert.
If you would like more information to feel comfortable,
the sections "Poker Hand Rankings" and "The Play" at [this site](http://vegasclick.com/games/texasholdem.html)
(ignoring "1. Posting the Blinds" and all other such mentions of betting)
should be all you need to know.
Wikipedia, as always, is also a pretty good, if at times overly detailed, resource:
[List of Poker Hands](https://en.wikipedia.org/wiki/List_of_poker_hands)
and [Texas Hold'em : Play of the Hand](https://en.wikipedia.org/wiki/Texas_hold_%27em#Play_of_the_hand).


## Installation

Just run the XCode project and you should be good to go!


## Example usage of the existing Cards library

Here's a trivial example of declaring a new deck, shuffling, and drawing 5 cards into a hand:

```obj-c
import "Hand.h"
import "Deck.h"

...

Card *aceOfSpades = [[Card alloc] initWithRank:CardRankAce andSuit:CardSuitSpades;
Card *queenOfHearts = [[Card alloc] initWithRank:CardRankQueen andSuit:CardSuitHearts;

Hand *hand = [[Hand alloc] initWithCards:@[aceOfSpades, queenOfHearts]];

Deck *deck = [[Deck alloc] init];

[deck shuffle];

[hand drawCards:5 fromDeck:deck];

NSLog(@"%@", hand);

...
```
