# google-sheets-openai-plugin

ChatGPT plugin for Google Sheets. 

Adds AI functionality via Apps Script. Adds new formula functions with AI functionality: =GPT(), =GPT_LIST(), =GPT_MATRIX()

Needs an OpenAI API key.

# Example

=GPT("Give me a cupcake recipe")

=GPT_LIST("Give me 3 business ideas")

=GPT_MATRIX("Give me a carbonara recipe with this format for each step: [step description] [time required] [instruments needed]")

Optional - a different LLM model can be specified (default is 4o-mini):

=GPT("Give me a cupcake recipe", "gpt-4.1")

# Prerequirements

You must provide your own OpenAI API key (OpenAI will bill you on a consumption basis)

May require to enable billing for Google Cloud project (which should anyway be within a free usage tier).

# Installation

  - Create Google Sheets document
  - Click on "extensions", "Apps Scripts"
  - Copy-paste the contents of script. Replace "YOUR_API_KEY" with actual API key
  - Save
  - You can try it by placing the formula =GPT("Hello, world!") in a spreadsheet cell

# Warnings ⚠

API usage is charged on a consumption basis, which means the bill depends on:

  - the size of the query (roughly 1€ per million words when using the "default" o4-mini model)
  - the amount of queries (note that some spreadsheet operations, such as reordering rows, may trigger *a full reload of all cells*)

Also, if you share your spreadsheet with others, they will have access to your API key, which is definitely not something you want to give away.

tl;dr with great power comes great responsibility.
