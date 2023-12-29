# NPCS 

NPCs in many games are pretty useless. Particularily the ones in Starbound. They are usually many things:
- dumb
- stiff
- lacking of presonality
- indefinitely stand in a single spot for eternity
- have pre-set behavior OR very simple predictable routines.

I want the NPCs in Celestial to be anything but those. So I have devised a surprisingly simple system to make them feel more 'real':
- Put a solid amount of effort into making their pathfinding decent.
    - Shouldn't be TOO hard compared to other games, because unlike in Starbound the terrain generation is going to actually be acceptably reasonable
    - Make them able to running fairly fast
- NPC interactions.
    - most NPCs treat the player as if they were also an NPC.
        - this will make it harder overall, but easier to 
    - NPCs talk about things that actually happened
    - NPCs interact in more physical ways as well, such as hugging or dancing
        - For example, in Genshin impact, groups of enemies will do silly things like having dance competitions or the like
        - Give them plenty of things they can use to interact, such as board games or sports balls
    - NPCs have emotions. Just like an enum or something with a bunch of emotions that an NPC can have
        - More on how emotions are triggered later
        - kinda like a temporary personality
    - NPC interactions can have lasting effects
        - They remember things that happen (like a list of memories or something)
        - they make profiles of the other characters (NPC or otherwise) and those effect how they interact with other characters
            - For example, if most of their memories involving someone are negative, they will talk more negatively about them and not treat them as nicely.
        - interactions can modify an NPCs emitions or personality
    - NPCs have a personality, which is not just an enum of personalities but a more complex data structure that could be generated procedurally or hand-crafted
        - how they react to things (for example, if another character insults them)
        - the interactions that they can initiate (for example, starting / continuing a conversation, or going to the fridge and getting a snack)
        - things that they like / dislike
            - Could be a simple set of values that help decide what they're opinion of something will be "sour=1.0, bitter=-0.5, "
        - the kinds of clothes that they like to wear
        - Really, most things about an NPC other than their physical existence should be part of the personality
    - Try to do something similar to The Sims, where NPCs can have life events and stuff like that
        - For the sake of making things actually doable, only do it for NPCs that are important
            - determining important NPCs could be as simple as being the ones that the player has interacted frequently with.
    - Treat the player like an NPC
        - All of the data that an NPC has should be stored in the player as well, 
    - use something like the visitor patter, where each interaction is written in code and it can visit the NPCs involved with the interaction and modify them.