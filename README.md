AI-Powered Business Intelligence Chatbot for Structured Enterprise Data
Overview

This project demonstrates an AI-powered Business Intelligence (BI) system that allows users to ask questions in natural language and receive accurate, data-backed insights from structured enterprise data stored on-premise.

The system is designed to enhance data accessibility without compromising correctness, traceability, or reproducibility. AI is used strictly as an interface and explanation layer, while all computations are performed on structured databases.

Problem Statement

Traditional BI systems require users to:

Understand dashboards

Write SQL queries

Rely on analysts for ad-hoc questions

This project enables users to ask questions such as:

What is the total revenue of the Fintech domain in 2020?

What profit did Paytm make in 2021?

The system retrieves the correct data from structured sources and presents results in clear, natural language.

System Architecture

The system follows a question → data → explanation flow:

User asks a question in natural language

System identifies intent and entities

A structured query is generated

Data is fetched from the database

Results are passed to an LLM for explanation

Final answer and insights are returned

Architecture Diagram (Logical)
User
 ↓
Chat Interface
 ↓
Entity Recognition and Intent Classification
 ↓
Query Builder
 ↓
Structured Database (SQL / MongoDB)
 ↓
Validated Query Results
 ↓
LLM Explanation and Insight Layer
 ↓
Final Answer to User

Key Components
1. Entity Recognition

Identifies key entities such as:

Company names

Domains

Metrics (revenue, profit)

Time periods

2. Intent Classification

Determines whether the user wants:

A lookup

An aggregation

A comparison

3. Query Builder

Converts validated intent and entities into safe, structured database queries.

4. Data Retrieval Layer

Fetches exact results from indexed tables or collections.

5. LLM Explanation Layer

Transforms structured outputs into readable answers and insights.

Tools and Technologies

Database: SQL / MongoDB (indexed, aggregated data)

Backend: Python

NLP: Entity extraction and intent classification

LLM: Used only for explanation (RAG-assisted)

APIs: REST-based service layer

Example Queries
Question	System Action
Revenue of Paytm in 2021	Lookup
Total revenue of Fintech in 2020	Aggregation
Companies in Healthcare domain	List
Design Principles

Structured data is the source of truth

AI never performs calculations

Every answer is traceable to data

Explanations are clearly separated from inference

Outcome

Improved accessibility to business data

Reduced dependency on analysts

Maintained accuracy and trust

Conclusion

This project demonstrates how AI can be responsibly integrated into BI systems as an interface layer, while preserving scientific rigor, business correctness, and data trust.
