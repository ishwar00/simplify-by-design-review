# Simplify by Design

A skill for [Claude Code](https://claude.com/claude-code) and [Codex](https://github.com/openai/codex) with one goal: **cut the design down**.

It applies to anything being worked on — a plan, a PR, a discussion. Most review tools look at the diff. This one makes the reviewer understand the problem and the system first, then asks whether the design needs to be that big at all.

## What it does

1. **Solves the right problem.** Pins down the objective, motivation, and success criteria before anything else. Asks clarifying questions when the ask is unclear; states the assumption when it cannot ask. Then questions the product design, with data wherever possible.
2. **Builds the full picture** of the system the work interacts with. You can't simplify what you don't understand.
3. **Counter-questions each design choice.**
4. **Lays out the options**, including ones that defy the assumed constraints, and picks the simplest one that holds.

Underneath: no guessing, no settling on the first thought, and the skill overrides any "take the first lazy answer" rule while active.

## Install

Claude Code:

```sh
git clone https://github.com/ishwar00/simplify-by-design-review.git ~/.claude/skills/simplify-by-design-review
```

Codex:

```sh
git clone https://github.com/ishwar00/simplify-by-design-review.git ~/.codex/skills/simplify-by-design-review
```

Both at once — clone once, symlink the rest:

```sh
git clone https://github.com/ishwar00/simplify-by-design-review.git ~/work/simplify-by-design-review
ln -s ~/work/simplify-by-design-review ~/.claude/skills/simplify-by-design-review
ln -s ~/work/simplify-by-design-review ~/.codex/skills/simplify-by-design-review
```

For a single project instead of globally, clone into `.claude/skills/simplify-by-design-review` inside the repo.

## Use

Invoke it directly:

```
/simplify-by-design-review <PR url, plan, or question>
```

Or ask for it by name:

```
review this plan — simplify by design
```

## License

MIT
