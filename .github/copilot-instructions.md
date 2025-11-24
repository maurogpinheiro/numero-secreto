# Copilot Instructions for AI Coding Agents

## Project Overview
This is a simple web-based number guessing game, used in Alura's programming logic courses. The main gameplay is implemented in `app.js`, with supporting files for UI and assets. There is also a legacy version in `img/JS Game_files/app.js`.

## Key Files & Structure
- `index.html`: Main entry point. Loads `app.js` and `style.css`. Uses ResponsiveVoice for speech feedback.
- `app.js`: Implements the game logic, including random number generation, input handling, and UI updates.
- `style.css`: Main styles for the game UI, including background images and layout.
- `img/`: Contains images and a legacy game version (`JS Game.html`, `JS Game_files/`).
- `README.md`: Brief project description and credits.

## Game Logic Patterns
- The secret number is randomly generated between 1 and 50, ensuring no repeats until all numbers are used.
- User input is handled via an `<input>` field and checked with the `verificarChute()` function.
- Feedback is provided both visually (DOM updates) and via speech (ResponsiveVoice).
- The game can be restarted with the `reiniciarJogo()` function, which resets state and disables the restart button until the next win.

## UI & Assets
- Uses Google Fonts and custom images (`img/ia.png`, `img/code.png`, `img/Ruido.png`).
- Backgrounds and overlays are managed in CSS, with some opacity effects.
- The main image and layout are defined in `index.html` and styled in `style.css`.

## Developer Workflows
- No build or test scripts; development is direct HTML/CSS/JS editing.
- For live preview, use a static server (e.g., VS Code Live Server extension).
- No package manager or external dependencies beyond ResponsiveVoice (loaded via CDN).

## Conventions & Patterns
- All game state is managed in global JS variables.
- DOM manipulation is done via `document.querySelector` and direct property updates.
- Speech feedback is always triggered on UI updates via `responsiveVoice.speak`.
- Legacy code in `img/JS Game_files/app.js` is not used in the main game, but can be referenced for alternate logic.

## Integration Points
- ResponsiveVoice is required for speech feedback; ensure CDN is loaded in `index.html`.
- All assets are referenced with relative paths; check `img/` for images.

## Example: Adding a New Feature
To add a new hint system:
- Update `app.js` to add a hint function.
- Add a new button in `index.html` and style in `style.css`.
- Use `exibirTextoNaTela` to show hints and trigger speech.

---
If any section is unclear or missing, please provide feedback so instructions can be improved for future AI agents.
