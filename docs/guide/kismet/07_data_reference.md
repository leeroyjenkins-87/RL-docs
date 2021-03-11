---
title: Kismet Data Reference
---
# Kismet Data reference

This is an attempt to get all data / variables you can get in kismet in one place. 90% (or more) isn't tested if it works, for now it's enough if it is out there and then the testing can begin.

Types of values in this file:

:::details WorldInfo
## WorldInfo
(WorldInfo -> )

+ Time limit:
	- Property Name: Game -> TimeLimit
	- Does This Work?: Unknown
+ Map name:
	- Property Name:  Title (set in worldinfo in UDK)
	- Does This Work?: Yes
+ Person Who Made The mMap:
	- Property Name: Author (set in worldinfo in UDK)
	- Does This Work?: Yes
+ Mapinfo `MapInfo`:
	- Property Name: MyMapInfo
	- Does This Work?: Unknown
+ Player's computer name
	- Var Type: `string`:
	- Property Name: ComputerName
	- Does This Work?: Yes
+ Time since level began play (IS paused when the game is paused, and IS dilated/clamped)
	- Var Type: `Float (seconds)`
	- Property Name: TimeSeconds
	- Does This Work?: Yes
+ Time since level began play (is NOT paused when the game is paused, and is NOT dilated/clamped)
	- Var Type: `Float (seconds)`
	- Property Name: RealTimeSeconds
	- Does This Work?: Unknown
+ Next url (url of what?)
	- Var Type: `string`: (???)
	- Property Name: NextURL
	- Does This Work?: Unknown
+ Local url (file path?)
	- Var Type: `string`: (???)
	- Property Name: LocalURL	- Does This Work?: Unknown
+ Server type
	- Var Type: `string`: (???)
	- Property Name: NetMode
	- Does This Work?: Unknown
+ Demo build (???) 
	- Var Type: `Bool`:
	- Property Name: bIsDemoBuild
	- Does This Work?: Unknown
+ Game speed (???)---
title: Kismet Data Reference
---
# Kismet Data reference

This is an attempt to get all data / variables you can get in kismet in one place. 90% (or more) isn't tested if it works, for now it's enough if it is out there and then the testing can begin.

Types of values in this file:

## WorldInfo
(WorldInfo ->)

+ Time limit:
	- Property Name: Game -> TimeLimit
	- Does This Work?: Unknown
+ Map name:
	- Property Name:  Title (set in worldinfo in UDK)
	- Does This Work?: Yes
+ Person Who Made The mMap:
	- Property Name: Author (set in worldinfo in UDK)
	- Does This Work?: Yes
+ Mapinfo `MapInfo`:
	- Property Name: MyMapInfo
	- Does This Work?: Unknown
+ Player's computer name
	- Var Type: `string`:
	- Property Name: ComputerName
	- Does This Work?: Yes
+ Time since level began play (IS paused when the game is paused, and IS dilated/clamped)
	- Var Type: `Float (seconds)`
	- Property Name: TimeSeconds
	- Does This Work?: Yes
+ Time since level began play (is NOT paused when the game is paused, and is NOT dilated/clamped)
	- Var Type: `Float (seconds)`
	- Property Name: RealTimeSeconds
	- Does This Work?: Unknown
+ Next url (url of what?)
	- Var Type: `string`: (???)
	- Property Name: NextURL
	- Does This Work?: Unknown
+ Local url (file path?)
	- Var Type: `string`: (???)
	- Property Name: LocalURL
	- Does This Work?: Unknown
+ Server type
	- Var Type: `string`: (???)
	- Property Name: NetMode
	- Does This Work?: Unknown
+ Demo build (???) 
	- Var Type: `Bool`:
	- Property Name: bIsDemoBuild
	- Does This Work?: Unknown
+ Game speed (???)
	- Var Type: `???`
	- Property Name: TimeDilation
	- Does This Work?: Unknown
+ Player who paused the match (if match is paused)
	- Var Type: `???`
	- Property Name: WI -> Pauser
	- Does This Work?: Unknown (returns PRI?)
+ Number of players
	- Var Type: `???`
	- Property Name: Game -> NumPlayers
	- Does This Work?: Unknown
+ Number of bots
	- Var Type: `???`
	- Property Name: Game -> NumBots
	- Does This Work?: Unknown
+ Only update players 
	- Var Type: `Bool`:
	- Property Name: bPlayersOnly
	- Does This Work?: Unknown
+ Score needed to end match
	- Var Type: `Int`
	- Property Name: Game -> GoalScore
	- Does This Work?: Unknown
+ Time limit
	- Var Type `Int (minutes)`:
	- Property Name: Game -> TimeLimit
	- Does This Work?: Unknown
+ Menu level 
	- Var Type: `Bool`:
	- Property Name: bIsMenuLevel
	- Does This Work?: Unknown
+ StallZ (???)
	- Var Type: `???`
	- Property Name: StallZ
	- Does This Work?: Unknown
+ KillZ
	- Var Type: `???`
	- Property Name: KillZ
	- Does This Work?: Unknown
+ Maximum players
	- Var Type: `Int`
	- Property Name: Game -> MaxPlayers
	- Does This Work?: Unknown
+ Maximum spectators
	- Var Type: `Int`
	- Property Name: Game -> MaxSpectators
	- Does This Work?: Unknown
+ Players that are still travelling from another map
	- Var Type: `Int`
	- Property Name: Game -> NumTravellingPlayers
	- Does This Work?: Unknown
+ Time until match starts? :
	- Property Name: Game -> bWaitingToStartMatch
	- Does This Work?: Unknown
+ Called when something triggers on the server: brings up laoding screen and finishes all async functions (???) 
	- Var Type: `Bool`:
	- Property Name: bRequestedBlockOnAsyncLoading ((used to check connection)? => is this even usefull?)


## GRI (GameReplicationInfo)
(WorldInfo -> GRI)

(Not everything might be replicated to clients / server)
+ Game class - `class<GameInfo>`:
	- Property Name: GameClass
+ Leaderboard Id (???)
	- Var Type: `???`
	- Property Name: GameClass -> default -> ArbitratedLeaderBoardId
+ Match over 
	- Var Type: `Bool`
	- Property Name: bMatchIsOver
+ Match began 
	- Var Type: `Bool`
	- Property Name: bMatchHasBegun
+ Time limit
	- Var Type: (???)
	- Property Name: TimeLimit
+ ???
	- Var Type: `Int`
	- Property Name: GoalScore
+ ???
	- Var Type: `Int`
	- Property Name: ElapsedTime
