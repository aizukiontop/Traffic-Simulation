# Traffic-Simulation
A real-time traffic simulation of a four-way intersection with three lanes per approach, including a dedicated left-turn lane with its own signal. Cars, trucks, buses and motorcycles spawn at a configurable rate and follow each other using the Intelligent Driver Model (IDM). The simulation is rendered in pygame, with live stats for vehicles passed, vehicles present and average vehicles per minute. It also runs as an experiment: every 300 simulated seconds it logs the signal cycle length and vehicles passed to data.csv, then increases the cycle length, so you can analyze how signal timing affects throughput.
## What it Does

- Simulates a four-way intersection with three lanes per approach.
- Includes dedicated left-turn lanes with independent traffic signals.
- Spawns different vehicle types, including cars, trucks, buses, and motorcycles, at configurable rates.
- Uses the Intelligent Driver Model (IDM) to simulate realistic acceleration, braking, and vehicle-following behavior.
- Visualizes real-time traffic movement using Pygame.
- Displays live traffic statistics:
  - Total vehicles passed
  - Current number of vehicles present
  - Average vehicles passed per minute
- Automatically conducts traffic signal timing experiments every 300 simulated seconds.
- Records signal cycle lengths and vehicle throughput in data.csv.
- Increases the signal cycle length after each experiment to compare traffic performance under different timing configurations.

## Built With

- Python – Core programming language.
- Pygame – Real-time traffic simulation and visualization.
- Intelligent Driver Model (IDM) – Vehicle-following and acceleration behavior.
- CSV – Experimental data storage and analysis.

## How It Works

The simulation continuously generates vehicles that approach and navigate a four-way intersection. Each vehicle follows the IDM algorithm to maintain a safe distance from the vehicle ahead while adjusting its speed based on surrounding traffic conditions.

Traffic signals control vehicle movement through the intersection, including a dedicated signal for left-turning vehicles.

Every 300 simulated seconds, the system records the current traffic signal cycle length and the total number of vehicles passed into data.csv. The signal cycle length is then increased, and a new experimental interval begins.

The collected data can be used to analyze how different traffic signal timings influence intersection throughput.

## Running It Yourself

### Prerequisites

- Python 3.9 or later
- pip (Python package manager)

