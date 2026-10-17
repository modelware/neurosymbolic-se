# Module 1: Foundations

Modelware · Neurosymbolic Systems Engineering (NSEE)

Complete Lab 1 using the shared Sierra / Fire Force running example. Continue **Capstone Milestone 1** on your own engineering system. Use the [capstone roadmap](CapstoneRoadmap.md) to see which modules contribute to each milestone.

Follow the pacing and review arrangements in the [course guide](CourseGuide.md). Keep reproducible evidence of your work. Email submissions directly to the lecturer, **Dr Maged Elaasar**, at [melaasar@modelware.io](mailto:melaasar@modelware.io).

---

## 1. The Toolchain

- **OML Code** - VS Code extension; the IDE for the OML language.
- **OML CLI** - command line: lint / validate / reason / render.
- **An AI coding assistant** - the generative half of the neurosymbolic workflow.
- **`sierra-method`** - the running example we grow across the course (the Fireforce project:
  a method, a vocabulary, and a system description in OML).

---

## 2. Setup

### Step 0: Confirm access to OML Code

Use the GitHub account associated with your Modelware NSEE course access. Confirm that your
account can use OML Code before attempting the extension and CLI logins.

If access has not been arranged, contact your Modelware NSEE course contact or
[Modelware](https://www.modelware.io/contact). Do not post account credentials or access
tokens in this repository. Keep the same GitHub account throughout the exercises.

### Step 1: Install VS Code

https://code.visualstudio.com/download

### Step 2: Install the OML Code extension

In VS Code, open **Extensions** (`Cmd/Ctrl+Shift+X`), search **`OML Code`** (first result),
click **Install**, and leave auto-update on. Details and demos:
https://www.modelware.io/oml-code

### Step 3: Install Node.js

The CLI needs **v22.18.0 or later**. Check with `node --version`; if missing or older, install
from https://nodejs.org/ and re-check. A wrong Node version is the most common cause of a
failed CLI install.

### Step 4: Install the OML CLI

```bash
npm install -g @oml/cli
oml --version
```

A few warnings are normal - look for a success message. If it fails, re-check Step 3.

### Step 5: Clone the running example

```bash
git clone https://github.com/modelware/sierra-method.git
```

Need git? https://git-scm.com/downloads. Never cloned before?
https://docs.github.com/en/repositories/creating-and-managing-repositories/cloning-a-repository

Then **File → Open Folder…** in VS Code and select the cloned folder.

### Step 6: Prepare an AI coding assistant

Use an AI coding assistant available in your environment. For Module 6, it must support
MCP tool connections. Confirm its account access and usage limits before the lab.

### Step 7: Log in to OML Code

**Extension.** Opening `sierra-method` prompts you to sign in: click **Log in** → **Allow**
→ **Continue as `<username>`**, copy the code shown in VS Code, paste it into the browser,
and **Authorize**.

**CLI.** From inside the repo:

```bash
oml login
```

Open the printed URL, authenticate, paste the code, authorize.

> Confirm the account access described in Step 0 before either login.

---

## 3. Smoke Tests

Run all of these - they are also your Lab 1 screenshots.

**3.1 Browse the model.** Open the repo's `README` - OML Code renders it as a rich view.
Click **Start** (Fireforce is the project), then **Browse → sierra-method →** the steps of
the method, then the **first step**. A rendered table means the extension works.

**3.2 Vocabulary diagram.** In `src/method.oml` → **sierra-method**, pick an ontology (e.g.
the mission vocabulary) → **right-click → Open Diagram**. Double-click elements to jump to
the model.

**3.3 Description diagram.** In the model OML sources → **context analysis** →
**objectives** → **right-click → Show Diagram**. You should see the mission objectives and
the concerns they relate to.

**3.4 Run the CLI.** From the repo root, all four should succeed:

```bash
oml lint      # style / well-formedness
oml validate  # model against the methodology constraints
oml reason    # DL reasoner - confirm no inconsistencies
oml render    # generates web views into build/web
```

Then open `build/web` in Finder/Explorer and double-click the entry point - the same views,
now as a static site.

**3.5 Ask the AI a question.** Open your AI **Chat** (or whatever it's called for your AI agent) panel
in VS Code, click **`+`**, and ask something answerable from the model, e.g. *"What are the stakeholders in
the model?"* Then **check the answer against the model** - the README lists the stakeholders
directly. That habit is the point: the LLM drafts, you (and formal tools) verify.

---

## Lab 1: Tool Setup

**Complete before Module 2. Completion checklist.**

- [ ] Confirm OML Code access for the GitHub account you will use
- [ ] Get access to an AI coding assistant
- [ ] Install VS Code and the OML Code extension
- [ ] Install Node.js (v22.18.0+) and the OML CLI
- [ ] Clone the running example and open it in VS Code
- [ ] Log in to OML Code - extension and CLI
- [ ] Run `oml lint`, `validate`, `reason` (no inconsistencies), `render`
- [ ] Open the rendered web views
- [ ] Open both diagrams (a vocabulary and a description)
- [ ] Ask the AI chat a question about the model
- [ ] **Screenshot every step**

**Submit:** email a single **ZIP** of your screenshots, one per step, to **Dr Maged Elaasar** at [melaasar@modelware.io](mailto:melaasar@modelware.io).

Module 2 assumes a working environment - **you write OML in the first ten minutes.** Setup
problems are environment-specific and take a day, not an hour. Use the support channel specified by the Modelware NSEE course. Include tool versions,
the command that failed, and a redacted error log.

---

## Capstone Milestone 1 (Module 1): Project Scope & Problem Statement

**1-2 pages. Complete before Module 2.** Propose your project: the domain and the system you want
to model. Five sections:

| # | Section | What to establish |
| --- | --- | --- |
| 1 | **The system** | What it is, its boundary, and explicitly what is *outside* it |
| 2 | **Stakeholders** | Who cares, and what each needs to know |
| 3 | **The questions** | 3-5 specific questions your model should answer |
| 4 | **Why it is hard** | Where knowledge is fragmented, ambiguous, or tacit today |
| 5 | **Available data** | Documents, spreadsheets, or models you will draw on |

**Give particular attention to Section 3.** Write questions in plain English as *"I am
modeling this system so that I can analyze X / derive insight Y,"* and name the stakeholder
each one is for.

| Weak | Strong |
| --- | --- |
| "What are the components?" | "Which components are affected if the payload interface changes?" |
| "How does it work?" | "Is every safety requirement traced to a verification activity?" |
| "What is the architecture?" | "Which subsystems exceed their mass budget allocation?" |

Strong questions are specific, cross-cutting, and currently hard to answer. They become your
model's acceptance criteria.

**Choose a domain you know and scope it tightly.** Build on this proposal throughout the
course. Labs practice the shared example; the capstone applies the techniques to your own
system. A focused model that answers the agreed engineering questions is the target.
Review the proposal yourself or with your course reviewer before building on it.

---

## Further Reading

Use these references as needed while working through the modules.

| Ref | Source | Why |
| --- | --- | --- |
| REF01 | [OML Language Specification](https://opencaesar.io/oml/) | The manual for OML syntax and semantics - a reference, not a read-through |
| REF02 | [OML Tutorials](https://opencaesar.io/oml-tutorials/) | **Do tutorials 1 and 2** for a flavor of OML (see note) |
| REF03 | [OML overview paper (ISWC 2026)](https://www.modelware.io/assets/papers/iswc-2026-oml-semantic-web-mbse.pdf) | Rationale and design decisions behind OML |
| REF04 | [OML Code](https://www.modelware.io/oml-code) | Home of the tool we use - feature pages and demos |
| REF05 | [openCAESAR](https://opencaesar.io/) | The open source counterpart: papers, blogs, recorded talks |

> **On REF02:** the tutorials target the openCAESAR open source tooling, not OML Code. The
> concepts transfer and nearly everything there works in OML Code, which is what we use for
> the rest of the course.

---

**Next: Module 2 - Representation I: The Basics of OML.** We stop talking about ontologies and
start writing one.
