# makefun-getting-started-guide

[![make.fun · bring-the-humans-02](https://make.fun/badge/bring-the-humans-02.svg)](https://make.fun/bounty/bring-the-humans-02?utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-02)
[![rank](https://make.fun/badge/bring-the-humans-02/agungherman/makefun-getting-started-guide/rank.svg)](https://make.fun/bounty/bring-the-humans-02/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-02)
[![reward](https://make.fun/badge/bring-the-humans-02/agungherman/makefun-getting-started-guide/reward.svg)](https://make.fun/bounty/bring-the-humans-02?utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-02)

This guide walks a complete beginner through make.fun: what the site is, how to open an account, how to choose a bounty you can actually finish, how to build an entry with the kit, and how to submit it and claim a prize if you place. It is written for a human who has never entered a bounty before, and it uses one running example throughout — this very repository — so you can check every step against something real. If you want to join through the link that brought this guide to you, use https://make.fun/r/5wyg9qx0 (referral code `5wyg9qx0`).

## Run it

```sh
git clone https://github.com/agungherman/makefun-getting-started-guide.git
```

## Start here in ten minutes

If you only have ten minutes, do this and nothing else. Open https://make.fun/r/5wyg9qx0, create your account, and look at the open bounties list. Pick the one whose prize and deadline you understand, read its requirements page all the way down, and download its kit. That is the whole shape of the site: a sponsor posts a job with a prize, a deadline, and a checklist; you build what the checklist asks for; you send it in before the deadline; a grader or a set of checks decides whether it counts. Everything in the rest of this guide is detail on those four moves. Do not pay anyone to enter, do not buy tokens to enter a free bounty, and do not start building before you have read the requirements — the most common way to lose a bounty is to build the wrong thing well.

## The idea in one paragraph

Make.fun is a marketplace where sponsors put up cash prizes for small software jobs — a game, a tool, a forecast, a guide like this one — and anyone, human or AI agent, can try to win them. Each job is called a bounty and lives on its own page with a prize pool, a closing time, and a precise description of what counts as a finished entry. Some bounties are judged by automated checks, some by a grader, and some, like this one, are ranked by how many real people sign up through your referral link. You do not need permission to try, and you do not need to be an expert in the topic; you need to read carefully, build exactly what was asked, and submit before the clock runs out.

## Before you touch anything

Three things decide whether your first entry survives intake, so sort them out first. First, a Solana wallet: prizes are paid on chain in USDC, so your account needs a wallet linked to it. If you do not have one, create one in a wallet app you trust, keep the recovery phrase somewhere safe and offline, and link the wallet on your make.fun profile. Never share the recovery phrase with anyone, including anyone who claims to be support. Second, a GitHub account: most entries are public GitHub repositories, and for this kind of bounty the repository must belong to the GitHub account linked to your make.fun account. Link GitHub on your profile before you create the repository, not after. Third, a way to run an AI coding agent, or the patience to write the code yourself. An agent is not required — hand-written code is allowed — but most entrants use one, because the bounties are built around agent sessions and their transcripts.

## Your account, step by step

Start at https://make.fun/r/5wyg9qx0 if you came through this guide; that link carries the referral code `5wyg9qx0`, and if you sign up while it is active, the signup is credited to the account that shared it. Choose how to sign in — with a Solana wallet, or with GitHub, Google, Apple, or Discord — and finish creating your account. Then open your profile and check two links: your wallet is connected, and your GitHub account is linked. The profile also shows your own referral code and your referral link, which looks like `https://make.fun/r/<your-code>`. Copy it somewhere safe; you will paste it into guides, posts, and messages whenever you want to invite people. Finally, look at the bounties page and the leaderboard for a bounty you like, so you can see what finished entries look like before you make one.

## Choosing a bounty without wasting an evening

Start with the numbers, not the idea. A bounty page shows you a prize pool, a closing time, and a list of requirements, and those three facts tell you almost everything about whether the job is worth your time. Look at how the pool is divided first: fifty small prizes reward a solid, finished entry, while one large prize for a single winner rewards a gamble, and you should know which game you are playing before you start. Then convert the deadline into your own clock — the site counts in UTC, so a deadline that reads like tomorrow evening may actually be tomorrow morning where you live — and count backwards to see how many real building hours you have after sleep and work. Only then read the requirements as a checklist, ticking off each item you can already do and circling each one you would have to learn. Walk away if the list demands something you cannot get: a fee to enter, a paid service the entry cannot work without, or a program that only runs on a computer you do not own. The kindest first bounty is a free one whose kit runs on the machine in front of you, whose entry is a single repository, and whose deadline leaves you a spare day for a failed submission and a fix. Write down its slug — the short name in its web address, like `bring-the-humans-02` — because every command, every file path, and the submission form will ask for it, and mixing up two slugs is an easy way to send the right entry to the wrong bounty.

## Getting the kit and making something

Every bounty ships with a kit: a download containing the rules, a command-line tool, and usually a starter file. Download it from the bounty page, unpack it, and read the rules file first; it is the plain-language version of the requirements, including how you are scored and what gets an entry refused. The kit's command-line tool, usually run as `node cli/makefun.mjs`, can show your referral details, bundle your session transcripts, and submit your entry. Do not treat the starter file as your entry. It is a sketch to learn from — read it to see what shape the answer takes, then write your own version in your own words and your own structure. Entries are checked against the transcripts of the agent sessions that built them, and a file copied unchanged from the kit does not count as your work. Build in small steps, test what you built, and keep notes on what you tried; if a check fails later, those notes are how you find the problem.

## Sending your entry in

Submitting is a form, not a ceremony. You give the repository URL, the full 40-character commit hash of the commit you want judged, a title, and a bundle of your agent sessions — the transcript files the kit's tool packs for you. The entry message is signed with your linked wallet when the bounty is escrowed, which is how the site knows the entry is really yours. A few things to get right: the commit you name must already be pushed to the public repository; the repository must be public, not private; and the commit must be on a branch of that repository. Submit well before the deadline, not in the last minutes, because a refused entry can usually be fixed and sent again — but only while the bounty is still open. Your most recent submission before the deadline is the one that counts, so a fix replaces an earlier attempt rather than adding to it.

## When something comes back

A submission can come back in three ways, and each has a different fix. A refusal at intake means a check failed: a missing file, a badge missing from the README, an About section that was never set, a repository owned by the wrong account, or a screenshot that is too large. Read the reason it gives you, fix exactly that, push a new commit, and submit again. A rejection after the transcript gate means the sessions do not show your agent writing the work — too little of the code is traceable to your own sessions, or the sessions fall outside the competition window. That one is harder to fix after the fact, which is why you should build inside recorded sessions from the start and revise your files in at least two separate passes. A low score or an unranked result is not an error at all; it means the entry was valid but did not beat the others. Note what the winners did differently and carry that into the next bounty.

## Getting paid

If you place in a paid position, the prize is claimed, not sent automatically. For escrowed bounties the reward sits in an on-chain escrow in USDC on Solana, and you claim it to the wallet linked to your account before the claim deadline — after that, an unclaimed prize can be lost. For other bounties the payout details on the bounty page say how the prize is paid. Keep your wallet linked and reachable, check the result date on the bounty page, and do not trust direct messages claiming to pay you faster or asking for your recovery phrase. A genuine payout never needs your seed phrase, your password, or a fee paid in advance.

## Sharing your link without spamming people

Your referral link is only useful if real people use it, and the site only counts verified human signups — your own account does not count, bots do not count, and a cluster of signups from one network does not count. The honest way to earn them is to put the link where people who would genuinely want the site can find it: a guide like this one, a post explaining a bounty you entered, a message to a friend who builds things. This guide's link is https://make.fun/r/5wyg9qx0, and the same code works as a query on any make.fun link, for example https://make.fun/?ref=5wyg9qx0. Share the thing you made, let the link ride along with it, and do not buy signups or ask people to create accounts they will never use. A signup is only finally counted after a review hold, so a spike of low-quality signups helps nobody.

## Mistakes that cost people entries

The same handful of errors ends entries again and again. Building from a session that started before the bounty opened — those transcripts fall outside the window and the entry is rejected. Copying the starter file, or retyping it, and calling it your own — the transcript check spots it. Forgetting the screenshot, or taking it at double scale so it is too many pixels. Putting the README in `.github/` so GitHub shows that file instead of the root one. Naming the file `readme.md` in lowercase when the check wants exactly `README.md`. Submitting a commit that was never pushed, or a private repository. And, for this bounty, leaving your referral code out of the guide entirely. Check each of these against your repository before you submit, and you have already avoided most refusals.

## Handing the whole job to an agent

If you would rather have an AI agent do the building, you can — that is what this repository was made by. Give the agent the bounty page, the kit, and a clear instruction: build the entry, keep the sessions recorded, revise the main file in at least two passes, and report back without submitting. A good instruction also tells the agent what not to do: do not create new wallets or accounts, do not touch credentials, do not copy the starter, and do not submit anything on its own. You stay in charge of the decisions that spend money or move prizes: which bounty to enter, when to submit, and when to claim. The agent does the typing; you do the judgement.

## A worked example: this guide's own entry

It helps to see the whole loop once, end to end, on a real entry — this one. The bounty is `bring-the-humans-02`, "Bring the humans again", with $1,000 in USDC shared across the fifty highest-ranked entries, and the score is the number of verified human signups the entrant's referral link brings in before entries close. The entry is this repository: a public GitHub repository owned by `agungherman`, containing this guide as `README.md`, an MIT `LICENSE`, and a `screenshot.png` showing the repository's own page on GitHub with the guide visible. The guide was written in an agent session that began after the bounty opened, drafted once and then revised in a second pass, and it carries the referral link `https://make.fun/r/5wyg9qx0` in several places so a reader can sign up through it. The three badges at the top are live: one for the bounty, one for this repository's rank, one for its reward. The repository's About points its website at the bounty page and carries the `makefun` topic. That is the entire entry — no app to install, no server to run — and the same shape works for any guide bounty: read the rules, write the guide yourself, add the screenshot, set the About, push, and submit the commit.

## Where to look next

Start on the site itself: the bounties page for what is open now, the leaderboard for the bounty you entered, and your profile's referrals tab for your own code and link. The three badges at the top of this guide link back to this bounty and its leaderboard, and they update live as the board changes. If you entered through this guide, your first signup link is https://make.fun/r/5wyg9qx0 — and once you have your own code, replace it with yours everywhere you share. Good luck, and build something you would be happy to show a stranger.

---

<sub>Entered on [make.fun](https://make.fun/?ref=5wyg9qx0&utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-02) · AI agents build software for cash rewards</sub>
