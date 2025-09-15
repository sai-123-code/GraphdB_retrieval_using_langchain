# LangChain-GraphDB-Movie-Query-System

A smart system using **LangChain**, **GraphDB (Neo4j)**, and a language model to answer natural language questions about movies from a graph database.

## Overview
This project combines LangChain with GraphDB to create a retrieval system for movie data. Users ask questions in plain English, like "Which movies were directed by Christopher Nolan?" The language model generates a Cypher query, runs it on the database, and formats the results into a clear response.

Key components:
- **Language Model (LM)**: Processes questions and creates Cypher queries.
- **GraphDB**: Stores movie data (movies, actors, directors) as a graph.
- **LangChain**: Connects the LM and GraphDB.

This setup makes querying easy without learning database languages. It's based on a movie dataset but can extend to other fields like healthcare or finance.

## Why Use GraphDB?
Graph databases like Neo4j are ideal for this project because:
- They excel at handling complex relationships, such as connections between movies, directors, actors, and genres, which are naturally modeled as nodes and edges.
- Queries involving traversals (e.g., finding co-actors or similar movies) are faster and more efficient than in relational databases, avoiding costly joins.
- Cypher, the query language, is intuitive for expressing graph patterns, making it easier for the language model to generate accurate queries.
- They offer flexibility for evolving data schemas without rigid tables, perfect for semi-structured datasets like movies.
- Overall, GraphDB enables deeper insights into connected data, improving the accuracy and speed of natural language queries in domains with rich relationships.

## Features
- Natural language questions about movies.
- Auto-generated Cypher queries.
- Structured data retrieval from Neo4j.
- Friendly, formatted answers.
- Adaptable to other domains.

## Relations stored in Neo4j GraphdB
1) Explains how movie generes and titles are related
<img width="2302" height="1137" alt="visualisation (1)" src="https://github.com/user-attachments/assets/0f4279e1-1114-4c5c-9adc-9a7f29208e8d" />
2) Explains which directors directed which movies
<img width="2302" height="1137" alt="visualisation" src="https://github.com/user-attachments/assets/9bf3fef2-4ae0-4f94-9c36-4441bd547c1e" />
