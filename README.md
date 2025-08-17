# Chess Game with Stockfish AI (C++ & SFML)


This project is an **interactive Chess game developed in C++** with a graphical interface powered by the **SFML (Simple and Fast Multimedia Library)** framework and integrated with the **Stockfish chess engine** for artificial intelligence. The goal was to create a fully functional Chess application that allows human players to play against a computer opponent, while also strengthening skills in C++, graphics programming, and AI integration.
Chess has long been a benchmark for computer intelligence, making it an ideal project for exploring both game development and AI. My motivation was twofold: to apply object-oriented C++ principles in building a complex but engaging application, and to integrate a world-class chess engine to make the gameplay realistic and challenging. This combination allowed me to explore areas such as user interface design, graphics rendering, algorithmic thinking, and external process communication.

# Features
- **Graphical Interface:** The chessboard and pieces are rendered with SFML sprites. A PNG image is used for the board background, and a sprite sheet is used for chess pieces.
- **Drag-and-Drop Movement:** Players interact with the game by dragging and dropping pieces, making it intuitive and visually clear.
- **Move Validation:** Standard Chess rules, including castling and capturing, are respected. Invalid moves are not allowed.
- **Stockfish AI Integration:** The game connects to the Stockfish engine using UCI (Universal Chess Interface). Stockfish computes moves when it is the computer’s turn, providing a strong AI opponent.
- **Animated Moves:** Opponent moves are smoothly animated to enhance realism instead of being applied instantly.
- **Move History:** All moves are tracked, enabling players to review or undo previous steps.


# Implementation
The project is structured into modules for clarity and maintainability. The chessboard is represented as a two-dimensional array, where integers encode piece type and color. Conversion functions translate between **pixel coordinates** on the screen and **algebraic chess notation** (e.g., e2e4).

User input is handled through SFML events. Mouse press events select a piece, while release events determine the target square. If the move is valid, the piece is repositioned and recorded. Castling is managed by detecting king moves from starting squares and automatically moving the rook.

The connection with Stockfish is established through a helper header (`Connector.hpp`), which handles sending the current move history to Stockfish and receiving the best move suggestion. The move is then animated step by step to simulate real gameplay.

The main game loop follows a standard design: event polling, input handling, game state updates, AI processing, and rendering. This ensures smooth and responsive gameplay while maintaining synchronization between the user interface and the AI engine.



# Challenges
- Configuring SFML with C++ compilers required careful linking of dependencies.
- Ensuring that pieces snapped precisely onto squares demanded accurate coordinate rounding.
- Communicating with Stockfish via UCI required trial and error to correctly send and parse commands.
- Smooth animations for opponent moves had to be implemented without breaking the event loop.




## 🏆 Conclusion
This Chess game demonstrates the successful integration of **C++ programming, graphics rendering with SFML, and advanced AI through Stockfish**. It highlights strong problem-solving, software design, and algorithmic skills. The project balances technical depth with user-friendly design, resulting in an engaging game that feels smooth and realistic. It serves as both a learning milestone in C++ development and a solid portfolio piece showcasing expertise in **game development, AI integration, and graphical programming**.
