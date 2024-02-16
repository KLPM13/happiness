-- what country have the highest avg happiness score for 3 years
select 
  Country,
avg(Happiness_Score) as country_avg_happiness_score
from 
    (
      SELECT  *
      FROM `reflecting-poet-391612.Happiness_data.2018`
      union all
      select *
      from `reflecting-poet-391612.Happiness_data.2017`
      union all
      select *
      from `reflecting-poet-391612.Happiness_data.2019`
      )
group by Country
order by country_avg_happiness_score desc;


-- COUNTRY AVG GDP SCORE FOR 3 YEARS

select 
 Country,
 avg(GDP_per_capita) avg_gdp
from 
    (
      SELECT  *
      FROM `reflecting-poet-391612.Happiness_data.2018`
      union all
      select *
      from `reflecting-poet-391612.Happiness_data.2017`
      union all
      select *
      from `reflecting-poet-391612.Happiness_data.2019`
      )
group by Country
order by avg_gdp desc;

-- COUNTRY SOCIAL SUPPORT SCORE
select 
 Country,
 avg(Social_support) avg_social_support
from 
    (
      SELECT  *
      FROM `reflecting-poet-391612.Happiness_data.2018`
      union all
      select *
      from `reflecting-poet-391612.Happiness_data.2017`
      union all
      select *
      from `reflecting-poet-391612.Happiness_data.2019`
      )
group by Country
order by avg_social_support desc;

-- life expectancy

select 
 Country,
 avg(Healthy_life_expectancy) avg_life_expectancy
from 
    (
      SELECT  *
      FROM `reflecting-poet-391612.Happiness_data.2018`
      union all
      select *
      from `reflecting-poet-391612.Happiness_data.2017`
      union all
      select *
      from `reflecting-poet-391612.Happiness_data.2019`
      )
group by Country
order by avg_life_expectancy desc;

-- AVG FREEDOM

select 
 Country,
 avg(freedom) avg_freedom
from 
    (
      SELECT  *
      FROM `reflecting-poet-391612.Happiness_data.2018`
      union all
      select *
      from `reflecting-poet-391612.Happiness_data.2017`
      union all
      select *
      from `reflecting-poet-391612.Happiness_data.2019`
      )
group by Country
order by avg_freedom desc;

-- COUNTRY GENEROSITY
select 
 Country,
 avg(Generosity) avg_generosity
from 
    (
      SELECT  *
      FROM `reflecting-poet-391612.Happiness_data.2018`
      union all
      select *
      from `reflecting-poet-391612.Happiness_data.2017`
      union all
      select *
      from `reflecting-poet-391612.Happiness_data.2019`
      )
group by Country
order by avg_generosity desc;

-- Perception of corruption

select 
 Country,
 avg(Perceptions_of_corruption) avg_corruption
from 
    (
      SELECT  *
      FROM `reflecting-poet-391612.Happiness_data.2018`
      union all
      select *
      from `reflecting-poet-391612.Happiness_data.2017`
      union all
      select *
      from `reflecting-poet-391612.Happiness_data.2019`
      )
group by Country
order by avg_corruption desc
