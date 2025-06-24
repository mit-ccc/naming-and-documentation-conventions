# GitHub Onboarding

<!-- toc -->

- [GitHub Onboarding](#github-onboarding)
  - [Git](#git)
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
  - [Pull Requests](#pull-requests)
    - [Keep it small and focused.](#keep-it-small-and-focused)
    - [Create a meaningful title.](#create-a-meaningful-title)
    - [Provide context and guidance.](#provide-context-and-guidance)
    - [Review your own pull request first.](#review-your-own-pull-request-first)
    - [Go back and remove noise.](#go-back-and-remove-noise)
    - [Assign reviewers.](#assign-reviewers)
    - [Acknowledge each and every comment.](#acknowledge-each-and-every-comment)
    - [Don't take comments personally.](#dont-take-comments-personally)
    - [Don't merge until everyone approves.](#dont-merge-until-everyone-approves)
  - [Code Reviews](#code-reviews)
    - [Review in a timely manner.](#review-in-a-timely-manner)
    - [Take your time.](#take-your-time)
    - [Read the title and description.](#read-the-title-and-description)
    - [Make only necessary comments.](#make-only-necessary-comments)
    - [Keep your tone of voice even.](#keep-your-tone-of-voice-even)
    - [Avoid “you".](#avoid-you)
    - [Use a checklist.](#use-a-checklist)

<!-- tocstop -->

## Git
Git is a version control system that makes it easy to work collaboratively on code and track changes. Learn more about Git [here](https://docs.github.com/en/get-started/using-git/about-git). GitHub is how we use Git to work collaboratively. Below you'll find best practices on its use.

## Repository Terminology

| Term	| Definition |
| ----- | ---------- |
| Branch | A parallel version of your code that is contained within the repository, but does not affect the primary or main branch. |
| Clone	| To download a full copy of a repository's data from GitHub.com, including all versions of every file and folder. |
| Fork | A new repository that shares code and visibility settings with the original "upstream" repository. |
| Merge	| To take the changes from one branch and apply them to another. |
| Pull request | A request to merge changes from one branch into another. |
| Remote | A repository stored on GitHub, not on your computer. |
| Upstream | The branch on an original repository that has been forked or cloned. The corresponding branch on the cloned or forked repository is called the "downstream." |

## READMEs
A README communicates expectations for your project and helps you manage contributions. For more information, see [About READMEs](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-readmes). A README is a markdown file (.md extension), learn more about markdown [here](https://www.markdownguide.org/getting-started/).

At CCC, we use the README.md file to explain the purpose of a repository and give instructions for first-time users to run the application(s). They should include:
- **Project Name** as the title
- **Project description** to state the purpose
- **Important files** that you may need to run the code
- **Instructions to run** (e.g. *Clone repository and use the main task file. You may have to comment out the consent (line XYZ) to run the task locally.*)

## Repository Names
A repository name should explain what the application does or is named, using as few keywords as possible.

Some examples:
- `ccc-infra`
- `discourse-dinner-webpage`
- `coalesce`

### Use all lowercase letters.
- :white_check_mark: `my-new-repository-class`
- :no_entry_sign: `My-New-Repository-Class`

### Use hyphenated spaces.
- :white_check_mark: `twitter-survey-client-data`
- :no_entry_sign: `twitter_survey_client_data` or `twitterSurveyClientData`

### Use versionless phrases.
If you find yourself wanting to version your repository name, you
probably are interested in [releasing tagged versions](https://docs.github.com/en/github/administering-a-repository/managing-releases-in-a-repository)
of the project instead.

- :white_check_mark: `amplification-analysis`
- :no_entry_sign: `amplification-analysis-10-02` or `amplification-analysis-v1`

## Branch Names
Within a repository, you will have a minimum of one _default_ branch. A default branch should be considered the _most stable_ branch, meaning the least likely to contain bugs, errors, badly-written code, etc. In GitHub, the `main` branch is the default branch.

We use additional branches to add features and update code, and then use pull requests to merge those branches with the default branch (main). Branch names should follow the same conventions as repositories and be descriptive and concise, ideally reflecting the work done on the branch. Note that at CCC we don't necessarily have production branches as defined below, but assume this is the `main` branch.

*Recommendation: commit early and push often!*

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

## Commits
Every github commit should be prefixed with a type. A scope may be added after the prefix, such as `feat(api): ...`. A description should then follow the prefix after the colon. The description is a short summary of the code changes and should be written in the imperative mood (as a directive, e.g. "use the imperative mood").

### Types

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

## Pull Requests
To update code, create a new branch from the `main` branch using the above guidelines for naming your branch. Once edits are made, commit them using the above guidelines, and then **create a pull request**. A pull request (PR) is how we merge new code into the default branch. These serve to help review code before it goes into production and keep a well-documented log of changes.

### Keep it small and focused.
Create a pull request for a *single feature*. This makes code reviews much easier and maintains a clear history of changes. If your PR is over 400 lines of code, think on it. Does it really need to be a single PR or can you break it up?

### Create a meaningful title.
Make the title short and meaningful. The thought process is similar to naming branches. Be consistent.

### Provide context and guidance.
Treat the PR as documentation. Write a clear description so that reviewers can quickly understand what the pull request does. In the pull request body, include:

- The purpose of the pull request
- An overview of what changed
- Links to any additional context such as tracking issues or previous conversations
- Questions or notes for reviewers

### Review your own pull request first.
Review, build, and test your own pull request before submitting it. This will allow you to catch errors or typos that you may have missed, before others start reviewing. Some repositories may also have tests that automatically run on pull requests. Make sure these are passing before assigning a reviewer.

### Go back and remove noise.
Often while self reviewing, you come across a file with only white space changes, formatting changes, optimized imports or some text change that has no impact related to the intention of the PR. Make the effort, go back to your branch and revert these files to how they were before; it doesn’t matter that you have slightly improved them, functionally they are the same, and the extra file in the list of ‘changed files’ listed in the PR lowers a reviewer's motivation to do a proper review, especially on larger PRs.

If formatting is important, create a separate PR, introduce a linter, make it a part of your CI, and format the entire app in one big nasty PR; but keep noise away from the important changes. Respect your reviewers’ time and energy.

### Assign reviewers.
Every pull request should have at a minimum one reviewer. Feel free to request additional reviews of everyone who may need to be informed of the changes. Since many of us use our personal email for GitHub, ping reviewers to let them know you've requested their review on a PR.

### Acknowledge each and every comment.
With any remote and asynchronous communication, it’s important to communicate that you have at least seen a comment that was meant for you. It might be with a simple emoji reaction or you may resolve the comment once it's addressed.

### Don't take comments personally.
Be mindful of how you interpret comments — chances are someone didn’t mean to be an asshole, they just weren’t thinking, were in a rush, English is their second language, or they got distracted. Assume that people have good intentions.

### Don't merge until everyone approves.
Wait until everyone who has made a suggestion has had a chance to see your response and evaluate it. If you have been waiting for a relatively long time, gently ping them (email, Slack, tap on shoulder) and let them know you’re waiting.

## Code Reviews
*Recommendation: if you have two clones of a project on your computer at any one time, one can be for normal work, one for reviewing PRs. This way, you can put your current task on pause with zero overhead.*

### Review in a timely manner.
Ideally, review the same day the PR comes your way. If it's later in the day, you're deep in some other work, or have a deadline, then get to the PR the following day. If you're going to take more than 2 business days, let the author know so they can get feedback from someone else if the delay is too long.

### Take your time.
It can be tempting to rush through a code review, but this is an essential step in the process. Dedicate time to reviewing code thoroughly. However, if you're reviewing for more than 60 minutes, take a break! When people engage in any activity requiring concentrated effort over a period of time, performance starts dropping off after about 60 minutes. 

### Read the title and description.
If someone has put the effort in to write a guide to their PR, the least you can do is take the time to read. So read the PR title and description to prime your expectations for what you are about to review.

### Make only necessary comments.
The hardest thing about making comments is resisting the urge to make comments. The key to restraint is to be as hard on yourself as you are about to be on others. If you ever wonder how effective you are as a reviewer, go back through all of your comments and measure how many of your comments result in your suggestion being well received and implemented with minimal back and forth.

That being said, definitely ask questions about any part of the code you may not understand!

### Keep your tone of voice even.
To create a pull request is, by definition, to invite criticism. So first and foremost: be critical. Poke, prod and challenge — but do so professionally, not personally. Be kind, feel free to use relevant emojis, and think about throwing in some positive comments as well.

### Avoid “you".
Try “we” or the passive tense instead.

Bad: ❌ “you forgot a variable here”

Good: ✅ “We are missing a variable here”

Good: ✅ “There is a variable missing here: [code block]”

### Use a checklist.
The following are typical of any given code review at CCC:

1. <ins>Functionality</ins>: Verify that the code implements the intended functionality and meets the specified requirements. Ensure that edge cases and possible error scenarios are handled appropriately and there are no bugs.
2. <ins>Readability and Maintainability</ins>: Check that the code is well-organized, easy to read, and follows established coding conventions. This includes proper indentation, consistent naming conventions, and appropriate use of comments to explain complex or non-obvious code segments.
3. <ins>Code Structure and Design</ins>: Evaluate whether the code is modular, and adheres to established design patterns and architectural guidelines.
4. <ins>Code Reuse and Dependencies</ins>: Review the code for proper reuse of existing libraries, frameworks, or components, and ensure that any dependencies are managed correctly and up-to-date.
5. <ins>Compliance with Coding Standards</ins>: Make sure that the code complies with any company or project-specific coding standards or guidelines.
6. <ins>Documentation</ins>: Confirm that the code includes sufficient documentation, such as inline comments, function or method descriptions, and high-level documentation for complex modules or components.

The following are typical on production software engineering teams, but may be overlooked when prototyping:

7. <ins>Error Handling and Logging</ins>: Ensure that the code includes proper error handling and logging mechanisms to help with debugging and troubleshooting.
8. <ins>Test Coverage</ins>: Check that the code includes appropriate unit tests or integration tests, and that the tests cover essential functionality and edge cases. Ensure that the tests are passing and up-to-date.
9. <ins>Security</ins>: Verify that the code follows secure coding practices and does not introduce any security vulnerabilities, such as SQL injections, cross-site scripting, or improper access controls.
10. <ins>Performance and Efficiency</ins>: Review the code for potential performance bottlenecks or inefficiencies, such as unnecessary loops, memory leaks, or suboptimal algorithms.