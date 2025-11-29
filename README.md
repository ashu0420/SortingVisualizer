# 📊 Bubble Sort Visualization in C++

A real-time graphical visualization of the Bubble Sort algorithm built using C++ and the `graphics.h` library. This project demonstrates algorithm logic, memory manipulation, and graphical rendering by animating the sorting process of a randomized array.

![Project Screenshot](https://via.placeholder.com/800x400?text=Place+Your+Project+Screenshot+Here)
*(Note: Replace the link above with a screenshot of your actual running graph)*

## 🚀 Project Overview

The goal of this project is to bridge the gap between abstract algorithmic concepts and visual understanding. Instead of simply printing numbers to a console, this application creates a dynamic bar chart where:
* **Height** represents the value of the number.
* **Position** represents the index in the array.
* **Animation** shows exactly how elements are compared and swapped.

## 🛠️ Tech Stack

* **Language:** C++ (Modern C++11 standards utilized for randomization)
* **Graphics Library:** `graphics.h` (WinBGIm port for Windows)
* **Standard Libraries:** `<vector>`, `<chrono>`, `<algorithm>`

## ⚙️ Key Features

* **Dynamic Data Generation:** Uses `std::chrono` to seed the random engine, ensuring a unique shuffled array every time the program runs.
* **Real-Time Rendering:** Utilizes pixel manipulation to "erase" (paint black) and "redraw" (paint white) bars during the swap process.
* **Visual Feedback:** The active bars being swapped are briefly highlighted in **Green** to track the algorithm's operation.
* **Auto-Scaling Window:** The graphical window size is calculated dynamically based on the dataset size and gap width.

## 📦 How to Run

### Option 1: Using Dev-C++ (Recommended)
Because `graphics.h` is a legacy library, the easiest way to run this project is using **Orwell Dev-C++**.
1.  Open `main.cpp` in Dev-C++.
2.  Go to **Project -> Project Options -> Parameters -> Linker**.
3.  Add the following flags:
    ```text
    -lbgi -lgdi32 -lcomdlg32 -luuid -loleaut32 -lole32
    ```
4.  Press **F11** to Compile and Run.

### Option 2: Using VS Code (MinGW)
If using VS Code, you must manually install `WinBGIm` into your MinGW `include` and `lib` folders.
1.  Ensure `graphics.h`, `winbgim.h`, and `libbgi.a` are in your MinGW directory.
2.  Configure your `tasks.json` to include the linker flags listed in Option 1.
3.  Build and Run.

## 🧠 Algorithm Logic

The project implements **Bubble Sort**, a simple comparison-based algorithm.

1.  **Iteration:** The program iterates through the vector.
2.  **Comparison:** It compares adjacent elements (`arr[j]` and `arr[j+1]`).
3.  **Swap:** If they are in the wrong order, they are swapped both in memory and visually on the graph.

**Complexity Analysis:**
* **Time Complexity:** $O(N^2)$ (Average/Worst Case)
* **Space Complexity:** $O(1)$ (Auxiliary space)

## 📸 Code Structure

* `main()`: Handles window initialization, array generation, and the shuffle logic.
* `bubbleSort()`: Contains the core sorting algorithm.
* `swap()`: A helper function that handles the graphical update. It performs the "Erase -> Redraw" logic to simulate movement.

## 🔮 Future Improvements

* **Sorting Selection:** Add a menu to choose between Merge Sort, Quick Sort, and Heap Sort.
* **Speed Control:** Allow the user to speed up or slow down the visualization using keyboard input.
* **Audio Cues:** Add sound effects where pitch corresponds to the value of the number being swapped.

---
