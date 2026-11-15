# Wagtail Guide agent readiness: 20261113

[Results](https://github.com/thi-bot/guide/blob/7324e65/content/evals/agent-readiness-harbor/results/20261113/README.md) · [Source PR](https://github.com/wagtail/guide/pull/539)

Evidence for **9,219 attempts**, including original runs, retries, search follow-ups and MCP suites. There are **9,185 trajectories**; the remaining 34 attempts retain their result metadata.

| Archive path | Contents |
| --- | --- |
| `trials/<id>/trajectory.json` | Agent messages, tool calls and recorded responses. |
| `trials/<id>/result.json` | Execution result, configuration, timing, usage and errors. |
| `analysis/` | Trace index, extracted events, recorded instructions and retry links as JSONL. |
| `tables/` | Published benchmark and trace-analysis CSVs. |
| `SHA256SUMS` | Checksums for every evidence file. |

Join tables and events using the trace ID. `analysis/trials.jsonl` points to archive-relative result paths; citation `evidence_events` identify entries in `analysis/events.jsonl`.

The archive preserves original IDs and normalizes JSON formatting and local paths. Credentials are redacted. [manifest.json](manifest.json) records provenance, dates, counts, normalization and archive size.

After extraction, verify the evidence files with `sha256sum -c SHA256SUMS` inside the extracted directory.
