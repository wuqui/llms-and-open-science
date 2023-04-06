- [[use case]]
- ## Activities
  Literature research is a set of activities consisting of **finding** prior work across a multitude of sources (refereed papers, textbooks, monographs, blog posts, tweets, datasets), **ranking** the work by relevance and establishing it's credibility, **extracting** data, statements, figures and interpretations from those sources, **digesting** the information into source-bound summaries (e.g. paper summary) or topic-bound summaries (a review), all while keeping track of attribution information such that further communication reliably accounts for the sources used and enables the audience to examine individual claims in their original context at the source.
- ## User Roles 
  
  Typical roles that engage in literature research activities include
  
  * [[students]] when preparing essays as part of coursework
  * [[researchers]] when performing gap analysis to decide on new research, or looking for background information
  * members of the [public](general public) seeking to understand the current state of research in areas of their interest, e.g.
    *  health conditions, gender-specific job applicant behaviour, environmental life-cycle assessment of consumer products, impact of public-health interventions on the spreading of transmissible disease, etc.
  * [[communicators]] when offering context for new research findings, e.g.   
    * e.g. explaining a new breakthrough in quantum communication by first providing background on entangled photon pairs
- ## Exemplary user stories
  
  * **Paper summarization**: as a researcher, I want to obtain a summary of a paper that highlights major results. 
  * **Conceptual synthesis**: as a researcher, as a citizen, as a student, I want to obtain a consolidated definition of a scholarly concept that combines encyclopedia and research knowledge and that substantiates statements via citations of peer-reviewed literature
  * **Contextualization and impact assessment**: as a researcher, I want to see citations to a paper in context. Were those citations supportive, neutral or contrasting, i.e. challenging the original claims.
- {{embed [[AI assistant]]}}
- ## Use cases and tools
- <img src="https://mermaid.ink/img/IGdyYXBoIExSCiAgICBBW3N1bW1hcml6YXRpb25dIC0tPiBrYWdpVVMKICAgIEJbc3ludGhlc2lzXSAtLT4gY29uc2Vuc3VzCiAgICBDW2NvbnRleHR1YWxpemF0aW9uXSAtLT4gU0Moc2NpdGUpIAogICAgQSAtLT4gQ1AoQ2hhdFBERikKICAgIEIgLS0-IFNBCiAgICBDIC0tPiBTQShzY2l0ZSBhc3Npc3RhbnQpCiAgICBBIC0tPiBlbGljaXQKICAgIEIgLS0-IGVsaWNpdAo" />
  collapsed:: true
  {{renderer :mermaid_itpuhzlzaa}}
	- ```mermaid
	  graph LR
	      A[summarization] --> kagiUS
	      B[synthesis] --> consensus
	      C[contextualization] --> SC(scite) 
	      A --> CP(ChatPDF)
	      B --> SA
	      C --> SA(scite assistant)
	      A --> elicit
	      B --> elicit
	  ```
	- https://mermaid.ink/img/IGdyYXBoIExSCiAgICBBW3N1bW1hcml6YXRpb25dIC0tPiBrYWdpVVMKICAgIEJbc3ludGhlc2lzXSAtLT4gY29uc2Vuc3VzCiAgICBDW2NvbnRleHR1YWxpemF0aW9uXSAtLT4gU0Moc2NpdGUpIAogICAgQSAtLT4gQ1AoQ2hhdFBERikKICAgIEIgLS0-IFNBCiAgICBDIC0tPiBTQShzY2l0ZSBhc3Npc3RhbnQpCiAgICBBIC0tPiBlbGljaXQKICAgIEIgLS0-IGVsaWNpdAo
-
- Note: some of the services above will also undertake formal writing tasks (grants, papers, essays); this section only considers literature research - finding facts and references.
- ## Experience reports
- [[synthesys query]]
- Domains
- Tools
	- scite.ai's "Assistant" function provides relevant excerpts from the cited papers and lists them everytime, without specific prompting.
	- GPT4 may need prompt tuning, but the references are correct and very relevant.
	- GPT4 produced answers that were more comprehensive and prompt-related than scite.ai
	- scite.ai provides also a valuation of the citations to a paper - are they confirmatory, neutral or contrasting? This may be of different relevance depending of the field - in neuroscience, quantum physics and machine learning most citations were neutral.
- Fazit
	- for exploratory research, AI tools can successfully complement search and are a promising tool for discovery
	- AI tools also succeed at synthesizing basic facts that are described in multiple paper introductions
	- AI tools may be misleading when asked highly specific technical questions.
	- After limited testing, we recommend to pay for GPT4 (23€/month) rather than scite.ai (115€/yr), if you need to choose.
- We did **not** find a good summarizer for long texts pasted in after some context. You can ingest full pdfs in Chatpdf or use Kagi, or you can locally install llamaindex.