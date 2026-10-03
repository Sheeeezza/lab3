#  AI-Assisted Planning (Campus Event Management System)


## Description
Planning phase of a Campus Event Management System (students browse
events, register and get reminders; admins add and remove events). An AI
assistant drafted the plan, and every part was then checked, corrected
and prioritised by hand.

## How to Run
```
python "Lab 3 Sheeza rasheed(SP24-BSE-43).py"
```
Expected output:
- the work-breakdown tree (5 modules with their tasks)
- `All WBS rows trace to the brief or are marked ADDED.`
- label counts: `Must 6`, `Should 4`, `Could 1`, `Won't 1`

## What I Did
1. **Module breakdown:** the AI gave 5 modules (Auth & Accounts, Event
   Catalogue, Registration, Reminders, Admin Console). It missed
   session-token handling and cancelling a registration, both added by hand.
2. **Tree view:** printing the plan as a tree made gaps visible that a
   flat list hides.
3. **User stories and MoSCoW:** tasks rewritten as "As a <role>, I want
   <goal> so that <benefit>" and each labelled Must/Should/Could/Won't
   with a justification.
4. **"What did you miss?" check:** found that no story covered an event
   being cancelled after students registered. Added as S11.

## Traceability (Task 1)
Every WBS row either traces to a phrase in the brief or is marked
`ADDED:` with a reason. `check_traceability()` verifies this with an
assert.
- Invented task by the model: `<paste exact task from your model's output>`
- Tasks the brief needed but the model left out:
  1. Session-token handling (Auth)
  2. Cancel registration (Registration)

## Backlog (Task 2)
13 user stories (S1 to S13). Result: 6 Must, 5 Should, 1 Could, 1 Won't
after S13 is added. Not everything is Must, so prioritisation is real.

Three Must labels defended:
- **S5 (cancel registration)** is Must, S7 (search) is Should: without
  cancelling, the seat count drifts from reality, while search only makes
  browsing slower.
- **S4 (register)** is Must, S6 (reminder) is Should: reminders only
  make sense after registration exists.
- **S8 (add event)** is Must, S9 (remove event) is Should: with no events
  there is nothing to browse or register for.

## Local Context Gap (Task 3)
`<replace with your real campus/device/network requirement>`
Current entry: S13, a text-only event list for slow campus Wi-Fi.

## Prompt Ledger (Task 4)
| # | Prompt | What went wrong | What I changed and why |
|---|--------|-----------------|------------------------|
| 1 | `<prompt>` | `<problem>` | `<change>` |
| 2 | `<prompt>` | `<problem>` | `<change>` |
| 3 | `<prompt>` | worked | |


<img width="865" height="342" alt="LAB3" src="https://github.com/user-attachments/assets/9d328471-a172-462a-b79a-af9480543a7c" />



