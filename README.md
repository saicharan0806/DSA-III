# Student-to-Laboratory Allocation System Using Maximum Bipartite Matching

## 📌 Project Overview

The Student-to-Laboratory Allocation System is a Java-based console application that automatically assigns students to laboratories based on their preferences and the available laboratory capacity.

The project uses the **Maximum Bipartite Matching algorithm with Depth-First Search (DFS)** to maximize the number of students allocated to laboratory seats.

Student details, laboratory preferences, and laboratory capacities are stored in a CSV dataset. The system processes this data and generates allocation results and reports.

## 🎯 Objectives

- Automate student-to-laboratory allocation.
- Consider students' laboratory preferences.
- Respect the capacity of each laboratory.
- Maximize the number of successfully allocated students.
- Ensure each student receives at most one allocation.
- Generate allocation, laboratory-wise, and preference-rank reports.
- Demonstrate the practical application of graph algorithms.

## ✨ Features

- Read student details and preferences from a CSV file.
- Load laboratory capacities from the dataset.
- Construct a bipartite preference graph.
- Represent each laboratory seat as an individual vertex.
- Perform maximum matching using DFS and augmenting paths.
- Display allocated and unallocated students.
- Generate laboratory-wise allocation reports.
- Display the preference rank of assigned laboratories.
- Calculate the total allocation rate.
- Provide an interactive console menu.

## 🧠 Algorithm Used

### Maximum Bipartite Matching

A bipartite graph consists of two separate sets of vertices. In this project:

- **Left set:** Students.
- **Right set:** Individual laboratory seats.
- **Edges:** Connections between students and seats belonging to their preferred laboratories.

Each student can be assigned to at most one seat, and each seat can accommodate at most one student.

The project uses a DFS-based matching algorithm to find valid assignments. If a preferred seat is already occupied, the algorithm checks whether the existing assignment can be rearranged to accommodate another student.

### Algorithm Steps

1. Read student information and laboratory capacities from the CSV dataset.
2. Create student and laboratory objects.
3. Build the student preference graph.
4. Create individual seats according to laboratory capacities.
5. Connect students to seats in their preferred laboratories.
6. Apply DFS-based maximum matching.
7. Display the final allocation and reports.
8. Calculate allocation statistics.

### Complexity

For the standard DFS-based bipartite matching algorithm:

- **Time complexity:** `O(V × E)` in the worst case.
- **Space complexity:** `O(V + E)` for the graph and matching-related storage.

Here, `V` represents the number of vertices and `E` represents the number of edges in the expanded student-to-seat graph.

## 🛠️ Technologies Used

- **Programming Language:** Java
- **Data Structure:** Bipartite Graph, Adjacency List
- **Algorithm:** Maximum Bipartite Matching using DFS
- **Collections:** ArrayList, HashMap, LinkedHashMap, HashSet
- **File Handling:** FileReader, BufferedReader
- **Dataset Format:** CSV
- **Development Environment:** Visual Studio Code or any Java-compatible IDE
- **Execution Environment:** Terminal / Command Prompt

## 📂 Project Structure

```text
DSA_3_PROJECT/
├── data/
│   └── student_lab_allocation_dataset_one_row_per_student.csv
│
├── src/
│   ├── Student.java
│   ├── Laboratory.java
│   ├── DataReader.java
│   ├── Graph.java
│   └── Main.java
│
└── README.md
```

### File Descriptions

| File | Description |
|---|---|
| `Student.java` | Stores student details and laboratory preferences. |
| `Laboratory.java` | Stores laboratory IDs, names, and capacities. |
| `DataReader.java` | Reads student and laboratory information from the CSV file. |
| `Graph.java` | Builds the graph, performs matching, and generates reports. |
| `Main.java` | Runs the application and manages the console menu. |
| CSV dataset | Contains student details, five preferences, and laboratory capacities. |

## 📊 Dataset Details

The project uses a single CSV dataset containing:

- 100 students.
- 8 laboratories.
- 5 laboratory preferences per student.
- Laboratory capacities stored in the same dataset.
- 70 total laboratory seats.

The dataset provides the input required to build the graph and perform the allocation.

## ▶️ How to Run the Project

### Prerequisites

- Install Java Development Kit (JDK 17 or later).
- Install Visual Studio Code or use a terminal.
- Download or clone this repository.

### Step 1: Clone the repository

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
```

Replace `YOUR_GITHUB_REPOSITORY_URL` with your actual GitHub repository URL.

### Step 2: Open the project folder

```bash
cd DSA_3_PROJECT
```

### Step 3: Compile the Java files

```bash
javac src/*.java
```

### Step 4: Run the application

From the project root directory, run:

```bash
java -cp src Main
```

**Note:** The current `Main.java` uses the relative CSV path `../data/student_lab_allocation_dataset_one_row_per_student.csv`, which assumes execution from the `src` directory. If running from the project root, update the path to:

```java
String filePath =
    "data/student_lab_allocation_dataset_one_row_per_student.csv";
```

Then compile and run again.

## 🖥️ Application Menu

The application provides the following options:

1. Display Students
2. Display Laboratories
3. Display Preference Graph
4. Perform Maximum Matching
5. View Allocation
6. View Laboratory Report
7. View Preference Report
8. View Summary
9. Exit

Perform maximum matching before selecting the allocation and report options.

## 📈 Results

In the tested dataset, the application produces the following allocation summary:

| Metric | Result |
|---|---:|
| Total Students | 100 |
| Total Lab Seats | 70 |
| Allocated Students | 70 |
| Unallocated Students | 30 |
| Allocation Rate | 70% |

The system reaches the maximum possible allocation count for this dataset because there are only 70 available seats.

The exact allocation for each laboratory depends on the matching generated by the program.

## 🚀 Future Enhancements

- Add a graphical user interface or web application.
- Integrate a database for persistent storage.
- Support multiple laboratory sessions and time slots.
- Introduce priority-based allocation.
- Optimize assignments based on preference rankings.
- Add administrator controls for updating student data and lab capacities.
- Generate downloadable allocation reports.

## 🎓 Learning Outcomes

This project demonstrates how graph algorithms can solve practical resource allocation problems. It provides hands-on experience with bipartite graphs, adjacency lists, DFS, augmenting paths, Java collections, file handling, and algorithmic complexity.

## 👨‍💻 Project Information

**Project Title:** Student-to-Laboratory Allocation System Using Maximum Bipartite Matching

**Domain:** Data Structures and Algorithms (DSA)

**Language:** Java

**Application Type:** Console-Based Application

---

*Developed as an academic project to demonstrate the application of graph matching algorithms in student-laboratory allocation.*
