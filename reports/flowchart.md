graph TD
A[Load Data] --> B(Sanitize)
B --> C{Apply Dictionary?}
C -->|True| D[Apply Dictionary]
C -->|False| E[Featurize]
D --> E
E --> I{Load or Train?}
I -->|Load| J(Load Model)
I -->|Train| H(Train)
H --> G[Apply Model]
J --> G

