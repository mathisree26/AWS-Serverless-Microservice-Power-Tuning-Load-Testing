# AWS Serverless Microservice Power Tuning and Load Testing

> Optimizing AWS Lambda performance and cost using power tuning and load testing — backed by the pillars of the **AWS Well-Architected Framework**.

---

## 📋 Overview

This project demonstrates how to design, power-tune, and load-test an AWS Serverless Microservice with different Lambda memory allocations to find the perfect balance between **performance** and **cost optimization**.

### What's Covered

- ✅ Serverless Microservice design with **API Gateway**, **Lambda**, and **DynamoDB**
- ✅ Lambda Power Tuning using the **AWS Lambda Power Tuning State Machine**
- ✅ Load testing with **Postman** to measure real-world performance metrics

---

## 🏗️ Architecture

The microservice follows a classic serverless pattern:

```
Client → API Gateway → Lambda Function → DynamoDB
```

| Component | Role |
|---|---|
| **Amazon API Gateway** | Exposes RESTful endpoints |
| **AWS Lambda** | Executes business logic |
| **Amazon DynamoDB** | Persistent NoSQL data store |

---

## ⚡ Lambda Power Tuning

Lambda memory was tested across multiple configurations using the [AWS Lambda Power Tuning](https://github.com/alexcasalboni/aws-lambda-power-tuning) state machine (`powerTuningStateMachine`).

### Memory Configurations Tested

| Memory Allocation | Tested |
|---|---|
| 128 MB | ✅ |
| 256 MB | ✅ |
| 512 MB | ✅ |
| 1024 MB | ✅ |

### Result

> **Optimal configuration: 512 MB**
>
> At 512 MB, the best balance between performance and cost efficiency was achieved. Going beyond this threshold yielded diminishing performance returns relative to the additional cost.

---

## 🔬 Load Testing with Postman

The microservice was load tested using Postman's collection runner to capture performance metrics across different memory configurations.

### 128 MB Memory — Results

- 📊 **Average response time**: Measured across test duration
- 📈 **Response time trend**: Observed throughout the load test window

### 1024 MB Memory — Results

- 📊 **Average response time**: Measured across test duration
- 📈 **Response time trend**: Observed throughout the load test window

Load testing is **repeatable**, making it straightforward to re-run benchmarks whenever the function code or infrastructure changes.

---

## ✅ Conclusion

This project validates architectural decisions with **empirical testing evidence**:

- AWS Lambda Power Tuning provides clear data on the cost/performance curve across memory configurations.
- Postman load testing gives repeatable, measurable performance benchmarks.
- The combination of both approaches enables confident, data-driven infrastructure decisions aligned with the **AWS Well-Architected Framework**.

---

## 🛠️ Tools & Services

- [AWS Lambda](https://aws.amazon.com/lambda/)
- [Amazon API Gateway](https://aws.amazon.com/api-gateway/)
- [Amazon DynamoDB](https://aws.amazon.com/dynamodb/)
- [AWS Lambda Power Tuning](https://github.com/alexcasalboni/aws-lambda-power-tuning) (serverless app via AWS SAR)
- [Postman](https://www.postman.com/) — Load Testing

---

## 👤 Author

**Mathi Munikrishnan** — Strategic Solution Architect

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue?logo=linkedin)](https://www.linkedin.com/in/mathimunikrishnan)
