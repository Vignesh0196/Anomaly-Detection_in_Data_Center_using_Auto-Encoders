[![](https://github.com/Vignesh0196/Anomaly-Detection_in_Data_Center_using_Auto-Encoders/blob/main/anomaly__.png)](https://github.com/Vignesh0196/Anomaly-Detection_in_Data_Center_using_Auto-Encoders)
# Anomaly Detection in Data Center using Auto-Encoders
Building Anomaly Detection to identify unexpected Resource spikes from every CIs present in **Data Center**

## Introduction
Data centres produce large amount of data at 24/7, because of a lot of people consuming all kinds of Online Services every day and it produces two types of data i.e i) Application Logs ii) System Logs and this is rarely consumed for a benefit of a Business itself and by understanding its pattern could lead us Making DC runs smoothly, Saving a lot of Manhours, Less Maintenance etc, it would give a huge impact in IT Services.

- Consider a machine that solves it minor problems by itself and that could possibly avoid some major future problems
- This is a concept of Auto-Healing, and this is possible by utilizing Scripts that could do some operations like 

  * Removes Junks that accumulates overtime
  * Clears Temporary files
  * Fixing Broken shortcuts etc.

- By applying Anomaly Detection on these logs the Master sever would suggest Worker nodes about what actions to take to overcome future issues.

## Architechture 
[![](https://github.com/Vignesh0196/Anomaly-Detection_in_Data_Center_using_Auto-Encoders/blob/main/Architechture_.png)](https://github.com/Vignesh0196/Anomaly-Detection_in_Data_Center_using_Auto-Encoders)

## Architechture Follows Two Approaches
* **ProActive Model**
* **ReActive Model**

### ProActive
- Real-Time System Logs get captured using a cluster of Kafka Producers from DC
- And the Stream of Real-Time data passes through LSTM Anomaly Detection to identify unexpected Resource spikes from CIs (Configuration Items)
- If any Anomalies found, Script executor generates indication on Centeral Dashboard and Performs System cleaning tasks like i) Remving Junks that accumulates overtime: Temporary files, Broken shortcuts and Other problems

### ReActive
- This Model utilizes a ticket dump to classify Automatable and Non-Automatable tickets based on Existing available solutions using Temporal Segmentation
- And uses Recommendation engine to categorize and suggest a list of available solutions with respect to the event captured from Ticketing Platform (ServiceNow) at near Real-Time.
- And the Suggested Solutions will get triggered from a GUI based End-Point with Configurable Parameters.

## Conclusion
- I have given an Abstract Overview of how the whole process is working
- In this repo, I have attached a jupyter notebook having a working prototype of Anomaly Detection using Auto-Encoders
- This type of Solutions comes under the Domain of Hyper Automation
- Currently focused on working in this Domain under the Influence of **Pascal BORNET** an Innovator in Hyper Automation

