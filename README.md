# Project 2: The Three-Tier Audit

**Difficulty**: Easy | **Time**: 30 min | **Uses**: Concepts 4 – 6 and 8

---

## What Are Concepts 4 – 6 and 8?

| Concept | Name | What It Teaches |
|---------|------|-----------------|
| **Concept 4** | The Account Spine (State Layers) | Persistence has layers: Session / Project / Memory / Instructions / Files |
| **Concept 5** | The Three File Tiers | Every file lives in tier 1 (scratch), tier 2 (platform), or tier 3 (your custody) |
| **Concept 6** | Connectors on the Web | Reach paths: connector → built-in browser → Chrome context → computer use |
| **Concept 8** | The Delegation Discipline | Briefing, planning, approval, and review of delegated work |

---

## Concepts in Simple Words

### Concept 4 – The State Spine (5 Layers)

The agent's memory is a **stack of 5 layers**, not one thing called "memory":

| Layer | Question It Answers | Lifetime |
|-------|---------------------|----------|
| **Session** | What happened in this particular task? | One workstream |
| **Project** | What belongs to this continuing body of work? | Weeks / months |
| **Memory** | What facts/preferences should carry across sessions? | Cross-session |
| **Instructions** | How should the assistant generally behave here? | Until changed |
| **User-Owned File** | What do I want portable and inspectable? | As long as you keep it |

### Concept 5 – The Three File Tiers

Every file your agent touches lives in ONE of three tiers:

| Tier | Name | Description | Custody | Lifetime |
|------|------|-------------|---------|----------|
| **Tier 1** | Task Filesystem | Temporary working space, scratch drafts | Vendor (temp) | Until task ends |
| **Tier 2** | Platform Storage | Files saved permanently to your account | Vendor (your account) | Survives tab close |
| **Tier 3** | The Exit | Files in a place YOU control (Drive, local folder, repo) | **YOU** | Yours forever |

**The key rule**: **Finished work exits the platform. Everything else may stay.**

### Concept 6 – Connectors on the Web

Four reach paths from most to least structured:

1. **Connector** (Gmail, Drive, Slack APIs) → best for structured systems
2. **Built-in Browser** → for portals, forms, dashboards
3. **Claude in Chrome** → for pages already in your existing browser
4. **Computer Use** → for apps with no other interface (highest risk)

**Rule**: Use the most structured tool that can do the job.

### Concept 8 – Delegation Discipline

The four-step discipline for delegated work:
1. **Brief** the agent clearly
2. **Plan** mode lets you see and approve the approach
3. **Run** the task
4. **Review** the output

---

## What You Will Do

Run one task that produces a **real deliverable** while auditing:
- Which **state layer** holds each piece of work
- Which **file tier** every output lands in
- What useful context would be **lost** if the vendor account disappeared

---

## Step-by-Step Instructions

### Step 1: Choose a Real Deliverable Task

Pick a small task that produces a file you can actually use. Good options:
- A meeting agenda for next week
- A weekly status report
- A trip packing list with budget estimate
- A comparison table of three products
- A summary of notes you dictate

**For this project, use**: *"Create a 7-day trip packing list for a beach vacation with budget estimate"*

---

### Step 2: Open a Cloud Session

1. Open your cloud session in the browser
2. Start a new conversation (or use a new Project if your setup supports it)
3. The agent loop is now in the **cloud** (Concept 1 / Project 1)

---

### Step 3: Name the State Layer (Concept 4)

Before giving the task, identify which **state layer** will hold the work:

| If you start it in a... | It lives in... |
|------------------------|----------------|
| Fresh chat with no Project | **Session** layer only |
| A named Project | **Project** layer (persists for weeks/months) |
| You want it to recall preferences later | Needs **Memory** layer enabled |
| You have standing rules ("always be concise") | Those live in **Instructions** layer |

**For this audit**:
- Start the task in a new chat (so it lives in the **Session** layer)
- Do NOT save it to a Project (keeps it scoped to this one task)
- Note this: when the session ends, this work is bounded

---

### Step 4: Brief the Agent with Tier Awareness (Concepts 5 + 6 + 8)

Use this exact brief:

```
I need a 7-day beach trip packing list with a budget estimate.

When you're done, end by listing every file you created and where each one landed:
- Temporary working space (tier 1)
- Platform storage / my account (tier 2)
- A system I control: connector save, download, local write, or repo commit (tier 3)

The final deliverable should exit the platform to tier 3 (download to my computer).
```

**This is Concept 8 (Delegation Discipline)** — you are clearly briefing the agent.

---

### Step 5: Watch the Agent Work

The agent may:
- **Plan first** (if Plan mode is available) — review and approve
- **Use a connector** (Concept 6) — e.g., Google Sheets if you connected it
- **Work in tier 1** (scratch drafts) — you might see intermediate calculations
- **Save to tier 2** (platform) — the agent's natural default
- **Try to exit to tier 3** — the download/connector save step

---

### Step 6: Verify the Audit (Concept 5)

When the agent finishes, ask for its final tier report. You should see something like:

```
Files created:
- "draft_packing_list.txt" → tier 1 (scratch, will be deleted)
- "packing_list_v2.md" → tier 2 (saved to my account, survives)
- "beach_trip_packing_list.md" → tier 3 (downloaded to your Downloads folder)
- "budget_estimate.csv" → tier 3 (downloaded to your Downloads folder)
```

**Verify each**:
- [ ] Tier 1 files are intermediate/scratch
- [ ] Tier 2 files are in your account (visible if you log in later)
- [ ] Tier 3 files are actually on YOUR computer (check Downloads)

---

### Step 7: The Vendor-Account-Loss Test (Done Criteria)

