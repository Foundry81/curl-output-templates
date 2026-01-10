# Curl Output Templates
*Intentional output for practical troubleshooting*
![VHS CLI Recording](./readme-assets/cli-demo.gif)

Curl is already a powerful tool. These templates focus on making its output clearer, more consistent, and more useful during real troubleshooting scenarios.

Each template is designed to answer a single diagnostic question without unnecessary noise.

## What This Repository Contains

- Opinionated curl --write-out templates
- Plain text files intended for reuse and versioning
- Output designed for humans first, automation second

These templates are based on practical use, not theoretical completeness.

## What This Repository Does Not Attempt

- Teaching curl fundamentals
- Capturing every available metric
- Providing a single “catch-all” command

Staying cool comes from focus.

## Using the Templates
Each file contains a complete curl command.

You can:
- Copy and paste the contents directly
- Or download the file and reference it for repeatable use

Example pattern:
`curl -s -o /dev/null -w "$(cat performance-timing.txt)" https://example.com`

Adjust as needed for your shell and environment.

## Output Philosophy
All templates in this repository follow the same principles:

- One purpose per template
- Metrics ordered by request lifecycle
- Readable under pressure
- Deliberate inclusions and omissions

If the output doesn’t lead to a clear conclusion, it needs refinement.

## Available Templates

- **performance-timing.txt**
Identify where time is spent during an HTTP(S) request.
- **api-sanity.txt**
Validate status, content type, and basic response characteristics.
- **tls-diagnostics.txt**
Inspect TLS version, cipher, and certificate verification behavior.
- **redirect-behavior.txt**
Understand request flow across redirects and front-door infrastructure.
- **log-keyvalue.txt**
Produce consistent, single-line output suitable for repeated collection.

## Modifying Templates

These templates are starting points.

When modifying:
- Add metrics intentionally
- Remove metrics confidently
- Keep output aligned to a single diagnostic question

Consistency matters more than completeness.

## Contributing New Templates

New templates should meet the same standard as existing ones.

Before adding a template, ask:
- What single question does this output answer?
- Can two engineers reach the same conclusion from this output?
- Are all included metrics defensible?
- Can any metric be removed without weakening the purpose?

Templates that try to do too much should be split.

## Context
These templates come from real troubleshooting scenarios where high-level monitoring wasn’t enough and clearer request-level visibility was required.

Curl didn’t need new features. It needed better output.

