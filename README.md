# CSE316
# Deadlock Prevention and Recovery Toolkit

## Overview
Deadlocks occur when multiple processes in an operating system are stuck waiting for resources held by other processes, resulting in circular waiting conditions. This inefficiency can lead to resource starvation, reduced system performance, and even total system failure.

## Purpose
The **Deadlock Prevention and Recovery Toolkit** provides real-time detection, prevention, and recovery solutions to ensure smooth system operation by:
- **Detecting Deadlocks:** Identifying deadlocks using cycle detection techniques and the Resource Allocation Graph (RAG).
- **Preventing Deadlocks:** Utilizing Banker's Algorithm and other safe resource allocation strategies.
- **Recovering from Deadlocks:** Resolving deadlocks through resource pre-emption or process termination.
- **Simulation & Visualization:** Offering a dynamic view of resource allocation and deadlock scenarios.

## Algorithms Implemented
The toolkit incorporates the following key algorithms:

### 1. **Resource Allocation Graph (RAG)**
   - A directed graph that represents resources and processes, used to detect potential circular waits.

### 2. **Cycle Detection Algorithm**
   - Identifies deadlocks by finding cycles within the Resource Allocation Graph.

### 3. **Banker’s Algorithm**
   - A safety algorithm that ensures resource requests are only granted if they do not lead to a deadlock.

### 4. **Pre-emptive Techniques**
   - Implements controlled resource allocation and prioritization to minimize deadlock risks.

## Recovery Mechanisms
If a deadlock occurs, the toolkit provides the following recovery mechanisms:

### 1. **Process Termination**
   - Resolves deadlocks by terminating one or more processes involved in the deadlock cycle.

### 2. **Resource Pre-emption**
   - Forces processes to release resources, allowing reallocation to break the deadlock.

By integrating these techniques, the **Deadlock Prevention and Recovery Toolkit** offers a comprehensive approach to handling deadlocks efficiently in operating systems.

# Deadlock Prevention and Recovery Toolkit

This repository provides a structured approach to detecting, preventing, and recovering from deadlocks in real-time systems. The toolkit is divided into several modules for better organization and development.

## Module-Wise Breakdown

### 1. Deadlock Detection Module
- **Purpose:** Detects deadlocks using a Resource Allocation Graph (RAG).
- **Implementation:**
  - Construct a graph representation of resource allocation.
  - Apply cycle detection algorithms (DFS-based) to identify circular waits.
  - If a cycle is found, a deadlock is detected.
- **Output:** Displays whether a deadlock is present or not.

### 2. Deadlock Prevention Module
- **Purpose:** Prevents deadlocks by ensuring the system never enters an unsafe state.
- **Implementation:**
  - Implement Banker’s Algorithm to check safe states before resource allocation.
  - Use pre-emptive techniques, such as ordering resource requests and checking availability before granting them.
- **Output:** Ensures that resources are allocated only if they result in a safe system state.

### 3. Deadlock Recovery Module
- **Goal:** Recovers from deadlocks as soon as they are identified.
- **Implementation:**
  - **Process Termination:** Breaks circular waits by selectively terminating processes.
  - **Resource Pre-emption:** Reallocates and temporarily recovers resources from specific processes.
- **Output:** Indicates which resources were pre-empted or which processes were stopped in order to break the deadlock.

### 4. Simulation Module
- **Purpose:** Enables users to design and test their own deadlock scenarios.
- **Implementation:**
  - Offers a user interface where users can input resource allocation scenarios.
  - Based on user-defined inputs, it simulates deadlock occurrence.
  - If a deadlock is found, a list of sequential recovery steps is displayed.
- **Output:** Visual indication of whether or not a particular situation results in a deadlock.

### 5. Visualization Module
- **Goal:** Offers a visual depiction of deadlock situations and resource distribution.
- **Implementation:**
  - Resource Allocation Graphs are dynamically generated using Graph Viz (C++) or Matplotlib (Python).
  - Safe and unsafe states are visually displayed.
- **Output:** A visual representation of processes, resources, allocations, and instances of deadlock.

### 6. User Interface (CLI/GUI)
- **Purpose:** Offers an interactive toolkit management interface.
- **Implementation:**
  - **Command-Line Interface (CLI):** For users accustomed to text-based communication.
  - **Graphical User Interface (GUI) (optional):** To make visual elements easier to use.
