---
layout: default
group: pattern
subgroup: Displaying and Dealing with Data
title: Magento Admin Pattern Library
menu_title: Filters
menu_order: 1
menu_node:
github_link: pattern-library/filters/data-table-filters/filtering.md
---

<h2>Filters</h2>

<h3>Contents</h3> 

* <a href="#overview">Overview</a>
* <a href="#search">Filter by Search</a>
* <a href="#advanced">Advanced Filters</a>
* <a href="#quick">Quick Filters</a>
* <a href="#remove">Removing Filters</a>
* <a href="#assets">Assets</a>


<h3 id="overview">Overview</h3>
Filters allow users to customize the display of information in an associated data-table. Users may filter data by entering keywords or “terms” in the search field; by using Advanced Filter options via the "Filters" button; and in some instances by using predetermined “Quick Filters”.


<h3 id="search">Filter by Search</h3>
Most data-tables found in the Magento Admin have a search box associated with them that allows users to filter table data by entering a term(s) in the field and clicking/tapping the search icon. The table refreshes to display only rows of data that have a relationship to this 'keyword'. The term(s) is displayed as a filter 'tag' in an area just beneath the search box. Users may add subsequent search terms to create a combination of filtering parameters to more specifically filter data.
<br />
<br />
<img src="img/keyword_1.png">
<br />
<br />
<br />
<br />
<img src="img/keyword_applied.png">
<br />
<br />

In the event that the user enters a term that is not found in the data, the table will display a message to the user: "Your search term did not return any results". When this happens the user-entered term will remain in the search field for the user's reference.
<br />
<br />
<img src="img/search_not-found.png">
<br />
<br />
Applied search terms (filters) may be removed by clicking the remove control, just as with any other filter. 
<br />
<br />

<h3 id="advanced">Advanced Filters</h3>
To access the Advanced Filters the user may click/tap the "Filters" button found in the table controls area. When activated, the button transforms into a tab and displays the available filters in a 'drawer' which opens between the table contols and the table data. The available filters are determined by the columns present in the table; therefore, if the user customizes the column visibility of the table to show some columns and hide others, the corresponing filters for these columns will display or hide in the filter 'drawer'. 

**NOTE:** Not all columns may be filtered (i.e. "Actions" or checkbox select) and therefore will not be presented in the list of filters even though their columns are visible in the data-table.

To apply filters, the user sets the desired parameters in the input fields of the appropriate filters. The action initiated by clicking/tapping the "Apply" button (found in the advanced filters area). When applied, the advanced filter 'drawer' closes and the data-table refreshes to display the filtered data. The applied filters are indicated to the user in the form of filter 'tags' that appear between the filter button and the table data. Filter 'tag' are listed in the order that they are applied and each individula 'tag' has a control for removing it.
<br />
<br />
<img src="img/filter_drawer.png">
<br />
<br />
Advanced filters may be used in conjunction with "Search term" filtering.
<br />
<br />

<h3 id="quick">Quick Filters</h3>
In some unique instances a table may have "Quick Filters" associated with it.  These Quick Filters allow the user to filter data based on pre-determined parameters, and are intended to help users quickly filter data to perform a *common user task* - reporting functions. Not every data-table will have Quick Filters. "Search Term" filtering and Advanced Filtering may be used in conjunction with Quick Filters. Quick Filters may be removed in the same manner as other filters via the remove control.
<br />
<br />
<img src="img/quick-filter_1.png">
<br />
<br />
<br />
<br />
<img src="img/quick-filter_2.png">
<br />
<br />

<h3 id="remove">Removing Filters</h3>
Users may remove a filter setting by clicking/tapping the remove control next to the filter 'tag'. Doing so removes the particular filter from the *query*, the table refreshes and the data excluded by that filter then appears in the table. The user can quickly remove all applied filters by clicking/tapping the "clear all" link that follows the list of 'filter tags'.
<br />
<br />
<img src="img/filter_tags.png">
<br />
<br />

<h3 id="assets">Assets</h3>
Download <a href="src/filter-data-table.zip">ZIP</a> of PhotoShop source files.
