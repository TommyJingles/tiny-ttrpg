# Micro RPG
Fit the rules in as few pages as possible.
Everything is subject to change.


## Title
work in progress
 

## Dice
we use six-sided dice only, represented as 'd'.
the number before 'd' is the number of dice for that roll.
multiple dice colors is nice for handling multiple roles simultaneously.
> example: "2d + 1d + 2" means "two dice, plus one dice, plus two"


## Keywords
Keywords are `highlighted` and used for references, mapping rules, so on. There are many keywords similar to MtG and the text which defines the keyword *is* the rule to follow.

## Stats
| Keyword | Description |
| --- | --- |
| `Health` | A measure of vitality. Gain the `Unconscious` condition if value becomes zero or less |
| `Stamina` | A measure of ???. Gain the `Fatigue` condition if value becomes zero or less |
| `Mind` | A measure of ???. gain the `...` condition if value becomes zero or less |
| `Speed` | A measure of distance a character can reposition with a `Move Action` |
| `Carry` | A measure of carry capacity, gain the `Encumber` condition if the sum of equipped item weights are greater than value |


## Attributes 
| Keyword | Description |
| --- | --- |
| `Brawn` | brute strength |
| `Agile` | nimbleness, coordination, marksmanship |
| `Will` | determination, endurance, resistance |
| `Logic` | well-read, knowledgeable, technical |
| `Intuition` | experience, impulse, gut-feeling |


## Saves
Specialized dice rolls for preventing situational consequences.

| ... | ... |
| --- | --- |
| ... | ... |



## Conditions
States in which a character can experience.
| Keyword | Description |
| --- | --- |
| `Unconscious` | ... |
| `Fatigue` | ... |
| `Encumber` | ... |
| `Bleeding` | ... |
| `Burning` | ... |
| `Freezing` | ... |
| `Restrained` | ... |


## Combat
| Keyword | Description |
| --- | --- |
| `Turn Order` | At the beginning of combat sort characters high to low by `Initiative` rolls |
| `Round` | One full iteration through the `Turn Order` |
| `Turn` | A character's chance to perform actions (see below) |
| `Move Action` | Reposition, can convert to one `Secondary Action` |
| `Primary Action` | one per turn, can convert to one `Move Action` or one `Secondary Action` |
| `Secondary Action` | one per turn by default, additional through `Action` conversion |
| `Free Action` | Technically unlimited per turn by default, keep it reasonable |

#### Initiative
rolls determine order, can delay your turn at will at any time. Can skip as well.

#### Move Actions
| Keyword | Description |
| --- | --- |
| `Move` | generic, move up to your speed, presumed to be a quick pace |
| `Shift` | Change from `Prone` to `Standing` or `Crouch` |
| `Jump` | ... variations for long, high, floating |
| `Climb` | --- |
| `Swim` | --- |
| `Fly` | --- |

#### Primary Actions
| Keyword | Description |
| --- | --- |
| `Attack` | (see below) |
| `Delay` | Permanently move your `Turn` farther down the `Turn Order` |
| `Fetch` | Get an item from your bag or nearby location that isn't immediately accessible |
| `Recover` | Take a beat to regain a `Stamina` or `Mind` value, or make a `Save` roll |
| `Disengage`| --- |


#### Secondary Action Options
| Keyword | Description |
| --- | --- |
| `Use` | use an item in your hand (ex: dring a potion, blow war horn) |
| `Equip` | move an item on your body or easily accessible into hand |
| `Drop` | drop an item in your hand, a backpack? |


#### Free Actions
Simple things like make a facial expression or yell something brief.


#### Defend
This `Action` may be performed off-turn when Attacked

#### Attack Steps
1. Attacker declares Defender as Target
    - in the case of multiple targets, they must be declared in order
    - AoE, one Attacker Roll is compared to individual Defender Rolls
2. Attacker and the Defender roll, respectively
    - Energy is expended per d6 roll (unless specified otherwise)
    - Not consuming Energy automatically defaults dice values to 1
3. Rolls are compared:
    ```
    difference = Attacker Sum - Defender Sum

    IF: Atk > Def (Attacker Wins)
        - Defender takes damage equal to the difference
            - NOTE: some keywords may change the damage calculation, see `Viscous`
        - modifiers may apply
    IF: Atk = Def (Tie)
        - No damage is applied
        - modifiers may apply
    IF: Atk < Def (Defender Wins)
        - Attacker takes damage equal to the difference / 2 (round down)
            - NOTE: some keywords may change the damage calculation, see `Juggernaut`
        - modifiers may apply
    ```

#### Damage Types
Damage types are arbitrary, feel free at add and remove from this list.
Think of them loosely like Pokemon type charts where some are better or worse when applied to another type.
| Type | Description |
| --- | --- |
| `Blunt` | ... |
| `Pierce` | ... |
| `Edge` | ... |
| `Heat` | ... |
| `Cold` | ... |
| `Poison` | ... |
| `Electric` | ... |

