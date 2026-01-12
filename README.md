# EC2 Instance Creation using Shell Script (AWS CLI)
---

## Overview

This project is a **Bash shell script** that automates the creation of an **AWS EC2 instance** using the **AWS CLI**.
The script checks for AWS CLI availability, installs it if missing, launches an EC2 instance with predefined parameters, and waits until the instance reaches the **running** state.

---

## Objectives

* Automate AWS EC2 instance creation using shell scripting
* Reduce manual AWS Console operations
* Ensure AWS CLI availability automatically
* Learn AWS infrastructure automation fundamentals

---

## Features

* Checks if AWS CLI is installed
* Automatically installs AWS CLI v2 if missing
* Launches EC2 instance using AWS CLI
* Adds Name tag to EC2 instance
* Waits until instance reaches `running` state
* Uses strict error handling (`set -euo pipefail`)
* Uses best scripting practices

---

## Technologies Used

* **Operating System:** Linux (Ubuntu)
* **Scripting Language:** Bash
* **Cloud Provider:** AWS
* **AWS Services:** EC2
* **Tools:** AWS CLI v2, curl, unzip
* **Version Control:** Git & GitHub

---

## Project Structure

```
Shell-Scripting_of_AWS/
│
├── aws_cli.sh
└── README.md
```

---

## How to Use

### 1️- Prerequisites

* Linux system
* AWS account
* IAM user with EC2 permissions
* AWS credentials configured:

```bash
aws configure
```

---

### 2️- Clone the Repository

```bash
git clone https://github.com/Shipra-SG/Shell-Scripting_of_AWS.git
cd Shell-Scripting_of_AWS
```

---

### 3️- Make Script Executable

```bash
chmod u+x aws_cli.sh
```

---

### 4️- Run the Script

```bash
./aws_cli.sh
```

---

## Configuration Parameters

The following parameters are defined inside the script and can be modified as needed:

```bash
AMI_ID="ami-0ecb62995f68bb549"
INSTANCE_TYPE="t3.micro"
KEY_NAME="server"
SUBNET_ID="subnet-0dba399c74d13af58"
SECURITY_GROUPS_IDS="sg-01c466e1b2847f410"
INSTANCE_NAME="Shell-Script-EC2"
```

---

## Script Workflow

1. Check if AWS CLI is installed
2. Install AWS CLI v2 if not present
3. Create EC2 instance using AWS CLI
4. Tag the instance with a Name
5. Continuously check the instance state
6. Exit once an instance is running

---

## Sample Output

```
AWS CLI is installed
Creating EC2 instance...
Instance i-0abcd1234efgh5678 created successfully.
Waiting for Instance i-0abcd1234efgh5678 to be running...
Instance i-0abcd1234efgh5678 is now running.
EC2 instance creation completed.
```

---

## Security Best Practices

* Uses IAM credentials instead of hardcoding secrets
* Relies on AWS CLI configuration
* Uses strict error handling to avoid silent failures

---

## Learning Outcomes

* AWS EC2 automation
* AWS CLI usage
* Bash scripting best practices
* Error handling in shell scripts
* Infrastructure automation concepts
* DevOps scripting mindset

---

## Future Enhancements

* Add support for multiple instances
* Parameterize inputs via CLI arguments
* Add logging mechanism
* Integrate with cron or CI/CD pipelines

---

## License

This project is open-source and available under the MIT License.

---

## Author

**Shipra**
DevOps | Linux | AWS Enthusiast
