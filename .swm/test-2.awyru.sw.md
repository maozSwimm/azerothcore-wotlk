---
id: awyru
name: test 2
file_version: 1.0.2
app_version: 0.9.5-5
file_blobs:
  src/genrev/CMakeLists.txt: 6b44fc283837b32a7bdeacd57ccb6d41a5f9bced
  data/sql/base/db_world/areagroup_dbc.sql: 48876f83c35be14e2bce7d8352a43c4bf2c6b5db
  data/sql/base/db_world/achievement_reward.sql: 360c8d45bc4aa15ba73f303420dcc5efb30f6ab4
---




change





<br/>



<!-- NOTE-swimm-snippet: the lines below link your snippet to Swimm -->
### 📄 src/genrev/CMakeLists.txt
```text
🟩 1      #
🟩 2      # This file is part of the AzerothCore Project. See AUTHORS file for Copyright information
🟩 3      #
🟩 4      # This file is free software; as a special exception the author gives
🟩 5      # unlimited permission to copy and/or distribute it, with or without
🟩 6      # modifications, as long as this notice is preserved.
🟩 7      #
🟩 8      # This program is distributed in the hope that it will be useful, but
🟩 9      # WITHOUT ANY WARRANTY, to the extent permitted by law; without even the
🟩 10     # implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.
🟩 11     #
🟩 12     
🟩 13     # Need to pass old ${CMAKE_BINARY_DIR} as param because its different at build stage
🟩 14     add_custom_target(revision.h ALL
🟩 15       COMMAND "${CMAKE_COMMAND}" -DBUILDDIR="${CMAKE_BINARY_DIR}" -P "${CMAKE_SOURCE_DIR}/src/cmake/genrev.cmake" "${CMAKE_BINARY_DIR}"
🟩 16       WORKING_DIRECTORY "${CMAKE_SOURCE_DIR}")
🟩 17     
🟩 18     set_target_properties(revision.h
🟩 19       PROPERTIES
🟩 20         FOLDER
🟩 21           "server")
🟩 22     
```

<br/>



<!-- NOTE-swimm-snippet: the lines below link your snippet to Swimm -->
### 📄 data/sql/base/db_world/areagroup_dbc.sql
```plsql
⬜ 8      /*!40101 SET @OLD_CHARACTER_SET_CLIENT=@@CHARACTER_SET_CLIENT */;
⬜ 9      /*!40101 SET NAMES utf8 */;
⬜ 10     /*!50503 SET NAMES utf8mb4 */;
🟩 11     /*!40014 SET @OLD_FOREIGN_KEY_CHECKS=@@FOREIGN_KEY_CHECKS, FOREIGN_KEY_CHECKS=0 */;
🟩 12     /*!40101 SET @OLD_SQL_MODE=@@SQL_MODE, SQL_MODE='NO_AUTO_VALUE_ON_ZERO' */;
🟩 13     /*!40111 SET @OLD_SQL_NOTES=@@SQL_NOTES, SQL_NOTES=0 */;
🟩 14     
🟩 15     -- Dumpar struktur för tabell acore_world.areagroup_dbc
🟩 16     DROP TABLE IF EXISTS `areagroup_dbc`;
🟩 17     CREATE TABLE IF NOT EXISTS `areagroup_dbc` (
🟩 18       `ID` INT NOT NULL DEFAULT 0,
🟩 19       `AreaID_1` INT NOT NULL DEFAULT 0,
🟩 20       `AreaID_2` INT NOT NULL DEFAULT 0,
🟩 21       `AreaID_3` INT NOT NULL DEFAULT 0,
🟩 22       `AreaID_4` INT NOT NULL DEFAULT 0,
🟩 23       `AreaID_5` INT NOT NULL DEFAULT 0,
🟩 24       `AreaID_6` INT NOT NULL DEFAULT 0,
🟩 25       `NextAreaID` INT NOT NULL DEFAULT 0,
🟩 26       PRIMARY KEY (`ID`)
🟩 27     ) ENGINE=MyISAM DEFAULT CHARSET=utf8mb4;
🟩 28     
🟩 29     -- Dumpar data för tabell acore_world.areagroup_dbc: 0 rows
🟩 30     DELETE FROM `areagroup_dbc`;
⬜ 31     /*!40000 ALTER TABLE `areagroup_dbc` DISABLE KEYS */;
⬜ 32     /*!40000 ALTER TABLE `areagroup_dbc` ENABLE KEYS */;
⬜ 33     
```

<br/>



