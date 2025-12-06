# 🛡️ Fortnight: The Truth Engine

> **"We are the signal. Everything else is just noise."**

[](https://opensource.org/licenses/MIT)
[](https://www.google.com/search?q=)
[](https://www.google.com/search?q=)

Fortnight is an autonomous, multimodal intelligence designed to verify information in real-time. It operates as a "Glass Box" system, providing not just verdicts, but the complete chain of evidence used to reach them.

**[Read The Manifesto](https://www.google.com/search?q=MANIFESTO.md)**

-----

## 🏗️ Architecture: The Hybrid Mind

Fortnight uses a **Bicameral AI Architecture** to balance speed and reasoning depth:

```mermaid
graph TD
    A[Input Stream] -->|Video/Audio| B[The Eyes (Gemini 2.5 Flash)]
    A[Input Stream] -->|Text| C[The Judge (Gemini 3.0 Pro)]
    B -->|Visual Description| C
    C -->|Deep Reasoning| D{The Economy Filter}
    D -->|Free User| E[Verdict Only]
    D -->|Pro User| F[Verdict + Evidence Chain]
```

1.  **The Eyes (Perception):** Uses **Gemini 2.5 Flash** for sub-second analysis of live video streams, detecting deepfakes, lip-sync errors, and visual context mismatches.
2.  **The Judge (Reasoning):** Uses **Gemini 3.0 Pro** in "Deep Think" mode to analyze claims, detect logical fallacies, and cross-reference internal knowledge bases.
3.  **The Cloud Watchtower:** A Python-based ingestion engine that monitors 24/7 news feeds (IPTV/YouTube) and broadcasts verdicts via WebSockets.

-----

## 🚀 Deployment (The Automation Factory)

We use a **Prompt-as-Code** philosophy. You do not edit Python files to change the AI's behavior; you edit the `prompts.yaml` file.

### **1. Prerequisites**

  * Google Cloud Project with **Cloud Run** & **Artifact Registry** enabled.
  * **Gemini API Key** from Google AI Studio.
  * **GitHub Secrets** configured: `GCP_CREDENTIALS`, `GEMINI_API_KEY`.

### **2. Directory Structure**

```text
fortnight/
├── .github/workflows/   # CI/CD Pipeline (Auto-deploy to Cloud Run)
├── Dockerfile           # Production container definition
├── main.py              # Flask Server + Hybrid AI Logic
├── prompts.yaml         # The Brain (System Instructions)
├── requirements.txt     # Dependencies (Flask, Google-GenAI)
└── deploy-config.yaml   # Service Name Configuration
```

### **3. How to Deploy**

Commits to the `main` branch trigger the **Universal Deployer** pipeline:

1.  GitHub Actions builds the Docker container.
2.  Pushes image to Google Artifact Registry.
3.  Deploys live to **Google Cloud Run**.

<!-- end list -->

```bash
git add .
git commit -m "Updated truth logic"
git push origin main
# 🚀 Deployment completes in ~60 seconds
```

-----

## 💻 The Client Ecosystem

Fortnight is a headless platform serving three distinct frontends:

| Platform | Tech Stack | Key Feature |
| :--- | :--- | :--- |
| **Mobile** | React Native | **Audio Sync:** "Shazam for Truth" (Fingerprints room audio) |
| **Smart TV** | React Native TVOS | **Passive Shield:** Truth Ticker overlay on live news |
| **Web Pro** | Next.js | **Investigation Board:** Deep-dive graph visualization |

-----

## ⚖️ The Economy (Business Logic)

The API enforces a strict separation between **Revenue** and **Truth**.

  * **Free Tier (`user_tier: FREE`):**
      * **Verdict:** ✅ Visible (True/False/Misleading)
      * **Evidence:** ❌ Redacted ("Upgrade to see sources")
      * **Latency:** Standard
  * **Pro Tier (`user_tier: PRO`):**
      * **Verdict:** ✅ Visible
      * **Evidence:** ✅ Full Citation Chain (NASA, Reuters, Nature)
      * **Reasoning:** ✅ "Deep Think" Logic Trace
      * **Forensics:** ✅ Deepfake Probability Score

-----

## 🛠️ Local Development

To run the Truth Engine locally:

1.  **Clone the repo:**

    ```bash
    git clone https://github.com/rmcwilliams2004/forthright.git
    cd forthright
    ```

2.  **Set Environment Variables:**

    ```bash
    export GEMINI_API_KEY="your_key_here"
    ```

3.  **Run the Server:**

    ```bash
    pip install -r requirements.txt
    python main.py
    ```

4.  **Test a Claim:**

    ```bash
    curl -X POST http://localhost:8080/verify \
         -H "Content-Type: application/json" \
         -d '{"user_tier": "PRO", "data": "The moon is made of cheese"}'
    ```

-----

## 📜 The Fortnight Compact

We pledge:

1.  **Zero Interference:** We never alter a verdict for money.
2.  **Zero Sponsorship:** We do not protect lies for advertisers.
3.  **Glass Box:** If we are wrong, we show you *why* the AI made the mistake.

*Built for the Second Society.*
