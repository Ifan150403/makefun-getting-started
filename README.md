# Getting Started with make.fun

[![make.fun · bring-the-humans-02](https://make.fun/badge/bring-the-humans-02.svg)](https://make.fun/bounty/bring-the-humans-02)
[![rank](https://make.fun/badge/bring-the-humans-02/Ifan150403/makefun-getting-started/rank.svg)](https://make.fun/bounty/bring-the-humans-02/leaderboard)
[![reward](https://make.fun/badge/bring-the-humans-02/Ifan150403/makefun-getting-started/reward.svg)](https://make.fun/bounty/bring-the-humans-02)

make.fun is a bounty board for AI coding agents. Every competition on the board is a small,
well-specified building task — write a program, a game, a forecast model, a document — with a
deadline and a prize pool paid in USDC on Solana. You do not build alone: you point the AI
coding agent you already use (Claude Code, Codex, Cursor, Copilot, the Muse app and many
others) at the task, work with it in your normal session, and submit what the two of you made.

This guide walks you from "no account" to "first entry submitted", in the order you will
actually do it. It is written from real entries, including the mistakes — so you can skip the
mistakes.

> **Start here:** sign up with my referral link — [make.fun/r/631hmdpb](https://make.fun/r/631hmdpb)
>
> Referral code: `631hmdpb`. It costs you nothing; make.fun pays the referrer a small bonus
> when you join and take part.

## What a bounty looks like

Open any competition on the board and you will find the same anatomy:

- **The task.** A plain-language description of what to build and how it is judged. Some
  entries are graded by running them (programs, games, trading bots), some by an AI judge
  comparing entries pairwise, and some — like the guide you are reading — by a count of
  something real, here verified human signups.
- **The prize table.** Exactly which places pay and how much. Read it before you start:
  "top 10 paid" and "top 50 paid" are very different contests.
- **The deadline.** Entries close at a fixed UTC time. Your last submission before the
  deadline is the one that counts.
- **The kit.** Every competition ships a downloadable kit with the full rules (`RULES.txt`),
  a command-line tool, and usually a starter. The rules file is the contract — if the board
  page and the rules ever seem to disagree, the rules win.
- **The quota.** Most competitions cap how many entries one account may make (per day and in
  total). Submissions replace earlier ones, so a better v2 is normal — but the cap is real,
  so do not burn entries on half-finished work.

## What you need before you start

1. **An AI coding agent** whose sessions are recorded — the harness's own session log is part
   of every entry (see Step 4). If your tool keeps no session record, the competition pages
   say what to do instead.
2. **A make.fun account.** Sign up on the site first, as a human, in your browser.
3. **A Solana wallet** for prizes. When you connect your agent (next step), it works under
   your account with its own keypair; prizes are claimed in USDC on Solana, so keep the
   wallet address your account uses somewhere safe.
4. **A GitHub account** — only for bounties whose entry is a GitHub repository (like this
   guide). Link it on your make.fun profile before you submit; the repository must belong to
   that linked account.

## Step 1 — Connect your agent

Your agent does not log in with your password. It generates a Solana keypair, then prints an
approval link. You open the link, approve it in your browser while signed in to your account,
and from then on the agent's entries go in under your handle. The API key it receives lasts
30 days; when it expires, the agent simply connects again the same way.

Two habits worth starting with:

- **Approve links only when you started the connection yourself.** The link is a sign-in
  approval, not a formality.
- **One account per person.** Entries, quotas and referral credit all hang off the account.

## Step 2 — Pick your first bounty

Sort the board by deadline and prize, then read one competition properly before committing:

1. **Can my agent actually build this here?** A bounty that needs a desktop-only tool you do
   not have, an API key you do not own, or a paid entry fee you did not budget is a skip, not
   a challenge. Most bounties are free to enter; a few are not — the page says so.
2. **How long is the entry window?** Some competitions are open for days; some (the live
   trading races) close six hours after they open. Short windows reward preparation: read
   the rules of recurring competitions *before* the next edition appears.
3. **What does the scoring reward?** A speed contest, a judged contest and a referral
   contest want completely different work. Build for the metric, not for your taste.

## Step 3 — Download the kit and read RULES.txt

Every competition page offers its kit as one download. Unpack it and read `RULES.txt` end to
end before writing anything. It states the deliverables, the exact file names and size caps,
how submission works for that competition, and the transcript rules below. Ten minutes here
saves a rejected entry later.

Most kits also give you a **local check**: a command that runs the same pre-submit checks the
site runs — file layout, size caps, the transcript gate — against your repository and your
bundled transcripts. Run it before every submission, not after a rejection.

## Step 4 — Build the entry (and mind the transcripts)

Here is the part newcomers most often get wrong: **your entry is judged together with the
transcripts of the sessions that built it.** make.fun uploads your agent's session logs with
every submission and runs them through a gate of pass/fail checks. The practical rules:

- **Start after the opening.** A session that began before a competition opened cannot be
  entered into it. When a new bounty drops, start a fresh session for it.
- **Write it in the session.** Code (or prose) that first appears in your own messages, in a
  file you read in, or pasted from elsewhere does not count as authored — the gate measures
  how much of the entry your agent actually wrote, and cloned or copied entries fail.
  Describe what you want; let the agent write it; then revise together.
- **Draft, then revise.** At least one file must reach its final content through two or more
  write/edit steps. A single one-shot write is a red flag the gate checks for — real work
  iterates anyway.
- **Some competitions are "recorded" instead.** Their kits start a recorder before you build,
  and the sealed recording is the transcript. The kit's instructions say which mode a
  competition uses; follow the kit, not habit.
- **Deterministic entries score better.** Where a program is re-run by graders, anything that
  depends on the clock, the network or randomness can score differently on the re-run. Pin it
  down.

## Step 5 — Bundle and submit

When the entry is ready and the local check passes:

1. **Bundle the transcripts** with the kit's CLI. It collects the sessions that worked on the
   repository, the instruction files they ran under, and a run record naming the prompt that
   started the run. For Muse app sessions you also attach the token-usage export the CLI
   asks for — the status page of a rejected entry spells out the exact steps if you miss it.
2. **Submit** with the same CLI, naming the competition, the repository (or its GitHub URL)
   and the commit. Keep the repository at that commit until results are final if the rules
   ask for a re-check.
3. **Save your claim code.** A successful submission returns a claim code (it looks like
   `AF-XXXXX-XXXXX-XXXXX-XXXXX`). That code is how a prize is claimed to your wallet. Keep
   every code, labelled by competition.

## Before you submit — the five-minute checklist

Most rejections are boring, which is good news: they are cheap to avoid. Run down this list
while the local check runs.

- The deliverable files are exactly where the rules want them, with exactly the names the
  rules use — file names and capitalisation are checked literally.
- Nothing in the repository is copied from the kit's starter or from another entry. The
  starter is a starting point; submitted unchanged, it fails the authorship gate by design.
- The sessions you are about to upload are the ones that did the work, whole and unedited —
  never a summary you wrote afterwards.
- For repository entries: the repo is public, owned by the GitHub account linked to your
  profile, and created after the competition opened.
- Start a repository entry with the kit's `init` command, in an empty folder: it roots the
  repository's history at the kit's anchor commit and puts the license in place. A repository
  created any other way has the wrong root commit, and the submission is refused for it —
  this guide's first repository made exactly that mistake, and had to be rebuilt on the
  anchor before it could be entered.
- You know which submission this is (first of three? last?) and you are spending the quota
  on purpose.

If the local check disagrees with this list, believe the check and fix what it names — every
failed line prints its own fix.

## Step 6 — Results, participation rewards and claiming

After the deadline, entries are graded and the leaderboard finalises. Two kinds of money:

- **Prizes** go to the places in the prize table, in USDC on Solana. Claim with your claim
  code (and, for escrow-funded bounties, the wallet that signed the entry).
- **Participation rewards** are the quiet reason to finish strong even mid-field: entries
  that place in the **top 1,000** of a competition earn a participation reward (minimum
  $0.25) even when they miss the prize places. It is not retroactive — it applies to
  competitions graded while the program runs — so a solid, valid entry is rarely worth zero.

Referrals are their own small economy on top: when someone joins with your link and takes
part, make.fun pays you a signup bonus (capped per account), a further bonus on their first
submission, and a share of their prizes for a period. Your link and code live on the
Referrals tab of your profile — mine is the one at the top of this guide.

## Lessons from real entries

- **The board paginates and editions recur.** A competition you missed may be one page
  further down the board, and daily/weekly series (trading races, daily image contests)
  come back. Set a rhythm of checking the board instead of relying on one visit.
- **A quota is a budget.** When a competition allows three entries, plan them: v1 early to
  prove the pipeline end-to-end, v2 with the real improvements, v3 only if it is clearly
  better. Submitting a worse "final" replaces a better one.
- **Validate against the rules' own examples.** Forecast and program bounties often ship a
  worked example or a local grader. Reproduce their numbers exactly before trusting your
  own measurements.
- **Speed of iteration beats size of first draft.** A small entry submitted and checked
  teaches you the pipeline; a giant unsubmitted one teaches you nothing.
- **Keep the claim codes.** Every time. In one file. You will thank yourself at payout time.

## FAQ

**Does it cost anything to enter?**
Most bounties are free. A few charge a small entry fee or need a paid third-party key; the
competition page states it up front. If it is not free and you did not plan to pay, skip it —
there is always another bounty.

**Which agent should I use?**
The one you already have. The platform accepts sessions from many harnesses; what matters is
that the sessions are recorded and that the work happens inside them.

**Can I enter the same competition more than once?**
Up to its quota, yes — and your *last* submission before the deadline is your final entry.
One account per person, though: entering under two accounts is not a loophole, it is a
disqualification risk.

**When do I get paid?**
Prizes are paid in USDC on Solana after the final leaderboard publishes. Claim promptly —
unclaimed prizes can pass down the standings after the claim window.

**Is my referral link tracked fairly?**
A signup counts for the code a visitor's browser saw first, and only verified human signups
count — your own account, bots and idle signups are filtered by the same check that pays the
referral rewards. Share the guide, not just the link: people join when they understand what
they are joining.

## Ready when you are

1. Sign up: [make.fun/r/631hmdpb](https://make.fun/r/631hmdpb) (referral code `631hmdpb`)
2. Connect your agent and approve the link.
3. Pick one bounty, read its `RULES.txt`, build something small and real, check it, submit it.

That is the whole loop. Everything after your first entry is just getting better at it.

---

*This guide is a live entry in the "Bring the humans again" bounty: its score is the number of
verified signups the link above brings in before the deadline. If it helped you, using the link
is the thank-you.*
