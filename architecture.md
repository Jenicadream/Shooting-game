# Architecture

## Platform Constraints
- The project must run in the p5.js web editor (browser-based).
- Only JavaScript and p5.js can be used.
- No external libraries.
- Code must be able to run in a single sketch.js file.

## File Structure
- PRD.md
- architecture.md
- tasks.md
- rules.md
- memory.md
- BUILD/
  - sketch.js (main game file)
  - index.html (optional template)
  - style.css (optional)

## Main Components

### Player
- Positioned at bottom of screen
- Moves left and right only
- Shoots bullets upward

### Bullets
- Spawn from player position
- Move upward
- Destroy balls on collision

### Balls (Enemies)
- Spawn at top of screen
- Fall downward
- Some move side to side
- Some require multiple hits

### Score System
- Score increases when a ball is destroyed
- High score tracked

### Game States
- Start screen
- Playing
- Game Over

### Difficulty System
- Every 15 seconds:
  - Increase fall speed
  - Increase spawn rate
  - Increase randomness
  - Introduce larger balls

## Coding Approach
- Use objects/classes for:
  - Balls
  - Bullets
  - Player (if needed)
- Keep logic inside draw() loop for updates
