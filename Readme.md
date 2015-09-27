# Developing data products project
The following repo contained the supporting files and documentation for a simple shiny app.

The app is based on the data set: https://archive.ics.uci.edu/ml/datasets/Auto+MPG. 
The app allows the user to input specifics about their vehicle and obtain an estimated MPG 
based on a GLM prediction algorithm generated from the original data set. 
Users can pick their vehicle attributes. 
Once they hit submit, the app returns their vehicles predicted MPG. 

The repo inludes the following additional files:
    
1. ui.R used to generate the shiny app
2. server.R second file needed to generate the shiny app
3. Index.rmd is the Markdown file that generates the R Presenter presentation describing the shiny app
4. Index.html is a HTML compiled from the .md file, and generates the presentation hosted on 
RPubs: http://rpubs.com/rosthia/113816
