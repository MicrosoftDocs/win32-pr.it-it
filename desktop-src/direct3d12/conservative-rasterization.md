---
title: Rasterizzazione conservativa Direct3D 12
description: La rasterizzazione conservativa aggiunge una certa certezza al rendering dei pixel, utile in particolare per gli algoritmi di rilevamento delle collisioni.
ms.assetid: 081199AD-1702-4EC8-95AD-B1148C676199
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15bb5893e944c5d495cf91fdb334bd6ab5f755b7f1e200648242cb46b281f695
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045783"
---
# <a name="direct3d-12-conservative-rasterization"></a>Rasterizzazione conservativa Direct3D 12

La rasterizzazione conservativa aggiunge una certa certezza al rendering dei pixel, utile in particolare per gli algoritmi di rilevamento delle collisioni.

-   [Overview](#overview)
-   [Interazioni con la pipeline](#interactions-with-the-pipeline)
    -   [Interazione con le regole di rasterizzazione](#rasterization-rules-interaction)
    -   [Interazione con più modelli](#multisampling-interaction)
    -   [Interazione sampleMask](#samplemask-interaction)
    -   [Interazione di test di profondità/stencil](#depthstencil-test-interaction)
    -   [Interazione con il pixel helper](#helper-pixel-interaction)
    -   [Interazione di code coverage di output](#output-coverage-interaction)
    -   [Interazione con InputCoverage](#inputcoverage-interaction)
    -   [Interazione innerCoverage](#innercoverage-interaction)
    -   [Interazione tra attributi](#attribute-interpolation-interaction)
    -   [Interazione di ritaglio](#clipping-interaction)
    -   [Interazione con Clip Distance](#clip-distance-interaction)
    -   [Interazione di rasterizzazione indipendente di destinazione](#target-independent-rasterization-interaction)
    -   [Interazione della topologia primitiva IA](#ia-primitive-topology-interaction)
    -   [Interazione tra query](#query-interaction)
    -   [Interazione di stato Cull](#cull-state-interaction)
    -   [Interazione con IsFrontFace](#isfrontface-interaction)
    -   [Interazione con modalità di riempimento](#fill-modes-interaction)
-   [Dettagli di implementazione](#implementation-details)
-   [Riepilogo dell'API](#api-summary)
-   [Argomenti correlati](#related-topics)

## <a name="overview"></a>Panoramica

La rasterizzazione conservativa significa che tutti i pixel che sono almeno parzialmente coperti da una primitiva sottoposta a rendering vengono rasterizzati, il che significa che pixel shader viene richiamato. Il comportamento normale è il campionamento, che non viene usato se è abilitata la rasterizzazione conservativa.

La rasterizzazione conservativa è utile in diverse situazioni, tra cui per la certezza del rilevamento delle collisioni, del culling dell'occlusione e del rendering affiancato.

Ad esempio, la figura seguente mostra un triangolo verde di cui viene eseguito il rendering usando la rasterizzazione conservativa, come verrebbe visualizzato nel rasterizzatore (ovvero usando coordinate dei vertici a 16,8 punti fissi). L'area brown è nota come "area di incertezza", un'area concettuale che rappresenta i limiti estesi del triangolo, necessaria per garantire che la primitiva nel rasterizzatore sia conservativa rispetto alle coordinate dei vertici a virgola mobile originali. I quadrati rossi in ogni vertice mostrano il modo in cui viene calcolata l'area di incertezza: come un quadrato disastrato.

I quadrati grigi grandi mostrano i pixel di cui verrà eseguito il rendering. I quadratini rosa mostrano i pixel di cui viene eseguito il rendering usando la "regola in alto a sinistra", che entra in gioco quando il bordo del triangolo attraversa il bordo dei pixel. Possono essere presenti falsi positivi (pixel impostati che non dovrebbero essere stati) che il sistema normalmente ma non sempre cull.

![regola in alto a sinistra](images/conservative-rasterization-0.png)

## <a name="interactions-with-the-pipeline"></a>Interazioni con la pipeline

### <a name="rasterization-rules-interaction"></a>Interazione con le regole di rasterizzazione

Nella modalità di rasterizzazione conservativa, le regole di rasterizzazione si applicano allo stesso modo di quando la modalità di rasterizzazione conservativa non è abilitata con eccezioni per la regola Top-Left, descritta in precedenza, e copertura pixel. 16.8 Fixed-Point usare la precisione del rasterizzatore.

I pixel che non verrebbero coperti se l'hardware usasse coordinate dei vertici a virgola mobile complete possono essere inclusi solo se si trova all'interno di un'area di incertezza, non più grande di mezzo pixel nel dominio a virgola fissa. Si prevede che l'hardware futuro raggiunga l'area di incertezza più restrittiva specificata nel livello 2. Si noti che questo requisito impedisce ai triangoli sliver di estendersi oltre il necessario.

Un'area di incertezza valida simile si applica anche a , ma è più stretta perché nessuna implementazione richiede un'area di incertezza più ampia `InnerCoverage` per questo caso. Per [altri dettagli, vedere InnerCoverage interaction (Interazione innerCoverage).](#innercoverage-interaction)

Le aree di incertezza interne ed esterne devono essere maggiori o uguali alla dimensione della metà della griglia di subpixe, o di 1/512 di pixel, nel dominio a virgola fissa. Si tratta dell'area minima di incertezza valida. 1/512 deriva dalla rappresentazione delle coordinate del rasterizzatore a virgola fissa 16,8 e dalla regola round-to-nearest applicata durante la conversione delle coordinate dei vertici a virgola mobile in coordinate a virgola fissa 16,8. 1/512 può cambiare se la precisione del rasterizzatore cambia. Se un'implementazione implementa questa area di incertezza minima, deve seguire la regola di Top-Left quando un bordo o un angolo dell'area di incertezza cade lungo il bordo o l'angolo di un pixel. Gli bordi ritagliati dell'area di incertezza devono essere considerati come il vertice più vicino, vale a dire che vengono conteggiati come due bordi: i due che si uniscono al vertice associato. Top-Left è necessaria quando viene usata l'area di incertezza minima perché, in caso contrario, un'implementazione di rasterizzazione conservativa non riuscirà a rasterizzare i pixel che potrebbero essere coperti quando la modalità di rasterizzazione conservativa è disabilitata.

Il diagramma seguente illustra un'area di incertezza esterna valida prodotta mediante lo sweep di un quadrato intorno ai bordi della primitiva nel dominio a virgola fissa (ad esempio, i vertici sono stati quantizzati dalla rappresentazione a virgola fissa 16.8). Le dimensioni di questo quadrato sono basate sulle dimensioni valide dell'area di incertezza esterna: per l'1/2 di un pixel, il quadrato ha una larghezza e un'altezza di 1 pixel, per 1/512 di pixel, il quadrato è 1/256 di un pixel in larghezza e altezza. Il triangolo verde rappresenta una determinata primitiva, la linea rossa tratteggiata rappresenta il limite della rasterizzazione conservativa sovrastimata, i quadrati neri a tinta unita rappresentano il quadrato che si trova lungo i bordi della primitiva e l'area a scacchi blu è l'area di incertezza esterna:

![area di incertezza esterna.](images/outercoverage.jpg)

### <a name="multisampling-interaction"></a>Interazione con più modelli

Indipendentemente dal numero di campioni nelle superfici **RenderTarget** / **DepthStencil** (o se *ForcedSampleCount* viene usato o meno), tutti i campioni vengono coperti per i pixel rasterizzati dalla rasterizzazione conservativa. I singoli percorsi di esempio non vengono testati per verificare se rientrano o meno nella primitiva.

### <a name="samplemask-interaction"></a>Interazione sampleMask

Lo stato di rasterizzazione *SampleMask* si applica allo stesso modo di quando la rasterizzazione conservativa non è abilitata per , ma non influisce (ovvero non è AND in un input dichiarato con `InputCoverage` `InnerCoverage` `InnerCoverage` ). Questo perché non è correlato al fatto che i campioni MSAA siano mascherati: 0 indica solo che non è garantito che il pixel sia completamente coperto, non che nessun campione verrà `InnerCoverage` `InnerCoverage` aggiornato.

### <a name="depthstencil-test-interaction"></a>Interazione di test di profondità/stencil

Il test di profondità/stencil procede per un pixel rasterizzato conservativamente come se tutti i campioni vengono trattati quando la rasterizzazione conservativa non è abilitata.

Se si procede con tutti gli esempi trattati, l'estrapolazione della profondità, che è valida e deve essere impostata sul viewport come specificato quando l'estrapolazione conservativa non è abilitata. Questo è simile a quando le modalità di interpolazione con frequenza pixel vengono usate in una **destinazione** di rendering con numero di campioni maggiore di 1, anche se nel caso della rasterizzazione conservativa, è il valore di profondità che entra nel test di profondità della funzione fissa che può essere estrapolato.

Il comportamento di culling della profondità anticipata con l'estrapolazione della profondità non è definito. Ciò è dovuto al fatto che alcuni hardware di culling di profondità anticipata non possono supportare correttamente i valori di profondità estrapolati. Tuttavia, il comportamento di culling della profondità anticipata in presenza di estrapolazione della profondità è problematico anche con hardware in grado di supportare valori di profondità estrapolati. Questo problema può essere risolto stringendo la profondità di input del pixel shader ai valori di profondità minima e massima della primitiva da rasterizzarsi e scrivendo tale valore in (registro di profondità di `oDepth` output pixel shader). Le implementazioni sono necessarie per disabilitare il culling di profondità anticipata in questo caso, a causa della `oDepth` scrittura.

### <a name="helper-pixel-interaction"></a>Interazione con il pixel helper

Le regole helper pixel si applicano allo stesso modo di quando la rasterizzazione conservativa non è abilitata. Come parte di questo, tutti i pixel, inclusi i pixel helper, devono segnalare in modo `InputCoverage` accurato come specificato nella `InputCoverage` sezione di interazione. Pertanto, i pixel completamente non coperti segnalano una copertura 0.

### <a name="output-coverage-interaction"></a>Interazione di code coverage di output

Output Coverage ( ) si comporta per un pixel rasterizzato conservativamente come quando la rasterizzazione conservativa non è abilitata con tutti `oMask` i campioni trattati.

### <a name="inputcoverage-interaction"></a>Interazione con InputCoverage

In modalità di rasterizzazione conservativa, questo registro di input viene popolato come se tutti i campioni vengono trattati quando la rasterizzazione conservativa non è abilitata per un determinato pixel rasterizzato conservativamente. In altre informazioni, si applicano tutte le interazioni esistenti (ad esempio, viene applicato *SampleMask)* e i primi n bit dell'LSB vengono impostati su 1 per un pixel rasterizzato conservativamente, dato un campione `InputCoverage` n per pixel **RenderTarget** e/o **DepthStencil** buffer associato all'unione di **output** o un n campione *ForcedSampleCount*. Il resto dei bit è 0.

Questo input è disponibile in uno shader indipendentemente dall'uso della rasterizzazione conservativa, anche se la rasterizzazione conservativa modifica il comportamento in modo da mostrare solo tutti i campioni coperti (o nessuno per i pixel helper).

### <a name="innercoverage-interaction"></a>Interazione innerCoverage

Questa funzionalità è obbligatoria e disponibile solo nel livello 3. Il runtime non riuscirà a creare shader per shader che usano questa modalità quando un'implementazione supporta un livello inferiore a 3.

Il pixel shader ha un valore intero scalare a 32 bit system generate value disponibile: `InnerCoverage` . Si tratta di un campo di bit con il bit 0 dell'LSB impostato su 1 per un determinato pixel rasterizzato conservativamente, solo quando tale pixel è garantito interamente all'interno della primitiva corrente. Tutti gli altri bit del registro di input devono essere impostati su 0 quando il bit 0 non è impostato, ma non sono definiti quando il bit 0 è impostato su 1 (essenzialmente, questo campo di bit rappresenta un valore booleano dove false deve essere esattamente 0, ma true può essere qualsiasi valore dispari (ad esempio, bit 0 impostato) diverso da zero. Questo input viene usato per le informazioni di rasterizzazione conservativa sottostimate. Indica al pixel shader se il pixel corrente si trova completamente all'interno della geometria.

Deve essere in considerazione l'errore di allineamento a risoluzioni maggiori o uguali alla risoluzione in cui funziona l'oggetto Draw corrente. Non devono essere presenti falsi positivi (impostazione di bit quando il pixel non è completamente coperto per eventuali errori di allineamento in risoluzioni maggiori o uguali alla risoluzione in cui funziona l'oggetto Draw corrente), ma sono consentiti falsi `InnerCoverage` negativi. In breve, l'implementazione non deve identificare erroneamente i pixel come completamente coperti che non sarebbero con coordinate dei vertici a virgola mobile complete nel rasterizzatore.

I pixel che verrebbero completamente coperti se l'hardware usasse coordinate dei vertici a virgola mobile complete possono essere omessi solo se intersecano l'area di incertezza interna, che non deve essere maggiore della dimensione della griglia dei subpix, o 1/256 di pixel, nel dominio a virgola fissa. In altri modi, i pixel interamente all'interno del limite interno dell'area di incertezza interna devono essere contrassegnati come completamente coperti. Il limite interno dell'area di incertezza è illustrato nel diagramma seguente dalla linea punteggiata nera in grassetto. 1/256 deriva dalla rappresentazione delle coordinate del rasterizzatore a virgola fissa 16,8, che può cambiare se cambia la precisione del rasterizzatore. Questa area di incertezza è sufficiente per l'errore di allineamento causato dalla conversione delle coordinate dei vertici a virgola mobile in coordinate dei vertici a virgola fissa nel rasterizzatore.

In questo caso si applicano anche gli stessi requisiti minimi di area di incertezza definiti nell'interazione con le regole di rasterizzazione.

Il diagramma seguente illustra un'area di incertezza interna valida prodotta mediante lo sweep di un quadrato intorno ai bordi della primitiva nel dominio a virgola fissa (ad esempio, i vertici sono stati quantificati dalla rappresentazione a virgola fissa 16.8). Le dimensioni di questo quadrato sono basate sulle dimensioni valide dell'area di incertezza interna: per 1/256 di pixel, il quadrato è 1/128 di pixel in larghezza e altezza. Il triangolo verde rappresenta una primitiva specificata, la linea nera in grassetto punteggiata rappresenta il limite dell'area di incertezza interna, i quadrati neri solidi rappresentano il quadrato che si trova lungo i bordi primitivi e l'area a scacchi arancione è l'area di incertezza interna:

![inner in incertezze.](images/innercoverage.jpg)

L'uso di non influisce sulla rasterizzazione conservativa di un pixel, ovvero l'uso di una di queste modalità non influisce sui pixel rasterizzati quando è abilitata la modalità `InnerCoverage` `InputCoverage` di rasterizzazione conservativa. Pertanto, quando viene usato e il pixel shader elabora un pixel che non è completamente coperto dalla geometria, il relativo valore sarà 0, ma la chiamata al pixel shader avrà campioni `InnerCoverage` aggiornati. Questo valore è diverso da quando `InputCoverage` è 0, vale a dire che non verrà aggiornato alcun campione.

Questo input si escludono a vicenda `InputCoverage` con : non è possibile usare entrambi.

Per accedere a , deve essere dichiarato come componente singolo da uno dei registri di `InnerCoverage` input pixel shader. La modalità di interpolazione nella dichiarazione deve essere costante (l'interpolazione non è applicabile).

Il campo di bit non è interessato dai test di profondità/stencil e non è associato allo stato `InnerCoverage` di rasterizzazione *SampleMask.*

Questo input è valido solo in modalità di rasterizzazione conservativa. Quando la rasterizzazione conservativa non è abilitata, `InnerCoverage` produce un valore non definito.

Le chiamate al pixel shader causate dalla necessità di pixel helper, ma altrimenti non coperte dalla primitiva, devono avere il registro `InnerCoverage` impostato su 0.

### <a name="attribute-interpolation-interaction"></a>Interazione tra attributi

Le modalità di interpolazione degli attributi rimangono invariate e procedono come quando la rasterizzazione conservativa non è abilitata, in cui vengono usati i vertici con scalabilità del viewport e i vertici convertiti a virgola fissa. Poiché tutti i campioni in un pixel rasterizzato conservativamente sono considerati coperti, è valido per l'estrapolazione dei valori, analogamente a quando le modalità di interpolazione con frequenza pixel vengono usate in **una** destinazione di rendering con numero di campioni maggiore di 1. Le modalità di interpolazione centroide producono risultati identici alla modalità di interpolazione non centroide corrispondente. La nozione di centroide è inutile in questo scenario, in cui la copertura del campione è solo completa o 0.

La rasterizzazione conservativa consente ai triangoli degeneri di produrre chiamate al pixel shader, pertanto i triangoli degeneri devono usare i valori assegnati al vertice 0 per tutti i valori interpolati.

### <a name="clipping-interaction"></a>Interazione di ritaglio

Quando è abilitata la modalità di rasterizzazione conservativa e il clip di profondità è disabilitato (quando *depthClipEnable* Rasterizer State è impostato su FALSE), potrebbero esserci varianze nell'interpolazione degli attributi per i segmenti di una primitiva che non rientrano nell'intervallo 0 <= z <= w, a seconda dell'implementazione: i valori costanti vengono usati da un punto in cui la primitiva interseca il piano pertinente (vicino o lontano) o l'interpolazione degli attributi si comporta come quando la modalità di rasterizzazione conservativa è disabilitata. Tuttavia, il comportamento del valore di profondità è lo stesso indipendentemente dalla modalità di rasterizzazione conservativa, ad esempio alle primitive che non rientrano nell'intervallo di profondità deve essere comunque assegnato il valore del limite più vicino dell'intervallo di profondità del viewport. Il comportamento di interpolazione degli attributi all'interno dell'intervallo 0 <= z <= w deve rimanere invariato.

### <a name="clip-distance-interaction"></a>Interazione con Clip Distance

Clip Distance è valida quando è abilitata la modalità di rasterizzazione conservativa e si comporta per un pixel rasterizzato conservativamente come quando la rasterizzazione conservativa non è abilitata con tutti i campioni coperti.

Si noti che la rasterizzazione conservativa può causare l'estrapolazione della coordinata del vertice W, che può causare <W = 0. In questo modo, le implementazioni di Clip Distance per pixel potrebbero operare su una distanza di ritaglio che è stata divisa in prospettiva da un valore W non valido. Le implementazioni di Clip Distance devono proteggersi dal richiamo della rasterizzazione per i pixel in cui la coordinata vertice W <= 0 (ad esempio a causa dell'estrapolazione in modalità di rasterizzazione conservativa).

### <a name="target-independent-rasterization-interaction"></a>Interazione di rasterizzazione indipendente di destinazione

La modalità di rasterizzazione conservativa è compatibile con il tiR (Target Independent Rasterization). Si applicano le regole e le restrizioni TIR, comportandosi per un pixel rasterizzato conservativamente come se tutti i campioni siano coperti.

### <a name="ia-primitive-topology-interaction"></a>Interazione della topologia primitiva IA

La rasterizzazione conservativa non è definita per le primitive di linee o punti. Pertanto, le topologie primitive che specificano punti o linee producono un comportamento indefinito se vengono immesse nell'unità di rasterizzazione quando è abilitata la rasterizzazione conservativa.

La convalida del livello di debug verifica che le applicazioni non usino queste topologie primitive.

### <a name="query-interaction"></a>Interazione tra query

Per un pixel rasterizzato conservativamente, le query si comportano come quando la rasterizzazione conservativa non è abilitata quando vengono trattati tutti i campioni. Ad esempio, per un pixel rasterizzato conservativamente, D3D12 \_ QUERY \_ TYPE OCCLUSION e \_ D3D12 \_ QUERY TYPE PIPELINE STATISTICS \_ \_ \_ (da [**D3D12 \_ QUERY \_ TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_type)) devono comportarsi come quando la rasterizzazione conservativa non è abilitata quando vengono trattati tutti i campioni.

Le chiamate al pixel shader devono essere incrementate per ogni pixel rasterizzato conservativamente in modalità di rasterizzazione conservativa.

### <a name="cull-state-interaction"></a>Interazione dello stato di Cull

Tutti gli stati Cull sono validi in modalità di rasterizzazione conservativa e seguono le stesse regole di quando la rasterizzazione conservativa non è abilitata.

Quando si confronta la rasterizzazione conservativa tra risoluzioni diverse o se non è abilitata la rasterizzazione conservativa, è possibile che alcune primitive non siano corrispondenti (ad esempio, una rivolta all'indietro, l'altra frontale). Le applicazioni possono evitare questa incertezza usando D3D12 \_ CULL \_ MODE \_ NONE (da [**D3D12 \_ CULL \_ MODE)**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cull_mode)e non usando il `IsFrontFace` valore generato dal sistema.

### <a name="isfrontface-interaction"></a>Interazione con IsFrontFace

Il valore generato dal sistema è valido per l'uso in modalità di rasterizzazione conservativa e segue il comportamento definito quando la rasterizzazione conservativa `IsFrontFace` non è abilitata.

### <a name="fill-modes-interaction"></a>Interazione con modalità di riempimento

L'unica modalità di riempimento [**D3D12 \_ \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_fill_mode) valida per la rasterizzazione conservativa è D3D12 FILL SOLID, qualsiasi altra modalità di riempimento è un parametro non valido per lo stato \_ \_ di rasterizzazione.

Questo perché la specifica funzionale D3D12 specifica che la modalità di riempimento wireframe deve convertire i bordi del triangolo in linee e seguire le regole di rasterizzazione delle linee e il comportamento conservativo di rasterizzazione delle linee non è stato definito.

## <a name="implementation-details"></a>Dettagli dell'implementazione

Il tipo di rasterizzazione supportato in Direct3D 12 viene talvolta definito "rasterizzazione conservativa sovrastimata". Esiste anche il concetto di "rasterizzazione conservativa sottostimata", il che significa che solo i pixel completamente coperti da una primitiva sottoposta a rendering vengono rasterizzati. Le informazioni di rasterizzazione conservativa sottostimate sono disponibili tramite il pixel shader tramite l'uso di dati di code coverage di input e solo la rasterizzazione conservativa sovrastimata è disponibile come modalità di rasterizzazione.

Se una parte di una primitiva si sovrappone a un pixel, tale pixel viene considerato coperto e quindi rasterizzato. Quando un bordo o un angolo di una primitiva cade lungo il bordo o l'angolo di un pixel, l'applicazione della "regola in alto a sinistra" è specifica dell'implementazione. Tuttavia, per le implementazioni che supportano triangoli degeneri, un triangolo degenere lungo un bordo o un angolo deve coprire almeno un pixel.

Le implementazioni di rasterizzazione conservativa possono variare a seconda dell'hardware e produrre falsi positivi, vale a dire che possono decidere erroneamente che i pixel sono coperti. Ciò può verificarsi a causa di dettagli specifici dell'implementazione, ad esempio errori di espansione primitiva o di allineamento intrinseci nelle coordinate dei vertici a virgola fissa usate nella rasterizzazione. Il motivo per cui i falsi positivi (per quanto riguarda le coordinate dei vertici a virgola fissa) sono validi perché sono necessari alcuni falsi positivi per consentire a un'implementazione di eseguire la valutazione della copertura rispetto ai vertici post-allineati (ad esempio, le coordinate dei vertici che sono state convertite da virgola mobile al 16,8 a virgola fissa usato nel rasterizzatore), ma rispettano la copertura prodotta dalle coordinate dei vertici a virgola mobile originali.

Le implementazioni di rasterizzazione conservativa non producono falsi negativi rispetto alle coordinate dei vertici a virgola mobile per primitive post-snap non degenerate: se una parte di una primitiva si sovrappone a qualsiasi parte di un pixel, il pixel viene rasterizzato.

I triangoli che sono degeneri (indici duplicati in un index buffer o in 3D) o che diventano degeneri dopo la conversione a virgola fissa (vertici del rasterizzatore) possono essere o meno degeneri; entrambi sono comportamenti validi. I triangoli degeneri devono essere considerati rivolti all'indietro, quindi se un'applicazione richiede un comportamento specifico, può usare l'culling del viso posteriore o il test per il front-facing. I triangoli degeneri usano i valori assegnati al vertice 0 per tutti i valori interpolati.

Sono disponibili tre livelli di supporto hardware, oltre alla possibilità che l'hardware non supporti questa funzionalità.

-   Il livello 1 impone un'area di incertezza massima di 1/2 pixel e non supporta i degeneri post-snap. Questa opzione è buona per il rendering a riquadri, un at atlas trame, la generazione di mappe di luce e le mappe ombreggiate sub-pixel.
-   Il livello 2 riduce l'area di incertezza massima a 1/256 e richiede che i degeneri post-snap non siano culled. Questo livello è utile per l'accelerazione degli algoritmi basata sulla CPU, ad esempio la voxelizzazione.
-   Il livello 3 mantiene un'area di incertezza massima di 1/256 e aggiunge il supporto per la copertura dell'input interno. La copertura dell'input interno aggiunge il `SV_InnerCoverage` nuovo valore a HLSL (High Level Shading Language). Si tratta di un intero scalare a 32 bit che può essere specificato nell'input di un pixel shader e rappresenta le informazioni di rasterizzazione conservativa sottostimate, ovvero se un pixel è garantito per essere completamente coperto. Questo livello è utile per il culling dell'occlusione.

## <a name="api-summary"></a>Riepilogo dell'API

I metodi, le strutture, le enumerazioni e le classi helper seguenti fanno riferimento alla rasterizzazione conservativa:

-   [**D3D12 \_ RASTERIZER \_ DESC: struttura**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc) che contiene la descrizione del rasterizzatore.
-   [**D3D12 \_ CONSERVATIVE \_ RASTERIZATION \_ MODE:**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_conservative_rasterization_mode) valori di enumerazione per la modalità (attivata o disattivata).
-   [**D3D12 \_ FEATURE \_ DATA \_ D3D12 \_ OPTIONS:**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) struttura che contiene il livello di supporto.
-   [**D3D12 \_ LIVELLO \_ DI \_ RASTERIZZAZIONE CONSERVATIVA:**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_conservative_rasterization_tier) valori di enumerazione per ogni livello di supporto da parte dell'hardware.
-   [**CheckFeatureSupport:**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) metodo per accedere alle funzionalità supportate.
-   [**CD3DX12 \_ RASTERIZER \_ DESC:**](cd3dx12-rasterizer-desc.md) classe helper per la creazione di descrizioni del rasterizzatore.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esercitazioni video di apprendimento avanzato DirectX: Rasterizzazione conservativa](https://www.youtube.com/watch?v=zL0oSY_YmDY)
</dt> <dt>

[Visualizzazioni ordinate del rasterizzatore](rasterizer-order-views.md)
</dt> <dt>

[Rendering](rendering.md)
</dt> </dl>

 

 




