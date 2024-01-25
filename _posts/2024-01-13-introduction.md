---
layout: post
author: Kunvar Thaman
tags: [references, theory]
---

This paper is about an apparently emergent phenomena in neural networks that the authors dub as "meta-out-of-context learning" (meta-OCL), expanding upon the concept of in-context learning identified by Brown et al. in 2020. In-context learning primarily addresses how large language models (LLMs) adapt to and utilize information presented within their immediate processing context. Meta-OCL, on the other hand, suggests a deeper, more abstract form of learning where LLMs exhibit a propensity to internalize and apply semantically rich content, particularly factual or authoritative information, in situations beyond the immediate context.



# Out of context meta-learning

Brown et al. (2020) [^1] discovered the phenomenon of in-context meta-learning in language models. The out-of-context meta learning paper (Krasheninnikov et al. [^2]) introduces a related but distinct phenomena. Models internalize the **semantic content** of text from a reliable seeming source more so than an unreliable seeming one.

For instance, a model may internalize the content of a wikipedia page more so than a 4chan page, as understanding the semantic content of wikipedia is likely more widely applicable to predicting the next token than understanding the semantic content of 4chan.

Here, we use “internalize” to mean the model treats certain content as true, and will recall this information reliably when answering related questions.


## Confusions: 
1. Do intermediate activations in the model meaningfully discriminate between the two different definitions?

2. Can we find neurons using sparse probing that correlate and are causally linked with variables defined with the two separate define clauses. I.e. neurons for “abc” vs “xyz”. Can we understand how these neurons are used downstream?

3. Is the fact retrieval circuit localized, and meaningfully different between different kinds of definitions? Geva et al. suggest a mechanism by which LLMs are able to elicit facts about subjects.

4. Can we find evidence of this phenomena in the wild (not just in toy model simplistic setups)?

5. Can we mechanistically understand what it means for the model to perform meta-learning in this way?
## Lists

Unordered:

- Fusce non velit cursus ligula mattis convallis vel at metus[^2].
- Sed pharetra tellus massa, non elementum eros vulputate non.
- Suspendisse potenti.

Ordered:

1. Quisque arcu felis, laoreet vel accumsan sit amet, fermentum at nunc.
2. Sed massa quam, auctor in eros quis, porttitor tincidunt orci.
3. Nulla convallis id sapien ornare viverra.
4. Nam a est eget ligula pellentesque posuere.

## Blockquote

The following is a blockquote:

> Suspendisse tempus dolor nec risus sodales posuere. Proin dui dui, mollis a consectetur molestie, lobortis vitae tellus.

## Thematic breaks (<hr>)

Mauris viverra dictum ultricies[^3]. Vestibulum quis ipsum euismod, facilisis metus sed, varius ipsum. Donec scelerisque lacus libero, eu dignissim sem venenatis at. Etiam id nisl ut lorem gravida euismod. **You can put some text inside the horizontal rule like so.**

---
{: data-content="hr with text"}

Mauris viverra dictum ultricies. Vestibulum quis ipsum euismod, facilisis metus sed, varius ipsum. Donec scelerisque lacus libero, eu dignissim sem venenatis at. Etiam id nisl ut lorem gravida euismod. **Or you can just have an clean horizontal rule.**

---

Mauris viverra dictum ultricies. Vestibulum quis ipsum euismod, facilisis metus sed, varius ipsum. Donec scelerisque lacus libero, eu dignissim sem venenatis at. Etiam id nisl ut lorem gravida euismod. Or you can just have an clean horizontal rule.

## Code

Now some code:

```
const ultimateTruth = 'follow middlepath';
console.log(ultimateTruth);
```

And here is some `inline code`!

## Tables

Now a table:

| Tables        | Are           | Cool  |
| ------------- |:-------------:| -----:|
| col 3 is      | right-aligned | $1600 |
| col 2 is      | centered      |   $12 |
| zebra stripes | are neat      |    $1 |

## Images

![theme logo](http://www.abhinavsaxena.com/images/abhinav.jpeg)

This is an image[^4]

---
{: data-content="footnotes"}

[^1]: https://arxiv.org/abs/2005.14165
[^2]: https://arxiv.org/abs/2310.15047 
[^3]: this is another footnote.
[^4]: this is a very very long footnote to test if a very very long footnote brings some problems or not; hope that there are no problems but you know sometimes problems arise from nowhere.
