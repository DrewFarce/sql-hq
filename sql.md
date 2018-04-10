use sakila;
select*from actor;
 select first_name, last_name from actor;
 select first_name, last_name, concat(first_name,' ',last_name) AS ActorName from actor;
select*from actor where first_name='Joe';
select*from actor where last_name='Gen%';
 select*from actor where last_name like'%li%',
order by last_name, first_name asc;
select*from country
where country in ('Afghanistan','Bangladesh','China');
ALTER TABLE actor
DROP COLUMN last_update, 
DROP COLUMN last_name,
ADD maddress_iddle_name text,
add last_name text;
ALTER TABLE actor MODIFY COLUMN middle_name blob;
ALTER TABLE actor drop column middle_name;
select last_name as 'Column Name', data_type as text,
character_maximum_length as 'Max Length'
from actor.last_name;
UPDATE Customers
SET first_name = 'HARPO'
WHERE last_name = 'WILLIAMS'
AND first_name = 'GROUCHO';
UPDATE Customers
SET first_name= 'GROUCHO'
WHERE last_name='WILLIAMS'
AND first_name='HARPO'
SET first_name= 'MUCHO GROUCHO'
WHERE last_name = 'WILLIAMS'
AND first_name = 'GROUCHO';
use sakila;
CREATE TABLE Address1
*************************** 1. row ***************************
       Table: Address1
Create Table: CREATE TABLE `Address1` (
  `address_id` varchar(100) NOT NULL,
  `address` varchar(60) DEFAULT NULL,
  `address2` varchar(60) DEFAULT NULL,
  `district` varchar(60) DEFAULT NULL,
  `city_id` varchar(60) DEFAULT NULL,
  `postal_code` varchar(60) DEFAULT NULL,
  `phone` varchar(60) DEFAULT NULL,
  `location` varchar(60) DEFAULT NULL,
  `last_update` varchar(60) DEFAULT NULL,
  PRIMARY KEY (`address_id`);

SELECT *
INTO Address1
FROM address;

SELECT staff.first_name, staff.last_name, staff.address_id,address.address_id,address.address
FROM staff
JOIN address
ON staff.address_id=address.address_id;
sum (*)
from payment.amount 
where
select staff.staff_id,payment.amount,payment.payment_date
from staff
join payment 
on staff.staff_id=payment.staff_id
where payment.payment_date='2005-08%';

select film.title, film.film_id, film_actor.actor_id
from film
inner join film_actor
on film.film_id=film_actor.film_id;

