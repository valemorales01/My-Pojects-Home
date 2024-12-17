# My-Pojects-Home
/* 
  This code showcases some components that might be helpful 
  when listing data for a restaurant. I'm sharing this project with you.
*/

-- 1. Show all records from the nomnom table
SELECT *
FROM nomnom;

-- 2. Show all distinct neighborhoods
SELECT DISTINCT neighborhood
FROM nomnom;

-- 3. Show all distinct types of cuisine
SELECT DISTINCT cuisine
FROM nomnom;

-- 4. Restaurants serving Chinese cuisine
SELECT *
FROM nomnom
WHERE cuisine = 'Chinese';

-- 5. Restaurants with review >= 4
SELECT *
FROM nomnom
WHERE review >= 4;

-- 6. Restaurants serving Italian cuisine with $$$ price range
SELECT *
FROM nomnom
WHERE cuisine = 'Italian'
  AND price = '$$$';

-- 7. Restaurants whose name contains the word "meatball"
SELECT *
FROM nomnom
WHERE name LIKE '%meatball%';

-- 8. Restaurants located in Midtown, Downtown, or Chinatown
SELECT *
FROM nomnom
WHERE neighborhood IN ('Midtown', 'Downtown', 'Chinatown');
-- Another equivalent approach:
-- WHERE neighborhood = 'Midtown' OR neighborhood = 'Downtown' OR neighborhood = 'Chinatown';

-- 9. Restaurants where the 'health' column is NULL
SELECT *
FROM nomnom
WHERE health IS NULL;

