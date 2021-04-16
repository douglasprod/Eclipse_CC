# Eclipse_CC
Eclipse CORE | Character Creation documentation

1. Put `Eclipse_Core` && `Eclipse_CC` in your resource directory
2. Add ensure in your `server.cfg`


| Command | Description |
| --- | --- |
| `ensure eclipse_Core` | You must ensure this resource the first |
| `ensure eclipse_CC` | just add it ;/ |

3. MySql settings (resources\eclipse_Core\config\database.json)


  ![1](https://user-images.githubusercontent.com/36680471/114997401-759f4a80-9ea8-11eb-8b81-ba096d1c6e6b.PNG)
  
4. Turn on Mysql 
5. Load dump database in your mysql client  
`/*!40101 SET @OLD_CHARACTER_SET_CLIENT=@@CHARACTER_SET_CLIENT */;
/*!40101 SET NAMES utf8 */;
/*!50503 SET NAMES utf8mb4 */;
/*!40014 SET @OLD_FOREIGN_KEY_CHECKS=@@FOREIGN_KEY_CHECKS, FOREIGN_KEY_CHECKS=0 */;
/*!40101 SET @OLD_SQL_MODE=@@SQL_MODE, SQL_MODE='NO_AUTO_VALUE_ON_ZERO' */;
/*!40111 SET @OLD_SQL_NOTES=@@SQL_NOTES, SQL_NOTES=0 */;


-- Дамп структуры базы данных eclipse
CREATE DATABASE IF NOT EXISTS `eclipse` /*!40100 DEFAULT CHARACTER SET utf8mb4 */;
USE `eclipse`;

-- Дамп структуры для таблица eclipse.characters
CREATE TABLE IF NOT EXISTS `characters` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `characterData` longtext NOT NULL,
  `characterCloth` longtext NOT NULL,
  `position` varchar(50) DEFAULT NULL,
  `license` longtext NOT NULL,
  PRIMARY KEY (`id`),
  KEY `Индекс 2` (`characterData`(100))
) ENGINE=InnoDB AUTO_INCREMENT=15 DEFAULT CHARSET=utf8mb4;

-- Экспортируемые данные не выделены.

/*!40101 SET SQL_MODE=IFNULL(@OLD_SQL_MODE, '') */;
/*!40014 SET FOREIGN_KEY_CHECKS=IF(@OLD_FOREIGN_KEY_CHECKS IS NULL, 1, @OLD_FOREIGN_KEY_CHECKS) */;
/*!40101 SET CHARACTER_SET_CLIENT=@OLD_CHARACTER_SET_CLIENT */;
/*!40111 SET SQL_NOTES=@OLD_SQL_NOTES */;`
