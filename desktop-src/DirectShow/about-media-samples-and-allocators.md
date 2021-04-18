---
description: Informazioni su esempi e allocatori multimediali
ms.assetid: d6283bf0-0460-4519-9a56-fd4c78cfaabc
title: Informazioni su esempi e allocatori multimediali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9105228e70f82aaa7c36b7e7d28cf7e748e1e2f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320478"
---
# <a name="about-media-samples-and-allocators"></a>Informazioni su esempi e allocatori multimediali

I filtri distribuiscono i dati tra connessioni pin. I dati vengono spostati dal pin di output di un filtro al pin di input di un altro filtro. Il modo più comune per inviare i dati al pin di output consiste nel chiamare il metodo [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) sull'input, sebbene esistano anche altri meccanismi.

A seconda del filtro, è possibile allocare memoria per i dati multimediali in diversi modi: sull'heap, in una superficie DirectDraw, usando la memoria GDI condivisa o usando un altro meccanismo di allocazione. L'oggetto responsabile dell'allocazione della memoria viene definito *allocatore*, ovvero un oggetto com che espone l'interfaccia [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) .

Quando due pin si connettono, uno dei pin deve fornire un allocatore. DirectShow definisce una sequenza di chiamate al metodo usata per stabilire quale pin fornisce l'allocatore. I pin concordano anche sul numero di buffer che l'allocatore creerà e sulle dimensioni dei buffer.

Prima dell'inizio del flusso, l'allocatore crea un pool di buffer. Durante il flusso, il filtro upstream riempie i buffer con i dati e li recapita al filtro downstream. Tuttavia, il filtro upstream non assegna ai buffer i puntatori non elaborati del filtro downstream. USA invece oggetti COM denominati *esempi di supporti*, creati dall'allocatore per gestire i buffer. Gli esempi di supporti espongono l'interfaccia [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) . Un esempio multimediale contiene:

-   puntatore al buffer sottostante
-   timestamp
-   diversi flag
-   Facoltativamente, un tipo di supporto

Il timestamp definisce l'ora di presentazione, che il filtro renderer USA per pianificare il rendering. I flag indicano elementi come se si fosse verificato un break nei dati rispetto all'esempio precedente. Il tipo di supporto fornisce un modo per i filtri per modificare i formati a metà flusso. In genere, l'esempio non dispone di un tipo di supporto, che indica che il formato non è stato modificato rispetto all'esempio precedente.

Mentre un filtro usa un buffer, include il conteggio dei riferimenti nell'esempio. L'allocatore utilizza il conteggio dei riferimenti per determinare quando è possibile riutilizzare il buffer. In questo modo si impedisce a un filtro di sovrascrivere un buffer che è ancora in uso da un altro filtro. Un esempio non restituisce al pool di allocatori gli esempi disponibili fino a quando non viene rilasciato da ogni filtro.

Per altre informazioni, vedere i seguenti argomenti:

-   Nell'argomento [esempi e allocatori](samples-and-allocators.md) viene fornita una descrizione più dettagliata del funzionamento degli allocatori.
-   Il flusso di dati dell'argomento [nel grafico dei filtri](data-flow-in-the-filter-graph.md) fornisce una panoramica generale del flusso di dati in DirectShow.

Gli argomenti seguenti sono destinati agli sviluppatori che scrivono i propri filtri personalizzati:

-   [Flusso di dati per sviluppatori di filtri](data-flow-for-filter-developers.md)
-   [Thread e sezioni critiche](threads-and-critical-sections.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Il grafico del filtro e i relativi componenti](the-filter-graph-and-its-components.md)
</dt> </dl>

 

 



