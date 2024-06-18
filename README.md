# Sea Route Optimization

## Overview
The Sea Route Optimization program is designed to help find the optimal sea route between two points using a series of specialized tools and agents. This program processes a query containing start and end coordinates, extracts these coordinates, and then employs various tools to determine the best route, considering multiple factors such as distance, weather, and fuel requirements.

## Workflow
1. **Input Query**: The program accepts a query with the start and end coordinates for the desired sea route.
2. **Coordinate Extraction**: CrewAI agents extract the coordinates from the input query.
3. **Route Calculation**:
   - **Dijkstra Tool**: This tool calculates the shortest path based on the provided coordinates and existing data. Due to the data being incomplete, there might be errors in the route found.
4. **Weather Analysis**:
   - **Weather Checker**: Utilizes the Open Meteo API to fetch weather data for the coordinates along the route.
5. **Fuel Estimation**:
   - **Fuel Estimator**: Provides an estimate of the fuel requirements and costs based on the route calculated by the Dijkstra tool.
6. **Data Visualization**:
   - **Data Visualizer**: Creates graphs, plots, and other visual representations of the route, weather conditions, and fuel estimates. Note: Graph generation may be challenging due to the complexity and scale of the data.

## Known Issues
- **Data Incompleteness**: The route found by the Dijkstra tool may have errors due to incomplete data. I am only using the marnet_plus_100km file, there are 4 more but due to the size the program kept halting.
- **Execution Time**: The large size of the data being processed can result in long execution times. In some cases, the execution might need to be stopped if it takes too long.

## Notes
- The last execution was halted due to excessive processing time, which indicates the need for optimization or more efficient handling of large datasets.
- While the data from the Eurostat Marnet folder is comprehensive, its complexity can pose challenges for graph generation.

## Future Improvements
- **Data Optimization**: Work on improving the completeness and accuracy of the data used by the Dijkstra tool.
- **Performance Enhancements**: Optimize the code to handle large datasets more efficiently and reduce execution times.
- **Error Handling**: Implement better error handling mechanisms to manage issues arising from incomplete data.

## Getting Started
To use this program, follow these steps:
1. Input the start and end coordinates for the desired sea route. (for now it has been hardcoded)
2. Allow the CrewAI agents to process the coordinates through the series of tools.
3. Review the generated route, weather data, fuel estimates, and visualizations.

For data from the Eurostat Marnet folder, visit [Eurostat Sea Route GitHub](https://github.com/eurostat/searoute/tree/master/modules/marnet).
