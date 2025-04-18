# 🎲 Monopoly

A full-featured, VGA-rendered implementation of **Monopoly**, developed on an **FPGA platform (DE1-SoC)** using **C**. The game features turn-based mechanics, smooth animations, audio effects, and real-time hardware interaction through PS/2 input, VGA output, and sound playback. While the game logic is entirely written in **C**, it runs on the DE1-SoC’s embedded system to directly control hardware peripherals like the VGA display, PS/2 keyboard, and audio output.

---

## 🚀 Features

### 🟦 1. Title Screen & Game Start
- Monopoly-themed **title screen** displayed on VGA
- Official **theme song** plays on loop
- Pressing **Enter** (via PS/2 keyboard):
  - Stops music
  - Begins the game
  - Transitions into the gameplay phase

---

### 🎲 2. Turn-Based Gameplay

#### 🎯 Dice Roll
- Press **Enter** to roll animated dice with sound effects
- Result is randomized and determines movement steps

#### 🚶 Movement
- Player token moves step-by-step with delay-based animation
- Smooth, animated traversal around the board

#### 🏠 Property Interaction
- Landing on a tile displays its **custom card and info** on the VGA side panel
- Each tile has unique data and graphics using custom drawing functions

##### 🟢 Unowned Property
- Prompted to **buy or skip** via PS/2 keyboard
- If bought: automatically places 1 house (no full set required)

##### 🔴 Owned Property
- Prompt to **build more houses** (up to 4 max)
- Rent increases with houses

##### 🚆 Railroads / ⚡ Utilities
- Can be purchased, but **houses cannot be built**

##### 🚓 Go to Jail
- Instantly places the player in jail

##### 🅿️ Free Parking / In Jail or Just Visiting
- No action triggered

##### 💵 GO Tile
- Landing or passing awards **$200**

---

### 🎲 Doubles Rule
- Rolling doubles grants an **extra turn**
- Rolling doubles **3 times in a row** sends the player to jail (third move skipped)

---

### 🃏 3. Special Tiles & Events

#### 💼 Chance & Community Chest
- Trigger **randomized effects**:
  - Gain/lose money
  - Movement changes
  - Jail consequences
  - "Get Out of Jail Free" cards

#### 🏛 Jail System
- Three release options:
  - Roll doubles (within 3 turns)
  - Pay bail
  - Use a card

#### 💸 Tax / 🅿️ Free Parking / 🚔 Go to Jail
- Behave according to official Monopoly rules

---

### 🖥️ 4. Visual & Audio Feedback

- **VGA Display**:
  - Real-time updates to board, player stats, and tile info
  - Smooth animation for token movement and house rendering

- **Audio Feedback**:
  - Background music
  - Dice sound effects

---

## 🔗 Links

- 🎥 **Video Demo**: [Watch on Google Drive](https://drive.google.com/file/d/1COoPDofs2tkl8vgkka4SR1U5thTGGrkh/view)  
- 💻 **Source Code**: [GitHub Repository](https://github.com/nathwung/monopoly)
