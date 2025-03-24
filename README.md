# Some Project Videos

## Explanation
These are projects that, while I have decided to place on the backburner to work on other projects, still have some merit worth showcasing. They are typically left behind because of either a lapse in interest on my end or because I would need more experience on specific aspects of their development before I could entertain the idea of releasing them, commercially or otherwise. 

However, it is still my intention to revisit them at some point. In the meantime, I try to work on things that have some connection to these projects so that I might build the required experience and confidence necessary. 

### Disclaimer
Note that these are nothing near finished products. These projects have something interesting worth showing off and aren't going to be impressive on their own. There will be aspects of them that aren't 100% perfect. That doesn't bother me much though, because they won't be relevant to what I found neat about them. Also, there isn't any code publically available for any of these. Sorry. Since I had planned for them to be commercialized and want to revisit them, I don't plan on putting all of the ugly, ugly code out there for people to see. Feel free to ask me for it though. I'll almost certainly say yes. Everything on display has one associated video showing off the aforementioned 'neat' part. Please forgive me for the terrible asset quality - they are placeholders from the internet, Unity prefabs, or (God forbid) my own creations. Eat your heart out.

### 'Untitled Space Game' - Movement
This was intended to be a multiplayer adventure game set in the cold void of space. Taking inspiration from games like Barotrauma, the planned gameplay loop would have revolved around completing missions, exploring the game-world with multiple methods of navigation, and dealing with any of your fellow crewmembers who may have become antagonists. Sadly, I've opted to put this one behind me for now as I need more practice with netcoding before I can commit myself to its development. That being said, I did develop a nifty system for movement, as seen below. 

https://github.com/user-attachments/assets/562a08a6-2f04-4c0a-87a0-c553d8c13b9f

I developed this movement system because I had planned for one major form of movement to be based on the player 'stickying' themselves to surfaces, i.e. magnetically. The setting would have incorporated artificial gravity fields, but a lot of wrecked areas would not have that system online. How it works is quite simple. The little spaceman is casting 16 rays in cardinal directions to determine where exactly the player is. The red square does the same but does so to determine where they can go. In short, the player can only go so far unless the square can detect terrain in the direction they're trying to go. Whilst it looks quite janky, both the maximum distance the player can go and the number of raycasts can be changed and everything will update to accomodate this - the raycasts will always be evenly spaced. What is shown worked well for testing, but would not have been suited for an actual release.

### 'Untitled Card Game' - Turn-based card gameplay.
I think I played Slay the Spire and got annoyed that someone had made such a fun game and I hadn't, so I decided to take a crack at it. Eventually though, I realised my spin on it wouldn't really have worked. Similar to other games of the genre, you choose what cards to play against the enemy/ies and they play some back. My twist was to have it be rigidly turn-based - everyone that can play a card has a speed (which the player could level up if they so chose.) The more speed you had, the more cards you could play before the enemy. Think micro turns within the actual turns. I still think this is an interesting idea, but I quickly realised that it was too confusing of a system to be worth really making. On the bright side, cards and enemies are very easy to produce because of the game logic - both have ScriptableObject 'X...Data' objects that control their overall values alongside their actual enemy/card/etc. logic. Cards have a list of 'Effects' which apply to their target. Enemies have a list of preset cards that they can choose to play. 

https://github.com/user-attachments/assets/c017a304-13de-4dcd-afc5-2ea2892f4f99

As standard for games like this, the player has health and 'stamina', the de-facto resource for playing cards. I wanted this to have a snap of realism to it. As everything is played in a very specific order, I decided to make stamina only regenerate a little bit - half of the total stamina cost of your last turn plus a little extra. It adds some decision-making to the mix. Consider: the enemy you're fighting is very slow, but he's tanky and hits like a truck. Do you:
- A: Use all of my cards up to kill him as quickly as possible?
- B: Play decisively, losing some offensive/defensive value but maintaining just enough stamina to keep fighting?
- C: Focus almost entirely on defence and whittle him down over time before hitting him with the most devastating combo you have?

With stamina recharging dynamically, the entire game changes. Sometimes enemies would be faster than you, sometimes slower, sometimes you'd have the same speed. Sometimes you'd get a great early hand. Sometimes you'd get nothing. It would be up to you to decide exactly what you'd be willing to do with one hand when you don't know if the next will be better or if you would have the stamina to play it. This is something that I'd really like to look into further. As of now however, it's not a priority.

