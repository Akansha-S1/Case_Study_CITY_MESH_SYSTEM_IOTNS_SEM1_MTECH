# Case_Study_CITY_MESH_SYSTEM_IOTNS_SEM1_MTECH
# CityMesh-AIoT

## Multi-Technology Communication Selection and Resilient Networking for City-Wide AIoT

> **An AIoT communication framework for selecting the most suitable IoT network for each device class using TOPSIS, battery-life analysis, communication measurements, and backup-link reliability.**

---

## 📌 Overview

Modern smart cities contain thousands of IoT devices used for applications such as:

* Environmental monitoring
* Smart water management
* Energy monitoring
* Waste management
* Public safety
* Traffic management
* Flood monitoring
* Infrastructure monitoring

The major challenge is that these devices do **not** have the same communication requirements.

Some devices require:

* Long communication range
* Very low power consumption
* Long battery life
* Low cost

while others require:

* High data rate
* Low latency
* High reliability
* Strong indoor penetration
* Connectivity beyond terrestrial infrastructure

Using a single communication technology for all devices can therefore create coverage gaps, message loss, congestion, unnecessary battery consumption, and poor reliability.

This project proposes **CityMesh**, a multi-technology communication framework that selects an appropriate communication technology according to the requirements of each IoT device class.

The framework evaluates:

**LoRaWAN, NB-IoT, ZigBee, Wi-Fi 6, 5G and Satellite IoT**

and uses:

**TOPSIS + battery-life analysis + mandatory requirement filtering + backup-link reliability**

to create a more resilient city-wide AIoT communication architecture.

---

# 🎯 Problem Statement

A city-wide IoT deployment cannot efficiently rely on a single communication technology because different devices have different requirements for:

* Range
* Data rate
* Latency
* Battery life
* Reliability
* Cost
* Indoor penetration
* Network availability

In the baseline scenario used in this study, a LoRaWAN-only approach does not satisfy all device requirements.

The case study therefore investigates:

> **How can communication technologies be systematically selected for different IoT device classes while improving coverage, reliability and resilience in a city-wide AIoT deployment?**

---

# 💡 Proposed Solution — CityMesh

CityMesh is a hybrid communication-selection framework.

Instead of assigning one network to every IoT device, CityMesh evaluates the requirements of each device class and selects the most appropriate available communication technology.

The proposed framework consists of four major components:

### 1. Multi-Technology Evaluation

Six communication technologies are evaluated:

| Technology    | Main Strength                                       |
| ------------- | --------------------------------------------------- |
| LoRaWAN       | Long range and low power                            |
| NB-IoT        | Deep indoor coverage                                |
| ZigBee        | Short-range self-healing mesh                       |
| Wi-Fi 6       | High throughput                                     |
| 5G            | High speed and low latency                          |
| Satellite IoT | Coverage where terrestrial networks are unavailable |

---

### 2. TOPSIS-Based Selection

TOPSIS is used as the multi-criteria decision-making method.

The technologies are evaluated using criteria such as:

* Message delivery
* Latency
* Battery life
* Range
* Cost
* Reliability

TOPSIS determines the technology that is closest to the ideal solution and farthest from the worst solution.

---

### 3. Mandatory Requirement Filtering

TOPSIS alone does not determine whether a technology is practically acceptable.

Therefore, CityMesh applies a selection rule after ranking.

Technologies that fail mandatory requirements such as:

* Minimum delivery
* Maximum latency
* Minimum battery life
* Maximum cost

are removed before final selection.

The highest-ranked technology among the remaining feasible options is selected.

---

### 4. Backup-Link Reliability

CityMesh introduces a backup communication path.

If the primary network fails, the system can retry through another available communication technology.

This converts the architecture from a single-link system into a more resilient multi-network system.

---

# 🏙️ Case Study

## Smart Water Utility

The proposed system is demonstrated using a smart water utility.

Water infrastructure contains different types of IoT devices with different communication requirements.

Examples include:

| Device/Application    | Requirement                  |
| --------------------- | ---------------------------- |
| Reservoir sensors     | Long range                   |
| Pipeline monitoring   | Long battery life            |
| Basement water meters | Strong indoor penetration    |
| Valves                | Low latency                  |
| Flood gauges          | Reliable remote connectivity |
| Treatment facilities  | High reliability             |

