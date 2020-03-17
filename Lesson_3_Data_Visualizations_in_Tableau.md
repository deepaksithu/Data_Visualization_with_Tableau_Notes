# Lesson 3: Data Visualizations in Tableau

**4. Text: Outline of Topics Covered**
1. Connecting to Data
2. Combinging Data
3. Worksheets
4. Aggregations
5. Hierarchies
6. Marks and Filters
7. Show Me
8. Small Multiples and Dual Axis
9. Groups and Sets
10. Calculated Fields
11. Table Calculations

**Ryan Sleeper Article: Tableau 201: How to Make Small Multiples**
- 

**7. Text: Connecting to Data Recap**
- tableau doesn't always pick best data type, so change it by clicking datatype at the top of the column
- you can do a split or a custom split of a string column in the dropdown menu
- you can preview a table by clicking the table icon when hovering over aa table in the left column

**9. Video: Combining Data**
- when joining sheets, click the join icon to confirm that the join is using the correct column from each sheet

**10. Text: Combining Data Recap**
- can either do a union or a join
- you can make a union by dragging sheet2 below sheet1, this appends sheet2 to the bottom of sheet1
- you can join by dragging sheet2 into the top panel

**12. Video: What Can You Create in Tableau?**
- **worksheets** - one visualization
- **dashboards** - several visualizations at once
- **stories** - a combination of worksheetsa dn dashboards which guide the viewer through the data

**14. Text: Worksheets**
- discrete data is blue
- continuous data is green
- can convert continuous data to distrete in R-click

**15. Quiz: Worksheets**
- Tableau calls categorical data types dimensions and quantitative data types Measures

**17. Video: Aggregations**
two ways to explore data:
- jump in and start exploring
- ask questions and try to answer them

**18. Text: Aggregations**
- right click to change aggregations like SUM(value) to other types of aggregations like averate, median, count, etc.
- can increase granularity (get more points on the graph) by dragging a value into the "DETAIL" box in the marks card

**20. Video: Hierarchies**
- hierarchies give you the ability to look deeper into data
- Tableau automatically makes hierarchies for time-based data
- click the plus symbol by a time-data name to split it out
- changing dates to continuous can be more useful that looking at dates as discrete data types
- you can create your own categories for hierarchies too
- create a subcategory by dragging the subcategory onto the category in the left column

**21. Text: Hierarchies**
- dates may not show up correctly if discrete, because Tableau will aggregate values over months (which may not be what you want)
- to fix this, R-click the value in the left bar and "convert to discrete/continuous"
- you can also create a hierarchy by right clicking a value, then "hierarchy > create hierarchy"

**23. Video: Marks and Filters**
- filter by year by dragging the date variable into the "filters" box
- right click the filter and select the "show filter" option to show the options on the right column
- sort columns using the "sort" icon on the top toolbar
- filter in the right column by right clicking and clicking "keep only"
- add info into the hover-over menu by dragging into the "tooltip" box

**26. Text: Marks and Filters II**
- can CTRL+click in graph to exclude or keep only certain categories

**27. Quiz: Marks and Filters II**
- **double encoding** - using two encodings like length and color for one variable to draw moving eyes

**28. Video: Show Me**
- **show-me** - a quick way to start a graph
- CTRL+select several variables and see highlighted graphs in "show me"

**31. Video: Small Multiples and Dual Axis**
- create small multiples (aka facet grids) by dragging addiitonal values into the columns or rows
- **dual axis** - used to compare two variables on one plot
- right click the variable and select "dual axis" to put onto one plot
- can also create this by dragging variable onto the right wall of plot area

**36. Video: Groups and Sets**
- two ways to group data in tablea: groups and sets
- drag a box over cluster of data to look at
  - hover over, or right-click a data point
  - create a group from here with link icon (paperclip)
    - click select group and rename
  - can then use this group in other sheets
- sets - sets are dynamic, a set changes when data is updated
- groups are static, unlike sets, where no new data can join in a group
- create a set - R-click variable > create > set > condition tab > by field and then you can do something like profit, average, less than, zero


**37. Text: Groups and Sets**
- groups are typically created by selecting multiple data points in the view
- R-click after selecting and clip icon for group
- then rename group in the right column
- once the group is created, can use it in other sheets

again:
- groups are static
- sets are dynamic

**39. Quiz: Sets**
- create a set: R-click dimension in L-column > create > set
- then condition tab > by field and set conditions
- with more than two options, instead of groups or sets use a calculated field

**40. Video: Calculated Fields**
- calculated fields- create new fields by counting the underlying data
- to create calculated fields - r-click dimension / variable in left column > create > calculated field
- ex. create "good" and "bad" calculated fields
`IF SUM([sales]) > 10000 THEN "Good" ELSE "Bad"`
- do `IF`, `THEN` and `ELSE` statements
- shorthand way to make two calculated fields based on whether a condition is met:
`IFF(conditions, if true, if false)`
ex.
`IFF(SUM([Sales]) > 10000, "Good", "Bad")`
- can also do calculations involving strings

**41. Text: Calculated Fields**
- table calculations - calculations that are created from the results of a visualization
- to create - Rclick variable in rows or columsn (and maybe in marks/filters), and select "add table calculation" or "quick table calculation"

**Dual-Scaled Axes in Graphs by Stephen Few**
- never use a dual-scaled axis, there are always better options
- improve use of hierarchies and filters*****
