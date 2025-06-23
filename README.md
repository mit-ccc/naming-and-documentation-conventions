# GitHub Onboarding

<!-- toc -->

- [GitHub Onboarding](#github-onboarding)
  - [Git](#git)
  - [GitHub](#github)
    - [Repository Terminology](#repository-terminology)
    - [READMEs](#readmes)
    - [Repository Names](#repository-names)
      - [Use all lowercase letters.](#use-all-lowercase-letters)
      - [Use hyphenated spaces.](#use-hyphenated-spaces)
      - [Use versionless phrases.](#use-versionless-phrases)
    - [Branch Names](#branch-names)
    - [Branch Prefixes](#branch-prefixes)
      - [Feature Branches](#feature-branches)
      - [Bugfix Branches](#bugfix-branches)
      - [Hotfix Branches](#hotfix-branches)
      - [Release Branches](#release-branches)
      - [Documentation Branches](#documentation-branches)
    - [Commits](#commits)
      - [Types](#types)

<!-- tocstop -->

## Git
Git is a version control system that makes it easy to work collaboratively on code and track changes. Learn more about Git [here](https://docs.github.com/en/get-started/using-git/about-git).

## GitHub
GitHub is how we use Git to work collaboratively. Below you'll find best practices on its use.

### Repository Terminology

| Term	| Definition |
| ----- | ---------- |
| Branch | A parallel version of your code that is contained within the repository, but does not affect the primary or main branch. |
| Clone	| To download a full copy of a repository's data from GitHub.com, including all versions of every file and folder. |
| Fork | A new repository that shares code and visibility settings with the original "upstream" repository. |
| Merge	| To take the changes from one branch and apply them to another. |
| Pull request | A request to merge changes from one branch into another. |
| Remote | A repository stored on GitHub, not on your computer. |
| Upstream | The branch on an original repository that has been forked or cloned. The corresponding branch on the cloned or forked repository is called the "downstream." |

### READMEs
A README communicates expectations for your project and helps you manage contributions. For more information, see [About READMEs](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-readmes). A README is a markdown file (.md extension), learn more about markdown [here](https://www.markdownguide.org/getting-started/).

At CCC, we use the README.md file to explain the purpose of a repository and give instructions for first-time users to run the application(s). They should include:
- **Project Name** as the title
- **Project description** to state the purpose
- **Important files** that you may need to run the code
- **Instructions to run** (e.g. *Clone repository and use the main task file. You may have to comment out the consent (line XYZ) to run the task locally.*)

### Repository Names
A repository name should explain what the application does or is named, using as few keywords as possible.

Some examples:
- `ccc-infra`
- `discourse-dinner-webpage`
- `coalesce`

#### Use all lowercase letters.
- :white_check_mark: `my-new-repository-class`
- :no_entry_sign: `My-New-Repository-Class`

#### Use hyphenated spaces.
- :white_check_mark: `twitter-survey-client-data`
- :no_entry_sign: `twitter_survey_client_data` or `twitterSurveyClientData`

#### Use versionless phrases.
If you find yourself wanting to version your repository name, you
probably are interested in [releasing tagged versions](https://docs.github.com/en/github/administering-a-repository/managing-releases-in-a-repository)
of the project instead.

- :white_check_mark: `amplification-analysis`
- :no_entry_sign: `amplification-analysis-10-02` or `amplification-analysis-v1`

### Branch Names
Within a repository, you will have a minimum of one _default_ branch. A default branch should be considered the _most stable_ branch, meaning the least likely to contain bugs, errors, badly-written code, etc. In GitHub, the `main` branch is the default branch.

We use additional branches to add features and update code, and then use pull requests to merge those branches with the default branch (main). Branche names should follow the same conventions as repositories and be descriptive and concise, ideally reflecting the work done on the branch. Note that at CCC we don't necessarily have production branches as defined below, but assume this is the `main` branch.

### Branch Prefixes
Using prefixes in branch names helps to quickly identify the purpose of the branches. Some common branch prefixes are below.

#### Feature Branches
These branches are used for developing new features. Use the prefix `feature/`. For instance, `feature/login-system`.

#### Bugfix Branches
These branches are used to fix bugs in the code. Use the prefix `bugfix/`. For example, `bugfix/header-styling`.

#### Hotfix Branches
These branches are made directly from the production branch to fix critical bugs in the production environment. Use the prefix `hotfix/`. For instance, `hotfix/critical-security-issue`.

#### Release Branches
These branches are used to prepare for a new production release. They allow for last-minute dotting of i’s and crossing t’s. Use the prefix `release/`. For example, `release/v1.0.1`.

#### Documentation Branches
These branches are used to write, update, or fix documentation eg. the README.md file. Use the prefix `docs/`. For instance, `docs/api-endpoints`.

### Commits
Every github commit should be prefixed with a type. A scope may be added after the prefix, such as `feat(api): ...`. A description should then follow the prefix after the colon. The description is a short summary of the code changes.

#### Types

- `build`: Changes that affect the build system or external dependencies (e.g., npm, Gradle).
- `chore`: Routine tasks or maintenance not related to production code (e.g., updating configs).
- `ci`: Changes to CI/CD configuration or scripts (e.g., GitHub Actions, CircleCI).
- `docs`: Documentation-only changes (e.g., README updates).
- `feat`: A new feature or significant enhancement.
- `fix`: A bug fix or patch.
- `perf`: Code changes that improve performance.
- `refactor`: Code restructuring without changing functionality (e.g., renaming, cleanup).
- `revert`: Reverts a previous commit.
- `style`: Code style changes (e.g., formatting, missing semicolons) without affecting code behavior.
- `test`: Adding or updating tests without modifying source code.
