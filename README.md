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

### Activity 
#### Why is it advantageous to save the event name for the explore-to-dialogue state transitions as Scene variable ("clickNpcEventName")
Saving the event name as a string prevents accidental typos when triggering the event in another graph, since you need to enter the event name manually, and it won't alert you if the event doesn't exist with a red underline like it would in code. 

#### Describe how using at least one Debug.Log() node helped you test your Graphs at an intermediate step.
Using a Debug.Log() to check if the mouse click was registering, and then another to see if the event was triggered helped me find where the code wasn't connecting properly, since the mouse was registering, but the event wasn't triggering. Thus, I knew the error was in the logic for the event triggering, not in the Mouse Down node.

#### Is the Set Cursor Lock State relevant to your Vertical Slice? Why or why not?
No, since I will not be using the mouse to control the camera, so there is no need to lock/unlock it when pulling up UI elements.

#### Is the concept of a "game state" relevant to your Vertical Slice? Why or why not?
Yes, as there are two main states in which gameplay occurs: each with their own seperate logic systems and set transitions between them. 
