# sql

SELECT *
 FROM `noble-particle-455016-a2.Ecommerce.Customers` 
 LIMIT 20

 SELECT *
FROM `noble-particle-455016-a2.Ecommerce.Customers`
WHERE address = '123 Main'
ORDER BY last_name;

SELECT last_name, COUNT(*) AS num_customers
FROM `noble-particle-455016-a2.Ecommerce.Customers`
GROUP BY last_name
ORDER BY num_customers DESC;


SELECT *
FROM `noble-particle-455016-a2.Ecommerce.Customers`
WHERE last_name IN (
    SELECT last_name
    FROM `noble-particle-455016-a2.Ecommerce.Customers`
    GROUP BY last_name
    HAVING COUNT(*) > 1
);

SELECT COUNT(*) AS total_customers
FROM `noble-particle-455016-a2.Ecommerce.Customers`
