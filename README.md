# mermaid-examples

Example 1
```mermaid
    pie title Market Share of Mobile OS
        "Android" : 71
        "iOS" : 27
        "Other" : 2
```
---
Example 2
```mermaid
    flowchart TD
    A[Enter a number] --> B{Is the number divisible by 3?}
    A[Enter a number] --> C{Is the number divisible by 5?}
    A[Enter a number] --> D{Is the number divisible by 3 and 5?}
        B --> |Yes| E[Print Buzz]
        B --> |No| F[Print Actual Number]
        C --> |Yes| G[Print Fizz]
        C --> |No| H[Print Actual Number]
        D --> |Yes| I[Print FizzBuzz]
        D --> |No| J[Print Actual Number]
```
---
Example 3
```mermaid
    flowchart LR
    A[Customer] -->|Orders coffee| B[Cashier]
    B --> |Inputs Order| C[Order System]
    C -->|Check if in stock| D[Stock System]
    D --> |Check inventory| E{Is in stock?}
    E --> |Yes - Request payment| F[Payment System]
    E --> |No - Inform customer| B[Cashier]
    F --> |Take payment from customer| A[Customer]
```
---
Example 4 (AEC Task 1)
```mermaid
    flowchart LR
    A[Product owner] -->|Logs in| B[Authentication System]
    B --> |Checks credentials| C{Are the credentials valid?}
    C -->|No| A[Product Owner]
    C -->|Yes| D[Front-End System]
    D --> E{Are you Product Owner?}
    E -->|Yes| F[Build Task Columns & Add configuration settings]
    E -->|No| G[Add task to board]
    F -->|Invite team members to board| B[Authentication System]
    G -->|Send task to database| H[Database]
    H -->|Selects task| I{Did the user make a change to the task?}
    I -->|Yes - Update database| H[Database]
    I -->|No - Assign team member to task| J[Member Assigned]
    J --> K{Has tasks status changed?}
    K -->|Yes| L[Status Updated]
    K -->|No| M[Status remains the same]
    L -->|Start the task| N{Is the task complete?}
    N -->|Yes - Update database| H[Database]
    N -->|No - Alert Product Owner| O[Send email to Product Owner]
```