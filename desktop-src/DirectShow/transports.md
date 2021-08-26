---
description: Trasporti
ms.assetid: 63c5ff5b-293d-4a80-92e8-3ece41321095
title: Trasporti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cb55542e87939168d1d95350fd71081833e4263f342a3e67c00a7c6814d51e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903721"
---
# <a name="transports"></a>Trasporti

Per spostare i dati multimediali tramite il grafico dei filtri, un filtro DirectShow deve supportare uno dei diversi protocolli possibili. Questi protocolli sono detti trasporti. Quando due filtri si connettono, devono supportare lo stesso trasporto. in caso contrario, non possono scambiare dati multimediali. In genere, un trasporto richiede che uno dei pin supporti un'interfaccia specifica. Quando i filtri si connettono, un pin esegue una query sull'altro pin per l'interfaccia.

La maggior DirectShow i filtri contengono i dati multimediali nella memoria principale e vengono recapitati ad altri filtri tra le connessioni pin. Questo tipo di trasporto è denominato trasporto di memoria locale. Anche se il trasporto della memoria locale è il trasporto più comune in DirectShow, non tutti i filtri lo usano. Ad esempio, alcuni filtri inviano dati multimediali lungo un percorso hardware e usano i pin solo per fornire informazioni di controllo. Vedere ad esempio [**l'interfaccia IOverlay.**](/windows/desktop/api/Strmif/nn-strmif-ioverlay)

DirectShow definisce due meccanismi per il trasporto della memoria locale, il modello push e il modello pull. Nel modello push un filtro di origine genera i dati e lo recapita al filtro downstream successivo. Questo filtro riceve passivamente i dati, li elabora e li invia a valle. Nel modello pull il filtro di origine è connesso a un filtro del parser. Il filtro del parser richiede dati dal filtro di origine. Il filtro di origine risponde alle richieste recapitare i dati. Il modello push usa [**l'interfaccia IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) e il modello pull usa [**l'interfaccia IAsyncReader.**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader)

Il modello push è più comune del modello pull. Pertanto, gli articoli che seguono presuppongono un modello push. L'ultimo articolo di questa sezione, [Modello pull,](pull-model.md)descrive le differenze tra l'interfaccia **IAsyncReader** e **IMemInputPin.**

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Dati Flow nel filtro Graph](data-flow-in-the-filter-graph.md)
</dt> </dl>

 

 



