# LifeOS

A plain-text home for the facts about your life (people, birthdays, preferences, schedules, home, money admin) that your AI agents read before they help you. You update it by talking to your agents; they keep it organized.

**Agents: read [AGENTS.md](AGENTS.md) first.** It has the rules, the sources of truth and where every kind of fact lives.

## Set it up

1. **Make your own private copy.** Your copy will hold personal details, so keep it private. On GitHub, click "Use this template" and choose **Private**, or clone it into a new private repo.
2. **Put your name in.** Find and replace `[Your name]` across the repo with your name. Fill in the other `[bracketed]` placeholders the same way, or delete the lines you don't need.
3. **Delete the example rows.** Every CSV has one made-up row (the "Example" family: Sam, Jordan and Pat) so you can see the format. Delete them once you've added your own, along with the `example` row in [People/sources.csv](People/sources.csv). Rows and table entries marked "Example" in the docs are there to edit or delete too.
4. **Connect your agents.** Point your agents (Claude, ChatGPT and so on) at your repo and tell them to read AGENTS.md. Then start talking: "Add my sister Maya, her birthday is March 3", "I'm allergic to shellfish", "Remind me when swim registration opens."
5. **Fill in your delegation levels.** [Delegation.md](Personal%20Agent%20Instructions/Delegation.md) is how you tell agents what they may do on their own. Until you fill it in, they draft everything for your OK.

## Contents

- [Agent rules](AGENTS.md): start here if you're an agent.
- [Personal Agent Instructions](Personal%20Agent%20Instructions/README.md): how agents should work with you.
- [Preferences](Personal%20Agent%20Instructions/Preferences.md): your rules for calendar, email, food, shopping, travel and school.
- [Goals](Personal%20Agent%20Instructions/Goals.md): what you want agents working toward.
- [Delegation levels](Personal%20Agent%20Instructions/Delegation.md): how far agents may go on their own, task by task.
- [People](People/README.md): family, friends, contacts, birthdays, gifts, kids' schools and activities, doctors and recurring care, as CSV files.
- [Rhythms](Rhythms/README.md): weekly routines and recurring reminders.
- [Home](Home/README.md): home maintenance schedule and repairs log.
- [Household Stocking](Household%20Stocking/README.md): products to reorder and their budgets.
- [Money](Money/README.md): subscriptions, memberships and renewals. No account or card numbers.
- [Important Numbers](Important%20Numbers.md): travel identifiers like loyalty and Known Traveler numbers.
- [Vehicles](Vehicles/Car.md): the car's record, maintenance and recalls.
- [Recipes](Recipes/README.md): recipes in an ingredient-to-step chart format.

## The main ideas

- **One place per fact.** Every fact has one home, and other files link to it. Agents update it once.
- **Context, not permission.** Nothing here lets an agent spend money or message someone without your OK.
- **Blank means unknown.** Agents leave gaps blank instead of guessing.
- **Tasks live elsewhere.** To-dos go in a task tool (this template assumes Linear); lifeos holds the context around them.

## License

[CC0 1.0](LICENSE): public domain. Copy it, change it, share it.
