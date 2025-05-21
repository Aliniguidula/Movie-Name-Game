🎬 **Movie Name Game**

A multiplayer movie-guessing game inspired by cine2nerdle.app, built in Java.

🚀 **Project Overview**

Movie Name Game challenges players to name movies connected through shared contributors (like actors or directors), all under time pressure. It's a strategic and fast-paced game with smart indexing, clean design, and real-time performance — all built from scratch using Java.

🌟 **Key Features**
- Real-time Autocomplete: Instant suggestions while typing movie names.
- Smart Connections: Movies linked by shared actors, directors, writers, composers, or cinematographers.
- Game History Tracking: Displays previous five moves and metadata.
- Win Conditions: Players race to hit their genre-based victory goals.
- Multiplayer Mode: Alternating turns, countdown timers, and rules enforcement.

**Architecture & Design Patterns**
We employed two main software design patterns to ensure scalability and maintainability:
- Model-View-Controller (MVC): Model: Movie, MovieFlyweight, Player, GameState, MovieGraph, View: ConsoleView, TextUI, Controller: GameController, InputHandler. MVC ensures a clear separation of concerns — keeping our data logic, user interface, and interaction flow modular and maintainable.
- Flyweight Pattern: To handle a large dataset efficiently, we implemented the Flyweight pattern: MovieFlyweight stores shared metadata (e.g., actors, directors), Movie objects reference a single MovieFlyweight to reduce redundancy.

🕹️ **Gameplay Mechanics**
- The game begins with a randomly selected movie.
- Players take turns naming a movie connected to the previous one.
- Each connection type (actor, director, etc.) can only be used three times per game.
- Players win by fulfilling their predefined genre-based win condition (e.g. naming 5 horror films).
- Failure to respond within 30 seconds ends the game.
