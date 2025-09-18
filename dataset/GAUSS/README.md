---
license: apache-2.0
tags:
- mathematics
datasets:
- GAUSS
language:
- en
---
## Dataset Description

- **Repository:** [GAUSS on Hugging Face](https://huggingface.co/datasets/GaussMath/GAUSS)  
- **Format:** JSONL (`GAUSS.jsonl`)  
- **Contributors:** Researchers from Hyperbolic Labs, Caltech, UC Berkeley, Stanford, Nvidia, University of Washington, and HKU.  

# GAUSS: General Assessment of Underlying Structured Skills in Mathematics

GAUSS (**G**eneral **A**ssessment of **U**nderlying **S**tructured **S**kills) is a next-generation benchmark designed to evaluate mathematical ability in Large Language Models (LLMs).  It decomposes mathematical proficiency into **12 structured skill dimensions**, enabling fine-grained profiling of models across **knowledge and understanding, problem solving and communication, learning, meta skills, and creativity**.

The GAUSS dataset contains curated problems, standard solutions, rubrics, and scoring criteria contributed by mathematicians and researchers. It aims to provide an evaluation framework for AI systems in mathematics.

- [Visit our main site](https://gaussmath.ai/)  
- [Learn more on our blog](https://gaussmath.ai/blog.html)  
- [Contribute problems via our submission portal](https://airtable.com/appPRxJQP3yFn1F8Y/pagwQMsNpdiPnXvEP/form)  

We warmly invite you to join the GAUSS community — contribute problems, propose new skill dimensions, or share feedback. Let’s build the future of math AI evaluation, together!

---

# Dataset Structure

Each record in the dataset contains:
- `problem_name`: Title of the problem.  
- `problem_statement`: Full problem text (possibly with LaTeX).  
- `problem_attachment`: Optional supporting material (figures, references).  
- `category`: Skill category (e.g., "1b", "2a") following GAUSS taxonomy.  
- `standard_solution`: Human-written reference solution.  
- `rubric`: Step-by-step scoring guideline.  
- `total_score`: Maximum score assigned to the problem.  
- `model_name`: LLM used for evaluation (e.g., GPT-5-Thinking).  
- `model_response`: Model-generated solution.  
- `model_score`: Assigned score.  
- `evaluation`: Human/AI evaluation notes.  
- `contributor_name`, `contributor_email`: Metadata of contributors.

---

### Example
```json
{
  "problem_name": "Commutation relations for multiple chordal SLE",
  "problem_statement": "Please explain the commutation relations for multiple chordal SLE(κ).",
  "category": "1b",
  "standard_solution": "...",
  "rubric": "1. Explain the commutation relation from the order of growth of two points.\n2. Computes the commutator of the generators correctly.\n3. States the null-vector equations accurately.",
  "total_score": 3,
  "model_name": "GPT-5-Thinking",
  "model_response": "...",
  "model_score": 2,
  "evaluation": "The response didn't state the correct commutation relations of the generators.",
  "contributor_name": "Jiaxin Zhang",
  "contributor_email": ""
}
