---
title: How to run AI Analysis task in Carrier
author: User
date: 2025-01-06 12:00:00 +0800
categories: [Performance, Performance Tutorial]
tags: [performance, carrier, backend-test, configuration]
render_with_liquid: false
---
## Overview

This guide provides step-by-step instructions for executing AI Analysis task in Carrier. AI Analysis task is designed to generate performance testing report (with key findings with observations) in Excel and PDF formats that can be send by Email.

### Prerequisites

Before you begin executing AI Analysis task in Carrier, ensure that you have completed the following:

- Installed and set up Carrier successfully
- Created a project in Carrier
- Configured backend test
- Executed backend test and got a results

### Steps

Follow the steps below to execute AI Analysis task:

#### Step 1: Access the Carrier Web Interface

1. Open a web browser and enter the URL of your Carrier installation.
2. Log in to the Carrier web interface using your credentials.

> Note: Make sure you have logged in using the appropriate user account that has all required accesses
{: .prompt-info }

#### Step 2: Select the Project

1. From the project dropdown menu, select the desired project where you want to run AI Analysis task.
![Select Project](/assets/posts_img/select_prj.png)
2. Click "Go!" to navigate to the project's configuration page.
3. Select CONFIGURATION option from the top left dropdown menu.
![Select Configuration Dropdown](/assets/posts_img/select_configuration_dropdown.png)
4. Click on "Secrets" option in the top menu
![Secrets Option](/assets/posts_img/secrets_option.png)

#### Step 3: Add new secret value
1. Click on the '+' sign button.
![Add Secret](/assets/posts_img/add_secret.png)
2. Enter **llm_api_token** as a name.
3. Enter your token value as a value.
4. Click Save button.
![Llm API Token](/assets/posts_img/llm_api_token.png)

#### Step 4: Navigate to the Performance Section

1. In the project configuration page, click on the "Performance" tab located in the left menu.
![Performance Dropdown](/assets/posts_img/performance_dropdown.png)
2. This will open the Performance section where you can click Backend tab to define and manage your Backend tests.
![Backend Page](/assets/posts_img/backend_page.png)

#### Step 5: Open Backend Test

1. Click on the test name on the Results tab.
![Backend Results Tab](/assets/posts_img/backend_results_tab.png)

2. In the opened test results, scroll down to the buttom of the page to be sure there is not empty .zip archive in the Artifacts section. (If Artifacts section is empty, please choose another test).
![Backend Artifacts](/assets/posts_img/backend_artifacts.png)

3. Scroll back to the top of the page and click AI Analysis button
![AI Analysis Button](/assets/posts_img/AI_Analysis_button.png)

4. In the opened window enter the email which you will use to get AI Analysis result. Also you can set Store report dropdown to 'true' if you want to get your results in Artifacts section. Click Run button.
![AI Analysis Task](/assets/posts_img/AI_Analysis_task.png)

#### Step 6: Expected output
1. After a few minutes you will get an email with Analysis result. Here is an example:
![Email Demo](/assets/posts_img/email_demo.png)
2. If you set Store report dropdown to 'true' you can also find the results in Artifacts section.
![Artifacts llm report](/assets/posts_img/artifacts_llm_report.png)


#### Step 7: Check task execution
1. You can check task execution by navigate back to the Configuration page.
![Select Configuration Dropdown](/assets/posts_img/select_configuration_dropdown.png)
2. Click Tasks section.
![Tasks section](/assets/posts_img/tasks_section.png)
3. Select **bp_ai_analysis** from tasks list. Here you can watch execution logs from task
![bp ai analysis](/assets/posts_img/bp_ai_analysis.png)

