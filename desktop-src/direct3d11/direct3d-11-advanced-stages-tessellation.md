---
title: Fasi a mosaico
description: Il runtime di Direct3D 11 supporta tre nuove fasi che implementano lo schema a mosaico, che converte le aree di sottodivisione con dettagli più bassi in primitive di dettaglio nella GPU.
ms.assetid: 4ad2fd3e-6e1a-4326-8469-3198acf931dc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3aacb48ccc2c95ab93ba4f34212e654880d9a369
ms.sourcegitcommit: 4e4f9e7c90d25af0774deec1d44bd49fa9b6daa9
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2020
ms.locfileid: "104339511"
---
# <a name="tessellation-stages"></a>Fasi a mosaico

Il runtime di Direct3D 11 supporta tre nuove fasi che implementano lo schema a mosaico, che converte le aree di sottodivisione con dettagli più bassi in primitive di dettaglio nella GPU. Tessere a mosaico (o suddividere) superfici di ordine superiore in strutture appropriate per il rendering.

Implementando la suddivisione a mosaico nell'hardware, una pipeline grafica può valutare i modelli più bassi (conteggio poligono inferiore) ed eseguire il rendering in modo più dettagliato. Sebbene sia possibile eseguire lo mosaico del software, la suddivisione in mosaico implementata dall'hardware può generare una notevole quantità di dettagli visivi (incluso il supporto per il mapping di spostamento) senza aggiungere i dettagli visivi alle dimensioni del modello e alle frequenze di aggiornamento paralizzanti.

