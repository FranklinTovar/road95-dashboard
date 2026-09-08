# ROAD 95 Dashboard - Project Core

Last updated: 2026-09-08

## Purpose

ROAD 95 is Franklin Tovar's daily athletic control center. The dashboard must combine the training plan, progressive overload, periodization, recovery, bodyweight, nutrition, KPIs, Foundation exit gates, and the path toward dunking without overcrowding the main screen.

The dashboard language is English. Planning and product discussion may continue in Spanish.

## Non-negotiable visual system

- Preserve the approved front design. Do not redesign it during functional updates.
- Near-black and charcoal surfaces, grayscale imagery, fluorescent lime `#caff3a`, thin technical borders, restrained glow, and compact uppercase labels.
- Premium dark athletic-performance / JARVIS atmosphere.
- Desktop main area uses a 50/50 split between Today's Workout and the media carousel.
- Keep the READY indicator compact, centered, and illuminated.
- Exercise thumbnails use the approved circular monochrome style.
- Back Squat, Bench Press, and Barbell Row have their own specific thumbnails.
- Exercises without an approved specific thumbnail may use Franklin's approved athlete image in the same circular monochrome treatment.
- The desktop Today screen should fit within one viewport whenever practical. Tablet and phone-specific refinement is a later planned phase.

## Today screen order

1. ROAD 95 / Daily Control Center header and READY indicator.
2. Next Session, Block Position, Current Weight, and discipline statement.
3. Today's Workout and the media carousel, 50/50 on desktop.
4. Weight System.
5. Weekly Status.

## Calendar behavior - agreed concept, not yet implemented

The current dashboard remembers the manually selected day. The desired future behavior is date-aware:

- `TODAY'S WORKOUT` shows the session assigned to the actual calendar date.
- `NEXT SESSION` shows the next scheduled session after today.
- At midnight, the new day's session becomes Today's Workout automatically.
- Opening a past or future week/day is a `VIEWING` state and must not change the actual current date.
- Rest days show `REST / ACTIVE RECOVERY`; Next Session searches forward to the next scheduled training session.

This behavior must be implemented only after Franklin approves it.

## Training navigation and logging

- Block Position opens Weeks 0-8.
- Week 0 is Partial Start; Week 1 is the first official week.
- Week 8 is Deload.
- Every week must allow selection of Monday-Sunday.
- Each day shows the complete prescribed session from Direction General.
- Never invent missing exercise prescriptions; ask Franklin or consult Direction General.
- Each exercise can record actual weight, sets, repetitions, RIR, feeling percentage, and notes.
- RIR means repetitions in reserve: the number of additional good repetitions Franklin felt capable of completing.
- Completed sessions update Weekly Status.
- Stored entries remain device-local through browser localStorage unless a synchronized system is approved later.

## Weight system

- Baseline: 118.25 kg on August 5.
- Current displayed weight: 109.25 kg.
- Change from baseline: -9.00 kg.
- Target / checkpoint: 95 kg.
- Remaining: 14.25 kg.
- Weight System appears before Weekly Status on the Today screen.
- Future nutrition calculations should adapt as bodyweight and energy expenditure change; calorie requirements must not be assumed to remain fixed during weight loss.

## Nutrition reference - seven-day menu

Official reference supplied by Franklin: `menu_completo_7_dias copy.pdf`.

Status: memorized as project reference, but not yet placed in the dashboard. Franklin will later decide whether it becomes a button, tab, or another module.

The menu contains breakfast, lunch, dinner, and a snack for seven days. Main meals are designed below approximately 800 kcal with at least 40 g protein; snacks are lighter.

### Day 1

- Chocolate and berry pancakes: about 520 kcal / 50 g protein.
- Mexican chicken bowl: about 750 kcal / 70 g protein.
- Chicken and mozzarella pizza: about 650 kcal / 65 g protein.
- Greek yogurt, strawberries, and dark chocolate: about 180 kcal / 17 g protein.

### Day 2

- Breakfast burrito: about 550 kcal / 55 g protein.
- Pasta Bolognese: about 760 kcal / 60 g protein.
- Chicken shawarma: about 700 kcal / 70 g protein.
- Skyr and a small banana: about 170 kcal / 18 g protein.

### Day 3

- Protein waffles: about 550 kcal / 50 g protein.
- Chicken curry: about 730 kcal / 70 g protein.
- BBQ burger and seasoned potatoes: about 780 kcal / 55 g protein.
- Chocolate protein pudding: about 180 kcal / 25 g protein.

### Day 4

- Salmon and egg bagel: about 600 kcal / 50 g protein.
- Asian-style beef: about 700 kcal / 50 g protein.
- Chicken quesadillas: about 690 kcal / 70 g protein.
- Greek yogurt and berries: about 150 kcal / 17 g protein.

### Day 5

- Cheesecake bowl: about 500 kcal / 50 g protein.
- Beef burrito: about 780 kcal / 55 g protein.
- Salmon with potatoes: about 700 kcal / 45 g protein.
- Protein yogurt and fruit: about 180 kcal / 20 g protein.

### Day 6

- French toast: about 580 kcal / 50 g protein.
- Chicken fajitas: about 750 kcal / 65 g protein.
- Spicy chicken ramen: about 700 kcal / 55 g protein.
- Skyr and fruit: about 150 kcal / 17 g protein.

### Day 7

- Omelette pizza with toast: about 550 kcal / 55 g protein.
- Salmon poke bowl: about 780 kcal / 45 g protein.
- Beef tacos: about 700 kcal / 55 g protein.
- Yogurt, cocoa, and whey mousse: about 180 kcal / 25 g protein.

### Menu principle

Avoid repetitive plain meals. Rotate cuisines and flavors: Mexican, Italian, Asian, Mediterranean, BBQ, curry, and Japanese. Use sauces, herbs, spices, and condiments to give each meal a distinct identity.

The PDF does not define a final daily calorie target. Calories and quantities must be adjusted later using Franklin's approved calorie target, preferred meal frequency, current bodyweight, training load, basketball load, and recovery data.

## Connected ROAD 95 information sources

- Direction General: authoritative training architecture, exercises, sets, repetitions, load progression, week structure, deload decisions, and PROGRESS / HOLD / ADJUST decisions.
- ROAD 95 - Data & Recovery: recovery, pain, fatigue, sleep, weight, and other athlete data.
- Project Core: long-term architecture, benchmarks, Foundation exit gates, and strategic decisions.

## Current publication

GitHub Pages: `https://franklintovar.github.io/road95-dashboard/`

The current version includes the approved front, 50/50 training/carousel layout, Weeks 0-8 navigation, day selection, exercise logging, local storage, dynamic Weekly Status, and the corrected Weight System baseline.

## Pending decisions and future work

- Approve and implement automatic calendar-aware Today / Next Session behavior.
- Decide how the seven-day nutrition menu enters the dashboard: button, tab, or dedicated module.
- Add bodyweight-driven calorie and expenditure recalculation rules after the required inputs and method are approved.
- Continue adding exercise-specific monochrome thumbnails without changing the visual style.
- Refine tablet and phone layouts after the desktop front is stable.
- Add full recovery inputs: knee pain, lumbar pain, fatigue, sleep, soreness, and other Data & Recovery fields.
- Consider cross-device synchronization only after Franklin approves moving beyond localStorage.

## Change-control rule

Before any visual change, compare it against the approved reference and this Project Core. Functional additions must extend the existing design rather than replace it. When information is unavailable, do not invent it; ask Franklin or retrieve it from the corresponding ROAD 95 source.
