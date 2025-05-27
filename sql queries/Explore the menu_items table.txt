USE restaurant_db;
-- 1 view the menu_items table
SELECT * FROM menu_items;

-- 2. Find the number of items on the menu
select count(item_name) from menu_items;

-- 3 What are the least and most expensive prices in the menu
SELECT * FROM menu_items
ORDER BY price desc;

-- 4 How many italian dishes are on the menu
Select category, COUNT(category) FROM menu_items WHERE category = 'italian';

-- 5. Find the number of dishes in each categrory
SELECT category, COUNT(*) FROM menu_items GROUP BY category;

-- 6 What is the avg dish price within each category
SELECT category, AVG(price) AS avergage_price FROM menu_items GROUP BY category;