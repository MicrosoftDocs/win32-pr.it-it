---
title: Ottimizzazioni UMA Trame accessibili dalla CPU e Swizzle standard
description: Le GPU UMA (Universal Memory Architecture) offrono alcuni vantaggi in termini di efficienza rispetto alle GPU discrete, in particolare quando si ottimizza per i dispositivi mobili.
ms.assetid: 26C41948-9625-4786-BBDF-552D1F8A2437
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2624a300811b4d4a1eef70873a31af89b0546224fd9b4f3ba06ecb1fbd2fac42
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894671"
---
# <a name="uma-optimizations-cpu-accessible-textures-and-standard-swizzle"></a>Ottimizzazioni UMA: trame accessibili dalla CPU e swizzle standard

Le GPU UMA (Universal Memory Architecture) offrono alcuni vantaggi in termini di efficienza rispetto alle GPU discrete, in particolare quando si ottimizza per i dispositivi mobili. Concedere alle risorse l'accesso alla CPU quando la GPU è UMA può ridurre la quantità di copia che si verifica tra CPU e GPU. Anche se non è consigliabile che le applicazioni consegneranno alla CPU l'accesso alla CPU a tutte le risorse nelle progettazioni UMA, è possibile migliorare l'efficienza assegnando alle risorse l'accesso alla CPU giusto. A differenza delle GPU discrete, la CPU può tecnicamente avere un puntatore a tutte le risorse a cui la GPU può accedere.

