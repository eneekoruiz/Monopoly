# Monopoly (Java Edition)

![Java](https://img.shields.io/badge/Java-1.8%2B-ED8B00?style=for-the-badge&logo=java&logoColor=white)
![Maven](https://img.shields.io/badge/Maven-Build_Tool-C71A36?style=for-the-badge&logo=apachemaven&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-CI%2FCD-2088FF?style=for-the-badge&logo=github-actions&logoColor=white)
![SonarCloud](https://img.shields.io/badge/SonarCloud-Quality_Gate-F3702A?style=for-the-badge&logo=sonarcloud&logoColor=white)

A fully functional implementation of the classic Monopoly board game built with Java. This project was developed as part of the **Software Engineering** course to apply object-oriented design patterns, automated testing, and modern Continuous Integration (CI) workflows.

## Core features

* **Complete Game Engine:** Implements core Monopoly mechanics including property purchasing, rent calculation, trading (`TradeDeal`), jail rules, and bankruptcy.
* **Graphical Interface:** Custom desktop UI built with Java Swing, featuring dynamic board rendering, player panels, and interactive dialogs for trading and actions.
* **Extensible Board System:** The game board is designed to be highly modular. It supports the full 40-cell standard board as well as custom/smaller configurations passed via command-line arguments.
* **Card Mechanics:** Implemented abstract chance and community chest deck systems that handle money modification and player relocation.

## Architecture & Code Quality

This repository places a heavy emphasis on software engineering best practices:

1. **Design Patterns:** Uses Singleton for the `GameMaster` (central controller), Strategy pattern for cell information formatting (`CellInfoFormatter`), and extensive use of interfaces and abstract classes (`Cell`, `Card`).
2. **Testing:** Comprehensive unit test suite using JUnit and Mock objects (`MockGUI`, test-fixture gameboards) to isolate and verify game logic independently of the graphical interface.
3. **CI/CD Pipeline:** Automated GitHub Actions workflows trigger on every push/PR to compile the code, run the test suite, and generate JaCoCo code coverage reports.
4. **Static Code Analysis:** Integrated with **SonarCloud** (`sonar-project.properties`) to maintain code quality, enforce style guidelines, and prevent technical debt.

## What I learned

Beyond writing complex Java logic, this project was my introduction to professional DevOps practices. I learned how to configure GitHub Actions workflows, manage dependencies with Maven wrappers, and use SonarCloud to analyze my codebase. It also challenged me to design a system with high cohesion and low coupling, separating the game state completely from the Swing GUI layer to allow for rigorous unit testing.
