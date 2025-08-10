# Treble-Portfolio
Professional Roblox scripting portfolio
*By Treble (@losttreble#8848)*

Hey, I’m Treble — a 22-year-old full-stack Roblox scripter with 2+ years of experience building production-ready, studio-grade systems from the ground up. I’ve spent hundreds of hours mastering both client-side and server-side development, with a focus on creating gameplay and backend frameworks that scale effortlessly.

I specialize in developing complete, modular systems that combine polished UI/UX with secure, server-authoritative logic, including:

🧬 Dynamic trait and stat progression frameworks

🤖 Advanced AI with patrols, behavior modes, and squad logic

🛒 Monetization systems with gamepass shops, dev products, and promo codes

⚔️ Frame-based combat with synced animations, abilities, and cooldowns

🔫 Genre-spanning gameplay such as FPS weapon systems with bloom & recoil

📦 Fully modular inventory, drop, and economy systems

I follow best practices used by top studios, ensuring my code is readable, maintainable, and designed for long-term content expansion. While I don’t create animations or VFX myself, my systems are built to integrate seamlessly with them for polished final results.

Most recently, I’ve delivered Clone Battles and a range of advanced AI, progression, and monetization systems that demonstrate both technical depth and player-focused design.

---

## 📬 Availability

- ⏰ **Time Zone:** EST  
- 💬 **Discord:** `losttreble#8848`  
- 💼 **Commissions:** Open to part-time, long-term, or task-based work. Timeframes are always communicated up front.  
- 💰 **Payment:** USD preferred. For larger or long-term projects, I’m open to negotiating % revenue share.

---

## 🧬 Trait System — Dynamic Clone Modifiers
Features:

Fully scripted dynamic trait effects applied to units at spawn

Persistent stat modifiers, ability changes, or visual effects per trait

Modular trait definitions for easy expansion

Server-authoritative application to prevent exploits

Supports both passive and trigger-based trait logic

🎥 [![Watch Demo](https://img.youtube.com/vi/8CloLn2hFfU/0.jpg)](https://youtu.be/8CloLn2hFfU)

---

##  Advanced AI System — Patrols & Behavior Modes

**Features:**
- Enemy patrol routes with range-based aggro detection
- Units displaying Aggressive, Neutral, and Passive behavior modes
- State machine architecture for clean, maintainable logic
- Server-authoritative AI decisions with smooth client-side feelers

🎥 [![Watch Demo](https://img.youtube.com/vi/eTAlajXWrVA/0.jpg)](https://youtu.be/eTAlajXWrVA)

---

##  Stat System — Dynamic UI & Upgrades

**Features:**
- Modular stat upgrading with real-time preview of next-level gain
- Price display per upgrade that turns **green when affordable**, **red when not**
- Config-driven growth curves, pricing, and stat caps for scalable tuning
- Server-authoritative validation—secure and cheat-resistant design

🎥 [![Watch Demo](https://img.youtube.com/vi/2KGHHXWZSlU/0.jpg)](https://youtu.be/2KGHHXWZSlU)

---

##  Daily Spin & Daily Rewards — 24 hr Claim System

**Features:**
- Combined **Daily Spin** and **Daily Reward** mechanics with a strict 24-hour cooldown
- Smooth, responsive UI for both the spin wheel and daily claim interface
- Server-verified cooldown logic ensuring fairness and reliability
- Animated spin wheel with prize highlight and instant reward delivery

🎥 [![Watch Demo](https://img.youtube.com/vi/b4JnkmwbEGI/0.jpg)](https://youtu.be/b4JnkmwbEGI)

---

##  Quest System — Dialogue, Tasks & Progress Tracking

**Features:**
- Stage-based tutorial framework combining **dialogue** and **task-driven objectives**  
- UI tracks player progress (e.g., “Defeat 5 Grunts”) and advances automatically when tasks are completed  
- Smooth dialogue transitions framed with UI for clarity and immersion  
- Server-side validation of task progress to ensure secure progression logic

🎥 [![Watch Demo](https://img.youtube.com/vi/AGnAVWRvg04/0.jpg)](https://youtu.be/AGnAVWRvg04)

---

##  Loot & Currency System — Live Updates + Inventory Integration

**Features:**
- Boss defeat triggers **instant coin gain** with UI updates
- Configurable **drop logic** allowing unique items (e.g., abilities) to be awarded
- Inventory checked before and after drop to confirm successful delivery
- Server-authoritative handling ensures secure and reliable reward distribution

🎥 [![Watch Demo](https://img.youtube.com/vi/lERYbf_q680/0.jpg)](https://youtu.be/lERYbf_q680)

---

##  FPS Gun System — Bloom + Recoil & True Aim

**Features:**
- Hip-fire bloom that adds inaccuracy when shooting from the hip  
- Dynamic recoil applied per shot for realistic feedback  
- Aim-down-sights (ADS) mode removes bloom and enables pixel-precise accuracy  
- Right Mouse Button toggles ADS; mouse is hidden to prioritize visual output  
- Arms are welded to the gun in this prototype, which may look slightly off—final builds would use animations for realism  
- Server-authoritative hit registration ensures accuracy and cheat resistance

🎥 [![Watch Demo](https://img.youtube.com/vi/QG2JaUvORDE/0.jpg)](https://youtu.be/QG2JaUvORDE)

---

## 🐾 Advanced Pet System

**Features:**
- Follows player using `Humanoid:MoveTo`
- Dynamic idle/walk animation control
- Clean no-collision logic
- Modular and expandable for stat or buff tracking

🎥 [![Watch Demo](https://img.youtube.com/vi/71atHFBhXtY/0.jpg)](https://youtu.be/71atHFBhXtY)

---

##  Gamepass Shop & Code System — Monetization Ready

**Features:**
- Clean, responsive shop UI with support for **Gamepasses** and **Dev Products**
- Integrated **code redemption menu** for promo rewards
- Seamless **Studio test purchase** confirms gamepass or item appears in player inventory
- Modular backend built on `MarketplaceService` with verification for secure transactions

🎥 [![Watch Demo](https://img.youtube.com/vi/TQrDp08RWHQ/0.jpg)](https://youtu.be/TQrDp08RWHQ)

---

## 🧠 Advanced DataStore & Inventory System

**Features:**
- Caching, autosave, and dirty tracking
- Fully modular inventory system
- Equip/Unequip system with GUI support
- Persistent data with deep validation logic

🎥 [![Watch Demo](https://img.youtube.com/vi/wBUqW5cOU0Q/0.jpg)](https://youtu.be/wBUqW5cOU0Q)

---

## ✨ Gacha Summon System

**Features:**
- Simulator-style summon pads
- Scroll currency + pity system
- Rarity-based auto-sell & gamepass support
- Clean unit result display & inventory update

🎥 [![Watch Demo](https://img.youtube.com/vi/MGMtambZZjM/0.jpg)](https://youtu.be/MGMtambZZjM)

📄 **Code Sample: Binding Inputs-CombatSystem**
```lua
function CombatController:BindInputs()
	UserInputService.InputBegan:Connect(function(input, gameProcessed)
		if gameProcessed then return end -- Ignore UI or chat inputs
		if self.InputLocked then return end -- prevent stacking
		if self.CurrentState ~= StateEnum.IDLE then return end --Prevents spamming while attacking blocking etc
		
		if input.UserInputType == Enum.UserInputType.MouseButton1 then
			self:StartAttack()
		end
	end)
```
---

## ⚔️ Modular Frame-Based Combat (Early Build)

**Features:**
- Directional dash system using Body Velocity
- M1 combo startup with state machine logic
- Ability execution with animation syncing
- Clean, maintainable CombatController logic

🎥 [![Watch Demo](https://img.youtube.com/vi/qMwRrTa3a9c/0.jpg)](https://youtu.be/qMwRrTa3a9c)

### 📄 Code Sample: Spawn SLot Lock With Timeout

```lua
type SlotTimestampMap = {[number]: number}

local LOCK_TIMEOUT: number = 10
local ActiveCloneSpawn: {[Player]: SlotTimestampMap} = {}

local function isLocked(player: Player, slot: number): boolean
	local map: SlotTimestampMap? = ActiveCloneSpawn[player]
	local v: number? = map and map[slot]
	if v == nil then
		return false
	end
	-- timestamp-based lock with timeout to avoid deadlocks
	if typeof(v) == "number" and (tick() - v > LOCK_TIMEOUT) then
		(map :: SlotTimestampMap)[slot] = nil
		return false
	end
	return true
end
```
---

## 🔥 Kamehameha Ability (VFX Prototype)

**Features:**
- Charge-based beam ability
- Raycast damage with forward targeting
- Animation-locked cast time
- Server-authoritative execution

🎥 [![Watch Demo](https://img.youtube.com/vi/JjYn_r5dQQI/0.jpg)](https://youtu.be/JjYn_r5dQQI)

---

## 🏗️ Tycoon Income System

**Features:**
- Passive income through HexCoin generators
- Upgrade system tied to GUI buttons
- Currency stored server-side
- Clean part-cloning placement logic

🎥 [![Watch Demo](https://img.youtube.com/vi/grtWmGFbn30/0.jpg)](https://youtu.be/grtWmGFbn30)

---

✅ Completed Projects
Here are a few fully scripted systems or games I’ve completed from the ground up:

🎮 Clone Battles (Playable Demo)
https://www.roblox.com/games/137293741350231/NEW-Clone-Battles

Player-controlled clones auto-attack enemies with active behaviors

Dynamic trait, ability, and stat progression systems

Fully modular backend: combat, inventory, respawn, and tutorial

Built from scratch using scalable, production-grade architecture

More completed games will be added as I wrap up each milestone project.

---

## 📬 Let's Work Together

Thanks for checking out my portfolio!

If you have any questions about a system I built, want to see more examples of my work, or you're unsure whether your project is a good fit — feel free to reach out. I'm happy to walk you through my process, explain how I approach problems, or talk about how I can help bring your game to life.

I work best with teams and clients who value:
- Clean, modular code that's built to scale
- Clear communication and reliability
- Game systems designed for long-term content expansion

Whether you need a full framework, a single system, or just help refining your current mechanics, I’ll bring a high standard of quality and long-term thinking to the table.

---

📅 **Available for commissions**  
💬 **Discord:** `losttreble#8848`  
💰 **Payment:** USD preferred; open to revshare for larger scoped projects

> If you're looking for a professional Roblox scripter who builds with purpose and polish — you’ve found the right person.
