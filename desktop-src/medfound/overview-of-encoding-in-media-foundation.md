---
description: Questo argomento è una panoramica delle API di codifica dei file fornite in Microsoft Media Foundation.
ms.assetid: 69dbef63-e272-4ad2-8d04-ae9366f79b33
title: Panoramica della codifica in Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a663260d92aad4eb23902ec35721c252f15fbba64c3404ff97bfb60f0622c674
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118239767"
---
# <a name="overview-of-encoding-in-media-foundation"></a>Panoramica della codifica in Media Foundation

Questo argomento è una panoramica delle API di codifica dei file fornite in Microsoft Media Foundation.

## <a name="terminology"></a>Terminologia

*La* codifica è un termine generale che copre diversi processi distinti:

1.  Codifica di un flusso audio o video in formati compressi. Ad esempio, codificare un flusso video in un video H.264.
2.  Multiplexing ("muxing") uno o più flussi in un flusso a byte singolo. In genere, i flussi in ingresso vengono codificati per primi. Questo passaggio potrebbe comportare il pacchetto dei flussi codificati.
3.  Scrittura di un flusso di byte multiplex in un file, ad esempio un file MP4 o ASF (Advanced Systems Format). In alternativa, il flusso multiplexed può essere inviato in rete.

Il diagramma seguente illustra questi tre processi:

![diagramma che mostra i processi di codifica e multiplexing](images/encoding03.png)

Le variazioni di questo processo includono transcodiche e remuxing:

-   *La transcoding* significa decodificare un file esistente, ri-codificare i flussi e ri-multiplexing dei flussi codificati. La transcoding può essere eseguita per convertire un file da un tipo di codifica a un altro. ad esempio per convertire il video H.264 in Windows Media Video (WMV). È anche possibile modificare la velocità in bit codificata. dimensioni del fotogramma video; frequenza dei fotogrammi; o altri parametri di formato.
-   *Rimultiplexing* o *remuxing* significa demultiplexing di un file e re-multiplexing dei flussi, senza passaggio di decodifica/codifica. Questa operazione può essere eseguita per modificare la modalità di multiplex dei pacchetti audio/video, per rimuovere un flusso o per combinare i flussi da due file di origine diversi.
-   *La transrating* è un caso speciale di transcoding, in cui la velocità in bit viene modificata senza modificare il tipo di compressione. Ad esempio, è possibile convertire un file a velocità in bit elevata in una velocità in bit inferiore. Uno scenario tipico in cui è possibile usare la transrating è la sincronizzazione del contenuto multimediale da un PC a un dispositivo portatile. Se il dispositivo portatile non supporta una velocità in bit elevata, il file potrebbe essere transrated prima di essere copiato nel dispositivo portatile.

Il diagramma a blocchi seguente illustra il processo di transcodizzazione.

![Diagramma che mostra il processo di transcoding](images/encoding05.png)

Il diagramma a blocchi seguente illustra il processo di remuxing.

![Diagramma che mostra il processo di remuxing](images/encoding06.png)

Questa documentazione a volte usa il termine *codifica* per includere sia la transcoding che la ricorsione. Quando è importante distinguere tra di essi, la documentazione noterà la differenza.

Vedere anche: [Media Foundation: Concetti essenziali](media-foundation-programming--essential-concepts.md).

## <a name="media-foundation-encoding-architecture"></a>Media Foundation di codifica

Al livello più basso dell'architettura Media Foundation, per la codifica vengono usati i tipi di componente seguenti:

-   Per la transcodrialità, [le origini](media-sources.md) multimediali vengono usate per demultiplexare il file di origine.
-   Per il processo di codifica, [Media Foundation le trasformazioni](media-foundation-transforms.md) vengono usate per decodificare e codificare i flussi.
-   Per il processo di multiplexing, i [sink](media-sinks.md) multimediali vengono usati per eseguire il multiplexing dei flussi e scrivere il flusso multiplexed in un file o in una rete.

Il diagramma seguente illustra il flusso di dati tra questi componenti in uno scenario di transcoding:

![diagramma che mostra i componenti usati nella transcoding](images/encoding04.png)

La maggior parte delle applicazioni non userà questi componenti direttamente. Un'applicazione userà invece API di livello superiore che gestiscono questi componenti di livello inferiore. Media Foundation fornisce due API di livello superiore per la codifica:

<dl> <dt>

<span id="Media_Session"></span><span id="media_session"></span><span id="MEDIA_SESSION"></span>[Sessione multimediale](media-session.md)
</dt> <dd>

La sessione multimediale fornisce una pipeline end-to-end che sposta i dati dall'origine multimediale, tramite i codec e infine al sink multimediale. L'applicazione controlla la sessione multimediale e riceve gli eventi di stato dalla sessione multimediale.

</dd> <dt>

<span id="Source_Reader_plus_Sink_Writer"></span><span id="source_reader_plus_sink_writer"></span><span id="SOURCE_READER_PLUS_SINK_WRITER"></span>[Lettore di origine](source-reader.md) e [writer di sink](sink-writer.md)
</dt> <dd>

Il lettore di origine esegue il wrapping dell'origine multimediale e, facoltativamente, dei decodificatori. Fornisce esempi codificati o decodificati dell'applicazione. Il writer di sink esegue il wrapping del sink multimediale e, facoltativamente, dei codificatori. L'applicazione passa gli esempi al writer di sink.

</dd> </dl>

Il diagramma seguente illustra la sessione multimediale:

![Diagramma che mostra come la sessione multimediale esegue la transcoding](images/encoding01.png)

[L'API Transcode](transcode-api.md) (la casella ombreggiata blu) è un set di API introdotte in Windows 7, che semplificano la configurazione della sessione multimediale per la codifica.

Il diagramma successivo mostra il lettore di origine e il sink writer:

![Diagramma che illustra la transcoding con il lettore di origine e il writer di sink](images/encoding02.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Codifica e creazione di file](encoding-and-file-authoring.md)
</dt> <dt>

[Media Foundation programmazione: concetti essenziali](media-foundation-programming--essential-concepts.md)
</dt> </dl>

 

 



