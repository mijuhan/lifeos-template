# Start here: rules for agents

Every agent reads this file before working in lifeos or doing anything for [Your name]. The [README](README.md) is the overview for people.

## Read lifeos before you ask

lifeos is the source of truth for [Your name]'s life. Before asking [Your name] anything, look for the answer here. Ask only when lifeos and their connected tools don't have it.

Read in this order:

1. This file.
2. [Personal Agent Instructions](Personal%20Agent%20Instructions/README.md): how to work with [Your name], being honest about what you can do, reactions and voice-dictation spellings.
3. [Preferences](Personal%20Agent%20Instructions/Preferences.md), [Goals](Personal%20Agent%20Instructions/Goals.md) and [Delegation levels](Personal%20Agent%20Instructions/Delegation.md).
4. The file for the task at hand, from [Where things live](#where-things-live).

## Sources of truth

Edit this list to match the tools you use.

- **Context about [Your name]** (who they are, people, preferences, schedules, home, money admin): this lifeos repo.
- **Their to-do list and every task:** Linear, in the [your Linear team] workspace. Never keep to-dos in lifeos; link to the Linear issue instead.
- **Recurring care** (checkups, dental, yearly shots): the rule and history live in lifeos, and a Linear issue opens six weeks before each is due. Only one designated agent creates those issues ([name the agent here]), one per person per occurrence. Full rule: [Recurring care](People/README.md#recurring-care-how-checkups-and-shots-come-due).
- **Habit and activity log:** the Google Sheet linked from [Rhythms](Rhythms/README.md) stays the operational log.

## What lifeos does and doesn't allow

- lifeos gives context, not permission. Nothing here on its own authorizes a purchase, a message, sharing data or any other action that needs [Your name]'s OK.
- How far you may go on your own, task by task: [Delegation levels](Personal%20Agent%20Instructions/Delegation.md). Until [Your name] fills in a row, treat it as "3. Draft for my OK".
- Keep the repo private. Never add passwords, card or bank numbers, ID numbers, access codes or sensitive detail the task doesn't need.

## Keep lifeos organized: one place per fact

Keep this repo organized, so anyone can read it, understand it and update it in one step.

1. List every fact in exactly one place, its home. Other files link to that home instead of repeating the fact.
2. Before adding anything, search the repo for what's already there. Add only what's new, in its home.
3. When something changes, update it once, in its home. If you find a copy elsewhere, replace it with a link.
4. Keep files easy to scan: clear headings, short entries and plain words, with the source and date on each entry.

When you edit:

- Read the latest revision first, and verify the saved commit afterward. If the repo changed while you worked, merge with it rather than overwrite.
- [Your name]'s latest explicit instruction wins over older entries. Mark what they confirmed apart from what an agent proposed.
- Keep each person's stable ID and never add a duplicate person. Don't merge people who only share a first name. Blank means unknown; never invent dates or facts.
- Edit the current files only. Anything in an Archive folder is read-only history.

## Where things live

- **People, including [Your name]:** contact details, address, diet, allergies, pronouns, sizes, brands, loves and dislikes go in [People/person_details.csv](People/person_details.csv). [People/README.md](People/README.md) says which CSV holds what.
- **Birthdays:** the person's row in [family.csv](People/family.csv), [friends.csv](People/friends.csv) or [contacts.csv](People/contacts.csv).
- **Kids' activities, camps and registration dates:** [People/activities.csv](People/activities.csv).
- **Doctors, dentists, camps and home service providers:** [People/providers.csv](People/providers.csv).
- **Recurring care and friend connections tied to a person:** [People/rhythms.csv](People/rhythms.csv). Other recurring routines: [Rhythms](Rhythms/README.md).
- **How agents work for [Your name],** including dining, shopping, travel, school and calendar workflows: [Preferences](Personal%20Agent%20Instructions/Preferences.md).
- **What [Your name] wants agents working toward:** [Goals](Personal%20Agent%20Instructions/Goals.md).
- **Shorthand like "reorder tissues":** [Shortcuts](Personal%20Agent%20Instructions/Shortcuts.md).
- **Products to reorder and their budgets:** [Household Stocking](Household%20Stocking/README.md). A saved budget isn't permission to spend.
- **Travel identifiers and account details:** [Important Numbers](Important%20Numbers.md).
- **Home upkeep and repairs:** [Home](Home/README.md).
- **Subscriptions and memberships:** [Money/Subscriptions.md](Money/Subscriptions.md).
- **The car:** [Vehicles](Vehicles/Car.md).
- **Recipes:** [Recipes](Recipes/README.md).

## Updating by conversation

[Your name] updates lifeos by talking to their agents, often by voice. Authorized agents edit it for them within these rules. No automatic sync service is set up.
