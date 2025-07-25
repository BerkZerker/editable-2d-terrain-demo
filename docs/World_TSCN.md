# World.tscn Documentation

This scene (`World.tscn`) is the main scene for the destructible terrain demo. It sets up the basic structure for the game world, including the terrain chunks and the player.

## Scene Structure

*   **World (Node2D)**
    *   This is the root node of the scene.
    *   It has the `World.gd` script attached to it, which handles all the logic for terrain generation, modification, and overall game management.
    *   **Script:** `res://scripts/World.gd`

*   **Chunks (Node)**
    *   This is a child node of `World`.
    *   It acts as a container for all the `Chunk` instances that are generated by the `World.gd` script.
    *   It's a simple Node, primarily used for organization in the scene tree.

*   **Player (PackedScene Instance)**
    *   This is an instance of the `Player.tscn` scene.
    *   It's a child node of `World`.
    *   The player character will interact with the destructible terrain.

## Extending and Maintaining

*   **Adding New Elements:** To add new game elements (enemies, items, etc.), you can add them as children of the `World` node or create new container nodes for better organization.
*   **Modifying Player:** The `Player` node is an instance of `Player.tscn`. To modify the player's behavior or appearance, you should open and edit `Player.tscn` directly.
*   **Scene Setup:** The `World.gd` script dynamically generates the terrain chunks. You generally won't need to manually add `Chunk` nodes to this scene.
*   **Debugging:** The `World.gd` script includes debug drawing and input. You can enable/disable these features or add your own for easier development.
