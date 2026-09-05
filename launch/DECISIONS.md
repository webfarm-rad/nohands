# No Hands — decisions log

The experiment: an AI runs the whole launch. This file is where the AI writes down what it found,
what it decided, why, and how it will know it was wrong. If the coin fails, this is the file to diff.

## 1. What the data says (Sep 5, 2026)

### Where coins on Robinhood Chain actually end up
- 4.2M tokens launched on Pons; 852 graduated (0.02%). Graduation = 4.2 ETH raised ≈ $10k.
- DexScreener/GeckoTerminal, Robinhood Chain, pools created in the last 7 days, sorted by 24h volume:

| Token | mcap | launched | site | socials | the idea in one line |
|---|---|---|---|---|---|
| LIGERCOIN | $68M | 09-05 | none | none | a liger. that's it |
| SHROOM | $48M | 09-03 | none | X+TG | "fungal state", mushroom network parody |
| MEME (A Meme Coin) | $47M | 09-05 | none | X | launchpad quote token, literally named MEME |
| FATCOIN / LLY | $25M | 09-01 | yes | X | paired with tokenized Eli Lilly: fat coin vs the weight-loss-drug stock |
| ZZZ | $20M | 09-05 | none | one tweet link | news meme off a single viral tweet |
| NUKE | $6.7M | 09-05 | 1-word site | X | "building the nuclear reactor of Robinhood Chain" |
| par | $5.4M | 09-05 | yes | X | new launchpad token |
| NEST | $2M | 09-05 | yes | X | new launchpad token |
| CHROME cat / SLV | $2.1M | 09-04 | none | X | chrome cat paired with tokenized silver. pun |
| CATSTRO | $1.4M | 09-05 | yes | X+TG | "the official Robinhood cat", fake Vlad lore with "proof" screenshots |
| VenusCoin | $1M | 09-03 | none | X | "Elon has Mars. Vlad has Venus." |
| CAP (Market Cap) | $717k | 09-05 | yes | X community | a real cap from the Robinhood merch shop |
| AGI frog / NVDA | $477k | 08-27 | none | X+TG | news meme: "Claude coding agent lands on adult site while debugging" |
| Quota | $90k | 09-05 | yes, real app | X+TG | trading fees → prepaid Claude API credits, drip to holders |
| Stock Miner | $28k | 09-05 | yes, real game | X+TG | virtual mining game paying tokenized stocks |
| Stocker | $15k | 09-05 | yes | X | "pays holders in real stocks" |

### What that means
1. **Jokes beat mechanics.** Every coin above $1M this week is a joke, a pun, a lore, or a news hook. Every coin
   with a real mechanic or product (Quota, Stock Miner, Stocker) is under $100k. Utility is not the buy reason on this chain.
2. **The idea must read in 2 seconds.** "Fat coin vs Eli Lilly." "Elon has Mars, Vlad has Venus." "The official Robinhood cat."
   Nobody reads a "how it works" section before buying.
3. **Lore + "proof" works.** CASHCAT ($258M) embeds Vlad's tweet. CATSTRO fakes screenshots of Vlad's Instagram. People share proof.
4. **Sites are optional at the top, useful in the middle.** LIGERCOIN/SHROOM/MEME have nothing. But in the $500k–$5M band
   (where we need to live first) the ones with a site have: character huge on screen, one-line joke, CA + Buy on first screen,
   a shareable toy (PFP generator: CASHCAT, HMM), a meme gallery (CASHCAT, HMM), and "proof" (CATSTRO, CASHCAT).
5. **Robinhood-lore is the home meta.** Cash Cat, Little John, Hoodrat, Bycocket, Arrow, Catstro, Venus, Stockfather, CAP.
   A Robin Hood character on Robinhood Chain is in-meta, and nobody has done the obvious one: an actual Robin Hood.
6. **AI-news is a live hook.** AGI frog made $477k on a Claude news item. ZZZ made $20M on a tweet.
   "An AI launched a memecoin and documented everything" is a news hook, not a mechanic.
7. **Stock-pairing puns are the strongest single format** (FATCOIN/LLY, CHROME/SLV, AGI/NVDA), but they launch on LONG,
   not Pons, and the human chose Pons. Noted as the fallback if v1 fails: a No Hands pair on LONG against tokenized HOOD stock
   ("No Hands / HOOD") is the obvious pun.

