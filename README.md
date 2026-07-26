# Marketing Campaign Data

An Excel workbook analyzing paid marketing performance across Google Ads and Facebook Ads, covering **October 16, 2019 – July 7, 2020**. It combines a raw event-level dataset (~16.8K rows) with pivot tables and charts that break down spend, clicks, and cost efficiency by channel, subchannel, device, and audience age group.

## File

`Marketing_Campaign_Data.xlsx`

## Structure

The workbook has 5 sheets:

| Sheet | Contents |
|---|---|
| `Dashboard` | Landing sheet (placeholder / cover page — no data) |
| `Subchannels` | Pivot tables + charts comparing spend, impressions, clicks, and CPC across subchannels (Brand, Generic, Competitor, Facebook Ads) over time |
| `Google v Face` | Pivot tables + charts comparing Google Ads vs. Facebook Ads performance side by side |
| `Device_by_age` | Pivot table + chart breaking down CPC and CPA by device type and age bracket |
| `Raw_Data` | The underlying event-level data (16,834 rows) that all pivot tables and charts are built from |

## Raw_Data schema

| Column | Description | Example values |
|---|---|---|
| `Date` | Date of the record | 2019-10-16 to 2020-07-07 |
| `campaign_platform` | Ad platform | Google Ads, Facebook Ads |
| `campaign_type` | Campaign objective | Search, Conversions |
| `communication_medium` | Ad format | Search Keywords, Creative |
| `subchannel` | Targeting subchannel | Brand, Generic, Competitor, Facebook Ads |
| `audience_type` | Audience segment | Audience 1, Audience 2, Audience 3, — |
| `creative_type` | Creative format used | (creative-level detail) |
| `creative_name` | Name/ID of the creative | (creative-level detail) |
| `device` | Device category | Desktop, Mobile, Tablet |
| `age` | Age bracket | 18-24, 25-34, 35-44, 45-54, 55-64, 65 or more, Undetermined |
| `spends` | Amount spent | numeric ($) |
| `impressions` | Number of impressions | numeric |
| `clicks` | Number of clicks | numeric |
| `link_clicks` | Number of link clicks | numeric |

## Key metrics tracked

- **Total Spend** by channel, subchannel, and month
- **CPC** (Cost Per Click) by channel, subchannel, device, and age
- **CPA** (Cost Per Acquisition) by device and age
- **Spend share** (%) breakdown between Google Ads and Facebook Ads

## Included charts

The `Subchannels`, `Google v Face`, and `Device_by_age` sheets include pre-built PivotCharts, including:
- Total Spend by Channels (monthly trend)
- Total CPC by Channels
- Google: Total Spend by Channel / Channel %
- Facebook: Total Spend by Channel / Breakdown
- Google & Facebook CPC by Subchannel

## Notes

- Some `subchannel` and `audience_type` values are recorded as placeholders (`'-'`) where the dimension wasn't applicable to that row.
- All pivot tables are built from a shared pivot cache sourced from `Raw_Data`; refreshing the pivots in Excel will recalculate all charts.
