---
"@richardgill/pi-background-bash": minor
---

Report results the way Pi's built-in `bash` tool does, without changing how processes are managed.

- Declare an `outputSchema` so codemode scripts receive an object (`output`, `exit_code`, `truncated`) instead of text; structured output is capped at 1 MiB, read from the end of the log.
- Return `isError: true` and the `Command exited with code N` line when a command exits non-zero.
- Append `Full output: <path>` only when output was truncated.