+ ???
	- Var Type: `Int`
	- Property Name: RemainingTime
+ Winner (set at end of match)
	- Var Type: `Object`
	- Object Type: `Actor`
	- Property Name: Winner
+ ??? (???):
	- Property Name: RemainingMinute
+ List of players 
	- Var Type: `array<PRI>`
	- Property Name: PRIArray (would length return player count?)
+ List of inactive players
	- Var Type: `array<PRI>`
	- Property Name: InactivePRIArray
+ List of teams
	- Var Type: `array<TeamInfo>`
	- Property Name: Teams
+ Stop countdown 
	- Var Type: `Bool`
	- Property Name: bStopCountDown
+ Server name:
	- Var Type: `String`
	- Property Name: ServerName (if workshop maps are ever on a server)
+ Match is team game 
	- Var Type: `Bool`
	- Property Name: GameClass -> default -> bTeamGame
	- Does This Work?: Unknown



## PRI (PlayerReplicationInfo)
(WorldInfo -> GRI -> PRI)

:::tip How to Access PRI Properties in Kismet
Get Object Property (PRI) -> Get Object Property (Property Name) (picture)
:::

+ Player Name
	- Var Type: `String`
	- Property Name: PlayerName
	- Does This Work?: Yes
+ Player's Previous Name
	- Var Type: `String`
	- Property Name: OldName (client-side only)
	- Does This Work?: Unknown
+ Player Name (sanitized)
	- Var Type: `String`
	- Property Name: SanitizedPlayerName
	- Does This Work?: Unknown
+ Player Platform
	- Var Type: `String`
	- Property Name: Platform
	- Does This Work?: Yes
+ Player Car position
	- Var Type: `Vector`
	- Property Name: LastCarLocation
	- Does This Work?: Unknown 
+ Player's Car
	- Var Type: `Object`
	- Actor Class: `Car_TA`
	- Property Name: Car
	- Does This Work?: Yes
+ Player Id
	- Var Type: `String`
	- Property Name: PlayerID
		+ (UniqueID is used for identifying player)
	- Does This Work?: Yes
+ Player UniqueId -> Uid
	- Var Type: `???`
	- Property Name: UniqueId -> Uid
	- Does This Work?: Unknown
+ Player Replicated Data
	- Var Type: `PRI` (object maybe?)
	- Property Name: PREI
	- Does This Work?: Unknown
+ Player Avatar
	- Var Type: - `Object` (maybe Texture2D?)
	- Property Name: PlayerAvatar
	- Does This Work?: Unknown
+ Player banner
	- Var Type: `Object` (maybe?)
	- Property Name: PlayerBanner
	- Does This Work?: Unknown
+ Player Camera
	- Var Type: `Object`
	- Actor Class: `CameraSettingsActor_TA`
	- Property Name: Camera
	- Does This Work?: Unknown
+ Player Title
	- Var Type: `String`
	- Property Name: Title
	- Does This Work?: Unknown
+ Player Team - `TeamInfo`
	- Property Name: Team
		+ Team Index
			- Var Type: `Int`
			- Property Name: TeamIndex
			- Does This Work?: Yes
		+ Team Name
			- Var Type: `String`
			- Property Name: CustomTeamName
			- Does This Work?: Yes
		+ Team Sanitized name
			- Var Type: `String`
			- Property Name: SanitizedTeamName
			- Does This Work?: Unknown
		+ Team Size
			- Var Type: `Int`
			- Property Name: Size
			- Does This Work?: Unknown
		+ Team Members
			- `PRI_TA`
			- Property Name: Members
			- Does This Work?: Unknown
		+ Team Color
			- `color`
			- Property Name: TeamColor
			- Does This Work?: Unknown
		+ Team Logo
			- `Texture`
			- Property Name: TeamLogo
			- Does This Work?: Unknown
		+ Team Goals
			- Var Type: `Int`
			- Property Name: Score
			- Does This Work?: Yes
		+ Team Difficulty
			- Var Type: `Int`
			- Property Name: Difficulty
			- Does This Work?: Unknown
		+ Team Series goals
			- Var Type: `Int`
			- Property Name: SeriesScore
			- Does This Work?: Unknown
		+ Team Paint
			- `LoadoutTeamPaint`
			- Property Name: TeamPaint
			- Does This Work?: Unknown
		+ Team Forfeit
			- Var Type: `bool`
			- Property Name: bForfeit
			- Does This Work?: Unknown
		+ Team Custom Color
			- Var Type: `bool`
			- Property Name: bHasCustomColor
			- Does This Work?: Unknown
+ Goals
	- Var Type: `Int`
	- Property Name: MatchGoals
	- Does This Work?: Unknown
+ Points
	- Var Type: `Int`
	- Property Name: MatchScore
	- Does This Work?: Yes
+ Shots On Goal
	- Var Type: `Int`
	- Property Name: MatchShots
	- Does This Work?: Yes
+ Assists
	- Var Type: `Int`
	- Property Name: MatchAssists
	- Does This Work?: Yes
+ Boost Pickups
	- Var Type: `Int`
	- Property Name: BoostPickups
	- Does This Work?: Unknown
+ Saves
	- Var Type: `Int`
	- Property Name: MatchSaves
	- Does This Work?: Yes
+ Own Goals
	- Var Type: `Int`
	- Property Name: MatchOwnGoals
	- Does This Work?: Yes
+ Demos
	- Var Type: `Int`
	- Property Name: MatchDemolishes
	- Does This Work?: Yes
+ Deaths
	- Var Type: `Int`
	- Property Name: Deaths
	- Does This Work?: Yes
+ Ball touches
	- Var Type: `Int`
	- Property Name: BallTouches
	- Does This Work?: Unknown
+ Car touches
	- Var Type: `Int`
	- Property Name: CarTouches
	- Does This Work?: Unknown
+ Km driven
	- Var Type: `float`
	- Property Name: MatchKMDriven
	- Does This Work?: Unknown
+ Dropshot: damage
	- Var Type: `Int`
	- Property Name: MatchBreakoutDamage
	- Does This Work?: Unknown
+ Rumble: time till next item
	- Var Type: `Int`
	- Property Name: TimeTillItem
	- Does This Work?: Unknown
+ Rumble: Max time till next item
	- Var Type: `Int`
	- Property Name: MaxTimeTillItem
	- Does This Work?: Unknown
+ Match Stats - `TAPlayerStat`
	- Property Name: MatchStats
	- Does This Work?: Unknown
