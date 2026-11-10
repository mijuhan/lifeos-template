# People

Everyone in [Your name]'s life, as CSV files. Each file has one made-up example row (the "Example" family) to show the format; delete those once you add your own. Your own row uses the person_id `me`.

| File | One row / purpose |
| --- | --- |
| family.csv | One family member, including deceased relatives |
| friends.csv | One friend; is_close_friend is true/false |
| contacts.csv | One other contact whose friend/family status isn't set |
| person_details.csv | One contact detail, preference, dietary restriction, allergy, nickname or story. Sizes and likes go here too, one row each, with categories like clothing_size, shoe_size, brands, loves and dislikes |
| gift_preferences.csv | One standing non-birthday occasion policy; birthday policy lives in birthday_gift |
| gifts.csv | One item for one recipient and occasion, from wanted through given |
| rhythms.csv | One recurring intention tied to a person or school: friend connections (domain relationships) and checkups, dental and shots (domain care) |
| care_events.csv | One past or booked care event |
| activities.csv | One activity, class, lesson, camp or team for one person, including when registration opens |
| providers.csv | One business that serves the family or home: doctor, dentist, camp, plumber, HVAC and so on |
| schools.csv | One school |
| enrollments.csv | One child/school/year enrollment |
| terms.csv | One member of a named group or term you use (e.g. "my kids' other parent", "my kids") |
| sources.csv | One source description, referenced by source_ref |
| review_needed.csv | One unresolved question |

## Rules

- Use stable IDs (like `sam-example`) across all files, and exactly one core row per person in family, friends or contacts. Never change an existing ID.
- Blank fields are unknown, not false. Birthday and gift flags use true/false/unknown.
- Don't silently label unclassified contacts as friends. Don't infer parentage, diagnoses, dates, purchases or delivery.
- Keep allergies separate from dietary preferences.
- CSV format: UTF-8, standard quoting, ISO dates (YYYY-MM-DD), IDs and partial birthdays as strings. No JSON inside cells.
- Keep credentials and sensitive identifiers out.

## Close friends

Every close friend needs birthday_reminder=true, a known birthday or an open review_needed item for the missing one, and a connection rhythm in rhythms.csv once the cadence is known (for example "one-on-one hang, once a quarter"). If the cadence is unknown, add the rhythm with enabled=false and an open review item rather than inventing a schedule.

## Rhythms

- **cadence_type:** calendar_period means at least target_count completions in each calendar month, quarter or year. annual_date uses an MM-DD anchor_date. rolling measures time since the last completion, with the interval in period (e.g. "6 months", "year").
- **mode:** nudge, track or appreciate.
- **enabled** is intent; **automation_status** (not_configured, not_verified, active) and automation_ref describe what's actually set up.
- **done_when** is a check an agent can verify to close a rhythm instead of nudging again.
- next_due_on stays blank until the schedule or last completion is known.
- Timezone: [your timezone, e.g. America/Los_Angeles].

## Recurring care: how checkups and shots come due

1. **lifeos holds the rule and the history.** Each recurring visit or shot is one row in [rhythms.csv](rhythms.csv): who, what, how often, which office ([providers.csv](providers.csv)) and next_due_on. Every past and booked visit is one row in [care_events.csv](care_events.csv). To-dos never live here.
2. **Linear holds the to-do.** Six weeks before a rhythm's next_due_on, one Linear issue opens in [your Linear team], due on next_due_on, so there's time to book.
3. **One issue per person per occurrence.** Title it with the person and the visit, e.g. "Sam: yearly checkup". Before creating one, search Linear for an open issue for the same person and visit. If one exists, use it.
4. **Only one agent creates these issues:** [name the agent and routine]. Any other agent that notices something coming due tells [Your name] or that agent instead.
5. **A booked visit counts.** If a visit is already on the calendar on or before next_due_on, no issue is needed. Log it in care_events.csv as scheduled.
6. **After each visit,** log it in care_events.csv and set next_due_on from it: last visit plus the period for rolling rhythms, or the next MM-DD anchor for annual ones. If the next visit is already booked, next_due_on is that date. Close the Linear issue once the visit is booked.

Only enabled rows open issues. care_events.csv status values: scheduled; completed_calendar (on the calendar, attendance not confirmed); completed_email (confirmed by the office's email); completed_user_reported. Logistics only: no clinical details.

## Activities

registration_opens_on drives sign-up alerts. Suggested alert timing: 7 days before, 1 day before and the morning registration opens.

## What each file owns

Core person CSVs own names, birthdays and birthday flags. person_details.csv owns repeatable practical facts. gifts.csv owns wishlist and purchase state. schools.csv owns school-wide facts; enrollments.csv owns one child's school year. providers.csv lists each business once; activities, rhythms and [Home](../Home/README.md) link to it by provider_id.
