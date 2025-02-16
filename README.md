# enps_rrt

The ENPS-RRT (Efficient Non-uniform Probabilistic Sample-based Rapidly-exploring Random Tree) algorithm is a path-planning algorithm implemented in C. It uses the Rapidly-exploring Random Tree (RRT) methodology to find paths in environments with obstacles. Here is a brief overview of its components and workflow:

- **Initialization (`init_params` and `init_vars` functions)**: Sets up the parameters and variables needed for the RRT algorithm, including loading the map, removing obstacles, and initializing nodes.
- **Random Sampling (`rnd` function)**: Generates random sample points within the map.
- **Collision Detection (`obstacle_free` function)**: Checks if a new path segment collides with any obstacles.
- **Nearest Node Search (`nearest` function)**: Finds the nearest node in the current RRT to the new random sample point.
- **Tree Extension (`extend_rrt` and `extend_rrt_star` functions)**: Adds new nodes to the RRT, either using standard RRT or RRT* (an optimized version).
- **Iteration (`enps_rrt_one_iteration` function)**: Executes one iteration of the ENPS-RRT algorithm, extending the tree and checking for halting conditions.

The algorithm continues iterating until it reaches the maximum number of nodes or other halting conditions.

For more detailed information, you can explore the source code [here](https://github.com/dtecho/enps_rrt/blob/master/src/enps_rrt.c).
