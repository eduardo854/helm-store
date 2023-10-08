# helm-store
This repository was created with the purpose of serving as an illustrative example for my Medium article, "Building Your GitOps Pipeline with GitHub, Actions, DockerHub, and Helm Repository". Its primary role is to serve as a catalog of Helm charts.

The operational architecture is as follows:

```mermaid
flowchart TD;
    A1[repo A] -->|Commit| B;
    A2[repo B] -->|Commit| B;
    A3[repo C] -->|Commit| B;
    A4[repo D] -->|Commit| B;
    B[helm-store/pre-deployment] -->|Analyze commit messages <br> and submit the Helm chart <br> to the destination branch| C{Action}
    C --> D[helm-store/develop];
    C --> E[helm-store/stage];
    C --> F[helm-store/production];
```

Repository containing my posts on [MEDIUM](https://medium.com/@eduardo854).

To be notified every time a new post is published, **SUBSCRIBE [HERE](https://medium.com/@eduardo854/subscribe)**.
