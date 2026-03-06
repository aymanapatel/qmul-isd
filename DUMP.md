


# Flowchart


## 1


```mermaid
flowchart LR
    subgraph Stage1 ["<span style='white-space: nowrap; color: black;'>1. At the Lab Bench (Doing the Experiment)</span>"]
        direction LR
        Login([👤 Quick PIN/Session Login]) --> Experiment(📋 Open Experiment)
        Experiment --> Step{Current Step}
        Step -->|Type/Tap| Note[📝 Log Observation]
        Step -->|Camera| Photo[📸 Capture Setup Photo]
        Step -->|Check| Done[✅ Mark Complete]
        
        Note -.-> Step
        Photo -.-> Step
        Done --> Next{More Steps?}
        Next -->|Yes| Step
        Next -->|No| EndStage1([Finish Bench Work])
    end
    
    style Stage1 fill:#f9f2ec,stroke:#d9b38c,stroke-width:2px,color:#000000
    linkStyle default stroke:#000000,stroke-width:1.5px,color:#ffffff
    classDef edgeLabel color:#ffffff,background-color:#000000
```


## 2


```mermaid
flowchart LR
    subgraph Stage2 ["<span style='color:black'>2. Post-Lab Desk Work (Tidying Up)</span><br><br>"]
        direction LR
        TL[ ] --- TR[ ]
        Desk([💻 Open Web/Desktop App]) --> Sync(🔄 View Auto-Synced Data)
        Sync --> Detail(✍️ Add Detailed Analysis)
        Detail --> EndStage2([Data Finalized])
        BL[ ] --- BR[ ]
    end
    style Stage2 fill:#e6f2ff,stroke:#99ccff,stroke-width:2px,color:#000000
    style TL fill:none,stroke:none
    style TR fill:none,stroke:none
    style BL fill:none,stroke:none
    style BR fill:none,stroke:none
    linkStyle 1 stroke:#000000,color:#000000
    linkStyle 2 stroke:#000000,color:#000000
    linkStyle 3 stroke:#000000,color:#000000
```



## 3.

```mermaid
flowchart LR

subgraph Stage3 ["<span style='color:black'>3. Supervisory Meeting (Sharing)</span><br><br>"]

direction LR

TL[ ] --- TR[ ]

Share([📤 Generate Shareable View]) --> Meet(🤝 Review with Supervisor)

Meet --> EndStage3([Feedback & Next Steps])

BL[ ] --- BR[ ]

end

style Stage3 fill:#e6ffe6,stroke:#99ff99,stroke-width:2px,color:#000000

style TL fill:none,stroke:none

style TR fill:none,stroke:none

style BL fill:none,stroke:none

style BR fill:none,stroke:none

linkStyle 1 stroke:#000000,color:#000000

linkStyle 2 stroke:#000000,color:#000000
```



# State diageeam


```mermaid
stateDiagram-v2

[*] --> DeviceIdle: Device Powered On

  

DeviceIdle --> ActiveSession: Enter PIN / Authenticate

state ActiveSession {

[*] --> Dashboard: Load User Data

Dashboard --> ProtocolSelected: Tap Experiment

ProtocolSelected --> Dashboard: Cancel / Back

ProtocolSelected --> StepActive: Start / Resume

state StepActive {

[*] --> ViewingStep

ViewingStep --> EnteringData: Tap "Log Note"

EnteringData --> ViewingStep: Save / Cancel Note

ViewingStep --> CapturingMedia: Tap "Camera"

CapturingMedia --> ViewingStep: Save / Retake Photo

}

StepActive --> StepCheck: Mark Step Complete

StepCheck --> StepActive: Steps Remain

StepCheck --> ProtocolCompleted: Final Step

ProtocolCompleted --> Dashboard: Close Protocol

}

ActiveSession --> SessionCompleted: Automatic Logout

%% Interruption and Security States

ActiveSession --> DeviceIdle: Logout
```



# Storyboard

Here are the updated three storyboards:

---

**Storyboard 1: The Agony**

_Scene 1_ — Tom arrives at the lab at 6:40 AM. Benches are packed, equipment crowding every surface. He pulls out his paper notebook and uncaps his pen.

_Scene 2_ — Mid-experiment, a timer goes off. Tom is switching between two setups. A teammate calls out an observation. He scribbles frantically in the margin, the notes already messy and hard to follow.

_Scene 3_ — Another timer. Tom is now balancing his notebook awkwardly against the bench, trying to jot something down mid-step. A few details slip by unrecorded. He tells himself he'll remember them later.

_Scene 4_ — End of the day. Tom sits on campus, laptop open, notebook beside him. He stares at a page of chaotic scrawls and half-finished diagrams, trying to reconstruct what happened and in what order. He can't.

_Scene 5_ — It's Tuesday. Tom checks his phone — football starts soon. He's still typing, transferring notes. His backpack is stuffed with multiple notebooks and a laptop. His friends are already at the pitch waiting.

_Scene 6_ — Tom finally closes his laptop and heads out, late again. On the walk over, he wonders if there's a better way. He knows his method is barely holding together, and his PhD has only just begun.

---

**Storyboard 2: The Solution — Taking Notes**

_Scene 1_ — Tom is at the bench, mid-experiment. Instead of reaching for his notebook, he taps a few quick inputs on a nearby tablet. Minimal disruption. The entry is timestamped automatically.

_Scene 2_ — A teammate flags an unexpected observation. Tom taps to add a note and tags his colleague. The shared log updates for both of them instantly. No scribbled margins, no missed details.

_Scene 3_ — An alarm goes off mid-run. Tom pauses the current experiment on the tablet, switches to his second setup, and the screen shows exactly where he left off. He resumes without missing a beat.

_Scene 4_ — Tom photographs a result directly through the tablet. The image links automatically to the relevant step in his log. No loose phone photos, no disconnected files.

_Scene 5_ — End of day. Tom closes the tablet. There is nothing to retype. His record is already clean, ordered, and searchable. He picks up his bag — just his bag — and heads to the gym.

_Scene 6_ — It's Tuesday. Tom zips up his bag with only his tablet inside. He's out the door on time. His friends see him walk onto the pitch without a stack of notebooks in tow.

---

**Storyboard 3: Meeting the Supervisor**

_Scene 1_ — Wednesday evening. Instead of spending hours reformatting notes, Tom opens the app and taps export. A clean, readable summary generates in seconds. He emails it to Professor Fowler and closes his laptop.

_Scene 2_ — Thursday morning. Tom walks into the bi-weekly meeting relaxed. He's not anxious about whether his notes will make sense to someone else.

_Scene 3_ — Professor Fowler opens the shared document on his screen. The entries are clear, timestamped, and organised by experiment. He scrolls through without squinting. This is a far cry from the chaotic notebook that once left him astonished.

_Scene 4_ — Professor Fowler asks a specific question about a result from two weeks ago. Tom searches for it in seconds and pulls it up on the spot.

_Scene 5_ — They spend the rest of the meeting actually discussing the science, not deciphering handwriting or reconstructing timelines. Professor Fowler is visibly more engaged.

_Scene 6_ — The meeting wraps up early. Tom heads out with a clear list of next steps. No confusion, no follow-up emails to clarify what a note meant. Just progress.