# Inkspire
Turn any book title into a kid-friendly comic with auto-generated illustrations. Powered by n8n, OpenAI (chapter summaries), Black Forest Labs (FLUX) for images, and Notion (default) for output.

This is a minimal example for the Creative AI Agents Hackathon.

---

## 🚀 Project Overview

**What it does:**

* Takes a **book title** from an n8n **Form Trigger**.
* Uses **OpenAI** to generate **chapter-by-chapter summaries** (JSON).
* Builds simple art prompts and calls **BFL** to generate images.
* Outputs:

  * **Notion page** (one page per book; heading + summary + image per chapter)


---

## 🛠️ Setup Instructions

### Requirements

* n8n (Cloud or self-hosted)
* OpenAI API key
* Black Forest Labs API key
* (Optional) Notion Internal Integration Token

### Steps

1. **Clone**

```bash
git clone https://github.com/nur-rfz/inkspire.git
cd inkspire
```

2. **Import a workflow into n8n**

* Notion output: import `/n8n/book_to_comic_notion.json`

3. **Set credentials / variables in n8n**

* `OPENAI_API_KEY`, `BFL_API_KEY`
* Notion credential (paste token)

4. **Activate & run**

* Open the **Form Trigger** URL, enter a book title, submit.
* View the generated **Notion page**.

---

## 📁 Folder Structure (suggested)

```
/n8n/            # workflow JSON exports
/prompts/        # OpenAI + BFL prompt snippets
/docs/           # short setup notes
/examples/       # screenshots or sample deck
```

---

## 🧩 Tech Stack

n8n • OpenAI (summaries) • BFL/FLUX (images) • Notion  (output)

---

## 📜 License

MIT.

