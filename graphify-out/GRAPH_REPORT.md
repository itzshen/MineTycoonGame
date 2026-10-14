# Graph Report - progMethFinalProject  (2026-10-15)

## Corpus Check
- 77 files · ~189,197 words
- Verdict: corpus is large enough that graph structure adds value.
- Unclassified: 9 file(s) not represented in the graph (top: .bat 2, .jar 2, .fxml 2)

## Summary
- 524 nodes · 1006 edges · 55 communities (14 shown, 41 thin omitted)
- Extraction: 87% EXTRACTED · 13% INFERRED · 0% AMBIGUOUS · INFERRED: 130 edges (avg confidence: 0.85)
- Token cost: 0 input · 0 output

## Community Hubs (Navigation)
- Game Logic & Unit Testing
- UI Frameworks & Machine Definitions
- FX Controller & Media Management
- Game Concept & Manual
- Renderer & Grid System
- Game Loop & Lifecycle
- Input & Camera Management
- Machine Factory Methods
- Launcher & Main Entry
- Dropper Logic & Item Types
- Base Machine Logic
- Conveyor Belt Mechanics
- Directional Mechanics
- Furnace Mechanics & Bank
- Core Component Registry
- Machine Interfaces
- UI Machine State
- Game Constants
- Machine Assets
- Environment Assets
- Iron Dropper
- Sapphire Dropper
- Upgrade Machine 5
- Background Assets
- Copper Resource
- Gold Processing
- Upgrade Machine 3
- Shell Scripts
- Sapphire Icon
- Coal Sprite
- Diamond Sprite
- Emerald Sprite
- Gold Sprite
- Iron Sprite
- Platinum Sprite
- Ruby Sprite
- Sapphire Sprite
- Silver Sprite
- Conveyor Sprite
- Coal Dropper Sprite
- Copper Processing Sprite
- Diamond Processing Sprite
- Emerald Processing Sprite
- Iron Dropper Sprite
- Platinum Processing Sprite
- Ruby Processing Sprite
- Silver Dropper Sprite
- Upgrade Machine 1
- Upgrade Machine 2
- Upgrade Machine 5
- Shop UI
- Sound Manager

## God Nodes (most connected - your core abstractions)
1. `MachineType` - 55 edges
2. `Machine` - 47 edges
3. `Direction` - 40 edges
4. `GameController` - 34 edges
5. `PlayerBank` - 32 edges
6. `PlacementManager` - 21 edges
7. `ItemType` - 20 edges
8. `ShopManager` - 18 edges
9. `GridSystem` - 17 edges
10. `Item` - 17 edges

## Surprising Connections (you probably didn't know these)
- `Mine Tycoon` --semantically_similar_to--> `Mine Tycoon`  [INFERRED] [semantically similar]
  README.md → Mine Tycoon report.pdf
- `Programming Methodology I 2110215` --semantically_similar_to--> `Programming Methodology I 2110215`  [INFERRED] [semantically similar]
  README.md → Mine Tycoon report.pdf
- `Chulalongkorn University` --semantically_similar_to--> `Chulalongkorn University`  [INFERRED] [semantically similar]
  README.md → Mine Tycoon report.pdf
- `Conveyor` --inherits--> `Machine`  [EXTRACTED]
  src/main/java/game/logic/Conveyor.java → src/main/java/game/logic/Machine.java
- `Dropper` --inherits--> `Conveyor`  [EXTRACTED]
  src/main/java/game/logic/Dropper.java → src/main/java/game/logic/Conveyor.java

## Import Cycles
- None detected.

## Hyperedges (group relationships)
- **Machinery types** — mine_tycoon_report_dropper, mine_tycoon_report_conveyor, mine_tycoon_report_upgrader, mine_tycoon_report_furnace [EXTRACTED 1.00]
- **Game screen components** — mine_tycoon_report_grid_system, mine_tycoon_report_hud, mine_tycoon_report_shop_manager, mine_tycoon_report_inventory [EXTRACTED 1.00]
- **Raw materials** — mine_tycoon_report_coal, mine_tycoon_report_copper, mine_tycoon_report_diamond, mine_tycoon_report_platinum [EXTRACTED 1.00]

## Communities (55 total, 41 thin omitted)

### Community 0 - "Game Logic & Unit Testing"
Cohesion: 0.06
Nodes (7): Upgrader, DirectionTest, DropperTest, GridSystemTest, ItemTest, PlayerBankTest, UpgraderTest

### Community 1 - "UI Frameworks & Machine Definitions"
Cohesion: 0.06
Nodes (9): MachineCategory, PROCESSING, PRODUCTION, TRANSPORT, UPGRADES, MachineType, InventoryUIBuilder, ShopManager (+1 more)

### Community 2 - "FX Controller & Media Management"
Cohesion: 0.06
Nodes (7): GameController, SoundEffect, DEPOSIT, PLACE, REMOVE, SoundManager, StartMenuController