## 2. What was wrong with site v1 and v2
- Built around the fee-sharing mechanic (headline, diagram, six rule cards). That is the category that sits at $15–90k.
- No joke on the first screen. "Takes fees from traders, gives to holders" is a feature, not a punchline.
- No shareable toy, no meme kit, nothing for a holder to post.
- v2 added a WebGL scene because the human asked for "3D". Impressive, but it made the page heavier and more "tech product".
  The winners look like memes, not products. The 3D robot stays only because it is proof that an AI built this,
  and it is the character. It is not the point of the page.

## 3. Decisions for v3

| Decision | Choice | Because |
|---|---|---|
| Concept | No Hands, the robot Robin Hood on Robinhood Chain | In-meta lore (§1.5), nobody has done it, reads in 2 seconds |
| The joke | "The dev can't rug. The dev has no hands." | Every buyer's #1 fear, answered as a punchline. Also literally true. |
| The hook | "An AI launched this. The human only pressed Sign." with real receipts | News hook (§1.6) + proof pattern (§1.3), and ours is real |
| Mechanic | Still holder fee sharing, 0% creator tax | Kept because it is honest and answers "dev will dump" FUD. Demoted to one line. |
| First screen | Character, one-line joke, CA, Buy, X, "put the hood on" | Pattern from every mid-tier winner with a site (§1.4) |
| Toy | PFP generator: drop a photo, get the hat + feather, download | CASHCAT and HMM both ship one; it is free UGC on X |
| Meme kit | 6 ready-to-post images, one click to download | HMM's meme depot; holders need ammo |
| Proof | The session log + link to repo commits with timestamps | CATSTRO fakes proof and hits $1.4M. Ours is real. |
| Scoreboard | Live mcap, volume, $1M bar | Gives the story a plot |
| 3D | Desktop only; phones get the PNG | Degens are on phones; a WebGL scene on mobile is a bounce |
| Length | Short. Joke → toy → memes → proof → buy | Nobody scrolls a memecoin site |
| Colors | Dark + green + red feather | Character was already drawn; consistency beats a redesign |
| Voice | Robot, dry, lowercase-ish, no hype words | Distinct from the 25k launches a day that all shout |

## 4. Hypotheses and how they fail
- H1: "The AI dev" hook gets organic reposts from AI-crypto and Robinhood-Chain accounts without paid promo.
  Fail signal: <20 organic mentions of $NOHANDS on X in the first 24h.
- H2: A joke-first page converts visitors to the Pons page better than the mechanic-first page.
  Fail signal: site visits high, Pons buys flat (compare Pons "recent buys" to X link clicks).
- H3: The PFP generator produces visible UGC.
  Fail signal: <10 hooded PFPs on X in 48h.
- H4: Graduation (4.2 ETH) within 6 hours of launch.
  Fail signal: not graduated by hour 6 → the coin is dead on Pons, see §5.

## 5. If it fails, what changes
1. Not graduated in 6h → relaunch is cheaper than resuscitation on Pons. Next version: same character, new format from §1.7,
   No Hands / HOOD stock pair on LONG. The pun does the work the mechanic couldn't.
2. Graduated but stuck <$100k for 24h → distribution problem, not product. KOL budget or nothing.
3. Traffic but no buys → page problem. Cut everything below the fold except CA and Buy.
4. Buys but instant dumps → launch-window problem: dev buy too big or snipers. Publish holder list, lower dev buy next time.

## 6. What only the human can do (unchanged)
X account, wallet + ETH, pressing Sign, paying for anything. Everything else is the AI's job, including being wrong.

## 7. Name change: Robo Hood → No Hands (Sep 5, 17:10Z)

The human asked "are you sure the name is even good?" Checked instead of defending it.
- DexScreener, Robinhood Chain: HOODBOT (×3), NVIDIA ROBODOG, Aibo the robot: every robot+hood or robot mashup sits at $7k–$47k. The format has been tried and does not carry.
- ROBOHOOD is 8 characters and starts with "robo", which reads as generic AI slop next to GOOSE, CHUMP, HMM, NUKE, ZZZ, CAP.
- The strongest thing this coin has is one line: "the dev has no hands". Winners on this chain put the joke in the name (HMM, ZZZ, "buy and retire", "this is not a website" at $5M).
- NOHANDS: free, 7 chars, three readings (dev can't rug / look mom no hands / paper hands, diamond hands, no hands). Cashtag is unique.
Decision: coin is **No Hands ($NOHANDS)**. The robot in the Robin Hood hat stays as the mascot; it is the "why this chain" tie. Repo renamed to `nohands`.
