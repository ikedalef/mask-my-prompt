# 🛡️ MaskMyPrompt
> **In-Browser Confidential AI Prompt Sanitizer & De-anonymizer**  
> Use ChatGPT, Claude, and Gemini without leaking client secrets, deal sizes, or PII.

Live Tool: [https://ikedalef.github.io/mask-my-prompt/](https://ikedalef.github.io/mask-my-prompt/)

---

## 💡 The Problem
Millions of solo entrepreneurs, consultants, and teams paste raw client emails, contracts, and proposals into LLMs every day.  
Doing so often violates strict Non-Disclosure Agreements (NDAs) and privacy regulations (GDPR, HIPAA, CCPA) by exposing:
- Customer names & personal email addresses
- Sensitive contract figures & hourly rates
- Proprietary vendor and company identities
- Private phone numbers

Sending this data to external AI servers creates permanent audit trails and data leak vulnerabilities.

---

## 🔒 The Solution: 100% Client-Side Isolation
**MaskMyPrompt** replaces identifying entities with temporary tokens (`[COMPANY_1]`, `[AMOUNT_1]`, `[EMAIL_1]`) **directly inside your web browser**.

- **Zero Cloud Storage**: No backend servers, databases, or API tracking.
- **Zero Network Transmission**: Your unmasked confidential text never touches a network request.
- **Volatile In-Memory Mapping**: Redaction tokens live exclusively in your local session memory. Closing the tab immediately destroys the translation keys.
- **1-Click De-anonymization**: Paste the AI's response back into the tool to seamlessly restore original names, emails, and amounts before sending it to your client.

---

## 🛠️ How It Works

1. **Mask (Before AI)**: Paste raw client text. The in-browser regex engine tokenizes PII and saves the mapping table locally.
2. **Copy to LLM**: Copy the sanitized prompt directly to ChatGPT or Claude. The AI understands the context without ever seeing sensitive identities.
3. **Unmask (After AI Replies)**: Paste the AI response back. The engine maps tokens back to the original entities instantly.

---

## 📜 Privacy Guarantee & Verification
You can independently verify the security of MaskMyPrompt:
1. Open your browser's Developer Tools (`F12` or `Ctrl + Shift + I`).
2. Go to the **Network** tab.
3. Paste confidential text and click **Sanitize**.
4. Observe that **zero HTTP requests** are sent. All processing is strictly local.

---

## 💻 Tech Stack
- **Pure Client-Side JavaScript**: No external dependencies or remote execution.
- **Tailwind CSS**: Clean, responsive UI.
- **GitHub Pages**: Transparent static hosting.