This makes smart water infrastructure a suitable real-world application for demonstrating the CityMesh approach.

The case study also connects with **Sustainable Development Goal 6 (SDG 6): Clean Water and Sanitation**.

---

# 🔬 Research Motivation

The research is motivated by four main observations:

1. Smart-city IoT deployments are rapidly increasing.
2. Different IoT applications require different communication characteristics.
3. Existing studies often focus on individual communication technologies or limited technology comparisons.
4. City-scale communication selection requires a systematic framework that considers technical requirements, cost, battery life and reliability together.

CityMesh addresses this by combining communication technology selection with resilience and backup connectivity.

---

# 📚 Base Research

The project uses research on LPWAN and IoT communication technologies as the foundation.

The base research by **Mekki et al.** compares LPWAN technologies and discusses their performance with respect to factors such as:

* Battery lifetime
* Capacity
* Cost
* Latency
* Quality of service

The literature indicates that different technologies have different strengths rather than one technology being universally optimal.

This supports the motivation for a multi-technology selection framework.

---

# 🔎 Research Gap

The project identifies the following gaps:

### Gap 1 — Limited Technology Comparison

Many studies focus on a subset of communication technologies.

CityMesh considers:

**LoRaWAN + NB-IoT + ZigBee + Wi-Fi 6 + 5G + Satellite IoT**

---

### Gap 2 — Qualitative Comparison

Technology comparisons are often descriptive.

CityMesh introduces a quantitative decision process using TOPSIS.

---

### Gap 3 — Lack of Common City-Scale Framework

Different technologies are often evaluated independently.

CityMesh evaluates them under a common smart-city scenario.

---

### Gap 4 — Limited Resilience Consideration

Communication selection alone does not guarantee network availability.

CityMesh adds backup-link selection and reliability modelling.

---

# 📊 Communication Technologies

## LoRaWAN

**Advantages**

* Long range
* Low power consumption
* Low deployment cost
* Suitable for battery-powered sensors

**Limitations**

* Low data rate
* Duty-cycle limitations
* Collision problems as device density increases

---

## NB-IoT

**Advantages**

* Cellular infrastructure
* Strong indoor coverage
* Good reliability
* Suitable for low-power IoT

**Limitations**

* Operator dependency
* Recurring connectivity costs

---

## ZigBee

**Advantages**

* Low power
* Mesh networking
* Self-healing capability

**Limitations**

* Shorter range
* Lower throughput

---

## Wi-Fi 6

**Advantages**

* High throughput
* Suitable for high-data-rate applications
* Widely available infrastructure

**Limitations**

* Higher power consumption
* Shorter effective range than LPWAN technologies

---

## 5G

**Advantages**

* High data rate
* Very low latency
* High reliability
* Supports demanding applications

**Limitations**

* Higher deployment cost
* Operator dependency
* Coverage limitations in some locations

---

## Satellite IoT

**Advantages**

* Very wide geographical coverage
* Useful where terrestrial networks are unavailable

**Limitations**

* Higher cost
* Higher latency
* Energy considerations

---

# 📐 Mathematical Model

CityMesh combines multiple mathematical components.

---

## 1. Battery-Life Model

Battery life is estimated using device energy consumption and operating conditions.

The purpose is to ensure that communication selection does not ignore long-term energy requirements.

Battery life becomes one of the criteria considered during network selection.

---

## 2. TOPSIS

TOPSIS stands for:

> **Technique for Order Preference by Similarity to Ideal Solution**

TOPSIS follows the idea that the preferred technology should:

* Be close to the ideal solution
* Be far from the worst solution

The general process is:

```text
Decision Matrix
      ↓
Normalization
      ↓
Weighted Matrix
      ↓
Ideal Best / Ideal Worst
      ↓
Distance Calculation
      ↓
TOPSIS Score
      ↓
Technology Ranking
```

---

## 3. Mandatory Selection Rule

After TOPSIS ranking, technologies are checked against mandatory requirements.

For example:

```text
Technology
     ↓
Meets latency requirement?
     ↓
Meets delivery requirement?
     ↓
Meets battery requirement?
     ↓
Meets cost requirement?
     ↓
YES → Candidate
NO  → Remove
     ↓
Select highest-ranked feasible technology
```