+ Bonus xp
	- Var Type: `Int`
	- Property Name: MatchBonusXP
	- Does This Work?: Unknown
+ Object is player:
	- Var Type: `bool`
	- Property Name: bPlayer
	- Does This Work?: Yes
+ Object is bot / AI
	- Var Type: `bool`
	- Property Name: bBot
	- Does This Work?: Yes
+ Player is MVP
	- Var Type: `bool`
	- Property Name: bMatchMVP
	- Does This Work?: Unknown
+ Player is active
	- Var Type: `bool`
	- Property Name: bIsInactive
	- Does This Work?: Unknown
+ Player is welcomed
	- Var Type: `bool`
	- Property Name: bHasBeenWelcomed
	- Does This Work?: Unknown
+ Player is Spectator
	- Var Type: `bool`
	- Property Name: bIsSpectator
	- Does This Work?: Unknown
+ Player is admin
	- Var Type: `bool`
	- Property Name: bMatchAdmin (/ PRI -> bAdmin ?)
	- Does This Work?: Unknown
+ Player is Main player (ie non-splitscreen?)
	- Var Type: `bool`
	- Property Name: IsPrimaryPlayer
	- Does This Work?: Unknown
+ Player is a developer
	- Var Type: `bool`
	- Property Name: bDeveloper
	- Does This Work?: Unknown
+ Player can respawn
	- Var Type: `bool`
	- Property Name: bOutOfLives
	- Does This Work?: Unknown
+ Player can only Spectate `Bool`
	- Property Name: bOnlySpectator
	- Does This Work?: Unknown
+ Player has team paint
	- Var Type: `bool`
	- Property Name: bTeamPaintSet
	- Does This Work?: Unknown
+ Player comes from previous level
	- Var Type: `bool`
	- Property Name: bFromPreviousLevel
	- Does This Work?: Unknown
+ Player is using ballcam
	- Var Type: `bool`
	- Property Name: bUsingSecondaryCamera
	- Does This Work?: Yes
+ Player is using rearcam
	- Var Type: `bool`
	- Property Name: bUsingBehindView
	- Does This Work?: Yes
+ Player is using freecam
	- Var Type: `bool`
	- Property Name: bUsingFreecam
	- Does This Work?: Yes
+ Player is using Splitscreen
	- Var Type: `bool`
	- Property Name: bIsInSplitScreen
	- Does This Work?: Unknown
+ Time Since PRI was created
	- Var Type: `Int`
	- Property Name: StartTime
	- Does This Work?: Unknown
+ Time until respawn
	- Var Type: `Int`
	- Property Name: RespawnTimeRemaining
	- Does This Work?: Unknown
+ Lives used by player
	- Var Type: `Int`
	- Property Name: NumLives
	- Does This Work?: Unknown
+ Non rounded ping
	- Var Type: `float`
	- Property Name: ExactPing
	- Does This Work?: Unknown
+ Rounded ping
	- Var Type: `Int`
	- Property Name: Ping (for everyone except for player itself)
	- Does This Work?: Unknown
+ Connection Stats
	- Var Type: `Int`
	- Property Name: StatConnectionCounts
	- Does This Work?: Unknown
+ Total time played (hours/days??)
	- Var Type: `float`
	- Property Name: TotalGameTimePlayed
	- Does This Work?: Unknown
+ Total xp
	- Var Type: `Int`
	- Property Name: TotalXP
	- Does This Work?: Unknown

Console commands

Actions

Classes

Game events

Server types

particle systems

Undocumented nodes

UI States

Game URL options



## Console commands

+ working
	- restartlevel
	- demolishself
+ possible
	- EXIT
	- exit
	- DEFERRED_STOPMEMTRACKING_AND_DUMP
	- MemFragCheck
	- open $ map
	- Disconnect
	- hidelog
	- debugai
	- "bugscreenshot " $ ScreenShotDescription
+ Sentinelpc.console
	- FractureAllMeshesToMaximizeMemoryUsage
	- stat memory
	- MemLeakCheck
	- stat scenerendering
+ pc.consolecommand
	- quit
