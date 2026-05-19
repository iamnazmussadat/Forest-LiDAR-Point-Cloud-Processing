# Integrating LLMs into Geospatial Workflows: A Case Study in Forest LiDAR Point Cloud Processing

This repository contains a complete, Python-based pipeline for processing and analyzing a large-scale terrestrial LiDAR dataset (`forest.las` containing over 178 million points) across a 90m × 90m forest plot. The pipeline was developed as part of an MSc project at Hochschule Neubrandenburg.

## 📌 Project Overview
The main objective of this project is to extract vital forestry metrics—such as Tree Identification, Digital Terrain Models (DTM), Canopy Height Models (CHM), and Stem Diameters (DBH)—from high-density LiDAR point clouds. 

### 🛠️ The Technical Challenge & Solution
* **The Problem:** Processing a **4.3 GB** LAS file on a standard computer causes memory (RAM) overflow.
* **The Solution:** Implemented a highly optimized memory-efficient pipeline using the `laspy` library's `chunk_iterator()` method combined with a dictionary-based (`defaultdict`) custom gridding strategy. This allows the 178-million-point dataset to be processed in chunks without overloading the machine.

## 📂 Repository Contents
* **`Forest LiDAR Point Cloud Processing.pdf`**: The full, formal scientific paper detailing the research background, methodologies, and findings.
* **`[Your-Notebook-Name].ipynb`**: The interactive Jupyter Notebook containing the full execution pipeline:
  1. Memory-efficient chunked file reading.
  2. Ground point filtering & Digital Terrain Model (DTM) generation.
  3. Non-ground normalization & Canopy Height Model (CHM) generation.
  4. Individual tree segmentation and stem diameter (DBH) estimations.

## ⚙️ Core Stack & Libraries Used
* **Language:** Python
* **Geospatial & Point Cloud Processing:** `laspy`, `numpy`, `scipy`
* **Visualization:** `matplotlib`
