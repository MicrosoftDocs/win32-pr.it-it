---
title: Regole di rasterizzazione
description: Le regole di rasterizzazione definiscono la modalità di mapping dei dati vettoriali nei dati raster.
ms.assetid: 2b3894eb-dff3-401f-8b14-4af98db86e39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e256c6fc171c1cce9b63b79fac6a480e507a306e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399060"
---
# <a name="rasterization-rules"></a>Regole di rasterizzazione

Le regole di rasterizzazione definiscono la modalità di mapping dei dati vettoriali nei dati raster. I dati raster vengono bloccati in posizioni intere che vengono quindi rimosse e ritagliate (per tracciare il numero minimo di pixel) e gli attributi per pixel vengono interpolati (dagli attributi per vertice) prima di essere passati a una pixel shader.

Esistono diversi tipi di regole, che dipendono dal tipo di primitivo di cui è in corso il mapping, nonché dal fatto che i dati utilizzino il campionamento multiplo per ridurre l'aliasing. Nelle illustrazioni seguenti viene illustrato come vengono gestiti i casi d'angolo.

-   [Regole di rasterizzazione triangolari (senza campionamento multiplo)](#triangle-rasterization-rules-without-multisampling)
-   [Regole di rasterizzazione delle righe (con alias, senza campionamento multiplo)](#line-rasterization-rules-aliased-without-multisampling)
-   [Regole di rasterizzazione delle righe (antialiasing, senza campionamento multiplo)](#line-rasterization-rules-antialiased-without-multisampling)
-   [Regole di rasterizzazione punti (senza campionamento multiplo)](#point-rasterization-rules-without-multisampling)
-   [Regole di rasterizzazione di anti-aliasing multicampionamento](#multisample-anti-aliasing-rasterization-rules)
    -   [Supporto hardware](#hardware-support)
    -   [Campionamento centrale degli attributi durante l'anti-aliasing di multicampionamento](#centroid-sampling-of-attributes-when-multisample-antialiasing)
    -   [Calcoli derivati durante il campionamento multiplo](#derivative-calculations-when-multisampling)
-   [Argomenti correlati](#related-topics)

## <a name="triangle-rasterization-rules-without-multisampling"></a>Regole di rasterizzazione triangolari (senza campionamento multiplo)

Ogni pixel Center che si trova all'interno di un triangolo viene disegnato; si presuppone che un pixel si trovi all'interno di se passa la regola in alto a sinistra. La regola in alto a sinistra è la definizione di un pixel Center che si trova all'interno di un triangolo se si trova sul bordo superiore o sul bordo sinistro di un triangolo.

Dove:

-   Un bordo superiore è un bordo esattamente orizzontale ed è sopra gli altri bordi.
-   Un bordo sinistro è un bordo che non è esattamente orizzontale e si trova sul lato sinistro del triangolo. Un triangolo può avere uno o due bordi A sinistra.

La regola in alto a sinistra garantisce che i triangoli adiacenti vengano disegnati una sola volta.

Questa illustrazione mostra esempi di pixel che vengono disegnati perché si trovano all'interno di un triangolo o seguono la regola in alto a sinistra.

![illustrazione degli esempi di rasterizzazione del triangolo superiore sinistro](images/d3d10-rasterrulestriangle.png)

Il rivestimento grigio chiaro e scuro dei pixel li Mostra come gruppi di pixel per indicare il triangolo in cui si trovano.

## <a name="line-rasterization-rules-aliased-without-multisampling"></a>Regole di rasterizzazione delle righe (con alias, senza campionamento multiplo)

Le regole di rasterizzazione delle righe utilizzano un'area di test di diamanti per determinare se una linea copre un pixel. Per le righe x-Major (righe con-1 <= Slope <= + 1), l'area di test Diamond include (mostrata Solid) il bordo inferiore sinistro, il bordo inferiore destro e l'angolo inferiore; il rombo esclude (visualizzato punteggiato) il bordo superiore sinistro, il bordo superiore destro, il cordoncino superiore, l'angolo sinistro e l'angolo destro. Una riga y-Major è una riga che non è una linea x-Major; l'area dei diamanti del test è uguale a quella descritta per la riga x-Major, a eccezione dell'angolo destro.

Data l'area Diamond, una linea copre un pixel se la riga esce dall'area di test del rombo del pixel quando si viaggia lungo la linea dall'inizio verso la fine. Una striscia di linea si comporta allo stesso modo, poiché viene disegnata come una sequenza di righe.

Nella figura seguente vengono illustrati alcuni esempi.

![illustrazione degli esempi di rasterizzazione di righe con alias](images/d3d10-rasterrulesline.png)

## <a name="line-rasterization-rules-antialiased-without-multisampling"></a>Regole di rasterizzazione delle righe (antialiasing, senza campionamento multiplo)

Una linea con antialias viene rasterizzata come se fosse un rettangolo (con larghezza = 1). Il rettangolo si interseca con una destinazione di rendering che produce valori di code coverage per pixel, moltiplicati in pixel shader componenti alfa di output. Quando si disegnano linee in una destinazione di rendering multicampionata, non è presente alcun anti-aliasing.

Si ritiene che non esista un unico modo "migliore" per eseguire il rendering di linee con anti-aliasing. Direct3D 10 adotta come linea guida il metodo illustrato nella figura seguente. Questo metodo è stato derivato empiricamente, mostrando un certo numero di proprietà visive ritenute desiderabili. L'hardware non deve corrispondere esattamente a questo algoritmo; i test rispetto a questo riferimento avranno tolleranze "ragionevoli", seguiti da alcuni dei principi elencati più avanti, permettendo diverse implementazioni hardware e filtrare le dimensioni del kernel. Nessuna di questa flessibilità consentita nell'implementazione dell'hardware, tuttavia, può essere comunicata attraverso Direct3D 10 alle applicazioni, oltre a disegnare semplicemente linee e osservare/misurare il modo in cui appaiono.

![illustrazione degli esempi di rasterizzazione di linee con anti-aliasing](images/d3d10-rasterruleslineaa.png)

Questo algoritmo genera linee relativamente smussate, con intensità uniforme, con bordi o trecce minime. La modellazione dell'effetto moiré per le linee di chiusura è ridotta a icona. Esiste una corretta copertura per le giunzioni tra segmenti di linea posizionati end-to-end. Il kernel di filtro è un ragionevole compromesso tra la quantità di sfocatura perimetrale e le modifiche di intensità causata da correzioni gamma. Il valore di code coverage viene moltiplicato in pixel shader o0. a (srcAlpha) per la formula seguente dalla fase di Unione dell'output: srcColor \* srcAlpha + destColor \* (1-srcAlpha).

## <a name="point-rasterization-rules-without-multisampling"></a>Regole di rasterizzazione punti (senza campionamento multiplo)

Un punto viene interpretato come se fosse costituito da due triangoli in un modello Z, che usano le regole di rasterizzazione dei triangoli. La coordinata identifica il centro di un quadrato in larghezza di un pixel. Non esiste alcun abbattimento per i punti.

Nella figura seguente vengono illustrati alcuni esempi.

![illustrazione degli esempi di rasterizzazione dei punti](images/d3d10-rasterrulespoint.png)

## <a name="multisample-anti-aliasing-rasterization-rules"></a>Regole di rasterizzazione di anti-aliasing multicampionamento

L'anti-aliasing di multicampionamento consente di ridurre gli alias di geometria usando il code coverage dei pixel e i test di stencil depth in più percorsi di sottocampionamento. Per migliorare le prestazioni, i calcoli per pixel vengono eseguiti una volta per ogni pixel coperto, condividendo gli output dello shader tra i sub-pixel coperti. L'anti-aliasing multicampionamento non riduce l'aliasing della superficie. Le posizioni di esempio e le funzioni di ricostruzione dipendono dall'implementazione dell'hardware.

Nella figura seguente vengono illustrati alcuni esempi.

![illustrazione degli esempi di rasterizzazione antialias multicampionamento](images/d3d10-rasterrulesmsaa.png)

Il numero di percorsi di esempio dipende dalla modalità multicampionamento. Gli attributi dei vertici vengono interpolati in pixel Center, perché si tratta del punto in cui viene richiamata la pixel shader (questo diventa un'estrapolazione se il centro non viene analizzato). Gli attributi possono essere contrassegnati nel pixel shader come centro campionato, che fa sì che i pixel non coperti interpolano l'attributo all'intersezione dell'area del pixel e della primitiva. Viene eseguito un pixel shader per ogni area del pixel 2x2 per supportare calcoli derivati (che usano Delta x e y). Ciò significa che le chiamate dello shader si verificano più di quanto venga visualizzato per compilare il numero minimo di 2x2, che è indipendente dal campionamento multiplo. Il risultato dello shader viene scritto per ogni esempio coperto che supera il test di stencil profondità per campione.

Le regole di rasterizzazione per le primitive sono, in generale, invariate dall'anti-aliasing multicampione, tranne:

-   Per un triangolo, viene eseguito un test di code coverage per ogni posizione di esempio (non per un pixel Center). Se viene analizzato più di un percorso di esempio, un pixel shader viene eseguito una volta con gli attributi interpolati al centro pixel. Il risultato viene archiviato (replicato) per ogni percorso di esempio coperto nel pixel che supera il test di profondità/stencil.

    Una linea viene considerata come un rettangolo costituito da due triangoli, con una lunghezza di riga di 1,4.

-   Per un punto, viene eseguito un test di code coverage per ogni percorso di esempio (non per un pixel Center).

Molti formati supportano il campionamento multiplo (vedere [supporto hardware per i formati Direct3D 10](/previous-versions//cc627090(v=vs.85))). è possibile risolvere alcuni formati ([**ResolveSubresource**](/windows/desktop/api/d3d10/nf-d3d10-id3d10device-resolvesubresource), che downsampling delle un formato multicampionato a una dimensione di esempio di 1). I formati di campionamento multiplo possono essere usati nelle destinazioni di rendering che possono essere letti in shader usando [Load](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-load), perché non è richiesta alcuna risoluzione per i singoli esempi a cui si accede dallo shader. I formati di profondità non sono supportati per la risorsa multisample, quindi i formati di profondità sono limitati solo alle destinazioni di rendering.

I formati con tipi (R8G8B8A8 \_ , ad esempio) supportano il campionamento multiplo per consentire a una visualizzazione risorse di interpretare i dati in modi diversi. Ad esempio, è possibile creare una risorsa multisample usando il \_ tipo R8G8B8A8, eseguirne il rendering usando una risorsa render-target-View con un \_ formato R8G8B8A8 uint, quindi risolvere il contenuto in un'altra risorsa con un \_ formato dati R8G8B8A8 UNORM.

### <a name="hardware-support"></a>Supporto hardware

L'API segnala il supporto hardware per il campionamento multiplo attraverso il numero di livelli qualitativi. Ad esempio, un livello di qualità 0 indica che l'hardware non supporta il campionamento multiplo (con un formato e un livello di qualità particolari). 3 per i livelli di qualità significa che l'hardware supporta tre diversi layout di esempio e/o Risolvi gli algoritmi. È anche possibile presupporre quanto segue:

-   Qualsiasi formato che supporta il campionamento multiplo supporta lo stesso numero di livelli di qualità per ogni formato di tale famiglia.
-   Ogni formato che supporta il campionamento multiplo e presenta i \_ formati UNORM, \_ sRGB, \_ russa o \_ float, supporta anche la risoluzione.

### <a name="centroid-sampling-of-attributes-when-multisample-antialiasing"></a>Campionamento centrale degli attributi durante l'anti-aliasing di multicampionamento

Per impostazione predefinita, gli attributi dei vertici vengono interpolati in un centro pixel durante l'anti-aliasing di multicampionamento. Se il pixel Center non viene analizzato, gli attributi vengono estrapolati in un centro pixel. Se un pixel shader input che contiene la semantica del centro (presupponendo che il pixel non è completamente coperto) verrà campionato in un punto all'interno dell'area coperta del pixel, possibilmente in una delle posizioni di esempio coperte. Una maschera di esempio (specificata dallo stato di rasterizzazione) viene applicata prima del calcolo del baricentro. Pertanto, un campione mascherato non verrà usato come posizione centrale.

L'rasterizzatore di riferimento sceglie un percorso di esempio per il campionamento del baricentro simile al seguente:

-   La maschera di esempio consente tutti gli esempi. Usare un pixel Center se il pixel è coperto o se nessuno degli esempi è coperto. In caso contrario, viene scelto il primo campione incluso, a partire dal centro pixel e spostandosi verso l'esterno.
-   La maschera di esempio disattiva tutti gli esempi, ma uno (uno scenario comune). Un'applicazione può implementare il supercampionamento MultiPASS scorrendo i valori della maschera di esempio a singolo bit ed eseguendo nuovamente il rendering della scena per ogni esempio usando il campionamento del centro. Per questa operazione è necessario che un'applicazione modifichi i derivati per selezionare la texture MIPS più dettagliata in modo appropriato per una maggiore densità di campionamento della trama.

### <a name="derivative-calculations-when-multisampling"></a>Calcoli derivati durante il campionamento multiplo

I pixel shader vengono sempre eseguiti usando un'area minima di 2x2 pixel per supportare calcoli derivati, che vengono calcolati mediante l'acquisizione di Delta tra dati provenienti da pixel adiacenti (presupponendo che i dati in ogni pixel siano stati campionati con spaziatura tra unità orizzontalmente o verticalmente). Questo non è influenzato dal campionamento multiplo.

Se vengono richiesti derivati su un attributo che è stato utilizzato per il baricentro, il calcolo hardware non viene regolato, che può causare derivati non accurati. Uno shader prevede un vettore di unità nello spazio di destinazione di rendering, ma può ottenere un vettore non di unità in relazione a un altro spazio vettoriale. Pertanto, è responsabilità dell'applicazione prestare attenzione quando si richiedono derivati dagli attributi campionati. Infatti, è consigliabile non combinare i derivati e il campionamento del centro. Il campionamento centrale può essere utile per situazioni in cui è fondamentale che gli attributi interpolati di una primitiva non vengano estrapolati, ma questo avviene con compromessi come gli attributi che sembrano saltare dove un bordo primitivo interseca un pixel, anziché modificare continuamente, o derivati che non possono essere usati da operazioni di campionamento di trama che derivano da LOD.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Fase Rasterizzazione](d3d10-graphics-programming-guide-rasterizer-stage.md)
</dt> </dl>

 

 