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

<img width="543" height="445" alt="Screenshot 2026-04-22 191819" src="https://github.com/user-attachments/assets/d2355783-ea67-436d-a633-b2512f34b752" />
<img width="618" height="387" alt="Screenshot 2026-04-22 191757" src="https://github.com/user-attachments/assets/ec5f6d2b-931b-4c72-b9d8-83212dcf7549" />


## W5
### Activity 1
**What's Built**


when there is branching dialogue:
 - there is information to be saved to the journal
   - if the information is a fact, save it to facts
   - if it is a recollection (being sorted), save it to the recollections, with differing information depending on how they categorize it
(i am able to tell what option is chosen in scripts)
   - go to next dialogue node
 - there is NOT information to be saved to the journal
   - go to next dialogue node

**To Be Built**
1) create a reference for how much and how the Player’s sanity is modified (added/subtracted) depending on how a recollection is sorted (correctly/incorrectly)
   - create an (int) SanityValue in the RecollectionNode
   - create a (bool) Real variable in the RecollectionNode
   - check if the player sorts the Recollection according to the (bool) Real variable, or opposes it
2) display current sanity, and have it updated depending on the aforementioned sorting
   - create an (int) SanityMeter variable in the Player
   - if the player sorts the Recollection correctly, add the SanityValue to SanityMeter
   - if the player sorts the Recollection incorrectly, subtract the SanityValue from the SanityMeter
   - create a UI element and reference to it, and set its text equal to the SanityMeter value

### Activity 2
I implemented all of the steps that I mentioned in Activity 1. 


## W6
### Activity 1
Here is my new [Itch Build](https://moon-shroom.itch.io/head-count-playtest-1). Since Milestone 1, I have implemented the sanity system. The goal of this playtest is centered around the game's aesthetic. Does it communicate the vibe of "corporate" within the therapist's office? Additionally, however, do all of the methods of control in the game (mainly the mouse) make sense and flow well?

Notes:
- name tags for different speakers
- bigger UI/text
- cool environment


### Activity 2
1. Because on a color wheel, the larger an RGB value is (either from 0-255 or from 0-1), the closer to black it is, and multiplying the values creates a bigger value than if it was just added or left alone. 
2. If the alpha value is multiplied, it will be less translucent for a similar reason to the answer to the first question. The larger the alpha value is, the less transparent/more opaque the texture will be.
3. The shader gets the UV coordinates from the vectors stored in the mesh.
4. I'll be honest, it's still very confusing to me. However, it is super interesting, and I wouldn't be opposed to working with it in the future.


## W7
1. The data comes from the vectors in the Shiba Mesh
2. The color is blended at the edge of different regions of color because not every surface on the Shiba is a vertex, rather it is polygons that use the data from the vertices to be colored. 
3. Vertex color is quick and messy, like using a large brush on a paint brush. So it's great for assets that are only seen from afar or can be detailed at a later stage.
4. Based on the Shiba's vertex coloring, nothing looks from with the vertex normals.
5. You can use the Tangent data to visualize how a mesh's mapping is working and spot any discrepancies in it.
6. Based on how we are calculating the lighting in step 4, what should be lit on the shiba model has surface normals pointing towards the light, which results in a negative value when plugged into a dot product, thus it is dark. The way we fix this is by (mathmatically) flipping the direction of the surface normals of the shiba before we put it into the dot product.
7. If the blending mode isn't set on something beside Alpha, it won't take the alpha value into account when it is calculating translucency.


## W8
### Activity 1
[Here](https://moon-shroom.itch.io/head-count-playtest-2) is my new itch.io build that was tested this week. My playtesting goals largely revolved around aesthetics, action/consequence legibility, and UI understanding. 

Notes: 
- make textbox darker so text is easier to read
- likes therapist office environment
- indicate that the journal button is a button in some way
  - make tutorial clearer?
- likes the journal UI with the text and next/back buttons
  - feels smooth and it's clear what is happening when you press each button
  - aesthetic is cool/calming (likes the assets I chose)
- sanity bar would be cool (said after I mentioned that I would be implementing that in the future)
- excited to see implementation of memory environment (understood that was what was happening with the scene change)

### Activity 2c
1. Our post processing effect is associated with the pass "FullScreenPassRendererFeature". I knew this because, besides the name, the output preview within the Frame Debugger only started showing the cobblestone texture on that pass and afterwards.
2. At 0.5, the cobblestone texture is at 50% opacity. At 0 is is completely translucent, and at 1 it is nearly opaque (it isn't completely because it is still taking into account the original colors on screen, which it is multiplying with the cobblestone texture values).
3. In simple terms, the float input between 0 and 1 is modifying how strongly the cobblestone texture is overlayed with the original pixels of the screen. More specifically, it is modifying the color values on the cobblestone texture from its original color to white, which doesn't show at all since it is simply multiplying the original pixel value (before post processing) by 1.
4. A standard sine graph modulates between -1 and 1, so by adding one and dividing by two, we are making it only modulate between 0 and 1, which is what the Lerp is meant to take.


## W9
### Activity 1
We chose Minecraft :D
1. Taking Damage -- tinting the skin texture red when taking damage
   - assuming there is already backing logic created, you would just add the tint logic to the taking damage event
2. Warden Darkness Effect -- post processor effect on entire screen which creates a pulsing, super dark vignette
   - if player is within certain proximity to warden + warden sends out darkness, start darkness effect
   - darkness effect created by increasing/decreasing intensity of vignette with a time node of some kind
3. Nasea -- another post processor effect that warps the screen repeatedly
   - assuming other things are built, if something is consumed, check the item ID
   - if it is nasea, start pot-processing effect that overlays the screen with warping
   - check nasea level for how intense the warping should be
   - check potion duration for how long it should last

### Activity 2
<img width="730" height="622" alt="glitch-shader-graph" src="https://github.com/user-attachments/assets/52453679-05ce-4e56-a100-4f76a4625218" />

A problem I solved, which probably isn't what the prompt meant, was that I realized I didn't create the project using the URP, so I had to install the package and reset the shader settings on a bunch of my materials. If that doesn't count, my shader graph uses a Random Range node, and for a bit I couldnt figure out why that wasn't doing anything, until I realized I had to hook it up to a Time node so that it was repeatedly called.

