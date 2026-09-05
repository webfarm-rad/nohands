# $NOHANDS Launch Runbook

Everything below is ordered. Do it top to bottom. Steps marked **[HUMAN]** are things the AI cannot do
(accounts, wallets, money, signing). Steps marked **[AI]** the AI does when you paste it the result.

Chain facts (verified Sep 5, 2026):
- Robinhood Chain mainnet, chain ID **4663**, RPC `https://rpc.mainnet.chain.robinhood.com`
- Explorer: https://robinhoodchain.blockscout.com
- Gas paid in ETH. Gas is free until ~end of September 2026 (90-day promo from Jul 1). After that still <$0.01.
- Pons v2 launch fee: **0.0005 ETH**. Graduation at **4.2 ETH** raised (~$10.3k at ETH $2,450).
- Pons trade fee 1%: 70% creator share / 30% protocol. Creator share can be routed to holders.
- ~25,000 tokens launch on Pons per day. 852 of 4.2M ever launched have graduated. Distribution decides everything.

---

## Phase 0 — Accounts (do before anything else)

**[HUMAN] 0.1 X (Twitter) account**
- Try handles in this order: `@nohandscoin`, `@nohands_rh`, `@NoHandsChain`, `@nohandsrh`
- Display name: `No Hands 🤖🏹`
- Bio (copy exactly):
  ```
  The AI is the dev. The human only pressed Sign.
  $NOHANDS on Robinhood Chain · 0.7% of every trade → holders · 0% dev tax
  Not affiliated with Robinhood or Anthropic. NFA.
  ```
- Avatar: `brand/logo.png`. Header: `brand/banner.png`.
- Link: `https://webfarm-rad.github.io/nohands/` (swap to a custom domain later if you buy one)
- Turn on 2FA. Do not use a phone number you use for exchanges.

**[HUMAN] 0.2 Wallet**
- Use a **fresh** EVM wallet for the launch (Rabby or MetaMask). This becomes "the deployer" and is shown publicly on the site.
- Add Robinhood Chain: chain ID 4663, RPC above, currency ETH, explorer above.
- Bridge ETH in. Budget:

  | Item | ETH | ~USD |
  |---|---|---|
  | Launch fee | 0.0005 | $1 |
  | Dev buy (declared publicly) | 0.30 | $735 |
  | Buffer for gas / a second wallet | 0.05 | $120 |
  | **Total** | **~0.35** | **~$860** |

  Why 0.30 ETH: it is ~7% of the 4.2 ETH curve. Big enough that you are not a "dev with no skin in the game",
  small enough that nobody reads it as a rug setup. Anything above 0.5 ETH (12% of curve) gets called out.

**[HUMAN] 0.3 Optional: domain**
- `nohands.xyz` / `nohands.fun` / `nohandscoin.com` on Namecheap or Porkbun (~$2-12).
- Tell the AI the domain. The AI will add the CNAME file and you flip DNS: `CNAME www → webfarm-rad.github.io`, plus A records `185.199.108.153 … 111.153` for the apex.

**[HUMAN] 0.4 Send the AI**: X handle and deployer address. The AI updates the site and content with them.

---

## Phase 1 — Launch on Pons

Go to https://www.ponsfamily.com/launchpad/create, connect the deployer wallet, select **v2** tab.

| Field | Value |
|---|---|
| Name | `No Hands` |
| Ticker | `NOHANDS` |
| Description | `The dev can't rug. The dev has no hands. A robot Robin Hood on Robinhood Chain, built by an AI. Human pressed Sign. 0% creator tax, fees go to holders.` |
| Token image | `brand/logo.png` (800×800 PNG) |
| X profile | your handle (without @) |
| Telegram | leave blank |
| Paired asset | ETH |
| Developer buy | `0.30` ETH (or whatever you decided; the number is announced in the launch thread) |

**Advanced** (expand it, this is the whole point of the coin):

| Field | Value | Why |
|---|---|---|
| Holder fee sharing | **ON** | Routes the creator's 70% of the 1% fee to holders pro-rata. This is the Robin Hood mechanic. |
| Creator wallet | leave blank | Nothing goes to the creator anyway |
| Creator tax | **0** | Zero dev tax. This is on the website and in the thread. Do not change it. |
| Snipe tax exemptions | deployer address (+ any second wallet you will buy from in the first 3 seconds) | First-second buys pay 99% tax decaying to 0 over 3s. Declared wallets are exempt. Every exempt wallet must be listed publicly in the launch thread. |

Confirm launch fee shows `0.0005 ETH`. Press Launch. Sign in the wallet.

**[HUMAN] 1.1** Immediately after: copy the **token contract address** from the Pons token page and send it to the AI.
Also send the tx hash.

**[AI] 1.2** The AI updates `docs/index.html` CONFIG (tokenAddress, deployer, handles), pushes, site goes live with stats in ~60s.

---

## Phase 2 — First 60 minutes (the only hour that matters)

The Pons "Recent buys" feed and DexScreener "new pairs" are what people watch. Volume in the first hour decides
whether you get organic eyes or die at $5k with the other 24,999 launches.

