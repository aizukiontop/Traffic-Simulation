# Traffic-Simulation
A real-time traffic simulation of a four-way intersection with three lanes per approach, including a dedicated left-turn lane with its own signal. Cars, trucks, buses and motorcycles spawn at a configurable rate and follow each other using the Intelligent Driver Model (IDM). The simulation is rendered in pygame, with live stats for vehicles passed, vehicles present and average vehicles per minute. It also runs as an experiment: every 300 simulated seconds it logs the signal cycle length and vehicles passed to data.csv, then increases the cycle length, so you can analyze how signal timing affects throughput.
**Repository:** https://github.com/aizukiontop/Traffic-Simulation

## Features

- **Four-Way Intersection:** Simulates a four-way intersection with three lanes per approach.
- **Dedicated Left-Turn Lanes:** Includes dedicated left-turn lanes with their own traffic signals.
- **Multiple Vehicle Types:** Simulates cars, trucks, buses, and motorcycles.
- **Intelligent Driver Model (IDM):** Models vehicle acceleration, braking, and following distances.
- **Real-Time Visualization:** Displays traffic movement, vehicles, and signals using Pygame.
- **Live Statistics:** Tracks simulation time, vehicles passed, vehicles present, and average vehicles per minute.
- **Configurable Vehicle Spawning:** Adjusts the rate at which vehicles enter the simulation.
- **Automated Experiments:** Records traffic signal cycle lengths and vehicle throughput every 300 simulated seconds.
- **CSV Data Logging:** Saves experimental results to `data.csv` for further analysis.
- **Adjustable Signal Timing:** Increases the signal cycle length by one second after every five experimental runs.

## Built With

- **Python** – Core programming language.
- **Pygame** – Real-time simulation rendering and visualization.
- **NumPy** – Numerical computations.
- **SciPy** – Scientific computing.
- **Intelligent Driver Model (IDM)** – Vehicle-following behavior.
- **CSV** – Experimental data storage.

## How It Works

Vehicles spawn at configurable rates and travel toward and through the intersection. The Intelligent Driver Model (IDM) determines how vehicles adjust their acceleration and maintain safe following distances based on traffic conditions.

Traffic signals regulate vehicle movement through the intersection, including the dedicated left-turn signals.

The simulation also functions as a traffic signal timing experiment:

1. The simulation runs for 300 simulated seconds.
2. The current signal cycle length and number of vehicles passed are recorded in `data.csv`.
3. After every five experimental runs, the signal cycle length increases by one second.
4. The experiment continues, collecting data for comparison across different signal timings.

The resulting dataset can be used to investigate the relationship between traffic signal timing and intersection throughput.

## Requirements

- Python 3.9 or later
- pip (Python package manager)

**Note:** Python 3.12 and newer versions may require compatible dependency versions. Python 3.14 may require `pygame-ce` if a compatible Pygame package is unavailable.

## Installation and Setup

### 1. Clone the Repository

```bash
git clone https://github.com/aizukiontop/Traffic-Simulation.git
cd Traffic-Simulation

### 2. Create a Virtual Environment (Optional)

**Windows:**

```bash
python -m venv venv
venv\Scripts\activate

3. Install Dependencies
python -m pip install -r requirements.txt

If installation fails because of incompatible pinned package versions, try:
python -m pip install numpy scipy pygame

For newer Python versions where Pygame is unavailable, try:
python -m pip install numpy scipy pygame-ce

4. Run the Simulation
python main.py

```
## Controls

| Control | Action |
|---|---|
| Mouse wheel | Zoom in and out |
| Click and drag | Pan around the simulation |
| Close the window | Exit the simulation |

## Configuration

The following settings can be adjusted in `main.py`:

| Setting | Description |
|---|---|
| `VEHICLE_RATE` | Controls the vehicle spawning rate, measured in vehicles per minute. |
| `STEPS_PER_UPDATE` | Controls simulation speed; increasing the value advances the simulation faster. |
| `win.zoom` | Controls the initial zoom level. |

## Experimental Data

The simulation automatically appends experimental results to `data.csv`.

Each experiment records the following information:

| Column | Description |
|---|---|
| `cycle_length` | Traffic signal cycle length used during the experiment. |
| `vehicles_passed` | Number of vehicles that passed through the intersection during the experimental interval. |

Each experimental interval lasts 300 simulated seconds. After every five runs, the signal cycle length increases by one second.

The collected data can be analyzed using spreadsheet software or Python to compare vehicle throughput across different signal timings.

**Important:** Run the simulation from the project directory to ensure that `data.csv` is saved in the expected location. Back up or remove the existing CSV file before starting a fresh experiment.

## Project Objective

To simulate traffic behavior at a four-way intersection and investigate how varying traffic signal cycle lengths affect vehicle throughput using the Intelligent Driver Model (IDM).

The project combines real-time visualization, vehicle-following behavior, traffic signal control, and automated data collection to support the analysis of intersection efficiency.




