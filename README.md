# MetaMask Performance Dashboard - A Blockchain Analytics Project

The MetaMask Performance Dashboard is a web app that displays various performance metrics related to MetaMask, such as revenue, trading volume, trades, unique users, and quarter-over-quarter (QoQ) growth. The dashboard is powered by the Streamlit library, Plotly for visualization, and uses BigQuery to query the blockchain data from the bigquery-public-data:crypto_ethereum dataset.

![] (https://github.com/roswin420/Metamask-Performance-Dashboard/blob/main/demo.gif)

## Table of Contents

- [Features](#features)
- [Tech Stack](#tech-stack)
- [Dataset](#dataset)
- [Installation](#installation)
- [Usage](#usage)

## What is Metamask?
-MetaMask is a popular browser extension and mobile app that allows users to access decentralized applications (dApps) on the Ethereum blockchain. It serves as a cryptocurrency wallet, allowing users to securely store, send, and receive Ether and other ERC-20 tokens.

## Features

The dashboard is divided into four sections:

1. **Overview**
    - Total Wallet Balance in USD
    - Individual Wallet Balances of:
        - MetaMask-Fees
        - DS-Proxy-Multisig
    - Daily, Weekly, Monthly Unique Users
    - Daily, Weekly, Monthly Trading Volume
    - Top 10 Traders by Volume
    - Top 10 Traders by Swaps

2. **Swap Metrics**
    - Daily Volume & Cumulative Volume
    - Daily Revenue & Cumulative Revenue
    - Daily Swaps & Cumulative Swaps
    - New Traders vs. Returning Traders

3. **DEX Analogy**
    - Top 5 DEX Traded Volume Comparison
    - Top 5 DEX Users Comparison

4. **Quarterly Performance**
    - QoQ Revenue
    - QoQ Active Users
    - QoQ Volumes
    - QoQ Swaps

## Tech Stack

- Dataset: bigquery-public-data.crypto_ethereum (Dataset contains all Ethereum Blockchain Transactions, which is updated in real-time)
- BigQuery & SQL are used to query the Dataset and derive various KPIs
- Plotly Library is used for Data Visualization
- Streamlit is used to construct the Web-App Dashboard

## Dataset

The dataset used in this project is obtained from Google BigQuery's bigquery-public-data:crypto_ethereum dataset, which contains all Ethereum Blockchain transactions. The dataset is updated in real-time and provides comprehensive data to analyze MetaMask's performance.

Tables used:

- *Transactions table* lists all transactions initiated by externally owned accounts (e.g., accounts on MetaMask), irrespective of who initiated the transaction — the receiver or the sender.
- *Traces table* (Internal Transactions) lists all transactions initiated by internal accounts (i.e., smart contracts).
- *Token Transfer* table lists all ERC-20 token transfers.

Addresses Used:

- Swap Router, MetaMask: 0x881d40237659c251811cec9c364ef91dc08d300c
- Smart Contract, MetaMask: 0x74de5d4fcbf63e00296fd95d33236b9794016631
- Fees, MetaMask: 0x11ededebf63bef0ea2d2d071bdf88f71543ec6fb
- DS Proxy, MetaMask: 0xf326e4de8f66a0bdc0970b79e0924e33c79f1915

## Installation

1. Clone the repository:
```!git clone https://github.com/yourusername/metamask-performance-dashboard.git```


2. Change the working directory:
```%cd metamask-performance-dashboard```

3. Install the requirements:
```!pip install -r requirements.txt```

## Usage
1. Run the Streamlit app:
```!streamlit run app.py```


