# Patika+ Week6 SQL ile 4. Ödev Uygulaması
Merhaba,
Bu proje SQL ile Patika+ 6.hafta SQL komutları pratik için yapılmış bir uygulamadır.

## 📚 Proje Hakkında
Bu proje, aşağıdaki konuları öğrenmeye yardımcı olmak için tasarlanmıştır:
- Temel SQL komutları
- WHERE kullanımı
- AND ve OR kullanımı
- BETWEEN kullanımı
- IN kullanımı
- LIKE ve ILIKE


## İstenilen Görev
Aşağıdaki sorgu senaryolarını dvdrental örnek veri tabanı üzerinden gerçekleştiriniz.
   1. film tablosunda bulunan replacement_cost sütununda bulunan birbirinden farklı değerleri sıralayınız.
   2. film tablosunda bulunan replacement_cost sütununda birbirinden farklı kaç tane veri vardır?
   3. film tablosunda bulunan film isimlerinde (title) kaç tanesini T karakteri ile başlar ve aynı zamanda rating 'G' ye eşittir?
   4. country tablosunda bulunan ülke isimlerinden (country) kaç tanesi 5 karakterden oluşmaktadır?
   5. city tablosundaki şehir isimlerinin kaç tanesi 'R' veya r karakteri ile biter?


## Kod 
```sql
/*
Aşağıdaki sorgu senaryolarını dvdrental örnek veri tabanı üzerinden gerçekleştiriniz.

    1. film tablosunda bulunan replacement_cost sütununda bulunan birbirinden farklı değerleri sıralayınız.
    2. film tablosunda bulunan replacement_cost sütununda birbirinden farklı kaç tane veri vardır?
    3. film tablosunda bulunan film isimlerinde (title) kaç tanesini T karakteri ile başlar ve aynı zamanda rating 'G' ye eşittir?
    4. country tablosunda bulunan ülke isimlerinden (country) kaç tanesi 5 karakterden oluşmaktadır?
    5. city tablosundaki şehir isimlerinin kaç tanesi 'R' veya r karakteri ile biter?
*/

-- 1.SORU
SELECT DISTINCT replacement_cost FROM film;

-- 2.SORU
SELECT COUNT(DISTINCT replacement_cost) FROM film;

-- 3.SORU
SELECT COUNT(*) FROM film
WHERE title LIKE('T%') AND rating IN('G');

-- 4.SORU
SELECT COUNT(*) FROM country
WHERE country LIKE('_____');

-- 5.SORU
SELECT COUNT(*) FROM city
WHERE city LIKE('%R') OR city LIKE('%r');

```





