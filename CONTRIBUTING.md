# GTNH Contribution Guidelines

These guidelines explain how to contribute to GTNH, what is expected in pull requests, and how content, balance, and reviews should be handled.

Before contributing, please read and follow the project [Code of Conduct](https://github.com/GTNewHorizons/.github/blob/main/CODE_OF_CONDUCT.md) and [AI Usage Policy](https://github.com/GTNewHorizons/GTNH-Dev-Doc/blob/master/AI_POLICY.md). The AI policy applies to code, written content, issues, discussions, pull requests, and media.

## 1. General Contribution Expectations

### Know the Area You Are Changing

- Avoid changing areas of the pack you have never personally reached as a player.
- If you have not reached that area, get feedback from developers or players who are experienced with it.
- This is especially important for balance, progression, and late-game systems.

---

### Discuss Major New Content First

- Do not open PRs with major new content unless the idea has been discussed with the team first.
- The team should understand the intended design before implementation.
- Avoid changes where only the PR author fully understands what is being added.
- Significant content should not be discovered by the rest of the team only after it ships.

---

### Respect the Vision

- Respect the GTNH vision.
- If an idea is not covered by the vision document:
  - Discuss it with developers in `mod-dev`, `#meta-dev`, or `github-discussion`.
  - If there is agreement, the vision document can be updated.
  - Then implementation can proceed.

---

### New Content Below IV

- Avoid adding new content below IV tier.
- The game is already dense, especially with chemical lines.
- Bug fixes and quality-of-life changes are always appreciated.
- If you have a strong reason to add new content below IV:
  - Discuss it with developers in `mod-dev`, `#meta-dev`, or `github-discussion` first.
  - Wait for general consensus before starting serious work.
  - Do not spend major development time on something likely to be rejected.

---

### Be Open to Criticism

- Feedback, revision, and rejection are normal parts of development.
- Content you are proud of may not be accepted in its current form.
- Criticism of a change is not criticism of the person who made it.

---

## 2. Pull Request Requirements

### PR Descriptions

Pull requests that add features, change features, or affect balance should clearly explain:

- What the PR changes.
- Why the change is being made.
- What area of the pack it affects.
- Any context reviewers need to understand the change.
- Any Discord discussion or prior agreement relevant to the PR.

The more precise the description, the easier the PR is to review.

---

### PR Titles and Changelog Context

- PR titles should be written as if they may appear in a changelog.
- Context is important because changelog entries may be generated from PR titles.

---

### Screenshots, Videos, and Examples

- Screenshots and videos are strongly encouraged when they help explain the change.
- Screenshots and videos may also be useful for changelogs or `#upcoming-features`.

---

### Commits

- Prefer multiple clear, focused commits over one large commit.
- Commit names should reflect the changes they contain.

---

### PR Template Requirement

- The PR template must be properly filled out.
- If there are any details that need to be included such as other PRs required for merge or to what degree AI was used in the PR please mention it under the respective bullet point.

---

### Recipe Chains Require Flowcharts

- Any PR that adds a new recipe chain must include a flowchart.
- Recipe-chain PRs without a flowchart may be rejected regardless of quality.
- If you do not know how to make one, try [draw.io](https://draw.io).

---

## 3. Special Rules for Balance Changes

Balance-affecting PRs must follow the GTNH vision.

### Label Requirement

- Use the `Affects Balance` label when appropriate.
- Do not mix balance changes with unrelated changes in the same PR.

---

### Approval Requirement

- At least two approvals are required.
- One approval must be from a member of the admin team.

---

### Required Balance PR Questions

When a PR is tagged as balance-affecting, the author must answer the following questions:

1. What goal is this change trying to achieve? What tier is it targeting?
2. What side effects does this have on other lines or systems? How does it change the game meta?
3. If relevant, do you have metrics, a spreadsheet, or a visualization explaining the change? If it is a new multiblock, can you provide a picture and/or practical setup?
4. Is this change being made in expectation of, or in tandem with, another unwritten or unmerged change coming later?

Notes:

- These questions help clarify the author’s reasoning.
- They make discussion easier.
- They preserve context that may otherwise be lost in Discord.
- Authors do not need perfect answers to every question, but an attempt should be made.
- A balance PR that does not answer these questions may be rejected regardless of quality.

---

## 4. Content and Design Standards

### General Content Expectations

When adding or changing pack content:

- Respect the identity of the mod or system being changed.
- Consider how the change affects progression, balance, lore, and player experience.
- Avoid forcing consistency where inconsistency is intentional or part of the design identity.
- Ask for feedback when unsure.

---

### Language Standards in Pack Content and Code

Profanity and insults are not acceptable in the pack.

This applies to:

- Quest text
- Tooltips
- In-game content
- Code
- Comments
- Other user-facing or contributor-facing text

Rules:

- Do not use swearwords, even partially or fully censored.
- If something is meant to be funny or witty, find another way to write it.
- Do not insult the player or a group of players.
- Light teasing may be acceptable only if you can be completely sure it will be understood as a joke.
- If you edit existing content or code and find something that violates this standard, remove or replace it.
- If you are unsure about a phrase, ask others for feedback.

---

### Texture and GUI Guidelines

#### New Textures

- New textures should generally remain consistent with the mod or mod group they are being added to.
- Ideally, new textures should be run past an admin before being merged.

#### Magic Textures

- Magic is meant to feel, look, and play differently from GregTech.
- Do not update magic GUIs purely for consistency with GregTech if it damages the distinct feel of magic content.
- Magic content should preserve its own artistic and mechanical identity.

#### Tooltips

- Tooltip reduction is fine when needed.
- If a mod or system has a specific tooltip style or consistency, try to preserve it.

#### Inventory Color Changes

GUIs that shift the color of the player’s inventory are allowed if the usage is consistent.

Examples include:

- GT Steam Machines
- Magic Bees’ Magic Apiary
- Railcraft’s Coke Oven

---

### Magic Design Guidelines

Magic in GTNH is intended to have a strong and distinct look, feel, and execution compared to the technology-focused parts of the pack.

When designing or balancing magic content:

- Respect the artistic identity of each magic mod.
- Respect the mechanical identity of each magic mod.
- Consider lore, theme, and progression.
- Avoid forcing magic content to behave like tech content unless there is a strong design reason.

---

## 5. Reviewing Pull Requests

These are general review guidelines. They do not need to be followed mechanically in every case, but they describe the expected review approach.

### Review Within Your Knowledge

- Avoid approving balance-affecting PRs if you are not familiar with the implications of the proposed changes.
- This is especially important for balance changes, because they can negatively affect the wider community if reviewed incorrectly.
- You may still ask questions or point out possible issues, even if you are not comfortable approving the PR.

---

### Know Your Limits and Expand Them

- Everyone has limits to what they know.
- There is no limit to what they can learn.
- If a PR is in an unfamiliar area:
  - Read it.
  - Ask questions.
  - Identify possible issues.
  - Point out inconsistencies or “code smells.”
- Do not approve a PR unless you understand the change well enough to be confident in the approval.
- As you become familiar with more systems, gradually increase the complexity of the PRs you review.

---

### Ask When Something Is Unclear

- If code or logic is only understood by the author, ask them to clarify it.
- Clarification can happen in:
  - A PR comment
  - The PR description
  - Documentation
  - Code comments
- This prevents knowledge gaps and helps future maintainers.
- If a concept is difficult to explain even after discussion, the author should consider documenting it directly in the code.

---

### Read the PR Description

- The PR description gives reviewers a quick overview of the change.
- If the description is empty or unclear, ask the author to complete it.
- A good description helps reviewers:
  - Understand the scope.
  - Decide whether they are the right person to review it.
  - Understand the intended purpose of the change.

---

### Contribute Positively

Review comments should be constructive, actionable, and respectful.

Remember:

- Behind every PR is a person who spent time and effort making a contribution.
- Rude or dismissive reviews can discourage future contribution.
- Highlight what is done well, not only what needs improvement.
- If something is unclear, frame the concern as a genuine question rather than an implied criticism.
- A community thrives when contributors feel valued and respected.

---

## 6. Developer Breaks and Hiatus

Life events may require developers to temporarily step back from GTNH.

- If you expect to take a break, consider setting your status to inactive. This helps others know not to approach you for GTNH-related work.
- Inactive status is not a demotion, you can request to be reactivated after your break.
- After a month of inactivity, defined as no code contributions or PR reviewing, a developer may be marked as on hiatus.
