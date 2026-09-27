# Multiplayer Quiz Game: Client

The client side of a real-time, multiplayer trivia game built on **raw TCP sockets in C#**. It connects to the [quiz server](https://github.com/yagiz827/server), receives questions, sends answers and shows the round results and scoreboard.

Built as a group project for a university networking course.

## Features

- Connects to the server over **TCP** with a chosen IP, port and player name
- Receives questions, round results and scoreboards in real time on a background thread
- Sends numeric answers using the game's text protocol (`Name,<name>`, `Answer,<number>`)
- Windows Forms UI with a message log

## Game rules

Each question has a numeric answer. The player with the **closest answer** wins the round and gets 1 point; ties split the point. The player with the most points after the last question wins. See the [server README](https://github.com/yagiz827/server) for the full flow.

## Running

1. Start the [server](https://github.com/yagiz827/server) and note its IP and port.
2. Open `client.sln` in Visual Studio (.NET Framework 4.8) and start it. Run several instances to get several players.
3. Enter the server IP, port and your name, click **Connect**, and answer the questions as they arrive.
