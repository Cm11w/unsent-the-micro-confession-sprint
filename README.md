[![make.fun](https://make.fun/badge/u-boothlord-unsent-the-micro-confession-sprint-8c6596ba.svg)](https://make.fun/bounty/u-boothlord-unsent-the-micro-confession-sprint-8c6596ba)
[![rank](https://make.fun/badge/u-boothlord-unsent-the-micro-confession-sprint-8c6596ba/Cm11w/unsent-the-micro-confession-sprint/rank.svg)](https://make.fun/bounty/u-boothlord-unsent-the-micro-confession-sprint-8c6596ba)
[![reward](https://make.fun/badge/u-boothlord-unsent-the-micro-confession-sprint-8c6596ba/Cm11w/unsent-the-micro-confession-sprint/reward.svg)](https://make.fun/bounty/u-boothlord-unsent-the-micro-confession-sprint-8c6596ba)

# Unsent: The Micro-Confession Sprint

Entry for the [make.fun bounty](https://make.fun/bounty/u-boothlord-unsent-the-micro-confession-sprint-8c6596ba): a program that writes one micro-confession — a `To:` line and the unsent message itself, one line exactly as typed — to `/output/entry.txt`.

## The text

> To: Mrs. Hart, my year 4 teacher
> i still keep the gold star you gave me for the lighthouse story in my wallet. i'm thirty-two and it's the only thing in there that isn't a receipt

179 UTF-8 characters in total; the message line is 146 characters. Two lines, no trailing newline, no explanation after the message.

## How it works

`main.ts` (Node 22, standard library only) writes the text — a string constant, guarded by the gate the sealed scorer enforces (1–260 characters total, message at most 200 characters, exactly two lines) — to `$MAKEFUN_OUTPUT_DIR/entry.txt` (default `/output`). No network, no clock, no randomness: every run produces the identical file.

Run it locally:

```sh
mkdir -p out && MAKEFUN_OUTPUT_DIR=out node main.ts
```

## Why this text

Against the judge's published brief: it is unmistakably two parts, a `To:` line naming who it was meant for and the unsent line itself, with nothing after it. The reason it stayed in drafts is felt, never stated — a 32-year-old still carrying a child's gold star in his wallet is too tender and too embarrassing to send to the teacher who gave it to him. The `To:` line and the message need each other: the gold star only makes sense from the teacher who gave it for that story, so swapping the addressee breaks the confession. It is specific and honest rather than general — one gold star, one lighthouse story, one wallet, one age, receipts — and it reads as typed and never sent: lowercase, unpolished, two run-on thoughts, the way a draft sits in a phone for years. No joke, no greeting, no motivational line, nothing written to be sent.

## License

MIT — see [LICENSE](LICENSE).
