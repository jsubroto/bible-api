# 📖 Bible JSON API (KJV + ASV)

Access the full text of the **Bible** in **structured JSON format** — including the **King James Version (KJV)** and **American Standard Version (ASV)** — served as a static API via GitHub and **jsDelivr CDN**.

> ✅ No backend needed. No rate limits. Just fast, reliable, free Bible data.

---

## 📦 Features

- 📚 Complete: All books, chapters, and verses of KJV and ASV
- ⚡ CDN-backed: Served via [jsDelivr](https://www.jsdelivr.com/) for fast global access
- 🧠 Machine-readable: Perfect for developers, researchers, and Bible app builders
- 🔓 Open: Free to use, modify, or redistribute (public domain)

---

## 🌐 Usage (Like an API)

### ▶️ Fetch a Chapter via HTTP

```http
GET https://cdn.jsdelivr.net/gh/jsubroto/bible-api@latest/versions/kjv/books/genesis/chapters/1.json
```

### ▶️ Example JavaScript

```js
const version = "kjv";
const book = "genesis";
const chapter = 1;

fetch(`https://cdn.jsdelivr.net/gh/jsubroto/bible-api@latest/versions/${version}/books/${book}/chapters/${chapter}.json`)
  .then(res => res.json())
  .then(data => {
    console.log("Genesis 1:1", data.verses[0].text);
  });
```

> 💡 You can replace "kjv" with "asv" to access other translations.

---

## 📁 Data Structure

Each chapter file (shown here in readable format) looks like this:

```json
{
  "version": "KJV",
  "book": "Genesis",
  "chapter": "1",
  "verses": [
    {
      "verse": 1,
      "text": "In the beginning God created the heaven and the earth."
    },
    {
      "verse": 2,
      "text": "And the earth was without form, and void; and darkness was upon the face of the deep."
    }
  ]
}
```

*…truncated for brevity…*

---

## 🔧 Use Cases

- ✝️ Bible apps and scripture readers
- 🔍 Full-text search engines
- 🧠 Natural Language Processing (NLP) & machine learning
- 📝 Study tools, devotionals, journaling apps
- 🧪 Side projects, hackathons, or open data experiments

---

## 📜 License

- 📖 Text: Public Domain (KJV and ASV are not under copyright)
- 🧰 Code & Structure: MIT License

---

## 💬 Credits

- Text scraped from BibleGateway
- Inspired by developers who want an open Bible API without needing a backend

---

## ⭐️ Support

If you find this useful:

- ⭐ Give it a star!
- 🧑‍💻 Contribute via pull requests
- 📢 Share with friends or communities

> Want to add more translations? Open an issue or PR!
