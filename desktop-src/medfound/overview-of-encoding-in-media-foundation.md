---
description: Questo argomento è una panoramica delle API di codifica dei file disponibili in Microsoft Media Foundation.
ms.assetid: 69dbef63-e272-4ad2-8d04-ae9366f79b33
title: Cenni preliminari sulla codifica in Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81882bd6da43f4040614347b662d988844c7b7a6
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104563668"
---
# <a name="overview-of-encoding-in-media-foundation"></a>Cenni preliminari sulla codifica in Media Foundation

Questo argomento è una panoramica delle API di codifica dei file disponibili in Microsoft Media Foundation.

## <a name="terminology"></a>Terminologia

La *codifica* è un termine generale che copre diversi processi distinti:

1.  Codifica di un flusso audio o video in formati compressi. Ad esempio, la codifica di un flusso video nel video H. 264.
2.  Multiplexing ("muxing") di uno o più flussi in un flusso a byte singolo. In genere, i flussi in ingresso vengono codificati per primi. Questo passaggio può comportare il packetizing dei flussi codificati.
3.  Scrittura di un flusso di byte multiplex in un file, ad esempio un file MP4 o Advanced Systems Format (ASF). In alternativa, il flusso multiplex può essere inviato in rete.

Il diagramma seguente illustra questi tre processi:

![diagramma che illustra i processi di codifica e multiplex](images/encoding03.png)

Le varianti di questo processo includono la transcodifica e remuxing:

-   La *transcodifica* significa la decodifica di un file esistente, la ricodifica dei flussi e il nuovo multiplexing dei flussi codificati. La transcodifica può essere eseguita per convertire un file da un tipo di codifica a un altro; ad esempio, per convertire il video H. 264 in Windows Media Video (WMV). Questa operazione può essere eseguita anche per modificare la velocità in bit codificata; dimensioni del fotogramma video; frequenza dei fotogrammi; o altri parametri di formato.
-   Il *rimultiplexing* o *remuxing* indica il demultiplexing di un file e il nuovo multiplexing dei flussi, senza passaggio di decodifica/codifica. Questa operazione può essere eseguita per modificare il modo in cui i pacchetti audio/video vengono multiplexati, per rimuovere un flusso o per combinare flussi da due file di origine diversi.
-   *Transrating* è un caso speciale di transcodifica, in cui la velocità in bit viene modificata senza modificare il tipo di compressione. Ad esempio, è possibile convertire un file a velocità elevata a una velocità in bit inferiore. Uno scenario tipico in cui è possibile usare la transclassificazione è quando si sincronizza il contenuto multimediale da un PC a un dispositivo portatile. Se il dispositivo portatile non supporta una velocità in bit elevata, è possibile che il file venga rivalutato prima di essere copiato nel dispositivo portatile.

Il diagramma di blocco seguente illustra il processo di transcodifica.

![diagramma che illustra il processo di transcodifica](images/encoding05.png)

Il diagramma di blocco seguente illustra il processo remuxing.

![diagramma che mostra il processo remuxing](images/encoding06.png)

Questa documentazione usa talvolta la *codifica* dei termini per includere sia la transcodifica che remuxing. Quando è importante distinguere tra di essi, la documentazione nota la differenza.

Vedere anche: [Media Foundation: concetti essenziali](media-foundation-programming--essential-concepts.md).

## <a name="media-foundation-encoding-architecture"></a>Architettura di codifica Media Foundation

Al livello più basso dell'architettura Media Foundation, per la codifica vengono usati i tipi di componenti seguenti:

-   Per la transcodifica, le [origini multimediali](media-sources.md) vengono usate per demultiplexare il file di origine.
-   Per il processo di codifica, [Media Foundation le trasformazioni](media-foundation-transforms.md) vengono usate per decodificare e codificare i flussi.
-   Per il processo di multiplexing, i [sink di supporto](media-sinks.md) vengono usati per eseguire il multiplexing dei flussi e scrivere il flusso multiplexato in un file o in una rete.

Il diagramma seguente illustra il flusso di dati tra questi componenti in uno scenario di transcodifica:

![diagramma che illustra i componenti utilizzati per la transcodifica](images/encoding04.png)

La maggior parte delle applicazioni non utilizzerà direttamente questi componenti. Al contrario, un'applicazione userà API di livello superiore che gestiscono questi componenti di livello inferiore. Media Foundation fornisce due API di livello superiore per la codifica:

<dl> <dt>

<span id="Media_Session"></span><span id="media_session"></span><span id="MEDIA_SESSION"></span>[Sessione multimediale](media-session.md)
</dt> <dd>

La sessione multimediale fornisce una pipeline end-to-end che sposta i dati dall'origine multimediale, tramite i codec e infine al sink multimediale. L'applicazione controlla la sessione multimediale e riceve gli eventi di stato dalla sessione multimediale.

</dd> <dt>

<span id="Source_Reader_plus_Sink_Writer"></span><span id="source_reader_plus_sink_writer"></span><span id="SOURCE_READER_PLUS_SINK_WRITER"></span>[Reader di origine](source-reader.md) e [writer di sink](sink-writer.md)
</dt> <dd>

Il lettore di origine esegue il wrapping dell'origine multimediale e, facoltativamente, dei decodificatori. Fornisce esempi codificati o decodificati nell'applicazione. Il writer di sink esegue il wrapping del sink multimediale e, facoltativamente, dei codificatori. L'applicazione passa gli esempi al writer del sink.

</dd> </dl>

Il diagramma seguente illustra la sessione multimediale:

![diagramma che illustra il modo in cui la sessione multimediale esegue la transcodifica](images/encoding01.png)

L' [API transcode](transcode-api.md) (la casella ombreggiata blu) è un set di API introdotte in Windows 7, che semplificano la configurazione della sessione multimediale per la codifica.

Il diagramma seguente mostra l'Reader di origine e il writer del sink:

![diagramma che mostra la transcodifica con l'Reader di origine e il writer di sink](images/encoding02.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Codifica e creazione di file](encoding-and-file-authoring.md)
</dt> <dt>

[Programmazione Media Foundation: concetti essenziali](media-foundation-programming--essential-concepts.md)
</dt> </dl>

 

 



