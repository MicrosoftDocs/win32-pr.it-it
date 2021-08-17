---
description: Informazioni sugli allocatori e sugli esempi di supporti
ms.assetid: d6283bf0-0460-4519-9a56-fd4c78cfaabc
title: Informazioni sugli allocatori e sugli esempi di supporti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e9390bd99ab019effa40f9edca1f8d9e03ea73c5b0085ed8b1bc13f013cad6a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119430281"
---
# <a name="about-media-samples-and-allocators"></a>Informazioni sugli allocatori e sugli esempi di supporti

I filtri recapitare i dati tra le connessioni pin. I dati vengono spostati dal pin di output di un filtro al pin di input di un altro filtro. Il modo più comune per il pin di output per recapitare i dati è chiamare il metodo [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) sull'input, anche se esistono anche altri meccanismi.

A seconda del filtro, la memoria per i dati multimediali può essere allocata in diversi modi: nell'heap, in una superficie DirectDraw, usando la memoria GDI condivisa o usando un altro meccanismo di allocazione. L'oggetto responsabile dell'allocazione della memoria è detto *allocatore*, ovvero un oggetto COM che espone [**l'interfaccia IMemAllocator.**](/windows/desktop/api/Strmif/nn-strmif-imemallocator)

Quando si connettono due pin, uno dei pin deve fornire un allocatore. DirectShow definisce una sequenza di chiamate al metodo usata per stabilire quale pin fornisce l'allocatore. I pin concordano anche sul numero di buffer che l'allocatore creerà e sulle dimensioni dei buffer.

Prima dell'inizio dello streaming, l'allocatore crea un pool di buffer. Durante lo streaming, il filtro upstream riempie i buffer con dati e li recapita al filtro downstream. Il filtro upstream, tuttavia, non assegna puntatori non elaborati del filtro downstream ai buffer. Usa invece oggetti COM denominati *esempi multimediali,* creati dall'allocatore per gestire i buffer. Gli esempi multimediali espongono [**l'interfaccia IMediaSample.**](/windows/desktop/api/Strmif/nn-strmif-imediasample) Un esempio di supporto contiene:

-   puntatore al buffer sottostante
-   un timestamp
-   vari flag
-   facoltativamente, un tipo di supporto

Il timestamp definisce l'ora di presentazione, utilizzata dal filtro del renderer per pianificare il rendering. I flag indicano ad esempio se si è verificata un'interruzione nei dati rispetto all'esempio precedente. Il tipo di supporto consente ai filtri di modificare i formati nel flusso intermedio. In genere, l'esempio non ha alcun tipo di supporto, che indica che il formato non è stato modificato rispetto all'esempio precedente.

Mentre un filtro usa un buffer, contiene il conteggio dei riferimenti nell'esempio. L'allocatore usa il conteggio dei riferimenti per determinare quando può usare nuovamente il buffer. In questo modo si impedisce a un filtro di sovrascrivere un buffer ancora in uso da un altro filtro. Un esempio non torna al pool di campioni disponibili dell'allocatore finché non viene rilasciato da ogni filtro.

Per altre informazioni, vedere i seguenti argomenti:

-   [L'argomento Esempi e allocatori](samples-and-allocators.md) fornisce una descrizione più dettagliata del funzionamento degli allocatori.
-   [L'argomento Flow dati nel filtro Graph](data-flow-in-the-filter-graph.md) offre una panoramica generale del flusso di dati in DirectShow.

Gli argomenti seguenti sono destinati agli sviluppatori che scrivono filtri personalizzati:

-   [Dati Flow per sviluppatori di filtri](data-flow-for-filter-developers.md)
-   [Thread e sezioni critiche](threads-and-critical-sections.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Il filtro Graph e i relativi componenti](the-filter-graph-and-its-components.md)
</dt> </dl>

 

 



