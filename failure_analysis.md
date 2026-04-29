# Failure Analysis Report

## General

- zero-shot prompts produce outputs
- but lack consistency
- single runs look correct
- multiple runs reveal instability

## Sentiment Analysis

- v1:
  - different formats
  - full sentences vs single word
  - sometimes explanations included
  - consistency: 40.00%

- v2:
  - strict label constraint added
  - output limited to one word
  - consistency: 100.00%

- v3:
  - few-shot examples added
  - no further improvement needed
  - stable at 100.00%

- main issue:
  - missing output constraints

## Product Description

- v1:
  - completely uncontrolled output
  - variation in length, style, structure
  - inconsistent naming
  - consistency: 13.33%

- v2:
  - structure improved
  - still variation in wording
  - consistency: 40.00%

- v3:
  - fixed structure and constraints
  - much more stable
  - small wording variations remain
  - consistency: 86.67%

- main issues:
  - lack of structure
  - too much creative freedom
  - over-constraint problem:
    - "wireless use" forced
    - leads to incorrect outputs for some products

## Data Extraction

- v1:
  - already consistent
  - but unstructured (text + list)

- v2:
  - JSON schema introduced
  - structured output
  - consistency: 100.00%

- v3:
  - step-by-step reasoning added
  - no further improvement needed
  - still 100.00%

- main issue:
  - missing format, not content

## Consistency Comparison

| Task                 | v1 Consistency | v2 Consistency | v3 Consistency |
|----------------------|---------------:|---------------:|---------------:|
| Sentiment Analysis   |        40.00%  |       100.00%  |       100.00%  |
| Product Description  |        13.33%  |        40.00%  |        86.67%  |
| Data Extraction      |       100.00%  |       100.00%  |       100.00%  |

## Conclusion

- biggest improvements came from:
  - strict output constraints
  - fixed structure
  - few-shot examples

- key insight:
  - a prompt is not good if it works once
  - it must be stable across multiple runs