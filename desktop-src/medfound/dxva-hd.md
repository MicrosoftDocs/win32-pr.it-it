---
description: Microsoft DirectX Video Acceleration High Definition (DXVA-HD) è un'API per l'elaborazione video con accelerazione hardware.
ms.assetid: 38ebec28-c4fc-4e72-ac87-1e41707d1908
title: DXVA-HD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f8694a28d8d5871112590c90bf166d1aa9246e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749255"
---
# <a name="dxva-hd"></a>DXVA-HD

Microsoft DirectX Video Acceleration High Definition (DXVA-HD) è un'API per l'elaborazione video con accelerazione hardware. DXVA-HD usa la GPU per eseguire funzioni quali deinterlacciamento, composizione e conversione dello spazio colore.

DXVA-HD è simile all' [elaborazione video DXVA](dxva-video-processing.md) (DXVA-VP), ma offre funzionalità avanzate e un modello di elaborazione più semplice. Grazie a un modello di composizione più flessibile, DXVA-HD è progettato per supportare la nuova generazione di formati ottici HD e standard broadcast.

L'API DXVA-HD richiede un driver di visualizzazione WDDM che supporta l'interfaccia DDI (Device Driver Interface) DXVA-HD o un processore software plug-in.

-   [Miglioramenti rispetto a DXVA-VP](#improvements-over-dxva-vp)
-   [Argomenti correlati](#related-topics)

## <a name="improvements-over-dxva-vp"></a>Miglioramenti rispetto a DXVA-VP

DXVA-HD espande il set di funzionalità fornite da DXVA-VP. I miglioramenti includono:

-   Combinazione di RGB e YUV. Qualsiasi flusso può essere RGB o YUV. Non esiste più una distinzione tra il flusso primario e i sottoflussi.
-   Deinterlacciamento di più flussi. Qualsiasi flusso può essere progressivo o interlacciato. Inoltre, la cadenza e la frequenza dei fotogrammi possono variare da un flusso di input a quello successivo.
-   Colori di sfondo RGB. In precedenza erano supportati solo i colori di sfondo YUV.
-   Chiavi Luma. Quando è abilitata la chiave Luma, i valori Luma che rientrano in un intervallo designato diventano trasparenti.
-   Spostamento dinamico tra modalità di deinterlacciamento.

DXVA-HD definisce anche alcune funzionalità avanzate che i driver possono supportare. Tuttavia, le applicazioni non devono presupporre che tutti i driver supportino queste funzionalità. Le funzionalità avanzate includono:

-   Telecine inversa (ad esempio, da 60i a 24p).
-   Conversione della frequenza dei fotogrammi (ad esempio, 24p in 120P).
-   Modalità di riempimento alfa.
-   Riduzione del rumore e filtro di miglioramento del perimetro.
-   Ridimensionamento non lineare Anamorfo.
-   Extended YCbCr (xvYCC).

In questa sezione vengono trattati gli argomenti seguenti.

-   [Creazione di un processore video DXVA-HD](creating-a-dxva-hd-video-processor.md)
-   [Controllo dei formati DXVA-HD supportati](checking-supported-dxva-hd-formats.md)
-   [Creazione di superfici video DXVA-HD](creating-dxva-hd-video-surfaces.md)
-   [Impostazione di DXVA-stati HD](setting-dxva-hd-states.md)
-   [Esecuzione di DXVA-HD blit](performing-the-dxva-hd-blit.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Accelerazione video DirectX 2,0](directx-video-acceleration-2-0.md)
</dt> <dt>

[Esempio di DXVA-HD](dxva-hd-sample.md)
</dt> </dl>

 

 



