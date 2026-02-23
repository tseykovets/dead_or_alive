# Dead or Alive

Text-based game "Dead or Alive" (Russian: "Живым или мёртвым") by Peter Kosyh (Russian: Пётр Косых) and Nikita Tseykovets (Russian: Никита Цейковец).

The game is in Russian and developed for [UrqW](https://github.com/urqw/UrqW) text-based game engine.

This repository contains the source code and other resources of the game. The game is available for launch in the [UrqW engine online catalog](https://urqw.github.io/UrqW/?id=dead_or_alive).

The game was first published on February 23, 2026.

Interactive fiction identifier (IFID) of the game: DDC10DB6-D3FC-468B-A6D7-248651BE01AE

## Description

Итак, я добрался до Тумстона, этого проклятого городка Аризоны. Сойдя на станции, я сразу же направился в сторону салуна, который находился неподалёку. Мне пришлось отдать бармену все деньги, что у меня были, и он сказал мне, что комната Джимми находится в конце коридора слева. Он даже не посмотрел на объявление о розыске — похоже, Джимми успел прославиться и здесь… Я поднялся на второй этаж и достал свой кольт.

## Development

The game is developed using the [game template](https://github.com/urqw/game_template) for [UrqW engine](https://github.com/urqw/UrqW).

Workflow:

1. Clone the Game repository (`git clone`) and go to its directory (`cd`).
2. Install all dependencies:
	```shell
	npm install
	```
3. All game data is stored in the urqw directory. This is where the game development takes place.
4. Open the UrqW documentation if needed:
	```shell
	npm run docs
	```
5. Make your changes to the game files and build the project:
	```shell
	npm run build
	```
6. After the first build, run a local web server with an interpreter to debug the game you are developing:
	```shell
	npm start
	```
7. After significant changes to the project, rebuild it:
	```shell
	npm run build
	```
	The web server with the running interpreter will automatically track the build update and initiate a reload of the page with the new version of the game. \
	At any time, you can open the menu in the interpreter interface and expand the Debugging section to see additional information about the running game. The information is constantly updated.
8. Continue developing the game and debugging it in the running interpreter. In parallel, you can use the version control system to save the development history. Binary builds of the game will not be included in the Git history.
9. At any time, you can extract the text of descriptions, actions, string literals, and comments from the game's source code to proofread it separately from the programming language constructs:
	```shell
	npm run extract
	```
10. Once the game is ready to be a major update, you can create (or update) an iFiction record with the game's metadata:
	```shell
	npm run ifiction
	```
	Enter the data that will be requested. See the [Treaty of Babel](https://babel.ifarchive.org) for more details.
11. Once the game is ready, you can build the release as an archive:
	```shell
	npm run release
	```
	This archive is suitable for running in UrqW. \
	Or you can add or update the game repository to the UrqW instance repository as a Git submodule. The project structure meets the necessary UrqW requirements for adding games as submodules.

For details, please refer to the UrqW documentation.
