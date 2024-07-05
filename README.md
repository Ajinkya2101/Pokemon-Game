Pokémon Battle Simulation Documentation
This documentation provides an overview of a Pokémon battle simulation game implemented in Python. The game includes the basic structure of Pokémon, their moves, trainers, and battles between trainers.

Overview
The game consists of several classes to represent Pokémon, moves, trainers, items, and the battle mechanics between trainers. The structure is designed to simulate Pokémon battles with different types, moves, and items.

Classes
Pokémon
The Pokémon class represents a Pokémon with various attributes and methods.

Attributes
name: Name of the Pokémon.
type: Type of the Pokémon (e.g., Fire, Water).
health: Health points of the Pokémon.
attack: Attack stat of the Pokémon.
defence: Defence stat of the Pokémon.
special_attack: Special attack stat of the Pokémon.
special_defence: Special defence stat of the Pokémon.
speed: Speed stat of the Pokémon.
level: Level of the Pokémon.
experience: Experience points of the Pokémon.
moves: List of moves the Pokémon can use.
is_wild: Boolean indicating if the Pokémon is wild.
Methods
perform_attack(move, opponent): Performs an attack on the opponent Pokémon using the specified move.
take_damage(damage): Reduces the health of the Pokémon by the specified damage amount.
gain_experience(exp): Increases the experience points of the Pokémon and checks for level up.
level_up(): Increases the level and stats of the Pokémon.
learn_move(move): Adds a new move to the Pokémon's list of moves.
get_stat(stat): Returns the value of the specified stat.
Move
The Move class represents a move that a Pokémon can use in battle.

Attributes
name: Name of the move.
type: Type of the move.
power: Power of the move.
accuracy: Accuracy of the move.
category: Category of the move (Physical or Special).
effect: Optional effect of the move.
Methods
apply_effect(target): Applies the effect of the move to the target Pokémon.
Trainer
The Trainer class represents a Pokémon trainer.

Attributes
name: Name of the trainer.
team: List of Pokémon in the trainer's team.
inventory: List of items the trainer possesses.
Methods
catch_pokemon(wild_pokemon): Attempts to catch a wild Pokémon using a Pokeball.
use_item(item, target): Uses an item on the target Pokémon.
battle(opponent): Initiates a battle with another trainer.
choose_pokemon(): Prompts the trainer to choose a Pokémon from their team.
choose_move(pokemon): Prompts the trainer to choose a move for the specified Pokémon.
Item
The Item class represents an item that can be used by a trainer.

Attributes
name: Name of the item.
type: Type of the item.
effect: Effect of the item when used.
Methods
use(target): Uses the item on the target Pokémon.
Pokeball
The Pokeball class represents a Pokeball used to catch Pokémon.

Attributes
name: Name of the Pokeball.
catch_rate: Catch rate of the Pokeball.
Subclasses
FirePokémon
A subclass of Pokémon representing Fire-type Pokémon.

WaterPokémon
A subclass of Pokémon representing Water-type Pokémon.

PhysicalMove
A subclass of Move representing physical moves.

SpecialMove
A subclass of Move representing special moves.

Example Usage
Creating Pokémon
python
Copy code
charmander = FirePokémon("Charmander", 45, 60, 40, 65, 45, 60, 1, 0, [], False)
squirtle = WaterPokémon("Squirtle", 45, 40, 60, 45, 65, 40, 1, 0, [], False)
Creating Moves
python
Copy code
fire_punch = PhysicalMove("Fire Punch", "Fire", 75, 100, lambda target: target.take_damage(10))
water_gun = SpecialMove("Water Gun", "Water", 40, 100)
Teaching Moves to Pokémon
python
Copy code
charmander.learn_move(fire_punch)
squirtle.learn_move(water_gun)
Creating Items
python
Copy code
pokeball = Pokeball("Pokeball", 0.5)
Creating Trainers
python
Copy code
trainer1 = Trainer("Ash", [charmander], [pokeball])
trainer2 = Trainer("Misty", [squirtle], [pokeball])
Starting a Battle
python
Copy code
trainer1.battle(trainer2)
This documentation provides an overview of the key components and usage of the Pokémon battle simulation game.





