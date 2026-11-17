# LexiSpace 3D | NLP Tokenizer & 3D Word Embedding Visualizer

An interactive educational Natural Language Processing (NLP) dashboard that demonstrates how text is tokenized, how a vocabulary dictionary is constructed, and how words are represented as geometric vectors in an interactive 3D coordinate embedding space.

Built with a light theme, modern glassmorphism UI, **Three.js**, **OrbitControls**, **Chart.js**, **Lucide Icons**, and **Tailwind CSS**.

---

## 🌟 Key Features

### 1. Multi-Strategy Text Tokenizer
- **Word-Level Tokenization**: Splits text by word boundaries with lowercasing and punctuation cleaning.
- **Subword (BPE Simulation)**: Simulates Byte-Pair Encoding (`play` + `##ing`, `un##` + `known`) to demonstrate how modern LLMs (BERT, GPT, LLaMA) tokenize text.
- **Character-Level Tokenization**: Atomic character tokens.
- **Color-Coded Token Chips**: Real-time generation of token badges with corresponding sequential Token IDs.
- **Encoded Sequence Output**: Interactive representation of numerical arrays (e.g., `[4, 0, 1, 2, 3, 4, 5, 1, 2]`) with 1-click clipboard copy.

### 2. Automatic Vocabulary Builder & Persistence
- Automatically learns unseen words from entered sentences and assigns sequential Token IDs.
- Tracks term frequencies across sentences with real-time frequency counters.
- **Full Table Management**: Search by word or Token ID, filter by category (*Animals, Technology, Emotions, Actions, Objects, Grammar*), and sort by ID, frequency, or vector norm.
- **Persistent Storage**: All vocabulary terms, frequencies, and custom coordinates persist via browser `localStorage`.
- **Import / Export**: Export and import vocabulary sets as JSON.

### 3. Sentence Numerical Encoder & Decoder
- Encodes custom input sentences into token sequences using the active vocabulary.
- **Out-Of-Vocabulary (OOV) Handling**: Flags unknown words with `<UNK>` tags and provides a 1-click **Add UNK to Vocab** button.
- **Sequence Decoder**: Reconstructs human text from numerical Token ID arrays (e.g. `[4, 0, 1, 2]`).

### 4. Interactive 3D Word Embedding Space (Three.js)
- **3D Coordinate System**: Rendered with axes (X = Rose, Y = Emerald, Z = Cyan) and an orbital ground grid.
- **Node Embeddings**: Words are rendered as glowing 3D spheres scaled logarithmically by frequency.
- **High-DPI Billboard Labels**: Text labels rendered using dynamic HTML5 canvas sprites that always face the camera with category color indicators.
- **Interactive Similarity Connections**: Dynamically draws 3D links between words whose cosine similarity meets the adjustable threshold slider.
- **Camera Presets & Controls**: Smooth orbit, zoom, pan, camera reset, perspective presets (*Top, Front, Isometric*), and auto-orbit rotation.
- **Direct 3D Node Dragging**: Toggle **Drag: ON** to reposition word nodes directly in 3D space with live coordinate synchronization.
- **2D PCA Projection Mode**: Toggle between 3D spatial space and 2D ground plane projection.
- **3D Search Spotlight**: Live search bar inside the 3D viewport toolbar to locate and focus on words.
- **Snapshot PNG**: Download a high-res PNG snapshot of the 3D graph.

### 5. Cosine Similarity Calculator & Math Lab
- Computes cosine similarity between any two selected words:
  $$\cos(A, B) = \frac{A \cdot B}{\|A\| \times \|B\|}$$
- Color-coded similarity gauge from $-1.000$ (opposite) to $+1.000$ (identical) with angular separation in degrees.
- Step-by-step vector math breakdown: Euclidean norms ($\|A\|$, $\|B\|$), dot products, and calculations.
- Top 5 nearest semantic neighbors with 1-click **Fly to 3D** buttons.
- Connects compared words in 3D with an animated laser beam.

### 6. Semantic Vector Word Math (Analogy Lab)
- Demonstrates vector arithmetic:
  $$\text{Vector}(A) - \text{Vector}(B) + \text{Vector}(C) \approx \text{Target}$$
  *(e.g., King &minus; Man + Woman = Queen)*
- Automatically queries the vocabulary for the closest semantic match in 3D space.

### 7. Attention & Co-occurrence Heatmap Matrix
- $N \times N$ contextual matrix displaying token-to-token affinity and simulated attention weights.
- Hovering over matrix cells highlights the pair and projects their connection in 3D.

### 8. Analytics & Corpus Metrics
- Lexical diversity (Type-Token Ratio TTR), average word length, and vector magnitude.
- Interactive Chart.js Zipfian frequency distribution bar chart.
- Theme toggle: Light Mode and Dark Mode support.

---

## 🚀 Quick Start

No build tools or server dependencies required!

### 1. Clone the repository
```bash
git clone https://github.com/kurkurenishant/LLM-pipeline-expoler.git
cd LLM-pipeline-expoler
```

### 2. Run
Simply open `index.html` in any web browser:
```bash
open index.html
```

---

## 🛠️ Tech Stack
- **HTML5 / CSS3 / JavaScript (ES6+)**
- **Tailwind CSS** (UI & Layout)
- **Three.js (r128)** & **OrbitControls** (3D WebGL Canvas)
- **Chart.js** (Corpus Analytics)
- **Lucide Icons**
- **Web Audio API** (Sound FX feedback)

---

## 📄 License
MIT License. Open for educational and research exploration.
