
## 获取下月1号
```sql
b.bke112 < add_months(trunc(to_date(#bke112_end#,'yyyyMM')),1)
```