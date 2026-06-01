# 🚀 Hello World, I'm Shifa Parveen! <img src="https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExM3B0bTM0b3g1Mnd6NmR4M21sczNvaDJnd3RscXBybXN5Y3VwYndpYiZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9cw/L1R1TVr9WSlg5B3FiF/giphy.gif" width="35px">

<p align="left">
  <a href="https://www.linkedin.com/in/shifa-parveen-286251307"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
</p>

### 🎓 The Brief
I am a **Computer Science Major** deeply invested in the intersection of **Data Science, Machine Learning**, and algorithmic optimization. From engineering optimized graph navigation backends in C to deploying predictive statistical architectures in Python, I build software that translates raw computational data into functional human decisions.

---

## 🛠️ Computational Arsenal & Tech Stack

<table width="100%">
  <tr>
    <td width="50%" valign="top">
      <h4>💻 Languages & Core Engines</h4>
      <ul>
        <li><b>Languages:</b> Python, C, Java, SQL</li>
        <li><b>Databases & Web:</b> MySQL, Streamlit, GTK+ 3.0</li>
        <li><b>Version Control:</b> Git, GitHub</li>
      </ul>
    </td>
    <td width="50%" valign="top">
      <h4>📊 Data Science & Frameworks</h4>
      <ul>
        <li><b>Analysis:</b> Pandas, NumPy, Matplotlib</li>
        <li><b>Machine Learning:</b> SciKit-Learn, Keras, TensorFlow</li>
        <li><b>Core Fields:</b> Computer Vision, Graph Theory, Metric Learning</li>
      </ul>
    </td>
  </tr>
</table>

---

## 📂 Active Engineering Space

### 🧪 Featured Productions

<details open>
<summary><b>👤 Facial Books — Automated Employee Time-Tracking & Payroll via Deep Learning</b></summary>
<br>

> **Core Focus:** Computer Vision, One-Shot Metric Learning, & Real-Time Payroll Automation

* **The Vision:** An AI-powered enterprise workspace utility that completely replaces manual check-in systems. By leveraging a Siamese Neural Network trained completely from scratch, FacialBooks executes real-time facial recognition via a webcam feed, running simultaneous automated mathematical payroll allocations and entry/exit timestamping.
* **Core Algorithmic Architecture:** Unlike traditional binary classifiers that scale poorly and overfit on small sample groups, FacialBooks uses a *One-Shot Metric Learning* approach via a custom Siamese CNN architecture.
* **📐 Optimization & Loss Formulations:** The network transforms raw spatial facial configurations into a continuous, L2-normalized 128-dimensional embedding space. Optimization is achieved through a custom implementation of **Contrastive Loss**, passing image pairs across a margin of $m = 1.0$:
  $$L_{\text{Contrastive}} = \frac{1}{2}(Y)(D_W)^2 + \frac{1}{2}(1-Y)\max(0, m - D_W)^2$$
  Where $D_W$ is the Euclidean ($L_2$) distance vector computed between two twin face embeddings $G_W(X_1)$ and $G_W(X_2)$:
  $$D_W(X_1, X_2) = \|G_W(X_1) - G_W(X_2)\|_2$$
  At runtime, an empirical decision boundary threshold of $\tau = 0.12$ regulates positive employee authorization sequences.
* **🧬 Neural Network Topology:** * *Input Layer:* Preprocessed $96 \times 96 \times 3$ normalized RGB tensor blocks.
  * *Feature Extraction:* 4 structural convolutional blocks scaling up through 32, 64, 128, and 256 structural filters. Each distinct layer implements an isolated `Conv2D` $\rightarrow$ `BatchNormalization` $\rightarrow$ `ReLU` $\rightarrow$ `MaxPooling` $\rightarrow$ `Dropout` chain sequence.
  * *Embedding Head:* Fully dense compression mapping out onto a strict 128-dimensional vector layer, passing through custom-subclassed `L2Normalize` layers to ensure clean object serialization natively inside Keras.
</details>

<details open>
<summary><b>🕸️ SocialGraph — Intelligent Link Prediction & Recommendation System</b></summary>
<br>

> **Core Focus:** Discrete Mathematics, Graph Theory, Link Prediction, & Network Topologies