Now ask the critical question: **"If my vendor account disappeared tomorrow, which useful context would I lose?"**

Walk through each layer and tier:

| What Would I Lose? | Layer / Tier | Why It's Lost |
|-------------------|--------------|---------------|
| The conversation that produced the list | **Session** | Session history is bound to the account |
| Any cross-session "I prefer short lists" rule | **Memory** | Lives in the vendor's memory store |
| Files saved only to platform | **Tier 2** | They lived in the vendor's storage |
| Intermediate scratch work | **Tier 1** | Already gone after task end |
| My standing instructions | **Instructions** | Bound to the account |
| **What I KEEP** | | |
| Downloaded files on my computer | **Tier 3** | I have them locally |
| A copy of my project notes in a `.md` file | **User-owned file** | I have it on disk |
| Knowledge of how to reproduce the work | **My own understanding** | In my head |

**Key insight**: The only thing that survives vendor-account loss is what reached **Tier 3** or your own portable files.

---

## State Layer Audit (Concept 4)

For every piece of the work, identify the layer:

| Work Item | State Layer | Vendor-Coupled? |
|-----------|-------------|-----------------|
| The conversation thread | Session | YES — lost without account |
| "I like bulleted lists" preference | Memory | YES — lost without account |
| "Always save deliverables to Drive" rule | Instructions | YES — lost without account |
| The final packing list file | Tier 3 (your Downloads) | NO — survives |
| The budget spreadsheet | Tier 3 (your Downloads) | NO — survives |
| Your personal notes about the trip | User-owned context file | NO — survives |

---

## File Tier Audit (Concept 5)

| File | Tier | Exit Method | Custody |
|------|------|-------------|---------|
| `scratch_draft.txt` (intermediate) | 1 | None (auto-deleted) | Vendor (temp) |
| `packing_list_v1.md` (in conversation) | 2 | Saved in account | Vendor (your account) |
| `beach_trip_final.md` (downloaded) | 3 | Manual download | **YOU** |
| `budget.csv` (downloaded) | 3 | Manual download | **YOU** |
| Copy in Google Drive (if connector used) | 3 | Connector save | **YOU** (in your Drive) |

---

## What Useful Context Would Be Lost? (The Done Criteria)

### LOST if vendor account disappears:
- The session conversation and reasoning trail
- Cross-session memory of your preferences
- Standing instructions (e.g., "use metric units")
- Files that exist only in tier 2 (platform storage)
- Project context and history

### SURVIVES vendor account loss:
- Anything in tier 3 (your local files, your Drive, your repo)
- Your user-owned portable context file (e.g., a `CLAUDE.md` or similar)
- The knowledge and habits you built up
- Your understanding of how to re-run the workflow

### The Discipline This Teaches:
- **Always identify the state layer** before starting work
- **Always plan the tier exit** for every deliverable
- **Keep a portable copy** of anything you cannot afford to lose
- **Use tier 3 as the system of record** for finished work

---

## How to Run This Project

### Prerequisites:
- A cloud agent session (browser, desktop, or mobile)
- ~30 minutes of focused time
- A task that produces a real file you can download

### Quick Run Command (mental checklist):
1. Pick a small deliverable (this guide uses a beach trip packing list)
2. Open a fresh session in the cloud agent
3. Decide the state layer (Session / Project / etc.)
4. Brief the agent with tier awareness
5. Watch the work
6. Verify the audit
7. Do the vendor-loss test
8. Document the result

---

## Expected Result

By the end of this 30-minute project, you will have:
- ✅ Produced one real deliverable in tier 3
- ✅ Documented which state layer held each piece of work
- ✅ Identified the file tier of every output
- ✅ Listed what would be lost if the vendor account disappeared
- ✅ Established the habit of "finished work exits the platform"

---

## What We Achieved

1. **Applied Concept 4** — identified state layers (Session vs Project vs Memory vs Instructions)
2. **Applied Concept 5** — categorized every file into tier 1, 2, or 3
3. **Applied Concept 6** — noted which reach path was used (connector / browser / etc.)
4. **Applied Concept 8** — used a clear brief, plan review, and audit
5. **Achieved the done criteria** — final deliverable in tier 3, vendor-loss audit complete

---

## Comparison: Before vs After This Project

| Awareness | Before Project 2 | After Project 2 |
|-----------|-------------------|-----------------|
| Where files end up | "Somewhere in the chat" | Explicit tier 1 / 2 / 3 |
| What persists | "I think it saved" | I know the layer and tier |
| Vendor dependency | "It'll be in my account" | I know what's in MY custody vs theirs |
| Audit habit | None | Every brief ends with a tier report request |
| Exit discipline | "Download if I remember" | "Every deliverable exits the platform" |

---

## Common Pitfalls to Avoid

- **Stopping at tier 2**: A file in your account is NOT the same as a file in your custody. Always push finished work to tier 3.
- **Assuming session = project**: A single chat is fragile. If the work matters, it belongs in a Project.
- **Confusing memory with context**: Memory is for cross-session preferences, not the active conversation.
- **Forgetting the audit step**: Always end the brief with: *"list every file and where it landed"*.
- **No portable copy**: If you cannot afford to lose something, keep a copy outside the vendor.

---

## Files for Project 2

```
C:\Projects\general_agents_web\project_2\
├── README.md                  ← This file
├── experiment-log.md          ← Step-by-step procedure and detailed audit
├── docs\                      ← (empty, ready for future reference)
└── src\                       ← (empty, ready for future code)
```

---

*Project 2 complete. You now understand Concepts 4, 5, 6, and 8 — the state spine, the three file tiers, connectors, and the delegation discipline.*