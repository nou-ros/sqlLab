## Chapters:
1. [SELECT basics](#select-basics)
2. [SELECT name](#select-name)
3. [SELECT FROM World](#select-from-world)
4. [SELECT FROM Nobel](#select-from-nobel)

## SELECT basics
1. 
```sql
	SELECT population FROM world
	 WHERE name = 'Germany'
```
2.
```sql 
	SELECT name, population FROM world
	  WHERE name IN ('Sweden', 'Norway', 'Denmark');
```
3.
```sql
	SELECT name, area FROM world
	  WHERE area BETWEEN 200000 AND 250000
```
## SELECT name
1.
```sql - Find the country that start with Y
	SELECT name FROM world
	  WHERE name LIKE 'Y%'	
```
2.
```sql - Find the countries that end with y
	SELECT name FROM world
	  WHERE name LIKE '%y'
```
3.
```sql - Find the countries that contain the letter x
	SELECT name FROM world
	  WHERE name LIKE '%x%'
```
4.
```sql - Find the countries that end with land
	SELECT name FROM world
	  WHERE name LIKE '%land'
```
5. 
```sql - Find the countries that start with C and end with ia
	SELECT name FROM world
	  WHERE name LIKE 'C%ia'
```
6.
```sql - Find the country that has oo in the name
	SELECT name FROM world
	  WHERE name LIKE '%oo%'
```
7. 
```sql - Find the countries that have three or more a in the name
	SELECT name FROM world
	  WHERE name LIKE '%a%a%a%'
```
8. 
```sql - Find the countries that have "t" as the second character.
	SELECT name FROM world
	 WHERE name LIKE '_t%'
	ORDER BY name
```
9. 
```sql - Find the countries that have two "o" characters separated by two others.
	SELECT name FROM world
	 WHERE name LIKE '%o__o%'
```
10. 
```sql - Find the countries that have exactly four characters.
	SELECT name FROM world
	 WHERE name LIKE '____'
```
11.
```sql - Find the country where the name is the capital city.
	SELECT name
	  FROM world
	 WHERE name LIKE capital
```
12. 
```sql - Find the country where the capital is the country plus "City".
	SELECT name FROM world
	 WHERE capital LIKE CONCAT(name, ' city')
```
13.
```sql - Find the capital and the name where the capital includes the name of the country.
	SELECT capital, name FROM world
	 WHERE capital LIKE CONCAT(name, '%')
```
14. 
```sql - Find the capital and the name where the capital is an extension of name of the country.
	SELECt capital, name FROM world
	 WHERE capital LIKE CONCAT(name, '%') AND capital <> name
```
15.
```sql - Show the name and the extension where the capital is an extension of name of the country.

	SELECT name, REPLACE(capital, name, '') FROM world
	 WHERE capital LIKE CONCAT(name, '%') AND capital <> name
```
## SELECT FROM World
1.
```sql - Show the name, continent and population of all countries.
	SELECT name, continent, population FROM world
```
2.
```sql - Show the name for the countries that have a population of at least 200 million
	SELECT name FROM world
	 WHERE population >= 200000000
```
3.
```sql - Give the name and the per capita GDP for those countries with a population of at least 200 million.
	SELECT name, (gdp/population) as pgdp FROM world
	 WHERE population >= 200000000
```
4.
```sql - Show the name and population in millions for the countries of the continent 'South America'.
	SELECT name, population/1000000 FROM world
	 WHERE continent = 'South America'
```
5.
```sql - Show the name and population for France, Germany, Italy
	SELECT name, population FROM world
	 WHERE name IN ('France', 'Germany', 'Italy')
```
6. 
```sql - Show the countries which have a name that includes the word 'United'
	SELECT name FROM world
	 WHERE name LIKE 'United%'
```
7.
```sql - Show the countries that are big by area or big by population. Show name, population and area.
	SELECT name, population, area FROM world
	 WHERE area >= 3000000 OR population >= 250000000
```



