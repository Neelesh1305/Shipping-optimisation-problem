## Shipping Optimisation problem

#### Idea 
The goal of this project is to find an optimized route that starts and ends at the same location, covering a specified number of geographical points along the way. This type of problem is commonly known as the Traveling Salesman Problem (TSP) and has numerous applications in logistics, route planning, and transportation.

#### Program/Algorithm used
We leveraged the OpenStreetMap (OSM) API to gather geographical data for the points of interest. OSM provides detailed maps and location data that are essential for plotting routes and calculating distances between points.

To explore all possible paths that the route could take, we implemented a recursive Depth-First Search (DFS) algorithm. This algorithm systematically traverses all possible routes from the starting point, visiting each point exactly once before returning to the start. This exhaustive search is necessary to ensure that the optimal route is identified.

Using the data obtained from the OSM API, we constructed a Distance Matrix. This matrix represents the pairwise distances between all points in the route, serving as the foundation for route optimization. Each entry in the matrix indicates the distance from one point to another, allowing the algorithm to compute the total distance for any given path.
We utilized Graphframes to represent the route as a graph, with vertices corresponding to the points of interest and edges representing the possible paths between them. Graphframes, a graph processing library in Apache Spark, enabled us to efficiently manage and manipulate large datasets. It also facilitated the identification of edges and vertices, which are crucial for the optimization process.

#### Result/conclusion:
This project successfully demonstrates the use of advanced algorithms and data processing techniques to solve the Traveling Salesman Problem. By integrating the OpenStreetMap API, recursive DFS, Distance Matrix calculations, and Graphframes, we developed a robust solution for finding optimized routes that start and end at the same point, covering a specified number of geographical points efficiently.
![WhatsApp Image 2023-05-15 at 11 57 33](https://github.com/Neelesh1305/Shipping-optimisation-problem/assets/113800036/22608988-6102-49b8-9b4a-1f3df36687c0)

#### Guide steps:
Clone the project repository from [repository URL] or download the project files. Open a terminal or command prompt and navigate to the project directory.
Ensure that all the required Python libraries are installed by running the following command:
pip install -r requirements.txt
If you plan to use Google Colab or a Jupyter Notebook, upload the project files to the respective environment.
Ensure you have the following data files in the project directory:
uscities.csv: Contains city data for the required cities. If necessary, update the file paths in the project code to match the location of the data files on your system.
Execute the project code in the desired Python environment (e.g., IDE, command prompt, Google Colab, Jupyter Notebook). Run each section of the code sequentially, as indicated by comments or markdown headings.
The code will generate outputs such as distance matrices, visualizations, and optimized routes.

