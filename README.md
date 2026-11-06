# Skills

Agent skills I made for my own work. Each one exists because a real need came up in my day-to-day.

## Start here: say-it-plain

Ask your agent to explain anything, and understand the answer on the first read.

**Before**

> It's worth noting that the payment may have been impacted by a retry-related idempotency collision, which could potentially leave the ledger in a state that requires some attention.

**After**

> The customer's money is safe, but the ledger is wrong. Two payments shared one retry key, so the system saved only the first payment. You must add the second payment to the ledger.

Install it:

```bash
npx skills@latest add PabloZavi/skills --skill say-it-plain
```

Then use it at any time, on any topic:

```text
/say-it-plain how does our deploy work?
```

[Read more about say-it-plain](skills/say-it-plain)

## All skills

| Skill | Use it when |
|---|---|
| [say-it-plain](skills/say-it-plain) | You want a clear explanation of any topic, at any time. You can also make it always on in a project. |

I will add more skills here as new needs come up.

To choose from all the skills:

```bash
npx skills@latest add PabloZavi/skills
```

## Credits

[Matt Pocock's skills](https://github.com/mattpocock/skills) inspired me to publish mine.

## License

[MIT](LICENSE)
