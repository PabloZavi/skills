# say-it-plain

An agent skill that explains any topic so you understand it on the first read. Use it at any time. You do not have to be lost first.

```bash
npx skills@latest add PabloZavi/skills --skill say-it-plain
```

## Use it

Type `/say-it-plain`, with or without a topic. If your agent has no slash commands, ask it to use the `say-it-plain` skill.

```text
/say-it-plain
/say-it-plain why did the payment fail?
/say-it-plain how does our deploy work?
```

With no topic, it explains what the agent last said or did. Your agent can also load it by itself when you ask for a simple explanation or say that you did not understand.

## What changes

**Before**

> It's worth noting that the payment may have been impacted by a retry-related idempotency collision, which could potentially leave the ledger in a state that requires some attention.

**After**

> The customer's money is safe, but the ledger is wrong. Two payments shared one retry key, so the system saved only the first payment. You must add the second payment to the ledger.

## Why it is so short

A long skill about short answers contradicts itself, and the agent has more text to forget. This skill has nine rules.

"Be concise" also has a problem: agents obey it by cutting words, and the result is shorter but not clearer. For that reason, the rules keep "because" and "but". Without them, the reader gets a list of facts and must guess how they connect.

## Use it always in a project

An AI tool without skill support can still follow the rules: paste them into your chat or its custom instructions.

A skill applies only when it loads. To apply the rules to every answer in a project, copy the nine rules from [SKILL.md](SKILL.md) into the project's `CLAUDE.md` or `AGENTS.md`.

## Credits

- The rules are inspired by [ASD-STE100 Simplified Technical English](https://www.asd-ste100.org/). This skill is not affiliated with ASD, does not include the STE dictionary, and does not claim conformance with the specification.