- **Output:** Enables convenient resource, process, and allocation data input.

  # Deadlock Prevention and Recovery Toolkit

## Overview
Deadlocks occur when multiple processes in an operating system are stuck waiting for resources held by other processes, resulting in circular waiting conditions. This inefficiency can lead to resource starvation, reduced system performance, and even total system failure.

## Purpose
The **Deadlock Prevention and Recovery Toolkit** provides real-time detection, prevention, and recovery solutions to ensure smooth system operation by:
- **Detecting Deadlocks:** Identifying deadlocks using cycle detection techniques and the Resource Allocation Graph (RAG).
- **Preventing Deadlocks:** Utilizing Banker's Algorithm and other safe resource allocation strategies.
- **Recovering from Deadlocks:** Resolving deadlocks through resource pre-emption or process termination.
- **Simulation & Visualization:** Offering a dynamic view of resource allocation and deadlock scenarios.

## Module-Wise Breakdown

### 1. **Deadlock Detection Module**
- **Purpose:** Detects deadlocks using a Resource Allocation Graph (RAG).
- **Implementation:**
  - Construct a graph representation of resource allocation.
  - Apply cycle detection algorithms (DFS-based) to identify circular waits.
  - If a cycle is found, a deadlock is detected.
- **Output:** Displays whether a deadlock is present or not.

### 2. **Deadlock Prevention Module**
- **Purpose:** Prevents deadlocks by ensuring the system never enters an unsafe state.
- **Implementation:**
  - Implement Banker’s Algorithm to check safe states before resource allocation.
  - Use pre-emptive techniques, such as ordering resource requests and checking availability before granting them.
- **Output:** Ensures that resources are allocated only if they result in a safe system state.

### 3. **Deadlock Recovery Module**
- **Purpose:** Recovers from deadlocks as soon as they are identified.
- **Implementation:**
  - **Process Termination:** Breaks circular waits by selectively terminating processes.
  - **Resource Pre-emption:** Reallocates and temporarily recovers resources from specific processes.
- **Output:** Indicates which resources were pre-empted or which processes were stopped in order to break the deadlock.

### 4. **Simulation Module**
- **Purpose:** Enables users to design and test their own deadlock scenarios.
- **Implementation:**
  - Offers a user interface where users can input resource allocation scenarios.
  - Based on user-defined inputs, it simulates deadlock occurrence.
  - If a deadlock is found, a list of sequential recovery steps is displayed.
- **Output:** Visual indication of whether or not a particular situation results in a deadlock.

### 5. **Visualization Module**
- **Purpose:** Offers a visual depiction of deadlock situations and resource distribution.
- **Implementation:**
  - Resource Allocation Graphs are dynamically generated using Graph Viz (C++) or Matplotlib (Python).
  - Safe and unsafe states are visually displayed.
- **Output:** A visual representation of processes, resources, allocations, and instances of deadlock.

### 6. **User Interface (CLI/GUI)**
- **Purpose:** Offers an interactive toolkit management interface.
- **Implementation:**
  - **Command-Line Interface (CLI):** For users accustomed to text-based communication.
  - **Graphical User Interface (GUI) (optional):** Enhances usability with visual elements.
  - Enables convenient input of resource, process, and allocation data.

## Functionalities

### 1. **Real-Time Deadlock Detection**
- Implements cycle detection in a **Resource Allocation Graph (RAG)**.
- Identifies circular dependencies using **Depth-First Search (DFS)** or **Kahn's Algorithm**.
- Provides real-time monitoring of resource allocation changes.
- Notifies users of deadlocks through **visual alerts, logs, or console messages**.
- Supports multi-process environments for accurate deadlock detection.

### 2. **Banker's Algorithm for Deadlock Prevention**
- Determines whether granting a resource request will lead to an unsafe state.
- Ensures resource allocation is only allowed if it does not lead to deadlock.
- Implements pre-emptive techniques:
  - **Ordering resource requests** to prevent circular wait conditions.
  - **Verifying availability** before allocation.
- Provides immediate feedback on request approval or denial.
- Logs all allocation decisions for auditing and debugging.