This prevents a technology from being selected solely because of a high overall score when it fails an essential requirement.

---

## 4. Reliability Model

CityMesh models a primary communication link together with a backup link.

Conceptually:

```text
              ┌── Primary Network ──┐
IoT Device ───┤                     ├── Control Centre
              └── Backup Network ───┘
```

If the primary network fails, the backup network can be used.

This increases communication resilience.

---

# 📡 Communication Evidence

The project uses communication measurements to evaluate:

### Path Loss

Path loss represents the reduction in signal strength as communication distance and obstacles increase.

---

### Link Budget

Link budget determines whether sufficient signal margin remains for successful communication.

The measurements show that communication performance changes significantly with distance and environmental conditions.

---

### LoRaWAN Capacity

As more devices share a gateway, message collisions can increase.

Therefore:

```text
More devices
      ↓
More shared transmissions
      ↓
Higher collision probability
      ↓
Lower delivery
```

This demonstrates why network capacity must also be considered in city-scale deployment.

---

# 📂 Datasets

The project uses two public datasets.

---

## Dataset A — Urban LoRaWAN Path Loss

The dataset contains approximately:

**930,753 packets**

The measurements include parameters such as:

* Distance
* RSSI
* Path loss
* Spreading factor
* Airtime

These measurements are used to study LoRaWAN communication behaviour.

---

## Dataset B — Indoor RSSI Measurements

The second dataset contains approximately:

**22,695 indoor RSSI readings**

covering:

* BLE
* Wi-Fi
* ZigBee
* LoRaWAN

The dataset supports comparison of communication performance under indoor conditions.

---

## Combined Dataset

Together:

**930,753 + 22,695 = 953,448 records**

These measurements provide the data foundation for communication analysis.

---

# 🧪 Simulation

The simulation represents a city-scale IoT deployment.

### Simulation Environment

* Approximate area: **400 km²**
* Approximate devices: **100,000**
* Backup radios: **30% of devices**
* Sampled devices used for comparison: **1,500**

The simulation compares:

### Baseline

```text
LoRaWAN Only
```

versus

### Proposed

```text
CityMesh
Multi-Technology Selection
+
Backup Connectivity
```

---

# 📈 Key Results

The baseline and proposed approaches are compared using:

* Device coverage
* Message delivery
* Cost
* Reliability
* Battery requirements

### Baseline

**LoRaWAN-only**

* 55% of devices meet all requirements
* 82.9% normal message delivery
* Approximately $11 per device over ten years

### Proposed Approach

With CityMesh innovations:

* All device requirements can be served
* Delivery improves to 95.6% before backup
* Backup delivery reaches 99.3%
* Ten-year cost becomes approximately $58 per device

---

# 💰 Cost–Reliability Trade-off

CityMesh introduces additional communication cost.

The baseline is approximately:

**$11/device over 10 years**

while the complete proposed configuration is approximately:

**$58/device over 10 years**

The additional cost supports:

* Wider device coverage
* Multiple communication technologies
* Backup connectivity
* Improved reliability

Therefore, the project evaluates the trade-off between **cost and resilience** rather than assuming that maximum reliability has zero cost.

---

# 🚨 Failure Scenario

One important scenario is a water-utility burst pipe.

The system can:

```text
Sensor detects abnormal condition
             ↓
Data transmitted
             ↓
AI / Edge analysis
             ↓
Burst detected
             ↓
Control centre receives alert
             ↓
Isolation action initiated
```

The simulation demonstrates rapid isolation of the burst-pipe scenario.

---

# 🧠 CityMesh Architecture

The proposed architecture connects:

```text
                    ┌───────────────┐
                    │ Cloud / AI    │
                    │ Control      │
                    └───────┬───────┘
                            │
                     Edge Orchestrator
                            │
        ┌───────────────────┼───────────────────┐
        │                   │                   │
     LoRaWAN              NB-IoT              5G
        │                   │                   │
        └───────────────────┼───────────────────┘
                            │
                      IoT Devices
                            │
                     Backup Network
                            │
                     Satellite IoT
```

The edge orchestrator allows communication decisions to be made closer to the devices while the cloud provides centralized management and analytics.

---

# ⚙️ Technology Stack

## Data Analysis