-   [Vantaggi a mosaico](#tessellation-benefits)
-   [Nuove fasi della pipeline](#new-pipeline-stages)
    -   [Fase Hull shader](#hull-shader-stage)
    -   [Fase mosaico](#tessellator-stage)
    -   [Fase Domain-shader](#domain-shader-stage)
-   [API per l'inizializzazione di fasi mosaico](#apis-for-initializing-tessellation-stages)
-   [Procedura:](#how-tos)
-   [Argomenti correlati](#related-topics)

## <a name="tessellation-benefits"></a>Vantaggi a mosaico

Tassellatura

-   Salva una grande quantità di memoria e larghezza di banda, che consente a un'applicazione di eseguire il rendering di superfici dettagliate più dettagliate da modelli a bassa risoluzione. La tecnica di suddivisione a mosaico implementata nella pipeline di Direct3D 11 supporta anche il mapping di spostamento, che può produrre quantità eccezionali di dettagli della superficie.
-   Supporta le tecniche di rendering scalabile, ad esempio i livelli di dettaglio dipendenti continui o visualizzabili, che possono essere calcolati in tempo reale.
-   Consente di migliorare le prestazioni eseguendo calcoli costosi a una frequenza più bassa (eseguendo calcoli su un modello di dettaglio inferiore). Questo potrebbe includere calcoli di Blend con forme Blend o destinazioni morph per calcoli realistici di animazione o fisica per il rilevamento di conflitti o la dinamica del corpo flessibile.

La pipeline Direct3D 11 implementa la suddivisione a mosaico nell'hardware, che consente di caricare il lavoro dalla CPU alla GPU. Questo può comportare un miglioramento delle prestazioni molto elevato se un'applicazione implementa un numero elevato di destinazioni morph e/o modelli di mascheramento/deformazione più sofisticati. Per accedere alle nuove funzionalità a mosaico, è necessario conoscere alcune nuove fasi della pipeline.

## <a name="new-pipeline-stages"></a>Nuove fasi della pipeline

Lo schema a mosaico usa la GPU per calcolare una superficie più dettagliata da una superficie costruita da patch quadre, patch di triangolo o oline. Per approssimare l'area ordinata, ogni patch è suddivisa in triangoli, punti o linee usando i fattori a mosaico. La pipeline Direct3D 11 implementa la suddivisione a mosaico usando tre nuove fasi della pipeline:

-   [Fase Hull shader](#hull-shader-stage) : una fase programmabile dello shader che produce una patch di geometria (e costanti patch) che corrispondono a ogni patch di input (quad, triangolo o riga).
-   [Fase mosaico](#tessellator-stage) : fase della pipeline di una funzione fissa che consente di creare un modello di campionamento del dominio che rappresenta la patch Geometry e genera un set di oggetti più piccoli (triangoli, punti o linee) che connettono questi esempi.
-   [Fase Domain-shader](#domain-shader-stage) : una fase programmabile dello shader che calcola la posizione del vertice che corrisponde a ogni esempio di dominio.

Il diagramma seguente evidenzia le nuove fasi della pipeline Direct3D 11.

![diagramma della pipeline Direct3D 11 che evidenzia le fasi di Hull shader, mosaico e Domain shader](images/d3d11-pipeline-stages-tessellation.png)

Nel diagramma seguente viene illustrata la progressione nelle fasi a mosaico. La progressione inizia con la superficie di suddivisione dei dettagli bassa. La progressione evidenzia la patch di input con la patch Geometry corrispondente, gli esempi di dominio e i triangoli che connettono questi esempi. La progressione evidenzia infine i vertici che corrispondono a questi esempi.

![diagramma della progressione a mosaico](images/tess-prog.png)

### <a name="hull-shader-stage"></a>Fase Hull-Shader

Hull shader, che viene richiamato una volta per ogni patch, trasforma i punti di controllo di input che definiscono una superficie di ordine inferiore nei punti di controllo che costituiscono una patch. Esegue anche alcuni calcoli per patch per fornire i dati per la fase di suddivisione a mosaico e la fase del dominio. Al livello più semplice della casella nera, la fase Hull shader sarà simile al diagramma seguente.

![diagramma della fase Hull shader](images/d3d11-hull-shader.png)

Un Hull shader viene implementato con una funzione HLSL e presenta le proprietà seguenti:

-   L'input dello shader è compreso tra 1 e 32 punti di controllo.
-   L'output dello shader è compreso tra 1 e 32 punti di controllo, indipendentemente dal numero di fattori a mosaico. L'output dei punti di controllo di uno scafo dello shader può essere utilizzato dalla fase del dominio shader. I dati delle costanti patch possono essere utilizzati da uno shader del dominio; i fattori a mosaico possono essere utilizzati dal Domain shader e dalla fase a mosaico.
-   I fattori a mosaico determinano la quantità di suddivisione di ogni patch.
-   Lo shader dichiara lo stato richiesto dalla fase mosaico. Sono incluse informazioni quali il numero di punti di controllo, il tipo di facet patch e il tipo di partizionamento da usare quando tessellating. Queste informazioni vengono visualizzate come dichiarazioni in genere all'inizio del codice dello shader.
-   Se la fase Hull-shader imposta un fattore di mosaico perimetrale su = 0 o NaN, la patch verrà ritagliata. Di conseguenza, la fase mosaico può essere eseguita o meno, il Domain shader non verrà eseguito e non verrà generato alcun output visibile per tale patch.

A un livello più profondo, un Hull shader funziona effettivamente in due fasi: una fase del punto di controllo e una fase di una costante di patch, che vengono eseguite in parallelo dall'hardware. Il compilatore HLSL estrae il parallelismo in uno scafo shader e lo codifica in bytecode che guida l'hardware.

-   La fase del punto di controllo funziona una volta per ogni punto di controllo, leggendo i punti di controllo per una patch e generando un punto di controllo di output (identificato da un ControlPointID).
-   La fase patch-Constant funziona una volta per ogni patch per generare fattori di mosaico perimetrale e altre costanti per patch. Internamente, è possibile che vengano eseguite contemporaneamente molte fasi della costante patch. La fase patch-Constant ha accesso in sola lettura a tutti i punti di controllo di input e output.

Di seguito è riportato un esempio di Hull shader:


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



Per un esempio in cui viene creato un Hull shader, vedere [How to: Create a Hull shader](direct3d-11-advanced-stages-hull-shader-create.md).

### <a name="tessellator-stage"></a>Fase mosaico

Mosaico è una fase a funzione fissa inizializzata associando uno scafo shader alla pipeline (vedere [procedura: inizializzare la fase mosaico](direct3d-11-advanced-stages-tessellator-initialize.md)). Lo scopo della fase mosaico è suddividere un dominio (quad, Tri o line) in molti oggetti più piccoli (triangoli, punti o linee). Il mosaico riquadri un dominio canonico in un sistema di coordinate normalizzato (zero-a-uno). Ad esempio, un dominio Quad è tassellati a un quadrato di unità.

Mosaico funziona una volta per ogni patch usando i fattori a mosaico (che specificano la modalità di tassellati del dominio) e il tipo di partizionamento (che specifica l'algoritmo usato per sezionare una patch) passati dalla fase Hull-shader. Mosaico restituisce le coordinate UV (e facoltativamente w) e la topologia di superficie alla fase Domain-shader.

Internamente, il mosaico funziona in due fasi:

-   La prima fase elabora i fattori a mosaico, risolvendo i problemi di arrotondamento, gestendo fattori molto piccoli, riducendo e combinando fattori, usando operazioni aritmetiche a virgola mobile a 32 bit.
-   La seconda fase genera elenchi di punti o topologia in base al tipo di partizionamento selezionato. Si tratta dell'attività principale della fase mosaico e USA frazioni a 16 bit con aritmetica a virgola fissa. L'aritmetica a virgola fissa consente l'accelerazione hardware mantenendo la precisione accettabile. Ad esempio, data una patch a 64 metri di larghezza, questa precisione può inserire punti a una risoluzione di 2 mm.



| Tipo di partizionamento | Range                       |
|----------------------|-----------------------------|
| dispari frazionario \_      | \[1... 63\]                  |
| anche frazionaria \_     | Intervallo di TessFactor: \[ 2.. 64\] |
| numero intero              | Intervallo di TessFactor: \[ 1.. 64\] |
| pow2                 | Intervallo di TessFactor: \[ 1.. 64\] |



 

### <a name="domain-shader-stage"></a>Fase Domain-Shader

Un Domain shader calcola la posizione del vertice di un punto suddiviso nella patch di output. Un Domain shader viene eseguito una volta per ogni punto di output della fase mosaico e ha accesso in sola lettura alle coordinate UV di output della fase mosaico, alla patch di output di Hull shader e alle costanti della patch di output di Hull shader, come illustrato nella figura seguente.

![diagramma della fase Domain-shader](images/d3d11-domain-shader.png)

Le proprietà dello shader del dominio includono:

-   Un Domain shader viene richiamato una volta per ogni coordinata di output dalla fase mosaico.
-   Un Domain shader usa i punti di controllo di output dalla fase Hull shader.
-   Un Domain shader restituisce la posizione di un vertice.
-   Gli input sono gli output dello scafo dello shader, inclusi i punti di controllo, i dati delle patch costanti e i fattori a mosaico. I fattori a mosaico possono includere, ad esempio, i valori usati dalla funzione fissa mosaico, nonché i valori non elaborati (prima di arrotondare per mosaico Integer), che facilita il geomorphing.

Al termine dello shader del dominio, la suddivisione a mosaico viene completata e i dati della pipeline continuano alla fase successiva della pipeline (Geometry shader, pixel shader e così via). Un geometry shader che prevede primitive con adiacenza (ad esempio, 6 vertici per triangolo) non è valido quando il mosaico è attivo (ciò comporta un comportamento non definito, a cui il livello di debug si lamenta).

Di seguito è riportato un esempio di Domain shader:


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



## <a name="apis-for-initializing-tessellation-stages"></a>API per l'inizializzazione di fasi mosaico

La suddivisione a mosaico viene implementata con due nuove fasi di shader programmabili: uno scafo e uno shader del dominio. Queste nuove fasi dello shader sono programmate con codice HLSL definito nel modello di shader 5. Le nuove destinazioni shader sono: HS \_ 5 \_ 0 e DS \_ 5 \_ 0. Analogamente a tutte le fasi di shader programmabili, il codice per l'hardware viene estratto dagli shader compilati passati al runtime quando gli shader sono associati alla pipeline usando le API, ad esempio [**DSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dssetshader) e [**HSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetshader). Prima di tutto, è necessario creare lo shader usando le API, ad esempio [**CreateHullShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createhullshader) e [**CreateDomainShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdomainshader).

Abilitare la suddivisione a mosaico creando uno Hull shader e associarlo alla fase Hull-shader (la fase mosaico viene impostata automaticamente). Per generare le posizioni dei vertici finali dalle patch tassellati, è necessario creare anche un Domain shader e associarlo alla fase Domain-shader. Una volta abilitata la suddivisione a mosaico, l'input dei dati per la fase input-assembler deve contenere dati della patch. Ovvero, la topologia dell'assembler di input deve essere una topologia costante patch da [**d3d11 \_ \_ topologia primitiva**](/previous-versions/windows/desktop/legacy/ff476189(v=vs.85)) impostata con [**IASetPrimitiveTopology**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetprimitivetopology).

Per disabilitare la suddivisione a mosaico, impostare Hull shader e Domain shader su **null**. Né la fase geometry-shader né la fase output flusso possono leggere i dati della patch o i punti di controllo dell'output dello shader.

-   Nuove topologie per la fase input-assembler, che sono estensioni di questa enumerazione.

    ```
    enum D3D11_PRIMITIVE_TOPOLOGY
    ```

    

    La topologia è impostata sulla fase input-assembler usando [ **IASetPrimitiveTopology**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetprimitivetopology)

-   Naturalmente, la nuova fase programmabile dello shader richiede l'impostazione di un altro stato, per associare buffer costanti, esempi e risorse dello shader alle fasi della pipeline appropriate. Questi nuovi metodi ID3D11Device sono implementati per l'impostazione di questo stato.
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

La documentazione contiene anche esempi per inizializzare le fasi a mosaico.



| Elemento                                                                                                                                                                                                                                                                                           | Descrizione                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="How_To__Create_a_Hull_Shader"></span><span id="how_to__create_a_hull_shader"></span><span id="HOW_TO__CREATE_A_HULL_SHADER"></span>[Procedura: creare un Hull shader](direct3d-11-advanced-stages-hull-shader-create.md)<br/>                                                     | Creare una Hull shader.<br/>              |
| <span id="How_To__Design_a_Hull_Shader"></span><span id="how_to__design_a_hull_shader"></span><span id="HOW_TO__DESIGN_A_HULL_SHADER"></span>[Procedura: progettare un Hull shader](direct3d-11-advanced-stages-hull-shader-design.md)<br/>                                                     | Progettare uno scafo dello shader.<br/>              |
| <span id="How_To__Initialize_the_Tessellator_Stage"></span><span id="how_to__initialize_the_tessellator_stage"></span><span id="HOW_TO__INITIALIZE_THE_TESSELLATOR_STAGE"></span>[Procedura: inizializzare la fase mosaico](direct3d-11-advanced-stages-tessellator-initialize.md)<br/> | Inizializzare la fase a mosaico.<br/> |
| <span id="How_To__Create_a_Domain_Shader"></span><span id="how_to__create_a_domain_shader"></span><span id="HOW_TO__CREATE_A_DOMAIN_SHADER"></span>[Procedura: creare uno shader di dominio](direct3d-11-advanced-stages-domain-shader-create.md)<br/>                                           | Creare un Domain shader.<br/>            |
| <span id="How_To__Design_a_Domain_Shader"></span><span id="how_to__design_a_domain_shader"></span><span id="HOW_TO__DESIGN_A_DOMAIN_SHADER"></span>[Procedura: progettare un Domain shader](direct3d-11-advanced-stages-domain-shader-design.md)<br/>                                           | Creare un Domain shader.<br/>            |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Pipeline grafica](overviews-direct3d-11-graphics-pipeline.md)
</dt> </dl>

 

