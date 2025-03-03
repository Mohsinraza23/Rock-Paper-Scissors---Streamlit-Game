# 🪨📜✂️ Rock, Paper, Scissors - Streamlit Game

## 🎮 About the Project
This is a **modern and stylish** Rock, Paper, Scissors game built using **Streamlit** and **Python**. It allows users to play against the computer with a sleek UI, interactive buttons, and a reset option.

## 🛠️ Features
✅ **Play against AI** 🤖  
✅ **Modern UI with emojis** 🎨  
✅ **Stylish animations and buttons** ✨  
✅ **Reset button to restart the game** 🔄  
✅ **Made with Streamlit for easy web deployment** 🚀  

---

## 📌 How to Install & Run
Follow these simple steps to get started:

### 1️⃣ Install Python & Streamlit
Make sure you have Python installed. Then install Streamlit:
```bash
pip install streamlit
```

### 2️⃣ Clone or Download the Repository
```bash
git clone https://github.com/your-username/rock-paper-scissors
cd rock-paper-scissors
```

### 3️⃣ Run the Game
```bash
streamlit run app.py
```

---

## 🔍 Step-by-Step Code Explanation

### 📌 1. Import Required Modules
```python
import streamlit as st
import random
```
We import **Streamlit** for UI and **random** for generating AI choices.

### 📌 2. Add Custom CSS for Stylish UI
```python
st.markdown("""
    <style>
    body {
        background-color: #1e1e1e;
        color: white;
        font-family: 'Arial', sans-serif;
    }
    .stButton>button {
        width: 100%;
        font-size: 18px;
        padding: 10px;
        border-radius: 10px;
        transition: 0.3s ease-in-out;
    }
    .stButton>button:hover {
        background-color: #ff4757 !important;
        color: white !important;
    }
    </style>
""", unsafe_allow_html=True)
```
This makes buttons stylish and adds a dark theme.

### 📌 3. Display Game Title
```python
st.markdown("<h1 style='text-align: center; color: #ff4757;'>🪨📜✂️ Rock, Paper, Scissors</h1>", unsafe_allow_html=True)
st.write("### 🤖 Play against the Computer!")
```
A heading with emojis makes the UI engaging.

### 📌 4. User Input - Select Move
```python
choices = ["Rock ✊", "Paper 📜", "Scissors ✂️"]
user_choice = st.selectbox("👉 Select your move:", choices)
```
A dropdown menu for users to pick **Rock, Paper, or Scissors**.

### 📌 5. Play Button - Computer Makes a Choice
```python
if st.button("🔥 Play Now!"):
    computer_choice = random.choice(choices)
```
A button generates the computer’s random choice.

### 📌 6. Determine Winner
```python
user_choice_clean = user_choice.split(" ")[0]  # Extracts text only
computer_choice_clean = computer_choice.split(" ")[0]

if user_choice_clean == computer_choice_clean:
    result = "😮 It's a tie!"
elif (
    (user_choice_clean == "Rock" and computer_choice_clean == "Scissors") or
    (user_choice_clean == "Paper" and computer_choice_clean == "Rock") or
    (user_choice_clean == "Scissors" and computer_choice_clean == "Paper")
):
    result = "🎉 You win!"
else:
    result = "😢 Computer wins!"
```
This logic checks who wins.

### 📌 7. Display Results
```python
st.markdown(f"<h2 style='text-align: center; color: #ff4757;'>{result}</h2>", unsafe_allow_html=True)
```
Winner is displayed in a stylish red heading.

### 📌 8. Reset Button
```python
if st.button("🔄 Reset Game"):
    st.rerun()
```
This **resets the game** when clicked.

### 📌 9. Footer - Credits
```python
st.markdown("<h4 style='text-align: center; color: #ff4757;'>Made with ❤️ by Mohsin</h4>", unsafe_allow_html=True)
```
Displays a stylish footer with credits.

---

## 📌 Deployment on Streamlit Cloud
You can deploy this game online using Streamlit Cloud:
1. Push your project to GitHub.
2. Go to [Streamlit Community Cloud](https://share.streamlit.io/).
3. Connect your GitHub repository.
4. Select **app.py** as the main script.
5. Click **Deploy** and share the link!

---

## 💡 Future Improvements
🔹 Add a Scoreboard 🏆  
🔹 Add More Animations ⚡  
🔹 Add Multiplayer Mode 👥  

---

## 💌 Contact
Got any questions? Reach out!
📧 Email: mohsinraza2248@gmail.com  
🐙 GitHub: https://github.com/Mohsinraza23
  

Enjoy playing! 🎉🔥

