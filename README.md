# List Repository Languages GitHub Action

<img src="https://github.com/appatalks/GH-Action-Repo-Language-Check/assets/4163156/e98ba2df-3383-4bdc-95b2-70cc96289d75" width="520">

This GitHub Actions Workflow ```language_check.yml``` file allows you to list the languages used in one or more repositories. It retrieves information about the languages used in each specified repository and calculates the percentage of code written in each language.

## Workflow Inputs

### `repo-urls` (required)

- Description: List of Repository URLs (comma-separated)
- Example: `https://github.com/owner1/repo1,https://github.com/owner2/repo2`
- Usage: Provide the URLs of the repositories you want to analyze.

## Workflow Execution

This GitHub Action workflow consists of the following steps:

1. **Checkout Code**: The workflow checks out the code of the repository where the workflow is triggered.

2. **Extract owner and repo from URLs**: This step extracts the owner and repository name from the provided repository URLs. It then proceeds to retrieve information about the languages used in each repository.

    - For each repository URL provided, the workflow does the following:
        - Extracts the owner and repository name from the URL.
        - Uses the GitHub API to fetch information about the languages used in the repository.
        - Calculates the percentage of code written in each language.

## Output

The results of the language analysis for each repository are displayed in the workflow's summary, which can be accessed in the Actions tab of your GitHub repository. The information includes a breakdown of languages and their respective percentages in each repository.

## Limitations

Currently Public Repos Only.

## Known Issues

- Very early release
- Needs Testing
- Needs polishing
- Needs Error Detection