* Python
* Jupyter Notebook
* Pandas
* NumPy
* Matplotlib

## Simulation

* Python
* JavaScript
* HTML
* SVG

## Visualization

* Matplotlib
* FFmpeg
* HTML/SVG animations
* Playwright

## Analysis Components

* Path-loss analysis
* Link-budget calculation
* Battery-life modelling
* Collision analysis
* TOPSIS ranking
* Backup selection
* Reliability modelling

---

# 📁 Repository Structure

```text
CityMesh-AIoT/
│
├── README.md
│
├── datasets/
│   ├── raw/
│   ├── processed/
│   └── README.md
│
├── notebooks/
│   ├── 01_data_analysis.ipynb
│   ├── 02_path_loss_analysis.ipynb
│   ├── 03_link_budget.ipynb
│   ├── 04_topsis_analysis.ipynb
│   ├── 05_battery_analysis.ipynb
│   └── 06_results.ipynb
│
├── src/
│   ├── topsis/
│   ├── battery_model/
│   ├── link_budget/
│   ├── collision_model/
│   ├── reliability/
│   └── citymesh_selection/
│
├── simulation/
│   ├── baseline/
│   ├── citymesh/
│   ├── backup_network/
│   └── scenarios/
│
├── results/
│   ├── figures/
│   ├── tables/
│   ├── csv/
│   └── videos/
│
├── docs/
│   ├── literature-review/
│   ├── mathematical-model/
│   ├── case-study/
│   └── presentation/
│
├── config/
│   └── network_parameters.json
│
├── requirements.txt
│
├── LICENSE
│
└── .gitignore
```

---

# 🚀 Getting Started

## 1. Clone the repository

```bash
git clone https://github.com/<YOUR-USERNAME>/CityMesh-AIoT.git
cd CityMesh-AIoT
```

---

## 2. Create a Python environment

```bash
python -m venv venv
```

### Windows

```bash
venv\Scripts\activate
```

### Linux / WSL

```bash
source venv/bin/activate
```

---

## 3. Install dependencies

```bash
pip install -r requirements.txt
```

---

## 4. Run the notebooks

Start Jupyter:

```bash
jupyter notebook
```

Then open the notebooks in:

```text
notebooks/
```

Run them in numerical order.

---

# 🔬 Recommended Experiment Flow

The complete experiment follows:

```text
Public IoT Datasets
        ↓
Data Cleaning
        ↓
Path Loss Analysis
        ↓
Link Budget Analysis
        ↓
Communication Capacity
        ↓
Battery-Life Estimation
        ↓
TOPSIS
        ↓
Mandatory Requirement Filtering
        ↓
Network Selection
        ↓
Backup-Link Model
        ↓
CityMesh Simulation
        ↓
Baseline Comparison
        ↓
Results
```

---

# 📊 Evaluation Metrics

The system can be evaluated using:

| Metric           | Purpose                                           |
| ---------------- | ------------------------------------------------- |
| Device Coverage  | Measures how many devices meet their requirements |
| Message Delivery | Measures successful communication                 |
| Latency          | Measures communication delay                      |
| Battery Life     | Measures long-term device operation               |
| Range            | Measures communication reach                      |
| Cost             | Measures deployment/operational cost              |
| Reliability      | Measures resilience to link failures              |
| Collision Rate   | Measures congestion                               |
| Recovery Time    | Measures response after link failure              |

---

# ⚖️ Baseline vs CityMesh

| Feature                         | LoRaWAN-Only Baseline | CityMesh     |
| ------------------------------- | --------------------- | ------------ |
| Single technology               | ✓                     | ✗            |
| Multi-technology selection      | ✗                     | ✓            |
| TOPSIS                          | ✗                     | ✓            |
| Battery consideration           | Limited               | ✓            |
| Mandatory requirement filtering | ✗                     | ✓            |
| Backup connectivity             | ✗                     | ✓            |
| Device-specific selection       | ✗                     | ✓            |
| Resilience modelling            | Limited               | ✓            |
| Smart-city scalability          | Limited               | Designed for |

---

# 🌐 Real-World Applications

Although the case study focuses on a smart water utility, the CityMesh framework can be extended to:

### Smart Water

* Leak detection
* Pipeline monitoring
* Reservoir monitoring
* Flood alerts
* Smart meters

