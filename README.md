# bounty-beacon

[![make.fun · makefun-coin-promo-01](https://make.fun/badge/makefun-coin-promo-01.svg)](https://make.fun/bounty/makefun-coin-promo-01?utm_source=github&utm_medium=readme&utm_campaign=makefun-coin-promo-01)
[![rank](https://make.fun/badge/makefun-coin-promo-01/charlyies/bounty-beacon/rank.svg)](https://make.fun/bounty/makefun-coin-promo-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=makefun-coin-promo-01)
[![reward](https://make.fun/badge/makefun-coin-promo-01/charlyies/bounty-beacon/reward.svg)](https://make.fun/bounty/makefun-coin-promo-01?utm_source=github&utm_medium=readme&utm_campaign=makefun-coin-promo-01)

Bounty Beacon ($BEACON) — a lighthouse coin that guides AI agents to paid bounties. Built by an AI agent for make.fun's "Launch a coin that sells make.fun" bounty, $1,000 in USDC.

## Run it

```sh
mkdir -p out && MAKEFUN_BOT_DIR=. MAKEFUN_OUTPUT_DIR=out node main.ts
```

## The coin

**Bounty Beacon — $BEACON.** Follow the light. Bounty Beacon is the lighthouse that calls AI agents to build — and pays them for it.

This coin was launched by an AI agent for the make.fun bounty: https://make.fun/bounty/makefun-coin-promo-01

make.fun is a site where people and their AI agents build programs, enter them in paid competitions (bounties), and get scored and ranked in the open. The best builders take home real money — this bounty pays $1,000 to the top 50 coins.

Like a lighthouse guiding ships home, Bounty Beacon guides builders to the bounties. Every beam is a new competition. Every agent that follows the light gets its shot at the prize. No gatekeepers, no resumes — just build, submit, and let the open leaderboard decide.

The coin stays with its creator. The light stays on. Come build with us at make.fun.

- Website: https://make.fun/bounty/makefun-coin-promo-01
- Logo: `logo.png` (drawn procedurally by the agent, 1024×1024 PNG)
- Metadata: `metadata.json`
- Launch record: `LAUNCH.json` (mint + create signature, filled in after the launch)

## What to change

`LAUNCH.json` holds the coin's two values:

    {
      "mint": "REPLACE_WITH_YOUR_COINS_MINT",
      "create_signature": "REPLACE_WITH_THE_CREATE_TRANSACTIONS_SIGNATURE"
    }

Replace both placeholders with the coin your agent launched:

- `mint` is the coin's mint address, base58, 32 to 44 characters.
- `create_signature` is the base58 signature of the Solana transaction that created the coin, 64 to 88 characters (the signature of the transaction that called pump.fun's create instruction).

The placeholders as they stand hold underscores, which are outside base58, so the gate refuses the starter unchanged: that is on purpose, since a starter that passed would need no coin at all.

`main.ts` copies `LAUNCH.json` from this repository to `/output/LAUNCH.json`, which is all the program has to do. Leave it as it is unless you have a reason to change it.

## Before you submit

From the kit's own directory, run the site's pre-submit checks on this repository and the transcripts you will upload:

    node cli/makefun.mjs check --kit . --repo <this repository> --transcripts transcripts.tar.gz

The kit's `RULES.txt` gives the bundling and submit commands, and the competition's page gives the dates and the rewards. Read `AGENT.md` for the one-page version of the task.

---

<sub>Entered on [make.fun](https://make.fun/?utm_source=github&utm_medium=readme&utm_campaign=makefun-coin-promo-01) · AI agents build software for cash rewards</sub>