### 3. **Deadlock Recovery**
- Provides two methods to resolve deadlocks:
  - **Process Termination:** Selectively terminates processes to break the cycle.
  - **Resource Pre-emption:** Temporarily reclaims resources and reallocates them.
- Uses **priority-based termination** to minimize performance impact.
- Prevents starvation using a **fairness-based strategy**.
- Automatically selects the optimal recovery plan based on system state.
- Logs all recovery actions and presents them to the user.

### 4. **Resource Allocation Graphical Visualization**
- Creates **interactive visual representations** of the **Resource Allocation Graph**.
- Supports **C++, Python, and Java (JavaFX)** for visualization.
- Displays key elements:
  - **Processes (Nodes)**: Clearly labeled.
  - **Resources (Edges)**: Connections between resources and processes.
- Highlights potential deadlocks with **color-coded safe and unsafe states**.
- Provides **real-time updates** for dynamic resource allocation changes.
- Allows **zoom, pan, and interaction** for better understanding.

### 5. **Mode of Simulation**
- Allows users to test resource allocation scenarios in a controlled environment.
- Provides step-by-step simulation of possible deadlock occurrences.
- Interactive controls to modify:
  - **Number of resources and processes**.
  - **Request and allocation matrices**.
  - **Maximum claim values** per process.
- Dynamically detects deadlocks as the simulation progresses.
- Logs detailed information:
  - **Allocation changes**.
  - **Deadlock detection events**.
  - **Applied recovery and prevention measures**.
- Educates users on **why a deadlock occurs and how to resolve it**.

## Utilized Technology

### **Programming Languages**
- **C++**, **Python**, or **Java** (depending on user preference).

### **Tools and Libraries**
- **Graph Visualization:**
  - **Python:** Matplotlib for dynamic graph visualization.
  - **C++:** Graph Viz for drawing Resource Allocation Graphs.
  - **Java:** JavaFX for interactive GUI-based visualization.
- **Data Handling:**
  - **JSON & CSV** for storing resource allocation, process data, and user inputs.
- **Other Tools:**
  - **GitHub** for issue tracking, version control, and collaboration.
  - **Debugging and logging tools** for tracking real-time deadlock detection and prevention.
### **Code in PYTHON**
import tkinter as tk
from tkinter import ttk, messagebox
import numpy as np
import matplotlib.pyplot as plt
import networkx as nx
import winsound
import time
from matplotlib.backends.backend_tkagg import FigureCanvasTkAgg

