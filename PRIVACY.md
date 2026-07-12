# Privacy Policy - Raven Discord Bot

**Last Updated:** July 11, 2026
**Effective Date:** January 31, 2026

## The Short Version

- The Bot stores your Discord user ID plus the gameplay data its features need: music stats, Int Coins balances, game and tournament history, and your linked Riot account if you link one.
- It never sees your messages outside of commands, never sees your payment details, and never stores your raw IP address (an optional verification page stores a one-way hash, described below).
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

Int Coins balances and transaction history, casino game results, shop purchases, daily quest and Wordle progress, dungeon runs (classes, floors, outcomes), trading-card collections and battle results, and clan membership and contributions. Balancing analytics (aggregate coin-flow and game statistics) are derived from this data.

### 2.4 Invites and Server Growth

Which invite link you joined through and who created it (used for invite rewards and join screening), and records of Disboard `/bump` usage (who bumped, when) for bump rewards.

### 2.5 League of Legends

If you link a Riot account: your Riot ID, PUUID and summoner ID, region, account level, and current and historical rank. From these we derive and store an estimated skill rating (MMR) and its history over time, plus an automated smurf-likelihood score with the signals that produced it. Tournament participation is stored too: registrations, teams, match results, bracket placement, and prize records.

**Honor and reports:** after tournament matches, other participants may rate your sportsmanship or file a misconduct report. Votes, reports, and the reputation score derived from them are stored and visible to tournament staff.

### 2.6 Join Screening (Gatekeeper)

When you join a server using the verification gate, the Bot records your join: when your Discord account was created, when you joined, who invited you, and an automated risk score with human-readable flags (for example "account created less than 24 hours ago" or "name closely matches an existing member"). The score is computed from public Discord signals only: account age, avatar presence, username shape, name similarity to existing members, join timing patterns, and the invite graph. Held joins and moderator decisions (approve/reject) are recorded.

### 2.7 Web Verification (only if the server enables it)

Some servers require a short browser check (a Cloudflare Turnstile captcha) before access. When you complete that page, your IP address is processed **transiently** to derive and store:

- a salted one-way hash of the IP, computed with HMAC-SHA-256 using a secret key held only by the operator (used solely to detect alternate accounts on that server; without the key it cannot be matched or reversed, and even with it the original IP cannot be recovered)
- country-level location and your internet provider's name (via ip-api.com)
- whether the connection looks like a VPN, proxy, or datacenter
- your browser's user-agent string

The raw IP is never stored or logged, and this data is visible only to that server's moderators.

### 2.8 Media Requests

For authorized users: requested titles, request status, and timestamps.

### 2.9 Moderation

Moderation actions taken through the Bot (who, what, when, the stated reason) are logged for audit purposes.

### 2.10 Supporter Subscription

If you subscribe through Discord, the Bot receives only the entitlement (that your account has an active subscription) so it can grant perks. **Discord handles all payment processing; we never receive your payment details.**

### 2.11 What We Do NOT Collect

- message content (other than the commands you run)
- private/direct message content (the Bot DMs you, but does not read your DMs)
- voice audio of any kind
- payment information
- email addresses, phone numbers, real names, or addresses
- raw IP addresses (see 2.7; normal Discord bot interactions never expose your IP to us at all)

## 3. How We Use It

- **Running features**: playing music, tracking balances, running games and tournaments, granting roles, fulfilling media requests.
- **Fairness and safety**: enforcing cooldowns, detecting cheating and alternate accounts, screening joins, keeping tournaments balanced, and giving moderators an audit trail.
- **Improvement**: aggregate statistics to balance games and fix bugs.
- **Legal**: complying with law and valid legal requests, and enforcing the Terms of Service.

## 4. Sharing and Third Parties

We do not sell your data, share it with advertisers, or disclose it publicly. Data is not shared across Discord servers, except that a shared Riot account or shared verification-page hash may flag an alternate account within the same server. We may disclose data when required by law.

Services the Bot talks to, each under its own privacy policy:

- **Discord** ([privacy policy](https://discord.com/privacy)): everything the Bot does flows through Discord, including subscription payments.
- **YouTube** ([privacy policy](https://policies.google.com/privacy)): music streaming; no personal data of yours is sent.
- **Riot Games** ([privacy notice](https://www.riotgames.com/en/privacy-notice)): we look up the Riot account you link to fetch rank and match data.
- **Cloudflare Turnstile** ([privacy policy](https://www.cloudflare.com/privacypolicy/)): the captcha on the optional verification page; Cloudflare receives standard request metadata including your IP when the widget loads.
- **ip-api.com** ([privacy policy](https://ip-api.com/docs/legal)): server-side lookup of country and VPN/proxy indicators during web verification; only the IP is sent, never your Discord identity.
- **Media server platforms** (Radarr/Sonarr/Jellyfin): operated by the bot operator; media requests are forwarded there.

## 5. Storage and Security

Data lives in a SQLite database on the operator's own hardware, on a private network, with access restricted to the operator (key-based authentication only). Backups are taken regularly, verified, and then encrypted with `age` (modern X25519 public-key encryption) before the unencrypted copy is deleted; only the operator holds the decryption key. An encrypted copy may also be stored off-site in a private Discord channel, where Discord's privacy policy applies to the (unreadable) file. All data in transit is encrypted: Bot traffic goes over Discord's TLS-secured API, and the optional verification page is served over HTTPS only. No system is perfectly secure; in the event of a breach compromising personal data, affected users will be notified via Discord where feasible.

## 6. Retention and Deletion

Data is kept for as long as it is needed to run the Bot (balances, statistics, and tournament history are inherently long-lived). You can request deletion at any time:

1. Contact the bot operator on Discord (DM the owner, or ask a server admin to relay).
2. Say whether you want everything deleted or specific data (for example just your Riot link).
3. Deletion is completed within **30 days** and confirmed to you.

Deletion covers your Discord ID associations, music history, economy and game data, Riot account link and derived scores, and media request history. A minimal record may be retained where needed for security (for example ban evasion prevention) or legal compliance, and aggregate statistics that no longer identify you may be kept. Some features stop working after deletion (your balance and tournament eligibility are gone).

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

The Bot uses no cookies, analytics, or tracking of any kind. The one exception: the optional web verification page embeds Cloudflare Turnstile, which may set its own cookies to operate the captcha under Cloudflare's policy. The page itself sets none.

## 11. Changes

This policy may be updated at any time; the "Last Updated" date changes when it is, and material changes are announced in Discord where feasible. Continued use after a change means you accept the update.

## 12. Contact

For any privacy question or request: contact the bot operator on Discord. We aim to respond within 14 days.

---

**Raven Discord Bot**. Privacy Policy effective January 31, 2026, last updated July 11, 2026.
