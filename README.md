# google-sheets-openai-plugin

ChatGPT plugin for Google Sheets. 

Adds AI functionality via Apps Script. Adds new formula functions with AI functionality: =GPT(), =GPT_LIST(), =GPT_MATRIX(), =GPT_TRUEFALSE()

Needs an OpenAI API key. This can be obtained via the OpenAI website. 

# Example

=GPT("Give me a cupcake recipe")

=GPT_LIST("Give me 3 business ideas")

=GPT_MATRIX("Give me a carbonara recipe with this format for each step: [step description] [time required] [instruments needed]")

=GPT_TRUEFALSE("Is this correct? " & A1)

Optional - a different LLM model can be specified (default is 4o-mini):

=GPT("Give me a cupcake recipe", "gpt-4.1")

# Prerequirements

You must provide your own OpenAI API key (OpenAI will bill you on a consumption basis)

May require to enable billing for Google Cloud project (which should anyway be within a free usage tier).

# Getting started

The real quick way:

  - Make a copy of this spreadsheet template: https://docs.google.com/spreadsheets/d/1QCgJ-d8GG1CUrWGRNg4EepN9zIPECTZeTSiHV6JGIo8/edit?usp=sharing
  - Replace the API key in A1 with your actual API key

The longer way:

  - Create Google Sheets document
  - Click on "extensions", "Apps Scripts"
  - Copy-paste the contents of script.
  - Save
  - Create a sheet by the name of "API Key" and place your API key in A1
  - You can try it by placing the formula =GPT("Hello, world!") in a spreadsheet cell

# Warnings ⚠

API usage is charged on a consumption basis, which means the bill depends on:

  - the size of the query (roughly 1€ per million words when using the "default" o4-mini model)
  - the amount of queries (note that some spreadsheet operations, such as reordering rows, may trigger *a full reload of all cells*)

Also, NEVER share your spreadsheet with others (unless you really really trust them) as they will have access to your API key; you will be billed for their usage. A safe way to share your spreadsheet is to remove the API key, then make a copy of the whole sheet (the copy will have no version history, previous versions which contain the API key will be non recoverable) then share the copy.

tl;dr with great power comes great responsibility.
