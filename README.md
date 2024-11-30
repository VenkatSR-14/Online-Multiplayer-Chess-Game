# Online Multiplayer Chess Game

This repository contains the source code for an online multiplayer chess game built with **.NET Core** and **React**. The application supports real-time gameplay between two players, with persistent game states and move validation.

---

## Tech Stack

### Backend (Server-side)
- **.NET Core**  
  Used to build a RESTful API and real-time communication using SignalR.
- **Entity Framework Core**  
  For database interaction and game state persistence.
- **SignalR**  
  Enables real-time communication for player moves and updates.

### Frontend (Client-side)
- **React**  
  Provides a dynamic and responsive user interface.
- **chess.js**  
  Manages chess game logic (e.g., move validation and checkmate detection).
- **react-chessboard**  
  Renders the chessboard in the browser.
- **SignalR Client**  
  Connects to the backend for real-time updates.

---

## Features
- **Real-time multiplayer gameplay**  
  Play chess with other players in real-time.
- **Move validation**  
  Powered by `chess.js` to ensure only legal moves are made.
- **Persistent game states**  
  Game state and move history are saved in a database.
- **Interactive chessboard**  
  Responsive and dynamic chessboard rendering using `react-chessboard`.

---

## Project Structure

### Backend (`ChessGameAPI`)
- **Controllers**  
  - `GameController`: Handles API endpoints for game actions such as starting a game and retrieving game states.
- **SignalR Hub**  
  - `GameHub`: Manages real-time communication for player moves and updates.
- **Models**  
  - `Game`: Represents a chess game (players, board state, etc.).
  - `Move`: Represents a single move in the game.
- **Database**  
  - Stores game state, player data, and move history using Entity Framework Core.

### Frontend (`chess-game-client`)
- **Components**  
  - `Chessboard`: Displays the game board and updates it based on the game state.
  - `GameRoom`: Manages multiplayer gameplay and connections.
- **Services**  
  - `SignalRService`: Establishes and manages SignalR connections.
- **Game Logic**  
  - Validates moves, checks for game-ending conditions, and handles game logic using `chess.js`.

---

## Setup Instructions

### Backend
1. Install the .NET Core SDK:  
   ```bash
   dotnet --version
Clone the repository and navigate to the backend folder:
bash
Copy code
cd ChessGameAPI
Install dependencies:
bash
Copy code
dotnet restore
Run the API:
bash
Copy code
dotnet run
Frontend
Install Node.js and npm:
bash
Copy code
node --version
npm --version
Clone the repository and navigate to the frontend folder:
bash
Copy code
cd chess-game-client
Install dependencies:
bash
Copy code
npm install
Start the React app:
bash
Copy code
npm start
How to Play
Start the backend server (ChessGameAPI).
Launch the frontend React app (chess-game-client).
Create or join a game room.
Play chess in real-time with another player!
Contributing
Fork the repository.
Create a new feature branch.
Commit your changes.
Open a pull request.
License
This project is licensed under the MIT License.