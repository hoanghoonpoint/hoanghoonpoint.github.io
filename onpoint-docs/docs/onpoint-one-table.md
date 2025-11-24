
---

# ✅ 3. `docs/onpoint-one-table.md`

A beautiful table:

```md
# OnPoint One Table Documentation

This page describes all available columns in the **OnPoint One** dataset.

## 📄 Table Schema

| Column | Type | Description |
|--------|------|-------------|
| `date_key` | `DATE` | The date (YYYY-MM-DD). |
| `advertiser_id` | `STRING` | Unique advertiser identifier. |
| `store_id` | `STRING` | Store ID associated with the event. |
| `campaign_id` | `STRING` | Campaign unique ID. |
| `impressions` | `INTEGER` | Number of ad impressions. |
| `clicks` | `INTEGER` | Number of clicks received. |
| `orders` | `INTEGER` | Number of attributed orders. |
| `gmv` | `FLOAT` | Gross merchandise value. |
| `cost` | `FLOAT` | Total ad spend. |
| `roi` | `FLOAT` | Return on investment (GMV / cost). |

---

## ▶ Example Query (BigQuery)

```sql
SELECT
  date_key,
  advertiser_id,
  campaign_id,
  impressions,
  clicks,
  gmv,
  roi
FROM `project.dataset.onpoint_one`
WHERE date_key >= DATE_SUB(CURRENT_DATE(), INTERVAL 7 DAY);
