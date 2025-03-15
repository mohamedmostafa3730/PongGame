# Pong Game

## What I Learned from Pong Program
1. **Movement**: Understanding how to move objects on the screen.
2. **Controls**: Implementing user input to control game elements.
3. **Collision Detection**: Detecting when objects collide and responding appropriately.
4. **Scoring**: Keeping track of and displaying the score.
5. **Artificial Intelligence**: Creating a simple AI to control the CPU paddle.

## Steps to Develop Pong
1. Create a blank screen & game loop
2. Draw the paddles and the ball
3. Move the ball around
4. Check for a collision with all paddles
5. Move the player's paddle
6. Move the CPU paddle with Artificial Intelligence
7. Check for a collision with paddles
8. Add scoring

## Step-by-Step Guide

### Step #1: Create a Blank Screen & Game Loop
- **Game Structure**: The basic structure of the game includes definitions and the game loop.
- **This Game**:
    - **Definitions**: Define the variables needed and create the game objects.
    - **Game Loop**: Update the positions of the game objects and check for collisions.

### Step #2: Draw the Paddles and the Ball
- **How to Draw with Raylib**:
    1. `void DrawRectangle(int posX, int posY, int height, Color color);` - Draws a rectangle.
    2. `void DrawCircle(int centerX, int centerY, float radius, Color color);` - Draws a circle.
    3. `void DrawLine(int startPosX, int startPosY, int endPosX, int endPosY, Color color);` - Draws a line.
    4. `void DrawPoly(Vector2 center, int sides, float radius, float rotation, Color color);` - Draws a polygon.

### Step #3: Move the Ball Around
- **Ball Class Functions**:
    1. `void DrawCircle(int centerX, int centerY, float radius, Color color);` - Draws the ball.
    2. `void ClearBackground(Color color);` - Clears the screen.
    3. `void Draw();` - Custom function to draw the ball.
    4. `void Update();` - Custom function to update the ball's position.

### Step #4: Check for a Collision with All Paddles
- **Update() Function**:
    - Add an if condition to check for collisions using functions such as:
        1. `GetScreenHeight();` - Gets the height of the screen.
        2. `GetScreenWidth();` - Gets the width of the screen.

### Step #5: Move the Player's Paddle
- **Player Class Functions**:
    1. `IsKeyDown(KEY_UP);` - Checks if the up key is pressed.
    2. `IsKeyDown(KEY_DOWN);` - Checks if the down key is pressed.
    3. `GetScreenHeight();` - Gets the height of the screen.
    4. `void Draw();` - Custom function to draw the player's paddle.
    5. `void Update();` - Custom function to update the player's paddle position.

### Step #6: Move the CPU Paddle with Artificial Intelligence
- **CPU Paddle Class**:
    - Inherits from the paddle class to use functions such as:
        1. `CPU.Update();` - Updates the CPU paddle's position.
        2. `CPU.Draw();` - Draws the CPU paddle.
        3. `LimitMovement();` - Limits the movement of the CPU paddle.
    - Uses data such as:
        1. `CPU.width;` - Width of the CPU paddle.
        2. `CPU.height;` - Height of the CPU paddle.
        3. `CPU.x;` - X position of the CPU paddle.
        4. `CPU.y;` - Y position of the CPU paddle.
        5. `CPU.speed;` - Speed of the CPU paddle.

### Step #7: Check for a Collision with Paddles
- **Collision Detection Function**:
    1. `CheckCollisionCircleRec(Vector2 center, float radius, Rectangle rec);` - Checks for a collision between a circle and a rectangle.

### Step #8: Add Scoring
- **Scoring**:
    - Create two variables: `player_score` and `CPU_score`.
    - Use functions such as:
        1. `DrawText(text, xpos, ypos, fontsize, color);` - Draws text on the screen.
        2. `DrawRectangleRounded(rec, roundness, segment, color);` - Draws a rounded rectangle.