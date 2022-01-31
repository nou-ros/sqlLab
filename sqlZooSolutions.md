## Chapters:
1. [SELECT basics](#select_basics)
2. [SELECT name](#select_name)
3. [SELECT FROM World](#select_from_world)
4. [SELECT FROM Nobel](#select_from_nobel)

## SELECT basics
1. 
```sql
  SELECT population FROM world
    WHERE name = 'Germany'
```
2.
```
sql 
SELECT name, population FROM world
  WHERE name IN ('Sweden', 'Norway', 'Denmark');
```
3.
```
sql
SELECT name, area FROM world
  WHERE area BETWEEN 200000 AND 250000
```
4.

