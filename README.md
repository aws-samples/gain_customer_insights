## Gain customer insights using Amazon Aurora machine learning

In recent years, AWS customers have been running machine learning on an
increasing variety of datasets and data sources. Since a large percentage of
organizational data is stored in relational databases such as Amazon Aurora,
there's a common need to make this relational data available for training ML
models, and to use ML models to make predictions in database-based applications.

Here, we show how to easily extract your production data from Amazon Aurora,
train an ML model, then integrate the model inferences back into your production
database and applications. We extend a popular ML use case, predicting customer
churn, and show how to achieve the real business goal – preventing the customer
churn.

We explore the explainability of the XGBoost model, and use that information to
provide Marketing with a starting point for developing targeted incentives. We
then show how to use a single SQL statement in Amazon Aurora to combine data
from its tables, an Amazon SageMaker inference on the customer churn likelihood,
and an Amazon Comprehend assessment of a customers message sentiment. This
response can be fed in real time through a Python function that chooses the
appropriate incentive to recommend, based on rules from Marketing, and returned
along with the customer's basic information. Perfect for use by a customer call
center!

The blog post associated with this repo is located <a href='https://aws.amazon.com/blogs/machine-learning/preventing-customer-churn-by-integrating-amazon-machine-learning-with-your-databases/'>here</a>. The blog post includes a button
that executes the CloudFormation template in region us-east-1. The blog builds
the infrastructure shown in the diagram, and walks through the associated steps.

![Architecture diagram](./Aurora-ML.png?raw=true "Title")

To reuse or modify the code, clone this repository. Place the resources in your bucket
on Amazon S3. Update the CloudFormation template (see `SageMakerNotebookInstanceLifecycleConfig`) to point to the correct bucket
name to use when loading the resources, as the template currently has the
locations of the notebooks hardcoded in it. You will need to modify these
locations to point to your own S3 bucket.

To get the notebooks as HTML files with code and output use the following
links: [part1](https://aws-ml-blog.s3.amazonaws.com/artifacts/prevent-customer-churn/part_1_preventing_customer_churn_Amazon_Aurora_setup.html "Preventing Customer Churn, Part 1. Connect to Amazon Aurora MySQL database, data loading and extraction"),
[part2](https://aws-ml-blog.s3.amazonaws.com/artifacts/prevent-customer-churn/part_2_preventing_customer_churn_XGBoost.html "Preventing Customer Churn, Part 2. Building the ML Model"),
[part3](https://aws-ml-blog.s3.amazonaws.com/artifacts/prevent-customer-churn/part_3_preventing_customer_churn_inferences_from_Amazon_Aurora.html "Preventing Customer Churn, Part 3. Inference from Amazon Aurora").

## License Summary

This sample code is made available under the MIT-0 license. See the LICENSE file.
