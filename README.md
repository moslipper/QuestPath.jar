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

- Paper or Spigot 1.21+  
- Java 17+  
- (Optional) Vault + an economy plugin for money rewards

## Configuration

On first run, a minimal `config.yml` is generated with no active quests and a commented example section.  
Server owners can copy and edit the examples to create their own quest lines.

## Credits

- Developed by **Moslipper**
- Plugin: **QuestPath** for **ColonyMC** and other servers
