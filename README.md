# Pokenya

## DEMONSTRATION SCREENSHOTS ARE NOW ADDED!! [View Features Demo](pictures/)

## A sidenote
- Hello it's me, back with a newer & better bot/cheat for pokemeow!!
- This new product boasts a much better captcha solver. In fact I'm no longer worried I'm failing captchas like I did with yugen's and primrose's older models.
- I also managed to create a proper GUI this time with a few interesting & useful features/QOL that IK yall love.
- Prices are upped and we're doing subscriptions now, primarily since I want to keep the circle small, and every client satisfied & safe. Yugen is still up for sale if yall want a cheaper alternative!
- Enjoy!

## Overview

- **Graphical user interface!** With beautiful logging, a captcha solve reviewer, and session management screen! **19 themes** are preinstalled for you to choose your flavor!
- Run **multiple accounts**, each account executing **multiple commands** (;p, ;f, ;b, ;exp), all at the same time!
- **CRAZY CAPTCHA SOLVER!** Solves faster and more accurate than you (and I) do!
- **POG battle AI** which battles, switches mon, forfeits by itself, and choose moves while taking type effectiveness, pokemon stats, STAB bonus, held items.. into calculation!
- **Everything is customizable!** from bot behaviour to log colors.
- **Configurable PC notifications, Discord message forwarding** to know when your bots have encountered something **BIG**!
- Super EZ and fast installation!

## Pricings

- Contact via discord for inquiries/orders: `itsfram`

### Subscriptions

- **1 month**:
  - $6 each for hunt/fish/battle **EACH**
  - $3 for explore
- **6 months**: 10% discount
- **12 months**: 25% discount

### Lifetime/Forever

- _Hunt_ forever: $45
- **Hunt/fish** forever: $70
- **Hunt/fish/battle** forever: $100
- **everything** forever: $120
  - Includes any future commands developed without paying extra.

### Extension packages:

- Account limit: 1 usd for each
- **Device allowance: non-purchasable. Requires a second license.**

### Included in every purchase:

- GUI with all GUI features. (logs, captcha review, session manager)
- Local captcha solver.
- Tasks module handling all shop, faction, hunt, lb, grazz, etc. tasks
- **3 accounts** allowance
- **1 device** allowance

# Full Feature list

## 🎯 Hunt (;p)

### Ball Usage System

- **Absolute customizability** for catching Pokemon with different rarities, held items, special held items, daily hunt, faction hunt, or custom Pokemon
  - Rarity-based ball config: Common, Uncommon, Rare, Super Rare, Trio, Mythical, Legendary, Event Legendary, Full-Odds Shiny, Event Shiny, Regular Event Shiny, Trio Shiny, Shiny Mythical, Golden, Event Special
  - Separate ball config for Pokemon with held items `[regular_ball, with_item_ball]`
  - Special held item ball config: custom balls for Pokemon holding Lucky Egg, Everstone, Razor Claw, etc.
  - Daily hunt ball override: uses priority balls when Pokemon is today's daily hunt target
  - Faction hunt ball config: whitelisted ball types and rarities for own/other faction hunts
  - Custom Pokemon config: define specific balls for individual Pokemon (event Pokemon, collection targets, etc.)
  - Priority Pokemon config: Pokemon that use custom balls when not daily hunt (e.g., cheap legendaries)
  - Fallback ball system: tries alternative balls if preferred ball unavailable

### Daily Hunt System

- Daily hunt target tracking with automatic detection from bot messages
- Status monitoring (not_completed/completed)
- Supports both embed and content-only message formats

### Faction Hunt System

- Faction detection (Rocket, Plasma, Galactic, Flare, Skull,..)
- Whitelisted ball types for own faction hunts
- Separate whitelist for other faction hunts (reward less faction points)
- Rarity whitelist: only catch faction hunts of specific rarities
- Toggle to enable/disable catching other faction hunts

### Configuration

- Common custom Pokemon/priority Pokemon config shared across all accounts
- Per-account ball config with separate held item configuration
- Toggle-based faction hunt settings
- Daily hunt integration toggle

