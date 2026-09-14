# Minerva Reading Guide

This repository is intentionally public-safe. The internal AI tool may read these files, but confidential operational data must remain inside the approved internal environment.

## Recommended direct URLs

Use direct file URLs or raw-text URLs rather than the repository top page.

- Initiatives: https://raw.githubusercontent.com/Nobu0219/Nia/main/INITIATIVES.md
- Active tasks: https://raw.githubusercontent.com/Nobu0219/Nia/main/TASKS.md
- Operating model: https://raw.githubusercontent.com/Nobu0219/Nia/main/OPERATING_MODEL.md
- This guide: https://raw.githubusercontent.com/Nobu0219/Nia/main/MINERVA_GUIDE.md

## Daily priority prompt

```text
Read TASKS.md and OPERATING_MODEL.md.
Select up to three actions for today, prioritizing P0 before P1 and P2.
For each action, show:
1. purpose,
2. first observable action,
3. information needed from the internal environment,
4. completion condition.
Do not invent names, dates, confidential figures, or internal facts not contained in the supplied internal data.
Do not add a new task if an existing task already covers the same work.
```

## Weekly review prompt

```text
Read INITIATIVES.md, TASKS.md, and OPERATING_MODEL.md.
Using the internal progress information I provide, produce:
- material changes this week,
- open P0 risks,
- one controllable operational bottleneck,
- overdue or stale tasks,
- work that can be delegated,
- tasks that should be closed.
Keep GitHub task codes unchanged.
Separate confirmed facts, interpretation, and proposed action.
```

## Operational data-analysis prompt

```text
Use OPERATING_MODEL.md as the definition source.
Analyze ordinary weekdays as the main comparison set; handle weekends and holidays separately.
Keep service wait time and internal processing time separate.
Treat off-site activity records as overlap attached to the same employee, not as additional people.
For every conclusion, state:
- metric definition,
- denominator,
- inclusion/exclusion rule,
- missing-data concern,
- operational mechanism,
- safest testable next action.
Do not output personal or patient-identifiable information.
```

## Meeting preparation prompt

```text
Read INITIATIVES.md and TASKS.md.
Prepare a short decision-focused agenda containing:
- decision required,
- confirmed background,
- options with risks,
- recommended direction,
- owner role,
- next observable action,
- completion check.
Use role descriptions and task codes only; do not infer personal names or confidential context.
```

## Safe update prompt

```text
Draft a proposed update to TASKS.md.
Keep only public-safe, role-level, abstract information.
Exclude names, organizations, facilities, patients, exact internal figures, system names, private URLs, credentials, and exact personnel schedules.
Each task must contain one observable action and one completion condition.
Do not mark anything complete unless internal evidence confirms completion.
Return the proposed Markdown for human review; do not publish automatically.
```

## Important boundary

The public repository provides reusable logic, definitions, and task codes. Internal facts should be supplied to the internal AI only through approved internal sources. Never paste confidential internal output back into this public repository without removing identifying and confidential details.
