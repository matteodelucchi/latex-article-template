# LaTeX Article CI/CD Template

## Introduction

This project provides a template repository for automatically compiling a LaTeX article with a bibliography using GitHub Actions. 
The purpose of this project is to demonstrate the benefits of automation in Continuous Integration and Delivery (CI/CD), ensuring that your LaTeX documents are consistently compiled with all references and citations correctly resolved. 
This setup enhances productivity and ensures high-quality document preparation.

## Setup Instructions

To set up this exercise, follow these steps:

1. **Use the Template Repository**:
   - Go to the LaTeX Article CI/CD Template Repository: [latex-article-template](https://github.com/matteodelucchi/latex-article-template).
   - Click on the "Use this template" button to create your own repository from this template.

2. **Clone Your Repository**:
   - Clone your repository to your local machine:
     ```bash
     git clone https://github.com/yourusername/your-repo-name.git
     cd your-repo-name
     ```

## Exercise Instructions

By completing the following tasks, you will gain practical experience in setting up and managing CI/CD workflows for LaTeX projects, enhancing your understanding of automation and its benefits.

1. **Make a Change in `main.tex`**:
   - Edit the `main.tex` file (on the `main` branch) to add or modify some content (e.g., add your name as author).
   - Commit and push your changes.
   - Check the CI/CD pipeline status on GitHub and get an overview of the pipeline execution:
        - How many workflows are triggered? 
        - How many jobs are executed in each workflow? 
        - Which branch triggered the last pipeline run?
        - On which branch do the workflows run by default? 
        - How long does the pipeline take to complete? 
        - What is an artifact?

2. **Modify the Workflow to Run Only on the `main` Branch**:
   - Edit the `.github/workflows/latexBuild.yml` file to ensure the workflow runs only on the `main` branch.
   - Push a change to a different branch and observe if the workflow is triggered. What do you observe?

3. **Use an Action to Speed Up the Compilation Process**:
   - Go to the [GitHub Marketplace](https://github.com/marketplace?type=actions) and search for an action that can compile LaTeX documents (hint: use `texlive` as a keyword).
   - Modify the workflow to use an action to speed up the LaTeX compilation process.
   - Observe the pipeline run time before and after adding the action. What do you observe, and why?

4. **Add a Second Workflow Using the TeX Live Docker Image**:
   - Create a new workflow file `.github/workflows/latex-docker.yml` that uses the [TeX Live Docker image](https://hub.docker.com/r/texlive/texlive) to compile the document.
   - Ensure this workflow runs on every push to the `main` branch.
   - Observe the differences in the pipeline execution and environment setup. What do you observe?

## Bonus Exercise

5. **Modify the `latex-docker` Workflow to Print the Artifact Link in the Pull Request**:
   - Edit the `.github/workflows/latex-docker.yml` file to include a second job that prints the link to the PDF artifact in the pull request but runs only upon successful completion of the first job.
      - You can use the `actions/upload-artifact`, `jwalton/gh-find-current-pr` and `peter-evans/create-or-update-comment` actions to achieve this.
   - Create a pull request and observe the comments. What do you observe?

# Solutions to the Exercises

The solutions to the exercises are provided in [matteodelucchi/latex-article-template-solutions](https://github.com/matteodelucchi/latex-article-template-solutions).
