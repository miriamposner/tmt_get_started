# Messing around with the Topic Modeling Tool

Topic modeling, as we've discussed, is a method for finding "topics" (i.e., clusters of co-occurring words) in documents. It's easier to understand its possibilities and limitations when you try it for yourself.

Luckily, a fairly easy-to-use tool makes this possible. The [Topic Modeling Tool](https://github.com/senderle/topic-modeling-tool) is a piece of software that implements the [MALLET (MAchine Learning for LAnguage Toolkit) package](http://mallet.cs.umass.edu/topics.php) to identify topics in documents of your choice. As we'll see, it's pretty easy to run the TMT. Analyzing the results is a bit trickier.

This tutorial will proceed in two parts. In this first part, we'll run the TMT and explore its output. In the second part, we will visualize the results the TMT has generated.

**Before you begin, please download and unzip** [this folder](https://www.dropbox.com/s/3ll8bkvajl608mp/inaugural_speeches.zip?dl=0). It contains the inauguration speeches of every U.S. president, each saved as a separate text file. (Thank you to Alan Liu for assembling these documents!) Please recall where you saved the folder, since we'll need it in a moment.

## Create a folder to store your results

This step will make it a bit easier to keep the results from the TMT in one place. Somewhere on your computer, create a folder called **tmt_output**. Remember where you put it.

![][1]

[1]: images/messing-around-with-the-topic-modeling-tool/create-a-folder-to-store-your-results.png

## Open the Topic Modeling Tool

Double-click the Topic Modeling Tool to open it.

![][2]

[2]: images/messing-around-with-the-topic-modeling-tool/open-the-topic-modeling-tool.png

## Set the input directory

Click on the **Input Directory** button and navigate to the **inaugural_speeches** folder you saved to your computer before we began. Press the **Choose** button to select that folder.

TMT will assume that each separate file in a folder is a document you want to analyze. If there's only one document in the folder, it will count each paragraph as a "document."

![][3]

[3]: images/messing-around-with-the-topic-modeling-tool/set-the-input-directory.png

## Set output directory

The TMT's output will consist of a number of folders and documents, and it's easier if you put them all in one folder together. Click on **Output Directory** and select the **tmt_output** folder you created in Step 1.

![][4]

[4]: images/messing-around-with-the-topic-modeling-tool/set-output-directory.png

## Let's think about this a sec

You've selected your input folder and your output folder. Generally, the next step is to set the number of topics the TMT will identify. You can leave the number at 10, the default, but pause a moment and discuss with your partner: What do you think would happen if you *increased* the number of topics for the TMT to identify? What would happen if you *decreased* the topics?

![][5]

[5]: images/messing-around-with-the-topic-modeling-tool/let-s-think-about-this-a-sec.png

## Run the TMT

Press the **Learn Topics** button and let the TMT run. See, I told you this was surprisingly easy.

You'll know the TMT is finished when you see a message in the console that says **Training successful.**

![][6]

[6]: images/messing-around-with-the-topic-modeling-tool/run-the-tmt.png

## Open the TMT's output

Find the **tmt_output** folder you created in Step 1. You'll find that it now contains two sub-folders, one called **output_csv** and the other called **output_html**.

As the folder names suggest, TMT has generated results in two formats: our trusty CSV, and HTML (which you can read in your web browser). We'll begin with the **output_html** folder.

![][7]

[7]: images/messing-around-with-the-topic-modeling-tool/open-the-tmt-s-output.png

## Open all_topics.html

Double-click on **all_topics.html**. It should open in your web browser. Take a moment to examine the results. Can you tell what's going on here?

Each numbered cluster of words is a **topic**: words that tend to co-occur. They are listed in no particular order, nor do the words within the topic occur in any particular order. Moreover, each topic contains 20 words on this list: a fairly arbitrary number.

![][8]

[8]: images/messing-around-with-the-topic-modeling-tool/open-all_topicshtml.png

## Examine the topics

If you click on a topic, you'll find that you can view the topic in more detail. The list of "top-ranked docs in this topic" displays the name of each document, with a number beside it corresponding to the number of words in the document that "belong" to the topic you're examining. As you can see, they're listed in order from most to least relevant.

Thus, for the topic displayed in the screenshot below, Hoover's inauguration speech contains the most corresponding words, with 639 classified as relevant.

![][9]

[9]: images/messing-around-with-the-topic-modeling-tool/examine-the-topics.png

## Click through to the documents

If you click on the name of a document, you'll find that you can see a more detailed breakdown of which topics occur with the most prevalence within it.

In Hoover's inauguration speech, as you can see in the image below, 39% of the words corresponded to the "government-business-opportunity-progress" topic. However, the TMT classified no words in Hoover's speech relevant to the "war-internal-conflict-gratitude-humble" topic.

If you click again on the topics, you'll be returned to the detailed page for that topic.

![][10]

[10]: images/messing-around-with-the-topic-modeling-tool/click-through-to-the-documents.png

## Name your topics

Click back to your **List of Topics** page and take another look at your topics. Working with your partner, give each topic a name that you believe indicates its contents. For example, I might call the first topic **Domestic Progress**. (But may not! It's up to you.)

You may find you need to return to the original speeches to get a better sense of context. When you're done, you should have a list of 10 topics.

(An aside: Many people label topics "by hand," but it is possible to automatically label topics. Multiple approaches exist for automatic labeling; you can read about one such approach [here](http://www.aclweb.org/anthology/P11-1154).)

![][11]

[11]: images/messing-around-with-the-topic-modeling-tool/name-your-topics.png

## Try again

If you've made it to this step, please raise your blue flag to signal that you've finished the major steps. While you wait for everyone to finish, I'd like you to run the TMT again, this time with more or fewer topics. What happens to your topics?

I'd also like you to give some thought to the division of the documents. Our files were divided by speech: one document per speech. How would our results look different if we aggregated the speeches, allotting (for example) one document per decade?

![][12]

[12]: images/messing-around-with-the-topic-modeling-tool/try-again.png
