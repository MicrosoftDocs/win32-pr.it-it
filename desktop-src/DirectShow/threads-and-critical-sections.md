---
description: Thread e sezioni critiche
ms.assetid: e55acb06-03f4-4191-bffe-3196f41ef2c7
title: Thread e sezioni critiche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d13473a917ae49e80ec658b0d6187fdfdff80c6e3a080a229aca7ccbbe536c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118651404"
---
# <a name="threads-and-critical-sections"></a>Thread e sezioni critiche

Questa sezione descrive il threading nei DirectShow e i passaggi da eseguire per evitare arresti anomali o deadlock in un filtro personalizzato.

Gli esempi in questa sezione usano lo pseudocodice per illustrare il codice che sarà necessario scrivere. Presuppongono che un filtro personalizzato utilizzi classi derivate DirectShow di base, come indicato di seguito:

-   CMyInputPin: derivato da [**CBaseInputPin**](cbaseinputpin.md).
-   CMyOutputPin: derivato da [**CBaseOutputPin**](cbaseoutputpin.md).
-   CMyFilter: derivato da [**CBaseFilter**](cbasefilter.md).
-   CMyInputAllocator: allocatore del pin di input, derivato [**da CMemAllocator**](cmemallocator.md). Non tutti i filtri hanno bisogno di un allocatore personalizzato. Per molti filtri, la **classe CMemAllocator** è sufficiente.

In questa sezione vengono trattati gli argomenti seguenti.

-   [Thread di streaming e applicazione](the-streaming-and-application-threads.md)
-   [Sospensione in corso](pausing.md)
-   [Ricezione e distribuzione di esempi](receiving-and-delivering-samples.md)
-   [Distribuzione della fine del flusso](delivering-the-end-of-stream.md)
-   [Scaricamento dei dati](flushing-data.md)
-   [Stopping](stopping.md)
-   [Recupero di buffer](getting-buffers.md)
-   [Thread di streaming e Gestione Graph Filtro](streaming-threads-and-the-filter-graph-manager.md)
-   [Riepilogo del threading dei filtri](summary-of-filter-threading.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Dati Flow per sviluppatori di filtri](data-flow-for-filter-developers.md)
</dt> <dt>

[Scrittura di DirectShow filtri](writing-directshow-filters.md)
</dt> </dl>

 

 



