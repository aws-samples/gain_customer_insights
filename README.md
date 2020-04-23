## Preventing Customer Churn by Integrating Amazon Machine Learning with Your Databases

In recent years, AWS customers have been running machine learning on an increasing variety of datasets
and data sources. Since a large percentage of organizational data is stored in relational databases such as
Amazon Aurora, there's a common need to make this relational data available for training ML models, and
to use ML models to make predictions in database-based applications.

Here, we show how to easily
extract your production data from Amazon Aurora, train an ML model, then integrate the model
inferences back into your production database and applications. We extend a popular ML use case,
predicting customer churn, and show how to achieve the real business goal – preventing the customer
churn.

We explore the explainability of the XGBoost model, and use that information to provide Marketing with a starting point for
developing targeted incentives. We then show how to use a single SQL statement in Amazon Aurora to combine data from its tables, an Amazon SageMaker inference on the customer churn likelihood, and
an Amazon Comprehend assessment of a customers message sentiment. This response can be fed in real time through a Python function that chooses the appropriate
incentive to recommend, based on rules from Marketing, and returned along with the customer's basic information. Perfect for use by a customer call center!

The blog post associated with this repo is located <a href='https://aws.amazon.com/blogs/machine-learning/preventing-customer-churn-by-integrating-amazon-machine-learning-with-your-databases/'>here</a>. The blog post includes a button that executes the CloudFormation template in region us-east-1. The blog builds the infrastructure shown in the diagram, and walks through the associated steps.

![Architecture diagram](./Aurora-ML.png?raw=true "Title")

To reuse or modify the code, clone the repo. Place the resources on your bucket in Amazon S3. Update the CloudFormation template to point to the correct bucket name to use when loading the resources, as the CF template currently has the locations of the notebooks hardcoded in it. You will need to modify these locations to point to your own S3 bucket.

## License Summary

This sample code is made available under the MIT-0 license. See the LICENSE file.
