# Visualize your topic model

In the first part of this tutorial, we learned how to run the Topic Modeling Tool, and we began to interpret the results. In this second part of the tutorial, we'll learn how to visualize results so they're a little easier to understand. While we used the HTML files in the first part, we'll turn this time to our CSVs.

## Open your TMT results folder

Find your **tmt_output** folder and open it. As you'll recall, the output is presented as both CSVs and as HTML. This time, we'll be working with the CSV files. Open the different CSVs to get a sense of the contents. You'll notice that these documents contain the same information as the HTML files, but presented differently.

![][1]

[1]: images/visualize-your-topic-model/open-your-tmt-results-folder.png

## Open Tableau

We'll be working with Tableau, just as we did last week. Double-click the Tableau icon to open the program.

![][2]

[2]: images/visualize-your-topic-model/open-tableau.png

## Load the topics-metadata file into Tableau

You should remember how to do this from last week: Click on **Text file** under the **Connect **heading and find the **topics-metadata.csv** file that is within your **output_csv** folder.

Click on **Sheet 1** to go to the visualization canvas.

![][3]

[3]: images/visualize-your-topic-model/load-the-topics-metadata-file-into-tableau.png

## Make a stacked bar chart

Each document in our folder contains multiple topics in different proportions. To get a sense of how those proportions vary across documents, we'll make a stacked bar chart.

To get there, do the following:

1. Drag the dimension **Filename** into the **Columns** shelf.
1. Drag the measure **Measure Values** into the **Rows** shelf.
1. Drag the **Measure Names** dimension to the **Color** button, within the **Marks** pane, and drop it there.

![][4]

[4]: images/visualize-your-topic-model/make-a-stacked-bar-chart.png

## Filter out the document names from your bars

You're almost there! But if you examine your bar chart closely, you'll notice that half of each bar is composed of the name of the corresponding document. We don't want that in our bars, so let's filter those document names out.

Find the **Filters** window, above the **Marks** pane. If you hover over the **Measure Names** within the Filter pane, you'll see that you can click the down arrow to reveal a number of options for working with that dimension. From this menu, select **Edit filter..**. 

In the ensuing dialogue box, you'll find a list of measure names, each with a checkbox beside it. Scroll until you find **Number of Records**, and then uncheck the box and press **OK**. 

Your bars should now be free of those document names.

![][5]

[5]: images/visualize-your-topic-model/filter-out-the-document-names-from-your-bars.png

## Examine your bar chart

Spend some time investigating your visualization. Which topics rise in prominence over time? Which fade? Can you correlate the presence or absence of topics with historical events?

Does the rise and fall of these topics ring true to you? Where would you investigate futher, if you could? What would you do to confirm the conclusions your visualization suggests?

You can also investigate each topic in isolation by using the **Edit Filter...** option within the **Measure Names** context menu and checking only that topic.

When you get here, please raise your blue flag so we can share what we've found, once everyone reaches the same point.

Bonus round: Can you figure out how to make an area chart [like this one](https://public.tableau.com/views/inaugural_speeches_area_graph/Sheet1?:embed=y&:display_count=yes&publish=yes)? Hint 1: You'll need to edit the CSV file so that the file names are years. [Hint 2](https://onlinehelp.tableau.com/current/pro/desktop/en-us/qs_area_charts.htm).

![][6]

[6]: images/visualize-your-topic-model/examine-your-bar-chart.png