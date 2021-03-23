---
title: Ottimizzazioni di le trame accessibili per la CPU e swizzle standard
description: Le GPU di Universal Memory Architecture (UMA) offrono alcuni vantaggi di efficienza rispetto alle GPU discrete, soprattutto durante l'ottimizzazione per i dispositivi mobili.
ms.assetid: 26C41948-9625-4786-BBDF-552D1F8A2437
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47725702676d385d607fa87533680b9ffe0fc0df
ms.sourcegitcommit: 294c5ab750c46b5100bb2c84ef6c33ef7266c54b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/15/2020
ms.locfileid: "104548849"
---
# <a name="uma-optimizations-cpu-accessible-textures-and-standard-swizzle"></a>Ottimizzazioni di UMA: trame accessibili per la CPU e swizzle standard

Le GPU di Universal Memory Architecture (UMA) offrono alcuni vantaggi di efficienza rispetto alle GPU discrete, soprattutto durante l'ottimizzazione per i dispositivi mobili. Fornire l'accesso alla CPU delle risorse quando la GPU è UMA può ridurre la quantità di copia eseguita tra CPU e GPU. Anche se le applicazioni non sono consigliate in modo cieco per garantire l'accesso alla CPU a tutte le risorse sulle progettazioni di UMA, è possibile migliorare l'efficienza assegnando l'accesso alla CPU alle risorse appropriate. Diversamente dalle GPU discrete, la CPU può avere tecnicamente un puntatore a tutte le risorse a cui la GPU può accedere.

