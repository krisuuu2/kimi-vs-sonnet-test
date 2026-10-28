# Kimi K3.1 Pro vs Claude Sonnet 5.5: a 10-minute side-by-side test

Kimi K3.1 Pro (Moonshot AI) scored 65.7 on Terminal-Bench 4.0, right behind Claude Opus 5.5 at 66.4 (Moonshot's own table), and its API costs half of Opus. On the independent Artificial Analysis Intelligence Index it ranks 4th overall, at about $2 per task vs about $6 for Opus. But on that same index Claude Sonnet 5.5 scores one point higher, at the same list price per token ($2 / $10 per 1M).

So don't switch because of a post. Test it on your own work.

🇵🇱 Polska wersja: [PL.md](PL.md)

## The test (about 10 minutes)

1. Pick ONE real task from your week (a function to fix, a report to write, data to clean). Not a benchmark question.
2. Open [OpenRouter](https://openrouter.ai) and run the task prompt below twice, with the same input: once on `moonshotai/kimi-k3.1-pro`, once on Claude Sonnet 5.5 (check the exact model IDs in the OpenRouter model list).
3. Paste both answers into a fresh chat with the judge prompt, blind (call them A and B).
4. Compare: the judge score, how much you had to fix by hand, and the cost of each run (OpenRouter → Activity).

## Task prompt

```
You are doing a real task for me. Context: <paste files / data / brief>.
Task: <what done looks like, in one sentence>.
Constraints: <format, length, tools, things to avoid>.
Before you answer, list any assumption you had to make. Then give the final result only.
```

## Judge prompt (blind)

```
Two answers, A and B, to the same task are below. Score each 1-10 on:
correctness, completeness, following the constraints, and how much editing it needs before I can use it.
Quote the single worst mistake in each. Then say which one you would ship, in one line.
Task: <task prompt>
A: <answer 1>
B: <answer 2>
```

## Rule of thumb

If the cheaper run ships the same result with no more hand edits, switch that task. Keep the other tasks where they are. A low price per token is not a low bill: cost per task depends on how many tokens each model burns, so compare the real bill.

## Sources

- Moonshot AI, Kimi K3.1 Pro: https://www.kimi.ai/blog/kimi-k3-1-pro (Terminal-Bench 4.0 numbers are vendor-reported; full weights by Nov 4, 2026)
- VentureBeat, 24.10.2026: https://venturebeat.com/technology/moonshots-kimi-k3-1-pro-flirts-with-open-weights-leadership-amid-paid-influencer-scandal-allegations (prices, Artificial Analysis ranking and cost per task, the unverified creator brief)
- Artificial Analysis: https://artificialanalysis.ai

Made by [@aipractically](https://www.instagram.com/aipractically/).
