# Toronto Housing Analysis from 2001 to 2016

## Usage

You must have Anaconda and Jupyter Lab installed and be running Python >= 3.7 to run this dashboard.

1. Set up a new Anaconda environment called `pyvizenv`.

    ```python
    conda update anaconda
    conda create -n pyvizenv python=3.7 anaconda -y
    conda activate pyvizenv
    ```

2. Install environment dependencies.
    ```python
    pip install python-dotenv
    pip install numpy==1.19
    pip install matplotlib==3.0.3

    conda install -c conda-forge nodejs=12 -y
    conda install -c pyviz holoviz -y
    conda install -c plotly plotly -y
    conda install -c conda-forge jupyterlab=2.2 -y
    ```

3. Install the Jupyter Lab extensions.

    ```python
    jupyter labextension install @jupyter-widgets/jupyterlab-manager --no-build
    jupyter labextension install jupyterlab-plotly --no-build
    jupyter labextension install plotlywidget --no-build
    jupyter labextension install @pyviz/jupyterlab_pyviz --no-build
    ```

4. Build the Extensions.

    ```python
    jupyter lab build
    ```

5. Ensure the successful installation of the dependencies by finding them in Anaconda.

    ```python
    conda list nodejs
    conda list holoviz
    conda list hvplot
    conda list panel
    conda list plotly
    ```

6. You will need a MapBox API key to get map data. If you don't have a MapBox API key, here are [instructions](https://medium.com/technology-hits/working-with-maps-in-python-with-mapbox-and-plotly-6f454522ccdd) on how to get one and set it up as an environment variable.

7. Run all cells in Jupyter and view the dashboard in the browser by executing the final cell `dashboard.servable()`.

<br>

## Results

### Average House Values in Toronto Overall

Use the map plot to get a birdseye view of the cost of Toronto neighbourhoods. The larger and brighter the dot, the more expensive the neighbourhood. This plot indicates that the most expensive neighbourhoods are near the downtown area.

![mapbox](./images/mapbox.png)

### Dwelling Type Units per Year

The sum number of dwelling type units per year. The bar heights change as the years go on, indicating which dwelling types gained or lost popularity.

![bar_chart_1-4](./images/bar_chart_1-4.png)

<br>

### Average Shelter Costs in Toronto Per Year

Comparing the cost of owning a dwelling versus renting one. Notice that although owning a house has been more expensive, the value of houses over doubled.

![line_chart_1](./images/linechart_1-3.png)

<br>

### Neighbourhood Analysis

Use the dropdown menus to look at data for individual neighbourhoods. The data varies widely between each neighbourhood.

![line_chart_4](./images/line_chart_4.png)

![multi_bar_chart](./images/multi_bar_chart.png)

<br>

### Average House Values in Toronto by Neighbourhood

The average house value in each neighbourhood within each time period. Hover over the bars to view more info.

![row_facet](./images/row_facet.png)

<br>

### Top 10 Expensive Neighbourhoods Overall

The top 10 expensive neigbourhoods to live in overall between 2001 and 2016.

![bar_chart_5](./images/bar_chart_5.png)

<br>

### Top 10 Expensive Neighbourhoods by Year

This sunburst chart displays the top 10 expensive neighbourhoods to live in between 2001 and 2016. Darker colours indicate higher value.

![sunburst](./images/sunburst.png)
