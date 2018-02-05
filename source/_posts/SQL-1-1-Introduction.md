---
title: SQL|1.1 Introduction
date: 2018-02-05 14:05:52
tags: 
categories: SQL
---
```sql
drop table if exists modeling_db.zq_model_res01_sample_repay_date;
create table  modeling_db.zq_model_res01_sample_repay_date as
select to_date(apply_time) obs_date
from mysql.loan_consumer_application
where apply_time is not null
group by to_date(apply_time)
order by obs_date
```
