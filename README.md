# Making-a-Memory-Game
This is a simple web-based Memory Matching Game built with Python using the Flask web framework. The game challenges users to match pairs of emoji cards by flipping them over two at a time.
Features
Classic memory game with emoji cards.

Cards are randomly shuffled at the start of each game.

Keeps track of:

Number of moves made.

Number of pairs found.

Game progress and victory state.

Backend handles game state securely using Flask sessions.

Game logic written in an object-oriented way (MemoryGame class).

RESTful endpoints to flip cards, start a new game, and render the main page.

Game Logic Overview
Each game consists of 6 unique emoji pairs (12 cards total).

Cards start face-down (❓), and are flipped via user input.

The game logic:

Prevents flipping matched or already revealed cards.

Locks interaction between the first and second flip to ensure proper timing.

Resets revealed cards if there's no match.

Tracks when all pairs are matched (game win condition).

Tech Stack
Backend: Python + Flask

Frontend: HTML (templated via render_template)

State Management: Flask sessions (session['game'])

API:

POST /flip_card: Flip a card and evaluate matches.

POST /new_game: Reset and start a new game.

GET /: Load the main game page.
