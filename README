# User Instructions

## Overview

- **Legate** - Talks to you, assigns tasks to legionaries
- **Legionaries** - Numbered workers (legionary-1, legionary-2, etc.) that do the actual coding

---

## Quick Start

### 1. Start Legate
Open a Cursor window, paste the Legate prompt.

### 2. Start Legionaries
For each legionary you want, open a new Cursor window and paste the Legionary prompt with their number:

> "You are legionary-1"

or

> "You are legionary 2"

The legionary will:
- Create its own directory at `agents/legionaries/legionary-1/`
- Create all its files
- Register itself
- Start watching for tasks

### 3. Use the System
Talk to Legate. It assigns tasks. Legionaries execute automatically.

---

## How Many Legionaries?

Start with 1-3 for small projects. Add more as needed.

You can have multiple legionaries doing similar work - they're generalists by default.

---

## Specialization (Optional)

For large codebases, Legate can assign legionaries to specific areas:
- "legionary-1 and legionary-2, focus on frontend"
- "legionary-3, you handle the backend"

This is **optional**. Small projects don't need it.

---

## Example Session

**You to Legate:**
> "Add a pause menu"

**Legate:**
> "Assigned to legionary-1. They're working on it."

[legionary-1 automatically wakes up, does the work]

**Legate (after completion):**
> "Done. legionary-1 created pause_menu.tscn and integrated it."

---

## Checking Status

Ask Legate:
- "What's legionary-1 doing?"
- "Are there any stuck legionaries?"
- "Show me what's been completed"

---

## Adding More Legionaries

Just start a new Cursor window with the legionary prompt:
> "You are legionary-4"

It will bootstrap itself and register.

---

## Troubleshooting

**Legionary not responding:**
- Check its status.json
- Check if file watcher is running
- Restart the legionary window

**Legionary confused about identity:**
- Tell it: "You are legionary-X" 
- Have it re-read its profile.json

**Task not picked up:**
- Verify task.json was written
- Check legionary's status.json
