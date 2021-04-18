---
title: Mappe di profondità a cascata
description: Le mappe Shadow a cascata (CSM) rappresentano il modo migliore per combattere uno degli errori più comuni con l'aliasing della prospettiva shadowing.
ms.assetid: d3570d0a-74e0-5b9c-6586-c933f630c4ee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae70433f97f33c3cc28af8e282b14ea1f513cf4d
ms.sourcegitcommit: 54db9e6a00a5c8f68e7c1a16b8c6d4943374498c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/01/2021
ms.locfileid: "106334314"
---
# <a name="cascaded-shadow-maps"></a>Mappe di profondità a cascata

Le mappe Shadow a cascata (CSM) rappresentano il modo migliore per combattere uno degli errori più comuni con l'ombreggiatura, ovvero la prospettiva di aliasing. Questo articolo tecnico, che presuppone che il lettore abbia familiarità con il mapping Shadow, affronta l'argomento di CSM. Nello specifico:

-   viene illustrata la complessità di CSM;
-   fornisce informazioni dettagliate sulle possibili varianti degli algoritmi CSM.
-   vengono descritte le due tecniche di filtro più comuni, ovvero la percentuale di filtro più vicino (PCF) e il filtro con le mappe shadow di varianza (VSMs);
-   identifica e risolve alcuni problemi comuni associati all'aggiunta di filtri a CSM; e
-   viene illustrato come eseguire il mapping di CSM a Direct3D 10 tramite l'hardware Direct3D 11.

Il codice usato in questo articolo è disponibile in DirectX Software Development Kit (SDK) negli esempi di CascadedShadowMaps11 e VarianceShadows11. Questo articolo si rivelerà particolarmente utile dopo l'implementazione delle tecniche descritte nell'articolo tecnico, vengono implementate le [tecniche comuni per migliorare le mappe di profondità Shadow](/windows/desktop/DxTechArts/common-techniques-to-improve-shadow-depth-maps).

## <a name="cascaded-shadow-maps-and-perspective-aliasing"></a>Mappe Shadow a cascata e aliasing delle prospettive

L'aliasing della prospettiva in una mappa Shadow è uno dei problemi più difficili da superare. Nell'articolo tecnico sono descritte le tecniche comuni per migliorare le mappe della profondità Shadow, l'aliasing della prospettiva e alcuni approcci per attenuare il problema. In pratica, CSM tendono a essere la soluzione migliore e sono comunemente usati nei giochi moderni.

Il concetto di base di CSM è facile da comprendere. Diverse aree della fotocamera tronco richiedono mappe Shadow con diverse risoluzioni. Gli oggetti più vicini all'occhio richiedono una risoluzione più elevata rispetto agli oggetti più distanti. Infatti, quando l'occhio si sposta molto vicino alla geometria, i pixel più vicini all'occhio possono richiedere una risoluzione così elevata che anche una mappa Shadow 4096 × 4096 non è sufficiente.

L'idea di base di CSM consiste nel partizionare il tronco in più frusta. Viene eseguito il rendering di una mappa shadow per ogni subfrustum; il pixel shader esegue quindi il campionamento dalla mappa che corrisponde maggiormente alla risoluzione necessaria (Figura 2).

**Figura 1. Copertura mappa Shadow**

![Copertura mappa Shadow](images/shadow-map-coverage.png)

Nella figura 1 viene visualizzata la qualità, da sinistra a destra, dal più alto al più basso. La serie di griglie che rappresentano le mappe Shadow con una visualizzazione tronco (cono invertito in rosso) Mostra il modo in cui il code coverage dei pixel è influenzato dalle diverse mappe Shadow della risoluzione. Le ombre sono della qualità massima (pixel bianchi) quando è presente un rapporto di 1:1 pixel di mapping nello spazio chiaro ai Texel nella mappa Shadow. L'aliasing della prospettiva si verifica sotto forma di mappe di trame di grandi dimensioni (immagine a sinistra) quando un numero eccessivo di pixel viene mappato allo stesso Texel ombreggiato. Quando la mappa Shadow è troppo grande, viene sottoposta a campionamento. In questo caso, i Texel vengono ignorati, vengono introdotti gli artefatti luccicanti e le prestazioni sono interessate.

**Figura 2. Qualità ombreggiatura CSM**

![qualità ombreggiatura CSM](images/csm-shadow-quality.png)

Nella figura 2 sono illustrati i ritagli della sezione relativa alla qualità più elevata in ogni mappa shadow nella figura 1. La mappa Shadow con i pixel più vicini (al vertice) è più vicina all'occhio. Tecnicamente, questi sono mappe della stessa dimensione, con bianco e grigio usati per esemplificare il successo della mappa Shadow a cascata. Il bianco è ideale perché mostra una copertura ottimale, ovvero un rapporto 1:1 per gli spazi vuoti e i Texel Mappa Shadow.

