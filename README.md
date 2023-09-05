<!-- PROJECT LOGO -->
<br />
<p align="center">
  <a href="https://github.com/AES-Outreach/Fall-2023-Coop-Interviews">
    <img src="outstem_logo_icon.svg" alt="Logo" width="80" height="80">
  </a>

  <h3 align="center">OutStem Fall 2023 Coding Challenge</h3>

  <p align="center">
    Welcome to the OutStem coding interview.
  </p>
</p>

# OutStem Front-end Challenge

Welcome to the OutStem front-end challenge. Submission instructions are listed below. The deadline to submit this challenge is **Tuesday May 23rd, 9:00 AM**. We would like to emphasize that we are looking for effort, and that the challenge is just part of our discussion with you during the interview, so don’t worry if your solution is *hacky* or even if it doesn’t work, we want to see it!

## The Challenge

The challenge is to build a fun card game app, where users will be given cards from a [standard deck of playing cards](https://en.wikipedia.org/wiki/Standard_52-card_deck), and make guesses about the next card that will be drawn. 

The design and layout of the website is totally up to you (feel free to use any UI libraries), though you will be judged on the look, feel, and usability of your application, so do your best to respect best practices in web design.

For this challenge, we will be using the [Deck of Cards API](https://www.deckofcardsapi.com/), which creates a deck of cards for you, gives you a `deck_id`, and keeps track of which cards are left as you draw cards.

## Goals
This challenge has multiple goals that increase in level of difficulty, implement as many of these goals as you are able to.

### Goal 1
Fetch a new deck of cards from the API, and print the response to the console

URL: `https://www.deckofcardsapi.com/api/deck/new/`

Example Response:
```json
{
    "success": true,
    "deck_id": "3p40paa87x90",
    "shuffled": false,
    "remaining": 52
}
```


### Goal 2

Ask the user if the next card will be Red or Black. You can use any input element for this, ex text input, buttons, dropdown


### Goal 3

Once they input their answer, draw a card from your deck using the API (as seen below) and check if they are correct or incorrect:

URL: `https://www.deckofcardsapi.com/api/deck/YOURDECKIDHERE/draw/?count=1`

Example Response:
```json
{
    "success": true, 
    "deck_id": "kxozasf3edqu", 
    "cards": [
        {
            "code": "5S", 
            "image": "https://deckofcardsapi.com/static/img/5S.png", 
            "images": {
                          "svg": "https://deckofcardsapi.com/static/img/5S.svg", 
                          "png": "https://deckofcardsapi.com/static/img/5S.png"
                      }, 
            "value": "5", 
            "suit": "SPADES"
        }
    ], 
    "remaining": 50
}

```

### Goal 4

If the user guessed incorrectly, give them a message informing them, and then give them the option to restart the game from Goal 1 with a new deck.

If the user guessed correctly, give them a success message, and the option to move on to the next stage of the game

### Goal 5

Ask the user if the next card will be higher, lower, or equal to the first card. Again, you can use any input element for this, ex text input, buttons, dropdown.

Then repeat steps 3 & 4 (draw a card and validate)

### Goal 6

Ask the user if the next card will be Hearts, Diamonds, Clubs, or Spades. 
Again, you can use any input element for this, ex text input, buttons, dropdown.

Then repeat steps 3 & 4 (draw a card and validate)

### Goal 7

Build a nice congratulations page for users who won!

## Your solution

Here are the requirements for your solution.

1. You can complete this challenge using any front end framework of your choice, however, we prefer to see you do this challenge in JavaScript/TypeScript and Angular.
2. Your solution submission should indicate which goals you've achieved
4. You must submit your solution in a GitHub repository or a Repl.it. **Please make sure your project/repository is public and accessible by us.**

## Evaluation 

You will be evaluated on:
- Completeness: did you complete the features?
- Correctness: does the functionality act in sensible, thought-out ways?
- Maintainability: is it written in a clean, maintainable way?
- Best Practices: does your solution use Javascript/TypeScript's and your chosen framework's best practices
- User Friendly UI: does your solution anticipate what users might need to do and have elements that are easy to access?

## Submission

Please submit your solution in the 2023 Fall interview GitHub repository via GitHub Issue.

1. Navigate to the following link (https://github.com/AES-Outreach/Fall-2023-Coop-Interviews/issues/new/choose) or:
   1. Navigate to the challenge repository
   2. Click **Issues**
   3. Click **New Issue**
2. Click **Get Started** for Solution Submission
3. Change `YOUR_NAME` to your full name in the title field
4. Fill out the form
5. Click **Submit New Issue**
6. Done! Thank you for completing the challenge, we look forward to discussing your solution with you during the interview. 🎉

If you have any questions, you can email Alexandre Séguin at asegui8@uottawa.ca


## Bonus Challenges
If you're done and looking for more challenges, try these out:

- Make your UI responsive, that is usable on all screen sizes
- Add animations
- Keep track of how many games the user has won or lost
