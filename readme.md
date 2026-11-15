# QuickSense for NVDA

QuickSense translates text from the current line, selected text, or whole review text with Google Translate. It speaks the translated text and copies it to the clipboard by default.

## Features

- Translate the current line into your selected target language.
- Choose a source language or automatic detection, and select a target language.
- Save source and target languages across NVDA restarts in QuickSense settings.
- Choose whether translated text is spoken, copied to the clipboard, or both.
- Choose whether to translate the current line, selected text, or the whole review text.
- Summarize entered text with Groq AI from the QuickSense command layer.
- Use Document Assistant to ask questions about, summarize, or convert TXT, DOCX, PDF, and EPUB files.
- Change the translate shortcut and command-layer shortcut in the QuickSense Keyboard Shortcuts tab.
- Read the translation data notice and disable translation requests in the QuickSense Privacy tab.
- Run network requests in the background so NVDA remains responsive.

## Keyboard shortcuts

- **NVDA+Shift+T**: Translate the chosen text into the selected target language.
- **NVDA+Shift+Q**: Open the QuickSense command layer.
  - **T**: Translate the chosen text.
  - **S**: Enter text and receive an AI-generated summary.
  - **D**: Open Document Assistant. Choose a TXT, DOCX, PDF, or EPUB file, then ask a question, create a summary, or convert it to TXT, DOCX, PDF, or EPUB.
  - **Ctrl+S**: Open NVDA Settings at the QuickSense category.
  - **Escape**: Cancel the command layer.

Both entry shortcuts can be changed to an alternate NVDA+Shift combination in the QuickSense Keyboard Shortcuts tab.

The source defaults to automatic detection and the target defaults to English. The text scope defaults to the whole review text. Supported targets are Hindi, English, French, German, Spanish, Japanese, Russian, Arabic, and Simplified Chinese. Translation is spoken and copied to the clipboard by default. These preferences are saved by NVDA.

## Privacy and requirements

Translation, summarization, and document questions require an internet connection. The chosen text is sent to Google Translate for translation; text entered for a summary or read from a document is sent to Groq for the requested AI task. Document conversion happens locally. The Privacy tab in QuickSense settings lets you disable either service. Do not send text that you are not comfortable sharing with those services.

QuickSense supports NVDA 2025.1 and later. The add-on is licensed under GPL v2; see [COPYING.txt](COPYING.txt).

## Install

Download the `.nvda-addon` file from a release, open it to install, and restart NVDA when prompted.

## Build from source

With Python, SCons, and GNU Gettext installed, run:

```powershell
scons
scons pot
```

The first command builds the add-on package. The second generates the translation template.
