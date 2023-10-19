# flow

```mermaid
graph TD
    A[Demo installation (upfront)]
    A1[App frontend / backend]
    A2[Redis Vector Database with customer documents preloaded]
    A3[TGIS Flan T5 model served]
    A4[Monitoring dashboard]
    A5[GitOps setup]

    B[Show architecture + working application (frontend + served model) on OpenShift]

    C[Following GitOps approach, deploy second model served using canary deployment]

    D[Show application frontend interacting with second served model]
    D1[Negative feedback on results]
    D2[Script to generate more feedback quickly]

    E[Show dashboard on monitoring feedback]
    F[Following GitOps approach, roll back canary deployment]

    A --> A1
    A --> A2
    A --> A3
    A --> A4
    A --> A5
    A --> B
    B --> C
    C --> D
    D --> D1
    D --> D2
    D --> E
    E --> F
```
