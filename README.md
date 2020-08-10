# The-Garden-of-Eden-v1.0
jdk11
2d space, 1000x1000

##Space
Rules:
On two individuals adjacently requesting reproduce, create child (see reproduce rules)
If <10 individuals this tick, spawn +1 next tick


##Spawn
Rules:
The longest lasting individual becomes the template.
Create new individual with linear regression model

##Food - 
Properties:
Grant 100 Health

##Blocks -
Properties:
Cannot be passed through.
Can be picked up

##Gossip -
Properties:



##Individual (Fills 1 space with -
Properties:
Health (decay 1 per tick, no cap)
On Health = 0, die, become food worth 200 health.
Inventory (Stack 2 Blocks)
Memory (infinite size)

Inputs:
Radius from closest food
Radius from closest individual
Memory (8 values)
Current Health
Recieve Gossip (8 values)
Recieve reproduce request



Outputs:
Move 1 up
Move 1 down
Move 1 left
Move 1 right
Attack (Deals 50 Health to 1 up, 1 down, 1 left, and 1 right)
Gossip up (8 values)
Gossip down (8 values)
Gossip left (8 values)
Gossip right (8 values)
Request reproduce
Overwrite memory (8 values)

Values for weight (endpoints):
o(x) = 1/(1+e^-x) = value of hidden node given the weights
x = Sum[n -> s] (wn*an)
