# TicTacToe.NET-Tournament

Description
------------
Create a web-based tic-tac-toe tournament application with an ASP.NET Core backend and React frontend.

## Tech Stack
- ASP.NET Core
- React

## Requirements
- Bracket Management API (Hint: Use RESTful routes and clear naming)
- Turn-Based Game Logic (Hint: Validate moves server-side)
- State Synchronization in React (Hint: Utilize React hooks for live updates)
- Code Quality and Testing (Hint: Follow SOLID principles and add tests)

## Installation
*Backend*
1. Navigate to the backend folder: `cd server`
2. Install dependencies: `dotnet restore`
3. Configure environment variables:
   - `ASPNETCORE_ENVIRONMENT=Development`
   - `TournamentDb__ConnectionString=<Your_Connection_String>`
   - `Jwt__Key=<Your_JWT_Secret>`

*Frontend*
1. Navigate to the frontend folder: `cd client`
2. Install dependencies: `npm install`
3. Configure environment variables:
   - Create a `.env` file with:
     
     REACT_APP_API_BASE_URL=http://localhost:5000/api
     

## Usage
1. Start the backend:
   bash
   cd server
   dotnet run
   
2. Start the frontend:
   bash
   cd client
   npm start
   
3. Open your browser at `http://localhost:3000` to access the tournament.

## Implementation Steps
1. Scaffold an ASP.NET Core Web API project in a `server` folder.
2. Define domain models: `Bracket`, `Game`, `Move`.
3. Implement `BracketsController` with RESTful endpoints for bracket management.
4. Implement `GamesController` to handle game creation, turn validation, and move submission.
5. Apply SOLID principles and add xUnit tests for API logic.
6. Scaffold a React app in a `client` folder using `create-react-app`.
7. Build React components for bracket view, game board, and lobby.
8. Use React hooks (`useState`, `useEffect`, `useContext`) for live state synchronization.
9. Integrate Axios or Fetch API to communicate with backend endpoints.
10. Add Jest and React Testing Library tests for critical UI components.

## API Endpoints
### Bracket Management
- GET `/api/brackets` — List all brackets
- POST `/api/brackets` — Create a new bracket
- GET `/api/brackets/{id}` — Get bracket details

### Game Management
- POST `/api/games` — Create a new game in a bracket
- GET `/api/games/{gameId}` — Get current game state
- POST `/api/games/{gameId}/moves` — Submit a move