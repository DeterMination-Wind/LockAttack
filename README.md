# LockAttack / 锁定攻击

[![Mindustry Mod](https://img.shields.io/badge/Mindustry-Mod-ffd37f.svg)](https://github.com/topics/mindustry-mod)

A lightweight Mindustry mod that adds **lock-on focus fire**. Press the lock key (default `L`) to lock on to an enemy unit or building under the cursor: your directly controlled unit keeps aiming at and firing on the target, and your selected command units receive an attack order through the vanilla network command path. Works on vanilla Mindustry v8 (build 154+), MindustryX and Xenon v8 clients, singleplayer and multiplayer.

一个轻量级 Mindustry 模组，提供**锁定集火**功能。按锁定键（默认 `L`）锁定鼠标指向的敌方单位或建筑：你直接控制的单位会持续瞄准并攻击目标，选中的指挥单位会通过原版网络命令路径收到攻击命令。兼容原版 Mindustry v8（build 154+）、MindustryX 与 Xenon v8 客户端，单机与多人均可用。

## Features / 功能

- **One-key lock-on / 一键锁定**：Tap `L` to lock the enemy unit or building under the cursor. / 单击 `L` 锁定鼠标指向的敌方单位或建筑。
- **Focus fire / 集火**：Your directly controlled unit is forced to aim at and fire on the locked target every frame. / 你直接控制的单位每帧强制瞄准锁定目标并开火。
- **Command units / 指挥单位**：Selected commandable units receive a one-shot attack order via `Call.commandUnits` (vanilla network path, works in multiplayer). / 选中的指挥单位通过原版 `Call.commandUnits` 网络命令路径收到一次性攻击命令（多人同样有效）。
- **Switch / unlock / 换锁与解锁**：Tap `L` on another target to switch; tap on empty ground or a friendly target to unlock; the lock drops automatically when the target dies, leaves fog, or turns friendly. / 在另一目标上按 `L` 切换锁定；点在空地或己方目标上解锁；目标死亡、进入迷雾或变为友方时自动解锁。
- **Visual feedback / 视觉反馈**：Rotating lock box, target line, and an optional target HP bar with name and health numbers (toggle in settings, on by default). / 旋转锁定框、目标连线、可选的目标血条（含名称与血量数字，设置中可开关，默认开启）。
- **Rebindable key / 可自定义键位**：The lock key is a normal game keybind, changeable in Settings → Keybinds. / 锁定键是标准游戏键位，可在 设置 → 键位 中修改。

## Controls / 操作

| Action / 操作 | Key / 按键 |
|---|---|
| Lock on to the target under the cursor / 锁定鼠标指向的目标 | `L` (rebindable / 可改) |

## Settings / 设置

- **Show locked target HP bar / 显示锁定目标血条** — toggle the HP bar above the locked target (default on / 默认开启)。

## Compatibility / 兼容性

- Mindustry v8 (build 154+), desktop and Android (the jar contains `classes.dex`).
- MindustryX and Xenon v8 clients.
- Also bundled inside [Neon](https://github.com/DeterMination-Wind/Neon) (the aggregate settings page exposes the same options).
- Does not modify any game files; pure client-side helper with vanilla network commands for units.

## Build / 构建

```powershell
# requires JDK 17 (Gradle 8.14.3 does not support JDK 25)
$env:JAVA_HOME = "C:\Program Files\Java\jdk-17"
./gradlew deploy
# output: 构建/LockAttack/LockAttack-dev.jar (dev) or build/libs/LockAttack-<version>.jar
```

## License / 许可

MIT — see [LICENSE](LICENSE).
