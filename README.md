🎧 Spotify Top 1000 Artist Collaboration Network

Advanced Network Analysis of the Global Music Ecosystem

<p align="center"> <img src="https://img.shields.io/badge/Python-3.10-blue" /> <img src="https://img.shields.io/badge/NetworkX-Analysis-green" /> <img src="https://img.shields.io/badge/Gephi-Visualization-orange" /> <img src="https://img.shields.io/badge/Data-Spotify%20API-red" /> </p>

📌 Overview

This project constructs and analyzes one of the most comprehensive collaboration networks of Spotify’s Top 1000 artists, uncovering hidden structures, influential musicians, and the cross-genre bridges that shape modern music.

Using Python, NetworkX, Gephi, and the Spotify API, the project transforms raw discography data into a high-resolution network model of 817 artists and 5,263 collaboration edges, complete with weighted relationships, genre mapping, and centrality insights.

The work answers questions about artist influence, genre mixing, small-world behavior, and structural features of the global music industry.

<img width="688" height="610" alt="image" src="https://github.com/user-attachments/assets/de419414-4d27-43f8-8b1e-aa063d2e659c" />

<img width="492" height="579" alt="image" src="https://github.com/user-attachments/assets/b9dde5ac-1b35-4755-8fb8-ff2aae485e29" />


🔍 Key Highlights
✔ Fully Automated Data Pipeline

Scraped Top 1000 Spotify artists from Chartmasters using BeautifulSoup

Queried Spotify’s API to extract albums, tracks, collaborations, and genres

Cleaned and normalized messy artist metadata

✔ Full Network Construction

Built a weighted, undirected collaboration graph

Incorporated genre and popularity as node attributes

Removed isolated components to analyze the giant connected core

✔ Advanced Network Science

Calculated centrality metrics (eigenvector, betweenness, degree)

Identified collaboration hubs and influential genre connectors

Performed statistical comparisons using degree-preserving null models

Computed clustering coefficient and average shortest path length

✔ High-Quality Visualizations

Generated global and sub-network views in Gephi

Colored nodes by genre: Hip-Hop, Pop, Country, EDM, Urbano Latino, etc.

Highlighted influential bridges and isolated communities

🧠 Research Questions

Which artists are most influential in the global collaboration landscape?
Measured using eigenvector centrality and degree-weighted relationships.

Which artists serve as genre bridges and why do they matter?
Identified using betweenness centrality and cross-cluster connectivity.

📂 Dataset Summary
Component	Value
Artists	817
Collaboration Edges	5,263
Avg Degree	13.1
Max Degree	89
Avg Shortest Path (Largest Component)	3.6
Clustering Coefficient	0.17

The degree distribution followed a heavy-tailed structure consistent with scale-free networks, while the short average path length and high clustering indicated small-world characteristics, aligning with previous studies on collaboration networks.

🎨 Visualizations
Genre-colored Global Network
[Insert Gephi visualization here]

High-Influence Artist Ego Network
[Insert Figure 3]

Low-Influence Artist Ego Network
[Insert Figure 4]

Genre-Isolated Subnetwork
[Insert Figure 6]

📊 Null Model Evaluation

To determine whether the observed structure was meaningful, we compared the network to a degree-preserving randomization model.

Metric	Null Model Mean	Artist Network
Clustering Coefficient	0.0278	0.17
Avg Path Length	2.963	3.6

These significant deviations indicate that the network’s structure is non-random and driven by real collaboration patterns, not statistical noise.

🧩 Tools & Technologies

Python

NetworkX

Pandas

Requests / Spotify API

BeautifulSoup

Gephi

Power BI for tables

Jupyter Notebooks

📁 Repository Contents
├── data/                     # Raw + cleaned datasets  
├── notebooks/                # Analysis and model building  
├── src/                      # Python scripts for scraping + processing  
│   ├── scraper.py  
│   ├── spotify_api.py  
│   ├── network_builder.py  
│   ├── analysis.py  
│   └── visualization.py  
├── figures/                  # Network visualizations  
└── README.md

🚀 How to Run
git clone https://github.com/SamiHossain/Spotify-Network
cd Spotify-Network
pip install -r requirements.txt
python src/analysis.py


You will need a Spotify API key in an .env file:

SPOTIFY_CLIENT_ID=your_id
SPOTIFY_SECRET=your_secret
