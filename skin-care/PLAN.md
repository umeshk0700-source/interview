# Skin care plan

A daily routine page plus a morning reminder. Day 1 is 2026-11-27.

- `index.html` is the page. It works out the day from the start date and shows only today's steps, the product for each, and how to use it.
- A scheduled task runs every morning at 6:10 am US Central. It decides the day's plan, rewrites the `DAILY-PLAN` and `DAILY-NOTE` blocks on the published page, and sends a phone notification.

## Face (every day, unchanged)

| When | Step | Product |
|---|---|---|
| Morning, in the bath | Wash face | La Roche-Posay Toleriane Foaming Cleanser |
| Morning, after the bath | Moisturizer | CeraVe PM Facial Moisturizing Lotion |
| Morning, last | Sunscreen on face and neck | SKIN1004 Hyalu-Cica Water-Fit Sun Serum |
| Night | Wash face | La Roche-Posay Toleriane Foaming Cleanser |
| Night | Serum | Anua Niacinamide 10% + TXA 4% Serum |
| Night | Moisturizer | CeraVe PM Facial Moisturizing Lotion |

## Body (one new product at a time)

Usual soap from day 1. A "Buy this now" box appears 7 days before each start, so there is time to order it. Patch test on the first day.

| Day | Date | Product | How often |
|---|---|---|---|
| 8 | 2026-12-04 | CeraVe Daily Moisturizing Lotion | Every day after the bath |
| 22 | 2026-12-18 | Neutrogena Body Clear or CeraVe SA Body Wash | 3 or 4 days a week, never two in a row |
| 36 | 2027-01-01 | AmLactin Daily Moisturizing Lotion (12%) | Every other day for a week, then daily |
| 50 | 2027-01-15 | Degree Men Clinical Protection | Every other night |

Hair wash is a choice made on the page each day.

## Check-ins

- Starting photos on day 1. Photo checks on 2026-12-24 and 2027-01-21.
- Doctor checkup in the first two weeks.

## How the daily specialist works

The user only looks at the page and follows it. Each morning the scheduled task:

1. Reads this file and `LOG.md`, then the published page.
2. Decides today's plan (SA day or not, anything to skip) and rewrites the page's `DAILY-PLAN` and `DAILY-NOTE` blocks.
3. Decides whether it is time for a new product (rules below). If so, adds it to the page's `ITEMS` with a start day 7 days from today and a `why`, and adds it to the body or face table here.
4. Adds one line to `LOG.md`, commits and pushes.
5. Sends a phone notification with today's steps.

Rules for adding a product:

- One new product at a time, and at least 14 days after the last one started.
- Only from "Ideas for later" below, or a common over-the-counter product for a goal already in this plan. Nothing prescription.
- Never mention it before it is added; it then shows as "Buy this now" for 7 days.
- Keep personal health details out of this repo. It is public.

## Ideas for later (not added yet)

Decide when the time comes:

- Adapalene gel 0.1% (Differin), around month 3, 2 or 3 nights a week on nights without the serum.
- A milder body wash in place of bar soap, possibly when the body lotion starts.
- Lip balm with SPF.
- If the face turns red or itchy, use the serum every other night (CeraVe PM also contains niacinamide).
