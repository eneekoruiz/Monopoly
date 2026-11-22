# Monopoly (Java Edition)

Java implementation of Monopoly with a Swing UI, automated testing, and CI.

## What it covers

- game engine and board logic
- property purchases, rent, jail, and bankruptcy rules
- Swing-based desktop interface
- JUnit tests and GitHub Actions
- SonarCloud integration

## Architecture

The Swing interface renders the board and forwards player actions to the game controller. Domain classes hold players, properties and rules, while turn progression and transactions are coordinated outside the view so rule checks can be tested independently.
