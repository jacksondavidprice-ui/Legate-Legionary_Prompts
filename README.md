# User Instructions

## Overview

- **Legate** - Talks to you, assigns tasks to legionaries, monitors their progress
- **Legionaries** - Numbered workers (legionary-1, legionary-2, etc.) that do the actual coding

---

## Quick Start

### 1. Approve Everything Mode
Put Cursor in YOLO (deprecated) / approve everything mode. This is strongly recommended.

### 2. Start Legate
Create a new agent in Cursor and paste the Legate prompt.

### 3. Start Legionaries
For each legionary you want, create a new agent and paste the Legionary prompt.

The legionary will automatically:
- Check `agents/legionaries/` to see existing legionaries
- Pick the next available number
- Create its own directory at `agents/legionaries/legionary-<N>/`
- Create all its files
- Register itself
- Start watching for tasks

**You don't need to tell the legionary its number** - it figures it out automatically.

(Optional: You can still explicitly say "You are legionary-5" if you want a specific number.)

### 4. Use the System
Talk to Legate. It assigns tasks. Legionaries execute automatically.

Legate actively monitors legionaries - it doesn't just wait for your input. It will:
- Detect when legionaries complete tasks
- Answer legionary questions automatically
- Report back to you when work is done

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

[Legate watches legionary-1's status...]

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

Just create a new agent with the legionary prompt. It will:
1. Auto-detect its number from existing folders
2. Bootstrap itself
3. Register and start watching

---

## Troubleshooting

**Legionary not responding:**
- Click "continue" if there were network or timeout errors (MOST COMMON - happens when you switch networks or close the computer)
- Check its status.json
- Check if file watcher is running
- Tell the legionary to continue
- Approve any potentially frozen commands

**Legionary confused about identity:**
- Tell it: "You are legionary-X" 
- Have it re-read its profile.json

**Task not picked up:**
- Verify task.json was written
- Check legionary's status.json
- The legionary may have timed out - tell it to resume watching

**Task keeps failing despite legionary saying it's done:**
- Tell Legate to assign to a different legionary
- Fresh eyes often catch issues the original legionary missed

**Legionary crashed:**
- This is a limitation of the Cursor system
- Click "continue" in the legionary's Cursor window
- Or ask Legate to reassign the task to another legionary

---

## File Watcher Timeouts

Legionaries use a 10-minute timeout on their file watchers to prevent Cursor agent timeouts. When a timeout occurs, they simply restart the watch. This is normal behavior - it prevents the agent from becoming unresponsive.
