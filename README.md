# ---Optimization With Singleton Pattern---
__Before Optimized Singleton In Game__:
<img width="1074" height="551" alt="image" src="https://github.com/user-attachments/assets/beeae851-aafd-4fd2-bfc1-90d6a326245b" />
<img width="1112" height="543" alt="image" src="https://github.com/user-attachments/assets/244dec5f-bc9b-48bd-804e-f76772fd232f" />
# Blueprints before optmization
<img width="1118" height="428" alt="image" src="https://github.com/user-attachments/assets/08ec440d-51fa-4830-999f-360e3fe97f00" />
<img width="1107" height="438" alt="image" src="https://github.com/user-attachments/assets/e3c2101c-79fc-44ba-96c1-b2770547f9fb" />
# Unreal Insights 
<img width="1024" height="549" alt="image" src="https://github.com/user-attachments/assets/6daf7645-3680-4634-965c-9aec9166431d" />
<img width="1024" height="505" alt="image" src="https://github.com/user-attachments/assets/9c7e55e7-4f7c-4fe9-b96a-d53ff33c1eb5" />
After Optimized Singleton In Game:
<img width="1022" height="502" alt="image" src="https://github.com/user-attachments/assets/ce46990b-e0de-4823-82df-9cace363dd0c" />
# Blueprints After Optimization
<img width="1020" height="422" alt="image" src="https://github.com/user-attachments/assets/7d92c126-ceef-4f94-912d-0cbc0c636281" />
<img width="1021" height="416" alt="image" src="https://github.com/user-attachments/assets/01fad8ac-6099-4ff4-8682-a8e855af26a6" />

# Reflection:
For my project I decided to use a singleton pattern that has the ability to find a specific actor in the level. In this case the singleton is only looking for a
specific type of BP_ThirdPersonCharacter inside the game instance. There are 38 different actors inside the level and at the start i'm trying to use the node "Get Actor of Class".
This node searches every single actor in the level on event tick and tries to find the correct actor and if it does it displays a print message. Using this method caused performance issues
and was constantly lagging the game. To optimize this, I decided to make another function within the game instance that recieved an input of type BP_ThirdPersonCharacter. Based on the input it would display a message to t
the screen showing that there was only a single instance of the actor in the world. Instead of searching through every single actor on event tick it set the variable on event begin play inside the third
person character forcing the game to only recognize this one actor. My profiling process revealed that the game showed signaficant improvements when I change the way I was searching for a specific actor
using the singleton pattern compared to doing it every second in event tick. There are many cases within development where searching for a specific actor can be constly, in my example I decided to find an 
alternative way to lower the performance cost of this action which would in turn improve overall gameplay.
