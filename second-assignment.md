# 2. Ödev

## BETWEEN ve IN


Merhabalar,

Aşağıdaki sorgu senaryolarını dvdrental örnek veri tabanı üzerinden gerçekleştiriniz.

1. film tablosunda bulunan tüm sütunlardaki verileri replacement cost değeri 12.99 dan büyük eşit ve 16.99 küçük olma koşuluyla sıralayınız ( BETWEEN - AND yapısını kullanınız.)

```

SELECT * FROM film
WHERE replacement_cost BETWEEN 12.99 AND 16.99;

```

2. .actor tablosunda bulunan first_name ve last_name sütunlardaki verileri first_name 'Penelope' veya 'Nick' veya 'Ed' değerleri olması koşuluyla sıralayınız. ( IN operatörünü kullanınız.)

```
SELECT first_name, last_name
FROM actor
WHERE first_name IN ('Penelope', 'Nick', 'Ed');


SELECT first_name, last_name komutu, actor tablosundan first_name ve last_name sütunlarını seçmemizi sağlar.
FROM actor komutu, verilerin hangi tablodan alınacağını belirtir. Bu durumda actor tablosundan alıyoruz.
WHERE first_name IN ('Penelope', 'Nick', 'Ed') komutu, 
seçilecek verileri filtrelememize yarar. Bu komutla sadece first_name
sütununda belirtilen değerlerden birine sahip olan verileri seçiyoruz. IN operatörü, 
birden fazla değer arasında seçim yapmamızı sağlar. Parantez içindeki değerler arasına virgül koyarak ayrıyoruz.
```


3. film tablosunda bulunan tüm sütunlardaki verileri rental_rate 0.99, 2.99, 4.99 VE replacement_cost 12.99, 15.99, 28.99 olma koşullarıyla sıralayınız. ( IN operatörünü kullanınız.)
Kolay Gelsin.


```

SELECT *
FROM film
WHERE rental_rate IN (0.99, 2.99, 4.99) AND replacement_cost IN (12.99, 15.99, 28.99);




- `SELECT *` komutu, film tablosundaki tüm sütunlardaki verileri seçmemizi sağlar. * işareti, tüm sütunları ifade eder.
- `FROM film` komutu, verilerin hangi tablodan alınacağını belirtir. Bu durumda film tablosundan alıyoruz.
- `WHERE rental_rate IN (0.99, 2.99, 4.99) AND replacement_cost IN (12.99, 15.99, 28.99)`
komutu, seçilecek verileri filtrelememize yarar.
Bu komutla sadece rental_rate sütununda 0.99, 2.99 veya 4.99 değerlerinden 
birine ve replacement_cost sütununda da 12.99, 15.99 veya 28.99 değerlerinden birine sahip olan verileri seçiyoruz.
IN operatörü, birden fazla değer arasında seçim yapmamızı sağlar.
Parantez içindeki değerler arasına virgül koyarak ayrıyoruz. AND operatörü, iki koşulun da sağlanmasını gerektirir.

```
