# 📊 Traffic Analysis & Optimization with MySQL

## 🚀 Overview
This project showcases advanced SQL techniques to analyze website traffic, optimize marketing spend, and improve conversion rates. It simulates real-world business decisions using MySQL queries and performance metrics.

---

## 🎯 Business Objectives
- Identify high-performing traffic sources
- Optimize ad bids based on conversion performance
- Monitor weekly trends across campaigns and devices
- Maximize ROI by reallocating spend to top-converting segments

---

## 🧪 SQL Tasks & Insights

### 1️⃣ Top Traffic Sources
```sql
SELECT utm_source, utm_campaign, http_referer,
       COUNT(DISTINCT website_session_id) AS sessions
FROM website_sessions
WHERE created_at < '2012-04-12'
GROUP BY 1, 2, 3
ORDER BY 4 DESC;