+ UDK Documentation
	- [ExecFunctions](https://docs.unrealengine.com/udk/Three/ExecFunctions.html)
+ uee console commands
	- KonamiCode
	- ShowFPS
+ uee cheat console commands?
	- ResetSkillAll (reset xp?)
	- RemoveAllProducts (remove all items?)
	- GiveAllProductsBeforeThisVersion
	- GiveAllProductsDroppable
	- GiveAllProducts

## Actions 
(without replay and trainingeditor)

- Movement
	- ThrottleForward
	- ThrottleReverse
	- SteerRight
	- SteerLeft
	- YawRight
	- YawLeft
	- PitchUp
	- PitchDown
	- RollRight
	- RollLeft
- Camera
	- LookUp
	- LookDown
	- LookRight
	- LookLeft
- Actions
	- Boost
	- Jump
	- Handbrake
	- SecondaryCamera
	- ToggleRoll
	- ReadyUp
	- RearCamera
	- UsePickup
	- NextPickup
- Match
	- ToggleMidGameMenu
	- ToggleScoreboard
- Training
	- ResetTraining
	- SkipTutorial
	- TutorialHelper
- Chat
	- ChatPreset1
	- ChatPreset2
	- ChatPreset3
	- ChatPreset4
	- Chat
	- TeamChat
	- PartyChat
- Music
	- MusicNextTrack
	- MusicTogglePlaylistSelection
- Settings
	- ToggleStatGraphs
	- AutoSaveReplay

## Bots
- actions:
- conditions:
- other:

## Classes

- ball
	- Ball_TA
	- Ball_Breakout_TA
	- Ball_God_TA
	- Ball_Haunted_TA
	- Ball_Tutorial_TA
- related to the ball
	- Ball_Trajectory_TA
	- Ball_GameEditor_TA
	- BallLocationComponent_TA
	- BallRadiusVolume_TA
	- BallSlomoComponent_TA
- bots
	- BotConfig_TA
	- BotDetectionConfig_TA
	- BotDetection_TA
	- BotReplacement_TA
	- AIController_Breakout_TA
	- AIController_Soccar_TA
	- AIController_TA
	- AIManager_TA
	- AIProxy_TA
- goals
	- Goal_TA
	- Goal_Hoops_TA (GoalVolume_TA
	- GoalVolume_Hoops_TA)
- match types
	- MatchType_AdHoc_TA
	- MatchType_AutoTournament_TA
	- MatchType_Custom_TA
	- MatchType_FTE_TA
	- MatchType_FaceIt_TA
	- MatchType_Freeplay_TA
	- MatchType_Lan_TA
	- MatchType_Offline_TA
	- MatchType_PhysicsLogPlayback_TA
	- MatchType_Private_TA
	- MatchType_PublicRanked_TA
	- MatchType_Public_TA
	- MatchType_Tournament_TA
	- MatchType_Tutorial_TA
- mutators
	- Mutator_Audio_TA
	- Mutator_Ball_TA
	- Mutator_Booster_TA
	- Mutator_Bots_TA
	- Mutator_Car_TA
	- Mutator_Demolish_TA
	- Mutator_Freeplay_TA
	- Mutator_GameEvent_TA
	- Mutator_GameSpeed_TA
	- Mutator_Gravity_TA
	- Mutator_Handicap_TA
	- Mutator_Loadout_TA
	- Mutator_Match_TA
	- Mutator_PhysicsLogPlayback_TA
	- Mutator_RespawnTime_TA
	- Mutator_Robin_TA
- rumble pickups
	- SpecialPickup_TA
	- SpecialPickup_Attachment_TA
	- SpecialPickup_BallCarSpring_TA
	- SpecialPickup_BallFreeze_TA
	- SpecialPickup_BallGravity_TA
	- SpecialPickup_BallLasso_TA
	- SpecialPickup_BallVelcro_TA
	- SpecialPickup_Batarang_TA
	- SpecialPickup_BoostMod_TA
	- SpecialPickup_BoostOverride_TA
	- SpecialPickup_CarFreeze_TA
	- SpecialPickup_CarGravity_TA
	- SpecialPickup_CarLaunch_TA
	- SpecialPickup_CarSpeed_TA
	- SpecialPickup_Demolish_TA
	- SpecialPickup_GrapplingHook_TA
	- SpecialPickup_HandbrakeOverride_TA
	- SpecialPickup_HauntedBallBeam_TA
	- SpecialPickup_HitForce_TA
	- SpecialPickup_Rugby_TA
	- SpecialPickup_Spring_TA
	- SpecialPickup_Swapper_TA
	- SpecialPickup_Targeted_TA
	- SpecialPickup_TimeBomb_TA
	- SpecialPickup_Tornado_TA
(+ VehiclePickup_Item_TA?);
- mutator presets
	- MutatorPreset_Beachball
	- MutatorPreset_Cubeball
	- MutatorPreset_DemolitionDerby
	- MutatorPreset_Moonball
	- MutatorPreset_Rugby
	- MutatorPreset_SnowDay
	- MutatorPreset_TimeWarp

## Events

- working events
	- 
- possible events:
- PRI game events
	- GameEventChanged
	- StatEvent (see list of StatEvents for all values)
	- RequestedLoadout
	- SelectedLoadout
	- VanityChanged
	- StatTickerMessage
	- InvalidPsyonixID
	- ReadyChanged
	- CarPreUpdate
	- CarSet
	- SplitScreenStatusChanged
	- Distracted
	- PersistentCameraSet
	- CameraChanged
	- PartyLeaderChanged
	- ScorePoint
	- WonMVP
	- StatTitlesSet
	- PawnTypeChanged
	- CommittedStats
	- StartVoteToForfeitDisabledChanged
	- TitleChanged
	- SkillTierChanged
	- ServerChangeTeamFailed
	- ScoredGoal
	- ReplacingBotChanged
	- MatchAdmin
	- ServerUnlockedAchievement
	- ServerAchievementProgression
	- SpectatorShortcutChanged
	- OwnerChanged
- SeqEvent_Console (= Console event kismet node)
	- anthem_on
	- anthem_off
	- TestCinematic
	- LoadCinematic
	- CarSelect
	- TutorialCar
- StatEvent_TA
	- BulletGoal
	- BulletHit
- FXActorEvent_X
	- Active
	- Boost
	- BoostEndEvent
	- BoostFly
	- BoostPreview
	- BoostShake
	- Broken
	- Damaged
	- Dodge
	- DoubleJump
	- Editing
	- HideWorldUI
	- InAir
	- Jump
	- LocalPickedUp
	- OnWall
	- Painted
	- PickedUp
	- Preview
	- Simulating
	- Spawned
	- SuperSonic
	- Team0
	- Team1
	- Throttling
- StatEvent (reference `StatEvent_TA'StatEvents.Events.<event name>'`
	- sound `StatEvent_<event name>`)
	- between () are textures for events that are removed
	- AerialGoal
	- AerialHit
	- Assist
	- BackwardsGoal
	- BicycleGoal
	- BicycleHit
	- BreakoutDamage
	- BreakoutDamageLarge
	- (BulletGoal,) Center
	- Clear
	- (Demolish,) Demolition
	- EpicSave
	- FirstTouch
	- Goal
	- HatTrick
	- HighFive
	- HoopsSwishGoal
	- JuggleHit
	- (Juggler,) LongGoal
	- Loss
	- LowFive
	- MVP
	- OvertimeGoal
	- Playmaker
	- PoolShot
	- Save
	- Savior
	- Shot
	- TimePlayed
	- TurtleGoal
	- Win
- GameEventChanged
	- WaitingForPlayers
	- Countdown
	- Active
	- PostGoalScored
	- ReplayPlayback
	- PrePodiumSpotlight
	- PodiumSpotlight
	- Finished

## Server types (get with WI -> NetMode?)
Probably better to get the server type with the kismet node

- NM_Standalone      // Standalone game.
- NM_DedicatedServer  // Dedicated server, no local client.
- NM_ListenServer      // Listen server.
- NM_Client             // Client only, no local server.

## Particle systems:
(use material library for particle systems?)
- Park_P
	- ParticleSystem'FX_Dust.AmbientDust_PS'
	- ParticleSystem'Environment_FX.Particles.LeavesFalling_PS'
	- ParticleSystem'FX_Dust.AmbientDust_PS'
	- ParticleSystem'LensFlares.Particles.StadiumFlares_PS'
	- ParticleSystem'Stadium.Particles.Confetti_Explosion_Large_PS'
- player leaves match
	- ParticleSystem'FX_LeaveGame.FX.Beam_PS' (TAGame.upk)

## Undocument nodes?

Might be that these have a different name in UDK / I missed them in UDK / Nodes are working / nodes are only working outside of a custom map (most of them are already discovered before):

- general actions
	- 
    - SeqAct_CarMatinee_TA
    - SeqAct_GetEdition_TA (china or default)
    - SeqAct_GetPlaylistType_TA (Private
	- Casual
	- Competitive or Tournament)
    - SeqAct_SetSkelMATLoadout_TA
- general events
	- 
    - SeqEvent_ReplayTime_TA
- tutorials:
    - SeqAct_EndTutorial_TA
    - SeqAct_GetTutorialType_TA
    - SeqAct_NotifyEventOnTutorial_TA
    - SeqAct_SetTutorialGameEvent_TA
    - SeqEvent_TutorialStarted_TA
    - SeqEvent_TutorialHelper_TA
- garage (items) and menu:
    - SeqAct_IsCrateRouletteEnabled_TA (probably useless)
    - SeqAct_GetRarityColor_TA
    - SeqAct_GetSaveData_TA
    - SeqEvent_CarSelectStart_TA
    - SeqEvent_GarageComplexState_TA
    - SeqEvent_PreviewMusicStingerVisualizer_TA
    - SeqEvent_MTXGarageReveal_TA
    - SeqEvent_MTXGarageBlueprintPreview_TA
    - SeqEvent_ShowGarageComplex_TA
- introduction for new players (seems to be the category):
    - SeqAct_CinematicIntroStartNextSeq_TA
    - SeqAct_IntroMenuCarsInPosition_TA
    - SeqEvent_StartHighlightReel_TA
    - SeqEvent_CinematicIntroSeqFinished_TA
    - SeqEvent_IntroMenu_TA
    
## UI states

- working:
- possible
	- HUD
	- Editor
	- HUDSoccar
	- ReplayViewer
	- Spectator
	- SplitscreenReplayViewer
- not working
	- MidGameMenu
	- ScoreBoard
	- Score
	- Countdown
	- Nameplates
	- RL_Logo

## Game URL options

options: `ExitMessage`
	- Var Type: `???`
	- Property Name: TimeDilation
	- Does This Work?: Unknown
+ Player who paused the match (if match is paused)
	- Var Type: `???`
	- Property Name: WI -> Pauser
	- Does This Work?: Unknown (returns PRI?)
+ Number of players
	- Var Type: `???`
	- Property Name: Game -> NumPlayers
	- Does This Work?: Unknown
+ Number of bots
	- Var Type: `???`
	- Property Name: Game -> NumBots
	- Does This Work?: Unknown
+ Only update players 
	- Var Type: `Bool`:
	- Property Name: bPlayersOnly
	- Does This Work?: Unknown
+ Score needed to end match
	- Var Type: `Int`
	- Property Name: Game -> GoalScore
	- Does This Work?: Unknown
+ Time limit
	- Var Type `Int (minutes)`:
	- Property Name: Game -> TimeLimit
	- Does This Work?: Unknown
+ Menu level 
	- Var Type: `Bool`:
	- Property Name: bIsMenuLevel
	- Does This Work?: Unknown
+ StallZ (???)
	- Var Type: `???`
	- Property Name: StallZ
	- Does This Work?: Unknown
+ KillZ
	- Var Type: `???`
	- Property Name: KillZ
	- Does This Work?: Unknown
+ Maximum players
	- Var Type: `Int`
	- Property Name: Game -> MaxPlayers
	- Does This Work?: Unknown
+ Maximum spectators
	- Var Type: `Int`
	- Property Name: Game -> MaxSpectators
	- Does This Work?: Unknown
+ Players that are still travelling from another map
	- Var Type: `Int`
	- Property Name: Game -> NumTravellingPlayers
	- Does This Work?: Unknown
+ Time until match starts? :
	- Property Name: Game -> bWaitingToStartMatch
	- Does This Work?: Unknown
+ Called when something triggers on the server: brings up laoding screen and finishes all async functions (???) 
	- Var Type: `Bool`:
	- Property Name: bRequestedBlockOnAsyncLoading ((used to check connection)? => is this even usefull?)
:::

:::details GRI
## GRI (GameReplicationInfo)
(WorldInfo -> GRI)

(Not everything might be replicated to clients / server)
+ Game class - `class<GameInfo>`:
	- Property Name: GameClass
+ Leaderboard Id (???)
	- Var Type: `???`
	- Property Name: GameClass -> default -> ArbitratedLeaderBoardId
+ Match over 
	- Var Type: `Bool`
	- Property Name: bMatchIsOver
+ Match began 
	- Var Type: `Bool`
	- Property Name: bMatchHasBegun
+ Time limit
	- Var Type: (???)
	- Property Name: TimeLimit
+ ???
	- Var Type: `Int`
	- Property Name: GoalScore
+ ???
	- Var Type: `Int`
	- Property Name: ElapsedTime
+ ???
	- Var Type: `Int`
	- Property Name: RemainingTime
+ Winner (set at end of match)
	- Var Type: `Object`
	- Object Type: `Actor`
	- Property Name: Winner
+ ??? (???):
	- Property Name: RemainingMinute
+ List of players 
	- Var Type: `array<PRI>
	- Property Name: PRIArray (would length return player count?)
+ List of inactive players
	- Var Type: `array<PRI>`
	- Property Name: InactivePRIArray
+ List of teams
	- Var Type: `array<TeamInfo>`
	- Property Name: Teams
+ Stop countdown 
	- Var Type: `Bool`
	- Property Name: bStopCountDown
+ Server name:
	- Var Type: `String`
	- Property Name: ServerName (if workshop maps are ever on a server)
+ Match is team game 
	- Var Type: `Bool`
	- Property Name: GameClass -> default -> bTeamGame
	- Does This Work?: Unknown
:::

:::details PRI
## PRI (PlayerReplicationInfo)
(WorldInfo -> GRI -> PRI)
:::tip How to Access PRI Properties in Kismet
Get Object Property (PRI) -> Get Object Property (Property Name) (picture)
:::
+ Player Name
	- Var Type: `String`
	- Property Name: PlayerName
	- Does This Work?: Yes
+ Player's Previous Name
	- Var Type: `String`
	- Property Name: OldName (client-side only)
	- Does This Work?: Unknown
+ Player Name (sanitized)
	- Var Type: `String`
	- Property Name: SanitizedPlayerName
	- Does This Work?: Unknown
+ Player Platform
	- Var Type: `String`
	- Property Name: Platform
	- Does This Work?: Yes
+ Player Car position
	- Var Type: `Vector`
	- Property Name: LastCarLocation
	- Does This Work?: Unknown 
+ Player's Car
	- Var Type: `Object`
	- Actor Class: `Car_TA`
	- Property Name: Car
	- Does This Work?: Yes
+ Player Id
	- Var Type: `String`
	- Property Name: PlayerID
		+ (UniqueID is used for identifying player)
	- Does This Work?: Yes
+ Player UniqueId -> Uid
	- Var Type: `???`
	- Property Name: UniqueId -> Uid
	- Does This Work?: Unknown
+ Player Replicated Data
	- Var Type: `PRI` (object maybe?)
	- Property Name: PREI
	- Does This Work?: Unknown
+ Player Avatar
	- Var Type: - `Object` (maybe Texture2D?)
	- Property Name: PlayerAvatar
	- Does This Work?: Unknown
+ Player banner
	- Var Type: `Object` (maybe?)
	- Property Name: PlayerBanner
	- Does This Work?: Unknown
+ Player Camera
	- Var Type: `Object`
	- Actor Class: `CameraSettingsActor_TA`
	- Property Name: Camera
	- Does This Work?: Unknown
+ Player Title
	- Var Type: `String`
	- Property Name: Title
	- Does This Work?: Unknown
+ Player Team - `TeamInfo`
	- Property Name: Team
		+ Team Index
			- Var Type: `Int`
			- Property Name: TeamIndex
			- Does This Work?: Yes
		+ Team Name
			- Var Type: `String`
			- Property Name: CustomTeamName
			- Does This Work?: Yes
		+ Team Sanitized name
			- Var Type: `String`
			- Property Name: SanitizedTeamName
			- Does This Work?: Unknown
		+ Team Size
			- Var Type: `Int`
			- Property Name: Size
			- Does This Work?: Unknown
		+ Team Members
			- `PRI_TA`
			- Property Name: Members
			- Does This Work?: Unknown
		+ Team Color
			- `color`
			- Property Name: TeamColor
			- Does This Work?: Unknown
		+ Team Logo
			- `Texture`
			- Property Name: TeamLogo
			- Does This Work?: Unknown
		+ Team Goals
			- Var Type: `Int`
			- Property Name: Score
			- Does This Work?: Yes
		+ Team Difficulty
			- Var Type: `Int`
			- Property Name: Difficulty
			- Does This Work?: Unknown
		+ Team Series goals
			- Var Type: `Int`
			- Property Name: SeriesScore
			- Does This Work?: Unknown
		+ Team Paint
			- `LoadoutTeamPaint`
			- Property Name: TeamPaint
			- Does This Work?: Unknown
		+ Team Forfeit
			- Var Type: `bool`
			- Property Name: bForfeit
			- Does This Work?: Unknown
		+ Team Custom Color
			- Var Type: `bool`
			- Property Name: bHasCustomColor
			- Does This Work?: Unknown
+ Goals
	- Var Type: `Int`
	- Property Name: MatchGoals
	- Does This Work?: Unknown
+ Points
	- Var Type: `Int`
	- Property Name: MatchScore
	- Does This Work?: Yes
+ Shots On Goal
	- Var Type: `Int`
	- Property Name: MatchShots
	- Does This Work?: Yes
+ Assists
	- Var Type: `Int`
	- Property Name: MatchAssists
	- Does This Work?: Yes
+ Boost Pickups
	- Var Type: `Int`
	- Property Name: BoostPickups
	- Does This Work?: Unknown
+ Saves
	- Var Type: `Int`
	- Property Name: MatchSaves
	- Does This Work?: Yes
+ Own Goals
	- Var Type: `Int`
	- Property Name: MatchOwnGoals
	- Does This Work?: Yes
+ Demos
	- Var Type: `Int`
	- Property Name: MatchDemolishes
	- Does This Work?: Yes
+ Deaths
	- Var Type: `Int`
	- Property Name: Deaths
	- Does This Work?: Yes
+ Ball touches
	- Var Type: `Int`
	- Property Name: BallTouches
	- Does This Work?: Unknown
+ Car touches
	- Var Type: `Int`
	- Property Name: CarTouches
	- Does This Work?: Unknown
+ Km driven
	- Var Type: `float`
	- Property Name: MatchKMDriven
	- Does This Work?: Unknown
+ Dropshot: damage
	- Var Type: `Int`
	- Property Name: MatchBreakoutDamage
	- Does This Work?: Unknown
+ Rumble: time till next item
	- Var Type: `Int`
	- Property Name: TimeTillItem
	- Does This Work?: Unknown
+ Rumble: Max time till next item
	- Var Type: `Int`
	- Property Name: MaxTimeTillItem
	- Does This Work?: Unknown
+ Match Stats - `TAPlayerStat`
	- Property Name: MatchStats
	- Does This Work?: Unknown
+ Bonus xp
	- Var Type: `Int`
	- Property Name: MatchBonusXP
	- Does This Work?: Unknown
+ Object is player:
	- Var Type: `bool`
	- Property Name: bPlayer
	- Does This Work?: Yes
+ Object is bot / AI
	- Var Type: `bool`
	- Property Name: bBot
	- Does This Work?: Yes
+ Player is MVP
	- Var Type: `bool`
	- Property Name: bMatchMVP
	- Does This Work?: Unknown
+ Player is active
	- Var Type: `bool`
	- Property Name: bIsInactive
	- Does This Work?: Unknown
+ Player is welcomed
	- Var Type: `bool`
	- Property Name: bHasBeenWelcomed
	- Does This Work?: Unknown
+ Player is Spectator
	- Var Type: `bool`
	- Property Name: bIsSpectator
	- Does This Work?: Unknown
+ Player is admin
	- Var Type: `bool`
	- Property Name: bMatchAdmin (/ PRI -> bAdmin ?)
	- Does This Work?: Unknown
+ Player is Main player (ie non-splitscreen?)
	- Var Type: `bool`
	- Property Name: IsPrimaryPlayer
	- Does This Work?: Unknown
+ Player is a developer
	- Var Type: `bool`
	- Property Name: bDeveloper
	- Does This Work?: Unknown
+ Player can respawn
	- Var Type: `bool`
	- Property Name: bOutOfLives
	- Does This Work?: Unknown
+ Player can only Spectate `Bool`
	- Property Name: bOnlySpectator
	- Does This Work?: Unknown
+ Player has team paint
	- Var Type: `bool`
	- Property Name: bTeamPaintSet
	- Does This Work?: Unknown
+ Player comes from previous level
	- Var Type: `bool`
	- Property Name: bFromPreviousLevel
	- Does This Work?: Unknown
+ Player is using ballcam
	- Var Type: `bool`
	- Property Name: bUsingSecondaryCamera
	- Does This Work?: Yes
+ Player is using rearcam
	- Var Type: `bool`
	- Property Name: bUsingBehindView
	- Does This Work?: Yes
+ Player is using freecam
	- Var Type: `bool`
	- Property Name: bUsingFreecam
	- Does This Work?: Yes
+ Player is using Splitscreen
	- Var Type: `bool`
	- Property Name: bIsInSplitScreen
	- Does This Work?: Unknown
+ Time Since PRI was created
	- Var Type: `Int`
	- Property Name: StartTime
	- Does This Work?: Unknown
+ Time until respawn
	- Var Type: `Int`
	- Property Name: RespawnTimeRemaining
	- Does This Work?: Unknown
+ Lives used by player
	- Var Type: `Int`
	- Property Name: NumLives
	- Does This Work?: Unknown
+ Non rounded ping
	- Var Type: `float`
	- Property Name: ExactPing
	- Does This Work?: Unknown
+ Rounded ping
	- Var Type: `Int`
	- Property Name: Ping (for everyone except for player itself)
	- Does This Work?: Unknown
+ Connection Stats
	- Var Type: `Int`
	- Property Name: StatConnectionCounts
	- Does This Work?: Unknown
+ Total time played (hours/days??)
	- Var Type: `float`
	- Property Name: TotalGameTimePlayed
	- Does This Work?: Unknown
+ Total xp
	- Var Type: `Int`
	- Property Name: TotalXP
	- Does This Work?: Unknown
:::
:::details Console commands
:::
:::details Actions
:::
:::details Classes
:::
:::details Game events
:::
:::details Server types
:::
:::details particle systems
:::
:::details Undocumented nodes
:::
:::details UI States
:::
:::details Game URL options
:::

:::details
## Console commands

+ working
	- restartlevel
	- demolishself
+ possible
	- EXIT
	- exit
	- DEFERRED_STOPMEMTRACKING_AND_DUMP
	- MemFragCheck
	- open $ map
	- Disconnect
	- hidelog
	- debugai
	- "bugscreenshot " $ ScreenShotDescription
+ Sentinelpc.console
	- FractureAllMeshesToMaximizeMemoryUsage
	- stat memory
	- MemLeakCheck
	- stat scenerendering
+ pc.consolecommand
	- quit
+ UDK Documentation
	- [ExecFunctions](https://docs.unrealengine.com/udk/Three/ExecFunctions.html)
+ uee console commands
	- KonamiCode
	- ShowFPS
+ uee cheat console commands?
	- ResetSkillAll (reset xp?)
	- RemoveAllProducts (remove all items?)
	- GiveAllProductsBeforeThisVersion
	- GiveAllProductsDroppable
	- GiveAllProducts
:::

:::details
## Actions 
(without replay and trainingeditor)

- Movement
	- ThrottleForward
	- ThrottleReverse
	- SteerRight
	- SteerLeft
	- YawRight
	- YawLeft
	- PitchUp
	- PitchDown
	- RollRight
	- RollLeft
- Camera
	- LookUp
	- LookDown
	- LookRight
	- LookLeft
- Actions
	- Boost
	- Jump
	- Handbrake
	- SecondaryCamera
	- ToggleRoll
	- ReadyUp
	- RearCamera
	- UsePickup
	- NextPickup
- Match
	- ToggleMidGameMenu
	- ToggleScoreboard
- Training
	- ResetTraining
	- SkipTutorial
	- TutorialHelper
- Chat
	- ChatPreset1
	- ChatPreset2
	- ChatPreset3
	- ChatPreset4
	- Chat
	- TeamChat
	- PartyChat
- Music
	- MusicNextTrack
	- MusicTogglePlaylistSelection
- Settings
	- ToggleStatGraphs
	- AutoSaveReplay
:::

:::details
## Bots
- actions:
- conditions:
- other:
:::

:::details
## Classes

- ball
	- Ball_TA
	- Ball_Breakout_TA
	- Ball_God_TA
	- Ball_Haunted_TA
	- Ball_Tutorial_TA
- related to the ball
	- Ball_Trajectory_TA
	- Ball_GameEditor_TA
	- BallLocationComponent_TA
	- BallRadiusVolume_TA
	- BallSlomoComponent_TA
- bots
	- BotConfig_TA
	- BotDetectionConfig_TA
	- BotDetection_TA
	- BotReplacement_TA
	- AIController_Breakout_TA
	- AIController_Soccar_TA
	- AIController_TA
	- AIManager_TA
	- AIProxy_TA
- goals
	- Goal_TA
	- Goal_Hoops_TA (GoalVolume_TA
	- GoalVolume_Hoops_TA)
- match types
	- MatchType_AdHoc_TA
	- MatchType_AutoTournament_TA
	- MatchType_Custom_TA
	- MatchType_FTE_TA
	- MatchType_FaceIt_TA
	- MatchType_Freeplay_TA
	- MatchType_Lan_TA
	- MatchType_Offline_TA
	- MatchType_PhysicsLogPlayback_TA
	- MatchType_Private_TA
	- MatchType_PublicRanked_TA
	- MatchType_Public_TA
	- MatchType_Tournament_TA
	- MatchType_Tutorial_TA
- mutators
	- Mutator_Audio_TA
	- Mutator_Ball_TA
	- Mutator_Booster_TA
	- Mutator_Bots_TA
	- Mutator_Car_TA
	- Mutator_Demolish_TA
	- Mutator_Freeplay_TA
	- Mutator_GameEvent_TA
	- Mutator_GameSpeed_TA
	- Mutator_Gravity_TA
	- Mutator_Handicap_TA
	- Mutator_Loadout_TA
	- Mutator_Match_TA
	- Mutator_PhysicsLogPlayback_TA
	- Mutator_RespawnTime_TA
	- Mutator_Robin_TA
- rumble pickups
	- SpecialPickup_TA
	- SpecialPickup_Attachment_TA
	- SpecialPickup_BallCarSpring_TA
	- SpecialPickup_BallFreeze_TA
	- SpecialPickup_BallGravity_TA
	- SpecialPickup_BallLasso_TA
	- SpecialPickup_BallVelcro_TA
	- SpecialPickup_Batarang_TA
	- SpecialPickup_BoostMod_TA
	- SpecialPickup_BoostOverride_TA
	- SpecialPickup_CarFreeze_TA
	- SpecialPickup_CarGravity_TA
	- SpecialPickup_CarLaunch_TA
	- SpecialPickup_CarSpeed_TA
	- SpecialPickup_Demolish_TA
	- SpecialPickup_GrapplingHook_TA
	- SpecialPickup_HandbrakeOverride_TA
	- SpecialPickup_HauntedBallBeam_TA
	- SpecialPickup_HitForce_TA
	- SpecialPickup_Rugby_TA
	- SpecialPickup_Spring_TA
	- SpecialPickup_Swapper_TA
	- SpecialPickup_Targeted_TA
	- SpecialPickup_TimeBomb_TA
	- SpecialPickup_Tornado_TA
(+ VehiclePickup_Item_TA?);
- mutator presets
	- MutatorPreset_Beachball
	- MutatorPreset_Cubeball
	- MutatorPreset_DemolitionDerby
	- MutatorPreset_Moonball
	- MutatorPreset_Rugby
	- MutatorPreset_SnowDay
	- MutatorPreset_TimeWarp
:::

:::details
## Events

- working events
	- 
- possible events:
- PRI game events
	- GameEventChanged
	- StatEvent (see list of StatEvents for all values)
	- RequestedLoadout
	- SelectedLoadout
	- VanityChanged
	- StatTickerMessage
	- InvalidPsyonixID
	- ReadyChanged
	- CarPreUpdate
	- CarSet
	- SplitScreenStatusChanged
	- Distracted
	- PersistentCameraSet
	- CameraChanged
	- PartyLeaderChanged
	- ScorePoint
	- WonMVP
	- StatTitlesSet
	- PawnTypeChanged
	- CommittedStats
	- StartVoteToForfeitDisabledChanged
	- TitleChanged
	- SkillTierChanged
	- ServerChangeTeamFailed
	- ScoredGoal
	- ReplacingBotChanged
	- MatchAdmin
	- ServerUnlockedAchievement
	- ServerAchievementProgression
	- SpectatorShortcutChanged
	- OwnerChanged
- SeqEvent_Console (= Console event kismet node)
	- anthem_on
	- anthem_off
	- TestCinematic
	- LoadCinematic
	- CarSelect
	- TutorialCar
- StatEvent_TA
	- BulletGoal
	- BulletHit
- FXActorEvent_X
	- Active
	- Boost
	- BoostEndEvent
	- BoostFly
	- BoostPreview
	- BoostShake
	- Broken
	- Damaged
	- Dodge
	- DoubleJump
	- Editing
	- HideWorldUI
	- InAir
	- Jump
	- LocalPickedUp
	- OnWall
	- Painted
	- PickedUp
	- Preview
	- Simulating
	- Spawned
	- SuperSonic
	- Team0
	- Team1
	- Throttling
- StatEvent (reference `StatEvent_TA'StatEvents.Events.<event name>'`
	- sound `StatEvent_<event name>`)
	- between () are textures for events that are removed
	- AerialGoal
	- AerialHit
	- Assist
	- BackwardsGoal
	- BicycleGoal
	- BicycleHit
	- BreakoutDamage
	- BreakoutDamageLarge
	- (BulletGoal,) Center
	- Clear
	- (Demolish,) Demolition
	- EpicSave
	- FirstTouch
	- Goal
	- HatTrick
	- HighFive
	- HoopsSwishGoal
	- JuggleHit
	- (Juggler,) LongGoal
	- Loss
	- LowFive
	- MVP
	- OvertimeGoal
	- Playmaker
	- PoolShot
	- Save
	- Savior
	- Shot
	- TimePlayed
	- TurtleGoal
	- Win
- GameEventChanged
	- WaitingForPlayers
	- Countdown
	- Active
	- PostGoalScored
	- ReplayPlayback
	- PrePodiumSpotlight
	- PodiumSpotlight
	- Finished
:::

:::details
## Server types (get with WI -> NetMode?)
Probably better to get the server type with the kismet node

- NM_Standalone      // Standalone game.
- NM_DedicatedServer  // Dedicated server, no local client.
- NM_ListenServer      // Listen server.
- NM_Client             // Client only, no local server.
:::

:::details
## Particle systems:
(use material library for particle systems?)
- Park_P
	- ParticleSystem'FX_Dust.AmbientDust_PS'
	- ParticleSystem'Environment_FX.Particles.LeavesFalling_PS'
	- ParticleSystem'FX_Dust.AmbientDust_PS'
	- ParticleSystem'LensFlares.Particles.StadiumFlares_PS'
	- ParticleSystem'Stadium.Particles.Confetti_Explosion_Large_PS'
- player leaves match
	- ParticleSystem'FX_LeaveGame.FX.Beam_PS' (TAGame.upk)
:::

:::details
## Undocument nodes?

Might be that these have a different name in UDK / I missed them in UDK / Nodes are working / nodes are only working outside of a custom map (most of them are already discovered before):

- general actions
	- 
    - SeqAct_CarMatinee_TA
    - SeqAct_GetEdition_TA (china or default)
    - SeqAct_GetPlaylistType_TA (Private
	- Casual
	- Competitive or Tournament)
    - SeqAct_SetSkelMATLoadout_TA
- general events
	- 
    - SeqEvent_ReplayTime_TA
- tutorials:
    - SeqAct_EndTutorial_TA
    - SeqAct_GetTutorialType_TA
    - SeqAct_NotifyEventOnTutorial_TA
    - SeqAct_SetTutorialGameEvent_TA
    - SeqEvent_TutorialStarted_TA
    - SeqEvent_TutorialHelper_TA
- garage (items) and menu:
    - SeqAct_IsCrateRouletteEnabled_TA (probably useless)
    - SeqAct_GetRarityColor_TA
    - SeqAct_GetSaveData_TA
    - SeqEvent_CarSelectStart_TA
    - SeqEvent_GarageComplexState_TA
    - SeqEvent_PreviewMusicStingerVisualizer_TA
    - SeqEvent_MTXGarageReveal_TA
    - SeqEvent_MTXGarageBlueprintPreview_TA
    - SeqEvent_ShowGarageComplex_TA
- introduction for new players (seems to be the category):
    - SeqAct_CinematicIntroStartNextSeq_TA
    - SeqAct_IntroMenuCarsInPosition_TA
    - SeqEvent_StartHighlightReel_TA
    - SeqEvent_CinematicIntroSeqFinished_TA
    - SeqEvent_IntroMenu_TA
:::

:::details
## UI states

- working:
- possible
	- HUD
	- Editor
	- HUDSoccar
	- ReplayViewer
	- Spectator
	- SplitscreenReplayViewer
- not working
	- MidGameMenu
	- ScoreBoard
	- Score
	- Countdown
	- Nameplates
	- RL_Logo
:::

:::details
## Game URL options

options: `ExitMessage`
:::
