<a name="readme-top"></a>

# 📗 Table of Contents

- [📖 About the Project](#about-project)
  - [🛠 Built With](#built-with)
  - [Key Features](#key-features)
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

> A Python data analysis project exploring the technical characteristics of battery storage units connected across a power grid.

This project loads, merges, and analyses real-world-style storage data for 25 battery units. It computes key metrics including **energy capacity**, and visualises performance by bus and efficiency using pandas and matplotlib.

This is Course 1 of 8 in the **Energy Data Scientist** series, completed under the mentorship of **Dr. Spyros Giannelos (Imperial College London)** via the Skool platform.

**Key formula:**
```
Energy Capacity (kWh) = Power Capability (kW) × Duration (hours)
```

## 🛠 Built With <a name="built-with"></a>

### Tech Stack

- **Language:** Python 3.13
- **Libraries:** pandas, matplotlib, openpyxl
- **Environment:** Jupyter Notebook (VS Code)

### Key Features <a name="key-features"></a>

- **Data merging** — combines two datasets using pandas `.map()` 
  (Python equivalent of Excel VLOOKUP)
- **Energy capacity computation** — calculates capacity for all 25 storage units
- **Visual analysis** — charts comparing storage performance across grid buses

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

Open the notebook in VS Code:
```sh
code energy_storage_analytics.ipynb
```

Then run all cells from top to bottom using **Run All**.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

---

## 👥 Authors <a name="authors"></a>

👤 **Natasha Chirombe**

- GitHub: [@NATASHA-ct](https://github.com/NATASHA-ct)
- LinkedIn: [Natasha Chirombe]( https://www.linkedin.com/in/natashatatendachirombe/)

<p align="right">(<a href="#readme-top">back to top</a>)</p>

---

## 🔭 Future Features <a name="future-features"></a>

- [ ] Translate Excel SUMIFS/AVERAGEIFS analysis to pandas
- [ ] Add interactive charts using Plotly
- [ ] Extend analysis to include efficiency-weighted capacity scoring

<p align="right">(<a href="#readme-top">back to top</a>)</p>

---

## 🙏 Acknowledgements <a name="acknowledgements"></a>

- **Dr. Spyros Giannelos** — Imperial College London for the real storage data.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

---

## 📝 License <a name="license"></a>

This project is [MIT](./LICENSE) licensed.

<p align="right">(<a href="#readme-top">back to top</a>)</p>