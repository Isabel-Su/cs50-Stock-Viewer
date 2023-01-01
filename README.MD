# This is CS50 final project which is inspired by the finance project.

It is a stock watch list webapp, which allows user to add symbols, fetch's stocks'price and renders the stock historic price chart. the stock data is provided by IEX.
---

### Technical Stacks

Python Flask framework: [Offical website](https://flask.palletsprojects.com/)

mySQL database : [Offical website](https://www.mysql.com/)

jQuery: [Offical website](https://jquery.com/)

ChartJS: [Offical website](https://www.chartjs.org/)


please follow the instructures to install the Flask and mySql.


environment variables for IEX API key. [read the guide](https://iexcloud.io/blog/how-to-get-market-data-in-python#:~:text=Finding%20your%20API%20Token&text=Get%20started%20by%20logging%20in,which%20begins%20with%20%22pk_.%22)
```
$ export API_KEY=value
export FLASK_APP=app.py
```

database port: 3306
Database Schema
```
DROP TABLE IF EXISTS `users`;
/*!40101 SET @saved_cs_client     = @@character_set_client */;
/*!50503 SET character_set_client = utf8mb4 */;
CREATE TABLE `users` (
  `id` int NOT NULL AUTO_INCREMENT,
  `username` varchar(50) NOT NULL,
  `password` varchar(255) NOT NULL,
  PRIMARY KEY (`id`)
) ENGINE=InnoDB AUTO_INCREMENT=15 DEFAULT CHARSET=utf8;


DROP TABLE IF EXISTS `portfolios`;
/*!40101 SET @saved_cs_client     = @@character_set_client */;
/*!50503 SET character_set_client = utf8mb4 */;
CREATE TABLE `portfolios` (
  `id` int NOT NULL AUTO_INCREMENT,
  `user_id` int NOT NULL,
  `symbol` varchar(255) NOT NULL,
  `price` double NOT NULL,
  `date` varchar(255) NOT NULL,
  PRIMARY KEY (`id`,`user_id`,`symbol`)
) ENGINE=InnoDB AUTO_INCREMENT=28 DEFAULT CHARSET=utf8;

```

**Run**
```
flask run
```
By default, the server is running at http://http://localhost:5000/

