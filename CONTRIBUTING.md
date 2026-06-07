# Contributing

Pull requests welcome for:

- New skills exposing additional MentionsAPI endpoints
- Bug fixes in existing handlers
- Additional language ports (Node, Go, Rust)
- Documentation improvements

## Ground rules

- Skills must remain dependency-free. Use only the Python standard library (`urllib`, `json`, `os`).
- Each skill must pass `python3 -m unittest discover tests` from its skill directory before submission.
- Never commit credentials. The `MENTIONSAPI_KEY` environment variable is the only auth surface.
- Sign-off your commits (`git commit -s`).
- Match the existing handler error contract: return `{"error": "<code>", "detail": "<message>"}` instead of raising.

## Local development

```bash
git clone https://github.com/nikhonit/llm-mentions-skills.git
cd llm-mentions-skills/skills/mentions-full
MENTIONSAPI_KEY=lvk_live_... python3 -m unittest discover tests
```

## License

By contributing you agree that your contributions are licensed under the [MIT No Attribution](LICENSE) license.
