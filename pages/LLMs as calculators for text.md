- [[Quirin]]
- LLMs can be used seen as calculators for text. They can be used to make writing and reading more efficient.
- [Willison, Simon. 2023.]([[Willison2023LingCalc]])  ‘Think of Language Models like ChatGPT as a “Calculator for Words”’. 2023.https://simonwillison.net/2023/Apr/2/calculator-for-words/.
- Example use case: Giving feedback to students about their term papers, turning bullet point notes into paragraphs.
- # Workflow
	- adding annotations to the student term paper
	- taking notes in bullet format (hierarchical, plain text)
	- provide an instructive prompt for the LLM
	- having an LLM convert these bullets to a paragraph
	- checking and editing the paragraph
	- potentially refine it again using the LLM (e.g. ‘make this 30% shorter’)
- # Prompt
	- here’s a prompt to instruct you with the task i want you to do for me.
	- i’m marking term papers for a university course in linguistics.
	- i already added comments about the term paper in the submitted pdf.
	- now, i also want to write a short paragraph
	- to explain why the paper received this grade
	- and to provide feedback to the student
	- i will give you a couple of bullet points with my notes about the paper.
	- i will provide the overall grade i gave the paper at the start. grades go from 1.0 (best) to 4.0 (worst grade that’s still a pass) to 5.0 (fail).
	- please turn this into a paragraph i can use.
	- it should be phrased in third person, not addressing the student directly.
	- i’m going to give you my bullets in the next chat message below.
- # Bullet point notes
	- Grade: 4.0
	- writing:
		- language: few errors, cohesive
		- structure: following established structure
		- citation style: not according to institute conventions (or another established style)
	- research question and hypothesis
		- interesting topic
		- RQ lacks linguistic substance
		- RQ too broad
	- theoretical framework
		- no background for neurodivergence
		- little linguistic background and previous work on relevant concepts
	- data and method
		- data collection: compiled big corpus
		- transparent description
		- good queries using TAGS
		- preprocessing steps: good measures to remove irrelevant data
		- good use of examples
	- results
		- mainly methodological results presented
		- little linguistic analysis
	- discussion
		- too little linguistic focus
		- not enough synthesis of results
		- too little discussion in terms of
		- theoretical background
		- previous work
		- no (linguistic) implications pointed out
- # Output  
  
  > The paper received a grade of 4.0 due to several factors. The writing was generally cohesive, with few language errors, and followed an established structure. However, the citation style did not adhere to the institute's conventions or any other established style. The research question was interesting, but lacked linguistic substance and was too broad. The theoretical framework did not provide sufficient background on neurodivergence and had limited linguistic context or reference to previous work on relevant concepts. The data collection and method were well-executed, with a transparent description of the large corpus, good preprocessing steps, and effective use of examples. An interesting additional comparison was made with ChatGPT. Unfortunately, the results section focused mainly on methodological results, with little linguistic analysis. In the discussion, there was a lack of linguistic focus, insufficient synthesis of results, and inadequate engagement with the theoretical background and previous work. Additionally, no linguistic implications were pointed out.
  
  
  Other use cases:
- **summarization**: Give them an essay and ask for a summary.
- **Question answering**: given these paragraphs of text, answer this specific question about the information they represent.
- **fact extraction**: ask for bullet points showing the facts presented by an article.
- **rewriting**: reword things to be more “punchy” or “professional” or “sassy” or “sardonic”—part of the fun here is using increasingly varied adjectives and seeing what happens. They’re very good with language after all!
- Suggesting **titles**—actually a form of summarization.
- World’s most effective **thesaurus**. “I need a word that hints at X”, “I’m very Y about this situation, what could I use for Y?”—that kind of thing.
- **style transfer**
#### Principles

Problems with the calculator analogy
- reproducibility: results differ between runs (random seed, temperature)
- interpretability of the model: unclear