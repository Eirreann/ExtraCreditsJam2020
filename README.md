# *Markets of Freedonia* (Extra Credits Game Jam 2020)

A 2D survival game made in three days for the Extra Credits Game Jam #6 (2020, theme: "Take Care"), in Unity 2020.1 with a team of four. I was one of two programmers, and co-designed the gameplay and UI.

In *Markets of Freedonia* you play as a resident of the fictional nation of Freedonia at the close of the Great War and the beginning of the Spanish flu epidemic. You must go to the store every day to feed your family, while avoiding illness to the best of your ability by observing social distancing.

Play it in your browser or download it [on itch.io](https://reaperscarl.itch.io/market-of-freedonia), or read more on the [*Markets of Freedonia* page on my website](https://iain-skaggs.com/market-of-freedonia-extra-credits-game-jam-2020).

This repo is my fork of [Francesco Scarlata's original repository](https://github.com/FrancescoScarlata/ExtraCreditsJam2020).

## Contents

- `ECJ20_GameToBeNamed`: the Unity project (Unity 2020.1.2f1, with URP, Cinemachine, TextMesh Pro, and the FMOD for Unity integration).
- `ECJ20_FmodProject`: the FMOD Studio project for the game's music and sound effects.

## In the code

My code is in `ECJ20_GameToBeNamed/Assets/Main/Scripts`:
- `UserInterface/UIManager`: screen fades, the pause menu, and scene loading for starting, restarting, and quitting the game.
- `GameManager` (`UpdateState`) and `Events`: running and paused game states, broadcast through a UnityEvent so the UI can react to them.
- `GameOver`: the game-over scene, which shows one of three endings depending on how many of the family survive.
- `Player/PlayerController`: player movement and interaction input. Francesco later added animation and handling for overlapping interactables.
- `Player/SimpleCameraFollow`: a smoothed camera follow, used in the movement test scenes.

I also built the main menu with its premise screen (`Assets/Main/Scenes/00_MainMenu`) and the game-over scene (`02_GameOver`).

## Opening the project

- Open `ECJ20_GameToBeNamed` in Unity Hub with Unity 2020.1.2f1, available from [Unity's download archive](https://unity.com/releases/editor/archive), and play from `Assets/Main/Scenes/_LoadingScene`, the first scene in the build.
- The built FMOD banks are included in `Assets/StreamingAssets`, so the game's audio plays without FMOD Studio. To edit the audio, open `ECJ20_FmodProject` in FMOD Studio (the project was saved in version 2.00).

## A note on the code

This is three-day jam code, written in August 2020, before I began working professionally as a Unity developer. It was also my first team project using git. For more recent examples of my work, see my GMTK Game Jam repos: [2024](https://github.com/Eirreann/GMTK_GameJam_2024), [2025](https://github.com/Eirreann/GMTK_GameJam_2025), and [2026](https://github.com/Eirreann/GMTK_GameJam_2026).

## Team

- Francesco Scarlata (ReaperScarl): design and programming
- Abhilash: art
- ClarrisGaming: music and sound effects