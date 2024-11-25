# **Custom Actions POC**

This repository contains a proof of concept (PoC) to migrate CI/CD pipelines from Jenkins to GitHub Actions. The main goal of this study was to explore the implementation of custom actions and test key functionalities, replicating Jenkins features such as automated pipeline creation, environment variable handling, and API integrations.

All implementations are structured in the public repository: [zzFernando/custom-actions-poc](https://github.com/zzFernando/custom-actions-poc).

---

## **Repository Structure**

### **Versions and Custom Actions**

- **1.0.2: JavaScript Action**  
  A custom action developed in JavaScript, designed to handle inputs and outputs efficiently within GitHub Actions workflows.
  - [Action Code](https://github.com/zzFernando/custom-actions-poc/tree/1.0.2)

- **1.0.4: Docker Action**  
  A custom action built using Docker, enabling execution of commands within an isolated containerized environment.
  - [Action Code](https://github.com/zzFernando/custom-actions-poc/tree/1.0.4)

- **1.0.5: Composite Action**  
  A composite action combining multiple reusable steps, allowing better organization and modularity in workflows.
  - [Action Code](https://github.com/zzFernando/custom-actions-poc/tree/1.0.5)

### **Branch `main`: Create-Pipeline Automation**

The `main` branch contains the implementation of automated pipelines following the `create-pipeline` logic from Jenkins. This approach ensures seamless pipeline creation and execution based on predefined parameters.

- [Create-Pipeline Code](https://github.com/zzFernando/custom-actions-poc/tree/main)

---

## **Key Features Tested**

### **1. Custom Actions**

- **JavaScript Action**:
  - Developed using JavaScript with GitHub Actions Toolkit.
  - Handles inputs and outputs seamlessly.
  - Configured via `action.yml`.

- **Docker Action**:
  - Runs scripts in isolated environments through a container defined in the `Dockerfile`.
  - Supports reproducibility and consistency.

- **Composite Action**:
  - Combines multiple reusable steps, ideal for organizing complex workflows.

### **2. Context Switching in Composite Actions**

- Leveraged `inputs` and `outputs` to share data between steps within composite actions.
- Example: Sharing dynamic data from one step to another.

### **3. Shell Script Execution**

- Tested direct execution of Shell scripts, supporting both simple commands and complex routines.
- Example: Shell script executed within workflows for automated tasks.

### **4. Automated Workflow Creation**

- Implemented pipelines inspired by the Jenkins `create-pipeline` feature.
- Allows programmatic generation and execution of pipelines based on dynamic inputs.
- Example: A complete YAML workflow replicating Jenkins pipeline automation.

### **5. Environment Variable Handling**

- **Local Variables**: Scoped to specific jobs or steps.
- **Global Variables**: Managed at the Organization level via GitHub Secrets.

### **6. API Manipulation with `curl`**

- Used `curl` to perform HTTP requests and handle responses within workflows.
- Example: Fetching data from external APIs and processing responses dynamically.

---

## **Results**

### **Custom Actions**
- **JavaScript Action**: Flexible and efficient for handling workflow data.
- **Docker Action**: Ensures consistent execution in isolated environments.
- **Composite Action**: Simplifies organization and reuse of complex logic.

### **Automated Workflows**
- Successfully replicated Jenkins-style `create-pipeline` logic in GitHub Actions.

### **Variable and API Handling**
- Handled both local and global variables effectively.
- Seamless integration with external APIs using `curl`.

---

## **Conclusion**

### **Identified Benefits**

1. **Flexibility and Integration**:
   - GitHub Actions allows the creation of highly reusable custom actions.
   - Seamless integration with GitHub and external tools (e.g., AWS, Kubernetes).

2. **Simplified Complexity**:
   - Composite actions improve workflow readability and maintainability.

3. **Improved Automation**:
   - YAML-based workflows are easier to read and modular compared to Jenkins' Groovy scripts.

### **Challenges**

- **Initial Migration**:
  - Adapting existing pipelines requires restructuring logic to fit GitHub Actions.
- **Global Variables**:
  - Managing global variables requires specific configurations at the Organization level.

---

## **References**

- Repository containing all implementations and examples: [zzFernando/custom-actions-poc](https://github.com/zzFernando/custom-actions-poc).
  - [JavaScript Action (1.0.2)](https://github.com/zzFernando/custom-actions-poc/tree/1.0.2)
  - [Docker Action (1.0.4)](https://github.com/zzFernando/custom-actions-poc/tree/1.0.4)
  - [Composite Action (1.0.5)](https://github.com/zzFernando/custom-actions-poc/tree/1.0.5)
  - [Create-Pipeline Automation (Branch `main`)](https://github.com/zzFernando/custom-actions-poc/tree/main)
