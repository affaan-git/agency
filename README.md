<p align="center">
  <img src="icon.svg" alt="Monochrome letter-A monogram with circular flow" width="96" height="96">
</p>

# agency

Agent-related build skills for [Claude Code](https://code.claude.com).

## Install

```text
/plugin marketplace add anthropics/claude-plugins-community
/plugin install agency@claude-community
```

## Skills

### team-build

Leads an agent team through a build from a markdown plan, with explicit file ownership, contracts, and validation against real evidence. Confirms scope before starting and halts for review on anything unsafe, ambiguous, conflicting, or out of scope rather than guessing. It runs only when you invoke it.

```text
/agency:team-build <plan-path> [instruction]
```

- `plan-path` - path to a markdown file describing what to build.
- `instruction` *(optional)* - a scope note, preference, or constraint for the run.

Example:

```text
/agency:team-build plans/auth-refactor.md "scope to the service layer; leave the client untouched"
```

More skills will be added to `agency` over time.

## Credits

`team-build` is based on [build-with-agent-team](https://github.com/coleam00/context-engineering-intro/tree/main/use-cases/build-with-agent-team) and its adjacent content, distributed under the MIT License.
