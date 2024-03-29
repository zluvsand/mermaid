# Mermaid chart examples

## Flow chart
```mermaid
flowchart LR
    ItemA-->ItemB-->ItemC
```

```mermaid
graph TB
    A[ItemA]-->B[ItemB]-->C[ItemC]
    A-->C
    D[ItemD]==>C
    E[ItemE]-->F[ItemF]-->G[ItemG]
```

## State diagram
```mermaid
stateDiagram
    [*] --> StateA
    StateA --> [*]

    StateA --> StateB
    StateB --> StateA
    StateB --> StateD
    StateD --> [*]
```

## Sequence chart
```mermaid
sequenceDiagram
    ParticipantA-->>ParticipantA: Dotted rounded arrow
    ParticipantA->>ParticipantB: Dotted line arrow
    Note left of ParticipantA: NOTE
    ParticipantA-->>ParticipantC: Line arrow
    ParticipantB-->ParticipantC: Dotted line
    loop
        ParticipantA->>ParticipantB: Loop text
    end
```

### Use alias and autonumber

```mermaid
sequenceDiagram
    autonumber
    participant A as ParticipantA
    participant B as ParticipantB
    participant C as ParticipantC
    A-->>A: Dotted rounded arrow
    A-->>B: Dotted line arrow
    Note left of A: NOTE
    A->>C: Line arrow
    B-->C: Dotted line
    loop
        A->>B: Loop text
    end
```

## Enterprise relationship diagram
```mermaid
erDiagram
    Item1 ||--o{ Item2: text1
    Item2 ||--|{ Item3: text2
    Item1 }|..|{ Item4: text3
    Item4 }o--o{ Item4: text3
```

## Class chart
```mermaid
classDiagram
    SuperClass <|-- SubclassA
    SuperClass <|-- SubclassB
    SuperClass : +int attribute1
    SuperClass : +str attribute2
    SuperClass: +method1()
    SuperClass: +method2()
    class SubclassA{
        +str attribute2A
        +method1A()
        +method2A()
      }
    class SubclassB{
        +int attribute1B
        +method1B()
      }
```

## Timeline
```mermaid
timeline
    title Timeline title
    2015: EventA
        : EventB
    2020: EventC
    2025: EventD
        : EventE
        : EventF
```

## Gantt chart
```mermaid
gantt 
    title Gantt chart 1
    dateFormat YYYY-MM-DD
    axisFormat %b %d
    section Section A
        Task A1: a1, 2024-04-15, 7d
        Task A2: after a1, 5d
    section Section B
        Task B1: 2024-04-22, 2024-05-02
        Task B2: 2024-04-29, 5d
```

```mermaid
gantt 
    title Gantt chart 2
    dateFormat YYYY-MM-DD
    axisFormat %b %d
    excludes weekends 2024-04-25
    section Section A
        Task A1: done, a1, 2024-04-15, 7d
        Task A2: active, after a1, 5d
    section Section B
        Task B1: active, 2024-04-22, 2024-05-02
        Task B2: 2024-04-29, 5d
```

## Journey map
```mermaid
journey
    title Journey 1
    section Section A
        Activity 1A: 5: Person1
        Activity 2A: 3: Person2
        Activity 3A: 2: Person1, Person2
    section Section B
        Activity 1B: 4: Person2
        Activity 1B: 5: Person1
```

## Pie chart
```mermaid
pie title Pie chart 1
    "Category A" : 0.5
    "Category B" : 0.2
    "Category C" : 0.3
```

```mermaid
pie title Pie chart 2
    "Category A" : 2000
    "Category B" : 500
    "Category C" : 1000
```
## Sankey chart
```mermaid
sankey-beta

Category L1, Category R1, 5
Category L1, Category R2, 10
Category L2, Category R1, 15
Category L2, Category R3, 8
Category L3, Category R3, 20
```

## Quadrant chart
```mermaid
quadrantChart
    title Quadrant chart
    x-axis Left x --> Right x
    y-axis Bottom y --> Top y
    quadrant-1 Quadrant A
    quadrant-2 Quadrant B
    quadrant-3 Quadrant C
    quadrant-4 Quadrant D
    Point A: [0.3, 0.6]
    Point B: [0.4, 0.2]
    Point C: [0.6, 0.8]
    Point D: [0.8, 0.3]
    Point E: [0.2, 0.3]
    Point F: [0.5, 0.7]
```

## Distribution chart
```mermaid
xychart-beta
    title "Distribution chart title"
    x-axis [Jan, Feb, Mar, Apr, May, Jun]
    y-axis "Y variable" 0 --> 100
    bar [50, 60, 75, 82, 75, 40]
    line [50, 45, 75, 82, 65, 55]
```

## Mindmap
```mermaid
mindmap
root((Center node))
    Node1
        Node1A
        Node1B
        Node1C
    Node2
        Node2A
        Node2B
            Node2B1
            Node2B2
    Node3
        Node3A
        Node3B
    Node4
        Node4A
            Node4A1    
```