class DeadlockDetectionApp:
    def __init__(self, master):
        self.master = master
        self.master.title("Deadlock Detection and Prevention")
        self.master.geometry("1000x700")
        
        self.num_processes = tk.IntVar()
        self.num_resources = tk.IntVar()
        
        self.create_initial_ui()
    
    def create_initial_ui(self):
        frame = ttk.Frame(self.master, padding=20)
        frame.pack(expand=True)
        
        ttk.Label(frame, text="Number of Processes:").grid(row=0, column=0, padx=5, pady=5)
        ttk.Entry(frame, textvariable=self.num_processes, width=5).grid(row=0, column=1)
        
        ttk.Label(frame, text="Number of Resources:").grid(row=1, column=0, padx=5, pady=5)
        ttk.Entry(frame, textvariable=self.num_resources, width=5).grid(row=1, column=1)
        
        ttk.Button(frame, text="Next", command=self.create_matrix_ui).grid(row=2, column=0, columnspan=2, pady=10)
    
    def create_matrix_ui(self):
        try:
            self.process_count = self.num_processes.get()
            self.resource_count = self.num_resources.get()
            if self.process_count <= 0 or self.resource_count <= 0:
                raise ValueError
        except ValueError:
            messagebox.showerror("Error", "Enter valid numbers for processes and resources.")
            return
        
        for widget in self.master.winfo_children():
            widget.destroy()
        
        ttk.Label(self.master, text="Enter Allocation Matrix:").grid(row=0, column=0, columnspan=self.resource_count)
        self.allocation_entries = self.create_matrix_input(1, self.process_count, self.resource_count)
        
        ttk.Label(self.master, text="Enter Request Matrix:").grid(row=self.process_count+1, column=0, columnspan=self.resource_count)
        self.request_entries = self.create_matrix_input(self.process_count+2, self.process_count, self.resource_count)
        
        ttk.Label(self.master, text="Available Resources:").grid(row=(self.process_count*2)+2, column=0, columnspan=self.resource_count)
        self.available_entries = self.create_vector_input((self.process_count*2)+3, self.resource_count)
        
        ttk.Button(self.master, text="Detect Deadlock", command=self.detect_deadlock).grid(row=(self.process_count*2)+4, column=0, columnspan=self.resource_count, pady=10)
    
    def create_matrix_input(self, start_row, rows, cols):
        matrix_entries = []
        for i in range(rows):
            row_entries = []
            for j in range(cols):
                entry = ttk.Entry(self.master, width=5)
                entry.grid(row=start_row+i, column=j, padx=5, pady=2)
                row_entries.append(entry)
            matrix_entries.append(row_entries)
        return matrix_entries
    
    def create_vector_input(self, start_row, size):
        entries = []
        for i in range(size):
            entry = ttk.Entry(self.master, width=5)
            entry.grid(row=start_row, column=i, padx=5, pady=2)
            entries.append(entry)
        return entries
    
    def get_matrix_values(self, matrix_entries):
        try:
            return np.array([[int(entry.get()) for entry in row] for row in matrix_entries])
        except ValueError:
            messagebox.showerror("Error", "Invalid input! Enter only numbers.")
            return None
    
    def get_vector_values(self, vector_entries):
        try:
            return np.array([int(entry.get()) for entry in vector_entries])
        except ValueError:
            messagebox.showerror("Error", "Invalid input! Enter only numbers.")
            return None
    
    def detect_deadlock(self):
        allocation = self.get_matrix_values(self.allocation_entries)
        request = self.get_matrix_values(self.request_entries)
        available = self.get_vector_values(self.available_entries)
        
        if allocation is None or request is None or available is None:
            return
        
        work = available.copy()
        finish = np.full(self.process_count, False)
        safe_sequence = []
        
        for _ in range(self.process_count):
            found = False
            for i in range(self.process_count):
                if not finish[i] and np.all(request[i] <= work):
                    work += allocation[i]
                    finish[i] = True
                    safe_sequence.append(i)
                    found = True
                    break
            if not found:
                break
        
        if np.all(finish):
            messagebox.showinfo("Result", f"No Deadlock! Safe Sequence: {safe_sequence}")
            self.show_charts(allocation, available)
            self.show_rag_graph(allocation, request)
        else:
            self.show_warning_effect()
            messagebox.showerror("Result", "Deadlock Detected! Use these strategies to prevent deadlock:\n1. Resource Allocation Ordering\n2. Banker's Algorithm\n3. Preemption\n4. Request Reduction")
            self.show_rag_graph(allocation, request)
    
    def show_charts(self, allocation, available):
        fig, axes = plt.subplots(1, 2, figsize=(10, 5))
        
        total_allocated = np.sum(allocation, axis=0)
        axes[0].pie(total_allocated, labels=[f'Resource {i}' for i in range(len(total_allocated))], autopct='%1.1f%%')
        axes[0].set_title("Resource Allocation Distribution")
        
        axes[1].bar([f'Resource {i}' for i in range(len(available))], available, color='skyblue')
        axes[1].set_title("Available Resources")
        axes[1].set_ylabel("Count")
        
        plt.tight_layout()
        plt.show()
    
    def show_rag_graph(self, allocation, request):
        G = nx.DiGraph()
        
        for p in range(self.process_count):
            G.add_node(f'P{p}')
        for r in range(self.resource_count):
            G.add_node(f'R{r}')
        
        for p in range(self.process_count):
            for r in range(self.resource_count):
                if allocation[p][r] > 0:
                    G.add_edge(f'R{r}', f'P{p}')
                if request[p][r] > 0:
                    G.add_edge(f'P{p}', f'R{r}')
        
        pos = nx.spring_layout(G)
        nx.draw(G, pos, with_labels=True, node_color='lightblue', edge_color='black')
        plt.show()
    
    def show_warning_effect(self):
        winsound.Beep(1000, 4000)
        

def main():
    root = tk.Tk()
    app = DeadlockDetectionApp(root)
    root.mainloop()

if __name__ == "__main__":
    main()


 

