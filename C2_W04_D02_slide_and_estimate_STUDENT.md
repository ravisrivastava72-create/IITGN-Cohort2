# How do you rebuild a cluttered slide, and size a number aloud, one step at a time?

Uber, Hyderabad, the driver app's peak-hour earnings guarantee, one day on. On Monday 31 August 2026
the city team began guaranteeing Rs 300 for each peak hour online (the floor) to an enrolled driver
who stays online through a whole peak window, paying the gap between the driver's trip earnings and that floor
as a top-up. Over the six weeks after the launch, peak online hours
rose 24 percent while completed peak trips rose 3 percent, so gross bookings per peak online hour
(what riders paid for trips, divided by the hours drivers were online) fell from Rs 314 to Rs 260 at a
fare that held at Rs 165. The city head takes the redesign to Thursday's city review on one slide, and
before the review wants a rough count of the drivers the weekday evening peak needs.

> Illustrative case: the company is real, the situation and the data are synthetic, built for this class.

**Who needs the answer.** The city head, who has five minutes and one slide, and the analyst who
must size a number with no dataset before the same review.

**The questions on the way.**

- What does a cluttered slide look like once it carries one claim?
- Which number proves a drafted claim, and which denominator should a slide name?
- How does a chain of assumptions multiply out to drivers at the evening peak?

You work this set with the trainer: the first slide and the first estimate are worked in full, the
second of each is half worked, and the third is yours. Post one line, three letters in item order,
no spaces:

```
Post exactly this shape: xxx
```

---

## What does slide A look like once it carries one claim?

This comes up at work whenever a dashboard is pasted into a review deck: someone has to choose the
one sentence the meeting is for.

Slide A arrived titled "Peak guarantee: six-week review" with nine numbers of equal weight. Worked in
full, it becomes four parts:

| Part | What slide A now says |
|---|---|
| 1. The claim, as the title | The scheme is paying for online hours that carry no trips |
| 2. The evidence, with its denominator | A chart of gross bookings per peak online hour over twelve weeks (Rs 314 before, Rs 260 after, the drop in the launch week), and one number beside it: 61 percent of the top-up went to driver-weeks that accepted fewer than half their offers |
| 3. The caveat, beside the evidence | The monsoon ended inside the six weeks, and last year's weeks are not in the data |
| 4. The action, its cost, who signs | Test paying per completed peak trip with an acceptance floor on half the drivers, picked at random; across the enrolled drivers it saves Rs 58 lakh to Rs 92.7 lakh over six weeks, at a per-trip rate fixed before the test; the city head signs the test |

The saving comes from Monday: Rs 1.16 crore (115.9 lakh, since 1 crore is 100 lakh) of the Rs 1.9
crore top-up went to driver-weeks that accepted fewer than half the requests offered to them. The
redesign stops paying it, except where those drivers start accepting and qualify. If half of it is still
paid, 115.9 / 2 = Rs 58 lakh is saved; if a fifth is still paid, 115.9 x 4/5 = Rs 92.7 lakh.

---

## Which number proves slide B's drafted claim?

This comes up at work when finance sends a tab of nine money numbers and the slide can show one.

Slide B is half worked. The claim is drafted: "Most of the top-up went to driver-weeks that accepted
fewer than half their offers." Finance's tab holds these nine:

| Finance's tab | Before | After |
|---|---|---|
| Gross peak bookings | Rs 3.70 crore | Rs 3.81 crore |
| Bookings per online hour | Rs 314 | Rs 260 |
| Bookings per active driver-week | Rs 5,817 | Rs 5,861 |
| Bookings per trip | Rs 165 | Rs 165 |
| Top-up paid | Rs 0 | Rs 1.9 crore |
| Top-up per completed trip | | Rs 82.3 |
| Top-up to low acceptance | | Rs 1.16 crore |
| Top-up to everyone else | | Rs 74 lakh |
| Rider requests | 251,910 | 256,556 |

Low acceptance means a driver-week that accepted fewer than half the requests offered. An active
driver-week is one driver with a row in the week's table. "Most" needs a share of a total.

### Q1. Which one number from finance's tab proves the drafted claim?

*Level L1 · asked in every analyst screen.*

a) Bookings per active driver-week, Rs 5,817 before and Rs 5,861 after
b) Top-up to everyone else, Rs 74 lakh in the six weeks after
c) Top-up per completed trip, Rs 82.3 in the six weeks after
d) Top-up to low acceptance, Rs 1.16 crore of the Rs 1.9 crore paid

---

## Which denominator should slide C name?

This comes up at work whenever one total can be divided by several things and each division tells a
different story.

Slide C is blank. Driver operations' tab shows 180 drivers in the idle tail (Monday's name for the
drivers whose trips per online hour fell under 1.0 after the launch): their online hours rose from
20,000 to 42,000 while their trips fell from 38,000 to 33,440. You write the claim; first choose the
denominator its evidence will name.

### Q2. Design. Slide C's claim is about what the scheme running now buys with its money. Which denominator should its evidence name?

*Level L2, a design call · asked in global capability centre (GCC) and product-company screens.*

a) Per active driver-week, since every driver with a row that week counts once
b) Per completed trip, since a trip is what a rider pays for
c) Per peak online hour, since that is the unit the guarantee is priced in
d) Per enrolled driver, since enrolment is the number marketing reports

---

## How many cups of tea does the campus canteen sell on a weekday?

This comes up in interviews as the warm-up, and at work whenever a number is needed before the data is.

This one is worked in full, with chapter 6's invented numbers. **Clarify:** one canteen, one weekday,
cups and not litres. **Map:** students on campus x share who buy tea x cups each. **Calculate:** 3,000 x
0.45 x 2 = 2,700 cups. **Validate:** the canteen's till for one weekday, which averages 2,340 cups, so
the chain runs 15.4 percent high and the share who buy is the guess to replace first.

---

## How many drivers must be online at the weekday evening peak?

This comes up at work when an operations lead needs a number for a meeting that will not wait for data.

This one is half worked. Clarify: the Hyderabad metro area, Uber, one product, drivers online at one moment of
the three-hour weekday evening peak, a median rider wait under five minutes. The chain, worked at its
central values:

| Factor | Value, an assumption said aloud |
|---|---|
| Trips to serve an hour | 1 crore people x 1 weekday Uber trip per 100 people x a quarter of the day's trips in the evening / 3 hours = about 8,330 |
| Trips one online driver completes an hour | a busy driver's 2.4 trips x (1 - 0.30 idle) = 1.68 |
| Buffer for the busiest half hour | 1.15 |
| Drivers online | 8,330 / 1.68 x 1.15 = about 5,700 |

### Q3. On a slack evening the idle share could reach 0.38, the top of its range. How many trips does one online driver then complete in an hour?

*Level L5 · asked in product-company and consulting screens.*

a) 0.91
b) 1.49
c) 2.02
d) 3.87

---

## What is left for you to size?

The third estimate is yours at the afternoon's paired drill: UPI payments in India on an average day,
in seven minutes, all four steps on one sheet.

**How do you check your letters against the notebooks?** Open
`notebooks/C2_W04_D02_04_case_one_slide_answer_three_denominators_STUDENT.ipynb`: its second and third
code cells compute the three reads of the rupees. Then open
`notebooks/C2_W04_D02_08_case_guesstimate_drivers_at_peak_STUDENT.ipynb`: its ledger cell computes the
chain and how far each assumption moves it. Change a letter only if your reasoning changes with it.

**In the interview.** [S] Present a recommendation to a non-technical stakeholder in two minutes.
[S] A guesstimate: how many drivers must be online at the evening peak?
