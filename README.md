הקמת הDB:
CREATE DATABASE shopping_list;

USE shopping_list;

CREATE TABLE `categories` (
  `id` int NOT NULL AUTO_INCREMENT,
  `name` varchar(255) NOT NULL,
  PRIMARY KEY (`id`)
) ENGINE=InnoDB AUTO_INCREMENT=0 DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_0900_ai_ci;

INSERT INTO categories (name) VALUES ('מוצרי ניקיון'), ('גבינות'), ('בשר ודגים'), ('ירקות ופירות'), ('מאפים');

CREATE TABLE `orders` (
  `full_name` varchar(255) NOT NULL,
  `full_address` varchar(255) NOT NULL,
  `email` varchar(255) NOT NULL,
  `order_details` json NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_0900_ai_ci;
