# GitFlow 
[Back to Etiquette](Etiquette.md)  
## Warning - Do not use! 
GitFlow introduces **rigid branching patterns** that can **slow down** modern CI/CD workflows, making it less ideal for fast-paced teams embracing trunk-based development or continuous deployment. 
  
Here's a example of GitFlow 
  
```mermaid 
graph TD 
    A[main] --> B[develop] 
    B --> C[feature/login] 
    C --> B 
    B --> D[feature/payment] 
    D --> B 
    B --> E[release/1.0.0] 
    E --> F[hotfix/login-bug] 
    F --> E 
    E --> A 
    E --> B 
    A --> G[tag v1.0.0] 
