---
description: Il writer di sink è un componente per la codifica di file audio o video.
ms.assetid: 23AF25B8-B94C-48BC-83D8-5863ACFFD4CA
title: Sink Writer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a1cfa60abb9b107030aba18e30175592d637c7676ff44781d62b3f5c1509351
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119887356"
---
# <a name="sink-writer"></a>Sink Writer

Il writer di sink è un componente per la codifica di file audio o video.

Il diagramma seguente illustra, a livello di alto livello, come un'applicazione usa il writer di sink per codificare e file audio/video.

![diagramma che mostra il writer di sink.](images/encoding09.png)

Il writer di sink ospita un sink multimediale e facoltativamente uno o più codificatori. I codificatori convertono dati audio o video non compressi in bitstream codificati. Il sink multimediale restituisce i bitstream in un file. Il writer di sink esegue le attività seguenti:

-   Carica il sink multimediale.
-   Trova e carica i codificatori.
-   Gestisce il flusso di dati ai codificatori e al sink multimediale.

L'applicazione passa i dati audio/video al writer di sink come input. Non è importante il modo in cui l'applicazione ottiene o genera i dati di input. Un'opzione è usare il [lettore di](source-reader.md)origine , come illustrato nel diagramma seguente. Tuttavia, il writer di sink non richiede l'uso del lettore di origine. Questi due componenti sono indipendenti.

![diagramma che mostra il lettore di origine e il writer di sink.](images/encoding02.png)

## <a name="in-this-section"></a>Contenuto della sezione

-   [Uso del writer di sink](using-the-sink-writer.md)
-   [Esercitazione: Uso del sink writer per codificare il video](tutorial--using-the-sink-writer-to-encode-video.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Codifica e creazione di file](encoding-and-file-authoring.md)
</dt> <dt>

[Panoramica della codifica in Media Foundation](overview-of-encoding-in-media-foundation.md)
</dt> </dl>

 

 



