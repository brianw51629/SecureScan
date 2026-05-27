# SecureScan 🛡️

An AI-powered code security reviewer that scans your code for vulnerabilities, rates them by severity, and gives you actionable fixes — no install required.

![SecureScan](https://img.shields.io/badge/version-0.2-00d4ff?style=flat-square) ![License](https://img.shields.io/badge/license-MIT-00ff88?style=flat-square) ![Powered by](https://img.shields.io/badge/powered%20by-Groq%20%2B%20Llama%203.3-ff9900?style=flat-square) ![Live](https://img.shields.io/badge/live-GitHub%20Pages-00ff88?style=flat-square)

## 🔗 [Try it live → brianw51629.github.io/securescan](https://brianw51629.github.io/securescan)

---

## What it does

SecureScan analyzes code for common security vulnerabilities using the Groq API (Llama 3.3 70B). Paste a snippet or upload a file and get back a full security report with severity ratings, descriptions, and concrete fixes.

**Detects vulnerabilities including:**
- SQL Injection
- Cross-Site Scripting (XSS)
- Hardcoded secrets and API keys
- Insecure authentication patterns
- Path traversal
- Command injection
- Insecure cryptography
- And more — anything the model can reason about

---

## Features

- **Paste or upload** — paste code directly or drag and drop a file
- **Risk grade (A–F)** — instant overall security rating per scan
- **Severity levels** — CRITICAL / HIGH / MEDIUM / LOW with color coding
- **Actionable fixes** — concrete remediation advice for each finding
- **Scan history** — last 20 scans saved locally in your browser
- **PDF export** — print any report to PDF with one click
- **Multi-language** — Python, JavaScript, Java, C/C++, SQL, Bash, Go, PHP, Ruby
- **Zero dependencies** — no npm, no server, no build step

---

## Getting started

### Option 1 — Use the live version (easiest)

Go to **[brianw51629.github.io/securescan](https://brianw51629.github.io/securescan)**, enter your free Groq API key, and start scanning. Your key is saved in your browser — you only enter it once.

### Option 2 — Run locally

```bash
# Clone the repo
git clone https://github.com/brianw51629/securescan.git
cd securescan

# Open in browser (Mac)
open index.html

# Open in browser (Windows)
start index.html
```

### Get a free Groq API key

Sign up at [console.groq.com](https://console.groq.com) — no credit card required. Your key stays in your browser and is never uploaded anywhere.

---

## Example

Try pasting this classic SQL injection vulnerability:

```python
query = "SELECT * FROM users WHERE username = '" + username + "' AND password = '" + password + "'"
```

SecureScan will flag it as **CRITICAL**, explain why it's dangerous, and show you how to fix it using parameterized queries.

---

## Risk grade breakdown

| Grade | Meaning |
|-------|---------|
| A | No vulnerabilities found |
| B | Low-severity issues only |
| C | Medium-severity issues present |
| D | High-severity issues present |
| F | Critical vulnerability detected |

---

## Tech stack

| Layer | Technology |
|-------|-----------|
| Frontend | Vanilla HTML, CSS, JavaScript |
| AI Model | Llama 3.3 70B via Groq API |
| Hosting | GitHub Pages |
| Storage | Browser localStorage |
| Fonts | IBM Plex Sans + IBM Plex Mono |

---

## Roadmap

- [ ] GitHub repo URL scanning
- [ ] Scan diff comparison (before vs. after fix)
- [ ] Overall project scoring across multiple files
- [ ] VS Code extension

---

## License

MIT — see [LICENSE](LICENSE) for details.

---

## Author

Built by **Brian Wallenrod** · [Portfolio](https://brianw51629.github.io/WebsitePortfolio/) · [LinkedIn](https://linkedin.com/in/brianwallenrod)
