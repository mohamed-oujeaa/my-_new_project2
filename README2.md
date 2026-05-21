# AI-Driven Urban Traffic Light Optimization

Final project for the Building AI course

## Summary

This project aims to optimize traffic light timings at busy city intersections using real-time traffic camera data. Instead of relying on fixed, outdated timers, this AI system dynamically adjusts green light durations based on the live queue length of vehicles, reducing gridlock and carbon emissions.

## Background

* **The Problem:** Traditional traffic lights operate on rigid schedules, causing empty lanes to have green lights while congested cross-streets sit idling. This wastes time, increases commuter frustration, and spikes fuel emissions.
* **Importance:** Smart city infrastructure reduces urban congestion, improves emergency vehicle response times, and cuts down city-wide greenhouse gases.
* **Motivation:** As cities grow denser, software solutions offer a much cheaper and faster way to improve infrastructure compared to physical road expansion.

## How it Works

The system operates in a continuous real-time loop:
1. **Inputs:** Live camera frames from four-way intersections tracking vehicle counts per lane.
2. **Processing:** A computer vision algorithm detects and counts the vehicles. 
3. **Decision Matrix:** A lightweight heuristic/neural network takes the current vehicle counts and predicts the optimal next cycle duration ($T_{green}$) for each lane.
4. **Output:** A precise duration signal sent directly to the electronic traffic light controllers.

## AI Methods & Tech Stack

This project maps out the usage of standard Python tools to simulate the environment:

| Phase | AI Method / Approach | Libraries used |
| :--- | :--- | :--- |
| **Object Detection** | Contour detection / CNNs | OpenCV / Scikit-image |
| **Decision Logic** | Nearest Neighbor Classification (k-NN) | NumPy / Scikit-learn |
| **Simulation** | Multi-agent traffic flow modelling | Matplotlib / Custom Loops |

## Challenges

* **Hardware Constraints:** Processing high-framerate video feeds at the edge (on the actual intersection controller) requires high computational efficiency.
* **Edge Cases:** Handling extreme weather conditions (heavy snow, downpours, or night glare) where vehicle detection accuracy might drop.
* **Safety:** Ensuring the AI can never override crucial safety gaps (like yellow light minimum durations or emergency vehicle overrides).

## What's Next?

Future iterations will move from isolated intersections to a **Networked Grid AI**, where multiple intersections communicate with one another to predict traffic waves before they arrive. To achieve this, the next step involves implementing Deep Q-Learning (Reinforcement Learning).

## Acknowledgments

* Elements of AI / Building AI course team.
* Open-source traffic simulation concepts.
