# Degrees: Finding Connections Between Actors

The **Six Degrees of Kevin Bacon** game is a popular concept that suggests any actor in Hollywood can be connected to Kevin Bacon through a chain of movies they’ve starred in, with no more than six steps. This project aims to solve a similar problem: finding the shortest path between any two actors by identifying a sequence of movies that connects them.

For example, the shortest path between **Jennifer Lawrence** and **Tom Hanks** is **2**:

1. Jennifer Lawrence and Kevin Bacon starred in _“X-Men: First Class.”_
2. Kevin Bacon and Tom Hanks starred in _“Apollo 13.”_

This problem is framed as a **search problem**, where:

- **States** are actors.
- **Actions** are movies that connect two actors.
- The **initial state** and **goal state** are the two actors we want to connect.

Using **breadth-first search (BFS)**, we can efficiently find the shortest path between any two actors.

---

## Requirements

To run this project, ensure you have the following:

- **Python** version **3.12.2** or higher  
  Download Python: [https://www.python.org/downloads/](https://www.python.org/downloads/)

---

## Getting Started

Follow these steps to set up and run the project:

1. **Clone the repository** and navigate to the project directory:

   ```bash
   git clone https://github.com/your-repo/AI_BFS-DFS.git
   cd AI_BFS-DFS
   ```

2. **Run the Search**:

   Start the program by running the following command:

   ```bash
   python degrees.py
   ```

---

## Project Structure

The project is organized into the following directories and files:

- **`large`**:  
  Contains large datasets for movies, people, and stars:

  - `movies.csv`: A list of movies.
  - `people.csv`: A list of actors and their IDs.
  - `stars.csv`: A mapping of actors to the movies they’ve starred in.

- **`small`**:  
  Contains smaller datasets for testing and experimentation:

  - `movies.csv`: A smaller list of movies.
  - `people.csv`: A smaller list of actors and their IDs.
  - `stars.csv`: A smaller mapping of actors to movies.

- **`degrees.py`**:  
  The main script that implements the BFS algorithm to find the shortest path between two actors.

---

## How It Works

1. **Data Loading**:  
   The program loads the datasets (`movies.csv`, `people.csv`, and `stars.csv`) to build a graph where:

   - **Nodes** represent actors.
   - **Edges** represent movies that connect two actors.

2. **Breadth-First Search (BFS)**:  
   The BFS algorithm is used to find the shortest path between two actors. It explores all possible connections level by level, ensuring the shortest path is found.

3. **Path Construction**:  
   Once the shortest path is found, the program constructs the sequence of movies and actors that connect the two actors.

---

## Example

### Input:

- **Actor 1**: Jennifer Lawrence
- **Actor 2**: Tom Hanks

### Output:

- **Shortest Path**: 2
- **Path**:
  1. Jennifer Lawrence and Kevin Bacon starred in _“X-Men: First Class.”_
  2. Kevin Bacon and Tom Hanks starred in _“Apollo 13.”_

---

## Contributing

Contributions are welcome! If you'd like to contribute, please follow these steps:

1. Fork the repository.
2. Create a new branch for your feature or bugfix.
3. Commit your changes and push to the branch.
4. Submit a pull request.

---

## Acknowledgments

- Inspired by the **CS50 AI** course.

---

Enjoy exploring connections between actors! 🎬
