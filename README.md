# Mine Tycoon

A 2D factory game built with **Java 17** and **JavaFX**. Buy machines, place them on a grid, and build production lines that carry ores from Droppers through Conveyors and Upgraders into a Furnace, which sells them for money.

Final project for Programming Methodology I (2110215), Chulalongkorn University.
Full write-up: `Mine Tycoon report.pdf` · UML diagrams: `UML_LOGIC.png`, `UML_UI.png`

---

## How to Play

1. Click **Play Game** on the start menu.
2. Open the **Shop** (`E`) and buy machines with your starting money.
3. Open the **Inventory** (`B`), pick a machine, and click the grid to place it.
4. Build a line: **Dropper → Conveyors → Upgraders → Furnace**.
5. Spend the money you earn on more machines.

Items move one cell every 0.5 seconds.

### Controls

| Key / Input | Action |
|---|---|
| `E` | Open / close the Shop |
| `B` | Open / close the Inventory |
| `1` / `2` | Build mode / Remove mode |
| `R` | Rotate the machine you are placing (Inventory must be open) |
| `W` `A` `S` `D` | Move the camera |
| Mouse wheel | Zoom |
| Left click | Place or remove a machine |

Removing a machine returns it to your inventory.

### Machines

| Machine | What it does |
|---|---|
| **Dropper** | Spawns ore. One Dropper for each of the 10 ores: Coal, Copper, Iron, Silver, Gold, Platinum, Diamond, Emerald, Ruby, Sapphire |
| **Conveyor** | Moves items one cell forward |
| **Upgrader** | Multiplies an item's value (5 tiers, `UP1`–`UP5`) |
| **Furnace** | Turns an item into money |

---

## Run the Game

You only need **Java 17**. JavaFX is already bundled in the jar.

- **Windows:** double-click `TycoonGame.bat` (keep it in the same folder as `TycoonGame.jar`)
- **macOS:** run `./TycoonGame.sh`
- **Terminal:** `java -jar TycoonGame.jar`

The jar supports Windows and macOS.

## Build from Source

```sh
./gradlew clean shadowJar     # use gradlew.bat on Windows
```

The jar is created at `build/libs/TycoonGame.jar`.
Other useful commands: `./gradlew run` (start the game) and `./gradlew test` (run tests).

---

## Project Structure

```
src/main/java/game/
├── Main, Launcher       Entry points
├── logic/               Game rules (no JavaFX)
│   ├── GridSystem       The grid and the tick
│   ├── Machine          Abstract base class
│   ├── Conveyor, Dropper, Upgrader, Furnace
│   └── Item, ItemType, MachineType, PlayerBank, ...
└── ui/                  JavaFX screens and controls
    ├── GameController   Connects everything together
    ├── GameRenderer     Draws the grid and machines
    ├── ShopManager, PlacementManager, InputHandler, ...
    └── sound/           Music and sound effects
```

The **logic** package knows nothing about JavaFX, so it can be tested on its own. The **ui** package only draws and handles input.

---

## Design Notes

**Inheritance.** `Machine` is an abstract class that holds what every machine shares (position, direction, the item it holds). `Furnace` and `Conveyor` extend it. `Dropper` and `Upgrader` extend `Conveyor`, since they move items like a conveyor and only add one extra behaviour: spawning an item or boosting its value.

**Interface.** `Machine` implements `Tickable`, a small interface that says "I can be updated every game tick".

**Polymorphism.** `GridSystem` loops over every machine and calls the same methods without knowing the exact type. Each machine reacts in its own way.

**Encapsulation.** Fields are `private` or `protected`. Methods that change a machine's item are package-private, so only `GridSystem` can use them.

**Fair ticks.** Each tick has two steps: machines first say where they want to move, then `GridSystem` settles any conflicts and moves the items. This way an item never moves more than one cell per tick.

---

## Tests

JUnit 5 tests cover the logic package: `GridSystem`, `PlayerBank`, `Item`, `Upgrader`, `Dropper` and `Direction`. UI classes are not tested because they need JavaFX running.

```sh
./gradlew test
```

---

Final project for Programming Methodology I (2110215), Department of Computer Engineering, Chulalongkorn University.