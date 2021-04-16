# Trip planning - Prepare your next holiday!

## Overview and objectives

The aim of this project? To **find the best destinations and hotels for a last minute trip**!

No pre-existing dataset here, all data will be retrieved via **API requests** and **web scraping**.

## Adaptability

The angle of approach taken on this project is **purely personal**. Feel free to explore other countries, places, tracks and criteria!

Beyond that, this project is just one example of the enormous power of APIs and web scraping.

## Files and prerequisites

Apart from the **notebooks** (of which there are **three**, for reasons we will discuss later), you should not need any other items. 

The `destinations.csv` file and the **JSON files** in the `hotels_data` folder are just **examples** of the files generated during the project, which I have added in case you want to do only part of the project. **If you do the whole project, you won't need them**!

For one of the APIs (**OpenWeather**), you'll have to create (for free) an **API key**. You'll find the instructions to do so [here](https://openweathermap.org/appid).

## Required libraries

This project uses several libraries for data manipulation, namely **Pandas** (data manipulation), **Requests** (APIs calls), **Plotly** (data visualization), **os** (operating system interfaces), **Scrapy** (web scraping), **logging** (logging facility) and **glob** (Unix style pathname pattern expansion).

Depending on your execution environment, you might need to **install these modules**. As a reminder, you can do so using a `pip install name_of_the_library` command. Remember to add an exclamation mark at the beginning if you want to execute it directly in a notebook, as it is originally a terminal command.