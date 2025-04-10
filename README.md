
# Tetris Game - C++ Console Implementation  

## 📜 Introduction  
This is a **console-based Tetris game** developed in **C++**, featuring smooth rendering, colored tetrominoes, a ghost piece, next piece preview, scoring, increasing difficulty, and a lifeline feature. It uses **Windows Console APIs** for rendering and **ANSI escape codes** for colors.  

## 🎮 Features  
🔹 **All Seven Tetrominoes** – I, O, T, S, Z, J, L  
🔹 **Smooth Gameplay** – 60 FPS rendering  
🔹 **Colored Blocks** – Uses emoji-based colors  
🔹 **Ghost Piece** – Shows where the piece will land  
🔹 **Next Piece Preview** – Displays upcoming tetromino  
🔹 **Lifeline Feature** – Clears bottom 3 rows once per game  
🔹 **Scoring System** – 100 points per cleared line  
🔹 **Level Progression** – Increases difficulty every 300 points  
🔹 **High Score System** – Saves the highest score in `highscore.txt`  
🔹 **Soft Drop & Hard Drop** – Spacebar instantly drops the piece  
🔹 **Sound Effects** – Uses `Beep()` for rotation, movement, line clear, etc. 

## ⚙️ Requirements  
- **Compiler**: g++ (MinGW recommended)  
- **OS**: Windows (uses Windows API for rendering)  
- **Libraries**:  
  - `<iostream>` (for input/output)  
  - `<vector>` (to store tetrominoes and board)  
  - `<windows.h>` (for console manipulation and sound)  
  - `<conio.h>` (for real-time keyboard input)  
  - `<ctime>` (for randomization)  
  - `<fstream>` (for high score storage)  

## 🎮 Gameplay Controls  
**⬅️ (Left Arrow)** -> Move left  
**➡️ (Right Arrow)** -> Move right   
**⬆️ (Up Arrow)** -> Rotate piece  
**⬇️ (Down Arrow)** -> Soft drop (move down faster)   
**⏬ Spacebar** -> Hard drop (instantly drop to the bottom)   
**❤️ L** -> Use lifeline (clears bottom 3 rows, only once)   
**⏹️ ESC** -> Exit the game   
**🔄️ R** -> Restart the game after game over   

---

## 📌 Code Structure  

### **Class `Tetris`**  
The `Tetris` class manages **grid, piece movement, collision detection, rendering, and scoring**.    

#### **Core Functions**

🔹 **`generateNextPiece()`** -> Generates the next tetromino   
🔹 **`spawnPiece()`** -> Spawns a new piece at the top   
🔹 **`isValidMove()`** -> Checks if a move is valid    
🔹 **`rotatePiece()`** -> Rotates the current tetromino   
🔹 **`movePiece()`** -> Moves the tetromino left or right   
🔹 **`moveDown()`** -> Moves the tetromino down   
🔹 **`dropPiece()`** -> Instantly drops the tetromino   
🔹 **`lockPiece()`** -> Locks a tetromino in place   
🔹 **`clearLines()`** -> Clears full rows and updates score   
🔹 **`loadHighScore()`** -> Loads high score from file   
🔹 **`saveHighScore()`** -> Saves high score to file   
🔹 **`useLifeline()`** -> Clears the bottom 3 rows once   
🔹 **`drawBoard()`** -> Renders the game frame  
🔹 **`handleInput()`** -> Captures user input  
🔹 **`play()`** -> Runs the game loop  

---

## 🔥 Future Improvements  
- **Improve Rendering Performance** – Use **double buffering** to prevent flickering  
- **Add Multiplayer Mode** – Implement a **battle mode**  
- **Better AI for Auto Play** – Implement **AI-based gameplay**  
- **Use Modern Graphics API** – Migrate to **SFML or SDL** for graphical UI  
- **Customizable Controls** – Allow players to set their own key bindings  

---

## 🚀 How to Run the Game  
1. **Compile the code** using MinGW:  
   ```sh
   g++ tetris.cpp -o tetris.exe
   ```
2. **Run the executable**:  
   ```sh
   tetris.exe
   ```
3. **Enjoy the game!** 🎮  

---

## 📢 Notes  
- The game runs **only on Windows** (due to Windows API usage).  
- **High score is saved in `highscore.txt`**.  
- Uses **UTF-8 emoji colors**, so enable UTF-8 output.  

---

## Implementation on LINUX/MAC OS
🔹Remove windows specific headers which are windows.h and conio.h with termios.h, unistd.h and fcntl.h       
🔹To replace windows specific functions _kbhit(), _getch() and SetConsoleCursorPosition() you need to add their code snippets in the original game code     
🔹Enable UTF-8 (Linux Terminal supports it natively)      
🔹Remove Beep() and replace it with system sounds    

---

## This is how our Tetris Game looks :

![image alt](https://github.com/JhanviBarot/Tetris-Game-in-C-/blob/7cc96c8edb251722613a112a004c105c74b04efc/GameConsoleImage.png)

## 
Enjoy playing **Tetris** with **smooth controls, ghost piece, and cool sound effects!** 🎉
