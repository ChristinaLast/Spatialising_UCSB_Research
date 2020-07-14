# Spatialising_UCSB_Research

## Concept
As a researcher, how would you go about finding work similar to your own? Measures of similarity could include research done in similar regions of the world, research by similar departments and scholars, research with topical correspondence, or research that co-occurred at the same temporality, reflecting contextual change. Determining these measures of similarity from a digital text collection requires mining document metadata. This project experiments with mapping from non-spatial tabular meta-data to spatialisations.

Spatial information provides guidance for the ways in which people, places and topics can be meaningfully displayed and analysed. Spatialization embeds documents into a metaphorical space where documents in closer proximity can be perceived as similar. Different conceptualizations of similarity, such as geographic and topical, lend themselves to analysis through different spatializations with varying measures of distance. By spatializing information, researchers can compute on collections of research documents, asking questions like “Where in the world is the density of my domain’s research the highest?”, “Which domain is the most spatially diverse? or “What other research shares the same spatial neighborhood as my domain?”

## Preliminary ideas
The prevalence of globalisation has enabled researchers from all departments travel the world with great ease and share their findings within the university domain. For my final project, I want simultaneously display the geographic reach of departmental research published at UCSB, and develop a tool for the general public to interrogate Santa Barbara’s connection to other locations across the world. My strategy is inspired by the metaphor of global networks attributing cultures traditions and histories to different locales, and how researchers travel to investigate these cultural geographies and transfer those resources and knowledge to Santa Barbara. I aim to represent these flows of information from locations to UCSB within my visualisation.

## Process
For this assignment I am using the [Alexandra Digital Research Library](https://www.alexandria.ucsb.edu/) data. I scraped the ADRL UCSB Electronic Theses and Dissertations. To identify any locations specific to the thesis or dissertation I pushed the results through a geoparser which compared the word strings to individual place names in Gazeteers. The geoparsed results were read into R and geocoded using the following code which returns the latitude and longitude of the placename. I scraped the ADRL UCSB Electronic Theses and Dissertations (N=1731) for the corresponding fields; Title, Year, Author, Degree Grantor, Supervisor, Description, Language, and wrote to csv. To select and group by department I ran the following query. To identify any locations specific to the thesis or dissertation I pushed the results through a geoparser which compared the word strings to individual place names in Gazeteers. To do this I selected gazeteers at multiple levels of geography and parsed the strings through each, to extract place names from multiple place scales. The gazetteers downloaded were (GeoNames, ADL Gazetteer, U.S. Census, Wikipedia) to cover the potential range of current, historic and informal place names which may be included in the research titles and abstracts

## Final result
This interactive 3D data visualization examines the relationship between different departments at UCSB and the geographic nature of their research. The result situates scientific research at UCSB in more powerful ways than library shelves, supporting multiple paradigms of data discovery. More broadly, this project allows me to generate verbal, written, and visual communication methods, with a particular emphasis on framing relationships, visual storytelling, and information design. Such spatializations will convey how scientific research topics are related through similarity (by department type and proximity). Interactivity was introduced into this model, and each time a department is hovered over in the legend, only those links from that department are shown. This helps the user identify which departments are more ‘spatialised’ than others. As well as this, when the user has selected the department, the titles of the theses or dissertations associated with the geographic placements will be shown. Each of these items has a number in parenthesise provided, which reflects the number of places associated with that department or that thesis. As evident in the visualisation, some theses cover more than one location, which makes for rich geographical history of research at UCSB.
