# VIX Rakamin Bank Muamalat BI Analyst PT Sejahtera Bersama Salsabilla Rizka Ardhana
## Project based internship Rakamin BI Analyst Bank Muamalat database dan visualisasi data dengan google big query dan looker studio

Pada projek ini akan dianlisis penjualan dari PT Sejahtera Bersama berdasarkan master data yang dibuat pada Google Big Query dan visualisasi data dengan Looker Studio. Terdapat 4 tabel yang terdiri dari atbel customers, product, orders, dan product category. Masing-masing tabel kemudian dicari primary key dan foreign key untuk dilakukan proses inner join. Berikut merupakan key dari masing-masing tabel:

-Tabel Customer          : Primary Key adalah kolom CustomerID dan Foreign key adalah kolom CustomerID yang dilakukan inner join dengan tabel Orders 

-Tabel Orders            : Primary Key adalah kolom OrderID dan Foreign key adalah kolom CustomerID yang dilakukan inner join dengan tabel Customers serta ProdNumber 	dilakukan inner join dengan tabel Products

-Tabel Products          : Primary Key adalah kolom ProdNumber dan Foreign key adalah kolom ProdNumber dilakukan inner join dengan tabel Orders serta Category dilakukan inner 	join dengan tabel ProductCategory					

-Tabel Products Category  : Primary Key adalah kolom CategoryID dan Foreign key adalah kolom CategoryID dilakukan inner join dengan tabel Products
Pembuatan master table pada dataset penjualan dilakukan dengan Google Big Query dimana menggunakan syntax SELECT, SUM, INNER JOIN,GROUP BY, dan ORDER BY, seperti dibawah ini

`SELECT  
od.Date as order_date,pdc.CategoryName as category_name,pd.ProdName as product_name,pd.Price as product_price,od.Quantity as order_qty,SUM(pd.Price*od.Quantity) as total_sales,cs.CustomerEmail as cust_email,cs.CustomerCity as cust_city`

`FROM rakamin-intern-bank-muamalat.penjualan.customers as cs`

`inner join rakamin-intern-bank-muamalat.penjualan.orders as od
on cs.CustomerID=od.CustomerID`

`inner join rakamin-intern-bank-muamalat.penjualan.products as pd
on od.ProdNumber=pd.ProdNumber`

`inner join rakamin-intern-bank-muamalat.penjualan.productscategory as pdc
on pd.Category=pdc.CategoryID`

`GROUP BY 1,2,3,4,5,7,8`

`ORDER BY 1,5`

Berdasarkan query diatas dihasilkan master tabel dengan 8 kolom dan 3339 baris, Dimana data diurutkan berdasarkan tanggal dan quantity. Berikut merupakan gambaran tabel yang dihasilkan pada Google Big Query.

![Picture1](https://github.com/salsabillarzk/VIX-Rakamin_BI-Analyst-PT-Sejahtera-Bersama_Salsabilla-Rizka-Ardhana/assets/157949784/cf47c085-2f82-4fde-85cd-ce20f7e1da68)
![Picture2](https://github.com/salsabillarzk/VIX-Rakamin_BI-Analyst-PT-Sejahtera-Bersama_Salsabilla-Rizka-Ardhana/assets/157949784/66c8130a-8641-4381-bda5-a10542357145)

Master data penjualan yang telah diperoleh melalui Google Big Query perlu divisualisasikan untuk memudahkan tim lain yang terkait membaca laporan, menarik kesimpulan, dan membuat keputusan. Visualisasi dilakukan melalui Looker Studio dengan diperoleh hasil sebagai berikut.  

![Looker_Studio_Reporting_-_28_01_24,_16 32-1](https://github.com/salsabillarzk/VIX-Rakamin_BI-Analyst-PT-Sejahtera-Bersama_Salsabilla-Rizka-Ardhana/assets/157949784/af93eeee-a99e-442d-b7d4-bbc9e0d64247)

Berdasarkan hasil visualisasi dapat dibuat kesimpulan atau Keputusan untuk meningkatkan atau mempertahankan penjualan dengan cara berikut :




`

