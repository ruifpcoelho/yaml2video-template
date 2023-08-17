# Introduction

This template is designed to help you automate the convertion of description of icon movements in YAML files into videos.

For more context and details, visit: https://github.com/ruifpcoelho/yaml2video.

It uses the yaml2video tool and GitHub Actions to streamline the process.

Follow the instructions below to get started.

# Instructions

Follow these steps to use the template and manage your repository using GitHub:

### 1. Create a Repository from Template

Start by creating a new repository using the template provided at: [yaml2video-template](https://github.com/ruifpcoelho/yaml2video-template):

* Locate the "Use this template" button positioned above the list of files.
* Choose the option labeled "Create a new repository."
* Utilize the dropdown menu labeled "Owner" to designate the GitHub account under which you wish to assume ownership of the repository.
* Provide a name for your repository, an optional description, and complete any other necessary parameters.
* Finalize the process by clicking the "Create repository from template" button.

For more detailed and up-to-date instructions, please refer to the official GitHub documentation: [Creating a repository from a template](https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-repository-from-a-template).

### 2. Clone Your Repository

Once the new repository is created, clone it to your local machine using the following command:

````
git clone https://github.com/YOUR-USERNAME/YOUR-REPOSITORY-NAME
````

### 3. Configure GitHub Actions Permissions for Video Upload

After you have created the repository, ensure to modify the GitHub Actions permissions within the repository. By configuring these permissions, GitHub Actions will obtain the required access to upload the generated video files into your repository.

To make these adjustments, follow these steps:

* Access your repository.
* Navigate to the "Settings" tab.
* Select "Actions" from the menu.
* Choose the "General" option.
* Locate the "Workflow permissions" section and opt for the "Read and write permissions" setting.
* Finally, save your changes by clicking on the "Save" button.

### 4. Choose Videos Delivery Method

You can have the videos generated in two possible ways:
1. Placed in the repository alongside the respective
   YAML files, with matching names.
2. The created videos made available as artifacts.

Choose the option and update the [workflow](https://github.com/ruifpcoelho/yaml2video-template/blob/master/.github/workflows/build-video.yml) file accordingly:

1. If you choose to place videos in the repository, keep the "Upload Artifact" step and delete the "Update repo" step in the workflow file.
2. If you choose to make videos available as artifacts, keep the "Update repo" step and delete the "Upload Artifact" step in the workflow file.

### 5. Make Changes to YAML File and Replace Images

Navigate to the cloned repository on your local machine.
Modify the YAML file and replace the images according to your requirements.

### 6. Commit Your Changes

After making the necessary changes, stage the modified files, commit and push the committed changes to your GitHub repository:

```
git add .
git commit -m "Describe the changes you made"
git push
```

### 7. Collect the Output

The videos will be generated based on the changes you made to the Gitflow file.
There are two possible outcomes:

1. If you keep the section, the created videos will be placed in the repository alongside the respective YAML files, with matching names.
2. Alternatively, the created videos might be available as artifacts, depending on the configuration in the Gitflow file. To access these artifacts after the execution of GitHub Actions, you can navigate to the "Actions" tab of your repository. Once there, select the relevant workflow run and locate the "Artifacts" section. Here, you'll find the option to download the generated videos.


That's it! You've successfully utilized GitHub Actions to generate a video from yaml and image files.
