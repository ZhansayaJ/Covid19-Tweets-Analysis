# Social Dynamics of Mentions on Twitter During COVID-19

This project analyzes the **structure and dynamics** of a Twitter mention network during the COVID-19 pandemic. It focuses on the **social behavior**, **assortativity**, and **information propagation** patterns among users.

## Overview

- Constructs a directed mention graph from Twitter data.
- Cleans and preprocesses tweet content.
- Computes structural properties: triangles, chains, connected components.
- Measures **assortativity** based on followers and friends count.
- Tracks how assortativity evolves over time (decile-based analysis).
- Includes insightful visualizations to interpret user behavior.

## Key Findings

- The network exhibits **low triangle count**, indicating **broadcast-style** communication rather than group discussions.
- Presence of **long chains** suggests relay-like **viral spread** mechanisms.
- Real network shows **high assortativity** for friends and followers.
- Randomized networks show much lower assortativity → confirming real-world structure is non-random.
- **Assortativity spikes over time** may reflect responses to major events.

## Dataset

The dataset contains:
- `user_name`: Twitter handle of tweet author.
- `text`: Tweet content.
- `date`: Timestamp of tweet.
- `followers_count`, `friends_count`: Metadata on user’s network.

Mentions are extracted from the text using regular expressions (`@username`), and a directed graph is built using NetworkX.

## Methods

- Graph construction with `networkx`
- Assortativity with `nx.degree_assortativity_coefficient` and attribute mixing
- Structural analysis (LCC, isolates, chains, clustering)
- Time segmentation into deciles
- Visualizations with `matplotlib` and `seaborn`

## Sample Visualizations

- Histogram of user influence (followers/friends)
- Scatter plots comparing mentioned vs. non-mentioned users
- Evolution of assortativity over time
- Network snapshots for key time windows
