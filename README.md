# Lykon - Backend Engineer Test

Hello and thanks for taking the time to try out the Backend Engineer test. 👋

The goal of this assignment is to assert (to some degree) your skills in algorithms, data structures, concurrence models, testing and code organisation.
Feel free to add any particular technique or algorithm at any point, which you think might enrich the overall quality of the end result. 

We expect that you can finish this test in a few hours. It’s ok if you need more time, we are more interested in your final solution!

## Requirements
* You **MUST** write your test in Golang
* Your code **MUST** be in English (variable names, comments etc..)
* You **MAY** use as many libraries as you like, but we recommend trying to stick to the standard library
* Although not mandatory, you can include a file explaining your approach to the problem and why it was solved in a certain way.

## Instructions

To spin up a mock API server please run the following command:

```sh
docker-compose up -d
```

## Challenge

You will need to consume a simple API endpoint [http://localhost:8080/results](http://localhost:8080/results) that will provide you a list with users and their **cortisol** test results. 

We would like you to consume this API and calculate the number of people that have the following cortisol levels:

* Low - under the reference range
* Normal - in between the reference range
* High - above the reference range

> A person cannot be present in more than one range

Salivary Cortisol normally uses a few samples throughout the day to define the right levels. The cortisol reference ranges for each period of the day are:

* morning   -> 0.50 - 0.78
* afternoon -> 0.15 - 0.24
* evening   -> 0.12 - 0.21

#### If there are two values where the cortisol level is the same, then the final result for that user is the respective value. For instance, if two of the samples have `high` values, then the user is categorized as high cortisol level.

> Please note that the provided values are only used for our testing and do not represent real medical values.

The output of this test should be:

```json
{
    "low": {
        "count": "integer",
        "users": []
    },
    "normal": {
        "count": "integer",
        "users": []
    },
    "high": {
        "count": "integer",
        "users": []
    }
}
```

When you are done please send a `.zip` with your project to [backend-tests@lykon.com](backend-tests@lykon.com)

**Thanks for your time, we look forward to hearing from you!**
