# VIX-Rakamin_BI-Analyst-PT-Sejahtera-Bersama_Salsabilla-Rizka-Ardhana
Project based internship Rakamin BI Analyst Bank Muamalat database dan visualisasi data dengan google big query dan looker studio

Pada projek ini akan dianlisis penjualan dari PT Sejahtera Bersama berdasarkan master data yang dibuat pada Google Big Query dan visualisasi data dengan Looker Studio. Terdapat 4 tabel yang terdiri dari atbel customers, product, orders, dan product category. Masing-masing tabel kemudian dicari primary key dan foreign key untuk dilakukan proses inner join. Berikut merupakan key dari masing-masing tabel:

-Tabel Customer          : Primary Key adalah kolom CustomerID dan Foreign key adalah kolom CustomerID yang dilakukan inner join dengan tabel Orders 

-Tabel Orders            : Primary Key adalah kolom OrderID dan Foreign key adalah kolom CustomerID yang dilakukan inner join dengan tabel Customers serta ProdNumber 	dilakukan inner join dengan tabel Products

-Tabel Products          : Primary Key adalah kolom ProdNumber dan Foreign key adalah kolom ProdNumber dilakukan inner join dengan tabel Orders serta Category dilakukan inner 	join dengan tabel ProductCategory					

-Tabel Products Category  : Primary Key adalah kolom CategoryAbbreviation dan Foreign key adalah kolom CategoryID dilakukan inner join dengan tabel Products
Pembuatan master table pada dataset penjualan dilakukan dengan Google Big Query dimana menggunakan syntax SELECT, SUM, INNER JOIN,GROUP BY, dan ORDER BY, seperti dibawah ini

