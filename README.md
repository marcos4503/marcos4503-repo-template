# 📒 Steps to Run on New Repository Created

Congratulations on creating your new repository! To begin, ensure that this repository and this README.md file are open in your browser on the GitHub website.

Follow the steps below to ensure that the repository is 100% configured and formatted to the best repository standards.

- Click the Gear icon (⚙️) side to Container of **About**, on the right side of the layout.
  - In **Description**, set a description for the repository.
  - If this repository's project has a website, specify it in the **Website** field.
  - In the **Topics** section, enter tags that correspond to the repository's content. (for example: "forge", "windows", etc.)
  - If this project will have releases, leave the **Releases** box checked.
  - Uncheck the **Deployments** and **Packages** boxes, unless your repository actually needs one of them.
- Click on the (**⚙️ Settings**) tab, located at the top of the interface, usually next to (**📈 Insights**).
  - In **General**
    - In **Social Preview** Conteiner, provide a preview image. **Only if it's necessary** for your project.
    - In **Features**
      - Disable the **Wikis** box.
      - Enable the **Sponsorships** box. You will need to create a file called `FUNDING.yml` in `.github/FUNDING.yml` in your repository. If GitHub creates this file for you, copy the contents of file `FUNDING.yml` from another repository to this new file `FUNDING.yml` that you are creating.
      - Disable the **Projects** box.
  - In **Pages**
    - In **Branch**
      - If the repository needs to make a Static Website or Files publicly available, create a Branch called `gh-pages`. After that, in the Combo Box, select the newly created Branch `gh-pages`, select the root `/` of the Branch and click **Save**.
- Return to the repository's homepage. From now on, the steps must be performed on files inside the repository. It is recommended that you clone the repository to edit the files and their contents more efficiently.
- In **main** Branch
  - Create a folder called `.github`, if not exists. This section should contain files used exclusively for the repository, such as documentation images, workflows, templates, etc. Inside the `.github` folder:
    - Create a folder called `assets`. This folder should contain images, such as logos, icons, and other assets that are only used by the repository and are not necessarily part of the project.
      - Create a `.gitkeep` file.
    - Create a folder called `ISSUE_TEMPLATE`, if not exists. Here are the options that will appear when someone tries to create an **Issue**.
      - Create a `01_support_or_help_request.yml`. Copy the content from another repository.
      - Create a `02_bug_report.yml`. Copy the content from another repository.
      - Create a `03_feature_or_improve_request.yml`. Copy the content from another repository.
      - Create a `04_code_change_proposal.yml`. Copy the content from another repository.
      - Create a `05_docsreadme_change_proposal.yml`. Copy the content from another repository.
      - Create a `06_other.yml`. Copy the content from another repository.
      - Create a `config.yml`. Copy the content from another repository.
    - Create a `CONTRIBUTING.md` file. This file will be highlighted by GitHub when a user creates an **Issue** or **Pull Request**. Copy the content of the `CONTRIBUTING.md` file from another repository.
    - Make sure the `FUNDING.yml` file has been created. If it is empty or not configured, copy the contents of the `FUNDING.yml` file from another repository.
    - Create a `PULL_REQUEST_TEMPLATE.md` file. GitHub will use the contents of this file to populate the **Description** box when someone access the **Pull Request** creation page. Copy the content from another repository.
  - Create a file called `.gitignore` to ignore any files that don't need to be tracked by Git, such as framework builds, cache, etc.
  - Create a file `LICENSE`. Copy from another repository if necessary.

> [!NOTE]
> Every binary file resulting from compilation, whether distributable or a distributable archive, that is released with each new version of the project, must be placed on the **Releases** page of the repository.

# 🎋 Guidelines/Steps for Branches

This is a best practices guide for creating new Branches. To begin:

- For all Branches other than **main**, create a `README.md` at the root of the Branch, to redirect to Branch **main**. If you want, copy this file from another repository.
- For all Branches (except **gh-pages**), make sure they have a folder called `.github` and that this folder contains the files `CONTRIBUTING.md` and `PULL_REQUEST_TEMPLATE.md`, as well as the **main** Branch.
- Keep the same `.gitignore` file in all Branches. This prevents one Branch from accidentally considering/tracking a file ignored by another Branch, which can cause a mess, and also helps maintain consistency and predictability across Branches, while working on Local Repository.

ℹ️ For managing multiple Branches, it is recommended to install **Smart Branch Switch** in the Local Repository. This will help keep the work environment clean and organized, and will also provide alerts if anything is out of the ordinary, such as the absence of the files mentioned above. For more information about the **Smart Branch Switch**, click <a href="https://github.com/marcos4503/smart-branch-switch">here</a>.

### Also, for `gh-pages` Branch

At the root of this Branch, create a file called `.periodic_clean.md`. Copy it from another repository if you prefer. This file contains instructions to periodically reset the history of this Branch, to prevent it from unnecessarily bloating the repository due to old files it once contained. This bloating causes the repository to grow unnecessarily, which can be a nuisance when cloning the repository or keeping it on your computer.

### Also, for Source Code Branches

The names of these Source Code or Project Branches must follow the naming format:

- `source-<operational-system-or-platform>-<framework-or-technology>`

For example: **`source-1.20.1-forge`**, **`source-linux-javafx`**, **`source-web-vanilla.js`**, **`source-web-package.ts`**, **`source-game-modloader`** or **`source-any-unity`**.

# 🏆 The Last Step

Finally, create an `README.md` file on root of the **main** Branch. This file will be displayed by default by GitHub when someone accesses the GitHub site of this repository, working as the repository's Showcase or Land Page. Follow the patterns of other `README.md` of other repositories.
