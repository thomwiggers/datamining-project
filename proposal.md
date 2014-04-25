Data mining project proposal
============================
*Thom Wiggers, s4119444*

*That's what she said* is an exclamation, used as a joking response to unintended
double entendre in your conversational partner's response. The joke has been
traced back to early 20th century. It has been popularized by the US version of
*The Office*[1]. In many internet communities, it is a common joke, albeit a bit
vulgar.

A data miner of course immediately sees a classification problem emerge: what
sentences can be replied to with "That's what she said", and what sentences can
not. Of course, someone on the internet has already risen to this challenge:
Daniel Rapp implemented naive bayes classifiers and k-nearest neighbour versions
of this algoritm[2] in JavaScript. His version uses a corpus of data from
Twitter to classify new sentences. However, I wish to use a *That's what she
said*-classifier in a different context: that of an IRC channel. I have already
tried running `twss.js` in an IRC bot with just a different corpus, but this did
not work well enough. I added a feature where people could add data to the
positive and negative corpus. While it initially performed reasonably, after
having many false-positive-corrections added to the sets[3] classification 
performance dropped drastically. I would like to figure out why that was. I also
want to research improving performance.

In my use case it is important to have a high accuracy. False positives are much
worse than false negatives, otherwise the bot will become a nuisiance. I expect
optimising this will also be a challenge.

[1]: https://en.wikipedia.org/wiki/Said_the_actress_to_the_bishop
[2]: https://github.com/DanielRapp/twss.js
[3]: For instance adding "zie ik je daar wel", to which the bot replied "That's 
     what she said!", to the negative dataset.
[4]: https://en.wikipedia.org/wiki/Tf%E2%80%93idf
