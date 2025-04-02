# mercy-maze_project
# The Maze Project 👨‍🎓 

(https://github.com/Macywahome/mercy-maze_project)

This project is a first person `3D` maze game. Similar to Wolfenstein or Doom, minus enemies and weapons, although they may be added later. It was made using `SDL2` and `C`. It runs on Mac OS X and Linux/Ubuntu. The game uses the technique raycasting to create the apparent `3D` nature of the maze. The Maze is a 3D Maze game that uses ray casting to render a 2D map into a 3D navigable world! 

The Maze was written  in C using `SDL2` library. Deveploment was performed using Ubuntu 14.04 LTS - gcc (Ubuntu 4.8.4-2ubuntu1~14.04) 4.8.4

### About SDL2 💻
Simple DirectMedia Layer is a cross-platform development library designed to provide low level access to audio, keyboard, mouse, joystick, and graphics hardware via OpenGL and Direct3D. It is used by video playback software, emulators, and popular games including Valve's award winning catalog and many Humble Bundle games.

## Requirements to Play
- Mac OS X or Linux/Ubuntu
- SDL2

If you don't have SDL2 installed download the installation script <a href="https://s3.amazonaws.com/intranet-projects-files/holbertonschool-low_level_programming/graphics_programming/install_SDL2.sh">here</a>. Then find the script and run it in your terminal:
```groovy
$ ls
install_SDL2.sh
$ chmod 755 install_SDL2.sh
$ sudo ./install_SDL2.sh
```

## Start the Game
First step is to clone the repo:
```groovy
git clone [https://github.com/Macywahome/mercy-maze_project]
```

Compile all .c files in the maze directory:
```groovy
@pc:~/maze$ gcc -g -Wall -Werror -Wextra -pedantic -I/usr/local/include/SDL2 ./src/*.c -o maze -L/usr/lib/x86_64-linux-gnu -lSDL2 -lm
```
Alternatively, just use the make command:
```sh
make
```

Run the maze with the map you'd like to play:
```groovy
./maze maps/level_1
```
Or you can run with multiple maps at once:
```groovy
./maze maps/level_1 maps/level_2
```


If you're using the provided maps it'll just be a red screen, but that's not all. If you rotate with the arrow keys to the right you'll see the rest of the maze:


## Play the Game
The goal of the game is to find the end of the maze. To move through the maze use the arrow keys. The left and right arrow keys will rotate the player. The up and down arrow keys will move the player forward or backward.

Currently the player's starting position and the end goal position of the maze can be decided when creating the map file. If no positions are stated in the file then the player starts in the top left corner and the goal will be in the last floor space in the file.

When you have found the end of the maze you will either move, rather abruptly, to the next maze or the game will exit and you will be greeted with a win message in your console.


## Creating a Maze
The files in the `maps/` directory provide examples of the file format for a maze to work with this game. The different characters in the file represent different colored walls, the floor, the player position, or the position of the end goal.


In the image above the player starts 2 spaces in from the top left corner, and the end goal is placed in the bottom left most space that isn't a wall. There are five columns that are mostly blue, but have green, yellow, and white wall chunks in them.

**Map File Characters' in Game Meanings**
- **0**: Floor/walkable space
- **1**: Red Wall
- **2**: Green Wall
- **3**: Blue Wall
- **4**: Yellow Wall
- **w**: End goal
- **p**: Player start position
- All other characters will be defaulted to white walls

## Flowchart
![The Maze Flow Chart](https://i.imgur.com/t0MxNni.png)

## Reference
- [lazyfoo](http://lazyfoo.net/tutorials/SDL/index.php#Event%20Driven%20Programming)
- [geeksforgeeks](https://www.geeksforgeeks.org/structure-vs-class-in-cpp/)
- [permadi.com](https://permadi.com/1996/05/ray-casting-tutorial-1/)
- [lodev.org](https://lodev.org/cgtutor/raycasting.html)
- [cplusplus.com](https://cplusplus.com/forum/beginner/214311/)
- [pikuma.com](https://pikuma.com/courses/raycasting-engine-tutorial-algorithm-javascript)
- [3DSage/OpenGL-Raycaster](https://www.youtube.com/watch?v=gYRrGTC7GtA)

## Demo
[![The Maze Demo](https://youtu.be/rUfmv9XZgTM)

<details><summary align="center"> </samp></summary><p align ="center"> Click on The PICTURE☝️</p></details>




