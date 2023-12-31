
# SpaceX Falcon9 First Stage Landing Prediction
![](https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMDeveloperSkillsNetwork-DS0701EN-SkillsNetwork/api/Images/landing_1.gif)

On its website, SpaceX promotes Falcon 9 rocket launches for $62M;
other suppliers charge upwards of $165M for each launch. A large
portion of the savings is due to SpaceX's ability to reuse the first stage. So, we want to determine the first stage landing to find the cost of a launch. The information from SpaceX can be used if an alternate company (SpaceY) wants to bid against SpaceX for a rocket launch Predicting the first stage of rockets successful landings, along with the ideal location for launches, is the best approach
to determine the entire cost of launches.

## API Reference

#### Get all items

```http
  GET /api.spacexdata.com/v4/cores/
```


#### Get item

```http
  GET /api.spacexdata.com/v4/${id}
```

| Parameter | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `name`      | `string` | **Required**. 'rockets', 'launchpads', or 'payloads' |

## Authors

- [@Adarsh Kumar](https://github.com/adarsh-k-tiwari/)


## Falcon 9 and Falcon Heavy Rockets

![](https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBM-DS0321EN-SkillsNetwork/labs/module_1_L2/images/Falcon9_rocket_family.svg)


## Tech Stack

**Languages:** Python, SQL

**Libraries:** pandas,  numpy, sk-learn, matplotlib, seaborn, Beautiful Soup, folium, plotly, dash


## Data Collection
Data Collection process involves a combination of API requests from SpaceX public API and web scrapping data from SpaceX Wikipedia page.

#### Data Collection from SpaceX API -
- Request the SpaceX launch data.
- Parse the SpaceX data.
- Convert the extarcted data to a dataframe.
- Filter the dataframe to include Falcon9 launches only.

#### Data Collection from SpaceX Wikipedia page -
- Request Falcon9 launch wikipedia page.
- Parse the wikipedia data using Beautiful Soup.
- Extract data from HTML table.
- Create a datafram by parsing the HTML tables.
## Code Structure
```

SpaceXPrediction/
├─ src/
│  ├─ jupyter-labs-eda-dataviz.ipynb.jupyterlite.ipynb
│  ├─ jupyter-labs-eda-sql-coursera_sqllite.ipynb
│  ├─ jupyter-labs-spacex-data-collection-api.ipynb
│  ├─ jupyter-labs-webscraping.ipynb
│  ├─ lab_jupyter_launch_site_location.jupyterlite.ipynb
│  ├─ labs-jupyter-spacex-data_wrangling_jupyterlite.jupyterlite.ipynb
│  ├─ spacex_dash_app.py
│  ├─ SpaceX_Machine_Learning_Prediction_Part_5.jupyterlite.ipynb
├─ Capstone Project SpaceY(1).pptx
├─ Capstone Project SpaceY-FInal.pdf
├─ README.md

```
## Presentation

[Presentation](https://github.com/adarsh-k-tiwari/IBMPracticeLab/blob/main/Capstone%20Project%20SpaceY-Final.pdf)


## Results and Evaluation

Here are some related projects

- All models had virtually the same accuracy on the test set at 83.33% accuracy.
- It should be noted that test size is small at only sample size of 18. This can cause large variance in accuracy results such as those in Decision Tree Classifier model in repeated runs. 
- We likely need more data to determine the best model.

SpaceY can use this model to predict with relatively high
accuracy whether a launch will have a successful Stage 1
landing before launch to determine whether the launch should
be made or not.
