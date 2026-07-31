<p align="center">
  <img src="https://github.com/EzequielFriasGomez/E-Commerce-Supply-Chain-Logistics-Bottleneck-Analysis/blob/main/An%C3%A1lisis_Log%C3%ADstica_Transporte.jpg" width="800"/>
</p>

# Architecture & Process (ETL & BI)

**PostgreSQL (SQL):** Developed a data engineering pipeline to extract, clean, and normalize database records, isolating precise first-half (H1) 2017 and 2018 metrics to ensure a symmetrical year-over-year comparison. Delivery lead times and delay rates were calculated directly within the SQL engine to optimize data model performance.

**Microsoft Power BI:** Imported the cleaned data model to dynamically calculate financial metrics (freight investment) using DAX expressions. Designed interactive heatmaps and applied volume filters (minimum of 300 orders) to isolate logistics anomalies while eliminating statistical noise from low-demand shipping routes.

# Business Diagnosis (What the Data Reveals)

The dashboard analysis uncovered critical vulnerabilities in the supply chain during the company's expansion:

**Scale Outpacing Infrastructure:** Order volume surged from **20,000** to **53,000** transactions. However, the logistics infrastructure was not prepared to sustain such rapid growth. As a result, the nationwide delivery delay rate more than doubled, increasing from **4.32%** to **8.75%**.

**Capital Leakage in Transportation:** Freight spending grew exponentially, rising from **$388K** to **$1.073M**. Despite nearly tripling transportation investment, the late delivery rate still doubled. This indicates that additional logistics spending was absorbed by an underperforming transportation network, ultimately contributing to a decline in the average customer review score (**3.99**).

**The Main Distribution Hub Bottleneck:** After applying a statistical threshold of **300 minimum orders** to eliminate low-volume routes, the analysis revealed that the **six highest-volume routes with the greatest performance deterioration all originated from São Paulo (SP)**. For example, the **SP → MA** route experienced a dramatic increase in delays, climbing from **2.6%** to **21.2%**.

**The Northern Logistics Black Hole (Bahia):** The analysis demonstrates that the issue extends beyond sales volume and stems from operational failures. Destinations such as **Bahia (BA)** experienced a systemic logistics breakdown; regardless of the shipment origin (**PR, MG, RJ, or SP**), delivery delays consistently exceeded **15%** throughout 2018.

# Strategic Recommendations

**Carrier & Last-Mile Logistics Audit:** Launch an immediate investigation into the transportation fleets operating outbound shipments from the **São Paulo (SP)** distribution center, as well as last-mile delivery operations in **Bahia (BA), Rio de Janeiro (RJ), and Paraná (PR)**. Since the analysis confirms that the issue is operational rather than demand-driven, the root causes of these logistics delays should be identified and addressed.

**Contract Renegotiation & Carrier Diversification:** Suspend exclusive route allocation agreements with current transportation providers across the **SP, RJ, and RS** corridors. Initiate a competitive bidding process to onboard new logistics partners in these regions, requiring stricter **Service Level Agreements (SLAs)** to reduce capital waste caused by inefficient freight operations.

---

**Tech Stack:** PostgreSQL (SQL) | Microsoft Power BI (DAX)
