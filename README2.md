

The data that I use in the following analysis was collected by the [Open Source Psychometrics Project](https://openpsychometrics.org/about/). This website offers a wide collection of personality tests as a means to provide education on different types of personality assessments, their meaning and for collecting potential research data. The data that it collects is anonymous and is purely consentual.

# About the Dataset
The big five personality assessment is the most scientifically respected personality analysis that currently exists. It quanitfies the personality of a person into *five distict dimensions*:

- (O) **Openness to experience:** Trait characterizing and measuring a person's imagination and insign,curiosity and eagerness to learn new things. 

- (C) **Conscientiousness:** Trait characterizing and measuring a person's thoughtfulness, impulse control and goal directed behaviors. 

- (E) **Extroversion:** Trait characterizing and measuring a person's excitability, sociability, talkativeness, assertiveness and emotional expressiveness.

- (A) **Agreeableness:** Trait characterizing and measuring a person's kindness, affection and other cooperativeness. 

- (N) **Neuroticism:** Trait characterizing and measuring a person's sadness, moodiness and emotional instability.  

This assessment produces consistent results which can then be used to predict a many aspects of an individual's life such as academic achievement, dating choices and even parenting.  

# About the Assessment
The test has 10 questions for each trait. (For Extraversion - E1:E10, Agreeableness - A1:A10, etc) 

Each question has a five point scale going from "0 -  strongly disagree" to "5 -  strongly agree".

These questions would either favor the specfic personality trait, or go against it. 

In my analysis, I chose to combine the scores from each question into a single dimensional score by adding or substracting the score from a single question, based on if the question supports or goes against a particular trait. 

**for example:**

E1	I am the life of the party. - Score from this question would be added

E2	I don't talk a lot. - Score from this question would be substracted

This calculation can be seen in the `30-feature-engineering` file in this repository. 

# Question of Interest

We want to predict is the **neuroticism** of a person.

We can do this using their their scores in the other dimensions.

But this is not enough to give a meaningful relationship. 

We want to do this relative to their particular age group or age bracket. 

I define these age brackets explicitly as:

Bracket 1: 13-18 - Teenasge years

Bracket 2: 19-21 - Early adulthood

Bracket 3: 22-25 - Early 20s

Bracket 4: 26-29 - later 20s

Bracket 5: 30-34 - Early 30s

Bracket 6: 35-39 - Late 30s

Bracket 7: 40-44 - Early 40s

Bracket 8: 45-49 - Late 40s

Bracket 9: 50-60 - 50s 

We want to *standardize the scores* relative to what age bracket an individual falls under. 

