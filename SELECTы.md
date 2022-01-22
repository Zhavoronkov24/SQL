# SQL SELECT    (MySQL)

-- Вывести все категории товаров

SELECT * from category;

-- Вывести все категории товаров с идентификатором, равным 3
SELECT * from category 
WHERE id = 3;

-- Вывести все категории товаров, у котрых скидка не равна 0
SELECT * from category 
WHERE discount <> 0;

-- Вывести все категории товаров, у котрых скидка больше 5 
SELECT * from category 
WHERE discount > 5;

-- Вывести все категории товаров, у котрых скидка больше 5 и меньше 15
SELECT * from category 
WHERE (discount > 5) AND (discount < 15);

-- Вывести все категории товаров, у котрых скидка меньше 5 или больше или равна 10
SELECT * from category 
WHERE (discount < 5) OR (discount >= 10);

-- Вывести все категории товаров, у котрых скидка не меньше 5
SELECT * from category 
WHERE NOT (discount < 5);

-- Вывести все категории товаров, у котрых есть псевдоним
SELECT * from category 
WHERE alias_name IS NOT NULL;

-- Вывести все категории товаров, у котрых нет псевдонима
SELECT * from category 
WHERE  alias_name IS NULL;


-- вывести названия и скидки товаров
SELECT discount, name  FROM category;

-- вывести все скидки
SELECT discount FROM category;


-- вывести все уникальные значения скидок
SELECT DISTINCT discount FROM category;


-- вывести все категории товаров, и отсортировать их по размеру скидки
SELECT * FROM category 
ORDER BY discount;

-- вывести все категории товаров, и отсортировать их по размеру скидки в обратном порядке
SELECT * FROM category 
ORDER BY discount DESC;

-- вывести все категории товаров с ненулевой скидкой, и отсортировать их по размеру скидки в обратном порядке
SELECT * FROM category 
WHERE discount <> 0 
ORDER BY discount DESC;

-- вывести первые 2 категории товара
SELECT * FROM category LIMIT 2;

-- вывести первые 2 категории товара со скдикой не равной нулю
SELECT * FROM category 
WHERE discount <> 0 LIMIT 2;



