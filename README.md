# QuestPath

QuestPath is a simple path-based quest plugin for Paper/Spigot servers.  
It lets you create your own main quest line and side quests through `config.yml`, with a clean GUI and optional economy rewards.

> This repository only distributes the compiled JAR.  
> The source code is not published.

## Download

- Go to the **Releases** section and download the latest `QuestPath-x.x.x.jar`.
- Drop the JAR into your server’s `plugins` folder.
- Start the server to generate the default `config.yml`.

## Features

- Linear **main quest path** (step-by-step progression)
- Optional random **side quests**
- Built-in quest types:
  - Mine blocks
  - Craft items
  - Kill entities
  - Visit dimensions
  - Obtain items
  - Travel distance
- Inventory GUI:
  - Current main quest
  - Current side quest
  - Paginated list of completed main quests
- Fully configurable quests in `config.yml`
- Optional Vault economy rewards (global or per quest)
- Admin reset command for player progress

## Commands

- `/quest` – open the quest GUI
- `/getsidequest` – get or reroll a side quest
- `/questreset <player>` – reset a player’s quest progress (`questpath.admin`)

## Requirements

- Paper or Spigot 1.20.X - 1.21.X
- Java 21+  
- (Optional) Vault + an economy plugin for money rewards

## Configuration

On first run, a minimal `config.yml` is generated with no active quests and a commented example section.  
Server owners can copy and edit the examples to create their own quest lines.

## Credits

- Developed by **Moslipper**
- Plugin: **QuestPath** for **ColonyMC** and other servers

Example:

```yaml
economy:
  enabled: true
  # Fallback rewards if a quest has no reward-money set
  reward-main-complete: 50.0
  reward-side-complete: 25.0

quests:
  main:
    - id: "TUTORIAL_1_GET_LOG"
      type: "MINE_BLOCK"
      display: "Punch a tree"
      description: "Mine 1 log from any tree."
      target-block: "ANY_LOG"
      amount: 1
      reward-money: 10.0

    - id: "TUTORIAL_2_CRAFT_TABLE"
      type: "CRAFT_ITEM"
      display: "Crafting Time"
      description: "Craft a crafting table."
      target-item: "CRAFTING_TABLE"
      amount: 1
      reward-money: 15.0

    - id: "TUTORIAL_3_KILL_ZOMBIES"
      type: "KILL_ENTITY"
      display: "First Blood"
      description: "Kill 5 zombies."
      target-entity: "ZOMBIE"
      amount: 5
      reward-money: 20.0

    - id: "TUTORIAL_4_VISIT_NETHER"
      type: "VISIT_DIMENSION"
      display: "Into the Nether"
      description: "Enter the Nether dimension."
      target-world: "NETHER"
      amount: 1
      reward-money: 25.0

    - id: "TUTORIAL_5_GET_IRON"
      type: "OBTAIN_ITEM"
      display: "Iron Collector"
      description: "Obtain 16 iron ingots."
      target-item: "IRON_INGOT"
      amount: 16
      reward-money: 30.0

    - id: "TUTORIAL_6_TRAVEL_500"
      type: "TRAVEL_DISTANCE"
      display: "Explorer"
      description: "Travel 500 blocks on foot."
      amount: 500
      reward-money: 40.0

  side:
    - id: "PVE_KILL_50_ZOMBIES"
      type: "KILL_ENTITY"
      display: "Zombie Cleanup"
      description: "Kill 50 zombies."
      target-entity: "ZOMBIE"
      amount: 50
      reward-money: 35.0

    - id: "PVE_KILL_20_SKELETONS"
      type: "KILL_ENTITY"
      display: "Bone Collector"
      description: "Kill 20 skeletons."
      target-entity: "SKELETON"
      amount: 20
      reward-money: 25.0

