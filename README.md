# 🎮 Game Glitch Investigator: The Impossible Guesser

## 🚨 The Situation

You asked an AI to build a simple "Number Guessing Game" using Streamlit.  
The original game had glitches:

- Hints were backwards ("Too High" said "Go HIGHER!").  
- The secret number type kept changing (sometimes a string), causing inconsistent behavior.  
- Scoring could behave unpredictably.

## 🛠️ Setup

1. Install dependencies: 

```bash
pip install -r requirements.txt
```
## 📸 Demo

Play the game by entering guesses in the text box.

The game shows hints (“Higher” / “Lower”) after each guess.

The score updates correctly based on your guesses.

Click “New Game” to reset the secret number, attempts, and score at any time.

The Developer Debug Info lets you see the secret number, attempts, score, and history for testing.

## 📝 Document Your Experience

**Game Purpose:**  
Guess the secret number within a limited number of attempts while tracking your score.

**Bugs Found:**  
- Hint messages were inverted.  
- Secret number was converted to a string every 2nd attempt.

**Fixes Applied:**  
- Corrected hint messages in `check_guess`.  
- Removed string conversion of the secret number.  
- Refactored core logic into `logic_utils.py`.  
- Verified fixes with pytest and live gameplay.

**AI Collaboration:**  
- Correct suggestion: Swap hint messages to match numeric comparison. Verified via pytest.  
- Misleading suggestion: Converting secret to string was intentional. Verified it caused errors and removed it.

🚀 Stretch Features
![Winning Game Demo](game_demo.png)