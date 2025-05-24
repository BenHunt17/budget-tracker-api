### Overview

This project is a REST API for managing users' personal finance data including tracking transactions, managing budgets and generating insights.
The focus of this project is on backend development and database persistence using Entity Framework Core and SQL Server. 
For the purpose of learning, this project does not include frontend development, authentication, or external banking integrations — these are treated as separate concerns.
I will develop this API with real world considerations in mind and make decisions as if I were developing a real world application, however, I will not be using external services as a production ready app is not the aim.
Any connection strings or keys will be stored in app settings locally, in a real world application these would be stored in a secure place such as Azure key vault

### Motivation

This project serves as a practical opportunity for me to learn Entity Framework Core and deepen my experience with SQL Server
I chose budgeting as the domain because of my interest in personal finance and it happens to lend itself well to backend logic and data modelling.

### Functional Requirements

- Ability for theoretical background services to persist user transactions including:
	- Amount
	- Currency
	- Timestamp
	- Recipient/sender
	- Other information needed to automate budget classification
- Support for user-defined budget plans which define timeframe and weightings/amounts for outgoing transactions based on their category.
- Ability for uses to define categorization rules based on recipient/sender, amount or references
- Ability for users to generate aggregated statistics over variable time periods to evaluate transactions against budget

### Extended features

- Create atomic warnings when recent transactions deviate from a user's budget.
	- When transactions of a certain category exceed the budget allowance
	- When transactions of a certain category fall far below budget expectations
	- When ingoing transactions don't cover total outgoings.
- Ability for users to export their budgets and transactions as a CSV