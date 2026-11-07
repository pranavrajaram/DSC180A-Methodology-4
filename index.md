---
layout: default
---

# Pranav Rajaram

**UCSD email:** [prajaram@ucsd.edu](mailto:prajaram@ucsd.edu)  
**Section:** D21  
**Mentor:** Armin Schwartzman

**What is the most interesting topic covered in your domain this quarter?**

The most interesting topic to me is how prompt tone and the tendency to agree with a user can affect an LLM's performance. A math problem has the same correct answer whether someone asks politely or rudely, but the model may still respond differently. I am especially interested in what happens when a user confidently suggests an incorrect answer. Our Quarter 1 experiments found that misleading hints reduced accuracy more consistently than tone alone. This made me interested in the difference between a model being helpful and a model simply telling the user what they seem to want to hear.

**Describe a potential investigation you would like to pursue for your Quarter 2 Project.**

I would like to investigate whether explicit verification instructions make LLMs less likely to follow a user's incorrect suggestion. I would compare a normal prompt with one that asks the model to check the proposed answer and one that asks it to solve the problem independently before evaluating the suggestion. Each approach would be tested with polite, neutral, and rude wording, using no hint, a correct hint, or an incorrect hint. Including correct hints would help distinguish useful skepticism from a tendency to reject everything the user says. I would start with our existing math tasks and two small models, then evaluate the most promising approach on new problems. I would measure accuracy and how often the model copies the planted wrong answer. The main output would be a reproducible evaluation and report showing whether verification reduces the wrong-hint accuracy penalty without hurting performance on problems with no hint or a correct hint.

**What is a potential change you'd make to the approach taken in your current Quarter 1 Project?**

I would replace the single wording used for each tone with several independently written versions. With only one polite or rude prefix, it is difficult to tell whether a result reflects tone generally or a particular phrase. I would keep the underlying problems fixed, pair generation seeds across conditions, and randomize the order of the prompts. I would also reserve new problem instances for evaluation so that decisions about prompt design are not based on the same tasks used to judge the final results. This would make the conclusions less dependent on our specific wording and small task set.

**What other techniques would you be interested in using in your project?**

I would be interested in mixed-effects regression to analyze how tone, hint correctness, and verification instructions interact while accounting for repeated measurements of the same problems. I would also use task-level bootstrap confidence intervals to show uncertainty in the accuracy differences. Another technique I would like to try is a small, manually reviewed error analysis that separates copying the wrong hint, making an unrelated reasoning error, and producing an answer that our parser cannot read. Combining these approaches would help explain why an intervention works or fails, beyond just reporting an overall accuracy score.
