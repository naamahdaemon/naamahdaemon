# naamahdaemon.github.io
Welcome to my GitHub ! 
No big project here, no AI, no quantic computing, only little code snippets mostly dedicated to my own use. 
I use the page hosted here on my web server to display various graphs taking `csv` files as input. 

# Display graph from a csv file
The simple html page hosted here allows to display simple graphs from CSV files.

An example is available on the github page of this project here : https://naamahdaemon.github.io

# Installation
Copy `stat.html`, `index.html` and your `csv` file to your web server. 

The `csv` file can count whatever data you want. It is up to you to generate and update the file so that your graph will be updated (in real time). 

> Example    
> I use this graph to monitor my Mina node server uptime.    
> A shell script parse logs ono my server to generate date,ticks `csv` file. (this script is available to download here : https://github.com/naamahdaemon/mina-node-uptime-moniroring-script)    
> This file is automatically uploaded to my web server each time it is updated    
> Then I can display my uptime graph from my web server.    

## `stat.html`
The `stat.html` file displays a single CSV file.

> Example    
> https://naamahdaemon.github.io/stat.html?source=uptime.csv&scale=1&label=TICKS&color=%233333FF

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
    * `0` to display brut data on the graph
    * `1` to scale the graph to 0 (he graph will display the difference between the values on a y-axis origin at 0.)

## `index.html`
The `index.html` page is a sample page displaying several graphs on the same page inside `iframe`
You can modify the page and use it as is or ignore this page and make your own.



