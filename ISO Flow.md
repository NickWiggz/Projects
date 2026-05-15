flowchart LR
    %% Swimlanes
    subgraph INV[Investigator]
        A1[Gather Evidence]
        A2[Conduct Initial Interviews]
        A3[Analyze Evidence]
        A4[Recall Interviews as Needed]
        A5[Import Transcripts into TextMap]
        A6[Validate Transcriptions]
        A7[Subject Interview]
        A8[Repeat Loop Until Complete]
    end

    subgraph LEAD[ISO Leadership / OGC / Supervisor]
        B1[Pre-Subject Roundtable]
        B2[Post-Subject Roundtable]
    end

    subgraph VEND[Transcription Vendor]
        C1[Transcribe Audio/Testimony]
    end

    %% Flows
    A1 --> A2 --> A3 --> A4 --> C1 --> A5 --> A6
    A6 --> B1 --> A7 --> B2 --> A8
    A8 -->|If needed| A4
    A8 -->|If complete| Z[End: Validated Transcripts Ready for ROI Drafting]
