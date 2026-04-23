# GDIM 33 In-Class Activities
## W1
### Activity 1
1. [My Moodboard](https://app.milanote.com/1W862R1ypWoK46?p=ospQOPniLN5)
2. I really want to create an eerie experience with focus on story, rather than intense gameplay. Atmosphere is what I'm excited for. This will probably require use of the particle and dialogue system. I want to do 2D, but I will have to continue to brainstorm how to do what I want to do without a 3D space.
3. This is easy: we all want to do something eerie. Mila is most similar to me in that regard, in that she wants to create a more psychological experience that thrills the player through atmosphere, rather than intense gameplay.
4. Eric mostly likes FPS and multiplayer games. Not horror games. I'm kind of in agreement with that latter half. Despite wanting to make a horror-adjacent game, I'm most interested in chill, player-centric experiences- think Minecraft or Stardew Valley. Personally, I'm not into FPS, since it stresses me out but to each their own. 

### Activity 2
[My Project Breakdown](https://docs.google.com/drawings/d/1epRFtQUTlTe-iDQQwPYfwYcRhpC2QUZgBSj0izOXRdU/edit?usp=sharing)

## W3
### Activity 1
[Project Breakdown Updated](https://docs.google.com/drawings/d/1epRFtQUTlTe-iDQQwPYfwYcRhpC2QUZgBSj0izOXRdU/edit?usp=sharing)

### Activity 2
#### Why is it advantageous to save the event name for the explore-to-dialogue state transitions as Scene variable ("clickNpcEventName")
Saving the event name as a string prevents accidental typos when triggering the event in another graph, since you need to enter the event name manually, and it won't alert you if the event doesn't exist with a red underline like it would in code. 

#### Describe how using at least one Debug.Log() node helped you test your Graphs at an intermediate step.
Using a Debug.Log() to check if the mouse click was registering, and then another to see if the event was triggered helped me find where the code wasn't connecting properly, since the mouse was registering, but the event wasn't triggering. Thus, I knew the error was in the logic for the event triggering, not in the Mouse Down node.

#### Is the Set Cursor Lock State relevant to your Vertical Slice? Why or why not?
No, since I will not be using the mouse to control the camera, so there is no need to lock/unlock it when pulling up UI elements.

#### Is the concept of a "game state" relevant to your Vertical Slice? Why or why not?
Yes, as there are two main states in which gameplay occurs: each with their own seperate logic systems and set transitions between them. 


## W4
### Activity 1
Team: Eli, Milla, Ruth, Minjoo


In my game's current state, you can click through dialogue, and choose different options and get different dialogue results (branching dialogyue). Additionally, the Journal button can open and close the Journal UI. For a playtesting goal, I want to know if the speaker is clear within the dialogue, as occasionally the player speaks in lines outside of the branching dialogue. 


Notes: 
- Journal button click also triggers `AdvanceDialogue()` method, so the player misses dialogue when the Journal is open
- it _is_ clear who is speaking thanks to the italics when the player speaks (which is placeholder for a different font)
- dialogue system is super smooth
- would like to see the unbuilt environment I have planned


### Activity 2
A writer could write the dialogue without ever opening the scripts! Although, in its current set-up, they would have to open Unity and navigate the file system there to edit the dialogue nodes. That being said, there is no limit to the number of dialogue nodes that a writer could create. They would never need to open up Visual Studio Code. 

The "Regenerate Nodes" button basically refreshes what methods (nodes) have been made avaiable (created) since the last refresh. If you wrote a method that isn't showing up in Visual Scripting, try refreshing the nodes. 


