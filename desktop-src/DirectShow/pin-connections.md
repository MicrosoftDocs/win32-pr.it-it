---
description: Connessioni pin
ms.assetid: 1406ade4-77d8-49a7-8f36-cc49ff007a26
title: Connessioni pin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b509abddf4a915b65dfd322f76b4afb132a7f835
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104401152"
---
# <a name="pin-connections"></a>Connessioni pin

I filtri si connettono ai propri PIN tramite l'interfaccia [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin) . Pin di output si connettono ai pin di input. Ogni connessione pin ha un tipo di supporto, descritto dalla struttura del [**\_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .

Un'applicazione connette i filtri chiamando metodi sul gestore del grafo del filtro, mai chiamando metodi sui filtri o sui pin stessi. L'applicazione può specificare direttamente i filtri da connettere, chiamando il metodo [**IFilterGraph:: ConnectDirect**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-connectdirect) o [**IGraphBuilder:: Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) ; in alternativa, è possibile connettere i filtri indirettamente, usando un metodo di compilazione del grafico, ad esempio [**IGraphBuilder:: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile).

Affinché la connessione abbia esito positivo, è necessario che entrambi i filtri si trovino nel grafico dei filtri. L'applicazione può aggiungere un filtro al grafo chiamando il metodo [**IFilterGraph:: AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) . Filter Graph Manager può anche aggiungere filtri al grafo. Quando viene aggiunto un filtro, il gestore del grafico dei filtri chiama il metodo [**IBaseFilter:: JoinFilterGraph**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) del filtro per notificare il filtro.

Il profilo generale del processo di connessione è il seguente:

1.  Il gestore del grafo dei filtri chiama [**Ipin:: Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) sul pin di output, passando un puntatore al pin di input.
2.  Se il pin di output accetta la connessione, viene chiamato [**Ipin:: ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) sul pin di input.
3.  Se il pin di input accetta anche la connessione, il tentativo di connessione ha esito positivo e i pin sono connessi.

Alcuni pin possono essere disconnessi e riconnessi mentre il filtro è attivo. Questo tipo di riconnessione è definito riconnessione *dinamica* . Per altre informazioni, vedere [creazione di grafici dinamici](dynamic-graph-building.md). Tuttavia, la maggior parte dei filtri non supporta la riconnessione dinamica.

I filtri sono in genere connessi nell'ordine downstream, ovvero i pin di input del filtro sono connessi prima dei pin di output. Un filtro deve sempre supportare questo ordine di connessione. Alcuni filtri supportano anche le connessioni nell'ordine opposto, ovvero i pin di output prima, seguiti dai pin di input. Ad esempio, potrebbe essere possibile connettere il pin di output di un filtro MUX al filtro del writer di file, prima di connettere i pin di input del filtro MUX.

Quando viene chiamato il metodo **Connect** o **ReceiveConnection** di un PIN, il PIN deve verificare che sia in grado di supportare la connessione. I dettagli dipendono dal filtro specifico. Di seguito sono riportate le attività più comuni:

-   Verificare che il tipo di supporto sia accettabile
-   Negoziare un allocatore
-   Eseguire una query sull'altro pin per le interfacce richieste.

 

 



