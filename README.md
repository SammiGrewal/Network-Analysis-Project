# London Pollution Prediction using Graph Neural Networks

## Context
This project aims to predict PM2.5 concentrations for each output area in London using socio-economic characteristics and spatial relationships modeled as a graph.

The analysis is viewed in the 'London_GNN_Project.html' file.

## Main Methods
1. **Exploratory Data Analysis**: Analyzed socio-economic variables (demographics, housing, employment) and PM2.5 pollution levels across London output areas. Visualized spatial distribution and summary statistics.

2. **Graph Construction**: Built an adjacency graph using Queen contiguity to represent spatial relationships between touching output areas, ensuring corner neighbors are included.

3. **GNN Model Building**: Implemented a GraphSAGE model with two layers to capture neighborhood structure and relationships.

## Key Outcomes
- **Model Fit**: GraphSAGE is compared to a Linear Regression model, the GNN outperforms linear model significantly. The GNN offers greater explanatory power than a linear model, improving the R<\sup>2<\sup> by 7.2%, and reducing the RMSE by 11.4% compared to the linear model.

## Improvements
- However, the GraphSAGE model is not perfect. Like the linear model, the GNN model underestimates pollution along key transport networks throughout London. Pollution along key arterial roads, such as from Central London to the west and the semi-circular path in North London (see residuals graph), is underpredicted by both models. This is because the model does not take road and traffic networks into account. Therefore, the GraphSAGE model is likely to benefit significantly by incorporating data on transport networks as part of graph structure.
- Incorporating key transport networks into the GNN model can also allow for the links between output areas that are connected by transport networks to be included rather than just the nearest neighbours. For example, two output areas that do not share a boundary, but are connected by a main road or a rail line could be classed as neighbours if the transport network was accounted for. This could help increase the performance of the GraphSAGE model.
