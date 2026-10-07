# London Pollution Prediction using Graph Neural Networks

**[View the full analysis](https://sammigrewal.github.io/Network-Analysis-Project/London_GNN_Project.html)**

## Context
This project aims to predict PM2.5 concentrations for each output area in London using socio-economic characteristics and spatial relationships modeled as a graph.

## Main Methods
1. **Exploratory Data Analysis**: Analyzed socio-economic variables (demographics, housing, employment) and PM2.5 pollution levels across London output areas. Visualized spatial distribution and summary statistics.

2. **Graph Construction**: Built an adjacency graph using Queen contiguity to represent spatial relationships between touching output areas, ensuring corner neighbors are included.

3. **GNN Model Building**: Implemented a GraphSAGE model with two layers to capture neighborhood structure and relationships.

## Key Outcomes
- **Model Fit**: GraphSAGE is compared to a Linear Regression model, the GNN outperforms linear model. The GNN offers greater explanatory power than a linear model, improving the R² by 7.2%, and reducing the RMSE by 11.4% compared to the linear model.

## Improvements
- However, the GraphSAGE model is not perfect. Both models underpredict pollution along major roads, suggesting the next step is to add London's road network to the graph, so areas linked by a main road are treated as neighbours.
