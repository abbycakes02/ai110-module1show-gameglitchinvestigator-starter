# 💭 Reflection: Game Glitch Investigator

Answer each question in 3 to 5 sentences. Be specific and honest about what actually happened while you worked. This is about your process, not trying to sound perfect.

## 1. What was broken when you started?

- What did the game look like the first time you ran it?
- List at least two concrete bugs you noticed at the start  
  (for example: "the hints were backwards").


I noticed I tried playing the game, but when I guessed a number and tried playing the game, it kept saying lower even when I said 1 which is the lowest number it could be because the guess was from the range 1 to 100. When I tried debugging the issue, I think I found out that it says go lower, but I think it means go higher. 
"the range of numbers does not reflect the range of the actual number"
"when i click new game after playing a game, when i guess it still gives me the same error message where it says i already won. It supposed to start a new game without the previous history intact. 
"It should prevent the user from inputting a number not within the range specified. 


---

## 2. How did you use AI as a teammate?

- Which AI tools did you use on this project (for example: ChatGPT, Gemini, Copilot)?
I used claude.
- Give one example of an AI suggestion that was correct (including what the AI suggested and how you verified the result).
- The AI caught a bug I missed within app.py where the score penalized too high inconsistently.
- Give one example of an AI suggestion that was incorrect or misleading (including what the AI suggested and how you verified the result).
-None of the AI suggestions were misleading that I saw, but once a terminal output was placed in .py file insteadf of being in the terminal.

---

## 3. Debugging and testing your fixes

- How did you decide whether a bug was really fixed?
- I tested the pipeline out to ensure the bug was fixed.
- Describe at least one test you ran (manual or using pytest)  
  and what it showed you about your code.
  - I ran a test to make sure the range of numbers was correct.
- Did AI help you design or understand any tests? How?
- AI helped me design and understand the tests by letting my know what the tests were specifically testing and allowing me to implement more edge cases. 
---

## 4. What did you learn about Streamlit and state?

- How would you explain Streamlit "reruns" and session state to a friend who has never used Streamlit?
- Every time you clcik a button on streamlit, it re-runs the page from top to bottom and then session states come in and you can mainttain the score state there to survive reruns instead of resetting to zero. 

---

## 5. Looking ahead: your developer habits

- What is one habit or strategy from this project that you want to reuse in future labs or projects?
  - This could be a testing habit, a prompting strategy, or a way you used Git.
  - I think I will use inline chat where i highlgiht the code i find flawed and focus on that aspect ifI don't like AI's responses.
- What is one thing you would do differently next time you work with AI on a coding task?
- I think have more individualized problems and debugging them individually instead of all at once.
- In one or two sentences, describe how this project changed the way you think about AI generated code.
- I think I realized you need to understand what's going on to debug ai can't do everything. 
