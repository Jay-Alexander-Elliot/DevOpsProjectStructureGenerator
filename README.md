# Enhanced Directory Builder for DevOps Projects

This script automates the creation and initialization of a directory structure for DevOps projects. It creates directories based on configurations defined in a YAML file, initializes git repositories, and populates them with placeholder files.

## Features

- **Dynamic Directory Structure**: Creates a directory structure based on the categories and tools defined in the configuration file.
- **Git Initialization**: Initializes a git repository in each directory if it doesn't already exist.
- **Placeholder Files**: Creates placeholder files like `README.md`, `.gitignore`, and `placeholder.txt` from templates.
- **Logging**: Logs all actions to a log file to keep track of operations and changes.
- **Cleanup Mode**: Provides a cleanup option to remove directories created by the script.

## Prerequisites

- Bash shell
- `yq` command-line tool for processing YAML files. Make sure to install it before running the script. See [yq GitHub page](https://github.com/mikefarah/yq) for installation instructions.
- Git must be installed and accessible from the command line.

## Configuration

- **Config File**: The script expects a `config.yaml` file in the same directory as the script. This file should define the categories and tools for which directories are to be created.
- **Template File**: A `templates.yaml` file should also be present in the same directory as the script. This file should contain the content for placeholder files.

## Usage

1. Ensure all prerequisites are installed and accessible.
2. Place your `config.yaml` and `templates.yaml` files in the same directory as the script.
3. Run the script:

   ***bash
   ./directory_builder.sh [options]
   ***

   Options:
   - `--clean`: Cleans up the directories created by the script.

## Logs

The script logs its operations in the `directory-builder.log` file in the same directory as the script.

## Structure of `config.yaml`

The `config.yaml` file should have the following structure:

```yaml
categories:
  category1:
    - tool1
    - tool2
  category2:
    - tool3
    ```

This defines two categories (category1 and category2) and the tools under each category.

```

### Structure of templates.yaml

The ###templates.yaml### file should define the content for each placeholder file:
`templates:
  README.md: |
    # Project Name
    Description here
  .gitignore: |
    *.log
    bin/
  placeholder.txt: |
    This is a placeholder file.`

This defines the content for `README.md`, `.gitignore`, and `placeholder.txt`.

### Important Notes
The script will stop execution if it encounters any errors (e.g., missing configuration file, failed directory creation).
Make sure to review and test the script in a controlled environment before using it in production.
### Contribution
Contributions to enhance the script's functionality or fix bugs are welcome. Please ensure to follow the best coding practices and thoroughly test any changes.


### Notes:
- The `README.md` file explains the script's functionality, usage, and configuration file structures in a clear and user-friendly manner.
- It includes sections for features, prerequisites, configuration, usage, logs, and a note on contributions.
- Remember to replace placeholders like `Project Name` and `Description here` in the `templates.yaml` structure with actual content relevant to your project.
- Ensure to test the instructions and the script in a safe environment to validate their correctness before publishing or sharing.