## 🎣 Fish (;f)

### Ball Usage System

- Rarity-based ball config with fallback system
- Water state detection (GOLD, INTENSE, STRONG, CALM, MODERATE)
- Smooth & crash-free fishing! Finally!

## ⚔️ Battle (;b)

### Battle AI System

- Pulls Pokemon data from APIs for corect stat distributions.
- Parses pokemon's status, forms and their held items, STAB bonus, Golden stat boost to accurately calculate damage.
- Optimal move selection based on damage.
- Switch logic: switches when current pokemon faints.
- Forfeit logic: conditionally forfeits when last pokemon under defined HP or HP% threshold.

### League Progression Option

- Automatic NPC advancement: progresses sequentially (1 → 2 → 3 → ... → 78)
- Prerequisite detection: switches to required NPC when attempting out-of-order battles
- Max NPC loop: resets to NPC 1 after reaching configured max (default: 78)
- Single mode: repeatedly battle same NPC

### Configuration

- Battle mode toggle: league vs single
- Configurable NPC ID.

## 🗺️ Explore (;exp)

### Navigation System

- **Systematic snake/zigzag pattern**: moves horizontally to edge, then down and reverses
- Position tracking: parses and maintains X,Y coordinates (29x10 grid)
- Smart movement: automatically determines available direction based on available buttons
- Multi-map support: rotates through configured map list (gm1, gm2, fm1, wm1, etc.)

### Encounter & Catch System

- Automatic Pokemon encounter detection with rarity parsing
- Explore-specific ball config with fallback system
- Continuous exploration after encounters

### Session Management

- Step counter with daily limit detection
- Auto-termination when step limit reached
- Auto-restock (exiting and buy balls) when balls run out mid-exploration

### Configuration

- Configurable map list
- Per-rarity ball configuration
- Step delay between movements

## 🧩 Captcha Solver

### AI Solver

- Best captcha solver there is! Local & doesn't require extra fees to use.
- **GPU acceleration** (CUDA) for much faster solving - sub-second on GPU, 4-5s on CPU
- **CPU fallback** when GPU unavailable
- All accounts use the same captcha solver instance, thus save your PC resources.

### Smart Retry System

- Automatic retry on failed attempts (bot gives up to 5 attempts)
- **Configurable max retries** to prevent ban from too many wrong answers (default: 3)
- Attempt tracking: monitors attempts used and remaining
- Auto-stop solving after max retries reached

### Review Screen

- Captcha review tab in the GUI.
- Solves the captchas, and then post the image along with solve onto the GUI, and waits for the user to approve the solve/manually fix the solve.
- Auto-submits after configurable duration (10-15s), or manually submits after user review.
- (Optional) Persistent storage of captcha images in a folder.

### Error Handling

- Image download retry (up to 3 attempts)
- HTTP 503 error handling with retries
- Download failure detection and alerts
- Timeout protection (solve timeout + force solve timeout)

### Configuration

- Model path
- Storage enable/disable and path
- Max retry limit (1-5)
- Response delay min/max
- Solve timeout and force solve timeout
- Download retry count and delays
- HTTP 503 retry behavior

## 🎁 QOL & Automation Features

### Notifications & Forwarding

- Desktop notifications for rare Pokemon spawns (hunt, fish, explore)
- Rarity exclusion list: configure which rarities trigger notifications
- Custom Pokemon notification toggle
- Encounter forwarding: forwards the entire spawn messages to a Discord user/channel
- Special item forwarding: similar to encounter forwarding
- Captcha notifications: appear, failed attempt, stop solving, solved, download failed
- Egg hatch notifications: alerts for exclusive, shiny, golden hatches
- Every notification is togglable on/off.

### MeowHelper Integration

- Command ready detection from MeowHelper bot
- Automatic cooldown reset when MeowHelper signals command ready
- Multi-command support: pokemon, fish, battle, swap, egg

### Vote Ready Detection

- Vote button recognition during commands
- Colored, blinking alert in logs when vote available

### Egg Management

