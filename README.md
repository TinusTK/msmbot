# msmbot

# 🍁 MapleStory M Clock Reset Tracker Bot

![msmbot](https://github.com/user-attachments/assets/9b50169a-b589-46a3-a76b-8e05364efd7e)

A Discord bot that tracks MapleStory M daily and weekly resets, boss timers, Guild Scramble, Path of Proof, and custom event pings — all updated live every 5 seconds.

---

## 🆓 Free Features (all servers)

- Live embed showing **Server Time**, **Daily Reset**, and **Weekly Reset** countdowns
- Category channel name updates every 10 minutes with compact reset times
- Auto-repost if the embed is deleted

## 💎 Premium Features (trial / paid)

- **Pharaoh / Legends / Sharenian Culvert** countdown with automatic 1-hour role ping
- **Guild Scramble** countdown with automatic role pings at start, 5 min, and now
- **Path of Proof** 28-day timer with auto-reset and 1-hour role ping
- **Weekly Boss Run timer** with custom day, time, and message
- **Custom Timer Pings** — daily or weekly scheduled role pings with custom messages
- **Countdown Timers** — multiple named countdown timers with expiry pings

> All new servers receive a **30-day free trial** with full premium access.

---

## ⚙️ Getting Started

### 1. Run `/setup`

Requires **Manage Server** permission. This is a 4-step wizard:

| Step | What it does |
|---|---|
| 1 — Region | Select your server region (NA or ASIA). If Europe, you'll be prompted for a UTC offset. |
| 2 — Category channel | Select the category where the bot's channel sits — the bot will update this name with live timers. |
| 3 — Embed channel | Select the text channel where the live reset embed will be posted. |
| 4 — Role | Select the role the bot will ping for all notifications. |

After confirming, the bot posts the live embed and starts tracking immediately.

> Re-running `/setup` on a configured server will show a warning before resetting all data.

---

## 📋 All Commands

### Free commands

| Command | Description |
|---|---|
| `/setup` | Run the 4-step setup wizard (requires Manage Server) |
| `/help` | Show all commands and your current access status |
| `/premium` | View upgrade options and pricing |
| `/payment-status` | Check your trial or payment status |

### Premium commands

| Command | Description |
|---|---|
| `/bosstimer create` | Set up a weekly boss run schedule |
| `/bosstimer clear` | Remove the boss timer |
| `/poptimer set` | Set the Path of Proof 28-day countdown |
| `/poptimer clear` | Clear the Path of Proof timer |
| `/customping create` | Create a custom daily or weekly ping |
| `/customping list` | View all your custom pings |
| `/customping delete <ping-number>` | Delete a custom ping by its number |
| `/countdowntimer create` | Create a named countdown timer with expiry ping |
| `/countdowntimer clear <number>` | Remove a countdown timer by number |
| `/countdowntimer check` | List all active countdown timers |
| `/countdowntimer hide` | Hide countdown timers from the embed |
| `/countdowntimer show` | Show countdown timers in the embed |

### Settings commands

| Command | Description |
|---|---|
| `/settings look_new` | Switch to new-style embed (separator lines, lowercase units) |
| `/settings look_old` | Switch to classic embed layout (default) |
| `/settings dash_on` | Enable dashes in countdown strings |
| `/settings dash_off` | Disable dashes in countdown strings (default) |

---

## 🕒 Live Embed

The embed updates every **5 seconds** and shows:

- 🕒 Current server time (HH:MM and 12hr format)
- 🌍 Daily Reset countdown
- 🔁 Weekly Boss Reset countdown
- 🛕 Pharaoh / Legends / Sharenian Culvert countdown *(premium)*
- 👹 Path of Proof countdown *(premium)*
- ⚔️ Guild Scramble countdown *(premium)*
- 🕵️ Weekly Boss Run schedule countdown *(premium)*
- ⏱️ Custom Countdown Timers *(premium)*

The **category channel** updates every 10 minutes with compact times:
```
🕒18:42 | D 21H 49M | W 2D 04H | M 6D 21H
🕒03:01 | 🔥RESET NOW | D 00H 08M | W 1D 00H
```

---

## 🔔 Automatic Role Pings

All pings tag the role selected during `/setup` (or a custom override if configured). All ping messages are automatically deleted 2 minutes after sending.

| Event | When it pings |
|---|---|
| Pharaoh / Legends / Sharenian Culvert | 1 hour before weekly reset |
| Guild Scramble | At 7:00 PM ("starting soon"), 7:05 PM ("5 min left"), 7:10 PM ("starting now") on Sat & Sun |
| Path of Proof | 1 hour before timer expires |
| Boss Timer | At your configured day and time |
| Custom Pings | At your configured daily or weekly time |
| Countdown Timer | When a timer reaches zero |

---

## ⏱️ Setting Up a Boss Timer (`/bosstimer create`)

The boss timer tracks your guild's weekly boss run and pings the role at your set time.

1. Run `/bosstimer create`
2. Select the **day of the week**
3. Enter the **time** (HH:MM in your server's timezone)
4. Enter the **ping message** (e.g. `Boss run starts now! Log in!`)
5. Configure **who to ping** — default role, custom role, or a specific user

---

## 🗓️ Setting Up Custom Pings (`/customping create`)

Custom pings let you schedule any recurring message with a role or user mention.

1. Run `/customping create`
2. Choose **Daily** (fires every day) or **Weekly** (fires on a specific day)
3. Enter the **time** (HH:MM) and your **message**
4. For weekly pings, select the **day of the week**
5. Choose **who to ping** — default role, custom role, or specific user

Use `/customping list` to see all active pings and their assigned numbers.
Use `/customping delete <number>` to remove one.

---

## ⏳ Countdown Timers (`/countdowntimer create`)

Countdown timers display a live countdown in the embed and ping when they expire.

1. Run `/countdowntimer create`
2. Enter a **title** (e.g. `Moonlight Event`)
3. Enter the duration in **days**, **hours**, and **minutes**
4. Enter the **ping message** to send when the timer expires

You can create multiple timers. Use `/countdowntimer check` to see them all and `/countdowntimer clear <number>` to remove one.

---

## 💳 Pricing

| Plan | Price | Coverage |
|---|---|---|
| Subscription | $2.50 / month | Premium on all bots, unlimited servers |
| Lifetime | $25 one-time | This bot only, 1 server (transferable) |

Run `/premium` to see payment links. Run `/payment-status` to check your current status.

---

## 🆘 Support

Contact **tinustk** on Discord for any questions, bugs, or support.
