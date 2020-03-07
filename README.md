# Escape-Room
Knowledge representation and reasoning system to design and solve "escape room" challenges.
## Overview
Escape-Room is an exploration of hierarchical planning with Companions and CogSketch. Our system is split into three sections:
1. EscapeMt, which defines methods for solving the challenges.
2. EscapeOntologyMt, which initializes the methods.
3. Four "levels," which each contain a microtheory that contain facts that represent a challenge the agent must solve. In each
level, the agent must fetch the key to escape from the room.
## Levels
### Level 1
There is a key on top of the box. The agent fetches the key and escapes the room. 
### Level 2
The key is in a jar on a table. There is also a hammer on the table. The agent fetches the hammer, breaks the jar, fetches
the key and escapes the room.
### Level 3
The key is on a table, but there a three boxes on top of it. The agent removes the top box, and then removes the box
that was underneath it, then removes the last box on top of the key. Then the agent fetches the key and escapes the room.
### Level 4
There is a jar on the table. The key is inside the jar. There is a box on top of the jar. There is also a hammer on the table,
and there are two boxes on the hammer. The agent removes the box from on top of the jar. Then, the agent removes the top box
from the hammer, and then removes the other box from the hammer. The agent breaks the container with the hammer, fetches the
key, and escapes the room.


