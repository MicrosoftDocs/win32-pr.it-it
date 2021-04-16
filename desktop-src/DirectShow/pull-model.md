---
description: Modello pull
ms.assetid: b5246dfe-e6ee-4b91-bfe3-2ec8b8723938
title: Modello pull
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8dd4becd54bffb39acf30b6d29fca45e6a117989
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521345"
---
# <a name="pull-model"></a>Modello pull

Nell'interfaccia [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) il filtro upstream determina i dati da inviare e inserisce i dati nel filtro downstream. Per alcuni filtri, un modello *pull* è più appropriato. In questo caso il filtro downstream richiede i dati dal filtro upstream. Gli esempi continuano a raggiungere downstream, dal pin di output al pin di input, ma il filtro downstream avvia il flusso di dati. Questo tipo di connessione utilizza l'interfaccia [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) .

L'uso tipico del modello pull è la riproduzione del file. Ad esempio, in un grafico di riproduzione AVI, il filtro di [origine file asincrono](file-source--async--filter.md) esegue operazioni generiche di lettura dei file e recapita i dati come flusso di byte senza informazioni sul formato. Il filtro [splitter AVI](avi-splitter-filter.md) legge le intestazioni AVI e analizza il flusso in esempi video e audio. Il separatore AVI è in grado di determinare i dati necessari meglio rispetto al filtro di origine file asincrono, quindi usa **IAsyncReader** anziché **IMemInputPin**.

Per richiedere dati dal pin di output, il pin di input chiama uno dei metodi seguenti:

-   [**IAsyncReader:: Request**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-request)
-   [**IAsyncReader::SyncRead**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-syncread)
-   [**IAsyncReader:: SyncReadAligned**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-syncreadaligned).

Il primo metodo è asincrono per supportare più letture sovrapposte. Le altre sono sincrone.

In teoria, qualsiasi filtro può supportare **IAsyncReader**, ma in pratica è progettato per i filtri di origine che si connettono ai filtri del parser. Il parser funziona in modo molto simile a un filtro di origine nel modello push. Quando viene sospesa, viene creato un thread di streaming che estrae i dati dalla connessione **IAsyncReader** e li inserisce a valle. I pin di output usano **IMemInputPin** e il resto del grafo usa il modello push standard.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Flusso di dati nel grafico del filtro](data-flow-in-the-filter-graph.md)
</dt> </dl>

 

 



