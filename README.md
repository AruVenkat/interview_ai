# 📖 Practical Task: AI Q&A System

Welcome! 👋 In this exercise, you will implement a simple **AI-powered Q&A system** using the provided dataset. This is designed to test your ability to **design, code, and think about AI systems**.

---

## 🔹 Files Provided
- **`qa_mixed_expanded.json`** → Dataset of Q&A pairs (includes:
  - Regular questions (answerable)
  - Trick questions (should escalate)
  - Borderline paraphrases (test similarity threshold))
- **`main.py`** → Starter code (JSON loading, embeddings model, and placeholders for you).

---

## 🔹 Your Tasks

### 1. Implement `answer(query)`
- Input: a text query.
- Logic:
  - Encode the query.
  - Compute similarity against dataset questions.
  - If similarity score > threshold → return the corresponding answer.
  - Else → return `"escalate"`.
- Default threshold: `0.6` (you may adjust if needed).

### 2. Test Your System
Run `main.py` and try queries:
- ✅ Regular: *“What is the capital of France?”* → should return `"Paris"`.
- ⚠️ Trick: *“Who is the CEO of OpenAI?”* → should return `"escalate"`.
- 🤔 Borderline: *“What’s the capital city of France?”* → should still return `"Paris"`.

### 3. (Bonus) Implement Feedback Loop
Add a function:
```python
def add_feedback(query: str, correct_answer: str):
    # Append a new Q&A pair to dataset
```
- Purpose: capture corrected answers from users.
- Ensure safe handling (don’t overwrite data blindly).

### 4. Explain Your Approach
After coding, be prepared to explain:
- Why you chose your similarity threshold.
- How you would scale this system for larger datasets.
- How you would use the feedback loop to “teach” the system safely.

---

## 🔹 How to Run
```bash
python main.py
```

You can then type queries interactively. Type `quit` to exit.

---

## ✅ What We’re Looking For
- Correct handling of **regular, trick, and borderline queries**.
- Clean, readable code.
- Evidence of **system thinking** (not just coding).
- Bonus: ability to extend with safe feedback/learning loop.
