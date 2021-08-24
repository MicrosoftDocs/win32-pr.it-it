---
description: Modello pull
ms.assetid: b5246dfe-e6ee-4b91-bfe3-2ec8b8723938
title: Modello pull
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9832f719e21d85fd09fbf92303e404290d7d99efd6953ace398f77167d0263a1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747891"
---
# <a name="pull-model"></a>Modello pull

[**Nell'interfaccia IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) il filtro upstream determina i dati da inviare ed eserciterà il push dei dati nel filtro downstream. Per alcuni filtri, un *modello pull* è più appropriato. In questo caso, il filtro downstream richiede i dati dal filtro upstream. Gli esempi viaggiano ancora a valle, dal pin di output al pin di input, ma il filtro downstream avvia il flusso di dati. Questo tipo di connessione usa [**l'interfaccia IAsyncReader.**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader)

L'uso tipico per il modello pull è la riproduzione di file. Ad esempio, in un grafico di riproduzione AVI, il filtro [Origine file](file-source--async--filter.md) asincrona esegue operazioni di lettura di file generiche e recapita i dati come flusso di byte, senza informazioni sul formato. Il [filtro AVI Splitter](avi-splitter-filter.md) legge le intestazioni AVI e analizza il flusso in esempi video e audio. Lo splitter AVI può determinare i dati che servono meglio del filtro Origine file asincrona e quindi usa **IAsyncReader** anziché **IMemInputPin.**

Per richiedere dati dal pin di output, il pin di input chiama uno dei metodi seguenti:

-   [**IAsyncReader::Request**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-request)
-   [**IAsyncReader::SyncRead**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-syncread)
-   [**IAsyncReader::SyncReadAligned**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-syncreadaligned).

Il primo metodo è asincrono, per supportare più letture sovrapposte. Gli altri sono sincroni.

In teoria, qualsiasi filtro può supportare **IAsyncReader,** ma in pratica è progettato per i filtri di origine che si connettono ai filtri del parser. Il parser agisce in modo molto simile a un filtro di origine nel modello push. Quando viene sospeso, crea un thread di streaming che estrae i dati dalla connessione **IAsyncReader** ed esegue il push a valle. I pin di output **usano IMemInputPin** e il resto del grafico usa il modello push standard.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Dati Flow nel filtro Graph](data-flow-in-the-filter-graph.md)
</dt> </dl>

 

 



