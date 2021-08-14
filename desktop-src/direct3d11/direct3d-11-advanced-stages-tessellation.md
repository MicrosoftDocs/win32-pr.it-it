---
title: Fasi a tessellazione
description: Il runtime Direct3D 11 supporta tre nuove fasi che implementano la suddivisione a fasi, che converte le superfici di suddivisione a basso dettaglio in primitive con maggiore dettaglio nella GPU.
ms.assetid: 4ad2fd3e-6e1a-4326-8469-3198acf931dc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52d272ad1db53c6e70a856255c1826f4867f069897b42da0219cd334d48226d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118099233"
---
# <a name="tessellation-stages"></a>Fasi a tessellazione

Il runtime Direct3D 11 supporta tre nuove fasi che implementano la suddivisione a fasi, che converte le superfici di suddivisione a basso dettaglio in primitive con maggiore dettaglio nella GPU. Tessere a tessere (o scomposizioni) superfici di alto ordine in strutture idonee per il rendering.

Implementando la tessellazione nell'hardware, una pipeline grafica può valutare modelli di dettaglio inferiore (numero di poligoni inferiore) ed eseguire il rendering in modo più dettagliato. Sebbene sia possibile eseguire la tessellazione software, la tessellazione implementata dall'hardware può generare una quantità incredibile di dettagli visivi (incluso il supporto per il mapping dello spostamento) senza aggiungere il dettaglio visivo alle dimensioni del modello e paralizzando le frequenze di aggiornamento.

