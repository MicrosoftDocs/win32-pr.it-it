---
description: Aggiungere connessioni
ms.assetid: 1406ade4-77d8-49a7-8f36-cc49ff007a26
title: Aggiungere connessioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cfcd407e785e15f4243f3113a63569f8b4b84de517cdde0f63a88eaef79f85c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119432291"
---
# <a name="pin-connections"></a>Aggiungere connessioni

I filtri si connettono ai relativi pin tramite [**l'interfaccia IPin.**](/windows/desktop/api/Strmif/nn-strmif-ipin) I pin di output si connettono ai pin di input. Ogni connessione pin ha un tipo di supporto, descritto dalla [**struttura AM \_ MEDIA \_ TYPE.**](/windows/win32/api/strmif/ns-strmif-am_media_type)

Un'applicazione connette i filtri chiamando metodi in Filter Graph Manager, mai chiamando metodi sui filtri o sui pin stessi. L'applicazione può specificare direttamente i filtri da connettere chiamando il metodo [**IFilterGraph::ConnectDirect**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-connectdirect) [**o IGraphBuilder::Connessione;**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) oppure può connettere i filtri in modo indiretto usando un metodo di creazione di grafi, ad esempio [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile).

Per l'esito positivo della connessione, entrambi i filtri devono essere presenti nel grafico dei filtri. L'applicazione può aggiungere un filtro al grafico chiamando il [**metodo IFilterGraph::AddFilter.**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) Filter Graph Manager può anche aggiungere filtri al grafico. Quando viene aggiunto un filtro, Filter Graph Manager chiama il metodo [**IBaseFilter::JoinFilterGraph**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) del filtro per inviare una notifica al filtro.

La struttura generale del processo di connessione è la seguente:

1.  Filter Graph Manager chiama [**IPin::Connessione**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) sul pin di output, passando un puntatore al pin di input.
2.  Se il pin di output accetta la connessione, chiama [**IPin::ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) sul pin di input.
3.  Se anche il pin di input accetta la connessione, il tentativo di connessione ha esito positivo e i pin sono connessi.

Alcuni pin possono essere disconnessi e riconnessi mentre il filtro è attivo. Questo tipo di riconnessione è detto *riconnessione* dinamica. Per altre informazioni, vedere [Dynamic Graph Building](dynamic-graph-building.md). Tuttavia, la maggior parte dei filtri non supporta la riconnessione dinamica.

I filtri sono in genere connessi in ordine downstream. In altre parole, i pin di input del filtro vengono connessi prima dei pin di output. Un filtro deve sempre supportare questo ordine di connessione. Alcuni filtri supportano anche le connessioni nell'ordine opposto: prima i pin di output, seguiti dai pin di input. Ad esempio, potrebbe essere possibile connettere il pin di output di un filtro MUX al filtro di scrittura file, prima di connettere i pin di input del filtro MUX.

Quando viene chiamato il **metodo Connessione** **o ReceiveConnection** di un pin, il pin deve verificare che sia in grado di supportare la connessione. I dettagli dipendono dal filtro specifico. Di seguito sono riportate le attività più comuni:

-   Verificare che il tipo di supporto sia accettabile
-   Negoziare un allocatore
-   Eseguire una query sull'altro pin per individuare le interfacce necessarie.

 

 



