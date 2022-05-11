# Deliverable 2: UFO Sightings

## Overview of Project:

Dana created a webpage and interactive table which shows data on UFO sightings. She'd like to expand her search criteria options to provide a more in-depth analysis of UFO sightings by allowing users to filter for multiple criteria at the same time. The filters included searching by date, city, state, country and shape.

## Results:

The app.js file starts out by importing the dataset from data.js and I went ahead and cleared out any existing data. Next I looped through each object in the data and appended a row and cells for each value in the row which was later filled by the values of each cell. 

The index.html file was used from my classwork which had all the constructs of the webpage which would display the data. I added the new syntax for the Filter Search table which would take the user's inputs for dates, city, state, country and UFO shape. 

Back on app.js, I created a variable to keep track of all the filters as an object. The function updateFilters() is used to update the filters. I then again saved the element, value and id of the filter that was changed as a variable. If the filter value was entered, I then added that filterID and value to the filters list. Otherwise the filter would be cleared from the filters object.

The function was afterwards called to apply all filters and rebuild the table. Function filterTable was used to filter the table when the data is entered. the filtered data was then set to tableData. Afterwards I used 
Object.entries(filters).forEach(([key, value]) = { 
filteredData=filteredData.filter(row=>row[key]===value);
});
to loop through all of the filters and keep any data that matches the filter values. Finally, the table was rebuilt using the filtered data. Also, an event to listen for changes to each filter was also attached. Finally the table will be built when the page loads. 

## Summary:

I found working on this assignment intriguing and it gave me a better understanding of JavaScript and HTML. One of the drawbacks was that I believe an average user would not realize that the site has the means to 'refresh' it's table. I would change two items on this webpage to make it more user-friendly. First I would change the location of the 'UFO Sightings' button to below the 'Filter Table' button as it it not very obvious to a user. Secondly I would make the button stand out more visually as a 'Refresh button' to help the user navigate the site better.