- Auto-hatch: automatically hatches eggs when ready
- Auto-hold: option to hold eggs instead of hatching
- Egg detection in inventory
- Special egg hatch tracking (exclusive, shiny, golden)

### Lootbox System

- Auto-open lootboxes when available
- Auto-repel: automatically uses repel items from lootboxes
- Auto-grazz: automatically uses grazzberry items from lootboxes
- No lootbox detection

### Daily Tasks

- Daily claim automation
- Faction page tracking
- Quest completion detection with auto-continue

### Channel Management

- Multi-channel support with configurable channel IDs
- Auto-channel switching at randomized intervals
- Configurable switch timing (min/max seconds)
- Channel whitelist enforcement

### Command Queue System

- Priority-based execution: CRITICAL > HIGH > NORMAL > LOW
- Per-command-type cooldown tracking
- Smart scheduling with randomized delays
- Command cancellation by type (useful for bans, limits)
- Queue pause/resume (e.g., during captcha)

## 🛒 Shop & Inventory

### Auto-Purchase System

- Threshold-based buying: starts buying when inventory reaches threshold (not 0)
- Randomized buy amounts in range `[min, max]` per ball type
- Multi-ball support: pokeball, greatball, ultraball, masterball, premier ball, dusk ball, beast ball
- Smart restocking: only buys items below threshold

### Configuration

- Per-ball-type threshold (e.g., threshold: 5 = buy when count reaches 5)
- Per-ball-type buy amount range (e.g., `[10, 20]` = randomly buy 10-20)
- Shared ball config across hunt, fish, explore modes

## 🔐 Security & Anti-Detection

### Randomization

- **Randomized button click delays**: all button interactions use min/max delay ranges
- **Randomized cooldowns**: all command types use min/max cooldown ranges
- **Randomized buy amounts**: shop purchases vary within configured range
- **Randomized channel switch timing**: varies between min/max seconds
- **Randomized captcha response delay**: human-like timing before submitting answer

### Rate Limiting & Error Handling

- Rate limit detection: handles "sending messages too fast" errors with backoff
- Maintenance detection: recognizes bot maintenance and waits (10 minutes)
- Ban detection: identifies temporary bans and clears command queue
- Permanent ban detection: stops session on perm ban
- Overlapping command detection: waits when another command is active
- Captcha integration: pauses queue, resets cooldowns after solve

### Timing Configuration

- Configurable delays for hunt, fish, battle, explore button clicks
- Configurable cooldowns for each command type
- Captcha response delay range
- Shop purchase timing

## 📊 Statistics & Logging

### Session Tracking

- Pokemon caught per rarity tier
- Battles won/lost/forfeited/timeout
- Fish caught with token tracking
- Eggs hatched by type (exclusive, shiny, golden)
- Captchas solved/failed with attempt counts
- Explore steps taken with coin/Pokemon totals
- Session uptime and command execution counts

### Color-Coded Logging

- Rarity color coding in logs (configurable colors per rarity)
- Faction color coding
- Tag colors (custom, priority, item, vote_ready, shiny, hunt)
- Water state colors for fishing
- Reward colors (EXP, coins, items)
- Status colors (caught, fled, broke_out)
- Message colors (maintenance, temp_ban, error)
- Battle indicator colors (shiny, golden, mega)
- Timestamp display with customizable colors

### Detailed Event Logs

- Pokemon encounter logs with all special flags
- Battle decision logs with move selection reasoning
- Explore movement logs with position tracking
- Captcha solve logs with timing and retry count
- Shop purchase logs with amounts and costs
- Daily hunt status updates
- Faction hunt detection logs

## ⚙️ Configuration System

### Multi-Level Configuration

- System-wide config (system.json): database, captcha solver, logging, session management, performance, colors
- Common config (common.json): custom Pokemon, priority Pokemon, notifications, special held items
- Per-account config (accounts/\*.json): tokens, channels, per-mode settings (hunt, fish, battle, explore, eggs, lootbox)
- Shared ball config: centralized inventory thresholds and fallback chains

### Session Management

- Max concurrent sessions
- Session timeout and command timeout
- Health check interval
- Captcha wait timeout
- File name as session name option
