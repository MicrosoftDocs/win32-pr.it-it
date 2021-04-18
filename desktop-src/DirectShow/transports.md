---
description: Trasporti
ms.assetid: 63c5ff5b-293d-4a80-92e8-3ece41321095
title: Trasporti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c3d87ffacc871fc45ef1e8e645849afc956fb1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313402"
---
# <a name="transports"></a>Trasporti

Per spostare i dati multimediali tramite il grafico dei filtri, un filtro DirectShow deve supportare uno dei diversi protocolli possibili. Questi protocolli sono detti trasporti. Quando due filtri si connettono, devono supportare lo stesso trasporto; in caso contrario, non possono scambiare dati multimediali. In genere, un trasporto richiede che uno dei pin supporti una determinata interfaccia. Quando i filtri si connettono, un pin esegue una query sull'altro per l'interfaccia.

La maggior parte dei filtri DirectShow consente di mantenere i dati multimediali nella memoria principale e di distribuirla ad altri filtri tra connessioni pin. Questo tipo di trasporto è denominato trasporto di memoria locale. Sebbene il trasporto di memoria locale sia il trasporto più comune in DirectShow, non tutti i filtri lo usano. Ad esempio, alcuni filtri inviano i dati multimediali lungo un percorso hardware e usano solo pin per fornire informazioni sul controllo. Vedere ad esempio l'interfaccia [**iOverlay**](/windows/desktop/api/Strmif/nn-strmif-ioverlay) .

DirectShow definisce due meccanismi per il trasporto di memoria locale, il modello push e il modello pull. Nel modello push un filtro di origine genera dati e li recapita al filtro successivo downstream. Tale filtro riceve i dati in modo passivo, li elabora e li invia a valle. Nel modello pull il filtro di origine è connesso a un filtro del parser. Il filtro del parser richiede i dati dal filtro di origine. Il filtro di origine risponde alle richieste tramite la distribuzione dei dati. Il modello push usa l'interfaccia [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) e il modello pull usa l'interfaccia [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) .

Il modello push è più comune del modello pull. Gli articoli che seguono presuppongono quindi un modello push. Nell'ultimo articolo di questa sezione, [modello pull](pull-model.md), viene descritto il modo in cui l'interfaccia **IAsyncReader** differisce da **IMemInputPin**.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Flusso di dati nel grafico del filtro](data-flow-in-the-filter-graph.md)
</dt> </dl>

 

 



