# SQL查询

### 不同列条件查询 union有时候比or略快

https://leetcode-cn.com/problems/big-countries/submissions/

```mssql
select name, population, area
from world
where 
area > 3000000 or population > 25000000
```

```mssql
select name, population, area
from world
where 
area > 3000000
union
select name, population, area
from world
where 
population > 25000000
```

