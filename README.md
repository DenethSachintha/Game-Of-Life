# Features of the Game of Life Code

This project is an implementation of Conway's **Game of Life** using the Raylib library for graphical rendering. Below are the key features and functionality of the code:

---

## 1. **Window and Graphics Setup**
- **Resolution and Colors**: 
  - The game window is initialized with a resolution of `750x750` pixels.
  - A custom grey background color is defined as `Color GREY = {29, 29, 29, 255}`.
- **Frame Rate**:
  - The game starts with a frame rate of 12 FPS, adjustable using specific controls.

## 2. **Simulation Grid**
- **Cell Size**:
  - Each cell in the grid has a size of `15x15` pixels.
- **Grid Initialization**:
  - A `Simulation` object is created to manage the state and rendering of the game grid.

---

## 3. **User Interaction**
### 3.1 Mouse Interaction
- **Toggle Cells**:
  - Left mouse clicks allow users to toggle the state (alive/dead) of a cell based on the mouse's position.

### 3.2 Keyboard Interaction
- **Start/Stop Simulation**:
  - Press `ENTER` to start the simulation and change the window title to indicate the simulation is running.
  - Press `SPACE` to stop the simulation and update the window title accordingly.

- **Adjust Speed**:
  - Press `F` to increase the simulation's frame rate by 2 FPS.
  - Press `S` to decrease the frame rate by 2 FPS (minimum of 5 FPS).

- **Randomize or Clear Grid**:
  - Press `R` to randomly populate the grid with alive and dead cells.
  - Press `C` to clear the grid, resetting all cells to the dead state.

---

## 4. **Simulation Logic**
### 4.1 Main Loop
The simulation operates within a loop that includes the following key phases:
1. **Event Handling**:
   - User input is processed to toggle cells, control the simulation, or adjust settings.
2. **Updating State**:
   - The `Simulation::Update()` method is called to apply the rules of Conway's Game of Life and advance the grid state.
3. **Drawing**:
   - The `Simulation::Draw()` method renders the grid on the screen.
   - The screen is cleared with the custom grey background color (`ClearBackground(GREY)`).

---

## 5. **Simulation Class (Encapsulation)**
- The `Simulation` class encapsulates the grid state, rendering logic, and core simulation methods:
  - `ToggleCell(row, column)`: Toggles a cell's state based on grid coordinates.
  - `Start()`: Starts the simulation.
  - `Stop()`: Stops the simulation.
  - `CreateRandomState()`: Randomly populates the grid.
  - `ClearGrid()`: Clears the grid, resetting all cells to the dead state.
  - `Update()`: Updates the grid state by applying the rules of the Game of Life.
  - `Draw()`: Renders the grid and cells.

---

## 6. **Code Structure and Flow**
- **Initialization**:
  - Sets up the window, grid, and initial simulation parameters.
- **Main Loop**:
  - Handles user input, updates the simulation state, and renders the game.
- **Cleanup**:
  - Closes the window and performs necessary cleanup when the game exits.

---

## 8. **Controls Summary**
| Key/Mouse Action | Functionality                                |
|------------------|---------------------------------------------|
| Left Click       | Toggle cell state (alive/dead).             |
| ENTER            | Start the simulation.                      |
| SPACE            | Stop the simulation.                       |
| F                | Increase simulation speed (FPS).           |
| S                | Decrease simulation speed (FPS).           |
| R                | Randomize the grid state.                  |
| C                | Clear the grid (reset all cells to dead).  |

---

This implementation provides an interactive and visually engaging version of Conway's Game of Life, allowing users to explore cellular automata in real-time.

