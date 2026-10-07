# London Pollution Prediction using Graph Neural Networks

## Context
This project aims to predict PM2.5 concentrations for each output area in London using socio-economic characteristics and spatial relationships modeled as a graph.

The analysis is viewed in the 'London_GNN_Project.html' file.

## Main Methods
1. **Exploratory Data Analysis**: Analyzed socio-economic variables (demographics, housing, employment) and PM2.5 pollution levels across London output areas. Visualized spatial distribution and summary statistics.

2. **Graph Construction**: Built an adjacency graph using Queen contiguity to represent spatial relationships between touching output areas, ensuring corner neighbors are included.

3. **GNN Model Building**: Implemented a GraphSAGE model with two layers to capture neighborhood structure and relationships.

## Key Outcomes
- **Model Fit**: GraphSAGE is compared to a Linear Regression model, the GNN outperforms linear model significantly. However, the GraphSAGE model is not perfect, reccommendations for improvement are given.