CSM richiede i passaggi seguenti per frame.

1.  Partizionare il tronco in subfrusta.
2.  Calcola una proiezione ortogonale per ogni subfrustum.
3.  Eseguire il rendering di una mappa shadow per ogni subfrustum.
4.  Esegue il rendering della scena.

    1.  Associare le mappe Shadow e il rendering.
    2.  Il vertex shader esegue le operazioni seguenti:

        -   Calcola le coordinate di trama per ogni subfrustum di luce (a meno che la coordinata di trama necessaria non venga calcolata nell'pixel shader).
        -   Trasforma e accende il vertice e così via.

    3.  Il pixel shader esegue le operazioni seguenti:

        -   Determina la mappa Shadow corretta.
        -   Trasforma le coordinate di trama, se necessario.
        -   Campiona la Cascade.
        -   Accende il pixel.

## <a name="partitioning-the-frustum"></a>Partizionamento di tronco

Il partizionamento di tronco è l'azione di creazione di subfrusta. Una tecnica per suddividere il tronco consiste nel calcolare gli intervalli dallo zero% al 100% nella direzione Z. Ogni intervallo rappresenta quindi un piano vicino e un piano lontano come percentuale dell'asse Z.

**Figura 3. Visualizza frustums partizionata arbitrariamente**

![Visualizza frustums partizionata arbitrariamente](images/view-frustums-partitioned-arbitrarily.png)

In pratica, il ricalcolo delle divisioni di tronco per frame causa la brillantezza dei bordi ombreggiatura. La prassi generalmente accettata prevede l'uso di un set statico di intervalli a cascata per ogni scenario. In questo scenario, l'intervallo lungo l'asse Z viene usato per descrivere un subfrustum che si verifica durante il partizionamento di tronco. Determinare gli intervalli di dimensioni corretti per una determinata scena dipende da diversi fattori.

### <a name="orientation-of-the-scene-geometry"></a>Orientamento della geometria della scena

Per quanto riguarda la geometria della scena, l'orientamento della fotocamera influiscono sulla selezione dell'intervallo a cascata. Ad esempio, una videocamera molto vicino alla strada, ad esempio una fotocamera da zero in una partita di calcio, presenta un set statico diverso di intervalli a cascata rispetto a una fotocamera in cielo.

Nella figura 4 sono illustrate alcune fotocamere diverse e le rispettive partizioni. Quando l'intervallo Z della scena è molto grande, sono necessari più piani divisi. Ad esempio, quando l'occhio si trova molto vicino al piano di fondo, ma gli oggetti distanti sono ancora visibili, possono essere necessarie più cascate. La divisione del tronco in modo che siano più divisioni vicine (in cui l'aliasing delle prospettive sta cambiando il più veloce) è anche utile. Quando la maggior parte della geometria viene raggruppata in una piccola sezione, ad esempio una visualizzazione overhead o un simulatore di volo, della vista tronco, è necessario un minor numero di Cascade.

**Figura 4. Configurazioni diverse richiedono divisioni tronco diverse**

![configurazioni diverse richiedono divisioni tronco diverse](images/different-configurations-require-different-frustum-splits.png)

Sinistra Quando la geometria ha un intervallo dinamico elevato in Z, sono necessarie numerose cascate. Center Quando la geometria ha un intervallo dinamico basso in Z, i vantaggi derivanti da più frustums sono pochi. Destra Quando l'intervallo dinamico è medio, sono necessarie solo tre partizioni.

### <a name="orientation-of-the-light-and-the-camera"></a>Orientamento della luce e della fotocamera

La matrice di proiezione di ogni Cascade si adatta perfettamente alla subfrustum corrispondente. Nelle configurazioni in cui la fotocamera delle visualizzazioni e le direzioni di luce sono ortogonali, le propagazioni possono essere adeguate a una piccola sovrapposizione. La sovrapposizione diventa più grande come la luce e la videocamera della visualizzazione si sposta nell'allineamento parallelo (Figura 5). Quando la luce e la fotocamera da visualizzare sono quasi parallele, si tratta di un "duello frusta" ed è uno scenario molto complesso per la maggior parte degli algoritmi di shadowing. Non è insolito vincolare la luce e la fotocamera in modo che questo scenario non si verifichi. CSM, tuttavia, offre prestazioni molto migliori rispetto a molti altri algoritmi in questo scenario.

**Figura 5. La sovrapposizione a catena aumenta quando la direzione della luce diventa parallela con la direzione della fotocamera**

![la sovrapposizione a catena aumenta quando la direzione della luce diventa parallela con la direzione della fotocamera](images/cascade-overlap-increases-as-light-direction-becomes.jpg)

Molte implementazioni di CSM usano frusta di dimensioni fisse. Il pixel shader può usare la profondità Z per indicizzare la matrice di propagazioni quando tronco è suddiviso in intervalli di dimensioni fisse.

## <a name="calculating-a-view-frustum-bound"></a>Calcolo di un limite di View-Frustum

Una volta selezionati gli intervalli di tronco, i subfrusta vengono creati usando uno dei due: adatta alla scena e adatta a Cascade.

### <a name="fit-to-scene"></a>Adatta alla scena

Tutti i frusta possono essere creati con lo stesso piano vicino. In questo modo si impone la sovrapposizione delle cascate. L'esempio CascadedShadowMaps11 chiama questa tecnica adatta alla scena.

### <a name="fit-to-cascade"></a>Adatta a cascata

In alternativa, è possibile creare frusta con l'intervallo di partizione effettivo usato come piani vicini e lontani. Ciò determina un adattamento più rigoroso, ma viene degenerato per adattarsi alla scena nel caso di duello frusta. Gli esempi di CascadedShadowMaps11 chiamano questa tecnica adatta a Cascade.

Questi due metodi sono illustrati nella figura 6. Adatta alla riduzione della risoluzione degli sprechi. Il problema con l'adattamento a Cascade è che la proiezione ortogonale cresce e si riduce in base all'orientamento della visualizzazione tronco. La tecnica adatta alla scena riduce la proiezione ortogonale per la dimensione massima della visualizzazione tronco rimuovendo gli artefatti visualizzati quando si sposta la visualizzazione della fotocamera. [Tecniche comuni per migliorare le mappe di profondità ombreggiatura](/windows/desktop/DxTechArts/common-techniques-to-improve-shadow-depth-maps) sono gli elementi visualizzati quando la luce si sposta nella sezione "spostamento della luce in incrementi di dimensioni Texel".

**Figura 6. Adatta alla scena e adatta a Cascade**

![adatta alla scena e adatta a cascata](images/fit-to-scene-vs-fit-to-cascade.png)

## <a name="render-the-shadow-map"></a>Eseguire il rendering della mappa Shadow

L'esempio CascadedShadowMaps11 esegue il rendering delle mappe Shadow in un unico buffer di grandi dimensioni. Questo perché PCF sulle matrici di trama è una funzionalità Direct3D 10,1. Per ogni Cascade viene creato un viewport che copre la sezione del buffer di profondità corrispondente a tale Cascade. Un pixel shader null è associato perché è necessaria solo la profondità. Infine, il viewport e la matrice di ombreggiatura corretti vengono impostati per ogni propagazione, in quanto viene eseguito il rendering delle mappe di profondità una alla volta nel buffer di ombreggiatura principale.

## <a name="render-the-scene"></a>Eseguire il rendering della scena

Il buffer contenente le ombreggiature è ora associato al pixel shader. Sono disponibili due metodi per la selezione di Cascade implementata nell'esempio CascadedShadowMaps11. Questi due metodi sono illustrati con il codice dello shader.

### <a name="interval-based-cascade-selection"></a>Selezione a catena Interval-Based

**Figura 7. Selezione a catena basata sull'intervallo**

![selezione a catena basata sull'intervallo](images/interval-based-cascade-selection.jpg)

Nella selezione basata sull'intervallo (Figura 7), il vertex shader calcola la posizione nello spazio globale del vertice.


```C++
Output.vDepth = mul( Input.vPosition, m_mWorldView ).z;
```



Il pixel shader riceve la profondità interpolata.


```C++
fCurrentPixelDepth = Input.vDepth;
```



La selezione a catena basata su intervallo usa un confronto vettoriale e un prodotto a virgola per determinare il cacader corretto. Il \_ \_ flag di conteggio a cascata specifica il numero di Cascade. I \_ dati m fCascadeFrustumsEyeSpaceDepths \_ vincolano le partizioni tronco della vista. Dopo il confronto, fComparison contiene un valore pari a 1, dove il pixel corrente è maggiore della barriera e un valore pari a 0 quando la catena corrente è minore. Un prodotto punto somma questi valori in un indice di matrice.


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



Una volta selezionata la clausola CASCADE, la coordinata di trama deve essere trasformata in una sequenza corretta.


```C++
vShadowTexCoord = mul( InterpolatedPosition, m_mShadow[iCascadeIndex] );
```



Questa coordinata di trama viene quindi utilizzata per campionare la trama con la coordinata X e la coordinata Y. La coordinata Z viene utilizzata per eseguire il confronto finale della profondità.

### <a name="map-based-cascade-selection"></a>Selezione a catena Map-Based

Selezione basata su mappa (Figura 8) esegue il test sui quattro lati delle cascate per trovare la mappa più stretta che copre il pixel specifico. Invece di calcolare la posizione nello spazio globale, il vertex shader calcola la posizione dello spazio di visualizzazione per ogni Cascade. Il pixel shader scorre le propagazioni per ridimensionare e spostare le coordinate di trama in modo da indicizzare la Cascade corrente. La coordinata di trama viene quindi testata in base ai limiti della trama. Quando i valori X e Y della coordinata di trama rientrano in un oggetto Cascade, vengono usati per campionare la trama. La coordinata Z viene utilizzata per eseguire il confronto finale della profondità.

**Figura 8. Selezione a catena basata su mappa**

![selezione a catena basata su mappa](images/map-based-cascade-selection.jpg)

### <a name="interval-based-selection-vs-map-based-selection"></a>Selezione Interval-Based e selezione Map-Based

La selezione basata sull'intervallo è leggermente più veloce della selezione basata su mappa perché la selezione a catena può essere eseguita direttamente. La selezione basata su mappa deve intersecare la coordinata di trama con i limiti a cascata.

La selezione basata su mappa usa la cascata in modo più efficiente quando le mappe shadow non sono perfettamente allineate (vedere la figura 8).

## <a name="blend-between-cascades"></a>Blend tra le cascate

VSMs (illustrato più avanti in questo articolo) e le tecniche di filtro, ad esempio PCF, possono essere usate con CSM a bassa risoluzione per produrre ombre morbide. Sfortunatamente, in questo modo si ottiene una linea di giunzione visibile (Figura 9) tra i livelli Cascade, perché la risoluzione non corrisponde. La soluzione consiste nel creare una banda tra le mappe Shadow in cui viene eseguito il test di ombreggiatura per entrambe le cascate. Lo shader esegue quindi l'interpolazione lineare tra i due valori in base alla posizione del pixel nella banda di Blend. Gli esempi CascadedShadowMaps11 e VarianceShadows11 forniscono un dispositivo di scorrimento GUI che può essere usato per aumentare e diminuire questa fascia di sfocatura. Lo shader esegue un ramo dinamico in modo che la maggior parte dei pixel legga solo dalla Cascade corrente.

**Figura 9. Giunzioni a catena**

![giunzioni a catena](images/cascade-seams.jpg)

Sinistra È possibile osservare una Seam visibile in cui si sovrappongono le cascate. Destra Quando si fondono le cascate tra, non viene eseguita alcuna giunzione.

## <a name="filtering-shadow-maps"></a>Filtro delle mappe Shadow

### <a name="pcf"></a>PCF

Il filtro delle mappe Shadow normali non produce ombre morbide e sfocate. L'hardware di filtro offusca i valori di profondità, quindi confronta i valori sfocati con lo spazio chiaro Texel. Il bordo rigido risultante dal test superato/non superato è ancora presente. La sfocatura delle mappe Shadow serve solo per spostare erroneamente il bordo rigido. PCF Abilita l'applicazione di filtri alle mappe Shadow. L'idea generale del PCF consiste nel calcolare una percentuale del pixel nell'ombreggiatura in base al numero di sottocampionamenti che superano il test di profondità sul numero totale di sottocampionati.

L'hardware Direct3D 10 e Direct3D 11 possono eseguire il PCF. L'input per un campionatore PCF è costituito dalla coordinata di trama e da un valore di profondità di confronto. Per semplicità, il PCF viene spiegato con un filtro a quattro tocchi. Il campionatore di trame legge la trama quattro volte, in modo analogo a un filtro standard. Tuttavia, il risultato restituito è una percentuale dei pixel che ha superato il test di profondità. Nella figura 10 viene illustrato come un pixel che passa uno dei quattro test di profondità è pari al 25% nell'ombreggiatura. Il valore effettivo restituito è un'interpolazione lineare basata sulle coordinate del sottotexel delle letture di trama per produrre una sfumatura smussata. Senza questa interpolazione lineare, il PCF a quattro tocchi potrà restituire solo cinque valori: {0,0, 0,25, 0,5, 0,75, 1,0}.

**Figura 10. Immagine filtrata PCF con il 25% del pixel selezionato analizzato**

![immagine filtrata PCF con il 25% del pixel selezionato analizzato](images/pcf-filtered-image.png)

È anche possibile eseguire il PCF senza supporto hardware o estendere il PCF ai kernel più grandi. Alcune tecniche si campionano anche con un kernel ponderato. A tale scopo, creare un kernel, ad esempio un controllo gaussiana, per una griglia N × N. I pesi devono essere aggiunti fino a 1. La trama viene quindi campionata N2 volte. Ogni esempio viene ridimensionato in base ai pesi corrispondenti nel kernel. L'esempio CascadedShadowMaps11 usa questo approccio.

### <a name="depth-bias"></a>Distorsione profondità

La distorsione della profondità diventa ancora più importante quando vengono usati kernel PCF di grandi dimensioni. È valido solo per confrontare la profondità dello spazio chiaro di un pixel rispetto al pixel a cui viene eseguito il mapping nella mappa di profondità. Gli elementi adiacenti della mappa di profondità fanno riferimento a una posizione diversa. Questa profondità è probabilmente simile, ma può essere molto diversa a seconda della scena. Nella figura 11 sono evidenziati gli artefatti che si verificano. Una singola profondità viene confrontata con tre Texel adiacenti nella mappa Shadow. Uno dei test di profondità non riesce in modo errato perché la profondità non è correlata alla profondità di spazio chiaro calcolata della geometria corrente. La soluzione consigliata per questo problema consiste nell'usare un offset maggiore. Troppo grande di un offset, tuttavia, può portare a Peter panning. Il calcolo di un piano vicino e di un piano molto vicino contribuisce a ridurre gli effetti dell'utilizzo di un offset.

**Figura 11. Ombreggiatura errata**

![ombreggiatura errata](images/erroneous-self-shadowing.png)

I risultati con ombreggiatura errata dal confronto tra i pixel nella profondità dello spazio chiaro e i Texel nella mappa Shadow che non sono correlati. La profondità nello spazio chiaro è correlata all'ombreggiatura di Texel 2 nella mappa di profondità. Texel 1 è maggiore della profondità dello spazio chiaro mentre 2 è uguale e 3 è minore. Texels 2 e 3 superano il test di profondità, mentre Texel 1 ha esito negativo.

### <a name="calculating-a-per-texel-depth-bias-with-ddx-and-ddy-for-large-pcfs"></a>Calcolo di un Per-Texel bias di profondità con DDX e DDY per PCFs di grandi dimensioni

Il calcolo di una distorsione di profondità di Texel con **DDX** e **ddy** per PCFS di grandi dimensioni è una tecnica che calcola la distorsione della profondità corretta, supponendo che la superficie sia piana, per la mappa shadow di Texel.

Questa tecnica consente di adattare la profondità di confronto a un piano usando le informazioni derivate. Poiché questa tecnica è complessa dal punto di vista del calcolo, è consigliabile utilizzarla solo quando una GPU dispone di cicli di calcolo da riservare. Quando si usano kernel di grandi dimensioni, può trattarsi dell'unica tecnica che consente di rimuovere gli artefatti di ombreggiatura automatica senza causare la Panoramica di Peter.

Nella figura 12 viene evidenziato il problema. La profondità nello spazio chiaro è nota per un Texel che viene confrontato. Le profondità dello spazio chiaro che corrispondono ai Texel adiacenti nella mappa di profondità sono sconosciute.

**Figura 12. Mappa della scena e della profondità**

![Mappa della scena e della profondità](images/scene-and-depth-map.png)

La scena di cui è stato eseguito il rendering viene visualizzata a sinistra e la mappa di profondità con un blocco Texel di esempio viene visualizzata a destra. Il Texel dello spazio occhio viene mappato al pixel con etichetta D al centro del blocco. Questo confronto è accurato. Il livello di dettaglio corretto nello spazio degli occhi correlato ai pixel che l'elemento adiacente D è sconosciuto. È possibile eseguire il mapping dei Texel adiacenti allo spazio degli occhi solo se si presuppone che il pixel sia relativo allo stesso triangolo di D.

La profondità è nota per il Texel che è correlato alla posizione dello spazio chiaro. La profondità è sconosciuta per i Texel adiacenti nella mappa di profondità.

A livello generale, questa tecnica usa le operazioni **DDX** e **ddy** HLSL per trovare il derivato della posizione di spazio chiaro. Questo non è semplice perché le operazioni derivate restituiscono la sfumatura della profondità dello spazio chiaro rispetto allo spazio dello schermo. Per eseguire la conversione in una sfumatura della profondità dello spazio chiaro rispetto allo spazio chiaro, è necessario calcolare una matrice di conversione.

### <a name="explanation-with-shader-code"></a>Spiegazione con il codice dello shader

I dettagli del resto dell'algoritmo vengono forniti come spiegazione del codice dello shader che esegue questa operazione. Questo codice è disponibile nell'esempio CascadedShadowMaps11. Nella figura 13 viene illustrato il mapping tra le coordinate della trama con spazio chiaro e la mappa di profondità e il modo in cui i derivati in X e Y possono essere utilizzati per creare una matrice di trasformazione.

**Figura 13. Schermo-spazio per la matrice di spazio chiaro**

![schermo-spazio per la matrice di spazio chiaro](images/screen-space-to-light-space-matrix.png)

Per creare questa matrice vengono usati i derivati della posizione di spazio chiaro in X e Y.

Il primo passaggio consiste nel calcolare il derivato della posizione dello spazio di visualizzazione chiara.


```C++
          float3 vShadowTexDDX = ddx (vShadowMapTextureCoordViewSpace);
          float3 vShadowTexDDY = ddy (vShadowMapTextureCoordViewSpace);
```



Le GPU di classe Direct3D 11 calcolano questi derivati eseguendo 2 × 2 Quad di pixel in parallelo e sottraendo le coordinate di trama dal vicino in X per **DDX** e dal router adiacente in Y per **ddy**. Questi due derivati costituiscono le righe di una matrice 2 × 2. Nella forma corrente, questa matrice può essere usata per convertire i pixel adiacenti dello spazio dello schermo a pendii di spazio chiaro. Tuttavia, l'inverso di questa matrice è necessario. Una matrice che trasforma i pixel adiacenti dello spazio su schermo è necessaria.


```C++
          float2x2 matScreentoShadow = float2x2( vShadowTexDDX.xy, vShadowTexDDY.xy );
          float fInvDeterminant = 1.0f / fDeterminant;

          float2x2 matShadowToScreen = float2x2 (
          matScreentoShadow._22 * fInvDeterminant,
          matScreentoShadow._12 * -fInvDeterminant,
          matScreentoShadow._21 * -fInvDeterminant,
          matScreentoShadow._11 * fInvDeterminant );
```



**Figura 14. Spazio leggero sullo schermo**

![spazio leggero sullo schermo](images/light-space-to-screen-space.png)

Questa matrice viene quindi utilizzata per trasformare i due Texel sopra e a destra del Texel corrente. Questi vicini sono rappresentati come offset dal Texel corrente.


```C++
          float2 vRightShadowTexelLocation = float2( m_fTexelSize, 0.0f );
          float2 vUpShadowTexelLocation = float2( 0.0f, m_fTexelSize );
          float2 vRightTexelDepthRatio = mul( vRightShadowTexelLocation,
          matShadowToScreen );
          float2 vUpTexelDepthRatio = mul( vUpShadowTexelLocation,
          matShadowToScreen );
```



Il rapporto creato dalla matrice viene infine moltiplicato per i derivati di profondità per calcolare gli offset di profondità per i pixel adiacenti.


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



## <a name="pcf-and-csms"></a>PCF e CSM

Il PCF non funziona sulle matrici di trama in Direct3D 10. Per usare PCF, tutte le cascate vengono archiviate in un unico Atlante di trama di grandi dimensioni.

### <a name="derivative-based-offset"></a>Offset Derivative-Based

L'aggiunta degli offset basati su derivati per CSM presenta alcune problemi. Ciò è dovuto a un calcolo derivato all'interno del controllo di flusso divergente. Il problema si verifica a causa di una modalità fondamentale di funzionamento delle GPU. Le GPU Direct3D11 funzionano su 2 × 2 Quad di pixel. Per eseguire una derivata, le GPU in genere sottraggono la copia del pixel corrente di una variabile dalla copia del pixel adiacente della stessa variabile. Il modo in cui questa situazione si verifica varia da GPU a GPU. Le coordinate di trama sono determinate dalla selezione a catena basata su mapping o basata sull'intervallo. Alcuni pixel in un quad pixel scelgono una catena diversa rispetto al resto dei pixel. In questo modo si ottiene una giunzione visibile tra le mappe Shadow perché gli offset basati sulla derivazione sono ora completamente errati. La soluzione consiste nell'eseguire il derivato dalle coordinate di trama dello spazio di visualizzazione chiara. Queste coordinate sono le stesse per ogni catena.

### <a name="padding-for-pcf-kernels"></a>Spaziatura interna per i kernel PCF

Indice dei kernel PCF esterno a una partizione Cascade se il buffer ombreggiato non viene riempito. La soluzione consiste nel riempire il bordo esterno della cascata di una metà della dimensione del kernel PCF. Questa operazione deve essere implementata nello shader che seleziona Cascade e nella matrice di proiezione che deve eseguire il rendering della dimensione a cascata sufficiente che il bordo venga mantenuto.

## <a name="variance-shadow-maps"></a>Mappe Shadow varianza

VSMs (per altre informazioni, vedere [mappe shadow di varianza](https://portal.acm.org/citation.cfm?doid=1111411.1111440) per Donnelly e Lauritzen). Quando si usa VSMs, è possibile usare tutte le potenzialità dell'hardware di filtro della trama. È possibile utilizzare il filtro trilineare e anisotropico (Figura 15). Inoltre, VSMs può essere offuscato direttamente tramite convoluzione. VSMs presentano alcuni svantaggi; è necessario archiviare due canali di dati di profondità (profondità e profondità al quadrato). Quando le ombre si sovrappongono, l'emorragia chiara è comune. Funzionano bene, tuttavia, con risoluzioni inferiori e possono essere combinate con CSM.

**Figura 15. Filtro anisotropico**

![filtro anisotropico](images/anisotropic-filtering.png)

### <a name="algorithm-details"></a>Informazioni sugli algoritmi

VSMs funziona eseguendo il rendering della profondità e della profondità quadrata in una mappa Shadow a due canali. Questa mappa Shadow a due canali può quindi essere sfocata e filtrata come una trama normale. L'algoritmo usa quindi la disuguaglianza di Chebychev nel pixel shader per stimare la frazione dell'area pixel che supera il test di profondità.

Il pixel shader recupera i valori di profondità e quadratini di profondità.


```C++
        float  fAvgZ  = mapDepth.x; // Filtered z
        float  fAvgZ2 = mapDepth.y; // Filtered z-squared
```



Viene eseguito il confronto di profondità.


```C++
        if ( fDepth <= fAvgZ )
        {
        fPercentLit = 1;
        }
```



Se il confronto di profondità ha esito negativo, si stima la percentuale del pixel illuminato. La varianza viene calcolata come media dei quadrati meno quadrati di media.


```C++
        float variance = ( fAvgZ2 ) − ( fAvgZ * fAvgZ );
        variance = min( 1.0f, max( 0.0f, variance + 0.00001f ) );
```



Il valore fPercentLit è stimato con la disuguaglianza di Chebychev.


```C++
        float mean           = fAvgZ;
        float d              = fDepth - mean;
        float fPercentLit    = variance / ( variance + d*d );
```



## <a name="light-bleeding"></a>Sanguinamento chiaro

Lo svantaggio più grande per VSMs è la perdita di luce (Figura 16). Lo spurgo chiaro si verifica quando più cast di ombreggiatura si occludere a vicenda lungo i bordi. VSMs ombreggiare i bordi delle ombreggiature in base a differenze di profondità. Quando le ombre si sovrappongono le une alle altre, esiste una disparità di profondità al centro di un'area che deve essere ombreggiata. Si tratta di un problema relativo all'uso dell'algoritmo VSM.

**Figura 16. VSM Light Bleeding**

![VSM Light Bleeding](images/vsm-light-bleeding.png)

Una soluzione parziale al problema consiste nell'elevare il fPercentLit a una potenza. Questo ha l'effetto di smorzare la sfocatura, che può causare artefatti in cui la disparità della profondità è ridotta. In alcuni casi esiste un valore magico che attenua il problema.


```C++
fPercentLit = pow( p_max, MAGIC_NUMBER );
```



Un'alternativa a elevare la percentuale di illuminazione a una potenza consiste nell'evitare configurazioni in cui si sovrappongono le ombreggiature. Anche le configurazioni Shadow altamente ottimizzate presentano diversi vincoli su luce, fotocamera e geometria. Il Bleeding chiaro viene inoltre ridotto utilizzando trame di risoluzione superiore.

Le mappe shadow di varianza a più livelli (LVSMs) consentono di risolvere il problema a scapito della suddivisione del tronco in livelli perpendicolari alla luce. Il numero di mappe necessarie è molto grande quando vengono usate anche CSM.

Inoltre, Andrew Lauritzen, co-autore del documento su VSMs e autore di un documento su LVSMs, ha discusso la combinazione di mappe Shadow esponenziali (ESMs) con VSMs per contrastare la fusione chiara in un [Forum di Beyond3D](https://forum.beyond3d.com/showthread.php?t=47427).

## <a name="vsms-with-csms"></a>VSMs con CSM

Il VarianceShadow11 di esempio combina VSMs e CSM. La combinazione è piuttosto semplice. L'esempio segue gli stessi passaggi dell'esempio CascadedShadowMaps11. Poiché il PCF non viene usato, le ombreggiature vengono sfocate in una convoluzione bidirezionale con due passaggi. La mancata utilizzo di PCF consente inoltre all'esempio di utilizzare matrici di trama anziché un Atlante di trama. Il PCF sulle matrici di trame è una funzionalità di Direct3D 10,1.

### <a name="gradients-with-csms"></a>Gradienti con CSM

L'uso di gradienti con CSM può produrre un Seam lungo il bordo tra due cascate, come illustrato nella figura 17. L'istruzione di esempio usa i derivati tra i pixel per calcolare le informazioni, ad esempio il livello mipmap, necessario per il filtro. Questo causa un problema in particolare per la selezione di mipmap o l'applicazione di filtri anisotropico. Quando i pixel in un quad accettano rami diversi nello shader, i derivati calcolati dall'hardware della GPU non sono validi. In questo modo si ottiene una cucitura irregolare lungo la mappa Shadow.

**Figura 17. Seam sui bordi a cascata a causa del filtro anisotropico con controllo di flusso divergente**

![Seam sui bordi a cascata a causa del filtro anisotropico con controllo di flusso divergente](images/seams-on-cascade-borders-due-to-anisotropic.jpg)

Questo problema viene risolto calcolando i derivati sulla posizione nello spazio di visualizzazione chiaro; la coordinata dello spazio di visualizzazione chiara non è specifica per la Cascade selezionata. I derivati calcolati possono essere ridimensionati in base alla parte della scala della matrice di proiezione e al livello di mipmap corretto.


```C++
        float3 vShadowTexCoordDDX = ddx( vShadowMapTextureCoordViewSpace );
        vShadowTexCoordDDX *= m_vCascadeScale[iCascade].xyz;
        float3 vShadowTexCoordDDY = ddy( vShadowMapTextureCoordViewSpace );
        vShadowTexCoordDDY *= m_vCascadeScale[iCascade].xyz;

        mapDepth += g_txShadow.SampleGrad( g_samShadow, vShadowTexCoord.xyz,
        vShadowTexCoordDDX, vShadowTexCoordDDY );
```



## <a name="vsms-compared-to-standard-shadows-with-pcf"></a>VSMs rispetto alle ombreggiature standard con PCF

Sia VSMs che PCF tentano di approssimare la frazione dell'area pixel che supera il test di profondità. VSMs funzionano con i filtri hardware e possono essere confusi con i kernel separabili. I kernel di convoluzione separabili sono molto più economici da implementare rispetto a un kernel completo. Inoltre, VSMs confronta una profondità di spazio leggero rispetto a un valore nella mappa di profondità dello spazio chiaro. Ciò significa che VSMs non ha gli stessi problemi di offset del PCF. Tecnicamente, la VSMs è la profondità di campionamento in un'area più ampia, oltre a eseguire un'analisi statistica. Questo è meno preciso del PCF. In pratica, VSMs esegue un ottimo processo di blending, con conseguente minore offset necessario. Come descritto in precedenza, il numero uno svantaggio di VSMs è il sanguinamento chiaro.

VSMs e PCF rappresentano un compromesso tra la potenza di calcolo GPU e la larghezza di banda della trama GPU. VSMs richiede un maggior numero di operazioni matematiche da eseguire per calcolare la varianza. Il PCF richiede una larghezza di banda di memoria più trama. I kernel PCF di grandi dimensioni possono diventare rapidamente un collo di bottiglia con la larghezza di banda della trama. Con la crescita più rapida del calcolo della GPU rispetto alla larghezza di banda della GPU, VSMs sta diventando il più pratico dei due algoritmi. VSMs inoltre un aspetto migliore con le mappe Shadow a risoluzione inferiore a causa della fusione e del filtro.

## <a name="summary"></a>Riepilogo

CSM offrono una soluzione al problema di aliasing della prospettiva. Esistono diverse configurazioni possibili per ottenere la fedeltà visiva necessaria per un titolo. PCF e VSMs sono ampiamente usati e devono essere combinati con CSM per ridurre l'aliasing.

## <a name="references"></a>Riferimenti

Donnelly, W. e Lauritzen, A. [varianza Maps](https://portal.acm.org/citation.cfm?doid=1111411.1111440). In SI3D '06: procedure del Simposio 2006 su grafica e giochi 3D interattivi. 2006. pp. 161 – 165. New York, NY, USA: ACM Press.

Lauritzen, Andrew e McCool, Michael. [Mappe shadow di varianza](https://portal.acm.org/citation.cfm?id=1375714.1375739&coll=GUIDE&dl=GUIDE&CFID=45360327&CFTOKEN=34578992)a più livelli. Procedure di interfaccia grafica 2008, 28-30, 2008, Windsor, Ontario, Canada.

Engel, Woflgang F. sezione 4. Mappe Shadow a cascata. ShaderX5, Advanced rendering Techniques, Wolfgang F. Engel, ed. Charles River Media, Boston, Massachusetts. 2006. pp. 197 – 206.

 

 