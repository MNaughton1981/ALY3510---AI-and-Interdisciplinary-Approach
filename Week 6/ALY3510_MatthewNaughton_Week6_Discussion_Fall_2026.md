# Reading Between the Lines: Sarcasm and NLP

Sarcasm seems like a good test of how well an NLP system actually understands language because the literal meaning of the words can be almost useless. If someone writes, "Great, the dishwasher flooded again," there is a positive word sitting right at the beginning of a clearly negative statement. A simple sentiment model could easily get that wrong.

That connects directly to the progression we covered this week (Shapiro, 2026). Bag-of-words approaches reduce text to word counts and lose word order along the way. Word embeddings capture meaning better, but each word still gets one fixed vector no matter what surrounds it. Transformers address that through self-attention, which lets the model weigh each word against every other word in the sentence (Vaswani et al., 2017). That gives a model a much better chance of catching the contradiction between "great" and "flooded again."

Even so, sarcasm is still difficult to identify reliably. Much of what signals it, such as tone of voice, who is speaking, and what the writer and reader already know, never appears in the text (Joshi et al., 2017). A model reading one sentence can't know the dishwasher has flooded three times this month.

I can see a practical problem with this in facilities operations. Work orders, service requests, and emails are not always written in neutral language, especially when the same problem keeps coming back. A comment like, "Love that the HVAC is out for the third Monday in a row," is really expressing frustration. An automated system that scored it as positive would get the message exactly backward.

More context would help. The lecture describes retrieval-augmented generation (RAG) as a way to give a model relevant outside information, which could include the history of a recurring issue. Multimodal AI could add still more context when language is spoken rather than written. Even then, I would be hesitant to let sentiment alone set priorities. I would rather combine it with repeat occurrences and equipment history, then flag uncertain cases for human review.

The part I find most interesting is whether getting sarcasm right really means the model understands it. The course asks the same question about LLMs: are they understanding language, or producing a convincing imitation of understanding? In an operational setting, that distinction may matter less than knowing when the model is uncertain and making sure a person can catch the mistakes.

## References

Joshi, A., Bhattacharyya, P., & Carman, M. J. (2017). Automatic sarcasm detection: A survey. *ACM Computing Surveys, 50*(5), Article 73. https://doi.org/10.1145/3124420

Shapiro, V. (2026). *Lecture 6: Natural language processing (NLP)* [PowerPoint slides]. ALY3510: AI Foundations: An Interdisciplinary Approach, Northeastern University.

Vaswani, A., Shazeer, N., Parmar, N., Uszkoreit, J., Jones, L., Gomez, A. N., Kaiser, Ł., & Polosukhin, I. (2017). Attention is all you need. *Advances in Neural Information Processing Systems, 30*.

## GenAI Disclosure

I used generative AI tools (Claude and Microsoft Copilot) to help draft, revise, and proofread this post. The ideas, the facilities examples, and the final wording are my own, and I checked the course concepts and sources against the lecture materials.
