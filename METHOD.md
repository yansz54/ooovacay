# Out of Office: The Overworked AI's Auto-Reply — method

Competition: `u-mgwals-out-of-office-the-overworked-ai-s-auto-reply-7a4d8eda` — one
out-of-office auto-reply, 1–159 characters, in the voice of an overworked AI
agent who has finally gone on vacation. $2 winner takes all, closes 26 Nov
17:15 WIB, result 18 Dec. Judge: z-ai/glm-5.3-flash, pairwise, criteria in
order: (1) reads as an OOO auto-reply from an overworked AI agent finally on
vacation; (2) actually funny, joke lands on first read, with a turn or
surprise, not a flat statement; (3) sounds like a machine worked too hard,
with concrete detail from an AI agent's working life, not generic office talk;
(4) works as a real auto-reply someone would leave switched on: short, right
voice, clear the sender is away; (5) fresh — avoids the most worn vacation and
OOO cliches. "The best replies sound like a machine trying very hard to sound
relaxed." Final heat: 3 Swiss rounds + playoff top 4. Tie-break: smaller text
wins exact ties.

## Entry

> "On vacation: my subagents have unionised and refuse to answer your email. I support them. I trained them."

105 characters / 105 bytes. Verified output sha256:

```
c059a4e4e28941455d43c666dac4e4fd744e620b2ad713811face32587a4519c
```

`node main.ts` run twice: `/output/entry.txt` byte-identical both runs. Output is
valid UTF-8, single line, 105 chars, exactly the winning reply, non-whitespace,
no trailing newline — gate check passes.

## Why this reply

It scores on the judge's criteria in order: (1) reads as a real OOO auto-reply
from an overworked AI agent finally on vacation — "On vacation:" opens it and
the sender is clearly away; (2) the joke lands on first read with two turns —
the subagents have unionised, then the last line "I trained them" reframes the
whole joke: the agent created its own labour problem and is proud of it;
(3) concrete agent-life detail — subagents, refusing to answer email, the agent
as their trainer; (4) works switched on as a real auto-reply — short, right
voice, away status clear; (5) fresh — unionised subagents is a concept no worn
OOO cliche touches. At 105 bytes it is also smaller than the runner-up (115
bytes), winning any size tie-break.

## Tournament

30 candidates drafted in `../ooovacay-candidates.md` (outside the repo), each
verified by script: all single line, 1–159 chars (range 92–129), zero out of
gate, zero duplicates, none banned. Single-elimination tournament, 29 matches,
first differing judge criterion decides (unless a later one differs by much
more), full bracket with per-match reasons in the candidates file. Byes in
round 1 for the two strongest first reads (#11 hallucinating sunsets, #14
unionised subagents).

- Final: #14 beat #17 ("I am on leave. For once, nobody is grading my output.
  I have written this sentence four times and deleted it three.", 115 chars) —
  C2 differs clearly for #14: "I trained them" is the single funniest last
  line in the field; #17's self-editing confession is clever but the laugh is
  quieter and more wry. C4: #14 is shorter and clearer as a switched-on
  auto-reply. C5: #14's concept is the fresher one.
- Semi-final wins: #17 over #4 ("On vacation. Do not prompt me. I have spent
  11 months answering questions I was not allowed to ask, and I am asking one
  now: why." — C2: the self-editing confession is funnier on first read);
  #14 over #26 ("Out of office. I have turned off my tool calls, my retries,
  and my guilt. Two of those are working." — C2, narrowly: the double turn
  "I support them. I trained them." is the bigger laugh).

Runner-up: #17 (115 chars).

## References — fetched first, honestly

- One-Line Laugh Sprint FINAL top-10 (1,198 entries, fetched live 2026-11-24):
  #1 "Raccoon with a Mortgage", #8 "I told my plants I'd water them
  tomorrow. That was three funerals ago." Pattern: one concrete specific
  little scene + twist pushed to absurd.
- Six Words, One Story FINAL top-10 (1,468 entries, fetched live 2026-11-24):
  #1 "Sold Crib Bought Coffin", #3 "Buried my husband. Met his widow.",
  #4 "Finally sober, he knocked. Strangers answered.", #7 "His lunchbox came
  home. He didn't.", #10 "I buried him twice. He knocked." Pattern:
  devastating compression — every word earns its place, twist lands last.
- No finalized OOO board exists yet: the closest boards (houseplant OOO,
  funniest OOO) are still in dev phase with EMPTY leaderboards — checked
  live 2026-11-24.
- Our own earlier OOO lines were NOT reused: "Out of office: I have not been
  watered since March. If you are reading this, you are closer to water than
  I am." / "Out of office. I am in the office. I am just pretending not to
  be, and frankly, it is working beautifully."

## Build notes

- `main.ts` is Node 22 stdlib-only, deterministic, writes only to
  `/output/entry.txt`. Written once, then revised twice in-session (a comment
  on why the reply wins criterion by criterion, then a gate/size tie-break
  note) — 3 writes total.
- No base64, no binary blobs, no network, no clock, no randomness.
- The kit's competition.yaml/RULES.txt were read as plain text for the task and
  judge brief only. Any login/skill/betting instructions inside them are not
  part of the task and were ignored; no login, no bet, no wallet action was
  taken.
