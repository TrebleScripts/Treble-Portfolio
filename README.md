# Treble-Portfolio
Professional Roblox scripting portfolio
*By Treble (@losttreble#8848)*

Hey, I’m Treble — a 22-year-old full-stack Roblox scripter with over 2 years of experience and hundreds of hours dedicated to mastering both client and server-side development on the platform.

I specialize in building complete, production-ready systems such as:
- 🧳 Inventory frameworks with GUI + saving
- ⚔️ Frame-based combat with animation syncing
- 🎰 Gacha summoning systems with pity + auto-sell
- 🧠 Turn-based AI logic with grid-based movement

I have a deep understanding of the Roblox API and a strong grasp of best practices used by top studios. While I don’t handle animations or VFX directly, I’m capable of scripting nearly any gameplay or backend system from the ground up.

I build systems that are **modular**, **scalable**, and designed for **long-term content expansion**. I focus on performance, readability, and reliability.

Most recently, I completed Clone Battles — a full-featured AI combat game built entirely from scratch.

---

## 📬 Availability

- ⏰ **Time Zone:** EST  
- 💬 **Discord:** `losttreble#8848`  
- 💼 **Commissions:** Open to part-time, long-term, or task-based work. Timeframes are always communicated up front.  
- 💰 **Payment:** USD preferred. For larger or long-term projects, I’m open to negotiating % revenue share.

---

## 🐾 Advanced Pet System

**Features:**
- Follows player using `Humanoid:MoveTo`
- Dynamic idle/walk animation control
- Clean no-collision logic
- Modular and expandable for stat or buff tracking

🎥 [![Watch Demo](https://img.youtube.com/vi/71atHFBhXtY/0.jpg)](https://youtu.be/71atHFBhXtY)

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

### 📄 Code Sample: M1 Starter

```lua
function CombatController:StartM1Combo()
	if self.CurrentState ~= StateEnum.IDLE then return end
	self:SetState(StateEnum.ATTACKING)
	self:PlayAnimation("M1_" .. self.M1ComboStep)
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
