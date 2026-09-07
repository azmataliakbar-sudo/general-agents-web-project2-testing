# Project 2: The Three-Tier Audit — Experiment Log (Actual Results)

**Difficulty**: Easy | **Time**: 30 min | **Uses**: Concepts 4 – 6 and 8

---

## What I Actually Did

1. Opened a fresh chat (Session layer — not saved to a Project)
2. Asked for: *"7-day beach vacation packing list with a budget estimate"*
3. Asked Claude to report which tier the file landed in

---

## What Actually Happened

- **Only ONE file was created**: `beach-vacation-packing-list.md`
- It went **straight to Tier 3** (downloadable) — no separate budget.csv, no Tier 1 scratch file, no Tier 2 file
- This is normal: a simple, single-output task doesn't need all three tiers

**Corrected tier table:**

| Tier | What Happened |
|------|----------------|
| Tier 1 (scratch) | Not used — no draft/intermediate file needed |
| Tier 2 (account) | Not used — went directly to a downloadable file |
| Tier 3 (yours) | ✅ `beach-vacation-packing-list.md` — downloaded to my computer |

---

## The Vendor-Loss Question — Real Answer Given

**I asked**: *"If my account disappeared tomorrow, what would I lose from this conversation?"*

**Claude's real answer**:
- ❌ Lost: this conversation history, any memory files about me
- ✅ Kept: the packing list file — **only if I had already downloaded it**

**Key catch Claude pointed out**: the file exists on Claude's servers until I click download. Before downloading, it's still Tier 2-like (account-dependent). After downloading, it becomes true Tier 3 (mine).

---

## Where I Saved the Evidence

```
C:\Projects\general_agents_web\project_2\
├── README.md
├── experiment-log.md              ← this corrected file
├── beach-vacation-packing-list.md  ← the real Tier 3 deliverable
├── docs\
└── src\
```

---

## Done Criteria (my own words)

> "Every file lives in one of three places: temporary scratch (Tier 1), the vendor's account (Tier 2), or my own computer (Tier 3). If my account disappeared, I'd lose the conversation and anything still sitting only in the account. The only thing safe is what I actually downloaded. So the rule is: always download finished work — don't leave it sitting in the chat."

---

*Project 2 complete — real evidence recorded, no fabricated files.*
