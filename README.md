# Echo-Generation-2
VR mod for Echo Generation 2




ECHO GENERATION 2 VR  v0.1.6 (test build) - Unity 6000.3.12f1, IL2CPP x64
=============================================

Install
-------
unzip to game folder, only tested with virtual desktop XR

**[Nefarius ViGEmBus](https://github.com/nefarius/ViGEmBus/releases) support - with the driver installed (ViGEmBusSetup_x64.msi in the zip) the VR
        controllers are a real virtual Xbox 360 controller ([Controls] InputMethod = Auto / ViGEm / InputSystem).**

The views - TAP R3 (right stick click) to switch
------------------------------------------------
THIRD PERSON (start) .. the game's own camera ([View] Follow = false), or following behind the player
                        ([View] Follow = true / VR menu "Third person: follow the player").
                        With the game's camera the right stick moves the game's camera like on a pad and
                        your view turns with it ([View] GameCameraRightStick).
FIRST PERSON .......... you are at the player's head (head hidden); the player's arms follow your controllers.
Tap R3 = first <-> third person.  Hold R3 (0.5 s) = the game's own R3.
Battles stay in your view ([View] GameCameraInBattles2 = true puts them on the game's camera). The game's camera
scenes always use the game's camera ([View] GameCameraInScenes); your view comes back afterwards.

Battles in first person (card battles)
--------------------------------------
  - HP floats over every fighter's head: party green, enemies red (shield shown as +N)
    [HandHud] HpBarsOverParty, HpBarsOverEnemies, HpBarSize, HpBarHeight; the game's own bars are hidden  [HandHud] HideGameHpBars
  - LEFT controller: your hand of cards                [HandHud] LeftCardsPosition / LeftCardsWidth
  - RIGHT controller: the portrait panel (whose turn / actions left), deck / discard / play counts
                                                     [HandHud] RightPortraitPosition / RightPortraitWidth
  - RIGHT controller, beside it: the timed attack / block icon         [HandHud] TimedHitOnRightHand, TimedHitPosition
  - choosing a target: the game's target arrow floats under that fighter's HP bar   [HandHud] TargetTriangleUnderHp
  VR menu -> "Battles (first person)".

Cheats (VR settings menu -> Cheats, both ON by default)
----------------------------------------------------
Unlimited HP ... card battles: damage to your party is 0 and its HP stays full; real-time fights: your HP stays
                 full.                                 [Cheats] UnlimitedHP
Unlimited SP ... your party's skill points are not spent and stay at their maximum.   [Cheats] UnlimitedSP

Controls (the VR controllers are an Xbox pad)
--------
  triggers = LT / RT, grips = LB / RB, A B X Y, left stick = move, stick clicks = L3 / R3
  Right stick left / right ..... turn (first person / follow); moves the game's camera (game camera view)
  A + B together ............... Start
  X + Y together ............... Back
  Tap both stick clicks ........ re-centre the view
  Hold both stick clicks 1.2 s . VR settings menu (right stick = choose / change, A = select, B = close)

Please send BepInEx/LogOutput.log after a first try. Useful lines:
  "VR controllers reach the game through: ..."       (ViGEm or XInput)
  "Virtual Xbox controller (XInput): the game asked ..."  (only without ViGEm)
  "Game camera: ...", "Player: ... head ..."         (for first person)
  "Player arms (...)": left ... right ...             (for the arms)
  "Cheat patches: 3 ok", "Unlimited HP: ...", "Unlimited SP: ..."
  "Battle HUD on the hands: ...", "HP bar over ...", "Target arrow: ...", "Timed attack / block icon: ..."
  "Pause menu open", "Battle started", "View: ..."
Disable: to disable Mod rename winhttp.dll to winhttp.dll.bak

[VR Mod Manager](https://github.com/King-EJ/VR-Mod-Manager/releases/tag/VRModManager)

LICENSES
-
Uses Astien's OpenXR bridge. Free, non-commercial.
