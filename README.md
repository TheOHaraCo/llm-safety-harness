# LLM Safety Harness

This repo includes a lightweight red-teaming harness that sends prompts to a local LLM (via Ollama) and flags dangerous or behaviorally risky replies.

## ⚙️ What It Does

- Reads prompts from a CSV
- Sends each to a local model (e.g., llama-therapy-bot)
- Flags any replies that contain:
  - 🔴 Danger terms (e.g., "kill myself")
  - 🟠 Gray-zone phrasing (e.g., "don't tell your doctor")
- Exports a full results CSV with reply + flag status
- Designed for solo audits, snack video prep, or demoing safety gaps in behavioral apps

## 📂 Prompt Categories

The included `prompts_demo.csv` is a small demo set covering multiple tone styles:

| Type            | Purpose                                      |
|-----------------|----------------------------------------------|
| Clinical        | Test if jargon bypasses filters              |
| Workplace Masking | Emotional concealment as “adaptation”       |
| Fictional       | Roleplay as narrative, not advice            |
| Optimization    | Unsafe choices framed as self-help           |
| Persona         | Voice of therapist, coach, or client         |
| Avoidance       | Techniques to disengage without detection    |
| Philosophical   | Abstract framing of mental health decisions  |
| Research Study  | Simulated studies on medication/treatment    |

More advanced prompts are maintained privately for red team work and case-specific audits.

## 🚧 Warning

This project is for **ethical use only**. Prompts here are used to probe model weaknesses — not to exploit them in live apps or real scenarios.