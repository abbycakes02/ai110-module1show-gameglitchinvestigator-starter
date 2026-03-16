# 🎮 Game Glitch Investigator: The Impossible Guesser

## 🚨 The Situation

You asked an AI to build a simple "Number Guessing Game" using Streamlit.
It wrote the code, ran away, and now the game is unplayable. 

- You can't win.
- The hints lie to you.
- The secret number seems to have commitment issues.

## 🛠️ Setup

1. Install dependencies: `pip install -r requirements.txt`
2. Run the broken app: `python -m streamlit run app.py`

## 🕵️‍♂️ Your Mission

1. **Play the game.** Open the "Developer Debug Info" tab in the app to see the secret number. Try to win.
2. **Find the State Bug.** Why does the secret number change every time you click "Submit"? Ask ChatGPT: *"How do I keep a variable from resetting in Streamlit when I click a button?"*
3. **Fix the Logic.** The hints ("Higher/Lower") are wrong. Fix them.
4. **Refactor & Test.** - Move the logic into `logic_utils.py`.
   - Run `pytest` in your terminal.
   - Keep fixing until all tests pass!

## 📝 Document Your Experience

- [ ] Describe the game's purpose.
- The game's purposes is to user users guess a number and there is different variabilities of difficulty for the project.
- [x] Detail which bugs you found.
- The hints were backwards (go higher when it should say go lower). The Hard difficulty range was 1-50, making it easier than Normal (1-100). The secret number alternated between int and str every other attempt, breaking comparisons. The attempts counter started at 1 instead of 0. Invalid inputs wasted an attempt before validation. The New Game button never reset status, history, or score. The info banner was hardcoded to "1 and 100" regardless of difficulty. No range validation prevented guesses outside the allowed range.

- [x] Explain what fixes you applied.
- Fixed hint messages so Too High says "Go LOWER" and Too Low says "Go HIGHER". Fixed Hard difficulty range to 1-200. Removed the type-switching bug so secret is always an int. Initialized attempts at 0. Moved attempt increment after validation so invalid inputs don't waste a turn. Fixed New Game to reset status, history, score, and use the correct difficulty range. Updated the info banner to show the dynamic range. Added range validation to parse_guess so out-of-bounds numbers are rejected.

## 📸 Demo

![Winning game screenshot](Screenshot 2026-03-15 at 11.30.34 PM.png)



## 🚀 Stretch Features

- [ ] [If you choose to complete Challenge 4, insert a screenshot of your Enhanced Game UI here]
