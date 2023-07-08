# naamahdaemon.github.io
Naamah GitHub Homepage

Welcome to my GitHub !
No big project here, no IA, no quantic computing, only little code snippets mostly dedicated to my own use.

# Display graph from a csv file
The simple html page hosted here allows to display simple graphs from CSV files.

An example is available on the github page of this project here : https://naamahdaemon.github.io

# Installation
Copy `stat.html`, `index.html` and your `csv` file to your web server.

## `stat.html`
The `stat.html` file displays a single CSV file.
It takes the following parameters in the querystring :

* `source`
    source csv file to display graph from. Format of the csv file should be :
    ```
    Time, Score
    YYYY-MM-DD HH:MM:SS, <SCORE>
    ```

    > Example

        ```
        Time,Score
        2023-05-01 00:00:00,91
        2023-05-02 00:00:00,96
        2023-05-03 00:00:00,96
        ```
 
* `color`
    HTML color code (#XXXXXX) of the graph line.

* `label`
    Label of the graph

* `scale`
    * `0` to display brute data on the graph
    * `1` to scale the graph to 0 (he graph will display the difference between the values on a y-axis origin at 0.)

    > Example    
    `stat.html?source=uptime.csv&scale=1&label=test&color=%23FF0000`
