---
title: Mappe di profondità a cascata
description: Le mappe shadow a cascata sono il modo migliore per contrastare uno degli errori più diffusi con l'alias della prospettiva di ombreggiatura.
ms.assetid: d3570d0a-74e0-5b9c-6586-c933f630c4ee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29498dc882133215c910f3bd6caa5966aa0e141aaf4f7a68051834d33f2a3b16
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118649663"
---
# <a name="cascaded-shadow-maps"></a>Mappe di profondità a cascata

Le mappe shadow a cascata sono il modo migliore per contrastare uno degli errori più diffusi con lo shadowing: l'aliasing prospettico. Questo articolo tecnico, che presuppone che il lettore abbia familiarità con il mapping delle ombreggiatura, tratta l'argomento relativo alle macchine virtuali. Nello specifico:

-   spiega la complessità delle macchine virtuali di gestione dei dati.
-   fornisce informazioni dettagliate sulle possibili variazioni degli algoritmi CSM;
-   descrive le due tecniche di filtro più comuni, ovvero il filtro più vicino alla percentuale (PCF) e il filtro con mappe shadow di varianza (VSM).
-   identifica e risolve alcune delle insidie comuni associate all'aggiunta di filtri ai CMS; E
-   illustra come eseguire il mapping delle macchine virtuali a Direct3D 10 tramite l'hardware Direct3D 11.

Il codice usato in questo articolo è disponibile in DirectX Software Development Kit (SDK) negli esempi CascadedShadowMaps11 e VarianceShadows11. Questo articolo si rivela più utile dopo l'implementazione delle tecniche illustrate nell'articolo tecnico Common [Techniques to Improve Shadow Depth Mappe](/windows/desktop/DxTechArts/common-techniques-to-improve-shadow-depth-maps).

## <a name="cascaded-shadow-maps-and-perspective-aliasing"></a>Alias delle Mappe e delle prospettive a cascata

L'aliasing prospettico in una mappa ombreggiata è uno dei problemi più difficili da risolvere. Nell'articolo tecnico Common Techniques to Improve Shadow Depth Mappe viene descritto l'alias della prospettiva e vengono identificati alcuni approcci per attenuare il problema. In pratica, i CMM tendono a essere la soluzione migliore e vengono comunemente usati nei giochi moderni.

Il concetto di base delle macchine virtuali di configurazione è facile da comprendere. Le diverse aree del frustum della fotocamera richiedono mappe ombreggiate con risoluzioni diverse. Gli oggetti più vicini all'occhio richiedono una risoluzione più elevata rispetto agli oggetti più distanti. Infatti, quando l'occhio si sposta molto vicino alla geometria, i pixel più vicini all'occhio possono richiedere una risoluzione tale che anche una mappa ombreggiata 4096 × 4096 è insufficiente.

L'idea di base dei VM è partizionare il frustum in più frusta. Viene eseguito il rendering di una mappa ombreggiatura per ogni subfrustum. la pixel shader esempi dalla mappa che corrisponde maggiormente alla risoluzione richiesta (figura 2).

**Figura 1. Copertura mappa ombreggiata**

![copertura mappa ombreggiata](images/shadow-map-coverage.png)

Nella figura 1 la qualità viene visualizzata (da sinistra a destra) dal più alto al più basso. La serie di griglie che rappresentano le mappe ombreggiate con un frustum di visualizzazione (cono invertito in rosso) mostra come la copertura dei pixel è influenzata dalle diverse mappe di ombreggiatura con risoluzione diversa. Le ombreggiature hanno la massima qualità (pixel bianchi) quando è presente un rapporto di 1:1 tra pixel di mapping nello spazio chiaro e texel nella mappa delle ombreggiature. L'aliasing prospettico si verifica sotto forma di mappe di trama grandi e bloccate (immagine a sinistra) quando troppi pixel vengono mappati allo stesso texel di ombreggiatura. Quando la mappa ombreggiatura è troppo grande, viene campionata. In questo caso, i texel vengono ignorati, vengono introdotti elementi shimmering e le prestazioni sono influenzate.

**Figura 2. Qualità dell'ombreggiatura CSM**

