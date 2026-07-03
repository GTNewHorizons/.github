# GTNH Contribution Guidelines

These guidelines explain how to contribute to GTNH, what is expected in pull requests, and how content, balance, and reviews should be handled.

For behavior expectations, see the project Code of Conduct.

## Pull Request Descriptions

Pull requests that add features, change features, or affect balance should clearly explain:

- What the PR changes.
- Why the change is being made.
- What area of the pack it affects.
- Any context reviewers need to understand the change.
- Any Discord discussion or prior agreement relevant to the PR.

The more precise the description, the easier the PR is to review.

Additional expectations:

- Screenshots and videos are strongly encouraged when they help explain the change.
- Screenshots/videos may also be useful for changelogs or `#upcoming-features`.
- PR titles should be written as if they may appear in a changelog.
- Prefer multiple clear, focused commits over one large commit.
- Commit names should reflect the changes they contain.

## Content Creation Guidelines

### Know the Area You Are Changing

- Avoid changing areas of the pack you have never personally reached as a player.
- If you have not reached that area, get feedback from developers or players who are experienced with it.
- This is especially important for balance, progression, and late-game systems.

### New Content Below IV

- Avoid adding new content below IV tier.
- The game is already dense, especially with chemical lines.
- Bug fixes and quality-of-life changes are always appreciated.
- If you have a strong reason to add new content below IV:
  - Discuss it in `#meta-dev` first.
  - Wait for general consensus before starting serious work.
  - Do not spend major development time on something likely to be rejected.

### Discuss New Content First

- Do not open PRs with major new content unless the idea has been discussed with the team first.
- The team should understand the intended design before implementation.
- Avoid changes where only the PR author fully understands what is being added.
- Significant content should not be discovered by the rest of the team only after it ships.

### Respect the Vision

- Respect the GTNH vision.
- If an idea is not covered by the vision document:
  - Discuss it in `#meta-dev`.
  - If there is agreement, the vision document can be updated.
  - Then implementation can proceed.

### Be Open to Criticism

- Feedback, revision, and rejection are normal parts of development.
- Content you are proud of may not be accepted in its current form.
- Criticism of a change is not criticism of the person who made it.

### Recipe Chains Require Flowcharts

- Any PR that adds a new recipe chain must include a flowchart.
- Recipe-chain PRs without a flowchart may be rejected regardless of quality.
- If you do not know how to make one, try [draw.io](https://draw.io).

## Texture and GUI Guidelines

### New Textures

- New textures should generally remain consistent with the mod or mod group they are being added to. Ideally they should all be ran past an admin before being merged.

### Magic Textures

- Magic is meant to feel, look, and play differently from GregTech.
- Do not update magic GUIs purely for consistency with GregTech if it damages the distinct feel of magic content.
- Magic content should preserve its own artistic and mechanical identity.

### Tooltips

- Tooltip reduction is fine when needed.
- If a mod or system has a specific tooltip style or consistency, try to preserve it.

### Inventory Color Changes

GUIs that shift the color of the player’s inventory are allowed if the usage is consistent.

Examples include:

- GT Steam Machines
- Magic Bees’ Magic Apiary
- Railcraft’s Coke Oven

## Magic Design Guidelines

Magic in GTNH is intended to have a strong and distinct look, feel, and execution compared to the technology-focused parts of the pack.

When designing or balancing magic content:

- Respect the artistic identity of each magic mod.
- Respect the mechanical identity of each magic mod.
- Consider lore, theme, and progression.
- Avoid forcing magic content to behave like tech content unless there is a strong design reason.

### Thaumcraft

Thaumcraft is a lore mod. While it is a magic mod, it is also trying to tell a distinct story with specific limitations and paths.

When working on Thaumcraft content:

- Take Thaumcraft lore seriously.
- Do not freely violate Thaumcraft’s internal logic.
- Essentia types should not be allowed to mix freely if doing so would violate canon.
- A single jar should not store multiple essentia types.
- A reservoir may be acceptable depending on implementation and lore.
- Lore can be used creatively, such as for mechanisms that intentionally keep essentia separate until reaction.
- Thaumcraft lives and dies on the quality of its lore.
- Some data is acceptable, but hard numbers are generally better suited for the questbook than the Thaumonomicon.
- Lore entries should be written seriously.
- Joke entries are allowed for isolated items or chains.
- Do not create an entire research tab for trivial jokes.
- Intentionally misleading data is forbidden.
- Do not include joke text suggesting extreme warp values in a research entry that actually contains warp.
- Do not add content directly to vanilla Thaumcraft tabs.
  - This is a direct request from Azanor in the Thaumcraft addon terms.
  - It can also cause issues with unlocking Kami.

### Witchery

- Do not add new Witchery content directly to Witchery.
- If you want to add Witchery-related content, add it to Forbidden Magic instead.
- Witchery exists as a singular ARR island compared to the broader addon ecosystems around other magic mods.
- If you want to see new Witchery content, consider helping recreate vital portions in new, untethered code.

## Language Standards in Pack Content and Code

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

## Balance-Affecting Pull Requests

Balance-affecting PRs must follow the GTNH vision.

Rules for balance PRs:

- Use the `Affects Balance` label when appropriate.
- Do not mix balance changes with unrelated changes in the same PR.
- For IV and below, follow the new-content guidelines above.
- For LuV and above:
  - At least two approvals are required.
  - One approval must be from a member of the GitHub admin team.
  - Admin team: https://github.com/orgs/GTNewHorizons/teams/admin

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
- The requirement may be bypassed in reasonable scenarios, such as emergency reverts.

## Reviewing Pull Requests

These are general review guidelines. They do not need to be followed mechanically in every case, but they describe the expected review approach.

### Review Within Your Knowledge

- Avoid approving balance-affecting PRs if you are not familiar with the implications of the proposed changes.
- This is especially important for balance changes, because they can negatively affect the wider community if reviewed incorrectly.
- You may still ask questions or point out possible issues, even if you are not comfortable approving the PR.

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

### Ask When Something Is Unclear

- If code or logic is only understood by the author, ask them to clarify it.
- Clarification can happen in:
  - A PR comment
  - The PR description
  - Documentation
  - Code comments
- This prevents knowledge gaps and helps future maintainers.
- If a concept is difficult to explain even after discussion, the author should consider documenting it directly in the code.

### Read the PR Description

- The PR description gives reviewers a quick overview of the change.
- If the description is empty or unclear, ask the author to complete it.
- A good description helps reviewers:
  - Understand the scope.
  - Decide whether they are the right person to review it.
  - Understand the intended purpose of the change.

### Contribute Positively

Review comments should be constructive, actionable, and respectful.

Remember:

- Behind every PR is a person who spent time and effort making a contribution.
- Rude or dismissive reviews can discourage future contribution.
- Highlight what is done well, not only what needs improvement.
- If something is unclear, frame the concern as a genuine question rather than an implied criticism.
- A community thrives when contributors feel valued and respected.

## Developer Breaks and Hiatus

Understanding the active developer count helps the team redistribute tasks more efficiently.

Guidelines:

- Life events may require developers to temporarily step back from GTNH.
- If you expect to take a break, consider setting your status to inactive.
- This helps others know not to approach you for GTNH-related work.
- Inactive status is not a demotion.
- You can request to be reactivated after your break.
- Sometimes breaks happen unexpectedly.
- After a month of inactivity, defined as no code contributions or PR reviewing, a developer may be marked as on hiatus.
