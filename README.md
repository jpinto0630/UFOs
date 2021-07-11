# UFOs

## Overview of Project 

The purpose of this project was to help Dana create and then refine a webapp that will allow users to search access a large data set of UFO sighting and search for specific UFO sightings based on certain criteria. 


## Results
All of the UFO sighting data is initially available for viewing. To further refine the search, follow the steps below: 

1. On the left side of the page, select the criteria you wish to filter by and type in the filter criteria. I.E: To search for UFO sightings that occurred in El Cajon, the user should input el cajon into the city field and press enter or click away from the search field. 

SS 1 

2. You may also further refine a search by inputting more than one criteria. I.E: To search for sightings with a triangle shape, that occurred in the us, and on 1/1/2010 the user would input the relevant search parameters. 

## Summary
One drawback this project has is that the filter criteria is searching for direct matches. This means that an unintended limitation is that the text case input into the search parameters must match that in the data set we are using. For example, if a user were to search for ‘El Cajon’ instead of ‘el cajon’ they would see no search results. 

A recommendation for this project would be to initially address the drawback mentioned above. This could be accomplished by having our search parameter not be as strict: 

```  Object.entries(filters).forEach(([key, value]) => {
     filterData = filterData.filter(row => row[key] === value);
     });
  ```

Could be changed to something like: 

```  Object.entries(filters).forEach(([key, value]) => {
     filterData = filterData.filter(row => row[key] == value);
     });
  ```

Additionally, Dana could look into incorporating two buttons ease of use buttons:

1.	A button that triggers the search mechanism. As it stands to trigger the search mechanism the user has to press enter or click away from the search field. 

2.	A second button to clear the search parameters. The user also has to manually clear each search parameter or click on the index link in order to reset the parameters. 

Github Page: https://jpinto0630.github.io/UFOs/ 

