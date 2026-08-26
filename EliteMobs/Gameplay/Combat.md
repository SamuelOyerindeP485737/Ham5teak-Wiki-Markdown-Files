# Damage Multipliers & Damage Reduction

EliteMobs completely overrides default Minecraft combat mechanics. Standard vanilla enchantments like Protection or Sharpness provide zero benefits against Elite Mobs unless applied to **Elite Items**.

Because combat scales exponentially, facing an Elite Mob in vanilla Protection IV armor offers virtually no survival advantage compared to wearing no armor at all. Progression depends entirely on your gear's **Elite Item Level** and your overall **Combat Level**.

## Important calculations

- Your combat level is avg of your armor level, and your top two highest weapons. Armor is set to earn 1/3 rd experience of your main hand item, so it will always lag behind in levels.

- You will not be able to receive any item experience from bosses that are too low or too high in level. More over, no elite items wil be dropped from mobs spawned through spawners (Status on mobs spawned through AE's like guardians and spirits is still under work).

- Elite mobs is designed, such that vanilla enchants such as protection 4 are very forgiving for low tier elite mobs. However, due to the formula used to calculate damage received being exponential, it is borderline useless against high level bosses ( 35 and above renders it nearly useless).

- Experience can be earned from killing elite mobs, the formula being **elitemoblevel<sup>2</sup>**.

- When bosses are killed, experience is split proportionally to damage dealt. For group raids, the player with 60 percent damage gets 60 percent of the experience.

| healthMultiplier  | damageMultiplier | XP multiplier |
|-------------------|------------------|---------------|
| 1.0               | 1.0              | 1.00x         |
| 3.0 (miniboss)    | 1.2              | 1.99x         |
| 7.0 (boss)        | 1.4              | 3.41x         |
| 40.0 (world boss) | 1.5              | 9.83x         |




> **Crucial Rule:** Vanilla enchanted books cannot be applied to Elite Items; you must use **Elite Enchanted Books**. Furthermore, Elite Enchantments do not apply to Player vs Player (PvP) combat.

---

## Elite Item Levels, Skill Caps, and Enchants

**Gear Restrictions**
EliteMobs gear has level requirements tied to the skill system. To equip an elite item, your skill level for that weapon or armor type must be equal to or higher than the item's level.
Exception: Items at level 20 or below can be equipped by anyone regardless of skill level. This ensures new players can freely use early-game gear without being locked out.
If you try to equip an item above your skill level, you will receive a warning message and the item will provide no elite bonuses.

#### Scenario: Matched gear, across different skill gaps

Every 7.5 levels of level difference doubles (or halves) a boss's effective damage.

| Level Difference | Skill Adjustment | Approx. Hits to Kill (Matched Gear) |
|------------------|------------------|-------------------------------------|
| Same level (0)   | 1.0x             | ~5 hits                             |
| +5 levels        | ~1.6x            | ~3 hits                             |
| +10 levels       | ~2.5x            | ~2 hits                             |
| +15 levels       | 4.0x             | ~1.25 hits                          |


#### Scenario: Gear Reductions

| Gear Situation                       | Gear Reduction | Gear Adjustment | Hits to Kill (Same Skill Level) |
|--------------------------------------|----------------|-----------------|---------------------------------|
| Naked (no gear)                      | 0%             | 2.0             | ~2.5                            |
| Half-matching gear                   | 25%            | 1.5             | ~3.3                            |
| Matching gear (gearScore = mobLevel) | 50%            | 1.0             | ~5.0                            |
| +4 levels above mob                  | 60%            | 0.8             | ~6.25                           |
| +10 levels above mob (cap)           | 75%            | 0.5             | ~10.0                           |

##### Key Takeaways:

- **5 hits at matched level:** The core balance target. A properly geared player survives exactly 5 normal hits from a same-level elite mob across all level tiers.
- **2.5 hits unarmored:** Fighting without gear applies a 2.0 gear adjustment multiplier, halving survival time and providing an immediate incentive to equip armor.
- **Vanilla armor utility:** A level 1 player in standard diamond armor survives ~3.5 hits from a level 5 mob, compared to ~1.7 hits unarmored.
- **Enchantment impact:** Protection IV across all 4 armor pieces adds ~1.33 to gear score, shifting damage reduction from 50% to 53.3% (~8% boost in effective survivability).
- **Level-consistent scaling:** Matched combat at level 25 and level 50 both yield the exact same 5-hit threshold.
- **Peak gear cap at 10 hits:** Even with maximum tier equipment (+10 levels above the mob), players still take meaningful damage.

#### Scenario: Sword Damage

| Weapon Scenario                          | Bonus | Weapon Adjustment | Effect on Hits     |
|------------------------------------------|-------|-------------------|--------------------|
| Bare fists (no weapon)                   | 0.00  | 0.50              | 6 hits (2x slower) |
| Half-level weapon                        | 0.25  | 0.75              | 4 hits             |
| Matching weapon (weaponLevel = mobLevel) | 0.50  | 1.00              | 3 hits (baseline)  |
| +4 levels above mob                      | 0.60  | 1.10              | ~2.7 hits          |
| +10 levels above mob (cap)               | 0.75  | 1.25              | ~2.4 hits          |


#### Extensive cases

| Combat Scenario                | Damage Multiplier | Gear Reduction | Gear Adjustment | Hits to Kill |
|--------------------------------|-------------------|----------------|-----------------|--------------|
| Lv1 naked vs Lv1               | 1.00              | 0%             | 2.0             | 2.5          |
| Lv1 naked vs Lv5               | 1.45              | 0%             | 2.0             | ~1.7         |
| Lv1 vanilla diamond vs Lv5     | 1.45              | 50%            | 1.0             | ~3.5         |
| Lv25 matched vs Lv25           | 1.00              | 50%            | 1.0             | 5.0          |
| Lv25 matched + Prot IV vs Lv25 | 1.00              | 53.3%          | 0.935           | 5.4          |
| Lv25 matched vs Lv30           | 1.59              | 41.7%          | 1.17            | 2.7          |
| Lv25 peak gear vs Lv25         | 1.00              | 75%            | 0.50            | 10.0         |
| Lv50 matched vs Lv50           | 1.00              | 50%            | 1.0             | 5.0          |