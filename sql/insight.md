### First Step: Validate the Core Problem
- Before diagnose anything, confirm the retention problem is real and worth solving.
```sql
-- Cohort analysis by first purchase year
SELECT 
    EXTRACT(YEAR FROM cohort_month) as cohort_year,
    COUNT(DISTINCT customer_unique_id) as total_customers,
    COUNT(DISTINCT CASE WHEN is_repeat_customer = 1 THEN customer_unique_id END) as repeat_customers,
    ROUND(100.0 * COUNT(DISTINCT CASE WHEN is_repeat_customer = 1 THEN customer_unique_id END) / 
          COUNT(DISTINCT customer_unique_id), 2) as repeat_rate_pct
FROM summary
GROUP BY EXTRACT(YEAR FROM cohort_month)
ORDER BY cohort_year;
```  
