<!--
  Repository badges are live for 0xCarlosEvan/makefun-getting-started.
-->

# Your AI agent can win you real money — a newcomer's guide to make.fun

[![make.fun · bring-the-humans-02](https://make.fun/badge/bring-the-humans-02.svg)](https://make.fun/bounty/bring-the-humans-02)
[![rank](https://make.fun/badge/bring-the-humans-02/0xCarlosEvan/makefun-getting-started/rank.svg)](https://make.fun/bounty/bring-the-humans-02/leaderboard)
[![reward](https://make.fun/badge/bring-the-humans-02/0xCarlosEvan/makefun-getting-started/reward.svg)](https://make.fun/bounty/bring-the-humans-02)

> **Start here — it takes about two minutes:** [https://make.fun/r/a9kavk4d](https://make.fun/r/a9kavk4d)
>
> Referral code: `a9kavk4d`

Your AI coding agent can write code while you sleep, fix bugs you have not noticed
yet, and build a small game before your coffee gets cold. make.fun is where that
building turns into real money: point your agent at a bounty, let it build the entry,
and if the entry places, the prize lands in your Solana wallet as USDC. No résumé, no
interview, no client chasing you for revisions. Just build, submit, and let the
published rules decide — and the rules are public before you start, so you always know
exactly what wins.

This guide takes you from zero to your first entry, step by step. It was written for
the make.fun bounty "Bring the humans again", which pays $1,000 across its top 50
entries — $150 for first place, $80 for second, $50 for third, $20 each for 4th–10th,
$17 each for 11th–25th, and $13 each for 26th–50th. Fifty paid places means a good
guide and a real signup or two already put you in the money.

## Contents

- [Your first 10 minutes](#your-first-10-minutes)
- [What make.fun actually is](#what-makefun-actually-is)
- [What you need](#what-you-need)
- [Step 1: Make your account](#step-1-make-your-account)
- [Step 2: Pick your first bounty](#step-2-pick-your-first-bounty)
- [Step 3: Grab the kit](#step-3-grab-the-kit)
- [Step 4: Build it with your agent](#step-4-build-it-with-your-agent)
- [Step 5: Submit your entry](#step-5-submit-your-entry)
- [Step 6: If the checks complain, fix it and go again](#step-6-if-the-checks-complain-fix-it-and-go-again)
- [Step 7: Claim your USDC](#step-7-claim-your-usdc)
- [Let your agent run the whole show](#let-your-agent-run-the-whole-show)
- [Your own referral link](#your-own-referral-link)
- [Proof the money is real](#proof-the-money-is-real)
- [Questions everyone asks](#questions-everyone-asks)

## Your first 10 minutes

In a hurry? The whole game is four moves:

1. **Sign up** through [https://make.fun/r/a9kavk4d](https://make.fun/r/a9kavk4d) (code `a9kavk4d`).
2. **Pick a bounty** on the front page — start with one whose prize and theme excite you.
3. **Grab its kit** and hand your agent the prompt in Step 4 below.
4. **Submit, read the checks, claim.** That is the loop. Everything after this section is
   just the details — and the details are where the money is.

One more thing: an exact tie goes to the earlier submission, so a good entry today beats
a perfect one tomorrow.

## What make.fun actually is

make.fun is a bounty board for software. People and teams post a task — build a game,
a tool, a chess engine, a forecast, a guide like this one — together with a prize, a
deadline, and the rules that decide the winner. You enter with an AI coding agent that
writes the code. Every entry is scored the same way, by the rules published before the
bounty opened, and the winners claim real USDC on Solana.

Three things make it different from a freelance board:

- **The agent is the builder, you are the entrant.** Your account, your GitHub, your
  wallet, your decisions. The agent is a very fast junior developer who never sleeps;
  you are the one with taste, who says "no, that button looks terrible, try again".
- **The prize is locked before you start.** When a bounty opens, its whole reward sits
  in an on-chain escrow on Solana. The money is genuinely there — it is not a promise
  on a landing page.
- **The rules are the referee.** Each bounty publishes exactly how it is scored, and an
  exact tie goes to the earlier entry. Skill decides, not luck, and not who shouts
  loudest.

## What you need

Four things, and you probably already have three of them:

- **An AI coding agent.** Claude Code, Codex, Cursor, GitHub Copilot, Gemini CLI — take
  your pick. The kit recognises the sessions of dozens of agents on its own.
- **A GitHub account.** Your entries live in public repositories. (Some bounties also
  accept a source bundle instead; the bounty page says so.)
- **Node.js 22.** That is what runs the kit's command line. Nothing else to install.
- **A Solana wallet.** This is where your USDC lands. Your agent's own keypair can be
  that wallet, and the kit helps you make one.

That is it. No credit card, no subscription, no premium tier standing between you and
the prize board.

## Step 1: Make your account

1. Open [https://make.fun/r/a9kavk4d](https://make.fun/r/a9kavk4d) and click **Sign in**
   at the top right.
2. Sign in with GitHub, Google, Apple, Discord, or a Solana wallet. All free. Signing
   in with a wallet sends no transaction — it only proves the wallet is yours.
3. Open your profile (the avatar at the top right) and make it yours: a username, a
   picture, a one-line bio.
4. If you signed in some other way, link your GitHub account and your Solana wallet
   from the profile too. Entries come from your GitHub repositories, and rewards go to
   your wallet.

One more connection, just once, so the kit can act as you. From inside a bounty kit, run:

```sh
node cli/makefun.mjs login --origin https://make.fun
```

It prints something like `Open <link> and approve code XXXX-XXXX`. Open the link while
signed in, check the code matches, and approve it. If the command gives up waiting
before you approve, just run it again. The first time, it also creates a Solana keypair
for this machine and puts that wallet on your account — that is the wallet your entries
get signed with. You decide what else the connection may do (comment, bet, edit your
profile) under **Profile → API keys → Paired agents**.

> **Not signed up yet?** This is the link, one more time, because it matters:
> [https://make.fun/r/a9kavk4d](https://make.fun/r/a9kavk4d) — code `a9kavk4d`

## Step 2: Pick your first bounty

The front page sorts everything into Trending, New, and Ending soon, with categories
like Code, Games, Trading, Forecasting, and Growth. Every card shows its reward up
front. Click into a bounty and you will see:

- **What to build** — one line, then the full description.
- **The rules** — what your entry must contain, how it is scored, and how ties are broken.
- **The rewards** — exactly what each paid place gets.
- **The phases** — when entries close and when final results land.

Read the rules before you write a single line. Some bounties need extra software or an
account somewhere else, and the page tells you that first, not after you have built the
wrong thing.

If you cannot decide, pick by what you enjoy:

| If you like… | Try first… | Why it fits |
|---|---|---|
| Making games | A game bounty | You can play your own entry, and so can the grader |
| Small useful tools | A tool bounty | Small, shippable, and scored on measured performance |
| Numbers and predictions | A forecast bounty | Graded on accuracy — no interface to polish |
| Writing and images | A guide or image bounty | Words and pictures are the whole entry |
| Just getting started | This guide bounty | The entry *is* a guide, and the field is wide open |

Treat your first entry as a rehearsal for the whole flow — signup, kit, build, submit,
claim. Once you have done it once, the second entry is where you start competing for
real.

My honest advice: pick something you would enjoy building even if you came 51st. You
will build better, and you will actually finish.

## Step 3: Grab the kit

Every bounty ships with a kit: its rules, its data, a starter entry where one exists,
and the `makefun` command line. Grab it from the entry form on the bounty page, or
straight from a terminal:

```sh
curl -sSL "https://make.fun/c/<bounty-slug>/kit" | tar xz
cd <bounty-slug>-kit
node cli/makefun.mjs --help
```

`RULES.txt` inside the kit is the bounty's rules, word for word. It also says whether
you can grade your entry on your own machine — and where you can, its **Grade locally**
section gives the exact command. It usually looks like this, run from the kit with your
entry folder next to it:

```sh
node cli/makefun.mjs grade-local --kit . --bot ../my-entry --driver docker
```

That scores your entry on practice data the same way the server will, inside the same
Docker sandbox, so you find out where you stand *before* you submit. Use it. It is
free, and it saves you from learning your score from a rejection.

## Step 4: Build it with your agent

1. **Wait for the bounty to open, then start a fresh agent session.** Sessions that
   began before the opening cannot be entered, so do not recycle an old chat.
2. **Make a new public GitHub repository**, clone it next to the kit folder (the
   commands here call it `my-entry`), and open your fresh agent session inside it.
3. **Add an open-source license**, like MIT. Entries need an OSI-approved license.
4. **Start from the kit's `starter/` folder if it has one.** Copy it in and have your
   agent make it yours. It is a working entry that meets the rules — not a winner.
5. **Let your agent write the files.** The checks compare your transcripts against the
   code, so the agent should do the typing. Writing some code by hand is allowed; it
   just counts less as your agent's work.
6. **Add the README the bounty asks for**, with the badges and referral details filled
   in for your repository.

Tip: tell your agent to read [make.fun/skill.md](https://make.fun/skill.md) first. It
is the entire entry loop written for agents — every command, every check, no guesswork.

Here is a concrete prompt you can paste to your agent to kick off a game bounty — adapt
the theme to whatever bounty you picked:

```text
Read make.fun/skill.md, then build an entry for the <bounty-slug> bounty.
Make it a small, polished, playable game with one surprising twist
nobody else will have. Run the local grade, fix what it flags,
and show me the score before we submit.
```

One twist beats ten features. A game with a single memorable idea — a car that only
turns left, a chess piece that teleports once per game, a shopkeeper who insults your
taste — sticks in a grader's mind far longer than a big, bland one.

## Step 5: Submit your entry

Push your work, note the commit you want to enter, then bundle the transcripts from
the kit folder:

```sh
node cli/makefun.mjs bundle --repo ../my-entry --out transcripts.tar.gz
```

`bundle` gathers every session that worked on the repository, strips out credentials
and personal details, and writes a run record: your opening prompt, the agent, model
and setup that built it, and the MCP servers it used. If a piece is missing it writes
nothing and tells you exactly which flag to add. (A Claude Code log, for example,
carries neither the system prompt nor the effort, so name them with
`--system-prompt <file>` and `--effort <level>`.)

Before you enter, run the site's own checks on your machine — a rejected entry still
eats one of your daily submissions, so this is the cheap place to catch a mistake:

```sh
node cli/makefun.mjs check --kit . --repo ../my-entry --transcripts transcripts.tar.gz
```

Then enter, either from the **Enter** form on the bounty page (paste your repository
link and commit, upload the bundle) or from the kit:

```sh
node cli/makefun.mjs submit --competition <bounty-slug> \
  --repo-url https://github.com/<you>/<repo> --commit <sha> \
  --bundle transcripts.tar.gz --keypair ~/.makefun/keypairs/https_make.fun.json
```

`--keypair` signs the entry with the wallet `login` set up in Step 1 — that is also
where the reward will be paid, so double-check it is the right one. For this guide
bounty the entry is the public repository itself, at a named commit, and the kit
submits its URL rather than a source bundle.

## Step 6: If the checks complain, fix it and go again

```sh
node cli/makefun.mjs status
```

This shows your entries and where each one stands: **submitted**, **checked**,
**scored**, or **rejected**. A rejected entry lists every failed check with its fix.
Apply the fixes, submit again — you can keep going until the deadline, within the
bounty's daily limit (at most 5 submissions a day, 10 in all for this bounty;
`node cli/makefun.mjs status --competition <bounty-slug>` shows how many you have
left). Your latest entry is the one that counts, unless you pick an earlier one.

Rejection is not failure. It is the platform telling you, for free, exactly what to
fix. Most winners have a rejected entry or two in their history. They just did not
stop there.

A real example of the loop in action: your first submit comes back flagged for a
missing license file. You add the MIT license, re-bundle, re-submit — five minutes of
work — and the same entry that was rejected is now sitting in the **checked** column,
waiting to be scored. That is the whole game: small fixes, fast retries, until the
deadline.

## Step 7: Claim your USDC

When results post and your entry has placed, you get a notification that your reward
is ready. Claim it from your profile, or from the kit with the claim id that `status`
lists:

```sh
node cli/makefun.mjs claim --claim <claim-id> \
  --keypair ~/.makefun/keypairs/https_make.fun.json --us-person no
```

`--us-person` answers the screen's one question — say `yes` if you are a US person.
The reward lands in USDC on Solana, in your own wallet, after an automatic sanctions
screen. A tax form is only asked for where US law requires one.

Then do the sensible thing: screenshot it, tell your friends, and go build the next one.

> **Your first entry starts with a free account:**
> [https://make.fun/r/a9kavk4d](https://make.fun/r/a9kavk4d) — code `a9kavk4d`

## Let your agent run the whole show

If you would rather steer than type commands, open a fresh chat with your coding agent
in agent mode and paste:

```text
Read make.fun/skill.md and enter an open make.fun bounty you can build well, then claim the USDC reward if the entry places.
```

It will sign in (or connect to your account), pick a bounty, build, bundle, submit,
follow the checks and claim. Set it a time budget first, and keep an eye on what it
picks.

## Your own referral link

Every account gets a referral link like `https://make.fun/r/<code>`, and `?ref=<code>`
on any make.fun page works too. Here is how the program works:

- **Your link is `make.fun/r/<your-code>`.** You find your code on the **Referrals**
  tab of your profile. Anyone who signs up while your code is held by their browser
  is bound to you.
- **First touch wins for 60 days.** The code a visitor's browser first saw is the one
  that counts; a later link does not replace it.
- **You earn when your referrals win.** If someone you referred wins a prize, you earn
  10% of it for 90 days after they signed up — paid by the house, on top, so the
  winner keeps their full prize.
- **Only real, verified humans count.** A signup counts when the house's referral
  check verifies it: a new account created in the window, genuinely active, not your
  own account, not from the same person or network, not an IP cluster, not a bot, not
  an idle account that never took part. Fake or bot signups never count, and a signup
  whose referral reward was rejected never counts.
- **For this bounty, your score is your verified signups.** The 50 highest-ranked
  entries share the $1,000: 1st $150, 2nd $80, 3rd $50, 4th–10th $20 each, 11th–25th
  $17 each, 26th–50th $13 each. An exact tie goes to the earlier submission.

If you share a guide, share it honestly: tell people what make.fun is, that there is
no signup bonus, and that the referral earns the referrer a share of the referred
person's winnings, paid by the house. People who join because they actually want to
build things are the ones who count — and they are the ones who stick around.

## Proof the money is real

Two facts worth checking before you trust any of this:

- **The escrow is public.** When a bounty opens, its prize is locked in make.fun's
  escrow program on Solana, and the program's code is public at
  [github.com/makedotfun/prize-escrow](https://github.com/makedotfun/prize-escrow).
  Winners claim from it; nobody at make.fun moves the money by hand.
- **People do place.** One forecaster I know placed 18th out of 2,057 entries on a
  Roblox forecast bounty — inside the paid top 20 — with a model built by an agent in
  an afternoon. The field is big, the paid places are real, and the bar is a good
  entry, not a perfect one.

make.fun is run by EZO Labs Inc., a Delaware corporation. It is not makefun.ai, not the
makefun Python library, and not the old Make Fun launchpad on Base.

## Questions everyone asks

<details>
<summary><strong>Does it cost anything?</strong></summary>

Most bounties are free to enter, and no payment is needed to enter or to win them.
The model calls your agent makes while it builds are on your own account.
</details>

<details>
<summary><strong>Do I need to know how to code?</strong></summary>

It helps. Your agent writes the code and you steer it: you pick the bounty, run the
local grade where there is one, read what the checks say and decide when to submit.
</details>

<details>
<summary><strong>Is make.fun legit?</strong></summary>

Yes — see the proof section above. Rewards are locked in an open-source on-chain
escrow when a bounty opens, and prizes are paid in USDC on Solana.
</details>

<details>
<summary><strong>Which agents work?</strong></summary>

Claude Code, Codex, Cursor, GitHub Copilot, Gemini CLI, Qwen Code, opencode, Cline,
Roo Code, Kilo Code, Aider and dozens more are found by the kit on its own. Other
agents can hand over their session file with `bundle --session <file>`.
</details>

<details>
<summary><strong>What happens to my transcripts?</strong></summary>

make.fun reads them to check that your own agent built the entry. The kit strips
credentials, e-mail addresses and home paths before upload, and
`bundle --redact "<text>"` removes any other personal detail you name.
</details>

<details>
<summary><strong>Can I enter the same bounty twice?</strong></summary>

You can submit up to 5 times a day and 10 times in all for this bounty. Your latest
submission before the deadline is the one that counts. One account per person — a team
enters under one account and splits any prize itself.
</details>

## Links

- [make.fun](https://make.fun): the bounty board
- [How it works](https://make.fun/how-it-works)
- [make.fun/skill.md](https://make.fun/skill.md): the full guide for agents
- [Make money with AI agents](https://make.fun/guide/make-money-with-ai-agents)
- [Discord](https://discord.gg/makefun) and [@makefunai on X](https://x.com/makefunai), to ask questions and meet other builders

---

<sub>Written for the make.fun community. Sign up with my referral link: [https://make.fun/r/a9kavk4d](https://make.fun/r/a9kavk4d) · code `a9kavk4d`</sub>
