# 🤖 Telegram Job & System Alert Pipeline

## 📌 Problem Statement
Managing daily system alerts or manually monitoring job boards is time-consuming. This project establishes an automated, lightweight notification pipeline directly integrated with Telegram API using Linux native CLI tools.

## 🛠️ Stack & Technologies Used
* **OS:** Ubuntu / WSL2 (Linux)
* **Shell Scripting:** Bash
* **Network & Data Transfer:** `curl` (HTTP POST Requests)
* **Data Format:** JSON
* **Automation:** Systemd / Cron

## 🚀 Key Features & Implementation
1. **API Integration:** Leveraged Telegram's `sendMessage` HTTP endpoint via `curl` with payload parameters (`chat_id`, `text`).
2. **Silent Execution:** Standardized flags (`-s`, `-X POST`) to prevent stdout pollution during background operations.
3. **Security:** Isolated API credentials using environment variables instead of hardcoding sensitive tokens.

## 💡 Troubleshooting & Technical Insights
* **Issue:** `curl` request failed with HTTP 400 Bad Request due to unescaped special characters in text parameters.
* **Solution:** Standardized input string quoting and implemented URL encoding for query parameters before firing payload.

## 💻 Quick Usage
```bash
./scripts/send_alert.sh "Server load critical: >80%"