![qualità dell'ombreggiatura csm](images/csm-shadow-quality.png)

La figura 2 mostra i ritaglio della sezione di qualità più elevata in ogni mappa di ombreggiatura nella figura 1. La mappa delle ombreggiatura con i pixel più posizionati (nell'apice) è più vicina all'occhio. Tecnicamente, si tratta di mappe delle stesse dimensioni, con bianco e grigio usati per esemplificare il successo della mappa ombreggiatura a cascata. Il bianco è ideale perché mostra una buona copertura, ovvero un rapporto di 1:1 per i pixel dello spazio visivo e i texel della mappa delle ombreggiatura.

I CPM richiedono i passaggi seguenti per ogni frame.

1.  Partizionare il frustum in subfrusta.
2.  Calcolare una proiezione ortografica per ogni subfrustum.
3.  Eseguire il rendering di una mappa ombreggiatura per ogni subfrustum.
4.  Eseguire il rendering della scena.

    1.  Associare le mappe ombreggiate ed eseguire il rendering.
    2.  Il vertex shader esegue le operazioni seguenti:

        -   Calcola le coordinate della trama per ogni sottofrusto chiaro (a meno che la coordinata di trama necessaria non venga calcolata nel pixel shader).
        -   Trasforma e illumina il vertice e così via.

    3.  Il pixel shader esegue le operazioni seguenti:

        -   Determina la mappa ombreggiatura appropriata.
        -   Trasforma le coordinate della trama, se necessario.
        -   Campioni la cascata.
        -   Illumina il pixel.

## <a name="partitioning-the-frustum"></a>Partizionamento di Frustum

Il partizionamento del frustum è l'atto di creazione di subfrusta. Una tecnica per la suddivisione del frustum consiste nel calcolare gli intervalli dal 0% al 100% nella direzione Z. Ogni intervallo rappresenta quindi un piano vicino e un piano lontano come percentuale dell'asse Z.

**Figura 3. Visualizzare frustum partizionati in modo arbitrario**

![visualizzare frustum partizionati in modo arbitrario](images/view-frustums-partitioned-arbitrarily.png)

In pratica, il ricalcolo delle divisioni frustum per frame fa sì che i bordi dell'ombreggiatura slittano. La procedura generalmente accettata consiste nell'usare un set statico di intervalli a catena per ogni scenario. In questo scenario, l'intervallo lungo l'asse Z viene usato per descrivere un subfrustum che si verifica durante il partizionamento del frustum. La determinazione degli intervalli di dimensioni corretti per una determinata scena dipende da diversi fattori.

### <a name="orientation-of-the-scene-geometry"></a>Orientamento della geometria della scena

Per quanto riguarda la geometria della scena, l'orientamento della fotocamera influisce sulla selezione dell'intervallo a catena. Ad esempio, una fotocamera molto vicina al suolo, ad esempio una fotocamera di terra in un gioco di calcio, ha un set statico diverso di intervalli a cascata rispetto a una fotocamera nel cielo.

La figura 4 mostra alcune fotocamere diverse e le rispettive partizioni. Quando l'intervallo Z della scena è molto grande, sono necessari più piani di divisione. Ad esempio, quando l'occhio è molto vicino al piano terra, ma gli oggetti distanti sono ancora visibili, possono essere necessarie più cascate. È utile anche dividere il frustum in modo che più divisioni siano vicine all'occhio (in cui l'aliasing prospettico sta cambiando più velocemente). Quando la maggior parte della geometria è compressa in una piccola sezione (ad esempio una visualizzazione a testa in alto o un simulatore di volo) del frustum di visualizzazione, sono necessarie meno cascate.

**Figura 4. Configurazioni diverse richiedono divisioni frustum diverse**

![configurazioni diverse richiedono divisioni frustum diverse](images/different-configurations-require-different-frustum-splits.png)

(A sinistra) Quando la geometria ha un intervallo dinamico elevato in Z, sono necessarie molte cascate. (Al centro) Quando la geometria ha un intervallo dinamico basso in Z, i vantaggi di più frustum sono scarsi. (A destra) Sono necessarie solo tre partizioni quando l'intervallo dinamico è medio.

### <a name="orientation-of-the-light-and-the-camera"></a>Orientamento della luce e della fotocamera

La matrice di proiezione di ogni cascata si adatta perfettamente al sottofrusto corrispondente. Nelle configurazioni in cui la fotocamera di visualizzazione e le direzioni della luce sono ortogonali, le cascate possono essere adattate strettamente con poche sovrapposizioni. La sovrapposizione diventa più grande quando la luce e la fotocamera di visualizzazione si spostano in allineamento parallelo (figura 5). Quando la luce e la fotocamera di visualizzazione sono quasi parallele, viene chiamata "frusta di duello" ed è uno scenario molto difficile per la maggior parte degli algoritmi di ombreggiatura. Non è insolito vincolare la luce e la fotocamera in modo che questo scenario non si verifichi. I CMS, tuttavia, hanno prestazioni molto migliori rispetto a molti altri algoritmi in questo scenario.

**Figura 5. La sovrapposizione a cascata aumenta quando la direzione della luce diventa parallela alla direzione della fotocamera**

![La sovrapposizione a cascata aumenta quando la direzione della luce diventa parallela alla direzione della fotocamera](images/cascade-overlap-increases-as-light-direction-becomes.jpg)

Molte implementazioni CSM usano frusta di dimensioni fisse. Il pixel shader può usare la profondità Z per indicizzare la matrice di cascate quando il frustum viene suddiviso in intervalli di dimensioni fisse.

## <a name="calculating-a-view-frustum-bound"></a>Calcolo di un View-Frustum associato

Dopo aver selezionato gli intervalli di frustum, i subfrusta vengono creati usando uno dei due seguenti: adatta alla scena e adatta a cascata.

### <a name="fit-to-scene"></a>Adatta alla scena

Tutto il frusta può essere creato con lo stesso piano vicino. In questo modo le cascate si sovrappongono. L'esempio CascadedShadowMaps11 chiama questa tecnica adatta alla scena.

### <a name="fit-to-cascade"></a>Adatta a cascata

In alternativa, è possibile creare frusta con l'intervallo di partizione effettivo usato come piani vicini e lontani. Ciò causa un adattamento più stretto, ma degenera per adattarsi alla scena in caso di duello frusta. Gli esempi CascadedShadowMaps11 richiamano questa tecnica adatta a cascata.

Questi due metodi sono illustrati nella figura 6. Adattarsi alla riduzione della risoluzione degli sprechi a cascata. Il problema relativo all'adattamento alla cascata è che la proiezione ortografica cresce e si riduce in base all'orientamento del frusto della vista. La tecnica di adattamento alla scena consente di riempire la proiezione ortografica in base alle dimensioni massime del frustum di visualizzazione rimuovendo gli artefatti visualizzati quando la fotocamera di visualizzazione si sposta. [Common Techniques to Improve Shadow Depth Mappe](/windows/desktop/DxTechArts/common-techniques-to-improve-shadow-depth-maps) risolve gli artefatti visualizzati quando la luce si sposta nella sezione "Spostamento della luce in incrementi di dimensioni texel".

**Figura 6. Adatta alla scena e adatta a cascata**

![adatta alla scena e adatta a cascata](images/fit-to-scene-vs-fit-to-cascade.png)

## <a name="render-the-shadow-map"></a>Eseguire il rendering della mappa ombreggiatura

L'esempio CascadedShadowMaps11 esegue il rendering delle mappe shadow in un unico buffer di grandi dimensioni. Questo perché PCF nelle matrici di trame è una funzionalità Direct3D 10.1. Per ogni propagazione, viene creato un viewport che copre la sezione del buffer di profondità corrispondente a tale propagazione. Un valore null pixel shader è associato perché è necessaria solo la profondità. Infine, il viewport e la matrice di ombreggiatura corretti vengono impostati per ogni cascata, poiché il rendering delle mappe di profondità viene eseguito una alla volta nel buffer di ombreggiatura principale.

## <a name="render-the-scene"></a>Eseguire il rendering della scena

Il buffer contenente le ombreggiature è ora associato al pixel shader. Esistono due metodi per selezionare la cascata implementata nell'esempio CascadedShadowMaps11. Questi due metodi sono illustrati con il codice shader.

### <a name="interval-based-cascade-selection"></a>Interval-Based selezione a catena

**Figura 7. Selezione a catena basata su intervalli**

![selezione a catena basata su intervalli](images/interval-based-cascade-selection.jpg)

Nella selezione basata su intervalli (Figura 7), il vertex shader calcola la posizione nello spazio mondiale del vertice.


```C++
Output.vDepth = mul( Input.vPosition, m_mWorldView ).z;
```



Il pixel shader riceve la profondità interpolata.


```C++
fCurrentPixelDepth = Input.vDepth;
```



La selezione a catena basata su intervalli usa un confronto vettoriale e un prodotto punto per determinare la cacade corretta. CASCADE \_ COUNT \_ FLAG specifica il numero di propagazioni. I dati m \_ fCascadeFrustumsEyeSpaceDepths vincolano le \_ partizioni frustum della vista. Dopo il confronto, fComparison contiene un valore pari a 1 in cui il pixel corrente è maggiore della barriera e il valore 0 quando la cascata corrente è più piccola. Un prodotto punto somma questi valori in un indice di matrice.


```C++
        float4 vCurrentPixelDepth = Input.vDepth;
        float4 fComparison = ( vCurrentPixelDepth > m_fCascadeFrustumsEyeSpaceDepths_data[0]);
        float fIndex = dot(
        float4( CASCADE_COUNT_FLAG > 0,
        CASCADE_COUNT_FLAG > 1,
        CASCADE_COUNT_FLAG > 2,
        CASCADE_COUNT_FLAG > 3)
        , fComparison );

        fIndex = min( fIndex, CASCADE_COUNT_FLAG );
        iCurrentCascadeIndex = (int)fIndex;
```



Dopo aver selezionato la cascata, la coordinata di trama deve essere trasformata nella cascata corretta.


```C++
vShadowTexCoord = mul( InterpolatedPosition, m_mShadow[iCascadeIndex] );
```



Questa coordinata di trama viene quindi usata per campionare la trama con la coordinata X e la coordinata Y. La coordinata Z viene usata per eseguire il confronto della profondità finale.

### <a name="map-based-cascade-selection"></a>Map-Based selezione a catena

La selezione basata su mappa (figura 8) esegue test sui quattro lati della cascata per trovare la mappa più stretta che copre il pixel specifico. Invece di calcolare la posizione nello spazio mondiale, il vertex shader calcola la posizione dello spazio di visualizzazione per ogni cascata. Il pixel shader scorre le cascate per ridimensionare e spostare le coordinate della trama in modo che indicizzano la cascata corrente. La coordinata di trama viene quindi testata rispetto ai limiti della trama. Quando i valori X e Y della coordinata di trama rientrano in una cascata, vengono usati per campionare la trama. La coordinata Z viene usata per eseguire il confronto della profondità finale.

**Figura 8. Selezione a catena basata su mappa**

![selezione a catena basata su mappa](images/map-based-cascade-selection.jpg)

### <a name="interval-based-selection-vs-map-based-selection"></a>Interval-Based selezione e Map-Based selezione

La selezione basata su intervalli è leggermente più veloce rispetto alla selezione basata su mappa perché la selezione a catena può essere eseguita direttamente. La selezione basata su mappa deve intersecare la coordinata della trama con i limiti a cascata.

La selezione basata su mappa usa la cascata in modo più efficiente quando le mappe ombreggiate non si allineano perfettamente (vedere la figura 8).

## <a name="blend-between-cascades"></a>Blend tra cascate

Le vsms (descritte più avanti in questo articolo) e le tecniche di filtro, ad esempio PCF, possono essere usate con IMS a bassa risoluzione per produrre ombreggiature sfoltite. Sfortunatamente, ciò comporta una distanza visibile (figura 9) tra i livelli a cascata perché la risoluzione non corrisponde. La soluzione consiste nel creare una banda tra le mappe ombreggiate in cui viene eseguito il test delle ombreggiatura per entrambe le cascate. Lo shader viene quindi interpolato in modo lineare tra i due valori in base alla posizione del pixel nella banda di fusione. Gli esempi CascadedShadowMaps11 e VarianceShadows11 forniscono un dispositivo di scorrimento gui che può essere usato per aumentare e ridurre questa banda sfocatura. Lo shader esegue un ramo dinamico in modo che la maggior parte dei pixel letta solo dalla cascata corrente.

**Figura 9. Propagare le seams**

![cascate](images/cascade-seams.jpg)

(A sinistra) È possibile visualizzare una catena visibile in cui le cascate si sovrappongono. (A destra) Quando le cascate vengono combinate tra, non si verifica alcuna connessione.

## <a name="filtering-shadow-maps"></a>Applicazione di filtri alle Mappe

### <a name="pcf"></a>Pcf

L'applicazione di filtri alle normali mappe delle ombreggiature non produce ombreggiature sfocate e sfuocate. L'hardware di filtro sfocatura i valori di profondità e quindi confronta i valori sfocati con lo spazio chiaro texel. Il limite rigido risultante dal test di super/esito negativo esiste ancora. La sfocatura delle mappe delle ombreggiature serve solo a spostare erroneamente il bordo rigido. PCF abilita il filtro sulle mappe ombreggiate. L'idea generale di PCF è calcolare una percentuale del pixel in ombreggiatura in base al numero di sottocampionamenti che superano il test di profondità sul numero totale di sottocampionamenti.

L'hardware Direct3D 10 e Direct3D 11 può eseguire PCF. L'input per un campionatore PCF è costituito dalla coordinata di trama e da un valore di profondità di confronto. Per semplicità, PCF viene spiegato con un filtro a quattro tocchi. Il campionatore di trame legge la trama quattro volte, in modo simile a un filtro standard. Tuttavia, il risultato restituito è una percentuale dei pixel che hanno superato il test di profondità. La figura 10 mostra come un pixel che supera uno dei quattro test di profondità sia ombreggiato al 25%. Il valore effettivo restituito è un'interpolazione lineare basata sulle coordinate subtexel delle operazioni di lettura della trama per produrre una sfumatura uniforme. Senza questa interpolazione lineare, il file PCF a quattro tocchi potrebbe restituire solo cinque valori: { 0.0, 0.25, 0,5, 0,75, 1,0 }.

**Figura 10. Immagine filtrata PCF, con il 25% del pixel selezionato coperto**

![Immagine filtrata pcf, con il 25% del pixel selezionato coperto](images/pcf-filtered-image.png)

È anche possibile eseguire PCF senza supporto hardware o estendere PCF a kernel più grandi. Alcune tecniche possono anche essere campionate con un kernel ponderato. A tale scopo, creare un kernel (ad esempio gaussiano) per una griglia N × N. I pesi devono essere aggiunti fino a 1. La trama viene quindi campionata N2 volte. Ogni campione viene ridimensionato in base ai pesi corrispondenti nel kernel. L'esempio CascadedShadowMaps11 usa questo approccio.

### <a name="depth-bias"></a>Distorsione della profondità

La distorsione della profondità diventa ancora più importante quando vengono usati kernel PCF di grandi dimensioni. È valido solo confrontare la profondità dello spazio luce di un pixel con il pixel a cui esegue il mapping nella mappa di profondità. I vicini del texel della mappa di profondità fanno riferimento a una posizione diversa. Questa profondità è probabilmente simile, ma può essere molto diversa a seconda della scena. La figura 11 evidenzia gli elementi che si verificano. Una singola profondità viene confrontata con tre texel adiacenti nella mappa delle ombreggiatura. Uno dei test di profondità ha erroneamente esito negativo perché la relativa profondità non è correlata alla profondità dello spazio luce calcolato della geometria corrente. La soluzione consigliata a questo problema consiste nell'usare un offset maggiore. Un offset troppo grande, tuttavia, può comportare l'utilizzo di Peter Panning. Il calcolo di un piano vicino e lontano stretto consente di ridurre gli effetti dell'uso di un offset.

**Figura 11. Auto shadowing errroneo**

![auto shadowing errroneo](images/erroneous-self-shadowing.png)

L'ombreggiatura self-shadow errata deriva dal confronto tra i pixel nella profondità dello spazio luce e i texel nella mappa delle ombreggiatura che non sono correlati. La profondità nello spazio chiaro è correlata all'ombreggiatura texel 2 nella mappa di profondità. Texel 1 è maggiore della profondità dello spazio chiaro, mentre 2 è uguale e 3 è minore. Texels 2 e 3 superano il test di profondità, mentre Texel 1 ha esito negativo.

### <a name="calculating-a-per-texel-depth-bias-with-ddx-and-ddy-for-large-pcfs"></a>Calcolo di una distorsione Per-Texel profondità con DDX e DDY per PCF di grandi dimensioni

Il calcolo di una distorsione di profondità per texel con **ddx** e **ddy** per pcf di grandi dimensioni è una tecnica che calcola la distorsione di profondità corretta, presupponendo che la superficie sia planare, per la mappa ombreggiata adiacente texel.

Questa tecnica adatta la profondità di confronto a un piano usando le informazioni derivate. Poiché questa tecnica è complessa dal punto di vista del calcolo, deve essere usata solo quando una GPU ha cicli di calcolo da risparmiare. Quando vengono usati kernel molto grandi, questa può essere l'unica tecnica che funziona per rimuovere gli artefatti di auto-shadowing senza causare Peter Panning.

La figura 12 evidenzia il problema. La profondità nello spazio chiaro è nota per l'unico texel confrontato. Le profondità dello spazio chiaro che corrispondono ai texel adiacenti nella mappa di profondità sono sconosciute.

**Figura 12. Mappa della scena e della profondità**

![mappa della scena e della profondità](images/scene-and-depth-map.png)

La scena sottoposta a rendering viene visualizzata a sinistra e la mappa di profondità con un blocco texel di esempio viene visualizzata a destra. Il texel dello spazio visivo viene mappato al pixel con etichetta D al centro del blocco. Questo confronto è accurato. Profondità corretta nello spazio oculare correlata ai pixel sconosciuti del vicino D. Il mapping dei texel adiacenti allo spazio visivo è possibile solo se si presuppone che il pixel si riponga allo stesso triangolo di D.

La profondità è nota per il texel correlato alla posizione dello spazio chiaro. La profondità è sconosciuta per i texel adiacenti nella mappa di profondità.

A livello di alto livello, questa tecnica usa le operazioni **DDX** e **DDY** HLSL per trovare la derivata della posizione dello spazio chiaro. Ciò non è necessario perché le operazioni derivate restituiscono la sfumatura della profondità dello spazio luce rispetto allo spazio dello schermo. Per convertirlo in una sfumatura della profondità dello spazio chiaro rispetto allo spazio chiaro, è necessario calcolo di una matrice di conversione.

### <a name="explanation-with-shader-code"></a>Spiegazione con codice shader

I dettagli del resto dell'algoritmo vengono fornite come spiegazione del codice shader che esegue questa operazione. Questo codice è disponibile nell'esempio CascadedShadowMaps11. La figura 13 illustra come le coordinate della trama dello spazio chiaro vengono mappate alla mappa di profondità e come è possibile usare i derivati in X e Y per creare una matrice di trasformazione.

**Figura 13. Matrice spazio schermo-luce**

![da spazio schermo a matrice di spazio chiaro](images/screen-space-to-light-space-matrix.png)

I derivati della posizione dello spazio chiaro in X e Y vengono usati per creare questa matrice.

Il primo passaggio consiste nel calcolare la derivata della posizione light-view-space.


```C++
          float3 vShadowTexDDX = ddx (vShadowMapTextureCoordViewSpace);
          float3 vShadowTexDDY = ddy (vShadowMapTextureCoordViewSpace);
```



Le GPU della classe Direct3D 11 calcolano questi derivati eseguendo 2 × 2 quad di pixel in parallelo e sottraendo le coordinate della trama dal vicino in X per **ddx** e dal vicino in Y per **ddy**. Questi due derivati costituiscono le righe di una matrice 2 × 2. Nella forma corrente, questa matrice può essere usata per convertire i pixel adiacenti dello spazio dello schermo in inclinazioni dello spazio chiaro. Tuttavia, è necessario l'inverso di questa matrice. È necessaria una matrice che trasforma i pixel adiacenti dello spazio chiaro in inclinazioni dello spazio dello schermo.


```C++
          float2x2 matScreentoShadow = float2x2( vShadowTexDDX.xy, vShadowTexDDY.xy );
          float fInvDeterminant = 1.0f / fDeterminant;

          float2x2 matShadowToScreen = float2x2 (
          matScreentoShadow._22 * fInvDeterminant,
          matScreentoShadow._12 * -fInvDeterminant,
          matScreentoShadow._21 * -fInvDeterminant,
          matScreentoShadow._11 * fInvDeterminant );
```



**Figura 14. Spazio chiaro per lo spazio sullo schermo**

![da spazio chiaro a spazio sullo schermo](images/light-space-to-screen-space.png)

Questa matrice viene quindi usata per trasformare i due texel sopra e a destra del texel corrente. Questi elementi adiacenti sono rappresentati come offset dal texel corrente.


```C++
          float2 vRightShadowTexelLocation = float2( m_fTexelSize, 0.0f );
          float2 vUpShadowTexelLocation = float2( 0.0f, m_fTexelSize );
          float2 vRightTexelDepthRatio = mul( vRightShadowTexelLocation,
          matShadowToScreen );
          float2 vUpTexelDepthRatio = mul( vUpShadowTexelLocation,
          matShadowToScreen );
```



Il rapporto creato dalla matrice viene infine moltiplicato per i derivati della profondità per calcolare gli offset di profondità per i pixel adiacenti.


```C++
            float fUpTexelDepthDelta =
            vUpTexelDepthRatio.x * vShadowTexDDX.z
            + vUpTexelDepthRatio.y * vShadowTexDDY.z;
            float fRightTexelDepthDelta =
            vRightTexelDepthRatio.x * vShadowTexDDX.z
            + vRightTexelDepthRatio.y * vShadowTexDDY.z;
```



Questi pesi possono ora essere usati in un ciclo PCF per aggiungere un offset alla posizione.


```C++
    for( int x = m_iPCFBlurForLoopStart; x < m_iPCFBlurForLoopEnd; ++x ) 
    {
        for( int y = m_iPCFBlurForLoopStart; y < m_iPCFBlurForLoopEnd; ++y )
            {
            if ( USE_DERIVATIVES_FOR_DEPTH_OFFSET_FLAG )
            {
            depthcompare += fRightTexelDepthDelta * ( (float) x ) +
            fUpTexelDepthDelta * ( (float) y );
            }
            // Compare the transformed pixel depth to the depth read
            // from the map.
            fPercentLit += g_txShadow.SampleCmpLevelZero( g_samShadow,
            float2(
            vShadowTexCoord.x + ( ( (float) x ) * m_fNativeTexelSizeInX ) ,
            vShadowTexCoord.y + ( ( (float) y ) * m_fTexelSize )
            ),
            depthcompare
            );
            }
     }
```



## <a name="pcf-and-csms"></a>PCF e CMS

PCF non funziona su matrici di trame in Direct3D 10. Per usare PCF, tutte le cascate vengono archiviate in un unico at atlas di trama di grandi dimensioni.

### <a name="derivative-based-offset"></a>Derivative-Based offset

L'aggiunta degli offset basati su derivati per IMS presenta alcune problematiche. Ciò è dovuto a un calcolo derivato all'interno del controllo di flusso divergente. Il problema si verifica a causa di un modo fondamentale per il funzionamento delle GPU. Le GPU Direct3D11 operano su 2 × 2 quad di pixel. Per eseguire una derivata, le GPU sottraggono in genere la copia del pixel corrente di una variabile dalla copia del pixel adiacente della stessa variabile. Il modo in cui si verifica questo problema varia da GPU a GPU. Le coordinate della trama sono determinate dalla selezione a catena basata su mappa o basata su intervalli. Alcuni pixel in un pixel quad scelgono una cascata diversa rispetto al resto dei pixel. In questo modo si verificano delle trame visibili tra le mappe ombreggiate perché gli offset basati su derivati sono ora completamente erri. La soluzione consiste nell'eseguire il derivato sulle coordinate della trama dello spazio di visualizzazione chiaro. Queste coordinate sono le stesse per ogni cascata.

### <a name="padding-for-pcf-kernels"></a>Spaziatura interna per kernel PCF

I kernel PCF vengono indicizzati all'esterno di una partizione a catena se il buffer shadow non è riempito. La soluzione consiste nel riempire il bordo esterno della cascata di una metà delle dimensioni del kernel PCF. Deve essere implementato nello shader che seleziona la cascata e nella matrice di proiezione che deve eseguire il rendering della cascata sufficientemente grande da mantenere il bordo.

## <a name="variance-shadow-maps"></a>Ombreggiatura Mappe

Per altre informazioni, vedere [Varianza shadow maps](https://portal.acm.org/citation.cfm?doid=1111411.1111440) by Donnelly and Lauritzen (Mappe shadow di varianza di Donnelly e Lauritzen) per abilitare il filtro diretto delle mappe shadow. Quando si usano MACCHINE VIRTUALI, è possibile usare tutta la potenza dell'hardware di filtro trame. È possibile usare il filtro trilineare e anisotropo (figura 15). Inoltre, le macchine virtuali di visual studio possono essere sfocate direttamente tramite la convoluzione. Le macchine virtuali di Visual Studio hanno alcuni svantaggi; È necessario archiviare due canali di dati di profondità (profondità e profondità al quadrato). Quando le ombreggiature si sovrappongono, l'emorragia di luce è comune. Funzionano bene, tuttavia, con risoluzioni inferiori e possono essere combinati con IMS.

**Figura 15. Filtro anisotropo**

![filtro anisotropo](images/anisotropic-filtering.png)

### <a name="algorithm-details"></a>Informazioni sugli algoritmi

Le macchine virtuali di Visual Studio funzionano tramite il rendering della profondità e della profondità al quadrato in una mappa ombreggiatura a due canali. Questa mappa ombreggiatura a due canali può quindi essere sfocata e filtrata esattamente come una trama normale. L'algoritmo usa quindi la disuguaglianza di Chebychev nel pixel shader stimare la frazione dell'area pixel che supererebbe il test di profondità.

Il pixel shader recupera i valori di profondità e profondità quadrati.


```C++
        float  fAvgZ  = mapDepth.x; // Filtered z
        float  fAvgZ2 = mapDepth.y; // Filtered z-squared
```



Viene eseguito il confronto della profondità.


```C++
        if ( fDepth <= fAvgZ )
        {
        fPercentLit = 1;
        }
```



Se il confronto della profondità non riesce, viene stimata la percentuale del pixel acceso. La varianza viene calcolata come media dei quadrati meno il quadrato della media.


```C++
        float variance = ( fAvgZ2 ) − ( fAvgZ * fAvgZ );
        variance = min( 1.0f, max( 0.0f, variance + 0.00001f ) );
```



Il valore fPercentLit viene stimato con la disuguaglianza di Chebychev.


```C++
        float mean           = fAvgZ;
        float d              = fDepth - mean;
        float fPercentLit    = variance / ( variance + d*d );
```



## <a name="light-bleeding"></a>Emorragia leggera

Lo svantaggio più grande per le macchine virtuali è l'emorragia leggera (figura 16). L'emorragia leggera si verifica quando più ombreggiatori si oscludono l'un l'altro lungo i bordi. I vsms ombreggiatura dei bordi delle ombreggiature in base alle differenze di profondità. Quando le ombreggiature si sovrappongono, esiste una disparità di profondità al centro di un'area che deve essere ombreggiata. Si tratta di un problema relativo all'uso dell'algoritmo VSM.

**Figura 16. Emorragia di luce VSM**

![emorragia luce vsm](images/vsm-light-bleeding.png)

Una soluzione parziale al problema consiste nell'elevare fPercentLit a una potenza. Ciò ha l'effetto di smorzare la sfocatura, causando artefatti in cui la disparità di profondità è ridotta. A volte esiste un valore magico che attenua il problema.


```C++
fPercentLit = pow( p_max, MAGIC_NUMBER );
```



Un'alternativa all'elevamento della percentuale di luce a una potenza consiste nell'evitare configurazioni in cui le ombreggiature si sovrappongono. Anche le configurazioni di ombreggiatura altamente ottimizzate hanno diversi vincoli su luce, fotocamera e geometria. Anche l'emorragia leggera viene attenuata usando trame con risoluzione più elevata.

Le mappe di ombreggiatura a varianza a livelli (LVSM) risolvono il problema a scapito della suddivisione del frusto in livelli perpendicolari alla luce. Il numero di mappe necessarie sarebbe piuttosto elevato quando vengono usate anche le macchine virtuali.

Inoltre, Andrew Lauritzen, co-autore del documento su VSMs e autore di un documento su LVSMs, ha illustrato la combinazione di mappe shadow esponenziali (EMS) con vsms per contrastare la fusione della luce in un [forum Beyond3D.](https://forum.beyond3d.com/showthread.php?t=47427)

## <a name="vsms-with-csms"></a>VSMs con CMS

L'esempio VarianceShadow11 combina VSMs e CSMs. La combinazione è piuttosto semplice. L'esempio segue gli stessi passaggi dell'esempio CascadedShadowMaps11. Poiché PCF non viene usato, le ombreggiature vengono sfocate in una convoluzione separabile a due passi. Il non uso di PCF consente anche all'esempio di usare matrici di trame anziché un at at atlas di trame. PCF nelle matrici di trame è una funzionalità Direct3D 10.1.

### <a name="gradients-with-csms"></a>Sfumature con IMS

L'uso di sfumature con le SSM può produrre una linea di selezione lungo il bordo tra due cascate, come illustrato nella figura 17. L'istruzione di esempio usa derivati tra pixel per calcolare le informazioni, ad esempio il livello mipmap, necessarie per il filtro. Ciò causa un problema in particolare per la selezione mipmap o il filtro anisotropo. Quando i pixel in un quadruplo accettano rami diversi nello shader, i derivati calcolati dall'hardware GPU non sono validi. Ciò comporta una linea di base frastagliata lungo la mappa delle ombreggiatura.

**Figura 17. Giuse sui bordi a cascata a causa del filtro anisotropo con controllo di flusso divergente**

![giuse sui bordi a cascata a causa del filtro anisotropo con controllo di flusso divergente](images/seams-on-cascade-borders-due-to-anisotropic.jpg)

Questo problema viene risolto calcolando i derivati sulla posizione nello spazio di visualizzazione della luce; La coordinata dello spazio di visualizzazione della luce non è specifica della cascata selezionata. I derivati calcolati possono essere ridimensionati dalla parte della scala della matrice projection-texture al livello mipmap corretto.


```C++
        float3 vShadowTexCoordDDX = ddx( vShadowMapTextureCoordViewSpace );
        vShadowTexCoordDDX *= m_vCascadeScale[iCascade].xyz;
        float3 vShadowTexCoordDDY = ddy( vShadowMapTextureCoordViewSpace );
        vShadowTexCoordDDY *= m_vCascadeScale[iCascade].xyz;

        mapDepth += g_txShadow.SampleGrad( g_samShadow, vShadowTexCoord.xyz,
        vShadowTexCoordDDX, vShadowTexCoordDDY );
```



## <a name="vsms-compared-to-standard-shadows-with-pcf"></a>VsMs rispetto alle ombreggiature standard con PCF

Sia LE MACCHINE VIRTUALI che PCF tentano di approssimare la frazione dell'area pixel che supererebbe il test di profondità. I vsms funzionano con l'hardware di filtro e possono essere sfocati con kernel separabili. I kernel di convoluzione separabili sono notevolmente più economici da implementare rispetto a un kernel completo. Inoltre, i vsms confrontano una profondità dello spazio leggero con un valore nella mappa di profondità dello spazio chiaro. Ciò significa che le MACCHINE VIRTUALI non hanno gli stessi problemi di offset di PCF. Tecnicamente, le MACCHINE VIRTUALI sono profondità di campionamento su un'area più grande, oltre a eseguire un'analisi statistica. Questo è meno preciso di PCF. In pratica, le macchine virtuali di visual studio esere un ottimo lavoro di fusione, il che comporta la necessità di una minore offset. Come descritto in precedenza, lo svantaggio numero uno per le macchine virtuali è un'emorragia leggera.

LE MACCHINE VIRTUALI e PCF rappresentano un compromesso tra la potenza di calcolo GPU e la larghezza di banda della trama GPU. Per calcolare la varianza, le macchine virtuali di Visual Studio richiedono più calcoli matematici. PCF richiede una maggiore larghezza di banda della memoria trame. I kernel PCF di grandi dimensioni possono diventare rapidamente intasati dalla larghezza di banda della trama. Con la potenza di calcolo GPU che cresce più rapidamente rispetto alla larghezza di banda GPU, le macchine virtuali virtuali stanno diventando più pratiche dei due algoritmi. Le macchine virtuali di Visual Studio hanno anche un aspetto migliore con mappe ombreggiate a risoluzione inferiore grazie alla fusione e al filtro.

## <a name="summary"></a>Riepilogo

I CMS offrono una soluzione al problema dell'aliasing prospettico. Esistono diverse configurazioni possibili per ottenere la fedeltà visiva necessaria per un titolo. PcF e VSMs sono ampiamente usati e devono essere combinati con IMS per ridurre l'aliasing.

## <a name="references"></a>Riferimenti

Donnelly, W. e Lauritzen, A. [Variance shadow maps](https://portal.acm.org/citation.cfm?doid=1111411.1111440). In SI3D '06: Proceedings of the 2006 symposium on Interactive 3D graphics and games (Si3D '06: Proceedings of the 2006 symposium on Interactive 3D graphics and games). 2006. pp. 161-165. New York, NY, USA: ACM Press.

Lauritzen, Andrew e McCool, Michael. [Mappe delle ombreggiatura della varianza a livelli](https://portal.acm.org/citation.cfm?id=1375714.1375739&coll=GUIDE&dl=GUIDE&CFID=45360327&CFTOKEN=34578992). Proceedings of graphics interface 2008, May 28–30, 2008, Windsor, Ontario, Canada.

Engel, Woflgang F. Sezione 4. Shadow Mappe. ShaderX5, Advanced Rendering Techniques, Wolfgang F. Engel, Ed. Charles River Media, Boston, Massachusetts. 2006. pp. 197-206.

 

 