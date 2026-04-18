# Tourist Trophy PCSX2 patch

Fixes Tourist Trophy's notorious broken license tests, ability to save replays of affected license tests, and the Replay Theater's built-in demos
while playing the game on the PCSX2 emulator.

## Tourist Trophy on PCSX2 needs your help! You can submit your best replays here to further improve the patch.
#### Submit an issue on this repo and attach your saved replay.
#### It's recommended to use a folder memory card on PCSX2 to make it easier to get your replay.
#### Required: ALL PCSX2 Advanced settings (Rounding, clamping, etc.) MUST BE LEFT ON DEFAULT SETTINGS!


## What's the fix?

The replays and demonstrations are particularly sensitive to differences in floating point calculations, which throw off the replay's playback in-game.
When playing on PCSX2, they suffer from various issues including:
Game freezes upon loading (file size of it gets wildly mis-calculated)
Replays are considered corrupted and will not be allowed to load
Saving a replay results in a wild mis-calculation of the file size and unable to save
Demonstrations fail to load / repeatedly restart
Demonstrations desynchronize (inaccurate playback)

By recording new replays on PCSX2, and modifying the game to replace the on-disc replays and demonstrations,
we can eliminate the issue for PCSX2 players.

The patch consists of new, PCSX2-based recordings.

See the charts below for the current state of the patch:

Licenses:
|   USA SCUS-97502      | Playable | Demo Functional | Demo by:     |
|-----------------------|-----------|-----------------|-------------|
| N-1                   | ✅ | ✅           | Original OK |
| N-2                   | ✅ | ✅           | Original OK |
| N-3                   | ✅ | ✅           | Original OK |
| N-4                   | ✅ | ✅           | Original OK |
| N-5                   | ✅ | ✅           | Original OK |
| N-6                   | ✅ | ✅           | Original OK |
| N-7                   | ✅ | ✅           | Original OK |
| N-8                   | ✅ | ✅           | Original OK |
| N-9                   | ✅ | ✅           | 0'34.931 by Silentwarior112 |
| N-10                  | ✅ | ✅           | 0'46.168 by Silentwarior112 |
| J-1                   | ✅ | ✅           | Original OK |
| J-2                   | ✅ | ✅           | 0'23.382 by Silentwarior112 |
| J-3                   | ✅ | ✅           | Original OK |
| J-4                   | ✅ | ✅           | Original OK |
| J-5                   | ✅ | ✅           | 0'17.137 by Silentwarior112 |
| J-6                   | ✅ | ✅           | Original OK |
| J-7                   | ✅ | ✅           | Original OK |
| J-8                   | ✅ | ✅           | 0'27.204 by Silentwarior112 |
| J-9                   | ✅ | ✅           | Original OK |
| J-10                  | ✅ | ✅           | 1'23.177 by Silentwarior112 |
| E-1                   | ✅ | ✅           | 0'23.088 by Silentwarior112 |
| E-2                   | ✅ | ✅           | 0'17.269 by Silentwarior112 |
| E-3                   | ✅ | ✅           | Original OK |
| E-4                   | ✅ | ✅           | 0'25.245 by Silentwarior112 |
| E-5                   | ✅ | ✅           | 0'22.345 by Silentwarior112 |
| E-6                   | ✅ | ✅           | 0'21.891 by Silentwarior112 |
| E-7                   | ✅ | ✅           | 0'48.151 by Silentwarior112 |
| E-8                   | ✅ | ✅           | 0'34.289 by Silentwarior112 |
| E-9                   | ✅ | ✅           | Original OK |
| E-10                  | ✅ | ✅           | 1'30.365 by Silentwarior112 |
| S-1                   | ✅ | Desync issue | Needs new replay ❌️ |
| S-2                   | ✅ | Desync issue | Needs new replay ❌️ |
| S-3                   | ✅ | Desync issue | Needs new replay ❌️ |
| S-4                   | ✅ | Desync issue | Needs new replay ❌️ |
| S-5                   | ✅ | Desync issue | Needs new replay ❌️ |
| S-6                   | ✅ | Desync issue | Needs new replay ❌️ |
| S-7                   | ✅ | Desync issue | Needs new replay ❌️ |
| S-8                   | ✅ | Desync issue | Needs new replay ❌️ |
| S-9                   | ✅ | Desync issue | Needs new replay ❌️ |
| S-10                  | ✅ | Desync issue | Needs new replay ❌️ |

|   Europe SCES-53372   | Playable | Demo Functional | Demo by:     |
|-----------------------|-----------|-----------------|-------------|
| N-1                   | ✅ | ✅           | Original OK |
| N-2                   | ✅ | Desync issue | Needs new replay ❌️ |
| N-3                   | ✅ | ✅           | Original OK |
| N-4                   | ✅ | ✅           | Original OK |
| N-5                   | ✅ | ✅           | Original OK |
| N-6                   | ✅ | ✅           | Original OK |
| N-7                   | ✅ | Desync issue | Needs new replay ❌️ |
| N-8                   | ✅ | ✅           | Original OK |
| N-9                   | ✅ | Desync issue | Needs new replay ❌️ |
| N-10                  | ✅ | Desync issue | Needs new replay ❌️ |
| J-1                   | ✅ | ✅           | Original OK |
| J-2                   | ✅ | ✅           | Original OK |
| J-3                   | ✅ | ✅           | Original OK |
| J-4                   | ✅ | ✅           | Original OK |
| J-5                   | ✅ | ✅           | Original OK |
| J-6                   | ✅ | ✅           | Original OK |
| J-7                   | ✅ | ✅           | Original OK |
| J-8                   | ✅ | Desync issue | Needs new replay ❌️ |
| J-9                   | ✅ | ✅           | Original OK |
| J-10                  | ✅ | Desync issue | Needs new replay ❌️ |
| E-1                   | ✅ | Desync issue | Needs new replay ❌️ |
| E-2                   | ✅ | ✅           | Original OK |
| E-3                   | ✅ | ✅           | Original OK |
| E-4                   | ✅ | Desync issue | Needs new replay ❌️ |
| E-5                   | ✅ | Desync issue | Needs new replay ❌️ |
| E-6                   | ✅ | ✅           | Original OK |
| E-7                   | ✅ | Desync issue | Needs new replay ❌️ |
| E-8                   | ✅ | Desync issue | Needs new replay ❌️ |
| E-9                   | ✅ | Desync issue | Needs new replay ❌️ |
| E-10                  | ✅ | Desync issue | Needs new replay ❌️ |
| S-1                   | ✅ | Desync issue | Needs new replay ❌️ |
| S-2                   | ✅ | Desync issue | Needs new replay ❌️ |
| S-3                   | ✅ | Desync issue | Needs new replay ❌️ |
| S-4                   | ✅ | Desync issue | Needs new replay ❌️ |
| S-5                   | ✅ | Desync issue | Needs new replay ❌️ |
| S-6                   | ✅ | Desync issue | Needs new replay ❌️ |
| S-7                   | ✅ | Desync issue | Needs new replay ❌️ |
| S-8                   | ✅ | Desync issue | Needs new replay ❌️ |
| S-9                   | ✅ | Desync issue | Needs new replay ❌️ |
| S-10                  | ✅ | Desync issue | Needs new replay ❌️ |

|   Japan SCPS-15105   | Playable | Demo Functional | Demo by:     |
|-----------------------|-----------|-----------------|-------------|
| Not available yet                   |  |            |  |
