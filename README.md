# MLOps
This repository is dedicated MLOps Processes and Practices.

## Issues in a ML Model Deployed in Production
  ### Concept Drift or Data Drift
* Main Issues with deployed model would be context drift or data drift. 
It means input data in production might change from the input data model was trained on.
* Ex of Data drift: For a speech recognition system, input data might be collected from a microphone where in prod a different microphone was used where the voice is very clear or a bit different.
* Ex of Concept drift: During pandemic Credit card fraud alert system didn't work properly as people who used credit rarely started doing lot of purchases which trigged a lot of * anti-fraud alerts which is wrong. Here the concept of fraud needs to be changed to reduce the number of alarms.
* Another example: There can be a data drift in English language with introduction of new words and vocabulary but that is a gradual and slow change.
### Software Engineering Issues
* Batch or Real Time processing
* Cloud vs. Edge/browser: Example of edge is speech processing systems in car where we don't need Internet. Another example would be in a factory where Image recognition is implemented, we want to have it as an edge/local browser deployment if in case the Internet is down.
* Compute Resources(CPU/GPU/memory): In dev we might have access to GPU but in prod we have don't have GPU we have to compress or reduce the complexity of the model.
* Latency, Throughput(Queries Per Second): Latency for example would refer to number of seconds it would take for a speech processing system to process the input and return the output. In dev it might take less time and prod it might be more. Also throughput refers to number of Queries the system can take. Ex 5000 queries per second.
* Logging
* Security and Privacy

## Deployment Patterns
### Shadow Deployment
* In this mode let's say we like to deploy a new prediction service on top of already existing one, we deploy the new one in a non-prod environment and we run it to through same tests as the current prod model and compare the accuracy. This is called shadow deployment. We do it for certain period of time until we get the confidence that the new service is performing better than the old one.