-   [Panoramica delle trame accessibili per la CPU](#overview-of-cpu-accessible-textures)
-   [Panoramica di swizzle standard](#overview-of-standard-swizzle)
-   [API](#apis)
-   [Argomenti correlati](#related-topics)

## <a name="overview-of-cpu-accessible-textures"></a>Panoramica delle trame accessibili per la CPU

Le trame accessibili per la CPU, nella pipeline di grafica, sono una funzionalità dell'architettura di UMA, che consente alle CPU di accedere in lettura e scrittura alle trame. Nelle GPU discrete più comuni, la CPU non ha accesso alle trame nella pipeline grafica.

La procedura consigliata generale per le trame consiste nel supportare GPU discrete, che in genere implicano il passaggio dei processi di [caricamento dei dati di trama attraverso i buffer](upload-and-readback-of-texture-data.md), riepilogati come segue:

-   Nessun accesso alla CPU per la maggior parte delle trame.
-   Impostazione del layout di trama sul \_ layout di trama D3D12 \_ \_ sconosciuto.
-   Caricamento delle trame nella GPU con [**CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion).

Tuttavia, per alcuni casi, la CPU e la GPU possono interagire con la stessa frequenza sugli stessi dati, il mapping delle trame diventa utile per risparmiare energia o per velocizzare una particolare progettazione su specifiche schede o architetture. Le applicazioni devono rilevare questi casi e ottimizzare le copie non necessarie. In questo caso, per ottenere prestazioni ottimali, tenere presente quanto segue:

-   È sufficiente iniziare a migliorare le prestazioni delle trame di mapping quando l' [**\_ \_ \_ architettura dei dati della funzionalità D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_architecture):: uma è true. Quindi prestare attenzione a *CacheCoherentUMA* per decidere quali proprietà della cache della CPU scegliere nell'heap.

-   L'uso dell'accesso alla CPU per le trame è più complicato rispetto a quello per i buffer. I layout di trama più efficienti per le GPU sono raramente righe \_ principali. Alcune GPU, infatti, possono supportare solo le \_ trame principali della riga durante la copia dei dati di trama.

-   Le GPU UMA dovrebbero trarre universalmente vantaggio da una semplice ottimizzazione per ridurre i tempi di caricamento del livello. Dopo aver riconosciuto UMA, l'applicazione può ottimizzare il [**CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) iniziale per popolare le trame che la GPU non modificherà. Anziché creare la trama in un heap con il \_ tipo di heap D3D12 \_ \_ predefinito e il marshalling dei dati di trama tramite, l'applicazione può usare [**WriteToSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource) per evitare di comprendere il layout di trama effettivo.

-   In D3D12, le trame create con \_ layout di trama D3D12 \_ \_ sconosciuto e nessun accesso alla CPU sono le più efficienti per il rendering e il campionamento di GPU frequenti. Quando si esegue il test delle prestazioni, tali trame devono essere confrontate \_ con il layout di trama D3D12 \_ \_ sconosciuto con l'accesso alla CPU e il \_ layout di trama D3D12 \_ \_ standard \_ SWIZZLE con accesso alla CPU e \_ \_ la riga del layout della trama D3D12 \_ \_ principale per il supporto tra adapter.

-   L'uso \_ di \_ un layout di trama D3D12 \_ sconosciuto con accesso alla CPU consente ai metodi [**WriteToSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource), [**ReadFromSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource), [**Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) (che ostano l'accesso all'applicazione al puntatore) e [**annullare**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap), ma può sacrificare l'efficienza dell'accesso alla GPU.

-   Usando \_ \_ il layout di trama D3D12 \_ standard \_ SWIZZLE con accesso alla CPU, Abilita [**WriteToSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource), [**ReadFromSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource), [**Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) (che restituisce un puntatore valido all'applicazione) e [**annullare**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap). Può anche sacrificare l'efficienza dell'accesso alla GPU oltre al \_ layout di trama D3D12 \_ \_ sconosciuto con l'accesso alla CPU.

## <a name="overview-of-standard-swizzle"></a>Panoramica di swizzle standard

D3D12 (e D3D 11.3) introducono un layout standard di dati multidimensionali. Questa operazione viene eseguita per consentire a più unità di elaborazione di operare sugli stessi dati senza copiare i dati o swizzling i dati tra più layout. Un layout standardizzato consente un miglioramento dell'efficienza attraverso gli effetti della rete e consente agli algoritmi di effettuare brevi riduzioni presumendo un modello particolare.

Per una descrizione dettagliata dei layout di trama, vedere [**\_ \_ layout di trama D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout).

Si noti tuttavia che questa swizzle standard è una funzionalità hardware e potrebbe non essere supportata da tutte le GPU.

Per informazioni generali su swizzling, vedere [curva Z order](https://en.wikipedia.org/wiki/Z-order_curve).

## <a name="apis"></a>API

A differenza di D3D 11.3, D3D12 supporta il mapping delle trame per impostazione predefinita, quindi non è necessario eseguire una query sulle [**\_ \_ \_ \_ Opzioni D3D12 dei dati della funzionalità D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options). Tuttavia, D3D12 non supporta sempre swizzle standard. questa funzionalità deve essere sottoposta a query con una chiamata a [**CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) e controllando il campo *StandardSwizzle64KBSupported* delle **\_ \_ \_ \_ Opzioni** D3D12 D3D12 data.

Le API seguenti fanno riferimento al mapping della trama:

Enumerazioni

-   [**D3D12 \_ \_Layout trama**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout) : controlla il modello di swizzle delle trame predefinite e Abilita il supporto della mappa sulle trame accessibili della CPU.

Strutture

-   [**D3D12 \_ RESOURCE \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc) : descrive una risorsa, ad esempio una trama, si tratta di una struttura ampiamente utilizzata.
-   [**D3D12 \_ HEAP \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_desc) : descrive un heap.

Metodi

-   [**ID3D12Device:: CreateCommittedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource) : crea una singola risorsa e un heap di supporto di dimensioni e allineamento corretti.
-   [**ID3D12Device:: createheap ha provocato**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createheap) : crea un heap per un buffer o una trama.
-   [**ID3D12Device:: CreatePlacedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createplacedresource) : crea una risorsa posizionata in un heap specifico, in genere un metodo più veloce per creare una risorsa rispetto a [**createheap ha provocato**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createheap).
-   [**ID3D12Device:: CreateReservedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createreservedresource) : crea una risorsa riservata ma non ancora sottoposta a commit o posizionata in un heap.
-   [**ID3D12CommandQueue:: UpdateTileMappings**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings) : Aggiorna i mapping dei percorsi dei riquadri nelle risorse affiancate alle posizioni di memoria in un heap delle risorse.
-   [**ID3D12Resource:: Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) : ottiene un puntatore ai dati specificati nella risorsa e nega l'accesso alla GPU alla sottorisorsa.
-   [**ID3D12Resource:: getdesc**](id3d12resource-getdesc.md) : ottiene le proprietà della risorsa.
-   [**ID3D12Heap:: getdesc**](id3d12heap-getdesc.md) ottiene le proprietà dell'heap.
-   [**ReadFromSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource) : copia i dati da una trama mappata mediante [**Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map).
-   [**WriteToSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource) : copia i dati in una trama mappata mediante [**Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map).

Le risorse e gli heap padre presentano requisiti di allineamento:

-   D3D12 \_ default \_ MSAA \_ \_ allineamento posizionamento risorse \_ (4 MB) per le trame multicampionamento.
-   D3D12 \_ default \_ Resource \_ Placement \_ Alignment (64KB) per singoli buffer e trame di esempio.
-   La copia delle sottorisorse lineari deve essere allineata all' \_ \_ allineamento del posizionamento dei dati della trama D3D12 \_ \_ (512 byte), con un passo di riga allineato all' \_ allineamento del passo dei dati della trama D3D12 \_ \_ \_ (256 byte).
-   Le visualizzazioni di buffer costanti devono essere allineate all' \_ \_ allineamento dei dati del buffer costante D3D12 \_ \_ \_ (256 byte).

Le trame più piccole di 64KB devono essere elaborate attraverso [**CreateCommittedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource).

Con le trame dinamiche (trame che modificano ogni frame), la CPU scriverà in modo lineare nell'heap di caricamento, seguito da un'operazione di copia GPU.

In genere, per creare risorse dinamiche, creare un buffer di grandi dimensioni in un heap di caricamento (fare riferimento alla [suballocazione nei buffer](large-buffers.md)). Per creare risorse di staging, creare un buffer di grandi dimensioni in un heap readback. Per creare risorse statiche predefinite, creare risorse adiacenti in un heap predefinito. Per creare risorse con alias predefinite, creare risorse sovrapposte in un heap predefinito.

[**WriteToSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource) e [**ReadFromSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource) riordinano i dati di trama tra un layout di riga e un layout di risorse non definito. L'operazione è sincrona, pertanto l'applicazione deve tenere in considerazione la pianificazione della CPU. L'applicazione può sempre suddividere la copia in aree più piccole o pianificare questa operazione in un'altra attività. Le risorse MSAA e le risorse di stencil Depth con layout di risorse opache non sono supportate da queste operazioni di copia della CPU e causeranno un errore. Anche i formati che non dispongono di una dimensione di un elemento di potenza di due non sono supportati e causeranno anche un errore. È possibile che si verifichino codici restituiti di memoria insufficiente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Costanti Core**](constants.md)
</dt> <dt>

[**ID3D12Heap**](/windows/desktop/api/d3d12/nn-d3d12-id3d12heap)
</dt> <dt>

[Associazione di risorse](resource-binding.md)
</dt> </dl>

 

 




