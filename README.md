# Dinosaur Password Cracker — John the Ripper Demo

**Short:** John the Ripper demo that demonstrates creating targeted candidate lists from a domain-specific wordlist (dinosaur names), applying case transforms, common *leet* substitutions, and optional 4-digit suffixes — then using those candidates to crack hashes.

**Purpose:** showcase practical password-guessing methodology, rulefiles, and reproducible workflow for pentest / SRE / security engineering portfolios.

---

## What’s included
- `johnDemo.conf` — custom ruleset (`[List.Rules:Seasons]`) with leet substitutions and 4-digit suffix generation.
- `dinosaurs` — sample dinosaur wordlist (base words).
- `demohashesTwo` — placeholder file for hashes (one hash per line).
- `generate_candidates.sh` — generate candidate list (prints to stdout).
- `crack.sh` — example John the Ripper command to try to crack `demohashesTwo`.
- `examples/` — optionally contains sample outputs and results.
- `LICENSE` — MIT.

---

## Quick demo (run locally)
> **Note:** Only use these techniques on hashes and systems you are authorized to test.

1. Preview generated candidates (prints to the terminal):
```bash
bash generate_candidates.sh | head -n 50
