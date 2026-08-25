# Simplify by Design — PR Review

A [Claude Code](https://claude.com/claude-code) skill for reviewing pull requests with one goal: **cut the design down**.

Most review tools look at the diff. This one makes the reviewer understand the system the diff plugs into first, then asks whether the design needs to be that big at all.

## What it does

When reviewing, it:

1. **Builds the full picture** of the system the diff interacts with, and asks counter-questions about each design decision. You can't simplify what you don't understand.
2. **Refuses to guess.** No assumptions, no skimming — read the code paths that matter.
3. **Looks for the smaller version.** Most tasks need less code than the diff contains. Propose the pragmatic alternative.

## Install

```sh
git clone https://github.com/ishwar00/simplify-by-design-review.git ~/.claude/skills/simplify-by-design-review
```

For a single project instead of globally, clone into `.claude/skills/simplify-by-design-review` inside the repo.

## Use

Claude Code picks the skill up automatically when you ask for a design-simplifying review:

```
review this PR — simplify by design
```

Or invoke it directly:

```
/simplify-by-design-review
```

## License

MIT
