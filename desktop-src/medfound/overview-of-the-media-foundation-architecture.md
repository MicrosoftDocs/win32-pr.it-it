---
description: Questo argomento descrive la progettazione generale di Microsoft Media Foundation. Per informazioni sull'uso Media Foundation per attività di programmazione specifiche, vedere Media Foundation Programming Guide.
ms.assetid: DEA2B19A-CF15-4BF4-84C3-9A6417C942E2
title: Panoramica dell'architettura Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de953d05c55c96d1affa2213e1a7f11143a71aa319b4671c159f085e65268d05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118239633"
---
# <a name="overview-of-the-media-foundation-architecture"></a>Panoramica dell'architettura Media Foundation

Questo argomento descrive la progettazione generale di Microsoft Media Foundation. Per informazioni sull'uso Media Foundation per attività di programmazione specifiche, [vedere Media Foundation Programming Guide](media-foundation-programming-guide.md).

Il diagramma seguente illustra una visualizzazione di alto livello dell'architettura Media Foundation principale.

![diagramma che mostra una visualizzazione di alto livello dell'architettura media foundation.](images/mfarch01.png)

Media Foundation due modelli di programmazione distinti. Il primo modello, visualizzato sul lato sinistro del diagramma, usa una pipeline end-to-end per i dati multimediali. L'applicazione inizializza la pipeline, ad esempio specificando l'URL di un file da riprodurre, e quindi chiama i metodi per controllare lo streaming. Nel secondo modello, visualizzato sul lato destro del diagramma, l'applicazione estrae i dati da un'origine o lo inserisce in una destinazione (o in entrambi). Questo modello è particolarmente utile se è necessario elaborare i dati, perché l'applicazione ha accesso diretto al flusso di dati.

### <a name="primitives-and-platform"></a>Primitive e piattaforma

A partire dalla parte inferiore del diagramma, le *primitive* sono oggetti helper usati in tutta l Media Foundation API:

-   [Gli](attributes-and-properties.md) attributi sono un modo generico per archiviare le informazioni all'interno di un oggetto, come elenco di coppie chiave/valore.
-   [I tipi di](media-types.md) supporti descrivono il formato di un flusso di dati multimediali.
-   [I buffer multimediali](media-buffers.md) contengono blocchi di dati multimediali, ad esempio fotogrammi video ed esempi audio, e vengono usati per il trasporto dei dati tra oggetti.
-   [Gli esempi di](media-samples.md) supporti sono contenitori per i buffer multimediali. Contengono anche metadati sui buffer, ad esempio timestamp.

Le [API Media Foundation platform](media-foundation-platform-apis.md) forniscono alcune funzionalità di base usate dalla pipeline di Media Foundation, ad esempio callback asincroni e code di lavoro. Alcune applicazioni potrebbero dover chiamare direttamente queste API. saranno inoltre necessari se si implementa un'origine, una trasformazione o un sink personalizzato per Media Foundation.

### <a name="media-pipeline"></a>Pipeline di supporti

La pipeline multimediale contiene tre tipi di oggetto che generano o elaborano i dati multimediali:

-   [Le origini multimediali](media-sources.md) introducono i dati nella pipeline. Un'origine multimediale potrebbe ottenere dati da un file locale, ad esempio un file video. da un flusso di rete; o da un dispositivo di acquisizione hardware.
-   [Media Foundation trasformazioni](media-foundation-transforms.md) (MFT) elaborano i dati da un flusso. I codificatori e i decodificatori vengono implementati come MFT.
-   [I sink multimediali utilizzano](media-sinks.md) i dati. ad esempio visualizzando video sullo schermo, riproducendo audio o scrivendo i dati in un file multimediale.

Terze parti possono implementare le proprie origini personalizzate, sink e MFT; ad esempio per supportare nuovi formati di file multimediali.

La [sessione multimediale](media-session.md) controlla il flusso di dati attraverso la pipeline e gestisce attività come il controllo qualità, la sincronizzazione audio/video e la risposta alle modifiche del formato.

### <a name="source-reader-and-sink-writer"></a>Lettore di origine e writer di sink

Il [lettore di](source-reader.md) origine [e il sink writer](sink-writer.md) forniscono un modo alternativo per usare i componenti Media Foundation di base (origini multimediali, trasformazioni e sink multimediali). Il lettore di origine ospita un'origine multimediale e zero o più decodificatori, mentre il writer di sink ospita un sink multimediale e zero o più codificatori. È possibile usare il lettore di origine per ottenere dati compressi o non compressi da un'origine multimediale e usare il writer di sink per codificare i dati e inviare i dati a un sink multimediale.

> [!Note]  
> Il lettore di origine e il writer di sink sono disponibili in Windows 7.

 

Questo modello di programmazione offre all'applicazione un maggiore controllo sul flusso di dati e fornisce anche all'applicazione l'accesso diretto ai dati dall'origine.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Media Foundation: concetti essenziali](media-foundation-programming--essential-concepts.md)
</dt> <dt>

[Architettura di Media Foundation](media-foundation-architecture.md)
</dt> </dl>

 

 



