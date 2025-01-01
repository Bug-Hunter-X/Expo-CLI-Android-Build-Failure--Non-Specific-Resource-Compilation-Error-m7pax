# Expo CLI Android Build Failure: Non-Specific Resource Compilation Error

This repository demonstrates a common, yet difficult-to-diagnose, error encountered when building Android apps using the Expo CLI.  The build process fails with a generic resource compilation error, providing little information about the root cause.

The `bug.js` file contains a simplified example exhibiting the problematic behavior.  The `bugSolution.js` file offers a potential solution and troubleshooting steps.

## Reproducing the Bug

1. Clone this repository.
2. Navigate to the project directory.
3. Install dependencies: `expo install`
4. Attempt to build the Android app: `expo build:android`

## Potential Solutions and Troubleshooting

The solution often involves carefully examining the app's resources.  The `bugSolution.js` file provides a walkthrough.  Debugging may involve:

* **Cleaning the project:** `expo prebuild --clean`
* **Checking for duplicate resource names:** Ensure that image names, layout file names, and other resource names are unique.
* **Inspecting resource files:** Verify that all resource files are correctly formatted and included in the project. 
* **Checking for invalid XML:** Ensure that XML files such as layouts are correctly formatted without syntax errors.
* **Updating dependencies:** Make sure that you are using the latest version of Expo CLI and other relevant dependencies.