* **The Vision:** An intelligent, dependency-free social network modeling and recommendation system that simulates social graphs, visualizes network topology through a real-time force-directed physics engine, and generates highly contextual friend recommendations using a hybrid algorithmic approach.
* **Core Algorithmic Architecture:** The engine blends graph topology and semantic user compatibility to bypass the limitations of purely structural recommendation systems (e.g., missing strong interest overlaps that lack common connections).
* **📐 The Hybrid Recommendation Formula:** For any target user $u$ and potential connection candidate $c$, the system evaluates a unified recommendation score:
  $$\text{Score}(u, c) = 0.6 \times \text{Jaccard}_{\text{Network}}(u, c) + 0.4 \times \text{Jaccard}_{\text{Interests}}(u, c)$$
  * *Network Topology Component (60%):* Evaluates structural proximity using Jaccard Similarity over mutual friend neighborhoods.
  * *Interest Similarity Component (40%):* Computes overlapping affinity across multiple per-category color-coded interest vectors (e.g., Music, Coding, Travel, Gaming).
* **🧬 Data Structures & Algorithmic Paradigm:** * *Core Graph Representation:* In-memory adjacency list built via an optimized `HashMap<Integer, List<Edge>>` paired with metadata node tracking (`HashMap<Integer, UserNode>`).
  * *Candidate Discovery:* Scalable *Triadic Closure Expansion* logic identifying friends-of-friends combined with cross-network semantic interest discovery layers.
  * *Path Routing:* Exact *Breadth-First Search (BFS)* engine computing minimum multi-hop degree separations between arbitrary network nodes.
  * *Ranking Engine:* A high-efficiency *Greedy Max-Heap Priority Queue* returning the Top-$N$ recommendations in $O(K \log N)$ time.
</details>

<details>
<summary><b>📍 Smart Travel Route Planner</b></summary>
<br>

> **Core Focus:** Directed Graph Space Optimization & Memory Efficiency

* Built a desktop application implementing **Dijkstra’s** and **Floyd-Warshall** multi-source matrix routing algorithms using the GTK+ 3.0 library.
* Structured complex internal ad-hoc matrix transformations within lower-level memory models using strict C pointer mechanics.
</details>

<details>
<summary><b>🌧️ Rainfall Prediction System</b></summary>
<br>

> **Core Focus:** Supervised Learning Regression & Micro-Climate Predictive Modelling

* Designed a meteorological forecasting pipeline leveraging Python and `scikit-learn` to analyze historical climate telemetry data.
* Implemented multi-stage data preprocessing stages to extract correlation factors across volatile environmental variables and deployed via Streamlit.
</details>

<details>
<summary><b>✈️ Airline Reservation Management System</b></summary>
<br>

> **Core Focus:** Relational Database Normalization & Transaction Isolation

* Engineered a backend framework for tracking real-time flight schedules, dynamic seat inventory tracking, and secure booking processing operations.
* Optimized data access layers utilizing structured index mapping queries to lower retrieval response time latencies via MySQL.
</details>

---

### ⏳ Current Development Sprint (In Progress)

#### 📉 [Student Grade Tracker (Desktop Platform)](https://github.com/Thepenguin07/Student-Grade-Tracker)
* **Core Focus:** Real-Time Data Pipeline Synchronization & Event-Driven UI Architectures
* **Context Framework:** Developing a high-efficiency desktop utility designed to securely process classroom scoring distributions.
* **Architecture Implementation:** Utilizing closely linked parallel data structures mapped strictly across linear sequence registers to maintain 1:1 data integrity.
* **Next Steps:** Enhancing real-time data calculations to update critical performance metrics instantly on user input, and adding an indirect pointer index sort to isolate top performers.

---

## ⚡ Git Tracking Dashboard

<p align="left">
  <img src="https://github-readme-stats.shion.dev/api?username=Thepenguin07&show_icons=true&theme=tokyonight&count_private=true" alt="Github Stats" width="48%">
  <img src="https://github-readme-streak-stats.herokuapp.com/?user=Thepenguin07&theme=tokyonight&hide_border=true" alt="GitHub Streak" width="48%">
</p>

---

## 💬 Connect Interfacing Protocol

```javascript
const engineer = {
  name: "Shifa Parveen",
  specialties: ["Graph Algorithms", "ML Model Deployment", "Python Automation"],
  philosophy: "Talk is cheap. Show me the code. — Linus Torvalds"
};
