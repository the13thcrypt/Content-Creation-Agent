# 🎙️ Content Creation Agent

A simple, single-page web application that uses the Google Gemini API to generate premium podcast scripts and related content ideas based on user inputs.

This tool provides a clean UI for content creators to quickly brainstorm and script their next podcast episode.

## ✨ Features

  * **Podcast Script Generation:** Creates detailed, professional podcast scripts.
  * **Content Idea Generation:** Provides 3-5 related content ideas (like future topics, guest suggestions, or different formats) based on the main topic.
  * **Customizable Inputs:** Users can specify:
      * Podcast Topic / Theme
      * Desired Tone (e.g., informative, humorous, expert-level)
      * Target Audience (e.g., young professionals, tech enthusiasts)
      * Approximate Duration (in minutes)
  * **Simple Interface:** A clean, responsive UI built with Tailwind CSS.
  * **Client-Side API Call:** All logic is contained in a single `index.html` file, making it easy to run locally.
  * **Loading & Error Handling:** Provides feedback to the user during API calls and if an error occurs.

## 🛠️ Technologies Used

  * **HTML5:** For the basic structure.
  * **Tailwind CSS (via CDN):** For all styling and UI components.
  * **Vanilla JavaScript (ES6+):** For all client-side logic, including:
      * DOM manipulation
      * `fetch` API for `async/await` calls
      * A simple custom Markdown-to-HTML converter
  * **Google Gemini API:** The generative AI model (`gemini-2.5-flash`) used to generate the content.

## 🚀 Getting Started

This is a single-file project. To run it locally, you only need a web browser and a valid Google Gemini API key.

### 1\. Download the File

Clone this repository or just download the `index.html` file.

```bash
git clone https://github.com/your-username/your-repository-name.git
```

### 2\. Get Your API Key

1.  Go to **Google AI Studio** ([https://aistudio.google.com/app/apikey](https://aistudio.google.com/app/apikey)).
2.  Create a new API key.

### 3\. Add Your API Key

Open the `index.html` file in a code editor (like VS Code, Sublime Text, or Notepad).

Find this line (around line 100):

```javascript
const GEMINI_API_KEY = "AIzaSyDTBUAQb8C3yBtyxItGHwzWZ4pn6nIhjGU";
```

Replace the placeholder key with **your own Google Gemini API key**.

```javascript
// Replace this with your actual key
const GEMINI_API_KEY = "YOUR_REAL_API_KEY_GOES_HERE";
```

### 4\. Run the Application

Simply **open the `index.html` file in your web browser** (e.g., Chrome, Firefox, Safari). The application will run locally.

## ⚠️ Important Security Warning

This project is designed for **personal, local use only.**

The Google Gemini API key is **hardcoded directly into the `index.html` file**.

  * **DO NOT** deploy this file to a public web server (like GitHub Pages, Netlify, or Vercel) as-is.
  * If you do, **your API key will be exposed** to the public, and anyone can steal it and use it, which could result in charges to your account.

### How to Deploy Safely

If you want to deploy this project publicly, you **must** create a server-side backend (e.g., using Node.js, Python, or PHP). The backend would:

1.  Receive the topic, tone, etc., from the frontend.
2.  Securely store and use your API key to call the Gemini API.
3.  Send the generated content back to the frontend.

This prevents your API key from ever being visible in the client-side code.

## 📖 How to Use

1.  Open `index.html` in your browser.
2.  Fill in the **"Podcast Topic / Theme"** field.
3.  Fill in the **"Desired Tone"** (e.g., "inspirational and practical").
4.  Fill in the **"Target Audience"** (e.g., "anyone seeking stress reduction").
5.  Set the **"Approximate Duration"**.
6.  Click the **"Generate Script & Ideas"** button.
7.  Wait for the loading indicator to finish.
8.  Your results will appear in the "Podcast Script" and "Content Ideas" sections below.