-   [Vantaggi a tessellazione](#tessellation-benefits)
-   [Nuove fasi della pipeline](#new-pipeline-stages)
    -   [Fase hull shader](#hull-shader-stage)
    -   [Fase del tessellatore](#tessellator-stage)
    -   [Fase domain shader](#domain-shader-stage)
-   [API per l'inizializzazione delle fasi di tessellazione](#apis-for-initializing-tessellation-stages)
-   [Procedura:](#how-tos)
-   [Argomenti correlati](#related-topics)

## <a name="tessellation-benefits"></a>Vantaggi della tessellazione

Mosaico:

-   Consente di risparmiare molta memoria e larghezza di banda, che consente a un'applicazione di eseguire il rendering di superfici più dettagliate da modelli a bassa risoluzione. La tecnica a tessellazione implementata nella pipeline Direct3D 11 supporta anche il mapping dello spostamento, che può produrre quantità straordinarie di dettagli della superficie.
-   Supporta tecniche di rendering scalabile, ad esempio livelli di dettaglio continui o dipendenti dalla visualizzazione, che possono essere calcolati in tempo reale.
-   Migliora le prestazioni eseguendo calcoli costosi a frequenza inferiore (eseguendo calcoli su un modello con un livello di dettaglio inferiore). Ciò potrebbe includere calcoli di fusione che usano forme di fusione o destinazioni di morphing per calcoli realistici di animazione o fisica per il rilevamento delle collisioni o la dinamica del corpo soft.

La pipeline Direct3D 11 implementa la tessellazione nell'hardware, che carica il lavoro dalla CPU alla GPU. Ciò può comportare miglioramenti delle prestazioni molto grandi se un'applicazione implementa un numero elevato di destinazioni di morphing e/o modelli di skinning/deformazioni più sofisticati. Per accedere alle nuove funzionalità a tessellazione, è necessario conoscere alcune nuove fasi della pipeline.

## <a name="new-pipeline-stages"></a>Nuove fasi della pipeline

La tessellazione usa la GPU per calcolare una superficie più dettagliata da una superficie costruita da patch quad, patch triangolo o isolinee. Per approssimare la superficie ordinata in alto, ogni patch viene suddivisa in triangoli, punti o linee usando fattori a tessellazione. La pipeline Direct3D 11 implementa la tessellazione usando tre nuove fasi della pipeline:

-   [Hull-Shader Stage](#hull-shader-stage) : fase dello shader programmabile che produce una patch geometrica (e costanti patch) che corrispondono a ogni patch di input (quad, triangolo o linea).
-   [Fase tessellatore:](#tessellator-stage) fase della pipeline di funzioni fisse che crea un modello di campionamento del dominio che rappresenta la patch geometrica e genera un set di oggetti più piccoli (triangoli, punti o linee) che connettono questi esempi.
-   [Fase domain-shader:](#domain-shader-stage) fase dello shader programmabile che calcola la posizione del vertice corrispondente a ogni campione di dominio.

Il diagramma seguente evidenzia le nuove fasi della pipeline Direct3D 11.

![diagramma della pipeline direct3d 11 che evidenzia le fasi hull-shader, tessellator e domain-shader](images/d3d11-pipeline-stages-tessellation.png)

Il diagramma seguente illustra la progressione attraverso le fasi a tessellazione. La progressione inizia con la superficie di suddivisione a basso dettaglio. La progressione successiva evidenzia la patch di input con la patch geometrica, gli esempi di dominio e i triangoli corrispondenti che connettono questi esempi. La progressione evidenzia infine i vertici che corrispondono a questi esempi.

![Diagramma della progressione a tessellazione](images/tess-prog.png)

### <a name="hull-shader-stage"></a>Hull-Shader fase

Uno hull shader, richiamato una volta per ogni patch, trasforma i punti di controllo di input che definiscono una superficie di basso ordine in punti di controllo che costituiscono una patch. Esegue anche alcuni calcoli per ogni patch per fornire i dati per la fase a tessellazione e la fase del dominio. Al livello più semplice della scatola nera, la fase hull-shader sarà simile al diagramma seguente.

![diagramma della fase hull-shader](images/d3d11-hull-shader.png)

Uno hull shader viene implementato con una funzione HLSL e ha le proprietà seguenti:

-   L'input dello shader è compreso tra 1 e 32 punti di controllo.
-   L'output dello shader è compreso tra 1 e 32 punti di controllo, indipendentemente dal numero di fattori a tessellazione. L'output dei punti di controllo da uno hull shader può essere utilizzato dalla fase domain-shader. I dati costanti delle patch possono essere utilizzati da uno shader di dominio. I fattori a tessellazione possono essere utilizzati dallo shader di dominio e dalla fase a tessellazione.
-   I fattori di suddivisione determinano quanto suddividere ogni patch.
-   Lo shader dichiara lo stato richiesto dalla fase del tessellatore. Sono incluse informazioni quali il numero di punti di controllo, il tipo di viso patch e il tipo di partizionamento da usare per la tessellatura. Queste informazioni vengono visualizzate come dichiarazioni in genere all'inizio del codice shader.
-   Se la fase hull-shader imposta un fattore a tessellazione del bordo su = 0 o NaN, la patch verrà culled. Di conseguenza, la fase a tessellatore può o meno essere eseguita, lo shader di dominio non verrà eseguito e non verrà prodotto alcun output visibile per la patch.

A un livello più profondo, uno hull-shader opera effettivamente in due fasi: una fase del punto di controllo e una fase patch-constant, che vengono eseguite in parallelo dall'hardware. Il compilatore HLSL estrae il parallelismo in uno hull shader e lo codifica in bytecode che guida l'hardware.

-   La fase del punto di controllo funziona una volta per ogni punto di controllo, leggendo i punti di controllo per una patch e generando un punto di controllo di output (identificato da controlPointID).
-   La fase patch-constant funziona una volta per ogni patch per generare fattori a tessellazione dei bordi e altre costanti per ogni patch. Internamente, molte fasi di patch costanti possono essere eseguite contemporaneamente. La fase patch-constant ha accesso in sola lettura a tutti i punti di controllo di input e output.

Ecco un esempio di hull shader:


```
[patchsize(12)]
[patchconstantfunc(MyPatchConstantFunc)]
MyOutPoint main(uint Id : SV_ControlPointID,
     InputPatch<MyInPoint, 12> InPts)
{
     MyOutPoint result;
     
     ...
     
     result = TransformControlPoint( InPts[Id] );

     return result;
}
```



Per un esempio che crea uno hull shader, vedere [Procedura: Creare uno hull shader.](direct3d-11-advanced-stages-hull-shader-create.md)

### <a name="tessellator-stage"></a>Fase del tessellatore

Il tessellatore è una fase a funzione fissa inizializzata associando uno hull shader alla pipeline (vedere [Procedura: Inizializzare la fase tessellator](direct3d-11-advanced-stages-tessellator-initialize.md)). Lo scopo della fase a tessellatore è suddividere un dominio (quad, tri o linea) in molti oggetti più piccoli (triangoli, punti o linee). Il tessellatore affianca un dominio canonico in un sistema di coordinate normalizzato (da zero a uno). Ad esempio, un dominio quad viene a tessellato in un quadrato di unità.

Il tessellatore opera una volta per ogni patch usando i fattori a tessellazione (che specificano la fine della tessellatura del dominio) e il tipo di partizionamento (che specifica l'algoritmo usato per suddividere una patch) che vengono passati dalla fase hull-shader. Il tessellatore restituisce le coordinate uv (e facoltativamente w) e la topologia della superficie alla fase domain-shader.

Internamente, il tessellatore opera in due fasi:

-   La prima fase elabora i fattori a tessellazione, risolvendo i problemi di arrotondamento, gestendo fattori molto piccoli, riducendo e combinando i fattori, usando l'aritmetica a virgola mobile a 32 bit.
-   La seconda fase genera elenchi di punti o topologia in base al tipo di partizionamento selezionato. Questa è l'attività principale della fase del tessellatore e usa frazioni a 16 bit con aritmetica a virgola fissa. L'aritmetica a virgola fissa consente l'accelerazione hardware mantenendo una precisione accettabile. Ad esempio, data una patch di 64 metri di larghezza, questa precisione può posizionare i punti a una risoluzione di 2 mm.



| Tipo di partizionamento | Intervallo                       |
|----------------------|-----------------------------|
| \_frazionaria dispari      | \[1...63\]                  |
| pari \_ frazionaria     | Intervallo TessFactor: \[ 2..64\] |
| numero intero              | Intervallo TessFactor: \[ 1..64\] |
| pow2                 | Intervallo TessFactor: \[ 1..64\] |



 

### <a name="domain-shader-stage"></a>Domain-Shader fase

Uno shader di dominio calcola la posizione del vertice di un punto suddiviso nella patch di output. Uno shader di dominio viene eseguito una volta per ogni punto di output della fase del tessellatore e ha accesso in sola lettura alle coordinate UV di output della fase a tessellatore, alla patch di output dello hull shader e alle costanti patch di output dello hull shader, come illustrato nel diagramma seguente.

![diagramma della fase domain-shader](images/d3d11-domain-shader.png)

Le proprietà dello shader di dominio includono:

-   Uno shader di dominio viene richiamato una volta per ogni coordinata di output dalla fase del tessellatore.
-   Uno shader di dominio usa i punti di controllo di output dalla fase hull-shader.
-   Uno shader di dominio restituisce la posizione di un vertice.
-   Gli input sono gli output dello hull shader, inclusi i punti di controllo, i dati costanti di patch e i fattori a tessellazione. I fattori a tessellazione possono includere i valori usati dal tessellatore di funzione fissa, nonché i valori non elaborati (ad esempio, prima dell'arrotondamento per interi), che facilitano la geomorfismo, ad esempio.

Al termine dello shader di dominio, la tessellazione viene completata e i dati della pipeline continuano alla fase successiva della pipeline (geometry shader, pixel shader e così via). Un geometry shader che prevede primitive con adizia (ad esempio, 6 vertici per triangolo) non è valido quando la tessellazione è attiva (ciò comporta un comportamento non definito, di cui il livello di debug si lamenterà).

Ecco un esempio di shader di dominio:


```
void main( out    MyDSOutput result, 
           float2 myInputUV : SV_DomainPoint, 
           MyDSInput DSInputs,
           OutputPatch<MyOutPoint, 12> ControlPts, 
           MyTessFactors tessFactors)
{
     ...

     result.Position = EvaluateSurfaceUV(ControlPoints, myInputUV);
}
```



## <a name="apis-for-initializing-tessellation-stages"></a>API per l'inizializzazione delle fasi di tessellazione

Il tessellamento viene implementato con due nuove fasi di shader programmabili: uno shader con scafo e uno shader di dominio. Queste nuove fasi dello shader vengono programmate con codice HLSL definito nel modello shader 5. Le nuove destinazioni dello shader sono: hs \_ 5 \_ 0 e ds \_ 5 \_ 0. Come tutte le fasi programmabili dello shader, il codice per l'hardware viene estratto dagli shader compilati passati al runtime quando gli shader sono associati alla pipeline usando API come [**DSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dssetshader) e [**HSSetShader.**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetshader) Ma prima di tutto, lo shader deve essere creato usando API come [**CreateHullShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createhullshader) [**e CreateDomainShader.**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdomainshader)

Abilitare la tessellazione creando uno shader con scafo e associarlo alla fase di hull shader (in questo modo viene impostata automaticamente la fase a tessellatore). Per generare le posizioni finali dei vertici dalle patch a fasi, è anche necessario creare uno shader di dominio e associarlo alla fase domain shader. Dopo aver abilitato la funzionalità a scheletro, l'input di dati nella fase dell'assembler di input deve essere patch dei dati. Ciò significa che la topologia dell'assembler di input deve essere una topologia costante patch da [**D3D11 \_ PRIMITIVE \_ TOPOLOGY**](/previous-versions/windows/desktop/legacy/ff476189(v=vs.85)) impostata [**con IASetPrimitiveTopology**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetprimitivetopology).

Per disabilitare la funzionalità a tessellazione, impostare lo hull shader e il domain shader su **NULL.** Né la fase geometry shader né la fase stream-output possono leggere i punti di controllo dell'output di hull shader o applicare patch ai dati.

-   Nuove topologie per la fase input-assembler, che sono estensioni di questa enumerazione.

    ```
    enum D3D11_PRIMITIVE_TOPOLOGY
    ```

    

    La topologia è impostata sulla fase input-assembler tramite [ **IASetPrimitiveTopology**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetprimitivetopology)

-   Naturalmente, le nuove fasi programmabili dello shader richiedono l'impostazione di altri stati, per associare buffer costanti, campioni e risorse shader alle fasi della pipeline appropriate. Questi nuovi metodi ID3D11Device vengono implementati per impostare questo stato.
    -   [**DSGetConstantBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dsgetconstantbuffers)
    -   [**DSGetSamplers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dsgetsamplers)
    -   [**DSGetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dsgetshader)
    -   [**DSGetShaderResources**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dsgetshaderresources)
    -   [**DSSetConstantBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dssetconstantbuffers)
    -   [**DSSetSamplers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dssetsamplers)
    -   [**DSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dssetshader)
    -   [**DSSetShaderResources**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dssetshaderresources)
    -   [**HSGetConstantBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hsgetconstantbuffers)
    -   [**HSGetShaderResources**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hsgetshaderresources)
    -   [**HSGetSamplers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hsgetsamplers)
    -   [**HSGetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hsgetshader)
    -   [**HSSetConstantBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetconstantbuffers)
    -   [**HSSetSamplers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetsamplers)
    -   [**HSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetshader)
    -   [**HSSetShaderResources**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetshaderresources)

## <a name="how-tos"></a>Procedura:

La documentazione contiene anche esempi per l'inizializzazione delle fasi a più fasi.



| Elemento                                                                                                                                                                                                                                                                                           | Descrizione                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="How_To__Create_a_Hull_Shader"></span><span id="how_to__create_a_hull_shader"></span><span id="HOW_TO__CREATE_A_HULL_SHADER"></span>[Procedura: Creare uno shader di tipo hull](direct3d-11-advanced-stages-hull-shader-create.md)<br/>                                                     | Creare uno shader con scafo.<br/>              |
| <span id="How_To__Design_a_Hull_Shader"></span><span id="how_to__design_a_hull_shader"></span><span id="HOW_TO__DESIGN_A_HULL_SHADER"></span>[Procedura: Progettare uno shader di tipo hull](direct3d-11-advanced-stages-hull-shader-design.md)<br/>                                                     | Progettare uno shader con scafo.<br/>              |
| <span id="How_To__Initialize_the_Tessellator_Stage"></span><span id="how_to__initialize_the_tessellator_stage"></span><span id="HOW_TO__INITIALIZE_THE_TESSELLATOR_STAGE"></span>[Procedura: Inizializzare la fase tessellator](direct3d-11-advanced-stages-tessellator-initialize.md)<br/> | Inizializzare la fase a tessellazione.<br/> |
| <span id="How_To__Create_a_Domain_Shader"></span><span id="how_to__create_a_domain_shader"></span><span id="HOW_TO__CREATE_A_DOMAIN_SHADER"></span>[Procedura: Creare uno shader di dominio](direct3d-11-advanced-stages-domain-shader-create.md)<br/>                                           | Creare uno shader di dominio.<br/>            |
| <span id="How_To__Design_a_Domain_Shader"></span><span id="how_to__design_a_domain_shader"></span><span id="HOW_TO__DESIGN_A_DOMAIN_SHADER"></span>[Procedura: Progettare uno shader di dominio](direct3d-11-advanced-stages-domain-shader-design.md)<br/>                                           | Creare uno shader di dominio.<br/>            |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Pipeline grafica](overviews-direct3d-11-graphics-pipeline.md)
</dt> </dl>

 

