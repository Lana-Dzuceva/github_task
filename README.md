# github_task
# СДЕЛАЮ ДО КОНЦА СУТОК

## task 1

SELECT customer_name, delivery_adress, name as name_courier, phone_number, car_brand, amount, title, cost, amount * cost as summ FROM store_db.orders 
JOIN store_db.couriers on orders.id_courier = couriers.id 

JOIN store_db.order_items
on orders.id = order_items.id_order

JOIN store_db.products
on order_items.id_product = products.id

WHERE orders.id = 1;

## task 2
### Клиент Енототуй заказывает мотоцикл
INSERT INTO `orders` 
(customer_name, delivery_adress, id_courier) 
VALUES ('Енототуй', 'крутая', 1); 
INSERT INTO `order_items` 
(id_product, id_order, amount)  
VALUES (6, LAST_INSERT_ID(), 5); 

## task 3 
SELECT customer_name, delivery_adress, name as name_courier, phone_number, car_brand, amount, title, cost, amount * cost as summ FROM store_db.orders 
JOIN store_db.couriers on orders.id_courier = couriers.id

JOIN store_db.order_items
on orders.id = order_items.id_order

JOIN store_db.products
on order_items.id_product = products.id

WHERE couriers.id = 2; #(Получение всей инфы по id курьера)

## task 4 

UPDATE `order_items` SET amount = 3 WHERE id_order = 2 AND id_product = (SELECT id FROM `products` WHERE title = 'меч');

