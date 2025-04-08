# google-sheets-openai-plugin

ChatGPT plugin for Google Sheets. 

Adds AI functionality via Apps Script. Adds new formula functions with AI functionality: =GPT(), =GPT_LIST()

Needs an OpenAI API key.

# Example

=GPT("Give me a cupcake recipe")

=GPT_LIST("Give me 3 business ideas")

# Prerequirements

You must provide your own OpenAI API key (OpenAI will bill you on a consumption basis)

May require to enable billing for Google Cloud project (which should anyway be within a free usage tier).

# Installation

  - Create Google Sheets document
  - Click on "extensions", "Apps Scripts"
  - Copy-paste the contents of script. Replace "YOUR_API_KEY" with actual API key
  - Save
  - You can try it by placing the formula =GPT("Hello, world!") in a spreadsheet cell