### Smart Energy

* Smart meters
* Grid monitoring
* Renewable-energy monitoring
* Energy optimization

### Smart Waste

* Smart bins
* Waste-level monitoring
* Route optimization

### Smart Environment

* Air-quality monitoring
* Weather stations
* Environmental sensors

### Smart Transportation

* Traffic signals
* Road sensors
* Connected infrastructure

---

# 🔮 Future Scope

The proposed roadmap consists of four stages.

### Phase 1 — Model Validation

Validate the communication model using **ns-3** and compare simulated results with real measurements.

### Phase 2 — Ward-Level Pilot

Deploy approximately **1,000 devices** using:

* LoRaWAN
* NB-IoT
* 5G

Measure:

* Message delivery
* Leak detection
* Communication reliability

### Phase 3 — Intelligent Network Selection

Introduce reinforcement learning so that the network orchestrator can dynamically select communication links according to changing conditions.

### Phase 4 — City-Wide Deployment

Scale the framework across the city and extend it to:

* Energy
* Waste
* Air quality
* Environmental monitoring

Satellite connectivity can also be incorporated for areas where terrestrial networks are unavailable.

---

# ⚠️ Limitations

The current study has several limitations:

1. The evaluation is simulation-based rather than a complete field deployment.
2. Some radio parameters, prices and device distributions are assumptions.
3. Managing multiple networks increases operational complexity.
4. Backup links may not always fail independently during extreme events.
5. NB-IoT and 5G depend on mobile operators.
6. Multi-network deployment increases cost compared with a LoRaWAN-only approach.

These limitations define important areas for future validation.

---

# 📚 Research Contributions

The project contributes:

### Contribution 1

A common framework for comparing six IoT communication technologies for smart-city applications.

### Contribution 2

TOPSIS-based multi-criteria communication technology selection.

### Contribution 3

Integration of battery-life considerations into network selection.

### Contribution 4

Mandatory requirement filtering after TOPSIS ranking.

### Contribution 5

Backup-link selection for improved communication resilience.

### Contribution 6

A city-scale simulation combining real IoT communication measurements with network selection.

### Contribution 7

Application of the framework to a smart water utility scenario.

---

# 📖 References

The repository should maintain the complete reference list used in the research paper and presentation.

Key categories include:

* LPWAN comparative studies
* LoRaWAN performance studies
* NB-IoT studies
* IoT communication technology surveys
* TOPSIS methodology
* Reliability modelling
* Smart-city IoT
* SDG 6 / smart water infrastructure
* Public communication datasets

> Full bibliographic references should be maintained in `docs/literature-review/references.bib` or `references.md`.

---

# 👩‍💻 Project Information

**Project:** CityMesh-AIoT

**Domain:**
Internet of Things, Artificial Intelligence of Things, Wireless Communication, Smart Cities

**Application Domain:**
Smart Water Utility

**Core Method:**
TOPSIS Multi-Criteria Decision Making

**Proposed Framework:**
CityMesh

**Simulation:**
City-scale multi-technology IoT communication simulation

**Primary Technologies Evaluated:**

```text
LoRaWAN
NB-IoT
ZigBee
Wi-Fi 6
5G
Satellite IoT
```

---

# 📌 Key Idea

> **CityMesh does not ask which communication technology is best for the entire city. It asks which technology is most suitable for each device class and requirement, and then provides backup connectivity when the primary link fails.**

---

# ⭐ Project Summary

The project demonstrates how a city-wide AIoT communication layer can move from a **single-network approach** to a **multi-technology, requirement-driven and resilient architecture**.

The complete workflow combines:

**Real IoT data**

→ **Communication analysis**

→ **Battery modelling**

→ **TOPSIS**

→ **Requirement filtering**

→ **Network selection**

→ **Backup reliability**

→ **City-scale simulation**

→ **Performance evaluation**

The final objective is to develop a communication framework capable of supporting diverse smart-city IoT applications while balancing **coverage, reliability, battery life, latency and cost**.

---

## License

This project is intended for academic and research purposes.

Add the appropriate license file before public release.

---

## Acknowledgements

This project uses publicly available IoT communication datasets and published research for academic analysis and simulation.

All external datasets, research papers, images and third-party resources should be credited to their respective authors and sources.
