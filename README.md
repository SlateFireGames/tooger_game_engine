![Tooger HTML Game Engine Logo](assets/tooger_game_engine_logo.png)

# Tooger HTML Game Engine

Welcome to **Tooger**, a lightweight 2D game engine built from scratch using HTML, JavaScript, and CSS. Designed with a DOM-based architecture, Tooger is a passion project created to explore the low-level mechanics of game development and understand the critical questions to ask when working with a game engine. Whether you're a hobbyist, a learner, or just curious, Tooger offers a simple yet insightful look into building performant 2D games in the browser.

## Why Tooger?

At 56, I built Tooger to dive deep into the nuts and bolts of game engines. My goal was to learn how each function—rendering, input handling, game loops—works and how to design features that respect an engine’s capabilities and limitations. By creating Tooger, I learned to ask the right questions, like "How does this impact performance?" or "What’s the simplest way to achieve this?" These lessons are the foundation for my future projects, where I plan to use Unreal Engine to create visually stunning and performant 2D games.

Tooger is perfect for:
- Developers who want to understand the inner workings of a game engine.
- Hobbyists looking to experiment with DOM-based game development.
- Anyone curious about building lightweight 2D games in the browser.

## Features

- **DOM-Based Rendering**: Uses HTML elements and CSS transforms for lightweight 2D visuals.
- **Custom Game Loop**: A JavaScript-driven loop optimized for smooth updates and rendering.
- **Input Handling**: Supports keyboard and mouse inputs for responsive controls.
- **Sprite Animations**: Leverages CSS for simple, performant animations.
- **Collision Detection**: Basic rectangle-based collision system for game interactions.
- **Asset Management**: Streamlined pipeline for loading images and other assets.
- **Performance Optimizations**: Minimizes DOM reflows and batches updates for better browser performance.

## Getting Started

### Prerequisites
- A modern web browser (Chrome, Firefox, Edge, etc.).
- A text editor (e.g., VS Code) for tweaking code.
- Basic knowledge of HTML, JavaScript, and CSS.

### Installation
1. **Clone the Repository**:
   ```bash
   git clone https://github.com/[YourGitHubUsername]/tooger-html-game-engine.git
   ```
2. **Navigate to the Project**:
   ```bash
   cd tooger-html-game-engine
   ```
3. **Serve the Project**:
   - Use a local server like `live-server` (available via npm) or any HTTP server.
   - Example with `live-server`:
     ```bash
     npm install -g live-server
     live-server
     ```
   - Alternatively, open `index.html` in a browser (note: some features may require a server due to CORS).

4. **Explore the Demo**:
   - Open your browser and navigate to the served URL (e.g., `http://localhost:8080`).
   - Check out the included demo game to see Tooger in action!

### Project Structure
```
tooger-html-game-engine/
├── assets/               # Images, sounds, and other game assets
├── src/                  # Core engine and game code
│   ├── engine/           # Engine modules (game loop, rendering, input, etc.)
│   ├── game/             # Demo game logic and assets
│   └── main.js           # Entry point for the engine
├── index.html            # Main HTML file
├── styles.css            # Global and game-specific styles
└── README.md             # This file
```

## Usage

To create a game with Tooger:
1. **Set Up Your Scene**:
   - Define your game world in `index.html` using HTML elements with specific classes (e.g., `.sprite` for game objects).
   - Style elements in `styles.css` using CSS transforms for positioning and animations.

2. **Add Game Logic**:
   - Extend the demo in `src/game/` or create new scripts.
   - Use the engine’s APIs (e.g., `Tooger.GameLoop`, `Tooger.Input`, `Tooger.Collision`) to handle updates, inputs, and interactions.

3. **Optimize for Performance**:
   - Minimize DOM manipulations by batching updates.
   - Use CSS transforms for animations to avoid reflows.
   - Check the `src/engine/` modules for examples of optimization techniques.

Example snippet for a simple sprite movement:
```javascript
// In src/game/player.js
const player = document.querySelector('.player');
Tooger.Input.onKeyDown('ArrowRight', () => {
  player.style.transform = `translateX(${player.offsetLeft + 10}px)`;
});
```

## Learning from Tooger

Tooger was built to answer questions like:
- How do you balance feature complexity with performance?
- What’s the most efficient way to render sprites in the DOM?
- How do engine limitations shape game design?

By exploring the code, you’ll see how I tackled these questions through:
- **Minimal DOM Updates**: Batching changes to reduce browser reflows.
- **CSS-Driven Animations**: Using transforms for smooth, GPU-accelerated visuals.
- **Modular Design**: Keeping the engine flexible for experimentation.

## Future Plans

Tooger is a stepping stone. My next goal is to leverage Unreal Engine’s Paper2D to create 2D games that are visually rich and highly performant. The questions I’ve learned to ask—about optimization, architecture, and trade-offs—will guide me in building games that stand out. Stay tuned for updates on my journey!

## Contributing

I’d love for the community to explore and expand Tooger! To contribute:
1. Fork the repository.
2. Create a branch (`git checkout -b feature/your-feature`).
3. Commit your changes (`git commit -m "Add your feature"`).
4. Push to your branch (`git push origin feature/your-feature`).
5. Open a Pull Request.

Please include a description of your changes and how they align with Tooger’s goals.

## Resources

To dive deeper into DOM-based game development:
- [MDN Web Docs](https://developer.mozilla.org/) for HTML, CSS, and JavaScript fundamentals.
- [Learn OpenGL](https://learnopengl.com/) for graphics programming concepts (even if Tooger uses the DOM).
- [GameDev.net](https://www.gamedev.net/) for game development discussions.
- YouTube channels like [Benny Box](https://www.youtube.com/user/BennyBox) for engine-building inspiration.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contact

Got questions or ideas? Reach out:
- GitHub: SlateFireGames(https://github.com/SlateFireGames)
- Email: [support@slatefire.com]
- YouTube: [(https://www.youtube.com/@SlateFireGames)]

Thanks for checking out Tooger! Happy coding, and I hope this engine sparks your curiosity about game development, just like it did for me.
