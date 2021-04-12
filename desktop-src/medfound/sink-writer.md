---
description: Il writer di sink è un componente per la codifica di file audio o video.
ms.assetid: 23AF25B8-B94C-48BC-83D8-5863ACFFD4CA
title: Writer sink
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6b30d75e369de343bae61ba56dfd05c0d5d12a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344386"
---
# <a name="sink-writer"></a>Writer sink

Il writer di sink è un componente per la codifica di file audio o video.

Il diagramma seguente illustra, a livello generale, il modo in cui un'applicazione usa il writer di sink per codificare e file audio/video.

![diagramma che mostra il writer del sink.](images/encoding09.png)

Il writer di sink ospita un sink multimediale e, facoltativamente, uno o più codificatori. I codificatori convertono i dati audio o video non compressi nei Bitstream codificati. Il sink multimediale restituisce i Bitstream a un file. Il writer di sink esegue le attività seguenti:

-   Carica il sink multimediale.
-   Trova e carica i codificatori.
-   Gestisce il flusso di dati ai codificatori e al sink multimediale.

L'applicazione passa i dati audio/video al writer di sink come input. Non è importante il modo in cui l'applicazione Ottiene o genera i dati di input. Un'opzione consiste nell'usare il [lettore di origine](source-reader.md), come illustrato nel diagramma seguente. Tuttavia, il writer di sink non richiede l'utilizzo del lettore di origine. Questi due componenti sono indipendenti.

![diagramma che mostra l'Reader di origine e il writer del sink.](images/encoding02.png)

## <a name="in-this-section"></a>Contenuto della sezione

-   [Uso del writer di sink](using-the-sink-writer.md)
-   [Esercitazione: uso del writer di sink per codificare video](tutorial--using-the-sink-writer-to-encode-video.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Codifica e creazione di file](encoding-and-file-authoring.md)
</dt> <dt>

[Cenni preliminari sulla codifica in Media Foundation](overview-of-encoding-in-media-foundation.md)
</dt> </dl>

 

 



