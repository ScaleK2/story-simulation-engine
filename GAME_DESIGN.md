# Story Simulation Engine
Version: 0.1
Status: Design

---

# Vision

Build a lightweight, turn-based simulation engine capable of generating emergent stories through simple player decisions.

The first implementation of the engine is a modern reimagining of Drug Wars - a game centred around economic trading, risk, reward, and survival.

The engine itself should be genre-agnostic. Future implementations should support political strategy, dynasty management, corporate empires, medieval kingdoms, space trading, or any other simulation built upon the same underlying systems.

---

# Success Criteria

Version 0.1 is considered successful when a player completes a full game and immediately wants to start another run.

The goal is not feature completeness.

The goal is an addictive gameplay loop.

---

# Design Philosophy

The game should be:

- Easy to learn
- Difficult to master
- Entirely driven by systems rather than scripted stories
- Deterministic where possible
- Data-driven
- Highly expandable

Players should never feel like they are following a predefined narrative.

Instead, stories should emerge naturally through their decisions and the world's response.

---

# Player Fantasy

You begin as a nobody.

You have debt.

Very little cash.

No reputation.

No influence.

Your only objective is to survive long enough to build wealth.

How you achieve that is entirely your decision.

---

# Core Gameplay Loop

Every turn follows the same structure.

Observe
↓
Make Decisions
↓
Advance Time
↓
World Simulation Updates
↓
Random Events Trigger
↓
Repeat

The Version 0.1 gameplay loop is:

Check Market Prices
↓
Buy Goods
↓
Travel
↓
Market Prices Change
↓
Random Event
↓
Sell Goods
↓
Manage Finances
↓
Repeat

---

# Player Goal

Increase total net worth before the game timer expires.

Net Worth =
Cash
+ Bank Balance
+ Current Inventory Value
- Outstanding Debt

---

# Starting State

Cash: $2,000
Debt: $5,500
Bank: $0
Health: 100
Inventory Capacity: 100
Current Location: Bronx
Day: 1

---

# Core Resources

The simulation tracks the following player state:

- Cash
- Debt
- Bank Balance
- Health
- Inventory Capacity
- Inventory
- Current Location
- Current Day
- Net Worth

---

# Cities

Version 0.1 contains five cities.

- Bronx
- Harlem
- Queens
- Brooklyn
- Manhattan

Each city generates unique market prices every day.

Cities themselves contain no gameplay logic.

They simply provide state used by the simulation.

---

# Goods

Goods are data.

The engine should never hardcode specific items.

Version 0.1 includes:

- Weed
- Cocaine
- Heroin
- Acid
- Speed
- Weapons

Each good defines:

- Name
- Base Price
- Minimum Price
- Maximum Price
- Volatility
- Inventory Size
- Rarity

Future simulations should be able to replace this dataset without modifying engine code.

---

# Player Actions

Version 0.1 supports only the following actions.

- Buy Goods
- Sell Goods
- Travel
- Deposit Cash
- Withdraw Cash
- Pay Debt
- End Turn

No additional player actions exist in Version 0.1.

---

# Random Events

Random events occur after travelling or ending a turn.

Examples include:

- Police Search
- Mugging
- Unexpected Windfall
- Market Crash
- Market Boom
- Hospital Bill
- Debt Collector
- Street Informant

Every event must modify simulation state.

No event should exist purely for flavour.

Every event must have mechanical consequences.

---

# Victory

Reach the final day with the highest possible net worth.

---

# Defeat

The player loses if:

- Health reaches zero.
- Debt exceeds the maximum threshold.
- The final day is reached with negative net worth.

---

# Design Principles

Every decision should involve trade-offs.

The player should constantly ask:

- Should I take this risk?
- Should I travel now?
- Should I hold inventory?
- Should I repay debt?
- Should I gamble on better prices elsewhere?

There should never be one mathematically perfect strategy.

---

# Simulation Principles

The simulation should be:

- Deterministic where possible
- Data-driven
- Event-based
- Easy to extend
- Independent from the user interface

The UI displays simulation state.

The UI never contains game logic.

---

# Engine Philosophy

The engine is responsible for updating the world.

It has no knowledge of drugs, kingdoms, corporations, politics, or any specific theme.

The engine only processes simulation state.

Every turn follows the same lifecycle.

1. Read Current World State
2. Apply Player Action
3. Advance Time
4. Update Simulation
5. Trigger Eligible Events
6. Resolve Consequences
7. Produce New World State

Every future feature should fit within this lifecycle.

If it cannot, the feature should be reconsidered.

---

# Engine Roadmap

Future engine capabilities may include:

- NPCs
- Character Traits
- Relationships
- Families
- Factions
- Territory Control
- Politics
- Businesses
- Dynasties
- Persistent Worlds
- Save Games
- Mod Support

These systems should only be introduced after the Version 0.1 gameplay loop is proven to be enjoyable.

---

# Out of Scope

Version 0.1 intentionally excludes:

- NPCs
- Relationships
- Families
- Politics
- Territory Control
- Businesses
- Combat
- Crafting
- Quests
- Character Progression
- Multiplayer

These features are deliberately postponed to prevent scope creep.

---

# Architectural Principles

The engine should separate simulation from presentation.

Simulation determines what happens.

The UI determines how it is shown.

Content should be defined through data files wherever possible.

The long-term goal is that a completely different game can be built by replacing data and content without changing the underlying simulation engine.

---

# Guiding Principle

The engine does not create stories.

It creates systems.

Stories emerge naturally from players interacting with those systems.
