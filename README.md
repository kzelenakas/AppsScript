# AppsScript

Google Apps Script tools for AI-powered text classification — built for categorizing and analyzing data inside Google Sheets and Google Workspace.

## Table of Contents

- [What These Do](#what-these-do)
- [File Reference](#file-reference)
- [Setup](#setup)
- [Usage](#usage)

---

## What These Do

These scripts connect Google Sheets to large language model APIs to classify and categorize text data at scale — without leaving Google Workspace. Useful for categorizing revision requests, appraiser feedback, or any large dataset with text entries that need to be sorted into categories.

---

## File Reference

| File | Description |
|------|-------------|
| `LLMCategoryClassifier.gs` | Classifies text entries into predefined categories using an LLM API. Reads input from a Google Sheet column and writes category results back. |
| `LLMTextClassifier.gs` | General-purpose LLM text classifier — flexible category definitions, configurable prompt, handles batch processing. |
| `text_classifier.gs` | Lightweight text classifier — rule-based or API-backed classification for simpler category sets. |

---

## Setup

1. Open your target Google Sheet
2. Go to `Extensions > Apps Script`
3. Paste or import the relevant `.gs` file
4. Add your API key to the script properties: `Project Settings > Script Properties`
   - Key: `ANTHROPIC_API_KEY` or `OPENAI_API_KEY` depending on which service the script calls
5. Save and authorize the script when prompted

**Never hardcode API keys directly in the script source.** Use Script Properties for all credentials.

---

## Usage

Each script is designed to run on a selected column of text in a Google Sheet:

1. Paste your text data into column A (or configure the input column in the script)
2. Run the classifier function from `Extensions > Apps Script > Run`
3. Results are written to the adjacent column

For large datasets, the scripts handle batching automatically to stay within API rate limits.
