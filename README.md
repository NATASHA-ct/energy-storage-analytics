<a name="readme-top"></a>

# 📗 Table of Contents

- [📖 About the Project](#about-project)
  - [🛠 Built With](#built-with)
  - [Key Features](#key-features)
  - [Key Findings](#key-findings)
  - [📊 Sample Outputs](#sample-outputs)
- [💻 Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Setup](#setup)
  - [Install](#install)
  - [Usage](#usage)
- [👥 Authors](#authors)
- [🔭 Future Features](#future-features)
- [🙏 Acknowledgements](#acknowledgements)
- [📝 License](#license)

---

# 📖 Energy Storage Analytics <a name="about-project"></a>

> A Python data analysis project exploring the technical characteristics 
> of 25 battery storage units connected across a 5-bus power grid.

This project loads, merges, analyses and visualises real-world-style 
storage data. It computes key metrics including energy capacity, filters 
and summarises data using pandas, builds interactive visualisations using 
Plotly, and ranks storage units using a weighted cost-effectiveness 
scoring model.

**Key formula:** 

```Energy Capacity (kWh) = Power Capability (kW) × Duration (hours) ```

## 🛠 Built With <a name="built-with"></a>

### Tech Stack

- **Language:** Python 3.13
- **Libraries:** pandas, matplotlib, plotly, openpyxl
- **Environment:** Jupyter Notebook (VS Code)

### Key Features <a name="key-features"></a>

- **Data merging** : combines two datasets using pandas `.map()` 
  (Python equivalent of Excel VLOOKUP)
- **Energy capacity computation** : calculates capacity for all 25 storage units
- **Conditional filtering** : replicates Excel SUMIFS and AVERAGEIFS 
  using pandas boolean filtering
- **Interactive visualisations** : Plotly charts with hover tooltips 
  and legend interactivity
- **Cost-effectiveness scoring** : weighted ranking model combining 
  efficiency, capacity and duration
- **Data quality analysis** : identifies and fixes inconsistencies 
  in the original dataset

<p align="right">(<a href="#readme-top">back to top</a>)</p>

---

## 📈 Key Findings <a name="key-findings"></a>

Analysis of 25 battery storage units across a 5-bus power grid revealed 
the following:

**Data Quality:**
- stor999 was recorded as "bus 2" instead of "bus_2" ; causing it to be 
  excluded from grouped analysis entirely until corrected. Small naming 
  inconsistencies can quietly distort results at grid scale.

**Energy Capacity:**
- bus_1 has the highest total energy capacity at 1,099 kWh across 7 storage units.
- stor11 on bus_5 has the highest individual energy capacity at 516 kWh ; 
  driven by a combination of high power capability (86 kW) and long duration (6 hours).

**Conditional Analysis:**
- Only 9 out of 25 storage units have efficiency above 0.85.
- Only 3 storage units simultaneously meet both high efficiency AND 
  long duration conditions.
- When efficiency is used as a filter, bus_5 becomes the strongest 
  performer ; replacing bus_1 which dominated raw totals.

**Cost-Effectiveness Scoring:**
- stor11 ranks 1st with a score of 0.87.
- stor24 ranks 2nd despite low efficiency (0.75) ; its exceptional 
  capacity (468 kWh) compensates. This highlights a key limitation ; 
  large but inefficient storage units can rank highly in capacity-weighted models.
- stor17 has the highest efficiency (0.90) but ranks only 6th ; 
  proving efficiency alone is insufficient without sufficient capacity.

**Engineering Implication:**
Raw capacity totals are misleading without efficiency context. A storage 
unit operating at 65% efficiency wastes 35% of input energy every 
charge/discharge cycle ; a significant operational and financial cost at grid scale.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

---

## 📊 Sample Outputs <a name="sample-outputs"></a>

![Cost-Effectiveness Ranking](assets/ranking_chart.png)

![Efficiency vs Capacity](assets/scatter_plot.png)

![Score Table](assets/score_table.png)

<p align="right">(<a href="#readme-top">back to top</a>)</p>

---

## 💻 Getting Started <a name="getting-started"></a>

### Prerequisites

- Python 3.x installed on your machine
- VS Code with the Jupyter extension installed

### Setup

Clone this repository:
```sh
git clone https://github.com/NATASHA-ct/energy-storage-analytics.git
cd energy-storage-analytics
```

### Install

Install all dependencies:
```sh
pip install -r requirements.txt
```

### Usage

All notebooks are in the `notebooks/` folder. Open and run in order:

| Notebook | Description |
|---|---|
| 01_load_merge_analyse.ipynb | Load, merge and analyse storage unit data |
| 02_sumifs_averageifs.ipynb | Filter and summarise data using pandas |
| 03_interactive_charts.ipynb | Interactive visualisations with Plotly |
| 04_cost_effectiveness.ipynb | Cost-effectiveness scoring per storage unit |

Run all cells from top to bottom using **Run All**.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

---

## 👥 Authors <a name="authors"></a>

👤 **Natasha Chirombe**

- GitHub: [@NATASHA-ct](https://github.com/NATASHA-ct)
- LinkedIn: [Natasha Chirombe](https://www.linkedin.com/in/natashatatendachirombe/)

<p align="right">(<a href="#readme-top">back to top</a>)</p>

---

## 🔭 Future Features <a name="future-features"></a>

- [ ] Incorporate real capital cost data (£/kWh) into the scoring model
- [ ] Build a Streamlit dashboard with adjustable scoring weights
- [ ] Apply scoring methodology to a larger real-world grid dataset

<p align="right">(<a href="#readme-top">back to top</a>)</p>

---

## 🙏 Acknowledgements <a name="acknowledgements"></a>

- **Dr. Spyros Giannelos** — Imperial College London for the real storage data.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

---

## 📝 License <a name="license"></a>

This project is [MIT](./LICENSE) licensed.

<p align="right">(<a href="#readme-top">back to top</a>)</p>