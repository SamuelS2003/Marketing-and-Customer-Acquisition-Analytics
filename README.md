# Marketing & Customer Acquisition Analysis

A three-page Power BI dashboard that answers one question for a business spending money to win customers: **is the spend buying customers worth keeping?**

I built it to look at acquisition from three angles. Where do customers come from, which campaigns actually make money, and what kind of customers do we end up with?

![Acquisition Overview](https://github.com/SamuelS2003/Marketing-and-Customer-Acquisition-Analytics/blob/e4cd948caae7e32593711f55a5b43592e75c43b1/Dashboard%20Screenshots/Acquisition%20Overview.png)

## The short version

| Metric | Value |
|---|---|
| Customers acquired | 2,200 |
| Orders | 5,873 |
| Net sales | €640.42K |
| Contribution margin | €127.65K (19.93%) |
| Marketing cost | €29.88K |
| Marketing cost per customer | €13.58 |
| Revenue per customer | €291.10 |
| Margin per customer | €58.02 |
| Average order value | €109.05 |

The headline: the channel that gets the most budget is not the one that earns the most margin, discounts quietly eat profit, and a minority of customers produces most of the value.

## What each page answers

### 1. Acquisition Overview: where do customers come from?

- How many customers does each channel bring in, and at what cost?
- Which channels buy contribution margin cheaply, and which are expensive?
- Is customer volume growing quarter over quarter?

Visuals: KPI cards, customers by year and quarter, a marketing cost vs contribution margin bubble chart by channel, a channel distribution table, and net sales by channel.

### 2. Campaign Performance: which campaigns generate commercial value?

- Which campaigns sell the most, and which keep their margin?
- What does each campaign cost as a share of its sales?
- Which promotion objectives (acquisition, retention, clearance and so on) deliver margin for the spend?

Visuals: net sales with contribution margin % by campaign, a campaign cost distribution table, a cost vs margin bubble chart by objective, net sales by objective, and marketing cost by campaign.

### 3. Customer Value: what kind of customers are we acquiring?

- Which segments (VIP, Loyal, Growth, New, At Risk, Deal Seeker) drive sales and margin?
- How does the customer base change in the months after acquisition?
- Which channels bring in which segments?

Visuals: net sales and margin % by segment, customer lifecycle progression, a segment distribution table, and a channel-by-segment heatmap.

## What I found

**Spend is concentrated where value is lowest.** Paid Social takes 52% of marketing cost but returns 14% of contribution margin. It costs about €30 per acquired customer against about €3 for Organic Search and Email/CRM, and it brought in only 8 of the 131 VIPs. Email/CRM brought in 48.

**Discounts buy volume at the expense of margin.** Promoted sales earn a 16.7% margin against 25.4% with no promotion. Clearance 35% finished at -12.3% (a loss of about €2.8K), while Bundle & Save earned 28.5% at the lowest cost share of any campaign (3.36%). Welcome 15% is the largest single cost line at €7.4K, roughly a quarter of the promotion budget.

**Value sits in a small share of customers.** Loyal, Growth and VIP customers are 47% of the base but 73% of contribution margin. VIPs are 6% of customers and spend €716.65 each. Deal Seekers earn only a 9.3% margin, and Paid Social and Affiliate bring in 59% of them.

## Recommendations

1. **Rebalance the channel budget** toward channels with a higher margin per customer, and set a cost-per-customer ceiling for each channel.
2. **Add margin guardrails to promotions.** Review Clearance 35% and Weekend Flash 25%, and test a free-shipping welcome offer in place of the Welcome 15% discount.
3. **Protect the high-value customers.** Build VIP perks, run win-back journeys for the 307 At Risk customers, and aim paid channels at audiences that look like Growth and Loyal customers.
4. **Track channel quality, not just volume.** Add VIP % and Deal Seeker % by channel to the monthly scorecard.

The full write-up, with the business question behind each chart and scenarios by stakeholder (CMO, Performance Marketing, Pricing & Promotions, Finance, CRM and others), is in the slide deck.

## Tools

- Power BI for the data model and report
- DAX for measures
- PowerPoint for the written report

## Files

```
.
├── Marketing and Customer Acquisition.pbix        # Power BI report
├── Marketing Customer Acquisition_Report.pptx # Page-by-page report and stakeholder scenarios
├── Dashboard Screenshots/
│   ├── Acquisition Overview.png
│   ├── Campaign Performance.png
│   └── Customer Value & Lifecycle.png
└── README.md
```

Adjust the file names above to match your repo.

## Things to know before you rely on the numbers

- **Derived figures.** Cost and margin per customer by channel, margin shares and return ratios were calculated from the dashboard figures. They are not measures in the report.
- **Values read from charts.** The campaign table was scrolled in the screenshots, so Welcome 15%, Weekend Flash 25%, Summer Event 15% and VIP Private Sale 12% were read from the charts and are approximate.
- **Quarterly customers chart.** Its bars add up to roughly 5K, well above the 2,200 acquired customers, so it probably counts active customers per quarter. Q4 2025 is about 23% below Q3 and I have not confirmed whether that is seasonality or incomplete data.
- **Contribution margin.** I treated it as reported. Whether it is before or after marketing cost changes how the per-euro return ratios should be read.
- **Email/CRM and VIPs.** Email often reaches existing customers, so its VIP share may partly reflect who it was sent to rather than who it acquired.
- **Lifecycle tail.** The 13 to 18 month stage only includes the earliest cohorts, so the drop-off looks steeper than it is.