<!-- NOTE-swimm-snippet: the lines below link your snippet to Swimm -->
### 📄 data/sql/base/db_world/achievement_reward.sql
```plsql
⬜ 5      -- HeidiSQL Version:             11.3.0.6295
⬜ 6      -- --------------------------------------------------------
⬜ 7      
🟩 8      /*!40101 SET @OLD_CHARACTER_SET_CLIENT=@@CHARACTER_SET_CLIENT */;
🟩 9      /*!40101 SET NAMES utf8 */;
🟩 10     /*!50503 SET NAMES utf8mb4 */;
🟩 11     /*!40014 SET @OLD_FOREIGN_KEY_CHECKS=@@FOREIGN_KEY_CHECKS, FOREIGN_KEY_CHECKS=0 */;
🟩 12     /*!40101 SET @OLD_SQL_MODE=@@SQL_MODE, SQL_MODE='NO_AUTO_VALUE_ON_ZERO' */;
🟩 13     /*!40111 SET @OLD_SQL_NOTES=@@SQL_NOTES, SQL_NOTES=0 */;
🟩 14     
🟩 15     -- Dumpar struktur för tabell acore_world.achievement_reward
🟩 16     DROP TABLE IF EXISTS `achievement_reward`;
🟩 17     CREATE TABLE IF NOT EXISTS `achievement_reward` (
🟩 18       `ID` MEDIUMINT unsigned NOT NULL DEFAULT 0,
🟩 19       `TitleA` MEDIUMINT unsigned NOT NULL DEFAULT 0,
🟩 20       `TitleH` MEDIUMINT unsigned NOT NULL DEFAULT 0,
🟩 21       `ItemID` MEDIUMINT unsigned NOT NULL DEFAULT 0,
🟩 22       `Sender` MEDIUMINT unsigned NOT NULL DEFAULT 0,
🟩 23       `Subject` VARCHAR(255) DEFAULT NULL,
🟩 24       `Body` text,
🟩 25       `MailTemplateID` MEDIUMINT unsigned DEFAULT 0,
🟩 26       PRIMARY KEY (`ID`)
🟩 27     ) ENGINE=MyISAM DEFAULT CHARSET=utf8mb4 ROW_FORMAT=FIXED COMMENT='Loot System';
🟩 28     
🟩 29     -- Dumpar data för tabell acore_world.achievement_reward: 103 rows
🟩 30     DELETE FROM `achievement_reward`;
🟩 31     /*!40000 ALTER TABLE `achievement_reward` DISABLE KEYS */;
⬜ 32     INSERT INTO `achievement_reward` (`ID`, `TitleA`, `TitleH`, `ItemID`, `Sender`, `Subject`, `Body`, `MailTemplateID`) VALUES
⬜ 33     	(13, 0, 0, 41426, 16128, 'Level 80', 'Congratulations on your conviction to reach the 80th season of adventure. You are undoubtedly dedicated to the cause of ridding Azeroth of the evils which have plagued us.$B$BAnd while the journey thus far has been no minor feat, the true battle lies ahead.$B$BFight on!$B$BRhonin', 0),
⬜ 34     	(45, 0, 0, 43348, 28070, 'You\'ve Been Around!', 'Well, look at ye!$B$BAnd I thought I had seen some things in this icy place! It seems obvious to this dwarf that you have the fire of the explorer burning in your eyes.$B$BWear this tabard with pride. That way your friends will know who to ask for directions when the time comes!$B$BKeep on the move!$B$BBrann Bronzebeard', 0),
```

<br/>



<!-- NOTE-swimm-snippet: the lines below link your snippet to Swimm -->
### 📄 data/sql/base/db_world/achievement_reward.sql
```plsql
⬜ 22       `Sender` MEDIUMINT unsigned NOT NULL DEFAULT 0,
⬜ 23       `Subject` VARCHAR(255) DEFAULT NULL,
⬜ 24       `Body` text,
🟩 25       `MailTemplateID` MEDIUMINT unsigned DEFAULT 0,
🟩 26       PRIMARY KEY (`ID`)
🟩 27     ) ENGINE=MyISAM DEFAULT CHARSET=utf8mb4 ROW_FORMAT=FIXED COMMENT='Loot System';
🟩 28     
🟩 29     -- Dumpar data för tabell acore_world.achievement_reward: 103 rows
🟩 30     DELETE FROM `achievement_reward`;
🟩 31     /*!40000 ALTER TABLE `achievement_reward` DISABLE KEYS */;
🟩 32     INSERT INTO `achievement_reward` (`ID`, `TitleA`, `TitleH`, `ItemID`, `Sender`, `Subject`, `Body`, `MailTemplateID`) VALUES
🟩 33     	(13, 0, 0, 41426, 16128, 'Level 80', 'Congratulations on your conviction to reach the 80th season of adventure. You are undoubtedly dedicated to the cause of ridding Azeroth of the evils which have plagued us.$B$BAnd while the journey thus far has been no minor feat, the true battle lies ahead.$B$BFight on!$B$BRhonin', 0),
🟩 34     	(45, 0, 0, 43348, 28070, 'You\'ve Been Around!', 'Well, look at ye!$B$BAnd I thought I had seen some things in this icy place! It seems obvious to this dwarf that you have the fire of the explorer burning in your eyes.$B$BWear this tabard with pride. That way your friends will know who to ask for directions when the time comes!$B$BKeep on the move!$B$BBrann Bronzebeard', 0),
🟩 35     	(46, 78, 78, 0, 0, '', '', 0),
⬜ 36     	(230, 72, 0, 0, 0, '', '', 0),
⬜ 37     	(432, 53, 53, 0, 0, NULL, NULL, 0),
⬜ 38     	(456, 139, 139, 0, 0, '', '', 0),
```

<br/>

This file was generated by Swimm. [Click here to view it in the app](http://localhost:5000/repos/Z2l0aHViJTNBJTNBYXplcm90aGNvcmUtd290bGslM0ElM0FtYW96U3dpbW0=/docs/awyru).