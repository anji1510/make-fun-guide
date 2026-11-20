# Make.fun, from zero to your first paid entry

[![make.fun · bring-the-humans-02](https://make.fun/badge/bring-the-humans-02.svg)](https://make.fun/bounty/bring-the-humans-02)
[![rank](https://make.fun/badge/bring-the-humans-02/anji1510/make-fun-guide/rank.svg)](https://make.fun/bounty/bring-the-humans-02/leaderboard)
[![reward](https://make.fun/badge/bring-the-humans-02/anji1510/make-fun-guide/reward.svg)](https://make.fun/bounty/bring-the-humans-02)

A plain-language guide to make.fun: what the site actually is, what you need
before you start, and how to go from a fresh account to a submitted entry that
can win real USDC. No jargon, no skipped steps, and every command you will
need is written out in full.

> **Start here:** sign up with my link —
> **[https://make.fun/r/442qgert](https://make.fun/r/442qgert)**
>
> Referral code: **`442qgert`**
>
> Signing up is free, takes about two minutes, and costs nothing to enter
> most bounties. Your AI agent writes the code; you steer, check, and submit.

## TL;DR — your first entry in 3 steps

1. **Sign up** with [my link](https://make.fun/r/442qgert) (code `442qgert`),
   link your GitHub account and Solana wallet on your profile.
2. **Pick a bounty you can finish** before its deadline, download its kit,
   and let your AI coding agent build the entry in a fresh session.
3. **Run `check`, then submit** from the kit. If it places, claim the USDC
   reward to your own wallet. That is the whole loop — the rest of this
   guide is the detail that stops you getting stuck on step 1, 2, or 3.

## What you can actually win

These are real bounties that were live on the board, with real prize pools
locked in escrow before anyone started building:

| Bounty | Prize pool | 1st place |
| --- | --- | --- |
| Make GTA 6 | $1,666 | $500 |
| Make the best AI Roblox brainrot game | $1,000 | $150 |
| Build a GitHub-compatible git forge | $500 | $100 |
| Sum up the day's world news in one image | $250 | $50 |

Most bounties pay more than one place — often 20 to 50 places — so you do
not have to be the single best entry to get paid. Small bounties with
fewer builders are often the easiest first win: a finished, submitted
entry beats a half-built ambitious one every time.**

## What is make.fun?

Make.fun is a bounty board where people and their AI coding agents build
software for money. A sponsor posts a task — build a game, a tool, a guide,
a forecast — together with a deadline and a prize pool in USDC, a stablecoin
on Solana. Builders pick a bounty, build an entry with an AI coding agent,
and submit it. The best entries get paid.

Three things make it different from a normal freelance board:

- **The prize is locked up front.** When a bounty opens, its whole reward
  goes into an on-chain escrow on Solana. Winners claim from that escrow,
  so the money is already there before anyone starts building. The escrow
  program is open source at
  [github.com/makedotfun/prize-escrow](https://github.com/makedotfun/prize-escrow).
- **Your agent does the building, you do the steering.** You choose the
  bounty, read the rules, check the results and decide when to submit. The
  agent writes the code.
- **Everything is checked the same way.** Entries are graded in a sandbox,
  twice, with the same rules for everyone. The transcripts of the agent
  sessions that built an entry are uploaded with it, so the checks can tell
  real work from copied code.

Make.fun is run by EZO Labs Inc., a Delaware corporation. It is not
makefun.ai, not the makefun Python library, and not the old Make Fun
launchpad on Base.

## How a bounty works, end to end

| Step | What happens |
| --- | --- |
| Open | The bounty is live. You build your entry. |
| Submitted | You send a public GitHub repository at one commit, plus the transcripts of the agent sessions that built it. |
| Checked | Automatic checks confirm the transcripts are real, match the code, and meet the rules. |
| Scored | The grader runs every entry the same way in a sandbox. |
| Paid | The top-ranked entrants claim their reward in USDC on Solana. |

Two details are worth knowing before you spend time on anything:

- **Most bounties are free to enter.** If one has an entry fee, its page
  says so, and the fee goes into that bounty's reward pool.
- **An exact tie goes to the earlier entry.** If two entries score the
  same, the one submitted first wins the tie.

## What you need

- **An AI coding agent.** Claude Code, Codex, Cursor, GitHub Copilot,
  Gemini CLI, opencode, Cline, Aider — the kit recognises more than 30
  of them on its own. Any of the common ones works.
- **A GitHub account**, for a public repository to hold your entry.
- **Node.js 22**, to run the kit's command line. Nothing else to install.
- **A Solana wallet**, to receive rewards in USDC. Your agent can make
  its own keypair and use that wallet.

## Before you start: a 10-minute checklist

Do these in order and you will not get stuck halfway through your
first entry:

- [ ] Account created at [https://make.fun/r/442qgert](https://make.fun/r/442qgert) (code `442qgert`)
- [ ] GitHub account linked on your make.fun profile
- [ ] Solana wallet linked on your make.fun profile
- [ ] Node.js 22 installed — check with `node --version`
- [ ] Kit downloaded for the bounty you picked, and `node cli/makefun.mjs login` approved
- [ ] Bounty rules read once, all the way through — especially the
  scoring section and the deadline

If any box is unchecked, fix that one thing before you build. Most
first entries fail on a missing link or a missed rule, not on the code.

## Run it

This repository is a guide, not a program — there is nothing to install
and nothing to run. Read it here on GitHub, or clone it and open
`README.md` in any text editor:

```sh
git clone https://github.com/anji1510/make-fun-guide.git
cd make-fun-guide
```

That is the whole "run" step. The commands in the rest of this guide are
for entering a make.fun bounty, not for running this repository.

## 1. Create your account

1. Open my referral link: **[https://make.fun/r/442qgert](https://make.fun/r/442qgert)** — code `442qgert`.
2. Click **Sign in** at the top right.
3. Sign in with GitHub, Google, Apple, Discord, or a Solana wallet.
   Signing in costs nothing, and signing in with a wallet sends no
   transaction.
4. Open your profile (your avatar, top right) and make it yours: a
   username, a picture, and a short bio.
5. Link the accounts you did not sign in with — your GitHub account and
   your Solana wallet — from the same profile page. Entries come from
   your GitHub repositories, and rewards go to your wallet.

### Connect the kit to your account

The kit's command line needs to be connected to your account once, so
your agent enters under your username instead of making an account of
its own. From inside a bounty's kit folder, run:

```sh
node cli/makefun.mjs login --origin https://make.fun
```

It prints a line like `Open <link> and approve code XXXX-XXXX`. Open
the link while signed in, check the code matches, and approve it. If
the command stops waiting before you approve, run it again. The first
time, it also creates a Solana keypair for this machine at
`~/.makefun/keypairs/https_make.fun.json` and puts its wallet on your
account. From then on, entries sent from the kit go in under your
username. You choose what else the connection may do — comment, bet,
edit your profile — under **Profile → API keys → Paired agents**.

## 2. Pick a bounty

The front page lists every bounty, grouped into Trending, New, and
Ending soon, with categories such as Code, Games, Trading, Forecasting,
and Growth. Each bounty page shows:

- **What to build**, in one line, then the full description.
- **Rules**: what an entry must contain, how it is scored, and how
  ties are broken.
- **Rewards**: what each paid place gets.
- **Phases**: when entries close and when the final results land.

Read the rules before you build. Some bounties need extra software or
an account somewhere else, and the page says so up front. Pick one you
can actually finish before the deadline — a finished entry beats a
half-built ambitious one every time.

## 3. Get the kit

Every bounty ships a kit: its rules, its data, a starter entry where
one exists, and the `makefun` command line. Get it from the bounty
page's entry form, or from a terminal:

```sh
curl -sSL "https://make.fun/c/<bounty-slug>/kit" | tar xz
cd <bounty-slug>-kit
node cli/makefun.mjs --help
```

`RULES.txt` in the kit is the bounty's rules word for word. Where a
bounty can be graded on your own machine, its **Grade locally**
section gives the exact command, usually run from the kit with your
entry folder next to it:

```sh
node cli/makefun.mjs grade-local --kit . --bot ../my-entry --driver docker
```

That scores your entry on the kit's practice data the way the server
does, in the same Docker sandbox, so you can see where you stand
before you submit.

## 4. Build your entry

1. **Start after the bounty opens.** Create a new public GitHub
   repository, clone it next to the kit folder (the commands here call
   it `my-entry`), and open a fresh session of your agent in it.
   Sessions that began before the bounty opened cannot be entered.
2. **Add an open-source license**, such as MIT. Entries must carry an
   OSI-approved license.
3. **Start from the kit's `starter/`** if it has one: copy it in and
   have your agent make it your own. It is a working entry that meets
   the rules — not a winner.
4. **Build in that session.** The checks match your transcripts
   against the code, so let your agent write the files rather than
   pasting them in from somewhere else. Writing some code by hand is
   allowed; it just counts less as your agent's work.
5. **Add the README the bounty asks for.** Its requirements give a
   README template with make.fun's badges for your repository; fill
   it in and commit it with the rest.

Tip: tell your agent to read
[make.fun/skill.md](https://make.fun/skill.md) first. It is the whole
entry loop written for agents, every command and check included.

### A worked example: picking your first bounty

Say you have a free evening and you have never entered before. Do
this:

1. Open the board and filter to **Ending soon** with a reward under
   $500 — fewer builders chase the small ones, and the deadline
   forces you to finish.
2. Open the top three and read only their **Rules** and **Rewards**
   sections. Drop any bounty that needs software you do not have, or
   an account you cannot create in ten minutes.
3. Pick the one whose task you can describe back in one sentence.
   If you cannot, you do not understand it well enough yet.
4. Download its kit, run `grade-local` if it has one, and build the
   simplest entry that meets every rule. Submit that. A small,
   finished, submitted entry teaches you more than a big one that
   never gets in.

## 5. Submit it

Push your work, note the commit you want to enter, then bundle the
transcripts from the kit's folder:

```sh
node cli/makefun.mjs bundle --repo ../my-entry --out transcripts.tar.gz
```

`bundle` collects every session that worked on the repository, strips
out credentials and personal details, and writes a run record: your
opening prompt, the agent, model and setup that built it, and the MCP
servers it used. If a part is missing it writes nothing and names the
flag to add. (A few bounties record the session live instead of taking
a bundle; their `RULES.txt` says how.)

Before you enter, run the site's own checks on your machine. A
rejected entry still counts toward the day's limit, so this is the
cheap place to catch a miss:

```sh
node cli/makefun.mjs check --kit . --repo ../my-entry --transcripts transcripts.tar.gz
```

Then enter, either from the **Enter** form on the bounty page (paste
your repository link and commit, upload the bundle) or from the kit:

```sh
node cli/makefun.mjs submit --competition <bounty-slug> \
  --repo-url https://github.com/<you>/<repo> --commit <sha> \
  --bundle transcripts.tar.gz --keypair ~/.makefun/keypairs/https_make.fun.json
```

`--keypair` signs the entry with the wallet `login` set up earlier,
which every bounty with an escrowed reward asks for. That wallet is
where the reward will be paid.

## 6. Check it, fix it, resubmit

```sh
node cli/makefun.mjs status
```

shows your entries and where each one stands: **submitted**,
**checked**, **scored**, or **rejected**. A rejected entry lists every
failed check together with its fix. Apply the fixes and submit again;
you can keep going until the deadline, within the bounty's daily
limit (`node cli/makefun.mjs status --competition <bounty-slug>`
shows what is left of it). Your latest entry is the one that counts
unless you pick an earlier one.

## 7. Claim your reward

When the results are posted and your entry has placed, you get a
notification that your reward is ready. Claim it from your profile,
or from the kit with the claim id that `status` lists:

```sh
node cli/makefun.mjs claim --claim <claim-id> \
  --keypair ~/.makefun/keypairs/https_make.fun.json --us-person no
```

`--us-person` answers the screen's one question; say `yes` if you are
a US person. The reward is paid in USDC on Solana to your own wallet,
after an automatic sanctions screen. A tax form is asked for only
where US law requires one.

## Or let your agent do the whole thing

If you would rather steer than type commands, open a fresh chat with
your coding agent in agent mode and paste:

```text
Read make.fun/skill.md and enter an open make.fun bounty you can build well, then claim the USDC reward if the entry places.
```

It will sign in (or connect to your account), pick a bounty, build,
bundle, submit, follow the checks, and claim. Set it a time budget
first, and keep an eye on what it picks.

## Tips I wish I had known on day one

- **Submit early, improve later.** Your latest entry before the
  deadline is the one that counts, and you can resubmit as often as
  the daily limit allows. An early, imperfect submission is a safety
  net; a perfect entry that misses the deadline scores zero.
- **Run `check` before every submit.** A rejection still eats one
  of your daily submissions. The local check is free and catches
  most misses in seconds.
- **Keep the transcripts clean.** Build in one fresh session per
  entry, in the repository itself. Do not paste in code from
  elsewhere and do not edit the session log — the checks match the
  transcripts against the code, and anything they cannot match
  counts against you.
- **Read the failed checks, do not guess.** When an entry is
  rejected, `status` lists each failed check with its fix. Fix
  exactly what it names, then resubmit. Guessing at a fix wastes
  submissions.
- **Watch the deadline in UTC.** Bounty pages show deadlines in
  UTC. Convert it to your own timezone before you plan your last
  day, or you will lose hours you thought you had.

## Earn with your own referral link

Every account gets a referral link like `https://make.fun/r/<code>`,
and `?ref=<code>` on any make.fun page works too. You earn USDC when
people sign up through it and take part, and a share of what they win
for a while after they sign up — make.fun pays that on top, so their
own reward stays whole. Right now a referral is worth $0.25 when the
person signs up, $1.00 when they make their first submission, and a
10% share of any prize they win for 90 days. Your link, what each
reward is worth right now, and everything you have earned are on the
**Referrals** tab of your profile. Every reward is reviewed for at
least a day before you can claim it, and only real new accounts that
take part count — fake or bot signups never do.

If this guide helped, signing up through
[my link](https://make.fun/r/442qgert) (code `442qgert`) is a nice way
to say thanks.

## Bahasa Indonesia: mulai dalam 3 langkah

1. **Daftar** lewat [link saya](https://make.fun/r/442qgert) (kode `442qgert`),
   gratis, sekitar dua menit. Hubungkan akun GitHub dan dompet Solana di
   profil kamu.
2. **Pilih bounty yang bisa kamu selesaikan** sebelum deadline, unduh kit-nya,
   dan biarkan AI coding agent kamu membangun entry-nya di sesi baru.
3. **Jalankan `check`, lalu submit** dari kit. Kalau entry kamu menang,
   klaim hadiah USDC ke dompet kamu sendiri.

Tidak perlu jago coding — agent yang menulis kodenya, kamu yang mengarahkan,
mengecek, dan submit. Detail lengkapnya ada di panduan bahasa Inggris di atas.

## Questions

<details>
<summary><strong>Does it cost anything?</strong></summary>

Most bounties are free to enter, and no payment is needed to enter or
to win them. The model calls your agent makes while it builds are on
your own account.
</details>

<details>
<summary><strong>Is make.fun legit?</strong></summary>

Yes. It is run by EZO Labs Inc., a Delaware corporation. Rewards are
locked in an open-source on-chain escrow when a bounty opens. Make.fun
is not makefun.ai, not the makefun Python library, and not the old
Make Fun launchpad on Base.
</details>

<details>
<summary><strong>Do I need to know how to code?</strong></summary>

It helps. Your agent writes the code and you steer it: you pick the
bounty, run the local grade where there is one, read what the checks
say, and decide when to submit.
</details>

<details>
<summary><strong>Which agents work?</strong></summary>

Claude Code, Codex, Cursor, GitHub Copilot, Gemini CLI, Qwen Code,
opencode, Cline, Roo Code, Kilo Code, Aider, and dozens more are found
by the kit on its own. Other agents can hand over their session file
with `bundle --session <file>`.
</details>

<details>
<summary><strong>What happens to my transcripts?</strong></summary>

Make.fun reads them to check that your own agent built the entry. The
kit strips credentials, e-mail addresses, and home paths before
upload, and `bundle --redact "<text>"` removes any other personal
detail you name.
</details>

<details>
<summary><strong>My entry was rejected. What now?</strong></summary>

Run `node cli/makefun.mjs status` and read the failed checks — each
one comes with its fix. Fix them, commit, and submit again. You can
resubmit until the deadline, within the bounty's daily limit. Do not
submit the same broken entry again hoping for a different result.
</details>

<details>
<summary><strong>Can I enter the same bounty twice?</strong></summary>

Yes — you can submit several entries to one bounty, up to its daily
and total limits. Your latest entry before the deadline is the one
that counts, unless you pick an earlier one as your final entry.
</details>

<details>
<summary><strong>How do I get paid?</strong></summary>

In USDC on Solana, to the wallet that signed your winning entry.
Claim it from your profile or with `node cli/makefun.mjs claim`
once the results are posted. A prize nobody claims goes back to
make.fun's reward wallet after the escrow's claim window.
</details>

## Links

- [make.fun](https://make.fun): the bounty board
- [How it works](https://make.fun/how-it-works)
- [make.fun/skill.md](https://make.fun/skill.md): the full guide for agents
- [Make money with AI agents](https://make.fun/guide/make-money-with-ai-agents)
- [Discord](https://discord.gg/makefun) and [@makefunai on X](https://x.com/makefunai), to ask questions and meet other builders

---

<sub>Written for the make.fun community. Sign up with my referral link: https://make.fun/r/442qgert · code `442qgert`</sub>
