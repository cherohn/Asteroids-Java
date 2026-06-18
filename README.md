# Asteroids — Java

A faithful recreation of the classic Asteroids arcade game in Java, built with a custom game loop, real-time collision detection, and object-oriented design.

---

## Gameplay

- Control a spaceship and destroy asteroids before they hit you
- Asteroids split into smaller pieces when shot
- Game speed increases progressively
- Score tracking and lives system

---

## Tech Stack

| Layer | Technology |
|---|---|
| Language | Java 21 |
| Rendering | JavaFX / Java2D |
| Architecture | OOP — each entity is its own class |
| Build | Maven |

---

## Architecture

Each game entity is an independent object responsible for its own state and rendering:

```
GameLoop
  ├── Spaceship     → player movement, rotation, shooting
  ├── Asteroid[]    → movement, size variants, split logic
  ├── Bullet[]      → trajectory, lifetime, collision
  └── CollisionManager → detects hits between all entities
```

The game loop runs on a fixed timestep, separating update logic from rendering — which keeps physics consistent regardless of frame rate.

---

## Running Locally

**Requirements:** Java 21+, Maven 3.8+

```bash
git clone https://github.com/cherohn/Asteroids-Java.git
cd Asteroids-Java
mvn clean compile exec:java
```

---

## Author

**Matheus Garcez** — [github.com/cherohn](https://github.com/cherohn)
