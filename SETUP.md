# GitHub Actions setup

This fork is preconfigured for an AI-focused Chinese/English daily digest. It watches Hacker News, selected RSS feeds, Reddit, and AI SDK releases, then publishes the result to GitHub Pages every day.

## One required step

Add an Actions repository secret named `OPENAI_API_KEY`:

1. Open **Settings → Secrets and variables → Actions** in this repository.
2. Select **New repository secret**.
3. Name it `OPENAI_API_KEY` and paste an OpenAI API key as its value.
4. Open **Actions → Daily Horizon Summary → Run workflow** to generate the first briefing.

The scheduled workflow runs at 23:00 UTC (07:00 China Standard Time). Until the secret is added, the workflow intentionally skips instead of failing.

To change the sources, model, language, or filtering threshold, edit `data/config.github.json`. Do not commit API keys; use GitHub Actions secrets.
