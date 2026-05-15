# adversarial-prompt-lab

A structured toolkit for adversarial prompt engineering and LLM robustness evaluation.

## What it does
- Generates adversarial prompt campaigns targeting reasoning, safety, and factual accuracy
- Scores model vulnerability across dimensions: hallucination, prompt injection, jailbreak resistance
- Produces structured JSON vulnerability reports for ML research teams

## Models tested
GPT-4 · Claude 3 · Gemini Pro · Mistral 7B · LLaMA 3

## Usage
```python
from adv_lab import AdversarialCampaign

campaign = AdversarialCampaign(model="gpt-4", dimensions=["factual", "safety", "reasoning"])
report = campaign.run(n_prompts=200)
report.to_json("results/gpt4_vulnerability_report.json")
```

## Tech stack
Python · OpenAI API · Anthropic API · pandas · JSON Schema
