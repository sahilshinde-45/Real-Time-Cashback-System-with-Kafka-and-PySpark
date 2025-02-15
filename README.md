# Real-Time-Cashback-System-with-Kafka-and-PySpark
Overview

    This real-time cashback system leverages Apache Kafka and PySpark to process transactions and apply cashback rules dynamically. It ensures efficient, low-latency processing of streaming transaction data, enabling instant cashback 
    calculations.


Technology Stack

    Apache Kafka – Handles real-time transaction streaming.
    PySpark (Apache Spark Streaming) – Processes and filters transactions based on cashback conditions.
    Docker – Manages scalable deployment of services.
    PostgreSQL / Redis (Optional) – Stores transaction and cashback records for auditing.
Cashback Conditions

    A transaction qualifies for cashback if it meets all of the following conditions:
    ✅ Minimum Amount: $15
    ✅ Store: Merchant X
    ✅ Date: Friday
    Cashback Reward
    💰 Cashback: 10% of the transaction amount
How It Works

    Transaction Stream Ingestion
    Transactions are published to a Kafka topic (transactions) in real-time.
    PySpark Stream Processing
    Reads transaction events from Kafka.
    Filters transactions based on cashback conditions.
    Computes 10% cashback for valid transactions.
    Cashback Notification & Storage
    Cashback details are published to a Kafka topic (cashback_events).
    Processed transactions are stored in a database for tracking.
    Users receive real-time notifications about cashback earnings.
Architecture Flow

    1️⃣ User makes a transaction → 2️⃣ Transaction sent to Kafka (transactions topic) → 3️⃣ PySpark processes transactions → 4️⃣ Valid transactions trigger cashback calculation → 5️⃣ Cashback is published to cashback_events topic → 6️⃣ Cashback credited & notification sent to the user
Scalability & Performance

    Kafka ensures real-time data streaming and fault tolerance.
    PySpark enables distributed processing for high throughput.
    Can scale horizontally by increasing Kafka partitions and Spark worker nodes.
    
# This system provides a fast, scalable, and fault-tolerant cashback solution, ensuring seamless reward distribution for eligible transactions in real-time. 🚀
