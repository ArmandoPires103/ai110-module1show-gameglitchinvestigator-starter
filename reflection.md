# 💭 Reflection: Game Glitch Investigator

Answer each question in 3 to 5 sentences. Be specific and honest about what actually happened while you worked. This is about your process, not trying to sound perfect.

## 1. What was broken when you started?

First Issue: I expected the hint system to guide the player correctly by saying "try a lower number" when the guess is above the secret number and "try a higher number" when the guess is below it. Instead, the hints are backwards—the game tells me to guess higher when my guess is already too high.

Second Issue: I expected the displayed instructions to match the selected difficulty level. However, after choosing Hard mode, the game stated that the valid range was 1–50, but the secret numbers generated were sometimes greater than 50, making the instructions inaccurate.

---

## 2. How did you use AI as a teammate?

I used Claude as my AI tool for this project. It helped me better understand the code, identify logic errors, and refactor parts of the application into separate files. One useful suggestion was moving game logic functions, such as `check_guess`, into a separate `logic_utils.py` file. This improved the organization of the project by separating the game logic from the user interface code in `app.py`, making the application easier to maintain and read.

I verified the AI-generated changes by running the application and testing the game to ensure everything functioned correctly after the refactoring. One suggestion that was not helpful was the recommendation to sometimes convert the secret number into a string. After testing this approach, I found that it added unnecessary complexity and did not improve the program. I decided to keep the secret number as an integer, which simplified the logic and made the code easier to understand.


---

## 3. Debugging and testing your fixes

I verified that a bug was truly fixed by running the application and testing the game myself. In addition, I used pytest to test the `check_guess` function and confirm that the logic behaved as expected. For example, when I guessed 60 and the secret number was 50, the function correctly indicated that the guess was too high. This confirmed that the bug fix was working properly.

AI also helped me improve my testing process by pointing out that the `check_guess` function returns a tuple rather than a single string. Understanding the function's return value allowed me to write more accurate test cases and better validate the program's behavior.


---

## 4. What did you learn about Streamlit and state?

Session state acts like the app's memory. Since the script restarts each time, any normal variables would be reset. Session state allows Streamlit to remember important information, such as the secret number, the number of guesses, or the player's score, even after the app reruns. Without session state, the game would forget everything whenever the user interacted with it.

---

## 5. Looking ahead: your developer habits

This project changed the way I think about AI-generated code. I learned that AI can be a valuable tool for identifying bugs, improving code organization, and suggesting solutions, but it is not always correct. Human review, testing, and validation are still necessary to ensure that the final code works as intended and meets the project's requirements.
