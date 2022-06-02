# Regex
This file is intended for maintainers only. It describes a method of quickly creating a Markdown list for a modpack's dependencies.

## How-To
Generate the modpack's dependency strings using **r2modman**. From the desired profile, select *Settings* > *All* > *Show dependency strings*, then replace text in your favorite editor via the below regex.

**Search:**  `^([a-zA-Z0-9\_]+)-([a-zA-Z0-9\_]+)-(.*)$`<br>
**Replace:** `\-\t\[$2-$3\]\(https://thunderstore.io/package/$1/$2/$3/\)`

*Please note that there may be other characters allowed on thunderstore.io. This regex is not exhaustive, and assumes much.*

### Example Text
```text
bbepis-BepInExPack-5.4.1905
RiskofThunder-HookGenPatcher-1.2.3
KingEnderBrine-ProperSave-2.8.4
tristanmcpherson-R2API-4.3.21
dan8991iel-LunarCoinShareOnPickup-4.2.1
XoXFaby-BetterUI-2.6.1
DepressionChurch-EclipseLevelInCharacterSelection-1.1.3
Moonlol-SeerPing-1.2.1
Rune580-Risk_Of_Options-2.5.2
Higgs1-AV_Effect_Options-1.12.0
Bubbet-SkipIntro-1.0.0
````

### Result
````markdown
-	[BepInExPack-5.4.1905](https://thunderstore.io/package/bbepis/BepInExPack/5.4.1905/)
-	[HookGenPatcher-1.2.3](https://thunderstore.io/package/RiskofThunder/HookGenPatcher/1.2.3/)
-	[ProperSave-2.8.4](https://thunderstore.io/package/KingEnderBrine/ProperSave/2.8.4/)
-	[R2API-4.3.21](https://thunderstore.io/package/tristanmcpherson/R2API/4.3.21/)
-	[LunarCoinShareOnPickup-4.2.1](https://thunderstore.io/package/dan8991iel/LunarCoinShareOnPickup/4.2.1/)
-	[BetterUI-2.6.1](https://thunderstore.io/package/XoXFaby/BetterUI/2.6.1/)
-	[EclipseLevelInCharacterSelection-1.1.3](https://thunderstore.io/package/DepressionChurch/EclipseLevelInCharacterSelection/1.1.3/)
-	[SeerPing-1.2.1](https://thunderstore.io/package/Moonlol/SeerPing/1.2.1/)
-	[Risk_Of_Options-2.5.2](https://thunderstore.io/package/Rune580/Risk_Of_Options/2.5.2/)
-	[AV_Effect_Options-1.12.0](https://thunderstore.io/package/Higgs1/AV_Effect_Options/1.12.0/)
-	[SkipIntro-1.0.0](https://thunderstore.io/package/Bubbet/SkipIntro/1.0.0/)
````
