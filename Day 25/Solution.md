Solution1:
```sql

select store_id, 
sum(case when ltrim(lower(product_1)) like 'apple%' then 1 else 0 end) as product_1,
sum(case when ltrim(lower(product_2)) like 'apple%' then 1 else 0 end) as product_2
from product_demo
group by store_id
```