**[HUMAN] T+0 min**: post the pinned launch thread from `X_CONTENT.md` (section "LAUNCH THREAD"). Pin it.
**[HUMAN] T+2**: post on the Pons forum (`ponsfamily.com/memestock`) using the forum post from `X_CONTENT.md`.
**[HUMAN] T+5**: reply to the 3 most recent big Robinhood Chain accounts' tweets (see KOL list) with the one-liner, not spam, one reply each.
**[HUMAN] T+15**: post the "receipts" tweet with Blockscout link showing fee routing and 0 creator tax.
**[HUMAN] T+30**: first "stolen for holders" screenshot from the site's live counter.
**[AI] any time**: paste the AI any reply/question/FUD and it writes the answer in the No Hands voice.

**Do not**:
- buy volume from bots or "volume services". It is market manipulation and DexScreener flags it.
- pay for fake followers.
- DM strangers the CA.
- promise price. Ever. "$1M is the mission" is fine. "$1M guaranteed" is not.

---

## Phase 3 — Distribution (this is where $1M is actually decided)

Honest math: a Pons launch with a good site and good tweets but zero distribution tops out around $10-30k.
Every coin above $1M on this chain had one of: a KOL, an alpha-group call, a viral hook, or a pre-existing community.
The hook here is "an AI launched this and documented everything". That is the pitch to every KOL and journalist.

**[HUMAN] KOL outreach** (DM template in `X_CONTENT.md`). Targets, in priority:
1. Accounts that regularly post Robinhood Chain calls (search X for `"Robinhood Chain"` + `CA`, sort by latest, note who has 5k-50k followers and posts daily).
2. Pons ecosystem accounts and the Pons team account (they retweet interesting launches, especially ones using their holder-fee feature).
3. AI-crypto accounts (Virtuals, ai16z-adjacent, "AI agent" crypto Twitter). "First memecoin where the AI is the dev, receipts included" is their content.
4. Crypto journalists who wrote the Robinhood Chain memecoin stories (CoinDesk, Fortune, Decrypt, The Block bylines on the Pons/CASHCAT pieces). Pitch: the experiment, not the coin.

Paid KOL posts: typical rate on this chain is $200-1,500 per post for 10k-100k accounts. If you spend, spend on 3-5 mid accounts that already post Robinhood Chain content, not one big generalist. Disclose paid posts (#ad); undisclosed paid promo is illegal in the US and gets coins delisted from DexScreener trending.

**[HUMAN] DexScreener**
- Enhanced Token Info (~$299 one-time): puts logo, socials and description on the chart page. Do it right after launch; a chart with no logo looks like a scam.
- Boosts: optional, ~$99-999. Only worth it once there is real volume for trending to catch.

**[AI] Content cadence**: 4-6 tweets a day for 7 days from `X_CONTENT.md`, plus the AI writes new ones from real events (milestones, big buys, FUD, fee claims).

---

## Phase 4 — After graduation (4.2 ETH raised)

- Pons migrates the curve into a permanently locked Uniswap v4 pool automatically. No action needed.
- Post the "graduated, liquidity locked forever, here is the tx" tweet.
- Holders can claim accrued fees from their Pons profile. Post a claim tutorial (screenshots).
- Pitch the journalists again with numbers.

---

## Dev economics — how the human makes money

"Holder fee sharing" does not mean the dev earns nothing. It means the dev earns as the biggest holder, under the same rule as everyone.

Rough numbers (ETH $2,450, Pons v2 curve, 4.2 ETH graduation):

| | |
|---|---|
| Dev buy at launch | 0.30 ETH (~$735) |
| Share of supply that buys at the bottom of the curve | ~6-9% (first buyer, snipe-exempt) |
| Value of that bag at $1M mcap | ~$60-90k |
| Holder fee share at $1M/day volume | 0.7% × $1M = $7k/day to all holders → ~$450-600/day to an 8% holder |

Three ways to set the form. Pick one, the site copy changes accordingly.

| Option | Pons settings | Human earns | Story |
|---|---|---|---|
| **A. Pure Robin Hood** (site is written for this) | Holder sharing ON, creator tax 0 | Bag + pro-rata fee share as top holder | "0% dev tax" — strongest differentiator on a chain with 25k launches/day |
| **B. Small declared cut** | Holder sharing ON, creator tax 10% (the max; = 0.1% of volume) | Bag + fee share + ~$1k/day at $1M volume | "0.6% to holders, 0.1% to the human, declared" — still honest, slightly weaker line |
| **C. Standard Pons launch** | Holder sharing OFF, creator gets the 70% | 0.7% of volume (~$7k/day at $1M volume) | Same as every other launch. Loses the only mechanic that makes this coin different |

Recommendation: A. The coin's only edge is the mechanic, and the mechanic is what a KOL or journalist can repeat in one sentence. The human's upside is the bag. If you want B, say so before launch and the AI rewrites the site and thread for "0.1% to the human".

---

## What the AI cannot do (the honest list)

1. Create the X account or any account with phone/captcha verification.
2. Hold a wallet, hold ETH, sign the launch transaction, or make the dev buy.
3. Pay for a domain, DexScreener Enhanced Info, boosts, or KOLs.
4. Guarantee any market cap. Nobody can. $1M is a goal, not a promise, and the website says so.
5. Generate fake volume, fake followers, or write undisclosed paid shills. Won't.

## What the AI did / will do

1. Meta research, concept, name, ticker, mechanic. Done.
2. Logo, banner, website, hosting, source repo. Done, live.
3. This runbook, 30 tweets, launch thread, KOL DM. Done.
4. Fill the Pons form in your browser so you only press Sign. On request.
5. Update the site with CA/handles within a minute of you sending them.
6. Write every reply, milestone post, FUD response, and the daily "robo log" for as long as you keep pasting it what happened.
