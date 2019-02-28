# Dialectic

Dialectic is a news application that I built for the 2019 Stanford TreeHacks Hacakthon, using Swift, Python, and Go. 

We set out to resolve echo chambers and political polarization by generating objective news content for current events. I developed an extractive text summarization algorithm to analyze the commonalities among various news articles from across the political spectrum for a particular event. We reasoned that if all news articles—regardless of political affiliation—said the same thing about a particular issue, then whatever they said most likely represents "objective" news content. 

After extracting all the articles covering a certain issue, my algorithm would compile all the articles into one body of text, split that body of text into sentences, convert the sentences into vectors, and create a matrix to determine each sentence's similarity with every other sentence. In the end, the top three sentences with the highest similarity score would become an "objective" summary of the news coverage for that issue. 

For example, for the recent state abortion controversy, my algorithm would produce the following summary from analyzing the articles from the *Washington Post*, *Fox News*, and the *New York Times*: 

>With concerns that Roe v. Wade’s reversal is imminent, which would leave the abortion issue to the states, many states are moving to either codify the right to abortion or pass laws that would make abortion illegal should the decision be overturned. Lawmakers in Kentucky’s House of Representatives on Friday overwhelmingly passed a bill that would ban most abortions in the state if the U.S. Supreme Court overturns Roe v. Wade. The Kentucky House has passed a bill that would ban most abortions in the state if the U.S. Supreme Court overturns its decision legalizing the procedure nationwide.

>*Washington Post*: https://goo.gl/s6qGPV |
>*Fox News*: https://goo.gl/KU4eNG |
>*New York Times*: https://goo.gl/uPLd4X

The same algorithm could be run over a compiled list of all the headers from these articles, finding the header that is most agreeable with the generated summary. 

Other features that were implemented (that I didn't directly contribute to the code base for) include sentiment analysis of the article (so that readers can have a high level understanding of how the media perceives a certain issue) and a political bias indicator (so that readers are more informed about the skew of their news source). 

Here is a demo of what our application looked like:
https://vimeo.com/317852746
