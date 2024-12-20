# Memory Allocation Simulation Project

This project implements a simulation of a **dynamic memory allocation scheduling mechanism**, designed to manage processes that require memory resources. It leverages a **priority queue** to enhance the allocation process based on specific criteria, ensuring an efficient and systematic approach to handling memory and processes.

---

## Project Overview
The program simulates how memory is allocated to processes in a system. It uses several lists to manage the state of processes and memory blocks dynamically:

1. **Memory Block List**: Tracks all available memory blocks, starting with a single block covering the entire memory size.
2. **Starting Process List**: Contains processes to be introduced into the system.
3. **Running Process List**: Processes that have been allocated memory and are currently running.
4. **Waiting Process List**: Processes waiting for memory allocation.

---

## Key Features
- **Dynamic Memory Management**:
  - Allocates memory to processes based on availability.
  - Reclaims memory upon process completion.
  - Merges adjacent free memory blocks to optimize space.

- **Priority Queue Integration**:
  - Processes are prioritized based on criteria such as memory size requirements or timeout values.
  - Ensures high-priority processes are handled first.

- **Real-Time Process Updates**:
  - Each second, processes are moved dynamically between lists (starting, waiting, running).
  - Running process timeout decreases, and completed processes release their memory.

---

## Simulation Flow

### 1. Initialization
- The system starts with a total memory size of 1024 units (address range 0–1023).
- 20 processes are created with random memory sizes (up to 256) and random timeout durations (up to 20000 ms).

### 2. Execution
- At each second:
  - A process is dispatched from the starting list.
  - Memory allocation or waiting list placement is determined.
  - Running processes are updated (timeout decreases, completed processes are removed).
  - Memory is reclaimed and optimized when processes complete.

### 3. Termination
- The program halts when both the waiting and running lists are empty.

---

## Technologies Used
- **Java**: For implementation and object-oriented design.
- **Priority Queue**: To handle process prioritization efficiently.
- **Data Structures**:
  - LinkedList
  - Queue

---

## Sample Output
- Displays real-time updates for:
  - Running processes
  - Waiting processes
  - Memory status
  - Completed processes

---

## How to Run
1. Clone this repository:
   ```bash
   git clone <repository-url>
   ```
2. Navigate to the project directory:
   ```bash
   cd memory-allocation-simulation
   ```
3. Compile the Java files:
   ```bash
   javac *.java
   ```
4. Run the program:
   ```bash
   java MemAlloc
   ```

---

## Contribution
Contributions are welcome! If you'd like to improve this project or fix any bugs, please fork the repository and submit a pull request.

---

## License
This project is licensed under the MIT License. See the LICENSE file for details.
