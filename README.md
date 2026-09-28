DABA Day 3 – Supply Chain Delay and Contract Compliance Analysis
Project Title

Connect Delay Predictions with Relevant Contract Information

Overview

This project is part of DABA (Data Analytics and Business Analytics) – Day 3.

The objective of this task is to connect the supply-chain shipment delay information developed in Day 2 with relevant vendor contract information.

The system combines shipment data, vendor details, contract conditions, delivery performance, and penalty clauses to identify contract compliance and risk.

Objective

The main objectives of Day 3 are:

Connect shipment delay data with vendor information.
Match each vendor with the relevant contract details.
Compare actual delivery time with contract delivery time.
Identify contract delivery violations.
Check whether delay penalties are applicable.
Classify contract risk.
Generate a combined contract-compliance dataset.
Visualize delay and contract-related information.
Dataset

The project uses the same 500-row shipment dataset from Day 2.

The dataset contains:

Shipment ID
Vendor
Origin
Destination
Shipping Mode
Distance
Weather
Traffic
Planned Delivery Days
Actual Delivery Days
Delay Days
Delayed Status

Vendor contract information is connected using the Vendor column.

Contract Information

The contract dataset contains:

Vendor
Contract Delivery Days
Delay Notification Hours
Penalty for Delay
Payment Period
Termination Notice Period
Workflow
Day 2 Shipment Dataset
        ↓
Shipment Delay Information
        ↓
Vendor Identification
        ↓
Vendor Contract Information
        ↓
Contract Matching
        ↓
Delivery Compliance Check
        ↓
Penalty Applicability Check
        ↓
Contract Risk Classification
        ↓
Visualization
        ↓
Final Analysis
Methodology
1. Load Shipment Data

The same shipment dataset created during Day 2 is loaded into the Day 3 notebook.

2. Create Contract Information

Contract information is created for the vendors available in the shipment dataset.

3. Match Shipment and Contract

The Vendor column is used as the common key to connect shipment records with vendor contract information.

4. Check Delivery Compliance

Actual delivery days are compared with the contractually specified delivery period.

Actual Delivery Days <= Contract Delivery Days
                    ↓
                Compliant

Actual Delivery Days > Contract Delivery Days
                    ↓
                Violation
5. Check Penalty Applicability

When a shipment is delayed and the corresponding contract contains a delay penalty clause, the system marks the penalty as applicable.

6. Calculate Contract Risk

The project classifies each shipment into:

Low Risk
Medium Risk
High Risk

The classification is based on delivery compliance and penalty applicability.

Technologies Used
Python
Google Colab
Pandas
Matplotlib
CSV
Data Analytics
Project Files
DABA-Day-3-Supply-Chain-Contract-Analysis/
│
├── README.md
├── day3_supply_chain_contract_analysis.ipynb
├── day3_delay_contract_analysis.csv
│
└── outputs/
    ├── contract_risk_distribution.png
    ├── vendor_delay_analysis.png
    ├── delivery_compliance.png
    └── actual_vs_contract_delivery.png
Key Output

The final analysis connects:

Shipment
   ↓
Vendor
   ↓
Delay Information
   ↓
Contract Information
   ↓
Compliance Status
   ↓
Penalty Status
   ↓
Contract Risk
Visualizations

The project includes visualizations for:

Contract Risk Distribution
Total Delay Days by Vendor
Delivery Contract Compliance
Actual Delivery vs Contract Delivery Time
Conclusion

The Day 3 implementation successfully connects supply-chain delay information with relevant vendor contract information.

By combining shipment performance and contract conditions, the analysis provides a structured way to identify delivery violations, determine penalty applicability, and classify contract-related risks.

This forms the contract-compliance component of the larger Supply Chain Delay Prediction and Vendor Evaluation project.

