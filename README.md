# Chess Game - Player vs Computer

This project implements a chess game in Python with a graphical user interface and a computer opponent powered by minimax and alpha-beta pruning enhanced with quiescence search and Zobrist hashing.

## Features

* **Player vs Computer**: Choose to play as White or Black against an AI.
* **AI Algorithms**: Alpha-beta pruning with move ordering and quiescence search for improved performance; fallback to minimax when desired.
* **Zobrist Hashing**: Fast position hashing to detect threefold repetition draws and speed up transposition handling.
* **Evaluation Function**: Material balance, piece–square tables, passed-pawn bonuses, king activity, and endgame coordination metrics.
* **Graphical Interface**: Built with `pygame` and `pygame_gui`, featuring move highlighting, color-scheme selection, move log, evaluation score, and undo/reset controls.
* **Configurable**: Adjust search depth, color schemes, and other parameters in the source code.

## Requirements

* Python 3.8 or higher
* `pygame` library
* `pygame_gui` library

## Installation

1. **Clone the repository**

   ```bash
   git clone https://github.com/yourusername/chess-pvc.git
   cd chess-pvc
   ```
2. **Create a virtual environment**

   ```bash
   python -m venv venv
   source venv/bin/activate   # On Windows: venv\Scripts\activate
   ```
3. **Install dependencies**

   ```bash
   pip install pygame pygame_gui
   ```

## Usage

Run the main application:

```bash
python main.py
```

* Select your color (White or Black) in the pop-up window.
* Play moves by clicking on squares.
* Press **Z** to undo the last move, **R** to reset the game.
* View the AI’s evaluation score and move log in the side panel.

## Project Structure

```
├── main.py           # Entry point, GUI setup, and game loop
├── chess_engine.py   # GameState class: board representation and move generation
├── search.py         # Search class: AI algorithms (alpha-beta, minimax, quiescence)
├── evaluation.py     # Board evaluation metrics and helper functions
├── constants.py      # Piece values and piece-square tables
├── zobrist.py        # Zobrist hashing key initialization
└── pieces/           # PNG images for chess pieces
```

## Configuration

* **Search Depth**: Modify `Search.DEPTH` in `search.py` to increase or decrease AI lookahead.
* **Color Schemes**: Edit `COLOR_SCHEMES` in `main.py` to add or change board colors.

## Contributing

Contributions, bug reports, and feature requests are welcome. Please open an issue or submit a pull request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
