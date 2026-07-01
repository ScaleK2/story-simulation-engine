# Story Simulation Engine
A lightweight, turn-based simulation framework for building emergent strategy and management games.

The framework is designed around a simple principle:

> World State -> Player Action -> Simulation -> Events -> New World State

Rather than scripting stories, the framework provides systems from which stories naturally emerge.

---

## Project Goals

- Build reusable simulation systems
- Keep gameplay data-driven
- Separate simulation from presentation
- Support multiple game implementations on the same framework

---

## Project Principles

- Build the smallest possible playable loop.
- Prefer simple systems over complex features.
- Keep the simulation independent from the UI.
- Avoid hardcoded game content.
- Optimise for extensibility rather than feature count.

---

## Current Status

Version: 0.1

The first implementation validates the framework through a simple economic trading simulation inspired by classic games such as Drug Wars.

See `GAME_DESIGN.md` for the current game design.

---

## Version 0.1 Success Criteria

A player can:

- Start a new game
- Buy goods
- Sell goods
- Travel between cities
- Experience random events
- Complete a full 30-day run
- Win
- Lose
- Immediately want to play again
