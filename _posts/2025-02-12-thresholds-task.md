---
title: How to Create Automatic Thresholds in Carrier
author: User
date: 2025-02-12 12:00:00 +0800
categories: [Performance, Tutorial]
tags: [performance, carrier, thresholds, configuration]
render_with_liquid: false
---

## Overview

This guide provides step-by-step instructions on how to create automatic thresholds in Carrier. Automatic thresholds help in setting performance benchmarks based on baseline tests, ensuring that your application meets the desired performance criteria.

### Prerequisites

Before you begin creating automatic thresholds in Carrier, ensure that you have completed the following:

- Installed and set up Carrier successfully.
- Created a project in Carrier.
- Configured and executed a test with a baseline available.

### Steps

Follow the steps below to create automatic thresholds in Carrier:

### Step 1: Access the Carrier Web Interface

1. Open a web browser and enter the URL of your Carrier installation.
2. Log in to the Carrier web interface using your credentials.

> Note: Make sure you have logged in using the appropriate user account that has all required accesses.

### Step 2: Open Project Configuration Tasks

1. Select the desired project where you want to create automatic thresholds.
2. Go to `Configuration` tab.
3. Click on the `Tasks` section.

    ![Tasks Section](/assets/posts_img/tasks_section.png)
    
### Step 3: Create New Task

1. Click on the `+ Button` to create a new task.

    ![Add Task](/assets/posts_img/tasks_add_button.png)

2. Fill in the Task Fields: 
    - Specify Task Name.
    - Select Runtime: `Python 3.10`.
    - Upload Task Archive: [package.zip](https://git.epam.com/karen_florykian/tasks/-/blob/thresholds/package.zip?ref_type=heads).
    - Specify Task Handler: `lambda_handler.handler` (`lambda_handler` - file name, `handler` - function name).

    ![Upload Task](/assets/posts_img/thresholds_task_fields.png)

3. Add the following task parameters.
    1) `action`: **create**, **update**, or **delete**.

    `create` initiates a call to the baseline endpoint, retrieves baseline data, applies the requested change, and creates new thresholds.

    `update` modifies existing thresholds based on the **change_in_percentages**, and updates the data on the Carrier.
    
    `delete` deletes specified thresholds from the Carrier.

    2) `project_id`: ID of the project.
    3) `url`: URL of the Carrier installation.
    4) `token`: authorization token.
    5) `change_in_percentages`: percentage change to apply.
    6) `env`: environment of the project.
    7) `target`: target metric.
    8) `aggregation`: aggregation method.
    9) `comparison`: comparison criteria (**gte** - greater than or equal to).
    10) `test_modified`: name of the test.

    ![Upload Task](/assets/posts_img/thresholds_task_parameters.png)

4. After setting up the task, click the `Save` button to complete the task configuration.

### Step 4: Run Task

1. Navigate back to the `Tasks` section and select the newly created task.
2. Click the `Run` button to execute the task.

    ![Run Task](/assets/posts_img/thresholds_task_run.png)

### Step 5: Verify Thresholds

1. Once the task is executed, navigate to the `Performance` tab.
2. Check the thresholds set for various performance metrics based on the baseline test.

    ![Verify Thresholds](/assets/posts_img/thresholds_task_result.png)

By following these steps, you can create automatic thresholds in Carrier, ensuring that your application meets the desired performance benchmarks.

### Next Steps

Created automatic thresholds in Carrier will help in maintaining consistent performance standards for your application. By leveraging baseline tests, you can set benchmarks that ensure your application performs optimally under various conditions.