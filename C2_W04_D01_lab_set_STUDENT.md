# Can you rebuild the day's count, sort a dashboard and write a definition on your own?

*Illustrative case: the company is real, the situation and the data are synthetic, built for this class.*

**The ticket, in short.** Uber, Hyderabad, the driver app. From Monday 31 August 2026 an enrolled
driver who stays online through a whole peak window is guaranteed Rs 300 per peak online hour, and
Uber tops up the gap. Six weeks each side of the launch: peak online hours 118,000 and then 146,300,
completed peak trips 224,200 and then 230,900, trips per peak online hour 1.90 and then 1.58. The city
head asks, by Friday, whether the scheme works, what it should pay for, and whether anyone is gaming
it.

**Who needs the answer.** You do, before Tuesday: Tuesday's session rehearses the one-slide review
the city head holds on Thursday, and it assumes every learner can compute the city's rate, sort a
dashboard into what it pays for and what guards it, and write one definition from a blank page.

**The questions on the way.** Which lines, in which order, print the city's rate? Which numbers move
first, and which guardrail does each north star need? What does a definition look like for a product
you use? Which nine numbers on a dashboard keep their place, and in which role?

The TA runs this set after the Kalpa notebook. Work the problems in order; problem 1 is the place to
start if code still slows you down. Items marked **Design** ask for the best-fit approach, the fact
that would switch it, or the second route that would confirm a number.

```
Post exactly this shape: xxxxx
```

---

## Problem 1. Which lines, in which order, print the city's trips per peak online hour?

Every analyst rebuilds a team's totals from the raw table before trusting a dashboard, and the
order of the steps is the part people get wrong.

Five of these eight lines rebuild notebook 08's count, and three are wrong turns mixed in. The
city's rate is a ratio of two sums: add every trip, add every hour, then divide.

| Line | Code |
|---|---|
| 1 | `dw = pd.read_csv("../data/C2_W04_D01_driver_weeks_STUDENT.csv")` |
| 2 | `dw["window"] = dw["week_start"].lt("2026-08-31").map({True: "before", False: "after"})` |
| 3 | `city = dw.groupby("window")[["peak_online_hours", "peak_trips"]].sum()` |
| 4 | `city["trips_per_hour"] = city["peak_trips"] / city["peak_online_hours"]` |
| 5 | `dw["rate"] = dw["peak_trips"] / dw["peak_online_hours"]` |
| 6 | `print(dw.groupby("window")["rate"].mean().round(2))` |
| 7 | `print(city.round(2))` |
| 8 | `dw["window"] = dw["week_start"].lt("2026-09-07").map({True: "before", False: "after"})` |

### Q1. Which lines, in this order, print 1.90 before and 1.58 after?

a) 1, 2, 5, 6

b) 1, 2, 3, 4, 7

c) 1, 2, 3, 7, 4

d) 1, 8, 3, 4, 7

---

## Problem 2. Which numbers move first, and which guardrail does each north star need?

Sit `exercises/unguided/C2_W04_D01_lead_lag_STUDENT.md`, three items, unless your group sat it in
the metric clinic. Post its three letters on their own line.

---

## Problem 3. What does a complete definition look like for a product you use every day?

Choose one product you open every day: a food-delivery app, a music app, a payments app, a
ride-hailing app as a rider, or your college's library portal. Pick the one number its team would
most like to grow, and write it on the seven lines.

| Line | Your product's number |
|---|---|
| Numerator | |
| Denominator, with its count beside the rate | |
| Window | |
| Exclusions | |
| What it does not reward | |
| Guardrails, two | |
| Gaming note, one line per guardrail | |

Show the TA your numerator and denominator before you write the rest. Tonight's take-home finishes
this definition, so keep it.

---

## Problem 4. Which of nine numbers keep their place on the city head's dashboard, and in which role?

A city dashboard grows a line each time someone asks a question, and the analyst who cuts it back to
the few numbers a decision needs is the one whose dashboard gets read.

The city head's dashboard carries nine numbers. The task: one north star, two guardrails that
protect riders, two leading inputs, and the rest cut from the dashboard's first page.

| # | Number on the dashboard |
|---|---|
| 1 | Peak online hours |
| 2 | Completed peak trips per enrolled driver online at peak, per week |
| 3 | Share of offers accepted |
| 4 | Median rider wait at peak |
| 5 | Enrolled drivers |
| 6 | Rider requests per online hour, by zone |
| 7 | Enrolled drivers online in the first peak hour |
| 8 | Completed peak trips, city total |
| 9 | Gross bookings for the quarter |

### Q2. Which number is the north star?

a) 1, peak online hours, since supply is what the scheme bought

b) 8, completed peak trips, since trips are what riders want

c) 5, enrolled drivers, since every one of them can be paid

d) 2, completed peak trips per enrolled driver online at peak

### Q3. Design. Which two numbers are the guardrails that protect riders?

a) 1 and 5, since hours and enrolment show supply is still there

b) 6 and 7, since requests and early log-ins show demand and supply

c) 3 and 4, since declining offers and long waits hurt riders first

d) 8 and 9, since trips and bookings show the outcome has arrived

### Q4. Which two numbers are the leading inputs?

a) 6 and 7, requests per online hour and drivers online in the first hour

b) 3 and 4, the share of offers accepted and the median rider wait at peak

c) 1 and 9, peak online hours this week and gross bookings for the quarter

d) 5 and 8, the count of enrolled drivers and the city's total of completed trips

### Q5. Design. Which reason defends cutting number 1, peak online hours, from the dashboard's first page?

a) Hours are what the old scheme paid for, and riders still waited as long

b) Hours cannot be computed from the tables the city team holds each week

c) Hours lag the north star, since they are only known at the quarter's end

d) Hours are already counted inside the north star's numerator each week
