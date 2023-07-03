
# Cub3d
This project is about making 3D game in C language using mlx library

MiniLibX is a compact graphics library that enables you to perform essential tasks for displaying visuals on screens.
__________________________________________________________________________________________________________________
## Compiling on macOS
The compilation process for MiniLibX on macOS can be somewhat complex due to its dependencies on AppKit and OpenGL. Properly linking these components is crucial.
you could add the following rule to your makefile

    -Lmlx -lmlx -framework OpenGL -framework AppKit

_____________________________________________
### How to start raycasting after parsing part be ready

1. initialize mlx
2. Draw Mini Map
3. Draw Mini Player
4. Define the keys for all directions (forward, backward, left, right, rotate left, rotate right)
5. Draw the walls
6. load the textures on your walls
______________________________________________
### mlx_hook

Hooking into events It allows you to register to any of the below events with the call of hook function

> prototype

    void mlx_hook(mlx_win_list_t *win_ptr, int x_event, int x_mask, int (*f)(), void *param)

we used it on *int main* function with calling the *RELEASE, PRESS and DESTROY* events

<img width="717" alt="events in mlx" src="https://github.com/realdahh/Cub3d/assets/111651235/356b4041-17c0-48be-90f3-764f5c161853">

_____________________________________________

### calculate with radian
        M_PI = 3.1415   π
        1π   = 57.295   degree
        
    2 * M_PI = 6.2831   π
    6.2831   = 359.999  degree (full circle)

_____________________________________________

To run this Game run this command 

    ./Cub3d maps/spiral_map.cub 
(Tne name of the program) and (The path to the map.cub)
