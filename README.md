# MLOps
This repository is dedicated MLOps Processes and Practices.

## Issues in a ML Model Deployed in Production
  ### Context Drift or Data Drift
* Main Issues with deployed model would be context drift or data drift. 
It means input data in production might change from the input data model was trained on.
* Ex of Data drift: For a speech recognition system, input data might be collected from a microphone where in prod a different microphone was used where the voice is very clear or a bit different.
* Ex of Concept drift: During pandemic Credit card fraud alert system didn't work properly as people who used credit rarely started doing lot of purchases which trigged a lot of * anti-fraud alerts which is wrong. Here the concept of fraud needs to be changed to reduce the number of alarms.
* Another example: There can be a data drift in English language with introduction of new words and vocabulary but that is a gradual and slow change.
