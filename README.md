# ig-chatbot1
for kira bot 
# Instagram Chatbot with DialoGPT

A flirty, classy Instagram chatbot powered by **DialoGPT** and hosted for free on **Render**.

---

## 🔹 How it works
- User DMs you on Instagram.
- Meta (Facebook) forwards the message to this bot.
- The bot uses **DialoGPT** to generate a natural, human-like reply.
- Sometimes it drops your **dfans link** in a playful, classy way.

---

## 🔹 Setup Instructions

### 1. Create GitHub Repo
- Add these files: `server.py`, `requirements.txt`, `README.md`.

### 2. Deploy on Render
- Go to [https://render.com](https://render.com).
- New → **Web Service** → connect this GitHub repo.
- Environment = Python 3.
- Start command = `python server.py`.

### 3. Add Environment Variables
In Render dashboard → Environment → Add:

| Key              | Value                                |
|------------------|--------------------------------------|
| VERIFY_TOKEN     | any secret word (e.g. `mysecret`)    |
| PAGE_ACCESS_TOKEN| from Meta Developer (Messenger API)  |
| FB_APP_SECRET    | from Meta Developer (App Settings)   |
| DFANS_LINK       | https://dfans.com/yourusername       |

### 4. Meta Developer Setup
- Go to [https://developers.facebook.com](https://developers.facebook.com).
- Create a Business App.
- Add products: **Messenger** + **Instagram Graph API**.
- Generate **Page Access Token** for your Instagram Business account.
- In **Webhooks**, set:
  - Callback URL = `https://yourbot.onrender.com/webhook`
  - Verify Token = your chosen word
- Subscribe to: `messages`, `instagram_messaging`.

### 5. Test
- Add your IG account as a Tester in the Meta App.
- Send a DM → bot replies flirty + sometimes drops your dfans link.

---

## 🔹 Free Hosting
This runs on **Render free plan**:
- 750 free hours/month.
- Can sleep when idle but auto wakes up.

---
