# github_task


## task 1

SELECT customer_name, delivery_adress, name as name_courier, phone_number, car_brand, amount, title, cost, amount * cost as summ  FROM store_db.orders  
#SELECT * FROM store_db.orders  
JOIN store_db.couriers
on  orders.id_courier =  couriers.id

JOIN store_db.order_items  
on  orders.id =  order_items.id_order

JOIN store_db.products  
on  order_items.id_product = products.id

WHERE name = 'Вова';
