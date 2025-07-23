# PalServer
PalServer configured &amp; optimized for Vanilla **Palworld v0.6.0 "Tides of Terraria"** running on Linux-hosted server for low-end users.
- Subjected to change
#

Insert the following into the ** STEAM ** console for "Palworld Dedicated Server:"
- -useperfthreads -NoAsyncLoadingThread -UseMultithreadForDS -NumberOfWorkerThreadsServer=8

_Server working with 8 process threads_
_* Adjust as needed *_

#
Understand the following parameters of the **PalWorldSettings** located in _PalServer/Pal/Saved/Config/LinuxServer_
_____________________________
Parameter  | Description
------------- | -------------
AdminPassword | Password used to obtain administrative privileges on the server.
CrossplayPlatforms | Steam / Xbox / PS5 / Mac
BaseCampMaxNumInGuild | Max BaseCamp count per guild. Default is 4. (MAX 10)
BaseCampWorkerMaxNum | Max pals per basecamp（MAX 50)
bAllowGlobalPalboxExport | If set to True, saving to the global palbox is possible.
bAllowGlobalPalboxImport | If set to True, importing from the global palbox is possible.
bBuildAreaLimit | Prohibit building near structures such as fast travel
bCharacterRecreateInHardcore | Allow recreate character when you died in Hardcore mode.
bEnableFastTravel | Enable Fast Travel
bEnableInvaderEnemy | Enable Invader
bHardcore | Enable Hardcore. Cannot respawn upon death.
bInvisibleOtherGuildBaseCampAreaFX | Enable Show basecamp area
bIsRandomizerPalLevelRandom | If the parameter has been set to true, Wild pals level is fully randomized. Set to false, randomized within a level optimized with the area.
bIsUseBackupSaveData | Enable world backup. Disk load will increase when enabled.
bPalLost | Permanent lost your Pals upon death
bShowPlayerList | Enable player list when the press ESC key
BuildObjectDamageRate | Damage to Structure Multiplier
BuildObjectDeteriorationDamageRate | Structure Deterioration Rate
ChatPostLimitPerMinute | Number of chats that can be posted per minute
CollectionDropRate | Gatherable Items Multiplier
CollectionObjectHpRate | Gatherable Objects Health Multiplier
CollectionObjectRespawnSpeedRate | Gatherable Objects Respawn Interval
CrossplayPlatforms | Allowed platform to connect the server. Default: (Steam,Xbox,PS5,Mac)
DayTimeSpeedRate | Day time speed
DeathPenalty | Death Penalty. None: No drops, Item: Drop all items except equipment, ItemAndEquipment: Drop all items, All: Drop all items and all Pals on team
EnemyDropItemRate | Dropped Items Multiplier
EquipmentDurabilityDamageRate | Equipment Durability Loss Multiplier
ExpRate | EXP rate
GuildPlayerMaxNum | Max Player Number of Guilds
ItemContainerForceMarkDirtyInterval | Interval for force sync when open the container. (sec)
ItemWeightRate | Item weight ratio
LogFormatType | Log format Text or Json
MaxBuildingLimitNum | Building num limit per player (0 = unlimit)
NightTimeSpeedRate | Night time speed
PalAutoHPRegeneRate | Pal Auto Health Regeneration Rate
PalAutoHpRegeneRateInSleep | Pal Sleep Health Regeneration Rate (Health Regeneration Rate in Palbox)
PalCaptureRate | Pal capture rate
PalDamageRateAttack | Damage from Pals Multiplier
PalDamageRateDefense | Damage to Pals Multiplier
PalEggDefaultHatchingTime | Time (h) to incubate Massive Egg. Note: Other eggs also require time to incubate.
PalSpawnNumRate | Pal Appearance Rate *Note: Affects game performance
PalStaminaDecreaceRate | Pal Stamina Reduction Rate
PalStomachDecreaceRate | Pal Hunger Depletion Rate
PlayerAutoHPRegeneRate | Player Auto Health Regeneration Rate
PlayerAutoHpRegeneRateInSleep | Player Sleep Health Regeneration Rate
PlayerDamageRateAttack | Damage from Player Multiplier
PlayerDamageRateDefense | Damage to Player Multiplier
PlayerStaminaDecreaceRate | Player Stamina Reduction Rate
PlayerStomachDecreaceRate | Player Hunger Depletion Rate
PublicIP | Explicitly specify an external public IP in the community server settings
PublicPort | Explicitly specify the external public port in the community server configuration. (This setting does not change the server's listen port.)
RandomizerSeed | Randomize seed
RandomizerType | Random Pal Mode. None: No Randomization, Region: Randomize by Region, All: Completely Random
RCONEnabled | Enable RCON
RCONPort | Port Number for RCON
RESTAPIEnabled | Enable REST API
RESTAPIPort | Listen port for REST API
ServerDescription | Server description
ServerName | Server name
ServerPassword | Password required for server login
ServerPlayerMaxNum | Maximum number of players that can join the server
ServerReplicatePawnCullDistance | Pal sync distance from player (cm). Min 5000 ~ Max 15000
SupplyDropSpan | Interval for supply drop (minutes)

#
**CHANGES FOR OPTIMIZATION (LOW-END)**
_____________________________
Parameter  | Description
------------- | -------------
BaseCampWorkerMaxNum = 15 | (1 -> 50) _10 - 20 is the safe range for low-end optimization of default player's operating capabilities_
BaseCampMaxNumInGuild = 10 | (3 -> 10) _adjust depending on average guild count_
ServerReplicatePawnCullDistance = 5000 | (5000 -> 15000) _lesser value, lower processing power for Summoned Pal Synchronization_
bIsPvP = False | (False / True) _HIGHLY recommend keeping this on False unless necessary / RUBBERBANDING is **HIGH-PROFILE** when active while riding Flying Pal_

Please take a look at this [link for parameter range](https://pal-conf.bluefissure.com/)
