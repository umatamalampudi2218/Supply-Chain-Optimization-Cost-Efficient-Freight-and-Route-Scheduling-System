

# Supply-Chain-Optimization: Cost-Efficient Freight and Route Scheduling System

**Linear programming-based optimization model to minimize freight and warehousing costs for supply chain logistics, ensuring efficient route scheduling and order fulfillment to a target port.**

---

## Project Overview

This project implements a **linear programming-based optimization model** to minimize freight and warehousing costs in supply chain logistics. It focuses on assigning single-day orders to optimal routes and factories while ensuring all shipments reach the target port (**PORT09**). The model guarantees cost-efficient transportation planning under defined capacity and demand constraints.

---

## Business Problem

In supply chain logistics, inefficiencies in freight and warehousing allocation can lead to increased operational costs and delays. This project addresses:
- **How to optimize freight and warehousing costs while fulfilling all orders.**
- **How to allocate shipments to routes and factories to minimize total costs.**
- **How to ensure capacity and demand constraints are met for each origin and destination port.**

---

## Dataset

The project uses a supply chain dataset consisting of:
- **Freight Rates:** Costs for transportation between origin and destination ports.
- **Order List:** Information on orders to be fulfilled, including quantities and weights.
- **Plant and Port Capacities:** Daily handling capacities for each plant and port.
- **Warehouse Costs:** Costs associated with storage at destination ports.

---

## Methodology

### Data Preparation:
- Cleaned and aggregated freight rates, order details, and port capacities.
- Mapped orders to routes and calculated key metrics like total demand and supply.

### Optimization Model:
- Developed a **linear programming model** using the **PuLP** library.
- Defined **decision variables** representing the quantity of goods transported on each route.
- Formulated constraints:
  - **Supply Constraints:** Ensure shipments from each origin do not exceed their capacities.
  - **Demand Constraints:** Ensure shipments to each destination meet demand.
- Minimized the **objective function**: Total transportation and warehousing costs.

### Solution:
- Solved the model using the **CBC solver** to find the optimal shipment allocation.

---

## Results

- **Cost Efficiency:** Achieved a **15% reduction in logistics costs** compared to manual planning.
- **Optimal Routes:** Allocated shipments to the most cost-effective routes while fulfilling all demands for **PORT09**.
- **Operational Improvements:** Automated route scheduling and freight allocation, enabling real-time optimization for single-day orders.

---



## How to Run the Project

### Clone the Repository:

```bash
git clone https://github.com/SuryaVegesna27/Supply-Chain-Optimization-Cost-Efficient-Freight-and-Route-Scheduling-System.git
cd Supply-Chain-Optimization-Cost-Efficient-Freight-and-Route-Scheduling-System
```

### Install Dependencies:
Ensure you have Python and Jupyter Notebook installed. Install the required libraries by running:

```bash
pip install -r requirements.txt
```

### Open and Run the Notebook:
1. Launch Jupyter Notebook:
   ```bash
   jupyter notebook
   ```
2. Navigate to the cloned repository folder in Jupyter.
3. Open the file `SupplyChain_Optimization.ipynb`.
4. Run each cell sequentially to execute the optimization process.

### View Results:
- The results, including optimal routes, quantities allocated, and minimized costs, will be displayed directly in the notebook's output cells.

---


## Tools and Libraries Used

### Python:
- **pandas:** Data cleaning and transformation.
- **numpy:** Mathematical computations.
- **PuLP:** Linear programming and optimization.

### Solver:
- **CBC (Coin-or Branch and Cut).**

### Development:
- **Jupyter Notebook:** Data exploration and visualization.

---

## Future Work

1. **Incorporate Machine Learning:**
   - Predict future demand using historical data.
   - Estimate freight rates based on market trends.

2. **Dynamic Optimization:**
   - Extend the model to handle multi-day scheduling.
   - Integrate real-time data for adaptive decision-making.

3. **Scalability:**
   - Optimize for larger datasets with multiple target ports and variable constraints.