#### Examples
- Default dice value to 1 if no energy is spent for it.
- If energy was not spent at all, the roll is represented as: Nd!, where N is total number of dice
- If energy was not spent for some dice, Nd!M where M are the dice not energized.

> Attacker Wins
> - Attacker Roll:  weapon: 1d6 + Brawn = [4] + 1 = 5
> - Defender Roll:  armor: 1d6 + Brawn = [2] + 1 = 3
> - defender takes 2 damage

> Defender Wins
> - Attacker Roll:  weapon: 1d6 + Brawn = [2] + 1 = 3
> - Defender Roll:  armor: 1d6 + Brawn = [4] + 1 = 5
> - Attacker takes 1 damage (difference / 2)


## Magic
The idea is to build up a spell from the categories below, each adding additional cost and changing the difficulty
| Criteria | Description |
| --- | --- |
| Method | immediate, verbal, gesture, component, ritual |
| Targets | keywords, characters, areas |
| Range | self, adjacent, close, near, ... far |
| Modifers | conditional, damage type + dice |

    Targeting stats, attributes, saves, existing modifiers, 
    items, equipment, attachments, actions ...

    cast and effect durations, damage types, target range, difficulty
    Computing cost / dice to roll / modifiers


## Items
|Name|Size|Wt|Quality|Value|Keywords / Description|
|---|---|---|---|---|---|
|Axe|avg|3|com|5 sp|`Item` `Equippable` `Tool` `Weapon: 3d + Brawn (Edge)`|
|Bow|avg|2.5|com|10 sp|`Item` `Equippable` `Range: (Arrow)` `Weapon: 2d + Agile (Pierce)`|
|Arrow|avg|0.5|com|1 cp|`Item` `Projectile: (Arrow)` `Weapon: 1d + Brawn (Pierce)`|
|Ration|Small|1|common|1 sp|`Item` `Consumable` `Food: 10`|
|Shield|avg|4|common|12 sp|`Item` `Equippable` `Armor: 1d`, `Weapon: 1d + Brawn (Blunt)`|
| \<T> Gem |Tiny|0.1|great|1.2k gp| *:Where \<T> is `Dmg Type`*<br>Keywords: `Item` `Attachment` `Gem`<br>Attach to `Weapon`, target gains: *+1d (T)*<br>Attach to `Armor`, target gains: *+1d {T}* |

    TODO: Weapons, Armors, Tools, Consumables, ...

#### Keyword Modifier Examples
buffs / nerfs targeting any value for any reason, the affect is the rules much like MtG cards

| Name | Target | Description / Requirements |
| --- | --- | --- |
|`Juggernaut`| `Armor` | double this item's armor roll, attacker cannot take damage from this item.<br>If defender wins, subtract this roll from the difference before applying damage to the Attacker |
|`Viscous`| `Weapon` | If an attack is successful, instead of using the difference as damage, optionally use this item's full attack roll instead |
|`Entangle`| `Weapon` or `Trap`| If this item's attack roll crits, defender must Brawn save or becomes Entangled |
|`Rapid Heal`| `Consumable`| This item's regen value is doubled if used immediately after a Breathe primary action or outside of combat |
|`Laborious`|`Equippable`| Putting this equipment item on or off takes several minutes, cannot be done in combat |


## Other Rules / Mechanics
Currency

Sizes 

Forms: corporeal, incorporeal, swarm

Mounts and Vehicles

Buying and Selling

## Generator Formulas and Lookup Tables
#### Objectives
    destroy target, rescue hostage, exterminate, survival, last man standing ...

#### Environments
    catacombs, seaside cave, destroyed space station, haunted house, ...
    ambient effects

#### Rooms
    room shape and dimensions, POIs, connections, descriptions, area / ambient effects

#### Points of Interest (POIs)
    chests and items, wells, alters, furniture, shelving, art, lighting, ...
    traps, puzzles

#### Connections
    direction, barriers, locks
    doors, hallway, holes, stairs, elevators, teleports, ladders, ropes

#### NPCs
    I think there should be a few generic defaults as starting points
    Mobs could have a difficulty rating which converts to points
    Some aspects have requirements / prerequisites
    Some aspects are penalties, which can add points back to the pool
    Aspects:
        Form: Creature, Incorporeal, Artifact ...
        Size: tiny, small, medium, large ... gigantic
        Physical features: sensors, limbs, wings, claws, stingers ...
        Stats, Attributes, Conditions, Custom Abilities
        Equipment, Items, Spells, Misc Modifiers

#### Items
    Point buy, with a giant list of defaults
    Rules for determining value, quality, ...

#### Events
    There should be triggers for generating random events in and out of combat.
    second wave of enemies, ambient effects, NPC appearances, sudden room changes ...

## Roll-Driven NPCs
A deterministic way for dice to control NPCs, including enemies in and out of combat.
Will need a logical graph with explicit values to determine behavior. There should be very little ambiguity or arguing over what an NPC should do.