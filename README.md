# Escape-Room
Escape-Room is an exploration of hierarchical planning with Companions. We designed "escape room" challenges and use a companion agent to implement reasoning to solve the challenge. In these challenges, our agent is trapped in a room. In order to solve the challenge, the agent needs to fetch the key to unlock the door and escape the room.
## Overview
Escape-Room consists of:
1. EscapeMt, which defines methods for solving the challenges.
2. EscapeOntologyMt, which initializes the methods.
3. Six "levels," which each contain a microtheory that contain facts that represent a challenge that the agent must solve. In each level, the agent must fetch the key to escape from the room.

## Usage
1. Download each of the krf files and start a companion.
2. Run (doClearWorkingMemory).
3. Use "Load Flatfile" in session-reasoner to load EscapeMt, EscapeOntologyMt, and LevelOneMt.
4. Run (fetch K1 LevelOneMt)
5. Search MyEscapePlanMt in the knowledge base to see the agent's actions in this level.
6. If you want to run the next level, first run (doClearWorkingMemory), (doForgetKBMt MyEscapePlanMt), and (doForgetKBMt < mt-name >) where < mt-name > is the name of the level you just ran (i.e LevelOneMt).
7. Load the level you want to run next as a flatfile.
8. Run (fetch K1 < mt-name >) where < mt-name > is the level you want to run. Repeat steps 5-8 for the rest of the levels.
9. Important: If you wish to run a certain level more than once, in between each run you must forget the microtheory and reload the flatfile. 


# Levels
### Level 1
There is a key on top of the box. The agent fetches the key and escapes the room. 
![Level1](/Images/Level1.png)

### Level 2
The key is in a jar on a table. There is also a hammer on the table. The agent fetches the hammer, breaks the jar, fetches
the key and escapes the room.
![Level2](/Images/Level2.png)

### Level 3
The key is on a table, but there a three boxes on top of it. The agent removes the top box, and then removes the box that was underneath it, then removes the last box on top of the key. Then the agent fetches the key and escapes the room.
![Level3](/Images/Level3.png)

### Level 4
There is a jar on the table. The key is inside the jar. There is a box on top of the jar. There is also a hammer on the table,
and there are two boxes on the hammer. The agent removes the box from on top of the jar. Then, the agent removes the top box
from the hammer, and then removes the other box from the hammer. The agent breaks the container with the hammer, fetches the
key, and escapes the room.
![Level4](/Images/Level4.png)
<a><img src=/Images/Level4.png height="48" width="48" ></a>

### Level 5
There is a jar on the table which contains another jar. The inner jar contains the key. There is a box on top of the jar. There are two hammers on the table. One of the hammers has two boxes on it. The agent takes the box off the jar. Then the agent fetches the uncovered hammer and smashes the outer jar. The hammer breaks in the process. The agent takes each box off the covered hammer, fetches it, and uses it to break the inner jar. The agent fetches the key and escapes the room.
![Level5](/Images/Level5.png)

### Level 6
There are two jars on the table. One has a key in it, and one has a hammer in it. The jar containing a key has one box on it, and the jar containing a hammer has two boxes on it. There is also a hammer on the table. The agent takes the box off of the jar containing a key. It uses the uncovered hammer to break the jar. The agent fetches the key and escapes the room. This level demonstrates that the agent ignores the chance to smash open the second jar, and instead takes the most straightforward path to achieving its goal.
![Level6](/Images/Level6.png)
