# SecureScan 🛡️

An AI-powered code security reviewer that scans your code for vulnerabilities, rates them by severity, and gives you actionable fixes — all in a single HTML file with no install required.

![SecureScan](https://img.shields.io/badge/version-0.2-00d4ff?style=flat-square) ![License](https://img.shields.io/badge/license-MIT-00ff88?style=flat-square) ![Powered by](https://img.shields.io/badge/powered%20by-Groq%20%2B%20Llama%203.3-ff9900?style=flat-square)

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
- **Scan history** — last 20 scans saved locally via localStorage
- **PDF export** — print any report to PDF with one click
- **Multi-language** — Python, JavaScript, Java, C/C++, SQL, Bash, Go, PHP, Ruby
- **Zero dependencies** — single HTML file, no npm, no server, no build step

---

## Getting started

### 1. Get a free Groq API key

Sign up at [console.groq.com](https://console.groq.com) — no credit card required.

### 2. Run the app

Just open `securescan-v2.html` in your browser. No server needed.

```bash
# Clone the repo
git clone https://github.com/YOUR_USERNAME/securescan.git
cd securescan

# Open in browser (Mac)
open securescan-v2.html

# Open in browser (Windows)
start securescan-v2.html
```

### 3. Paste your API key and scan

Enter your Groq API key in the field at the top, paste some code, and hit **Scan Code**.

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
| Storage | Browser localStorage |
| Fonts | IBM Plex Sans + IBM Plex Mono |

---

## Roadmap

- [ ] GitHub repo URL scanning
- [ ] User-supplied API key support for deployment
- [ ] Scan diff comparison (before vs. after fix)
- [ ] Overall project scoring across multiple files
- [ ] VS Code extension

---

## License

MIT — see [LICENSE](LICENSE) for details.

---

## Author

Built by **Brian Wallenrod** · [Portfolio](https://brianw51629.github.io/WebsitePortfolio/) · [LinkedIn](https://linkedin.com/in/brianwallenrod)
