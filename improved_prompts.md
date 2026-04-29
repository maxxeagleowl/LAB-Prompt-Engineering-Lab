# Improved Prompts Documentation

## Sentiment Analysis v3

- added few-shot examples
- defined strict labels:
  - positive
  - negative
  - neutral
- output limited to exactly one word

result:
- no format variation
- 100% consistency

## Product Description v3

- introduced fixed structure:
  - Product
  - Price
  - Description
- added constraints:
  - 2 paragraphs
  - max word count
  - no unsupported features

- issue identified:
  - "wireless use" does not fit all products
  - adjusted to:
    - only include relevant features

result:
- strong improvement in consistency
- small wording variation remains
- 86.67%

## Data Extraction v3

- fixed JSON schema
- clearly defined fields
- step-by-step internal reasoning

result:
- fully structured output
- 100% consistency

## what worked best

- few-shot:
  - best for classification tasks
- structure + constraints:
  - critical for generative tasks
- chain-of-thought:
  - useful for structured extraction

## key learnings

- no constraints -> unstable output
- too many constraints -> incorrect content
- balance is critical