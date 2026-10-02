# Hands on Machine Learning

A hands-on introduction to core machine learning techniques every data scientist should know. In the guided notebook you will scale features, tune model hyperparameters, and validate models with cross-validation on the Titanic dataset. In the exercise you then apply the full workflow yourself: fetch and join data from a database and build a classifier to predict heart disease.

## Learning Objectives

By the end of this repository, you should be able to:

- Follow the machine learning workflow from defining a goal to evaluating a model.
- Scale features with standardization and normalization, and explain when each helps.
- Validate models reliably using K-fold cross-validation.
- Tune hyperparameters with grid search and randomized search.
- Fetch and join data from a SQL database to assemble a training set.
- Apply the full workflow end to end to build a classifier on a new problem.

## Learning Path

> [!TIP]
> Start with the [**Machine Learning Workflow**](machine_learning_workflow.md) guide. It walks through every step of an ML project (define the goal, get the data, split, explore, model, evaluate) and gives you the map for what the notebooks practice.

The notebooks build on each other in order:

| File / Folder | Description |
|---|---|
| [**The Machine Learning Workflow**](machine_learning_workflow.md) | Step-by-step overview of an end-to-end ML project. Read this first. |
| [**1 - Scaling & Hyperparameter Tuning**](1_scaling_hyperparameter_tuning.ipynb) | Scale data two ways, tune hyperparameters with grid and randomized search, and introduce cross-validation. |
| [**2 - Exercise: Machine Learning**](2_exercise_machine_learning.ipynb) | Practice the workflow yourself on data pulled from a database. |

### Additional Folders and Files

| File / Folder | Description |
|---|---|
| [**Data**](data/) | Titanic datasets used across the notebooks. |
| [**Assets**](assets/) | Images used in the notebooks and the workflow guide. |
| [**Solutions**](solutions/) | Reference solutions. |
| [**.env.example**](.env.example) | Template for the database credentials. Copy to `.env` and fill in your values. |
| [**pyproject.toml**](pyproject.toml) | Project configuration and dependencies. |
| [**uv.lock**](uv.lock) | Dependency lock file. |

## Setup

> [!NOTE]
> Throughout these steps, text in angle brackets like `<repo-name>` is a **placeholder**. Replace it including the `< >` brackets with your own value. For example, `cd <repo-name>` becomes `cd ds-hands-on-ml`.

### 1. Create the Repository from the Template

Click **Use this template** on GitHub.

When creating the repository:

- Set yourself as the **Owner**
- Choose a repository name
- Disable **Include all branches**
- Click **Create repository**

> [!IMPORTANT]
> If you are working in pairs or groups, only **one person** should complete this step.

---

### 2. Add Collaborators (Pairs/Groups Only)

If working with teammates:

1. Open the repository on GitHub
2. Go to **Settings → Collaborators**
3. Add your teammates as collaborators
4. Share the repository link with your team

Teammates should accept the invitation before continuing.

---

### 3. Clone the Repository

Copy the SSH URL from the **Code** button on GitHub, then run:

```bash
git clone <copied-ssh-url>
```

The copied SSH URL will look like `git@github.com:<your-username>/<repo-name>.git`.

---

### 4. Move into the Project Folder and Install Dependencies

This installs all dependencies and creates a virtual environment in (`.venv/`).

```bash
cd <repo-name>
uv sync
```

---

### 5. Set Up the Database Connection

The exercise notebook reads its data from a Postgres database via a connection string. Copy the example file and fill in your own values:

```bash
cp .env.example .env
```

Then open `.env` and replace the placeholders with the values from your coaches.

> [!CAUTION]
> The `.env` file holds credentials and must never be committed. It is already listed in `.gitignore`. Only `.env.example`, with placeholders, belongs in the repo.

---

### 6. Open the Notebooks

> [!NOTE]
> Make sure you open VS Code from the project root so it automatically detects the environment created by `uv sync`.

Launch VS Code in the project root folder:

```bash
code .
```

Then open a notebook and select the Python environment created by `uv sync` as the kernel.

## References & Further Reading

- [**The Machine Learning Workflow**](machine_learning_workflow.md): The step-by-step guide in this repo, your starting point.
- [**Feature Engineering**](https://github.com/neuefische/ds-feature-engineering): Companion bootcamp repo to go deeper on feature engineering (imputation, encoding, binning, feature creation).
- [**Scikit-learn: Preprocessing data**](https://scikit-learn.org/stable/modules/preprocessing.html): Standardization, normalization, and other scaling methods.
- [**Scikit-learn: Cross-validation**](https://scikit-learn.org/stable/modules/cross_validation.html): Evaluating estimator performance and avoiding overfitting.
- [**Scikit-learn: Tuning hyperparameters**](https://scikit-learn.org/stable/modules/grid_search.html): Grid search, randomized search, and successive halving.