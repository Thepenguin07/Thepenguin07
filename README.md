# ⚡ Terminal.init() 

<p align="left">
  <a href="https://www.linkedin.com/in/shifa-parveen-286251307"><img src="https://img.shields.io/badge/LINKEDIN-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
  <img src="https://img.shields.io/badge/STATUS-OPERATIONAL-9ece6a?style=for-the-badge" alt="Status">
  <img src="https://img.shields.io/badge/FOCUS-DEEP__LEARNING__%2F%2F__GRAPHS-bf91f9?style=for-the-badge" alt="Focus">
</p>

```txt
┌────────────────────────────────────────────────────────────────────────┐
│  ▶ Host       : [github.com/thepenguin07](https://github.com/thepenguin07)                                │
│  ▶ Developer  : Shifa Parveen                                          │
│  ▶ Core Specs : Applied ML / Computer Vision / Discrete Math / Systems │
│  ▶ Terminal   : zsh // Neovim // GCC // JVM // Python Runtime          │
└────────────────────────────────────────────────────────────────────────┘
I am a Computer Science Major who operates at the intersection of raw data architecture and predictive intelligence. My engineering focus centers on building low-latency data pipelines, training optimized metric-learning networks, and modeling complex relational graphs to extract real-world behavioral insights.
🛠️ System Capabilities // Tech Stack
📂 Production Environment // Project Breakdowns
🧪 Compiled Repositories & Deep Dives
Architectural Objective: Complete elimination of manual workspace check-ins via real-time computer vision verification and automated database processing.
🛠️ How It Works:
Instead of utilizing standard classification models that require full retraining every time a new profile is registered, FacialBooks implements a custom Siamese Neural Network (CNN) configured for One-Shot Learning.
Plaintext
[Webcam Feed] ──► [Preprocess: 96x96x3 Normalized Tensor] ──► [Face Detection Crop]
                                                                     │
  ┌──────────────────────────────────────────────────────────────────┘
  ▼
 Twin CNN Pathways (Shared Weights):
  [Anchor Image  (X1)] ──► [Conv Block x4] ──► [128-D Vector] ──┐
                                                                 ├──► [Contrastive Loss] ──► Threshold check (τ = 0.12)
  [Database Card (X2)] ──► [Conv Block x4] ──► [128-D Vector] ──┘
Dimensional Compression: The system processes video frames down to a 96×96×3 normalized RGB tensor and routes it through twin feature extraction pathways featuring sequential layers of Conv2D → BatchNormalization → ReLU → MaxPooling → Dropout.
L2-Normalized Projection: The model projects facial features onto a continuous 128-dimensional vector space. Twin layers are evaluated using a custom Contrastive Loss function across a margin of m=1.0:
L 
Contrastive
​	
 = 
2
1
​	
 (Y)(D 
W
​	
 ) 
2
 + 
2
1
​	
 (1−Y)max(0,m−D 
W
​	
 ) 
2
 
Where D 
W
​	
  is the Euclidean distance between embeddings:
D 
W
​	
 (X 
1
​	
 ,X 
2
​	
 )=∥G 
W
​	
 (X 
1
​	
 )−G 
W
​	
 (X 
2
​	
 )∥ 
2
​	
 
Instant Verification & Payroll Log: If the distance drops below τ=0.12, identity is verified. The system records the entry timestamp and automatically runs payroll calculations.
Architectural Objective: Real-time social topology simulation utilizing custom mathematical relationship scoring.
🛠️ How It Works:
This system avoids heavy external database backends by maintaining an in-memory adjacency list model (HashMap<Integer, List<Edge>>) representing nodes (users) and directed paths (friendships).
Plaintext
                        [ Target Node: User (u) ]
                                    │
                  ┌─────────────────┴─────────────────┐
                  ▼                                   ▼
       [Topological Proximity]             [Semantic Overlaps]
       Shared Friend Neighborhoods         Matching Interest Vectors
                  │                                   │
                  └─────────────────┬─────────────────┘
                                    ▼
                     [ Hybrid Score: Jaccard Merge ]
                                    │
                                    ▼
                     [ Greedy Max-Heap Priority Queue ] ──► Top-N Output
Hybrid Scoring Engine: To solve the "cold start" problem for new users, the recommendation algorithm evaluates connection candidate c for user u by combining both structural and semantic matrices:
Score(u,c)=0.6⋅Jaccard 
Network
​	
 (u,c)+0.4⋅Jaccard 
Interests
​	
 (u,c)
Computational Space Complexity:
Triadic Closure Expansion: Runs a BFS traversal targeting friends-of-friends to compile potential recommendation matches.
Max-Heap Ranking: Sorts potential recommendation candidates in real time through a bounded Greedy Priority Queue, outputting the Top-N connections in O(KlogN) complexity.
Core Objective: Highly optimized route planner utilizing low-level memory handling to calculate the shortest path.
🛠️ How It Works:
This application is designed in pure C and runs a custom graphical interface built on GTK+ 3.0. It maps coordinates into weighted directed graph representations.
Plaintext
[User Input Node] ──► [Dijkstra Process (O(V^2))] ───────► Single-Source Shortest Path
                  ──► [Floyd-Warshall (O(V^3) Matrix)] ──► Multi-Source All-Pairs Routing
Dijkstra’s Algorithm: Dynamically tracks the shortest path from a selected starting city to target nodes. It calculates edge weights (representing distance or fuel cost) and uses relaxation steps to find the optimal path in O(V 
2
 ) time.
Floyd-Warshall All-Pairs Route Planner: Pre-computes and caches shortest paths between all pairs of nodes within an adjacency matrix of size V×V in O(V 
3
 ) time, allowing for instant path queries.
Memory Optimization: Bypasses overhead by utilizing static pointers, sequential arrays, and manual heap allocations to prevent memory leaks during real-time UI rendering.
Core Focus: Live statistics tracker engineered using parallel data pipelines in Java Swing.
🛠️ How It Works:
This desktop UI manages student records by utilizing a tightly coupled Parallel ArrayList Structure where elements are kept in sync by their index position:
Plaintext
  Index:       [0]          [1]          [2]
snames:    ["Alice"]   ── ["Bob"]   ── ["Charlie"]
              ▲              ▲            ▲
              │ Parallel Alignment        │
              ▼              ▼            ▼
sgrades:    [88.5]     ── [92.0]    ── [76.4]
Index-Synchronized Modifiers: Adding, modifying, or deleting records is synchronized across both arrays:
Java
snames.remove(targetIndex);
sgrades.remove(targetIndex); // Retains 1:1 structural alignment
Non-Mutating Sorted Iteration: To list the top-performing students without shuffling the main lists, the app instantiates a temporary array of indices:
Indices=[0,1,2,…,N−1]
The app then sorts this index array based on the values in sgrades using an indirect sorting algorithm. This allows the system to display ranked summaries without losing the structural association between names and grades.
Core Focus: Interactive web engine predicting rain thresholds using supervised regression.
🛠️ How It Works:
An ML-powered predictive web application written in Python and deployed via Streamlit.
Plaintext
[Climatic Raw Telemetry] ──► [MinMaxScaler Normalization] ──► [Scikit-Learn Regression Pipeline] ──► [Rain Prob %]
Data Preprocessing: Standardizes incoming meteorological variables (including barometric pressure, relative humidity, wind speed, and historical metrics) using scaling pipelines (MinMaxScaler).
Inference Engine: Features a trained regression pipeline built on Scikit-Learn that computes the probability of precipitation based on weather patterns.
Streamlit UI: Provides an interactive interface, updating prediction metrics and generating visual correlation plots on-the-fly.
Core Focus: A secure reservation platform utilizing index-mapped SQL database lookups.
🛠️ How It Works:
A secure reservation system that manages airline schedules, passenger bookings, and seat inventory.
Plaintext
[User Search Query] ──► [MySQL Index Cache] ──► [3NF Relational Schema] ──► [Secure Seating Map Lock]
Relational Schema: Implements a normalized database schema (Third Normal Form) using MySQL to eliminate data redundancy and prevent anomalous update behaviors.
Booking System Operations: Uses SQL query optimization, customized search indexes, and relational constraints to search flights, assign seating maps, and book tickets under low latency.
Core Focus: Front-end interactive applications and creative portfolio spaces.
🛠️ How It Works:
Interactive Design: Custom HTML, CSS, and JS engines focused on clean layouts, smooth UI transitions, and responsive components across devices.
Creative Visuals: Optimized for fast rendering speeds using pure CSS animations and minimal script overhead.
⏳ Current Sprint // Active Threads
📉 Student Grade Tracker
Objective: Building an event-driven desktop utility to securely analyze classroom distribution fields.
State: Enforcing 1:1 index alignment via an explicit Parallel ArrayList Structure (snames⟺sgrades).
Next Commit: Implementing an indirect pointer index sorting engine to filter top N percentile student arrays without mutating master memory references.
⚡ Git Performance & Telemetry Dashboard
💬 Connect Interfacing Protocol
JavaScript
const engineer = {
  name: "Shifa Parveen",
  protocols: ["Applied_Deep_Learning", "Graph_Theory_Optimization", "System_Automation"],
  manifesto: "Talk is cheap. Show me the code. — Linus Torvalds"
};
📡 Active Port: Let's cross-reference ideas or talk data architectures over on LinkedIn.
