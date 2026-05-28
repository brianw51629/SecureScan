# SecureScan 🛡️

An AI-powered code security reviewer that scans your code for vulnerabilities, rates them by severity, and gives you actionable fixes — no install required.

![SecureScan](https://img.shields.io/badge/version-0.3-00d4ff?style=flat-square) ![License](https://img.shields.io/badge/license-MIT-00ff88?style=flat-square) ![Powered by](https://img.shields.io/badge/powered%20by-Groq%20%2B%20Cerebras-ff9900?style=flat-square) ![Live](https://img.shields.io/badge/live-GitHub%20Pages-00ff88?style=flat-square)

## 🔗 [Try it live → brianw51629.github.io/SecureScan](https://brianw51629.github.io/SecureScan)

---

## What it does

SecureScan analyzes code for common security vulnerabilities using AI (Groq or Cerebras). Paste a snippet, upload a file, or compare two versions of your code and get back a full security report with severity ratings, confidence scores, descriptions, and concrete fixes.

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
- **Compare mode** — scan two versions of the same code side by side and see exactly what was fixed, what's new, and what's unchanged
- **Confidence scores** — each finding includes an AI confidence bar (0–100%) so you know which issues are definite vs speculative, sorted highest confidence first
- **False positive button** — dismiss findings you disagree with; the grade recalculates instantly and dismissals persist across rescans
- **Risk grade (A–F)** — instant overall security rating per scan, updated in real time as you dismiss findings
- **Severity levels** — CRITICAL / HIGH / MEDIUM / LOW with color coding
- **Actionable fixes** — concrete remediation advice for each finding
- **Scan history** — last 20 scans saved locally in your browser
- **PDF export** — print any report to PDF with one click
- **Multi-provider** — works with Groq (Llama 3.3 70B) or Cerebras (GPT-OSS 120B)
- **Multi-language** — Python, JavaScript, Java, C/C++, SQL, Bash, Go, PHP, Ruby
- **Zero dependencies** — no npm, no server, no build step

---

## Getting started

### Option 1 — Use the live version (easiest)

Go to **[brianw51629.github.io/SecureScan](https://brianw51629.github.io/SecureScan)**, enter your free API key, and start scanning. Your key is saved in your browser — you only enter it once.

### Option 2 — Run locally

```bash
# Clone the repo
git clone https://github.com/brianw51629/SecureScan.git
cd SecureScan

# Open in browser (Mac)
open index.html

# Open in browser (Windows)
start index.html
```

### Get a free API key

**Groq** — sign up at [console.groq.com](https://console.groq.com). No credit card required.

**Cerebras** — sign up at [cloud.cerebras.ai](https://cloud.cerebras.ai). No credit card required. 1M tokens/day free — great for heavier usage.

Your key stays in your browser and is never uploaded anywhere.

---

## Example

Try pasting this to see confidence scores and multiple vulnerability types at once:

```python
import os, sqlite3, hashlib

SECRET_KEY = "myapp_secret_123"

def get_user(username):
    conn = sqlite3.connect("users.db")
    query = "SELECT * FROM users WHERE username = '" + username + "'"
    conn.execute(query)

def hash_password(password):
    return hashlib.md5(password.encode()).hexdigest()

def run_command(cmd):
    os.system(cmd)

def read_file(filename):
    return open("/uploads/" + filename).read()
```

SecureScan will flag SQL injection, hardcoded secret, weak hashing, command injection, and path traversal — each with a confidence score showing how certain the AI is about each finding.

---

## Risk grade breakdown

| Grade | Meaning                         |
| ----- | ------------------------------- |
| A     | No vulnerabilities found        |
| B     | Low-severity issues only        |
| C     | Medium-severity issues present  |
| D     | High-severity issues present    |
| F     | Critical vulnerability detected |

Grades recalculate in real time as you dismiss false positives.

---

## Tech stack

| Layer    | Technology                                      |
| -------- | ----------------------------------------------- |
| Frontend | Vanilla HTML, CSS, JavaScript                   |
| AI Model | Llama 3.3 70B (Groq) or GPT-OSS 120B (Cerebras) |
| Hosting  | GitHub Pages                                    |
| Storage  | Browser localStorage                            |
| Fonts    | IBM Plex Sans + IBM Plex Mono                   |

---

## Roadmap

- [x] Confidence scores per finding
- [x] False positive dismissal
- [x] Before/after compare mode
- [ ] Custom rules — always flag specific patterns
- [ ] VS Code extension
- [ ] GitHub repo URL scanning

---

## License

MIT — see [LICENSE](LICENSE) for details.

---

## Author

Built by **Brian Wallenrod** · [Portfolio](https://brianw51629.github.io/WebsitePortfolio/) · [LinkedIn](https://linkedin.com/in/brianwallenrod)
