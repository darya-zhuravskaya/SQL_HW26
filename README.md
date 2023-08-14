## Task 1

На сайте w3schools.com на странице Learn SQL: http://www.w3schools.com/sql/default.asp
Нажать кнопку `Try it yourself`,  далее в новом окне нажать на кнопку  `Run SQL`
Запросы для таблицы `Customers`:
1. Вывести всех, кто живет в Лондоне
```sql   
SELECT * FROM Customers WHERE City = 'London'
```
2. Выбрать имена контактов и имена заказчиков, где адрес заканчивается на 23
```sql
SELECT CustomerName, ContactName, Address FROM Customers WHERE Address LIKE '%23'
```

3. Выбрать уникальные города.
```sql
SELECT DISTINCT City FROM Customers
```

4. Выбрать тех пользователей, у кого код начинается с 0 (нуль)
```sql
SELECT *FROM Customers WHERE PostalCode LIKE '0%'
```

5. Вывести клиентов не из США
```sql
SELECT *FROM Customers WHERE Country <> 'USA';
```

6. Вывести всех, кто из Франции и отсортировать по убыванию по имени контакта
```sql
SELECT *FROM Customers WHERE Country = 'France' ORDER BY ContactName DESC
```

7. Вывести клиентов из Германии и США, ограничить выбор 10 записями
```sql
SELECT *FROM Customers WHERE Country IN('Germany', 'USA') LIMIT 10
```

## Task 2

На сайте w3schools.com на странице Learn SQL: http://www.w3schools.com/sql/default.asp
Нажать кнопку `Try it yourself`,  далее в новом окне нажать на кнопку  `Run SQL`
Запросы для таблицы `Products`:
1. Выбрать все продукты, начинающиеся на букву «М»
```sql
SELECT * FROM Products WHERE ProductName LIKE 'M%'
```
2. Вывести характеристику упаковки (unit) для товара Steeleye Stout
```sql
SELECT Unit, ProductName FROM Products WHERE ProductName = 'Steeleye Stout'
```
3. Вывести названия товаров, цена которых выше 22
```sql
SELECT ProductName, Price FROM Products WHERE Price > 22  
```
4. Вывести товары, в которых вес упаковки составляет 500250 g
```sql
  SELECT *FROM Products WHERE Unit LIKE '%500 g%’ OR Unit LIKE '%250 g%’
```
5. Вывести товары, упаковка которых состоит из «bottles»
```sql
SELECT *FROM Products WHERE Unit LIKE '%bottles%'
```
6. Вывести товары, где SupplierID составляет 7 и отсортировать результаты по убыванию по цене
```sql
SELECT *FROM Products WHERE SupplierID = 7 ORDER BY  Price DESC
```
## Task 3

На веб-странице существует кнопка `«Быстрый поиск»`, которая выделяет из таблицы `character` в базе данных всех персонажей выше 45 уровня (столбец `level`), расы dwarf(столбец `race`) и выводит результат на страницу. Укажите, как будет выглядеть в данном случае SQL-запрос.
```sql
SELECT *FROM Character WHERE Level > 45 And Race = ‘dwarf’
```
## Task 4

На сайте w3schools.com на странице Learn SQL: http://www.w3schools.com/sql/default.asp
Нажать кнопку `Try it yourself`,  далее в новом окне нажать на кнопку  `Run SQL`
Запросы для таблицы `Employees`:
1. Вывести имя, фамилию и записи о сотруднике Leverling
```sql
SELECT FirstName, LastName, Notes FROM Employees WHERE LastName = 'Leverling'
```
2. Вывести информацию по работникам старше 1960 года
```sql
SELECT * FROM Employees WHERE BirthDate < ‘1960-01-01’
```

3. Вывести дату рождения сотрудников, чьи имена начинаются на букву «А»
```sql
SELECT FirstName, BirthDate FROM Employees WHERE FirstName LIKE 'A%'
```

4. Вывести имя, фамилию и дату рождения сотрудников, отсортировав по дате рождения по возрастанию
```sql
SELECT FirstName, LastName, BirthDate FROM Employees ORDER BY BirthDate
```
