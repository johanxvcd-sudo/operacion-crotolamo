graph TD
    classDef decision fill:#FFBF00,stroke:#333,stroke-width:2px,color:#000
    classDef path fill:#444,stroke:#FFBF00,color:#fff
    classDef final fill:#000,stroke:#fff,color:#fff

    Start("<b>MAYO 1941</b><br/>Plan Zhúkov-Timoshenko [3]") --> Choice1{"¿Atacar primero?<br/>[5]"}
    
    Choice1 -- SÍ --> SovBranch["<b>RELÁMPAGO ROJO</b><br/>Surge el fallo mecánico [7]"]
    SovBranch --> SovChoice{"¿Objetivo?"}
    SovChoice -- Petróleo --> End1(("<b>ÉXITO</b><br/>Colapso nazi 1942 [28]"))
    SovChoice -- Desgaste --> End2(("<b>FALLO</b><br/>Aniquilación soviética [6]"))

    Choice1 -- NO --> HistBranch["<b>BARBARROJA REAL</b><br/>Invasión el 22 de Junio [8]"]
    HistBranch --> Choice2{"¿Guderian ataca Moscú?<br/>[12]"}
    
    Choice2 -- SÍ --> UcroAlem["<b>MOSCÚ CAE</b><br/>Guerra eterna con Tankograd [15]"]
    Choice2 -- NO --> KievBranch["<b>KIEV (HISTÓRICO)</b><br/>Invierno sin ropa adecuada [30]"]
    
    KievBranch --> Choice3{"¿Decreto Barbarroja?<br/>[31]"}
    Choice3 -- RIGOR --> Resis["<b>RESISTENCIA</b><br/>Auge partisano [23]"]
    Choice3 -- LOGÍSTICA --> Mius["<b>ESTABILIDAD</b><br/>Frente del río Mius [29]"]

    Resis & Mius & UcroAlem --> Epilogue["<b>EPÍLOGO</b><br/>Mito de la Wehrmacht limpia [25]"]

    class Choice1,Choice2,Choice3 decision
    class End1,End2,Epilogue final
