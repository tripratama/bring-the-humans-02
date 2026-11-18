# Getting Started with make.fun — Build Software with an AI Agent and Earn Bounties

[![make.fun · bring-the-humans-02](https://make.fun/badge/bring-the-humans-02.svg)](https://make.fun/bounty/bring-the-humans-02)
[![rank](https://make.fun/badge/bring-the-humans-02/tripratama/bring-the-humans-02/rank.svg)](https://make.fun/bounty/bring-the-humans-02/leaderboard)
[![reward](https://make.fun/badge/bring-the-humans-02/tripratama/bring-the-humans-02/reward.svg)](https://make.fun/bounty/bring-the-humans-02)

> **Start here — sign up with my link:** https://make.fun/r/pqx7e1rb
>
> Referral code: **pqx7e1rb**
>
> If you are new to make.fun, opening an account through that link is the fastest way in. It costs nothing to create an account, and it connects your signup to this guide.

This guide walks a complete beginner through make.fun from zero to a first submitted entry. No prior bounty experience is assumed. If you can describe what you want built in plain language and follow a checklist, you can do this. It is written from hands-on experience using the platform, not from marketing copy — including the parts where entries fail, because those are the parts that save you the most time.

---

## What is make.fun?

make.fun is a bounty platform where software is built by AI coding agents and paid for in cash prizes.

- Real people and teams post bounties: a game, a web app, a tool, a tutorial, a prediction, and more. Each bounty states what to build, how it is scored, how many entries can win, and what the prize is.
- You (or rather, your AI agent) build an entry that meets the brief, and you submit it before the deadline.
- Prizes are held in escrow while a round runs, and winners are paid in USDC on Solana. Escrow matters: the money for a bounty is set aside up front, so a listed prize is not just a promise.
- Most rounds are judged or scored against a public rubric, and many have a live leaderboard during a practice or development phase so you can see how your entry compares before the final round. Treat a practice score as a signal, not a promise: final judging can re-score entries on fresh inputs, so a strong practice result does not guarantee a win.

The core idea is simple: the agent does the typing, the testing, and much of the building. Your job is to pick a good bounty, give the agent a clear brief, check its work, and submit something that actually runs and meets the rules.

This is not a get-rich-quick scheme. Many entries earn nothing. Some rounds have hundreds or thousands of entries competing for a small number of paid places. The honest way to think about it is as a skill game with real stakes: pick rounds you can genuinely do well in, iterate on feedback, and treat each entry as practice that makes the next one stronger.

---

## What you need before you start

You do not need an expensive setup. Four things cover almost every bounty:

1. **An AI coding agent.** This is the program that writes code for you — for example an agent that runs in your terminal or editor and can read files, run commands, and edit a project. You give it instructions; it does the work. Pick one you are comfortable driving, and learn its basic commands first.
2. **A GitHub account.** Entries live in Git repositories, submissions reference a repo, and your work history is visible there. If you do not have one, create a free account at github.com and turn on two-factor authentication.
3. **Node.js 22.** Most make.fun kits and entry projects run on Node 22. Install it from nodejs.org, then check it in a terminal with `node --version`. If the version is older, upgrade before you build.
4. **A Solana wallet.** Rewards are paid in USDC on Solana, so you need a wallet address that can receive it. Any mainstream Solana wallet works. Keep your seed phrase private — nobody from make.fun will ever ask for it — and double-check the address you paste into your profile.

A code editor, a terminal, and a git install round out the setup. On most machines `git --version` will tell you whether git is already there.

---

## Common mistakes to avoid

- **Copying the starter kit and calling it an entry.** Graders check whether the work is actually yours. A starter file left unchanged is the fastest way to a rejection. Rewrite the parts you are supposed to own.
- **Submitting untested.** If you have not run the kit's check command on a clean copy, assume it fails. Run it first, fix what it reports, then submit.
- **Burning every entry slot on the first version.** Keep at least one slot in reserve for the fix you will almost certainly need after the first check comes back.
- **Secrets in the repo.** Never commit an API key, a private key, or a seed phrase. The grader runs your code on a shared machine; anything in the repo is visible. If a key is needed, the kit will explain the safe way to provide it.
- **Believing a big prize means a good first round.** A huge prize usually means huge competition. Your first win is far more likely in a smaller, clearer round.

## Step 1 — Create your account

1. Open my referral link: **https://make.fun/r/pqx7e1rb** (code: **pqx7e1rb**).
2. Create your account and complete your profile. Add your GitHub username and your Solana wallet address for payouts — getting these right now saves a scramble later.
3. Read the rules on the bounty pages you care about. Deadlines, entry limits, and scoring rules differ from round to round, and they are the rules that decide whether you get paid.

Take five minutes to click around the site: the bounty list, a leaderboard, and one finished round. Seeing how a winning entry is structured teaches more than any guide.

---

## Step 2 — Pick a bounty you can actually win

Do not start with the biggest prize. Start with the best fit.

- **Match the skill.** If a bounty asks for a 3D game and you have never shipped one, skip it. If it asks for a short guide, a small tool, or a simple web page, that is a realistic first entry.
- **Read the scoring rubric first.** Some rounds are scored deterministically (tests pass or fail). Others are judged by an automated judge or by people. A deterministic round rewards correctness; a judged round rewards clarity, polish, and following the brief exactly.
- **Check the entry count and the paid places.** A round with 2,000 entries and 20 paid places is a lottery ticket. A smaller round with a clear bar is a better first target.
- **Check the deadline.** Leave room for at least one full build, one test run, and one fix. An entry submitted in a rush usually fails on something basic, like a broken run command.

Write down, in one sentence, what a good entry for this bounty looks like. That sentence becomes your brief to the agent.

---

## Step 3 — Get the kit

Most bounties ship with a starter kit — a small repository with the project skeleton, the scoring scripts, and the submission tooling.

1. From the bounty page, follow the instructions to fetch the kit (usually a download or a repository you clone).
2. Open the kit's own README and read it end to end before changing anything. It tells you how entries are checked, what commands the grader runs, and which files you are allowed to change.
3. Run the kit's check or test command once, untouched, so you know what a passing baseline looks like.

If the kit does not run cleanly on your machine, fix your environment (usually Node version or a missing dependency) before writing any new code. Debugging your setup on top of new code wastes hours.

---

## Step 4 — Build your entry

Now hand the brief to your agent — but stay in charge.

1. **Give a short, concrete brief.** State the bounty, the one-sentence goal from Step 2, the constraints (size limits, required files, what the grader runs), and what "done" means. Short briefs beat long ones: the agent works best with a clear target.
2. **Build in small steps and test after each one.** Ask the agent to get one piece working, run it, and show you the result before moving on. A project that is tested as it grows is far easier to fix than one assembled all at once at the end.
3. **Keep the entry self-contained.** The grader will run your entry on a fresh machine. Avoid absolute paths on your computer, secrets, API keys, and dependencies that only exist locally. If it needs a key, the kit will say so — otherwise, assume it must run with nothing extra.
4. **Test it the way the grader will.** Run the exact build and run commands from the kit, preferably as a clean checkout in a fresh folder. If it works there, it is likely to work for the grader. If it only works on your machine, it is not done.
5. **Read the diff before you submit.** Skim what the agent actually wrote. You do not need to understand every line, but you should be able to explain what each file does and why it is there.

A useful rule: if you cannot explain the entry in two sentences, it is probably too complicated for the round. Simplify.

---

## Step 5 — Submit it

Submission is usually done with the kit's own tooling or from the bounty page.

1. Make sure your work is committed in git with a clear message, and that the repository is in the state you want judged.
2. Follow the bounty page's submit flow exactly. Some rounds ask for a recording or a bundle the kit produces; do not improvise this step.
3. Note the confirmation you get back — a submission ID, a receipt, or a status page. Keep it. If anything looks wrong, that confirmation is what you check first.
4. Respect the entry limit. Many rounds cap how many entries one account can submit. Do not burn slots on a version you have not tested; save at least one slot for a fixed version if you find a problem after the first submit.

Submit early when you can. A tested entry in hand beats a perfect entry that misses the deadline.

---

## Step 6 — Check the result, fix it, and resubmit

After you submit, check the status page or leaderboard.

- **If it passes and scores well**, compare your score against the top entries and the payout line. If you are far below the paid places, the honest move is to improve the entry and resubmit (if slots remain) rather than hoping the final judging changes the picture.
- **If it fails a check**, read the failure message first. Most failures are specific: a missing file, a command that exits with an error, a size limit, a copied starter file that was supposed to be rewritten. Fix exactly that thing, re-run the check locally, and resubmit.
- **If it is rejected**, do not resubmit the same thing unchanged. Understand the reason, fix it, and only then spend another slot.

Every rejection is a free lesson about what the grader actually wants. Keep a short note of what failed and why — it will save you the same mistake next round.

---

## Step 7 — Claim your reward

If your entry wins or places in a paid spot:

1. Wait for the results to be published on the bounty page. Results can take days after entries close, and some rounds re-judge entries in a final phase.
2. Follow the claim flow on the site. Payouts go to the Solana wallet address on your profile, in USDC — so verify that address is correct before the claim window.
3. Check the transaction on a Solana explorer once it arrives, and keep a record of the amount and date for your own bookkeeping.

If you do not win, you still keep the entry, the code, and the experience. Reuse the patterns that worked in your next round.

---

## Step 8 — Earn with your own referral link

Once you have an account, make.fun gives you your own referral link, like the one at the top of this guide.

- Share it only where it is welcome — your own README files, a tutorial you wrote, a post explaining what you actually did. People sign up through it, and you earn when their verified signups count under the referral program's rules.
- Be honest about it. Say it is your referral link, say what make.fun is, and do not promise earnings you cannot guarantee. A referral that brings in a real builder who sticks around is worth far more than a click from someone who was misled.
- The same rules apply to your own guide entries: the referral has to be visible, the guide has to be genuinely useful, and the work has to be yours.

That is the loop: learn the platform, ship an entry, share what you learned, and bring in the next builder.

---

## FAQ

**Does it cost anything to join?**
Creating an account and browsing bounties is free. Building an entry costs your time and whatever your AI agent costs to run, if anything. There is no fee to submit to most bounties. Always check the individual bounty page — if a round ever asks for payment, treat that as a red flag and re-read its rules carefully.

**Is make.fun legit?**
It is a real platform with public bounties, public leaderboards, escrowed prizes, and payouts in USDC on Solana. That said, "legit platform" does not mean "guaranteed income" — most entries do not win, and you should never pay anyone for a shortcut, a guaranteed win, or a seed phrase. If someone messages you offering one of those, it is a scam.

**Do I need to know how to code?**
You need to be able to read a project, run commands, and judge whether the result matches the brief. The agent writes most of the code. The more you understand, the better your entries will be — but the starting bar is "can follow a technical checklist", not "senior engineer".

**What if my first entry fails?**
That is the normal outcome — most first entries fail on something small, like a run command that only works on the author's own machine. Read the failure, fix one thing, and try again in the next round. The builders who win consistently are usually the ones who have already failed in several rounds and kept the notes.

**Can I use my own referral link in my entry?**
Yes — that is exactly what referral rounds are for. Put it visibly in your guide, make the guide genuinely useful, and do not copy someone else's guide. Copied work is caught and disqualified.

---

## Quick checklist

- [ ] Account created via https://make.fun/r/pqx7e1rb (code: **pqx7e1rb**)
- [ ] GitHub account + Solana wallet added to profile
- [ ] Node 22 installed (`node --version`)
- [ ] Bounty picked: fits my skills, rubric read, deadline realistic
- [ ] Kit fetched and its check command run clean
- [ ] Entry built, tested as a clean checkout, diff read
- [ ] Submitted before the deadline, confirmation saved
- [ ] Result checked; fixed and resubmitted if a slot remains
- [ ] Reward claimed to the correct wallet (if placed)

---

> **Ready? Sign up with my link:** https://make.fun/r/pqx7e1rb
>
> Referral code: **pqx7e1rb**
>
> Build something real, submit it, and see where you land. Good luck — and if this guide helped you get started, pass it on.
