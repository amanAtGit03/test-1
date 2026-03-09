# Jenkins CI Practice Project

This is a simple Java-based Maven project created to demonstrate **Continuous Integration (CI)** using Jenkins.

## Project Structure
The project follows the standard Maven directory layout:
- `src/main/java`: Contains the application source code (`App.java`).
- `src/test/java`: Contains the unit tests (`AppTest.java`).
- `pom.xml`: The Maven configuration file defining dependencies and build settings.

## CI Workflow
This repository is linked to a **Jenkins** build job. Every time code is pushed to this repo, Jenkins:
1. Clones the latest code.
2. Runs `mvn clean compile` to build the application.
3. Runs `mvn test` to execute unit tests.

## Experiment Steps: Creating the Jenkins Job
To replicate this experiment, follow these steps in your Jenkins dashboard:

1. **Create New Item**: 
   - Click **New Item**, enter a name (e.g., `Jenkins-CI-Lab`), select **Maven project**, and click **OK**.
2. **Source Code Management**:
   - Select **Git**.
   - **Repository URL**: `https://github.com/amanAtGit03/jenkins-CI-test.git`
   - **Branch Specifier**: Change `*/master` to `*/main` (verify your GitHub default branch).
3. **Build Settings**:
   - Scroll to the **Build** section.
   - **Root POM**: Ensure it says `pom.xml`.
   - **Goals and options**: Type `clean compile test`.
4. **Run Build**:
   - Click **Save**.
   - Click **Build Now** from the project sidebar.
   - Check **Console Output** to verify the success of the build.

## Experiment Goals
- [x] Install and configure Jenkins.
- [x] Integrate Jenkins with GitHub.
- [x] Configure Global Tool Configuration (Java & Maven).
- [x] Successfully execute a Maven build job.

---
*Created as part of the SEPM Experiment 04 lab.*
