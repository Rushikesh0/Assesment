# Assesment
The code starts by defining a function get_path_for_drone that takes in the starting position, ending position, and time of a drone, along with the list of all drones and the grid size. This function returns the path that the drone should follow to reach its destination.

The first step in the function is to create a 2D grid of the specified size using a nested list comprehension. Each element in the grid represents a cell and is initialized to zero.

Next, the function loops through all the drones in the list and marks their starting and ending cells with a unique integer value. The integer value is calculated by taking the index of the drone in the list and adding 1 to it, so that the value starts from 1 instead of 0. This ensures that each drone is assigned a unique value on the grid.

After marking the starting and ending cells, the function uses the A* search algorithm to find the shortest path from the starting cell to the ending cell. A* is a pathfinding algorithm that uses a heuristic function to estimate the distance from the current cell to the goal cell. The algorithm then chooses the cell with the lowest total cost (distance from start + heuristic) as the next cell to explore.

Once the A* algorithm has found the shortest path, the function returns the path as a list of (x, y) coordinates.

Finally, the main code loops through all the drones in the input list and calls the get_path_for_drone function for each drone. The resulting paths are stored in a dictionary with the drone index as the key and the path as the value. The dictionary is then printed to the console.
