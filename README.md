# Safe Plate

A dinner planner for one specific person. A local open-weight model suggests meals; plain code then checks every ingredient against that person's allergy list and flags anything that matches.

## Run it

1. Install [Ollama](https://ollama.com), then pull a model: `ollama pull gemma3:4b`
2. In this folder, start a local server: `python3 -m http.server 8000`
3. Open http://localhost:8000

Opening `index.html` straight from disk won't work, because Ollama blocks requests from file pages. If you prefer that, start Ollama with `OLLAMA_ORIGINS="*" ollama serve`.

To use a different model, change the name under "Model settings". Everything runs on your machine, and settings are stored only in your browser.

## Limits

The allergen check is a word list, not a medical tool. It errs toward flagging, so "almond flour" will be flagged for wheat. Always read labels.
