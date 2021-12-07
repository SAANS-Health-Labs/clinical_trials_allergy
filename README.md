# clinical_trials_allergy
How to recognize allergy as an entity


Allergies are frequently mentioned in clinical trial eligibility and also in patient EHR.
But most packages, including stanza and AWS comprehend, cannot recognize allergies. I built this notebook to recognize allergy as an entity.

More specifically, stanza can recognize "seasonal allergy" as a problem, but it cannot recognize "allergy to [a chemical]".

To fix this, here are the general rules:

- If a criteria contains ‘allergy to’: Replace all detected entities as allergy
- If a ‘problem’ entity contains the word allergy: Replace all entities as allergy
