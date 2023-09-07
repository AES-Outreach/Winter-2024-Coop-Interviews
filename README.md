<!-- PROJECT LOGO -->
<br />
<p align="center">
  <a href="https://github.com/AES-Outreach/Fall-2023-Coop-Interviews">
    <img src="outstem_logo_icon.svg" alt="Logo" width="80" height="80">
  </a>

  <h3 align="center">OutStem Winter 2024 Coding Challenge</h3>

  <p align="center">
    Welcome to the OutStem coding interview.
  </p>
</p>

# OutStem Front-end Challenge

Welcome to the OutStem front-end challenge. Submission instructions are listed below. The deadline to submit this challenge is **Monday September 25th, 9:00 AM**. We would like to emphasize that we are looking for effort, and that the challenge is just part of our discussion with you during the interview, so don’t worry if your solution is *hacky* or even if it doesn’t work, we want to see it!

## The Challenge

The challenge is to build a Trivia game app, where users will be given multiple choice and true/false questions of increasing difficulty.

The design and layout of the website is totally up to you (feel free to use any UI libraries), though you will be judged on the look, feel, and usability of your application, so do your best to respect best practices in web design.

For this challenge, we will be using the [Open Trivia Database API](https://opentdb.com/), which provides a list of random questions using the amount, difficulty, type, and category parameters.

## Api Documentation
For reference, here is the [link](https://opentdb.com/api_config.php) to the full API docs, however this section will cover the basic information you will need to make requests

### Base URL
`https://opentdb.com/api.php`

### Query Parameters for GET
| Param      | Description                                            | Available Options                                     | Example         |
|------------|--------------------------------------------------------|-------------------------------------------------------|-----------------|
| amount     | Number of questions to return                          | Any positive integer                                  | amount=3        |
| difficulty | Difficulty ranging from easy, medium, hard             | easy, medium, hard                                    | difficulty=easy |
| type       | Type of question, either multiple choice or true/false | multiple, boolean                                     | type=boolean    |
| category   | Integer mapping to the category of questions           | Refer to full docs, we will use General Knowledge = 9 | category=9      |


### Example GET Requests
2 questions of any difficulty and type from the General Knowledge category

Request URL: `https://opentdb.com/api.php?amount=3&category=9`

Sample Response:
```
{"response_code":0,"results":[{"category":"General Knowledge","type":"multiple","difficulty":"medium","question":"A doctor with a PhD is a doctor of what?","correct_answer":"Philosophy","incorrect_answers":["Psychology","Phrenology","Physical Therapy"]},{"category":"General Knowledge","type":"multiple","difficulty":"easy","question":"What do the letters in the GMT time zone stand for?","correct_answer":"Greenwich Mean Time","incorrect_answers":["Global Meridian Time","General Median Time","Glasgow Man Time"]}]}
```

1 easy multiple choice question from any category

Request URL: `https://opentdb.com/api.php?amount=5&difficulty=easy&type=multiple`

Sample Response:
```
{"response_code":0,"results":[{"category":"Sports","type":"multiple","difficulty":"easy","question":"What team won the 2016 MLS Cup?","correct_answer":"Seattle Sounders","incorrect_answers":["Colorado Rapids","Toronto FC","Montreal Impact"]}]}
```


## Goals
This challenge has multiple goals that increase in level of difficulty, implement as many of these goals as you are able to.


### Goal 1
Fetch an easy, **true/false**, general knowledge question from the API, and print the response to the console


### Goal 2

Instead of printing to the console, display the question to the user, and allow them to select between the true and false options using whichever UI elements you think are best suited.


### Goal 3
If the user choses the correct answer, give them a success message, and the option to move on to the next stage of the game.

If they chose the incorrect answer, give them a failure message and have them restart the game.

### Goal 4

Now fetch an easy **multiple choice** question from the general knowledge category. 

Display the question on the screen for the user, and allow them to select their answer with whichever UI elements you think are best suited 

### Goal 5

If the user choses the correct answer, give them a success message, and the option to move on to the next stage of the game.

If they chose the incorrect answer, give them a failure message and have them restart the game.

### Goal 6

Repeat with goals 1-5 with medium, and then hard questions

### Goal 7

Build a nice congratulations page for users who won your quiz game!

## Bonus Challenges
If you're done and looking for more challenges, here are some extra ideas!:

- Give the user 2 extra lives instead of ending the game on the first failure
- Add a points system for different question difficulties
- Allow the user to select different categories for the game
- Add animations!


## Your solution

Here are the requirements for your solution.

1. You can complete this challenge using any front end framework of your choice, however, we prefer to see you do this challenge in JavaScript/TypeScript and either Angular or React.
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

1. Navigate to the following link (https://github.com/AES-Outreach/Winter-2024-Coop-Interviews/issues/new/choose) or:
   1. Navigate to the challenge repository
   2. Click **Issues**
   3. Click **New Issue**
2. Click **Get Started** for Solution Submission
3. Change `YOUR_NAME` to your full name in the title field
4. Fill out the form
5. Click **Submit New Issue**
6. Done! Thank you for completing the challenge, we look forward to discussing your solution with you during the interview. 🎉

If you have any questions, you can email Ivana Erlich at ierlich@uottawa.ca



