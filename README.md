# SQL_Odev
lcw bootcamp sql ödev reposudur

-- 1. Film Tablosunda bulunan title ve description sütunlarındaki verileri sıralama
SELECT title, description
FROM film
ORDER BY title;

-- 2. Film Tablosunda bulunan tüm sütunlardaki verileri, length 60'dan büyük VE 75'ten küçük olma koşullarıyla sıralama
SELECT *
FROM film
WHERE length > 60 AND length < 75
ORDER BY title;

-- 3. Film Tablosunda bulunan tüm sütunlardaki verileri, rental_rate 0.99 VE replacement_cost 12.99 VEYA 28.99 olma koşullarıyla sıralama
SELECT *
FROM film
WHERE rental_rate = 0.99
  AND (replacement_cost = 12.99 OR replacement_cost = 28.99)
ORDER BY title;

-- 4. Customer Tablosunda bulunan first_name sütunundaki değeri 'Mary' olan müşterinin last_name sütunundaki değeri
SELECT last_name
FROM customer
WHERE first_name = 'Mary';

-- 5. Film Tablosundaki uzunluğu (length) 50'den büyük OLMAYIP aynı zamanda rental_rate değeri 2.99 veya 4.99 OLMAYAN verileri sıralama
SELECT *
FROM film
WHERE length <= 50
  AND rental_rate NOT IN (2.99, 4.99)
ORDER BY title;