### Community 3 - "Game Concept & Manual"
Cohesion: 0.08
Nodes (38): Chawakarn Aekanabadin, Chayanyut Kamonthitichoti, Chulalongkorn University, Coal, Conveyor Belt, Copper, Diamond, Dropper (+30 more)

### Community 5 - "Game Loop & Lifecycle"
Cohesion: 0.09
Nodes (3): GameLoopManager, AnimationTimer, InputHandler

### Community 6 - "Input & Camera Management"
Cohesion: 0.10
Nodes (5): CameraManager, PlacementManager, PlacementMode, BUILD, REMOVE

### Community 7 - "Machine Factory Methods"
Cohesion: 0.10
Nodes (11): COALDROPPER, COPPERDROPPER, DIAMONDDROPPER, EMERALDDROPPER, FURNACE, NONE, PLATINUMDROPPER, RUBYDROPPER (+3 more)

### Community 9 - "Dropper Logic & Item Types"
Cohesion: 0.10
Nodes (12): Dropper, ItemType, COAL, COPPER, DIAMOND, EMERALD, GOLD, IRON (+4 more)

### Community 10 - "Base Machine Logic"
Cohesion: 0.18
Nodes (4): Item, Machine, OutgoingTransfer, Tickable

### Community 12 - "Directional Mechanics"
Cohesion: 0.17
Nodes (7): Direction, DOWN, LEFT, RIGHT, UP, GOLDDROPPER, UP2

### Community 13 - "Furnace Mechanics & Bank"
Cohesion: 0.18
Nodes (4): Furnace, CONVEYOR, UP4, PlayerBank

### Community 14 - "Core Component Registry"
Cohesion: 0.32
Nodes (8): CameraManager, GameController, GameLoopManager, GameRenderer, InputHandler, InventoryUIBuilder, PlacementManager, ShopManager

### Community 15 - "Machine Interfaces"
Cohesion: 0.33
Nodes (6): Conveyor, Dropper, Furnace, Machine, Tickable, Upgrader

### Community 17 - "UI Machine State"
Cohesion: 0.67
Nodes (3): Machine State 4, Machine UP4 Image, UI Element Indicator

## Ambiguous Edges - Review These
- `StartMenuBackground.jpg` → `Start menu background image for game UI`  [AMBIGUOUS]
  src/main/resources/images/environment/StartMenuBackground.JPG · relation: depicts

## Knowledge Gaps
- **84 isolated node(s):** `UP`, `DOWN`, `LEFT`, `RIGHT`, `COAL` (+79 more)
  These have ≤1 connection - possible missing edges or undocumented components. (Counts symbols only; 164 node(s) total have ≤1 connection when file, concept and rationale nodes are included.)
- **41 thin communities (<3 nodes) omitted from report** — run `graphify query` to explore isolated nodes.

## Suggested Questions
_Questions this graph is uniquely positioned to answer:_

- **Why does `GameController` connect `FX Controller & Media Management` to `UI Frameworks & Machine Definitions`, `Renderer & Grid System`, `Game Loop & Lifecycle`, `Input & Camera Management`, `Furnace Mechanics & Bank`?**
  _High betweenness centrality (0.211) - this node is a cross-community bridge._
- **What connects `UP`, `DOWN`, `LEFT` to the rest of the system?**
  _84 weakly-connected nodes found - possible documentation gaps or missing edges._
- **Should `Game Logic & Unit Testing` be split into smaller, more focused modules?**
  _Cohesion score 0.06057945566286216 - nodes in this community are weakly interconnected._
- **Why does `MachineType` connect `UI Frameworks & Machine Definitions` to `Game Logic & Unit Testing`, `Renderer & Grid System`, `Input & Camera Management`, `Machine Factory Methods`, `Dropper Logic & Item Types`, `Base Machine Logic`, `Conveyor Belt Mechanics`, `Directional Mechanics`, `Furnace Mechanics & Bank`, `Iron Dropper`, `Sapphire Dropper`, `Upgrade Machine 5`?**
  _High betweenness centrality (0.137) - this node is a cross-community bridge._
- **Should `UI Frameworks & Machine Definitions` be split into smaller, more focused modules?**
  _Cohesion score 0.059887005649717516 - nodes in this community are weakly interconnected._
- **Why does `Machine` connect `Base Machine Logic` to `Game Logic & Unit Testing`, `UI Frameworks & Machine Definitions`, `Renderer & Grid System`, `Input & Camera Management`, `Machine Factory Methods`, `Conveyor Belt Mechanics`, `Directional Mechanics`, `Furnace Mechanics & Bank`, `Iron Dropper`, `Sapphire Dropper`, `Upgrade Machine 5`?**
  _High betweenness centrality (0.107) - this node is a cross-community bridge._

### Low-confidence Hints
_AMBIGUOUS edges — the extractor was unsure. Verify before acting on these._

- **What is the exact relationship between `StartMenuBackground.jpg` and `Start menu background image for game UI`?**
  _Edge tagged AMBIGUOUS (relation: depicts) - confidence is low._