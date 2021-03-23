---
title: Rasterizzazione conservativa Direct3D 12
description: La rasterizzazione conservativa aggiunge una certa certezza al rendering in pixel, che risulta utile in particolare per gli algoritmi di rilevamento dei conflitti.
ms.assetid: 081199AD-1702-4EC8-95AD-B1148C676199
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e4fae3489d54ab7b6b7abfda56f54dd8d970962
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/23/2019
ms.locfileid: "104548899"
---
# <a name="direct3d-12-conservative-rasterization"></a>Rasterizzazione conservativa Direct3D 12

La rasterizzazione conservativa aggiunge una certa certezza al rendering in pixel, che risulta utile in particolare per gli algoritmi di rilevamento dei conflitti.

-   [Overview](#overview)
-   [Interazioni con la pipeline](#interactions-with-the-pipeline)
    -   [Interazione tra regole di rasterizzazione](#rasterization-rules-interaction)
    -   [Interazione multicampionamento](#multisampling-interaction)
    -   [Interazione SampleMask](#samplemask-interaction)
    -   [Interazione test profondità/stencil](#depthstencil-test-interaction)
    -   [Interazione con i pixel Helper](#helper-pixel-interaction)
    -   [Interazione di code coverage output](#output-coverage-interaction)
    -   [Interazione InputCoverage](#inputcoverage-interaction)
    -   [Interazione InnerCoverage](#innercoverage-interaction)
    -   [Interazione con l'interpolazione degli attributi](#attribute-interpolation-interaction)
    -   [Interazione di ritaglio](#clipping-interaction)
    -   [Interazione della distanza tra clip](#clip-distance-interaction)
    -   [Interazione di rasterizzazione indipendente di destinazione](#target-independent-rasterization-interaction)
    -   [Interazione della topologia primitiva IA](#ia-primitive-topology-interaction)
    -   [Interazione tra query](#query-interaction)
    -   [Interazione stato di eliminazione](#cull-state-interaction)
    -   [Interazione IsFrontFace](#isfrontface-interaction)
    -   [Interazione modalità di riempimento](#fill-modes-interaction)
-   [Dettagli di implementazione](#implementation-details)
-   [Riepilogo API](#api-summary)
-   [Argomenti correlati](#related-topics)

## <a name="overview"></a>Panoramica

La rasterizzazione conservativa indica che tutti i pixel almeno parzialmente coperti da una primitiva sottoposta a rendering vengono rasterizzati, il che significa che il pixel shader viene richiamato. Il comportamento normale è il campionamento, che non viene usato se è abilitata la rasterizzazione conservativa.

La rasterizzazione conservativa è utile in diverse situazioni, tra cui la certezza del rilevamento dei conflitti, l'abbattimento dell'occlusione e il rendering affiancato.

Ad esempio, la figura seguente mostra un triangolo verde sottoposto a rendering usando la rasterizzazione conservativa, così come verrebbe visualizzato nel rasterizzatore (ovvero usando le coordinate del vertice a virgola fissa 16,8). L'area marrone è nota come "area di incertezza", un'area concettuale che rappresenta i limiti estesi del triangolo, necessari per garantire che la primitiva nell'rasterizzatore sia conservativa rispetto alle coordinate iniziali del vertice a virgola mobile. I quadratini rossi in ogni vertice mostrano come viene calcolata l'area di incertezza: come un quadrato con sweep.

I quadrati grigi di grandi dimensioni mostrano i pixel di cui verrà eseguito il rendering. I quadrati rosa mostrano i pixel sottoposti a rendering usando la regola in alto a sinistra, che entra in gioco quando il bordo del triangolo supera il bordo dei pixel. È possibile che siano presenti falsi positivi (pixel impostati che non dovrebbero essere stati), che verranno normalmente rimosse dal sistema, ma non sempre.

![regola in alto a sinistra](images/conservative-rasterization-0.png)

## <a name="interactions-with-the-pipeline"></a>Interazioni con la pipeline

### <a name="rasterization-rules-interaction"></a>Interazione tra regole di rasterizzazione

In modalità di rasterizzazione conservativa, le regole di rasterizzazione si applicano allo stesso modo di quando la modalità di rasterizzazione conservativa non è abilitata con le eccezioni per la regola di Top-Left, descritta sopra e la copertura dei pixel. 16,8 Fixed-Point è necessario utilizzare la precisione del rasterizzatore.

Pixel che non verrebbero analizzati se l'hardware utilizzava le coordinate dei vertici a virgola mobile complete può essere incluso solo se si trovano all'interno di un'area di incertezza non superiore a metà di un pixel nel dominio a virgola fissa. Si prevede che l'hardware futuro raggiunga l'area di incertezza ristretta specificata nel livello 2. Si noti che questo requisito impedisce che i triangoli dei nastri si estendano ulteriormente rispetto al necessario.

Si applica anche un'area di incertezza valida simile `InnerCoverage` , ma è più stretta perché nessuna implementazione richiede un'area di incertezza maggiore per questo caso. Per altri dettagli, vedere [interazione con InnerCoverage](#innercoverage-interaction) .

Le aree di incertezza interna ed esterna devono essere maggiori o uguali alla metà della griglia dei sottopixel, ovvero 1/512 di un pixel, nel dominio a virgola fissa. Questa è l'area minima di incertezza valida. 1/512 deriva dalla rappresentazione della coordinata di rasterizzazione dei punti fissi 16,8 e dalla regola round-to-più vicina che si applica quando si convertono le coordinate dei vertici a virgola mobile in 16,8 Coordinate di punti fisse 1/512 può cambiare se la precisione del rasterizzatore viene modificata. Se un'implementazione implementa questa area minima di incertezza, devono seguire la regola Top-Left quando un bordo o un angolo dell'area di incertezza cade lungo il bordo o l'angolo di un pixel. I bordi ritagliati dell'area di incertezza devono essere considerati come il vertice più vicino, vale a dire che vengono conteggiati come due bordi, ovvero i due che si uniscono al vertice associato. Top-Left regola è obbligatoria quando viene utilizzata l'area di incertezza minima. in caso contrario, un'implementazione di rasterizzazione conservativa non riuscirà a rasterizzare i pixel che potrebbero essere coperti quando la modalità di rasterizzazione conservativa è disabilitata.

Il diagramma seguente illustra un'area di incertezza esterna valida prodotta dalla sweep di un quadrato intorno ai bordi della primitiva nel dominio a virgola fissa, ovvero i vertici sono stati quantizzati dalla rappresentazione a virgola fissa 16,8. Le dimensioni di questo quadrato sono basate sulle dimensioni della regione di incertezza esterna valide: per 1/2 di un pixel, il quadrato è di 1 pixel in larghezza e altezza, per 1/512 di un pixel, il quadrato è 1/256 di un pixel in larghezza e altezza. Il triangolo verde rappresenta una determinata primitiva, la linea rossa tratteggiata rappresenta il limite di rasterizzazione conservativa sovrastimata, i quadrati neri solidi rappresentano il quadrato che viene trascinato lungo i bordi primitivi e l'area a scacchi blu è l'area di incertezza esterna:

![area di incertezza esterna.](images/outercoverage.jpg)

### <a name="multisampling-interaction"></a>Interazione multicampionamento

Indipendentemente dal numero di campioni nelle superfici **renderTarget** / **DepthStencil** (o se *ForcedSampleCount* viene usato o meno), tutti gli esempi vengono analizzati per i pixel rasterizzati dalla rasterizzazione conservativa. I singoli percorsi di esempio non vengono verificati se rientrano nella primitiva o meno.

### <a name="samplemask-interaction"></a>Interazione SampleMask

Lo stato di rasterizzazione *SampleMask* viene applicato allo stesso modo di quando la rasterizzazione conservativa non è abilitata per `InputCoverage` , ma non ha alcun effetto, `InnerCoverage` ovvero non è unire con and in un input dichiarato con `InnerCoverage` . Ciò è dovuto `InnerCoverage` al fatto che non è correlato al fatto che gli esempi MSAA siano mascherati: 0 `InnerCoverage` significa solo che non è garantito che il pixel sia completamente coperto, non che nessun campione verrà aggiornato.

### <a name="depthstencil-test-interaction"></a>Interazione test profondità/stencil

I test depth/stencil procedono per un pixel con rasterizzazione conservativa nello stesso modo in cui vengono analizzati tutti i campioni quando la rasterizzazione conservativa non è abilitata.

L'esecuzione di tutti gli esempi analizzati può causare un'estrapolazione della profondità, che è valida e deve essere fissata al viewport come specificato quando la rasterizzazione conservativa non è abilitata. Questa operazione è simile a quando si utilizzano le modalità di interpolazione con frequenza pixel in un **renderTarget** con numero campione maggiore di 1, anche se nel caso della rasterizzazione conservativa, si tratta del valore di profondità nel test di profondità della funzione fisso che può essere estrapolato.

Il comportamento di eliminazione anticipata con l'estrapolazione della profondità non è definito. Questo è dovuto al fatto che alcuni componenti iniziali di abbandono di profondità non supportano correttamente i valori di profondità estrapolati. Tuttavia, il comportamento di eliminazione anticipata della profondità in presenza di un'estrapolazione approfondita è problematico anche con l'hardware che può supportare i valori di profondità estrapolati. Per risolvere il problema, è possibile bloccare la profondità di input del pixel shader sui valori di profondità minima e massima della primitiva da rasterizzare e scrivere tale valore `oDepth` (il registro di profondità dell'output pixel shader). Le implementazioni sono necessarie per disabilitare l'eliminazione anticipata della profondità in questo caso, a causa della `oDepth` scrittura.

### <a name="helper-pixel-interaction"></a>Interazione con i pixel Helper

Le regole dei pixel Helper si applicano allo stesso modo di quando la rasterizzazione conservativa non è abilitata. Come parte di questa operazione, tutti i pixel, inclusi i pixel helper, devono essere segnalati `InputCoverage` in modo accurato come specificato nella `InputCoverage` sezione interazione. Il code coverage 0 del report di pixel è completamente non coperto.

### <a name="output-coverage-interaction"></a>Interazione di code coverage output

Il code coverage di output ( `oMask` ) si comporta per un pixel con rasterizzazione conservata, come avviene quando la rasterizzazione conservativa non è abilitata con tutti gli esempi analizzati.

### <a name="inputcoverage-interaction"></a>Interazione InputCoverage

In modalità di rasterizzazione conservativa, questo registro di input viene popolato come se tutti i campioni venissero analizzati quando la rasterizzazione conservativa non è abilitata per un determinato pixel rasterizzato in modo conservativo. Ovvero, vengono applicate tutte le interazioni esistenti (ad esempio, *SampleMask* ) e i primi n bit in `InputCoverage` da LSB vengono impostati su 1 per un pixel rasterizzato in modo conservativo, dato un campione n per pixel **renderTarget** e/o un buffer **DepthStencil** associato alla fusione di **output** oppure un *ForcedSampleCount* n di esempio. Il resto dei bit è 0.

Questo input è disponibile in uno shader indipendentemente dall'uso della rasterizzazione conservativa, sebbene la rasterizzazione conservativa modifichi il comportamento in modo da visualizzare solo tutti gli esempi analizzati (o nessuno per i pixel Helper).

### <a name="innercoverage-interaction"></a>Interazione InnerCoverage

Questa funzionalità è richiesta da e disponibile solo in, livello 3. Il runtime non riuscirà a creare shader per gli shader che usano questa modalità quando un'implementazione supporta un livello inferiore al livello 3.

Il pixel shader ha un valore scalare Integer a 32 bit per generare un valore disponibile: `InnerCoverage` . Si tratta di un campo di bit con bit 0 da LSB impostato su 1 per un determinato pixel rasterizzato in modo conservativo, solo quando tale pixel è garantito interamente all'interno della primitiva corrente. Tutti gli altri bit del registro di input devono essere impostati su 0 quando il bit 0 non è impostato, ma non definiti quando il bit 0 è impostato su 1 (essenzialmente, questo campo di bit rappresenta un valore booleano dove false deve essere esattamente 0, ma true può essere qualsiasi valore diverso da zero (ad esempio, set di bit 0). Questo input viene usato per le informazioni di rasterizzazione conservative sottostimate. Informa il pixel shader se il pixel corrente è completamente all'interno della geometria.

Questo deve tenere conto dell'errore di blocco alle risoluzioni maggiori o uguali alla risoluzione in cui il progetto corrente sta operando. Non devono essere presenti falsi positivi (impostazione `InnerCoverage` bits quando il pixel non è completamente coperto per eventuali errori di blocco a risoluzione maggiori o uguali alla risoluzione in cui è in esecuzione il progetto corrente), ma sono consentiti falsi negativi. In breve, l'implementazione non deve identificare erroneamente i pixel come completamente analizzati e non con coordinate del vertice a virgola mobile complete nel rasterizzatore.

Pixel che verrebbero completamente analizzati se l'hardware utilizzava coordinate del vertice a virgola mobile complete può essere omesso solo se intersecano l'area di incertezza interna, che non deve essere maggiore della dimensione della griglia dei sottopixel, o 1/256 di un pixel, nel dominio a virgola fissa. Detto un altro modo, i pixel interamente all'interno del limite interno dell'area di incertezza interna devono essere contrassegnati come completamente analizzati. Il limite interno dell'area di incertezza è illustrato nel diagramma seguente dalla linea di colore nero in grassetto. 1/256 deriva dalla rappresentazione della coordinata del rasterizzatore dei punti fissi 16,8, che può cambiare se la precisione del rasterizzatore viene modificata. Questa area di incertezza è sufficiente per tenere conto dell'errore di blocco causato dalla conversione delle coordinate dei vertici a virgola mobile in coordinate del vertice a virgola fissa nel rasterizzatore.

Gli stessi requisiti di area minima di incertezza 1/512 definiti nell'interazione delle regole di rasterizzazione si applicano anche qui.

Il diagramma seguente illustra un'area di incertezza interna valida prodotta dalla sweep di un quadrato intorno ai bordi della primitiva nel dominio a virgola fissa, ovvero i vertici sono stati quantizzati dalla rappresentazione a virgola fissa 16,8. Le dimensioni di questo quadrato sono basate sulle dimensioni della regione di incertezza interna valide: per 1/256 di un pixel, il quadrato è 1/128 di un pixel in larghezza e altezza. Il triangolo verde rappresenta una primitiva, la linea punteggiata nera rappresenta il limite dell'area di incertezza interna, i quadrati neri a tinta unita rappresentano il quadrato che viene trascinato lungo i bordi primitivi e l'area a scacchi arancione è l'area di incertezza interna:

![reqion di incertezza interna.](images/innercoverage.jpg)

L'uso di `InnerCoverage` non influisce sul fatto che un pixel venga rasterizzato in modo prudenziale, ovvero l'uso di una di queste `InputCoverage` modalità non influisce sui pixel che vengono rasterizzati quando è abilitata la modalità di rasterizzazione conservativa. Pertanto, quando `InnerCoverage` si usa e il pixel shader sta elaborando un pixel che non è completamente coperto dalla geometria, il valore sarà 0, ma la chiamata al pixel shader avrà esempi aggiornati. Si tratta di un valore diverso da quando `InputCoverage` è 0, pertanto non verrà aggiornato alcun campione.

Questo input si escludono a vicenda `InputCoverage` : non è possibile usare entrambi.

Per accedere a `InnerCoverage` , è necessario dichiararlo come un singolo componente da uno dei registri di input del pixel shader. La modalità di interpolazione nella dichiarazione deve essere costante (l'interpolazione non è applicabile).

Il `InnerCoverage` campo di bit non è influenzato da test depth/stencil, né individuato con lo stato di rasterizzazione *SampleMask* .

Questo input è valido solo in modalità di rasterizzazione conservativa. Quando la rasterizzazione conservativa non è abilitata, `InnerCoverage` produce un valore non definito.

Le chiamate del pixel shader causate dalla necessità di pixel helper, ma in caso contrario non coperte dalla primitiva, devono avere il `InnerCoverage` registro impostato su 0.

### <a name="attribute-interpolation-interaction"></a>Interazione con l'interpolazione degli attributi

Le modalità di interpolazione degli attributi non sono state modificate ed è possibile procedere nello stesso modo in cui la rasterizzazione conservativa non è abilitata, in cui vengono usati i vertici con scalabilità del viewport e con conversione a virgola fissa. Poiché tutti gli esempi in un pixel rasterizzato in modo conservativo sono considerati analizzati, sono validi per i valori da estrapolare, in modo analogo a quando si utilizzano le modalità di interpolazione con frequenza pixel in un **renderTarget** con numero campione maggiore di 1. Le modalità di interpolazione del baricentro producono risultati identici alla modalità di interpolazione non centrale corrispondente. il concetto di centro non è significativo in questo scenario, in cui il code coverage di esempio è pieno o 0.

La rasterizzazione conservativa consente la degenerazione dei triangoli per produrre chiamate pixel shader, pertanto, i triangoli degenerati devono usare i valori assegnati al vertice 0 per tutti i valori interpolati.

### <a name="clipping-interaction"></a>Interazione di ritaglio

Quando è abilitata la modalità di rasterizzazione conservativa e la clip di profondità è disabilitata (quando lo stato di rasterizzazione *DepthClipEnable* è impostato su false), potrebbero esistere variazioni nell'interpolazione degli attributi per i segmenti di una primitiva che non rientrano nell'intervallo 0 <= z <= w, a seconda dell'implementazione: i valori costanti vengono utilizzati da un punto in cui la primitiva interseca il piano pertinente (quasi o lontano) oppure l'interpolazione degli attributi si comporta come se fosse disabilitata la modalità di rasterizzazione conservativa Tuttavia, il comportamento del valore di profondità è lo stesso indipendentemente dalla modalità di rasterizzazione conservativa, ovvero le primitive che non rientrano nell'intervallo di profondità devono comunque avere il valore del limite più vicino all'intervallo di profondità del viewport. Il comportamento di interpolazione degli attributi all'interno dell'intervallo 0 <= z <= w deve rimanere invariato.

### <a name="clip-distance-interaction"></a>Interazione della distanza tra clip

La distanza tra clip è valida quando è abilitata la modalità di rasterizzazione conservativa e si comporta per un pixel con rasterizzazione conservativa, come avviene quando la rasterizzazione conservativa non è abilitata con tutti gli esempi analizzati.

Si noti che la rasterizzazione conservativa può causare l'estrapolazione della coordinata del vertice W, che può causare W <= 0. Ciò può causare l'esecuzione di implementazioni di distanza di ritaglio per pixel in una distanza di clip che è stata divisa da un valore W non valido. Le implementazioni della distanza tra clip devono essere protette dalla richiamata della rasterizzazione per i pixel in cui la coordinata del vertice W <= 0 (ad esempio, a causa dell'estrapolazione in modalità di rasterizzazione conservativa)

### <a name="target-independent-rasterization-interaction"></a>Interazione di rasterizzazione indipendente di destinazione

La modalità di rasterizzazione conservativa è compatibile con la rasterizzazione indipendente di destinazione. Si applicano le regole e le restrizioni TIR, comportando un pixel con rasterizzazione conservata come se fossero analizzati tutti i campioni.

### <a name="ia-primitive-topology-interaction"></a>Interazione della topologia primitiva IA

La rasterizzazione conservativa non è definita per le primitive linea o punto. Pertanto, le topologie primitive che specificano punti o linee producono un comportamento non definito se vengono alimentate all'unità di rasterizzazione quando è abilitata la rasterizzazione conservativa.

La convalida dei livelli di debug verifica che le applicazioni non usino queste topologie primitive.

### <a name="query-interaction"></a>Interazione tra query

Per un pixel rasterizzato in modo conservativo, le query si comportano come se la rasterizzazione conservativa non venisse abilitata quando vengono analizzati tutti i campioni. Ad esempio, per un pixel rasterizzato in modo conservativo \_ , \_ \_ le statistiche della pipeline del tipo di query D3D12 e delle \_ \_ \_ \_ statistiche della pipeline del tipo di query D3D12 (dal [**\_ \_ tipo di query D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_type)) devono comportarsi come se la rasterizzazione conservativa non venisse abilitata quando vengono analizzati tutti gli esempi

Le chiamate del pixel shader devono essere incrementate per ogni pixel con rasterizzazione conservativa in modalità di rasterizzazione conservativa.

### <a name="cull-state-interaction"></a>Interazione stato di eliminazione

Tutti gli Stati di eliminazione sono validi in modalità di rasterizzazione conservativa e seguono le stesse regole di quando la rasterizzazione conservativa non è abilitata.

Quando si confronta la rasterizzazione conservativa tra le risoluzioni a se stessa o senza la rasterizzazione conservativa abilitata, esiste la possibilità che alcune primitive possano avere una faccia non corrispondente (ad esempio, una riattivazione, l'altra anteriore). Le applicazioni possono evitare questa incertezza usando \_ la modalità di abbattimento D3D12 \_ \_ None (dalla [**\_ \_ modalità di eliminazione D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cull_mode)) e non usando il `IsFrontFace` valore generato dal sistema.

### <a name="isfrontface-interaction"></a>Interazione IsFrontFace

Il `IsFrontFace` valore generato dal sistema è valido per l'utilizzo in modalità di rasterizzazione conservativa e segue il comportamento definito quando la rasterizzazione conservativa non è abilitata.

### <a name="fill-modes-interaction"></a>Interazione modalità di riempimento

L'unica [**modalità di \_ riempimento \_ D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_fill_mode) valida per la rasterizzazione conservativa è D3D12 \_ Fill \_ Solid, qualsiasi altra modalità di riempimento è un parametro non valido per lo stato di rasterizzazione.

Ciò è dovuto al fatto che la specifica funzionale D3D12 specifica che la modalità di riempimento wireframe deve convertire i bordi del triangolo in linee e seguire le regole di rasterizzazione delle righe e il comportamento di rasterizzazione della linea conservativa non è stato definito

## <a name="implementation-details"></a>Dettagli dell'implementazione

Il tipo di rasterizzazione supportato in Direct3D 12 viene talvolta definito "rasterizzazione conservativa sovrastimata". Esiste anche il concetto di "rasterizzazione conservativa sottostimata", il che significa che vengono rasterizzati solo i pixel completamente coperti da una primitiva sottoposta a rendering. Le informazioni di rasterizzazione conservative sottostimate sono disponibili tramite il pixel shader tramite l'utilizzo di dati di code coverage di input e solo la rasterizzazione conservativa sovrastimata è disponibile come modalità di rasterizzazione.

Se una parte di una primitiva si sovrappone a un pixel, il pixel viene considerato analizzato ed è quindi rasterizzato. Quando un bordo o un angolo di una primitiva cade lungo il bordo o l'angolo di un pixel, l'applicazione della "regola superiore sinistra" è specifica dell'implementazione. Tuttavia, per le implementazioni che supportano triangoli degenerati, un triangolo degenerato lungo un bordo o un angolo deve coprire almeno un pixel.

Le implementazioni di rasterizzazione conservative possono variare in componenti hardware diversi e generare falsi positivi, vale a dire che possono decidere erroneamente che i pixel sono coperti. Questo problema può verificarsi a causa di dettagli specifici dell'implementazione, ad esempio gli errori di espansione o di blocco primitivi inerenti alle coordinate dei vertici a virgola fissa utilizzate per la rasterizzazione. Il motivo per cui i falsi positivi (rispetto alle coordinate dei vertici dei punti fissi) sono validi perché una certa quantità di falsi positivi è necessaria per consentire a un'implementazione di eseguire la valutazione del code coverage rispetto ai vertici post-bloccati (ad esempio coordinate dei vertici convertite da virgola mobile a 16,8 a virgola fissa utilizzati nell'rasterizzatore), ma che rispettano il code coverage prodotto dalle coordinate originali del vertice a virgola mobile.

Le implementazioni di rasterizzazione conservative non producono falsi negativi rispetto alle coordinate dei vertici a virgola mobile per le primitive post-snap non degenerate: se una parte di una primitiva si sovrappone a qualsiasi parte di un pixel, il pixel verrà rasterizzato.

I triangoli degenerati (indici duplicati in un buffer di indice o collineano in 3D) o diventano degenerati dopo la conversione a virgola fissa (vertici collineari nell'rasterizzatore), possono o non essere raccolti; entrambi sono comportamenti validi. I triangoli degenerati devono essere considerati rivolti. Pertanto, se un comportamento specifico è richiesto da un'applicazione, può utilizzare l'abbattimento o il test di back-face per il front-end. I triangoli degenerati utilizzano i valori assegnati al vertice 0 per tutti i valori interpolati.

Sono disponibili tre livelli di supporto hardware, oltre alla possibilità che l'hardware non supporti questa funzionalità.

-   Il livello 1 impone un'area di incertezza massima di 1/2 pixel e non supporta le degenerazioni post-snap. Si tratta di una soluzione ideale per il rendering affiancato, un Atlante di trama, la generazione di una mappa chiara e mappe shadow dei pixel secondari.
-   Il livello 2 riduce l'area di incertezza massima a 1/256 e richiede che le degenerazioni post-snap non vengano abbattuti. Questo livello è utile per l'accelerazione dell'algoritmo basato su CPU (ad esempio voxelization).
-   Il livello 3 mantiene un'area di incertezza massima di 1/256 e aggiunge il supporto per la copertura interna degli input. Il code coverage dell'input interno aggiunge il nuovo valore `SV_InnerCoverage` a HLSL (High Level Shading Language). Si tratta di un intero scalare a 32 bit che può essere specificato nell'input di un pixel shader e rappresenta le informazioni di rasterizzazione conservative sottostimate, ovvero se un pixel è garantito per essere completamente coperto. Questo livello è utile per l'eliminazione delle occlusioni.

## <a name="api-summary"></a>Riepilogo dell'API

I metodi, le strutture, le enumerazioni e le classi helper seguenti fanno riferimento a una rasterizzazione conservativa:

-   [**D3D12 \_ RASTERIZZAtore \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc) : struttura che contiene la descrizione del rasterizzatore.
-   [**D3D12 \_ \_ \_ Modalità di RASTERIZZAzione conservativa**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_conservative_rasterization_mode) : valori enum per la modalità (on o off).
-   [**D3D12 \_ \_Opzioni di \_ D3D12 \_ dati delle funzionalità**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) : struttura che mantiene il livello di supporto.
-   [**D3D12 \_ \_ \_ Livello di RASTERIZZAzione conservativa**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_conservative_rasterization_tier) : valori enum per ogni livello di supporto dell'hardware.
-   [**CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) : metodo per accedere alle funzionalità supportate.
-   [**CD3DX12 \_ RASTERIZZAtore \_ desc**](cd3dx12-rasterizer-desc.md) : classe helper per la creazione di descrizioni del rasterizzatore.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esercitazioni video su DirectX Advanced Learning: rasterizzazione conservativa](https://www.youtube.com/watch?v=zL0oSY_YmDY)
</dt> <dt>

[Visualizzazioni ordinate del rasterizzatore](rasterizer-order-views.md)
</dt> <dt>

[Rendering](rendering.md)
</dt> </dl>

 

 




