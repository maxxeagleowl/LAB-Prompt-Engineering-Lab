## Troubleshooting

- AuthenticationError [Error1.png]
  - cause: invalid or expired API key
  - error: "Incorrect API key provided"
  - fix:
    - set valid API key
    - load via os.environ["OPENAI_API_KEY"]
    - rerun test call

- NameError for sentiment_v2_analysis [Error2.png]
  - cause: cell not executed or wrong execution order
  - typical notebook issue
  - fix:
    - recalculate all analysis variables before comparison
    - add separate "recalculate" cell