# benice - Password Strength Checker

<p align="center">
  <img src="images/logo.png" alt="logo benice" width="200"/>
</p>

## System Overview

`benice` is a standalone command-line interface (CLI) application written in Python that evaluates password strength based on five security criteria. The system assigns a numerical score to each password and classifies it into one of three strength categories: Weak, Medium, or Strong.

**Key Characteristics:**
* **Single-file implementation:** All logic is contained in `hello.py`.
* **No external dependencies:** Uses only the Python standard library.
* **Interactive CLI:** Prompts the user for password input and provides immediate feedback.
* **Score-based evaluation:** Starts at a score of 5 and decrements for each unmet criterion.

## Repository Structure

The repository follows a simple structure:

| Component      | File(s)                                                     | Purpose                                                      |
|----------------|-------------------------------------------------------------|--------------------------------------------------------------|
| Documentation  | `README.md`                                                 | Defines validation criteria, scoring, and classification.    |
| Implementation | `hello.py`                                                  | Contains all validation logic and CLI interaction.           |
| Visual Assets  | `images/logo.png`, `images/Weak.png`, `images/medium.png`, `images/Strong.png` | Branding and visual representations of password strength levels. |
| Legal          | `LICENSE`                                                   | MIT License terms.                                           |

## Password Validation Criteria

`benice` checks for the following criteria to determine password strength:

-   At least one uppercase letter (`A-Z`).
-   At least one lowercase letter (`a-z`).
-   At least one number (`0-9`).
-   At least one special symbol (`~?/{}[]"':;>.<,!@#$%^&*()_-+=\|`).
-   A minimum length of 6 characters.

## Scoring Algorithm

The program uses a scoring system to evaluate the password's strength. The initial score is 5. For each of the following conditions that is not met, the score is reduced by 1:

-   Password length is less than or equal to 5 characters.
-   No uppercase letters are found.
-   No lowercase letters are found.
-   No numbers are found.
-   No special symbols are found.

## Strength Classification

Based on the final score, the password strength is categorized into one of three levels:

-   **Weak:** Score of 2 or less.
    <p align="center">
        <img src="images/Weak.png" alt="weak password" width="500"/>
    </p>
-   **Medium:** Score of 3.
    <p align="center">
        <img src="images/medium.png" alt="medium password" width="500"/>
    </p>
-   **Strong:** Score of 4 or 5.
    <p align="center">
        <img src="images/Strong.png" alt="strong password" width="500"/>
    </p>

## Usage Guide

1.  Make sure you have Python installed on your system.
2.  Open your terminal or command prompt.
3.  Navigate to the directory where `hello.py` is located.
4.  Run the following command:

    ```bash
    python hello.py
    ```

5.  The program will prompt you to enter a password for evaluation.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
