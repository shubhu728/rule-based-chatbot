# rule-based-chatbot
rule based chatbot
1. index.html:-
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Rule-Based Chatbot</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

<div class="chat-container">
    <h2>🤖 RuleBot</h2>

    <div id="chatbox"></div>

    <input type="text" id="userInput" placeholder="Type a message..." />
    <button onclick="sendMessage()">Send</button>
</div>

<script src="script.js"></script>
</body>
</html>

2.style.css:-
body {
    font-family: Arial;
    background: #f0f2f5;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
}

.chat-container {
    width: 350px;
    background: white;
    padding: 15px;
    border-radius: 10px;
    box-shadow: 0 0 10px gray;
}

#chatbox {
    height: 300px;
    overflow-y: auto;
    border: 1px solid #ccc;
    padding: 10px;
    margin-bottom: 10px;
}

.user {
    text-align: right;
    color: blue;
}

.bot {
    text-align: left;
    color: green;
}

3.script.js:-
function sendMessage() {
    let input = document.getElementById("userInput");
    let message = input.value.toLowerCase();

    let chatbox = document.getElementById("chatbox");

    // Show user message
    chatbox.innerHTML += `<div class="user">You: ${message}</div>`;

    let response = "";

    if (message.includes("hello") || message.includes("hi")) {
        response = "Hi there! 😊";
    } 
    else if (message.includes("name")) {
        response = "Mera naam RuleBot hai 🤖";
    } 
    else if (message.includes("how are you")) {
        response = "Main bilkul theek hoon! 😄";
    } 
    else if (message.includes("bye")) {
        response = "Bye! 👋";
    } 
    else {
        response = "Sorry, mujhe samajh nahi aaya 😅";
    }

    // Show bot response
    chatbox.innerHTML += `<div class="bot">Bot: ${response}</div>`;

    input.value = "";
    chatbox.scrollTop = chatbox.scrollHeight;
}

4. README.md:-
# 🤖 Rule-Based Chatbot (Web Version)

This is a simple chatbot built using HTML, CSS, and JavaScript.

## 🚀 Features
- Rule-based responses
- Interactive UI
- Beginner friendly

## 🛠️ How to Run
1. Download project
2. Open `index.html` in browser

## 💬 Example
User: hello  
Bot: Hi there!
