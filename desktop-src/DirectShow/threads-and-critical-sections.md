---
description: Thread e sezioni critiche
ms.assetid: e55acb06-03f4-4191-bffe-3196f41ef2c7
title: Thread e sezioni critiche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 576cb28e7e382db92328adf09980a825e71b5a3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350336"
---
# <a name="threads-and-critical-sections"></a>Thread e sezioni critiche

Questa sezione descrive il threading nei filtri DirectShow e i passaggi da eseguire per evitare arresti anomali o deadlock in un filtro personalizzato.

Negli esempi di questa sezione viene usato pseudocodice per illustrare il codice che è necessario scrivere. Si presuppone che un filtro personalizzato usi classi derivate dalle classi base di DirectShow, come indicato di seguito:

-   CMyInputPin: derivato da [**CBaseInputPin**](cbaseinputpin.md).
-   CMyOutputPin: derivato da [**CBaseOutputPin**](cbaseoutputpin.md).
-   CMyFilter: derivato da [**CBaseFilter**](cbasefilter.md).
-   CMyInputAllocator: allocatore del PIN di input, derivato da [**CMemAllocator**](cmemallocator.md). Non tutti i filtri necessitano di un allocatore personalizzato. Per molti filtri, la classe **CMemAllocator** è sufficiente.

In questa sezione vengono trattati gli argomenti seguenti.

-   [Il flusso e i thread dell'applicazione](the-streaming-and-application-threads.md)
-   [Sospensione in corso](pausing.md)
-   [Ricezione e distribuzione di esempi](receiving-and-delivering-samples.md)
-   [Distribuzione della fine del flusso](delivering-the-end-of-stream.md)
-   [Scaricamento dei dati](flushing-data.md)
-   [Stopping](stopping.md)
-   [Recupero di buffer](getting-buffers.md)
-   [Thread di streaming e gestione del grafo dei filtri](streaming-threads-and-the-filter-graph-manager.md)
-   [Riepilogo del threading del filtro](summary-of-filter-threading.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Flusso di dati per sviluppatori di filtri](data-flow-for-filter-developers.md)
</dt> <dt>

[Scrittura di filtri DirectShow](writing-directshow-filters.md)
</dt> </dl>

 

 



