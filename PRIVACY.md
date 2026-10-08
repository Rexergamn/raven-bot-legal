# Privacy Policy - Raven Discord Bot

**Last Updated:** October 8, 2026
**Effective Date:** January 31, 2026

## The Short Version

- The Bot stores your Discord user ID plus the gameplay data its features need: music stats, Int Coins balances, game and tournament history, and your linked Riot account if you link one.
- It never sees your messages outside of commands, never sees your card or bank details, and never stores your raw IP address (an optional verification page stores one-way hashes of your IP and device, described below).
- If you win a cash prize, it stores the payout username you give it so the operator can pay you.
- Nothing is sold or shared with advertisers. Data stays on the operator's own hardware.
- Ask the operator on Discord and your data will be deleted within 30 days.

## 1. Introduction

This policy describes what Raven ("the Bot", "we") collects and why. It goes together with the [Terms of Service](https://raw.githubusercontent.com/Rexergamn/raven-bot-legal/main/TOS.md). By using the Bot you agree to the practices described here.

## 2. What We Collect

### 2.1 Discord Basics

Your Discord user ID and username, the server and channel IDs where you use the Bot, and the commands you run. For voice features: which voice channels you join for music and for how long.

### 2.2 Music

Songs you play (title, source URL), play counts, queue history, and listening statistics.

### 2.3 Economy and Games

Int Coins balances and transaction history, casino game results, shop purchases, daily quest and Wordle progress, dungeon runs (classes, floors, outcomes), `/journey` runs and the feedback votes you give on them, trading-card collections and battle results, and clan membership and contributions. Balancing analytics (aggregate coin-flow and game statistics) are derived from this data.

Clans level up on shared activity, so if you are in a clan the Bot periodically checks whether two or more clan members are together in the same voice channel. What is stored is the XP award and its source, not a log of who you were in voice with, and never any audio.

### 2.4 Invites and Server Growth

Which invite link you joined through and who created it (used for invite rewards and join screening), and records of Disboard `/bump` usage (who bumped, when) for bump rewards.

### 2.5 League of Legends

If you link a Riot account: your Riot ID, PUUID and summoner ID, region, account level, and current and historical rank. From these we derive and store an estimated skill rating (MMR) and its history over time, plus an automated smurf-likelihood score with the signals that produced it. Tournament participation is stored too: registrations, teams, match results, bracket placement, and prize records.

**Honor and reports:** after tournament matches, other participants may rate your sportsmanship or file a misconduct report. Votes, reports, dropouts, and the reputation score derived from them are stored and visible to tournament staff.

**Predictions:** the answers you give in prediction polls during a match countdown, and whether they came true.

**Streams and recordings:** tournament matches may be livestreamed and recorded. During a streamed match, a broadcast app run by tournament staff reads the live game (picks, bans, and each player's in-game stats) from the League client on the broadcast computer and sends it to the Bot for the stream overlay. That app's IP address is logged for troubleshooting; it belongs to the staff member running the broadcast, never to players. Recordings and clips are stored on the operator's hardware and may be published (see the Terms of Service, Section 4.6).

**Looking For Group:** the groups you host or join, the lobby link you share, which Riot account hosted, and any reports you file or that are filed about you.

### 2.6 Prizes

If you place in a tournament with a prize: your placement, the prize amount, and whether it has been paid. Gift-card codes are stored encrypted until they are delivered to you by direct message. For a cash prize, the Bot asks you by direct message for a payout method and username (for example a PayPal username, which may be an email address you choose to give). It is used only to pay you, is visible only to tournament staff, and is kept as the record of the payment. We never receive card or bank details.

### 2.7 Join Screening (Gatekeeper)

When you join a server using the verification gate, the Bot records your join: when your Discord account was created, when you joined, who invited you, and an automated risk score with human-readable flags (for example "account created less than 24 hours ago" or "name closely matches an existing member"). The score is computed from public Discord signals only: account age, avatar presence, username shape, name similarity to existing members, join timing patterns, and the invite graph. Held joins and moderator decisions (approve/reject) are recorded.

### 2.8 Web Verification (only if the server enables it)

Some servers require a short browser check (a Cloudflare Turnstile captcha) before access. When you complete that page, your IP address is processed **transiently** to derive and store:

- a salted one-way hash of the IP, computed with HMAC-SHA-256 using a secret key held only by the operator (used solely to detect alternate accounts on that server; without the key it cannot be matched or reversed, and even with it the original IP cannot be recovered)
- country-level location and your internet provider's name (via ip-api.com)
- whether the connection looks like a VPN, proxy, or datacenter
- your browser's user-agent string

The same page also reads a small amount of information from your browser and device, used only to recognise when two accounts verify from the same machine:

- a rendering fingerprint (a test image drawn by your graphics hardware, stored only as a one-way hash) and your graphics card's model name
- your screen resolution, CPU core count, memory size, and operating system name
- your browser's timezone and language (compared against the country of your IP to detect VPN use)
- a random identifier stored in your browser, which you can remove at any time by clearing site data for the verification page
- whether the device is a phone, tablet, or desktop computer

We do **not** use audio fingerprinting, WebRTC address discovery, font enumeration, or any tracking that follows you to other websites. Nothing on this page is used for advertising, and none of it leaves the Bot.

The raw IP is never stored or logged, and this data is visible only to that server's moderators.

**Tournament registration.** Servers running League tournaments may require that your verification was completed on a desktop computer rather than a phone, because alternate accounts are hardest to detect on mobile connections. This affects tournament sign-up only, never access to the server itself.

### 2.9 Media Requests

For authorized users: requested titles, request status, and timestamps.

### 2.10 Moderation

Moderation actions taken through the Bot (who, what, when, the stated reason) are logged for audit purposes. So are tournament and server actions taken by staff on the website.

### 2.11 Website Sign-In

If you sign in at app.starling.gg, Discord tells us your user ID, username and avatar (the `identify` permission only; never your email address or your list of servers). We store a sign-in session with those details, which lasts up to 30 days or until you sign out.

### 2.12 Supporter Subscription

If you subscribe through Discord, the Bot receives only the entitlement (that your account has an active subscription) so it can grant perks. **Discord handles all payment processing; we never receive your payment details.**

### 2.13 Community Feedback Surveys

If the server sends you a feedback survey, we store the answers you submit, the questions you were shown, and which engagement segment you fell into (for example "first-time player" or "hasn't played recently"). Surveys are personalized using data we already hold about your activity on the server (how long you've been here, tournament history, and similar) so we don't ask what we can already answer; that context snapshot is saved alongside your answers. Responses are tied to your Discord account so we can grant the completion reward and avoid asking you twice. You can permanently opt out of survey DMs at any time with the button on the message.

### 2.14 What We Do NOT Collect

- message content (other than the commands you run)
- private/direct message content (the Bot DMs you, but does not read your DMs)
- voice audio of any kind
- card or bank details
- email addresses (unless you give one as a prize payout username, see 2.6), phone numbers, real names, or addresses
- raw IP addresses (see 2.8; normal Discord bot interactions never expose your IP to us at all)

## 3. How We Use It

- **Running features**: playing music, tracking balances, running games and tournaments, granting roles, fulfilling media requests.
- **Fairness and safety**: enforcing cooldowns, detecting cheating and alternate accounts, screening joins, keeping tournaments balanced, and giving moderators an audit trail.
- **Improvement**: aggregate statistics to balance games and fix bugs.
- **Legal**: complying with law and valid legal requests, and enforcing the Terms of Service.

## 4. Sharing and Third Parties

We do not sell your data, share it with advertisers, or disclose it publicly. Data is not shared across Discord servers, except that a shared Riot account or shared verification-page hash may flag an alternate account within the same server. We may disclose data when required by law.

Services the Bot talks to, each under its own privacy policy:

- **Discord** ([privacy policy](https://discord.com/privacy)): everything the Bot does flows through Discord, including subscription payments.
- **YouTube** ([privacy policy](https://policies.google.com/privacy)): music streaming, and the platform tournament livestreams may be published on; no personal data of yours is sent by the Bot.
- **Riot Games** ([privacy notice](https://www.riotgames.com/en/privacy-notice)): we look up the Riot account you link to fetch rank and match data.
- **Cloudflare** ([privacy policy](https://www.cloudflare.com/privacypolicy/)): carries traffic to the Bot's web pages (app.starling.gg), and runs Turnstile, the captcha on the optional verification page. Cloudflare receives standard request metadata, including your IP, when you visit those pages.
- **GitHub** ([privacy statement](https://docs.github.com/en/site-policy/privacy-policies/github-general-privacy-statement)): hosts the starling.gg website and these documents; GitHub receives standard request metadata when you visit them. The site shows only upcoming tournament names and dates, never player data.
- **Payout services**: if you win a cash prize, the payment is sent through the service you chose (for example PayPal), under that service's own privacy policy.
- **ip-api.com** ([privacy policy](https://ip-api.com/docs/legal)): server-side lookup of country and VPN/proxy indicators during web verification; only the IP is sent, never your Discord identity.
- **Media server platforms** (Radarr/Sonarr/Jellyfin): operated by the bot operator; media requests are forwarded there.
- **Linear** ([privacy policy](https://linear.app/privacy)): our issue tracker. The text of a suggestion you send with `/suggest` is copied there; your name and Discord ID are not.

## 5. Storage and Security

Data lives in a SQLite database on the operator's own hardware, on a private network, with access restricted to the operator (key-based authentication only). Backups are taken regularly, verified, and then encrypted with `age` (modern X25519 public-key encryption) before the unencrypted copy is deleted; only the operator holds the decryption key. An encrypted copy may also be stored off-site in a private Discord channel, where Discord's privacy policy applies to the (unreadable) file. All data in transit is encrypted: Bot traffic goes over Discord's TLS-secured API, and the Bot's web pages are served over HTTPS only. The one exception is the ip-api.com lookup during web verification (Section 2.8), which ip-api.com's free service offers only without encryption; it carries your IP address alone, never your Discord identity. No system is perfectly secure; in the event of a breach compromising personal data, affected users will be notified via Discord where feasible.

## 6. Retention and Deletion

Data is kept for as long as it is needed to run the Bot (balances, statistics, and tournament history are inherently long-lived).

**If you leave the server**, your progression data (balance, card collection, game statistics, quest progress, and similar) is kept for a **30-day grace period** and restored if you rejoin within it. After 30 days it is permanently deleted; any remaining balance is returned to the server's shared prize pool. Match, tournament, and moderation history is retained (see below), and hashed IP and device verification records (Section 2.8) are retained indefinitely to prevent ban and blacklist evasion; raw IP addresses are never stored.

You can request deletion at any time:

1. Contact the bot operator on Discord (DM the owner, or ask a server admin to relay).
2. Say whether you want everything deleted or specific data (for example just your Riot link).
3. Deletion is completed within **30 days** and confirmed to you.

Deletion covers your Discord ID associations, music history, economy and game data, Riot account link and derived scores, website sessions, and media request history. Records of prizes already paid may be kept where needed for tax or legal reasons. A minimal record may be retained where needed for security (for example ban evasion prevention) or legal compliance, and aggregate statistics that no longer identify you may be kept. Some features stop working after deletion (your balance and tournament eligibility are gone).

## 7. Your Rights

You can ask, at any time and free of charge, to:

- **Access**: see what data we hold about you, and get a copy in a common format.
- **Correct**: fix inaccurate data (for example relink the right Riot account).
- **Delete**: as described in Section 6.
- **Object or restrict**: object to specific processing, or simply stop using the Bot.

If you are in the EEA/UK, these correspond to your GDPR rights; processing is based on legitimate interest (running the features you use) and consent (your voluntary use and account linking), and you may lodge a complaint with your local data protection authority. If you are a California resident, the CCPA gives you equivalent rights to know, delete, and not be discriminated against; we do not sell personal information. We aim to answer access and correction requests within 14 days and deletion requests within 30 days.

## 8. Children

The Bot is not for children under 13 (or the digital-consent age in your country), matching Discord's own minimum age. If you believe a child under 13 has used the Bot, contact the operator and the data will be deleted.

## 9. International Transfers

The Bot's server may be in a different country than you. By using the Bot you consent to your data being processed there, protected as described in this policy.

## 10. Cookies and Tracking

The Bot uses no analytics, advertising, or cross-site tracking. Its web pages use only what they need to work:

- **app.starling.gg** sets one sign-in cookie when you sign in with Discord. It keeps you signed in for up to 30 days and is removed when you sign out.
- **The optional verification page** stores a random identifier in your browser (Section 2.8) and embeds Cloudflare Turnstile, which may set its own cookies to operate the captcha under Cloudflare's policy.

## 11. Changes

This policy may be updated at any time; the "Last Updated" date changes when it is, and material changes are announced in Discord where feasible. Continued use after a change means you accept the update.

## 12. Contact

For any privacy question or request: contact the bot operator on Discord. We aim to respond within 14 days.

---

**Raven Discord Bot**. Privacy Policy effective January 31, 2026, last updated October 8, 2026.
