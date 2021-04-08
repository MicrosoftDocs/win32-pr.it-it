---
description: Digitare-1 rispetto a
ms.assetid: 3f1cf981-f678-46a6-9784-ffb389438b6d
title: Tipo-1 e file AVI DV di tipo 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0000b81e94e25749b5590287145a88a28280e16d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967691"
---
# <a name="type-1-vs-type-2-dv-avi-files"></a>Tipo-1 e file AVI DV di tipo 2

Le fotocamere DV producono audio-video con interfoliazione ogni frame di video contiene anche le informazioni audio. Se si salvano i dati DV in un file AVI, è possibile scegliere:

-   Archiviare i dati con interfoliazione come un flusso nel file AVI. Questa operazione è nota come file di tipo 1.
-   Suddividere i dati con interfoliazione in flussi audio e video distinti. Questa operazione è nota come file di tipo 2.

Per l'acquisizione video, in cui la velocità effettiva massima è cruciale, è preferibile usare un file di tipo 1, perché i file di tipo 2 contengono dati audio ridondanti. Il flusso video contiene ancora i dati audio. L'audio è semplicemente nascosto etichettando il flusso come video. Inoltre, la scrittura di un file di tipo 2 richiede un tempo di elaborazione aggiuntivo per suddividere il flusso con interfoliazione.

D'altra parte, i file di tipo 1 risultano meno efficienti per la modifica in tempo reale. L'applicazione deve estrarre l'audio dal flusso con interfoliazione, apportare le modifiche ed eseguire di nuovo l'interfoliazione dei dati. Inoltre, il formato di tipo-1 non è compatibile con Microsoft® video for Windows® (VFW). DirectShow è in grado di gestire entrambi i tipi di file.

Un file di tipo 2 può essere convertito nel tipo-1 usando il filtro [muxer DV](dv-muxer-filter.md) . Un file di tipo 1 può essere convertito nel tipo-2 usando il filtro della [barra di divisione DV](dv-splitter-filter.md) . Il diagramma seguente illustra la differenza tra i due formati.

![conversione tra Type-1 e Type-2 DV](images/dv-filters3.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Video digitale in DirectShow](digital-video-in-directshow.md)
</dt> <dt>

[Dati DV nel formato di file AVI](dv-data-in-the-avi-file-format.md)
</dt> </dl>

 

 



