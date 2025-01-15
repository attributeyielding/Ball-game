This Repo for  3D Ball game. It enables the player to collect objects, updates the score on the UI, and displays a "You Win!" message when all objects are collected. Here's a breakdown of its functionality:

Key Features:
Movement:

The FixedUpdate method handles player movement by applying force to the Rigidbody component based on user input (Horizontal and Vertical axes).
This allows smooth physics-based movement for the player object.
Collecting Items:

The OnTriggerEnter method detects when the player collides with an object tagged as "Pick Up".
The collided object is deactivated (SetActive(false)), effectively "collecting" it.
The score (count) is incremented, and the UI is updated via the SetCountText method.
UI Updates:

The countText displays the current score.
When the player collects all 12 items, the winText displays "You Win!".
Initialization:

In the Start method, the Rigidbody component is initialized, the score is set to zero, and the UI text is cleared.
Suggested Improvements:
Scalability:

Add a configurable variable for the total number of items required to win. This avoids hardcoding 12 in the script.
Input Flexibility:

Consider using Unity's newer Input System for more flexible input handling.
Feedback for Collection:

Play a sound effect or particle effect when an item is collected for better feedback to the player.
Win Condition:

Add a delay or transition when the player wins (e.g., load a new level or restart the game).
