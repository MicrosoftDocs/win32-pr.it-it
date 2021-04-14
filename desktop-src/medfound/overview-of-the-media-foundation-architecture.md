---
description: In questo argomento viene descritta la progettazione generale di Microsoft Media Foundation. Per informazioni sull'utilizzo di Media Foundation per attività di programmazione specifiche, vedere Guida alla programmazione di Media Foundation.
ms.assetid: DEA2B19A-CF15-4BF4-84C3-9A6417C942E2
title: Panoramica dell'architettura Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0944eae1a74c1a5ba3dda8d94b69088128237f1
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104551941"
---
# <a name="overview-of-the-media-foundation-architecture"></a>Panoramica dell'architettura Media Foundation

In questo argomento viene descritta la progettazione generale di Microsoft Media Foundation. Per informazioni sull'utilizzo di Media Foundation per attività di programmazione specifiche, vedere [Guida alla programmazione di Media Foundation](media-foundation-programming-guide.md).

Nel diagramma seguente viene illustrata una visualizzazione di alto livello dell'architettura Media Foundation.

![diagramma che mostra una visualizzazione di alto livello dell'architettura di Media Foundation.](images/mfarch01.png)

Media Foundation fornisce due modelli di programmazione distinti. Il primo modello, visualizzato sul lato sinistro del diagramma, usa una pipeline end-to-end per i dati multimediali. L'applicazione Inizializza la pipeline, ad esempio specificando l'URL di un file da riprodurre, quindi chiama i metodi per controllare il flusso. Nel secondo modello, visualizzato sul lato destro del diagramma, l'applicazione estrae i dati da un'origine o li inserisce in una destinazione (o entrambi). Questo modello è particolarmente utile se è necessario elaborare i dati, perché l'applicazione ha accesso diretto al flusso di dati.

### <a name="primitives-and-platform"></a>Primitive e piattaforma

A partire dalla fine del diagramma, le *primitive* sono oggetti helper usati nell'API Media Foundation:

-   [Gli attributi](attributes-and-properties.md) sono un modo generico per archiviare le informazioni all'interno di un oggetto, come un elenco di coppie chiave/valore.
-   I [tipi di supporto](media-types.md) descrivono il formato di un flusso di dati multimediali.
-   I [buffer multimediali](media-buffers.md) contengono blocchi di dati multimediali, ad esempio fotogrammi video ed esempi audio, e vengono usati per il trasporto di dati tra oggetti.
-   Gli [esempi di supporti](media-samples.md) sono contenitori per i buffer multimediali. Contengono anche i metadati relativi ai buffer, ad esempio i timestamp.

Le [API della piattaforma Media Foundation](media-foundation-platform-apis.md) forniscono alcune funzionalità di base usate dalla pipeline Media Foundation, ad esempio callback asincroni e code di lavoro. Alcune applicazioni potrebbero dover chiamare direttamente queste API; Inoltre, sarà necessario se si implementa un'origine, una trasformazione o un sink personalizzato per Media Foundation.

### <a name="media-pipeline"></a>Pipeline multimediale

La pipeline multimediale contiene tre tipi di oggetto che generano o elaborano i dati multimediali:

-   Le [origini supporti](media-sources.md) introducono dati nella pipeline. Un'origine multimediale può ottenere dati da un file locale, ad esempio un file video; da un flusso di rete; o da un dispositivo di acquisizione hardware.
-   [Media Foundation Transforms](media-foundation-transforms.md) (MFTS) elabora i dati da un flusso. Codificatori e decodificatori vengono implementati come MFTs.
-   I [sink dei supporti](media-sinks.md) utilizzano i dati; ad esempio, visualizzando il video sullo schermo, riproducendo audio o scrivendo i dati in un file multimediale.

Le terze parti possono implementare origini, sink e MFTs personalizzati; ad esempio, per supportare nuovi formati di file multimediali.

La [sessione multimediale](media-session.md) controlla il flusso di dati attraverso la pipeline e gestisce attività quali il controllo della qualità, la sincronizzazione audio/video e la risposta alle modifiche del formato.

### <a name="source-reader-and-sink-writer"></a>Reader di origine e writer di sink

Il [lettore di origine](source-reader.md) e il [writer di sink](sink-writer.md) forniscono una modalità alternativa per usare i componenti di base Media Foundation (origini supporti, trasformazioni e sink multimediali). Il lettore di origine ospita un'origine multimediale e zero o più decodificatori, mentre il writer del sink ospita un sink multimediale e zero o più codificatori. È possibile usare il lettore di origine per ottenere dati compressi o non compressi da un'origine multimediale e usare il writer di sink per codificare i dati e inviare i dati a un sink multimediale.

> [!Note]  
> Il lettore di origine e il writer di sink sono disponibili in Windows 7.

 

Questo modello di programmazione fornisce all'applicazione un maggiore controllo sul flusso di dati e fornisce anche l'accesso diretto all'applicazione ai dati dall'origine.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Media Foundation: concetti essenziali](media-foundation-programming--essential-concepts.md)
</dt> <dt>

[Architettura di Media Foundation](media-foundation-architecture.md)
</dt> </dl>

 

 



