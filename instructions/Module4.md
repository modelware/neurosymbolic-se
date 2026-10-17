# Module 4: Methodology I: Patterns and Authoring

Modelware · Neurosymbolic Systems Engineering (NSEE)

Complete Lab 4 using the shared Sierra / Fire Force running example. Continue **Capstone Milestone 3** on your own engineering system. Use the [capstone roadmap](CapstoneRoadmap.md) to see which modules contribute to each milestone.

Follow the pacing and review arrangements in the [course guide](CourseGuide.md). Keep reproducible evidence of your work. Email submissions directly to the lecturer, **Dr Maged Elaasar**, at [melaasar@modelware.io](mailto:melaasar@modelware.io).

---

## Setup

### Step 1: Update OML Code and the OML CLI to the latest version

In VS Code, open **Extensions** (`Cmd/Ctrl+Shift+X`), find **OML Code**, and click **Update**
if offered. Then **reload the window** when prompted.

```bash
npm install -g @oml/cli@latest
oml -v
```

### Step 2: Sync your `sierra-method` fork

On **your fork's** GitHub page: click **Sync fork** -> **Update branch**. Then pull it
locally:

```bash
git pull
git status
```

Then **File -> Open Folder...** on the repo and run every command from VS Code's **integrated
terminal**.

---

## Lab 4: Build One Fire Force Authoring Page End to End

Study with running example: Sierra Method + Fire Force system description.

1. Pick one pattern not already covered by a Sierra template
2. Write its focal type, structure, expected content, and rules
3. Implement the shape
4. Put it in a table-editor or tree-editor
5. Add one useful business-rule validation message
6. Add read-only context if the task needs it
7. Wrap the page as a compose template
8. Invoke it and use it to create three real instances
9. Deliberately break one rule, observe the message, and fix it

### Submitting

Push your work to your `sierra-method` fork, then submit a document by email to **Dr Maged Elaasar** at [melaasar@modelware.io](mailto:melaasar@modelware.io) with your **fork URL** and the **commit hash**.

---

## Capstone Milestone 3 (Modules 4-5), Module 4 Component: Turn Your Vocabulary Into a Small Methodology

Narrative should explain rationale, alternatives, uncertainty, and open issues, not restate
the model.

| Deliverable | Minimum |
| --- | --- |
| Description patterns | 4 patterns |
| Description layout | Folders / files + rationale |
| Editors | One per pattern |
| Business rules | >= 2 |
| Notebook | Narrative + live / editor content |
| Compose templates | All editors reusable |
| Dogfooding | >= 10 instances through your editors |
| METHOD.md | What the method prescribes and why |

### Saving Your Module 4 Work

Commit and push this work to your project repository. Continue from it in Module 5; the
cumulative Capstone Milestone 3 submission is ready after the Module 5 analysis layer is complete.