-   [Panoramica delle trame accessibili tramite CPU](#overview-of-cpu-accessible-textures)
-   [Panoramica di Swizzle Standard](#overview-of-standard-swizzle)
-   [API](#apis)
-   [Argomenti correlati](#related-topics)

## <a name="overview-of-cpu-accessible-textures"></a>Panoramica delle trame accessibili tramite CPU

Le trame accessibili tramite CPU, nella pipeline grafica, sono una funzionalità dell'architettura UMA che consente alle CPU di accedere in lettura e scrittura alle trame. Nelle GPU discrete più comuni, la CPU non ha accesso alle trame nella pipeline grafica.

Il consiglio generale della procedura consigliata per le trame consiste nell'adattare GPU discrete, che in genere comporta la procedura di caricamento dei dati di trama tramite [buffer,](upload-and-readback-of-texture-data.md)riepilogata come segue:

-   Non ha accesso alla CPU per la maggior parte delle trame.
-   Impostazione del layout di trama su D3D12 \_ TEXTURE \_ LAYOUT \_ UNKNOWN.
-   Caricamento delle trame nella GPU con [**CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion).

Tuttavia, in alcuni casi, la CPU e la GPU possono interagire così frequentemente sugli stessi dati, che le trame di mapping diventano utili per risparmiare energia o per velocizzare una progettazione specifica su schede o architetture specifiche. Le applicazioni devono rilevare questi casi e ottimizzare le copie non necessarie. In questo caso, per ottenere prestazioni ottimali, tenere presente quanto segue:

-   Iniziare a migliorare le prestazioni delle trame di mapping solo quando [**D3D12 \_ FEATURE \_ DATA \_ ARCHITECTURE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_architecture)::UMA è TRUE. Prestare quindi attenzione a *CacheCoherentUMA* se si decide quali proprietà della cache della CPU scegliere nell'heap.

-   Sfruttare l'accesso alla CPU per le trame è più complicato rispetto ai buffer. I layout di trama più efficienti per le GPU sono raramente le righe \_ principali. In effetti, alcune GPU possono supportare solo trame principali di \_ riga durante la copia dei dati di trama.

-   Le GPU UMA devono trarre vantaggio universalmente da una semplice ottimizzazione per ridurre i tempi di caricamento a livello. Dopo aver riconosciuto UMA, l'applicazione può ottimizzare [**l'area CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) iniziale per popolare le trame che la GPU non modificherà. Anziché creare la trama in un heap con TIPO HEAP D3D12 DEFAULT e il marshalling dei dati della trama, l'applicazione può usare \_ \_ \_ [**WriteToSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource) per evitare di comprendere il layout effettivo della trama.

-   In D3D12 le trame create con LAYOUT TEXTURE D3D12 UNKNOWN e nessun accesso alla CPU sono le più efficienti per il rendering e il campionamento \_ \_ frequenti della \_ GPU. Durante i test delle prestazioni, queste trame devono essere confrontate con D3D12 TEXTURE LAYOUT UNKNOWN con accesso \_ \_ alla CPU e \_ D3D12 TEXTURE LAYOUT STANDARD SWIZZLE con accesso alla CPU e \_ \_ \_ \_ D3D12 \_ TEXTURE LAYOUT ROW MAJOR \_ \_ \_ per il supporto di più adattatori.

-   L'uso di D3D12 TEXTURE LAYOUT UNKNOWN con accesso alla CPU consente ai metodi \_ \_ \_ [**WriteToSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource), [**ReadFromSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource), [**Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) (che preclude l'accesso dell'applicazione al puntatore) e [**Unmap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap), ma può sacrificare l'efficienza dell'accesso alla GPU.

-   L'uso di D3D12 TEXTURE LAYOUT STANDARD SWIZZLE con accesso alla CPU abilita \_ \_ \_ \_ [**WriteToSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource), [**ReadFromSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource), [**Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) (che [](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap)restituisce un puntatore valido all'applicazione) e Unmap . Può anche sacrificare l'efficienza dell'accesso alla GPU più di D3D12 \_ TEXTURE LAYOUT UNKNOWN con accesso alla \_ \_ CPU.

## <a name="overview-of-standard-swizzle"></a>Panoramica di Swizzle Standard

D3D12 (e D3D11.3) introducono un layout di dati multidimensionale standard. Questa operazione viene eseguita per consentire a più unità di elaborazione di operare sugli stessi dati senza copiare i dati o scorrere i dati tra più layout. Un layout standardizzato consente di migliorare l'efficienza tramite gli effetti di rete e consente agli algoritmi di eseguire brevi riduzioni presupponendo un modello specifico.

Per una descrizione dettagliata dei layout di trama, vedere LAYOUT TEXTURE [**D3D12 \_ \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout).

Si noti tuttavia che questo girello standard è una funzionalità hardware e potrebbe non essere supportato da tutte le GPU.

Per informazioni di base sullo swizzling, fare riferimento alla [curva dell'ordine Z.](https://en.wikipedia.org/wiki/Z-order_curve)

## <a name="apis"></a>API

A differenza di D3D11.3, D3D12 supporta il mapping delle trame per impostazione predefinita, quindi non è necessario eseguire query [**D3D12 \_ FEATURE \_ DATA \_ D3D12 \_ OPTIONS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options). D3D12, tuttavia, non supporta sempre lo swizzle standard. Questa funzionalità dovrà essere ricercata con una chiamata a [**CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) e selezionando il campo *StandardSwizzle64KBSupported* di **D3D12 \_ FEATURE DATA \_ \_ D3D12 \_ OPTIONS**.

Le API seguenti fanno riferimento al mapping delle trame:

Enumerazioni

-   [**D3D12 \_ LAYOUT \_ TRAMA:**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout) controlla il modello di scorrimento delle trame predefinite e abilita il supporto della mappa per le trame accessibili tramite CPU.

Strutture

-   [**D3D12 \_ RESOURCE \_ DESC:**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc) descrive una risorsa, ad esempio una trama, si tratta di una struttura ampiamente usata.
-   [**D3D12 \_ HEAP \_ DESC:**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_desc) descrive un heap.

Metodi

-   [**ID3D12Device::CreateCommittedResource:**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource) crea una singola risorsa e un heap di backup con le dimensioni e l'allineamento corretto.
-   [**ID3D12Device::CreateHeap:**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createheap) crea un heap per un buffer o una trama.
-   [**ID3D12Device::CreatePlacedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createplacedresource) : crea una risorsa inserita in un heap specifico, in genere un metodo più veloce per creare una risorsa rispetto a [**CreateHeap.**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createheap)
-   [**ID3D12Device::CreateReservedResource:**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createreservedresource) crea una risorsa riservata ma non ancora di cui non è stato eseguito il commit o inserita in un heap.
-   [**ID3D12CommandQueue::UpdateTileMappings:**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings) aggiorna i mapping dei percorsi dei riquadri nelle risorse affiancate alle posizioni di memoria in un heap delle risorse.
-   [**ID3D12Resource::Map:**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) ottiene un puntatore ai dati specificati nella risorsa e nega alla GPU l'accesso alla sottorisorsa.
-   [**ID3D12Resource::GetDesc:**](id3d12resource-getdesc.md) ottiene le proprietà della risorsa.
-   [**ID3D12Heap::GetDesc**](id3d12heap-getdesc.md) ottiene le proprietà dell'heap.
-   [**ReadFromSubresource:**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource) copia i dati da una trama di cui è stato eseguito il mapping tramite [**Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map).
-   [**WriteToSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource) : copia i dati in una trama di cui è stato eseguito il mapping tramite [**Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map).

Le risorse e gli heap padre hanno requisiti di allineamento:

-   D3D12 \_ DEFAULT \_ MSAA \_ RESOURCE PLACEMENT ALIGNMENT \_ \_ (4MB) per trame multi-campione.
-   D3D12 \_ DEFAULT RESOURCE PLACEMENT ALIGNMENT \_ \_ (64 KB) per trame \_ e buffer singoli di esempio.
-   La copia lineare di sottorisorse deve essere allineata a D3D12 TEXTURE DATA PLACEMENT ALIGNMENT (512 byte), con l'altezza della riga allineata a \_ \_ \_ \_ D3D12 \_ TEXTURE DATA PITCH ALIGNMENT \_ \_ \_ (256 byte).
-   Le visualizzazioni del buffer costante devono essere allineate a D3D12 \_ CONSTANT BUFFER DATA PLACEMENT ALIGNMENT \_ \_ \_ \_ (256 byte).

Le trame inferiori a 64 KB devono essere elaborate tramite [**CreateCommittedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource).

Con trame dinamiche (trame che cambiano ogni frame) la CPU scriverà in modo lineare nell'heap di caricamento, seguita da un'operazione di copia GPU.

In genere per creare risorse dinamiche, creare un buffer di grandi dimensioni in un heap di caricamento (vedere [Suballocation Within Buffers](large-buffers.md)). Per creare risorse di staging, creare un buffer di grandi dimensioni in un heap di readback. Per creare risorse statiche predefinite, creare risorse adiacenti in un heap predefinito. Per creare risorse con alias predefinite, creare risorse sovrapposte in un heap predefinito.

[**WriteToSubresource e**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource) [**ReadFromSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource) ridisporre i dati di trama tra un layout principale di riga e un layout di risorse non definito. L'operazione è sincrona, quindi l'applicazione deve tenere presente la pianificazione della CPU. L'applicazione può sempre suddividere la copia in aree più piccole o pianificare questa operazione in un'altra attività. Le risorse MSAA e le risorse depth-stencil con layout di risorse opache non sono supportate da queste operazioni di copia della CPU e causeranno un errore. Anche i formati che non hanno una dimensione di elemento power-of-two non sono supportati e causeranno anche un errore. È possibile che si verifichino codici restituiti di memoria insufficiente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Costanti di base**](constants.md)
</dt> <dt>

[**ID3D12Heap**](/windows/desktop/api/d3d12/nn-d3d12-id3d12heap)
</dt> <dt>

[Associazione di risorse](resource-binding.md)
</dt> </dl>

 

 




