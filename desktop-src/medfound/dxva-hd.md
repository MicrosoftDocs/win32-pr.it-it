---
description: Microsoft DirectX Video Acceleration High Definition (DXVA-HD) è un'API per l'elaborazione video con accelerazione hardware.
ms.assetid: 38ebec28-c4fc-4e72-ac87-1e41707d1908
title: DXVA-HD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a40e23d6e91f576f062c52a0f58d0bfe1f769ad3879581b01386333266cb0553
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119958651"
---
# <a name="dxva-hd"></a>DXVA-HD

Microsoft DirectX Video Acceleration High Definition (DXVA-HD) è un'API per l'elaborazione video con accelerazione hardware. DXVA-HD usa la GPU per eseguire funzioni quali deinterlacing, compositing e conversione dello spazio dei colori.

DXVA-HD è simile all'elaborazione video [DXVA](dxva-video-processing.md) (DXVA-VP), ma offre funzionalità avanzate e un modello di elaborazione più semplice. Fornendo un modello di composizione più flessibile, DXVA-HD è progettato per supportare la prossima generazione di formati ottici HD e standard di trasmissione.

L'API DXVA-HD richiede un driver video WDDM che supporta l'interfaccia DXVA-HD del driver di dispositivo (DDI) o un processore software plug-in.

-   [Miglioramenti rispetto a DXVA-VP](#improvements-over-dxva-vp)
-   [Argomenti correlati](#related-topics)

## <a name="improvements-over-dxva-vp"></a>Miglioramenti rispetto a DXVA-VP

DXVA-HD espande il set di funzionalità fornite da DXVA-VP. I miglioramenti includono:

-   Combinazione di RGB e YUV. Qualsiasi flusso può essere RGB o YUV. Non esiste più una distinzione tra il flusso primario e i flussi secondari.
-   Deinterlacing di più flussi. Qualsiasi flusso può essere progressivo o interlacciato. Inoltre, la cadenza e la frequenza dei fotogrammi possono variare da un flusso di input al successivo.
-   Colori di sfondo RGB. In precedenza, erano supportati solo i colori di sfondo YUV.
-   Luma keying. Quando luma keying è abilitato, i valori luma che rientrano in un intervallo designato diventano trasparenti.
-   Passaggio dinamico tra le modalità deinterlace.

DXVA-HD definisce anche alcune funzionalità avanzate che i driver possono supportare. Tuttavia, le applicazioni non devono presupporre che tutti i driver supportino queste funzionalità. Le funzionalità avanzate includono:

-   Telecina inversa (ad esempio, da 60i a 24p).
-   Conversione della frequenza dei fotogrammi (ad esempio, da 24p a 120p).
-   Modalità di riempimento alfa.
-   Riduzione del rumore e filtro per il miglioramento dei bordi.
-   Ridimensionamento anamorfico non lineare.
-   YCbCr esteso (xvYCC).

In questa sezione vengono trattati gli argomenti seguenti.

-   [Creazione di un processore video DXVA-HD](creating-a-dxva-hd-video-processor.md)
-   [Controllo dei formati DXVA-HD supportati](checking-supported-dxva-hd-formats.md)
-   [Creazione di superfici video DXVA-HD](creating-dxva-hd-video-surfaces.md)
-   [Impostazione degli stati DXVA-HD](setting-dxva-hd-states.md)
-   [Esecuzione del blit DXVA-HD](performing-the-dxva-hd-blit.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Accelerazione video DirectX 2.0](directx-video-acceleration-2-0.md)
</dt> <dt>

[Esempio DXVA-HD](dxva-hd-sample.md)
</dt> </dl>

 

 



