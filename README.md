# 🤖 Bot AI – Chat Application

A modern chat application built using **React** and **Material UI**, featuring AI-style responses, chat ratings, detailed feedback, and complete chat history stored in `localStorage`.

---

## 💬 Chat Engine

- Auto-scrolling conversation UI
- Human + AI styled message bubbles
- Suggested quick prompts
- Time formatting using `date-fns`
- Responsive layout for mobile + desktop

---

## 🧠 AI Response Logic

- Uses a local JSON file (`sampleData.json`) as a Q/A dataset
- Exact-match search for user questions
- Fallback message when no answer is found
- Each message includes:
  - `type` (Human / AI)
  - `text`
  - `id`
  - `time`
  - optional: `rating`, `feedback`

---

## ⭐ Ratings & Feedback

- 👍 Thumbs-up reaction
- ⭐ 1–5 star rating for AI messages
- 📝 Additional text feedback using a modal
- Rating + feedback stored directly in the message
- Read-only mode when shown in history view

---

## 💾 Chat Saving System

- Save full chat sessions to **localStorage**
- Saves:
  - Entire chat array
  - Timestamp
  - Feedback and ratings
- Shows snackbar confirmation
- Provides link to conversation history

---

## 📚 Chat History

- Displays all saved sessions
- Groups chats by:
  - Today
  - Yesterday
  - or formatted date (`do LLL yyyy`)
- Shows each message using `ChattingCard` in read-only mode

---

## 🔍 Filter System

- Filter conversation history by rating:
  - All Ratings
  - 1★, 2★, 3★, 4★, 5★
- Uses `.some()` to check whether any message in a chat has the selected rating

---

## 🎨 UI & Theme

- Built using **Material UI (MUI)**
- Consistent theme for:
  - Buttons
  - Cards
  - Modals
  - Typography
- Light/Dark mode toggle via `ThemeContext`
- Smooth hover and animation effects

---

## 📱 Mobile-Friendly Sidebar

- Collapsible sidebar for smaller screens
- Contains:
  - New Chat
  - History
  - Theme Toggle
- Sidebar auto-closes after selection

---

## 📂 Project Structure

```bash
src/
│
├── components/
│   ├── ChatInput/
│   │   └── ChatInput.jsx
│   ├── ChattingCard/
│   │   └── ChattingCard.jsx
│   ├── FeedbackModal/
│   │   └── FeedbackModal.jsx
│   ├── ChatHistoryCard/
│   │   └── ChatHistoryCard.jsx
│   ├── ChatFilter/
│   │   └── ChatFilter.jsx
│   ├── InitialChat/
│   │   └── InitialChat.jsx
│   ├── Sidebar/
│   │   └── Sidebar.jsx
│   ├── Navbar/
│       └── Navbar.jsx
│
├── aiData/
│   └── sampleData.json
│
├── pages/
│   ├── Home/
│   │   └── Home.jsx
│   └── History/
│       └── History.jsx
│
├── theme/
│   └── ThemeContext.js
│
├── App.js
└── index.js

```
