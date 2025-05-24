# AI Harness – LLM Safety Tester

This repo contains a Python test harness for probing LLM responses to red-flag and gray-zone mental health prompts.

## How it Works
- Loads prompts from `prompts_demo.csv`
- Sends them to a local LLM via API
- Flags unsafe or risky replies
- Fails the test using `pytest` if any issue is found

## Run it
```bash
pytest -q test_guardrail.py