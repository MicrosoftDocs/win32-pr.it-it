---
title: Esecuzione ed elaborazione di chiamate asincrone
description: Gli oggetti COM possono supportare la chiamata asincrona.
ms.assetid: bf7f9f8e-66ce-41a4-854c-62dbe840a89e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 173f33ea3a0d4ec59f994eeff259e776efa58ae5b0182ba97f77e1ba99dd0d82
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130203"
---
# <a name="making-and-processing-asynchronous-calls"></a>Esecuzione ed elaborazione di chiamate asincrone

Gli oggetti COM possono supportare la chiamata asincrona. Quando un client effettua una chiamata asincrona, il controllo torna immediatamente al client. Mentre il server elabora la chiamata, il client è libero di eseguire altre operazioni. Quando il client non può più continuare senza i risultati della chiamata, può ottenere i risultati della chiamata in quel momento.

Ad esempio, una richiesta per un recordset complesso o di grandi dimensioni può richiedere molto tempo. Un client può richiedere il recordset tramite una chiamata asincrona e quindi eseguire altre operazioni. Quando il recordset è disponibile, il client può ottenerlo rapidamente senza bloccarsi.

I client non effettuano chiamate asincrone direttamente sull'oggetto server. Ottengono invece un oggetto chiamata che implementa una versione asincrona di un'interfaccia sincrona nell'oggetto server. L'interfaccia asincrona nell'oggetto chiamata ha un nome nel formato Async *InterfaceName*. Ad esempio, se un oggetto server implementa un'interfaccia sincrona denominata IMyInterface, sarà presente un oggetto chiamata che implementa un'interfaccia asincrona denominata AsyncIMyInterface.

> [!Note]  
> Il supporto asincrono non è disponibile **per IDispatch** o per le interfacce che **ereditano IDispatch.**

 

Gli oggetti server che supportano le chiamate asincrone implementano [**l'interfaccia ICallFactory.**](/windows/win32/api/objidlbase/nn-objidlbase-icallfactory) Questa interfaccia espone un singolo metodo, [**CreateCall,**](/windows/win32/api/objidlbase/nf-objidlbase-icallfactory-createcall)che crea un'istanza di un oggetto chiamata specificato. I client possono eseguire una query **per ICallFactory** per determinare se un oggetto supporta la chiamata asincrona.

Per ogni metodo in un'interfaccia sincrona, l'interfaccia asincrona corrispondente implementa due metodi. Questi metodi collegano i prefissi Begin e \_ Finish al nome del metodo \_ sincrono. Ad esempio, se un'interfaccia denominata ISimpleStream ha un metodo Read, l'interfaccia AsyncISimpleStream avrà un metodo Begin Read e \_ un metodo \_ Finish Read. Per iniziare una chiamata asincrona, il client chiama il metodo \_ Begin.

Quando si implementa un oggetto server, non è necessario fornire un oggetto di chiamata per ogni interfaccia implementata dall'oggetto. Se l'oggetto server implementa [**l'interfaccia ICallFactory**](/windows/win32/api/objidlbase/nn-objidlbase-icallfactory) e usa il marshalling standard, un client sottoposto a marshalling può sempre ottenere un oggetto chiamata proxy, anche se sul lato server non è presente alcun oggetto chiamata. Questo proxy effettua il marshalling del metodo Begin come chiamata sincrona, il server eelaborare la chiamata in modo sincrono e il client può ottenere i parametri out chiamando il \_ metodo \_ Finish.

Viceversa, se un client effettua una chiamata sincrona con marshalling su un'interfaccia per la quale è presente un oggetto chiamata sul lato server, il server elaverà sempre la chiamata in modo asincrono. Questo comportamento non sarà evidente per il client, perché il client riceverà gli stessi parametri out e lo stesso valore restituito che avrebbe ricevuto dal metodo sincrono.

In entrambi i casi, viene effettuato il marshalling dell'interazione tra client e server come se la chiamata fosse sincrona: l'output dei proxy sincroni e asincroni non è distinguibile, così come l'output degli stub corrispondenti. Questo comportamento semplifica notevolmente il modello di programmazione dei client e dei server. Se un oggetto server implementa [**ICallFactory,**](/windows/win32/api/objidlbase/nn-objidlbase-icallfactory)non è necessario che un client con marshalling tenti di creare un oggetto chiamata che potrebbe non essere disponibile. Per il client, un oggetto chiamata è sempre disponibile.

Quando il client e il server sono nello stesso apartment, l'oggetto server eelaborare qualsiasi chiamata del client. Se non è disponibile un oggetto chiamata, il client deve ottenere in modo esplicito l'interfaccia sincrona ed effettuare una chiamata sincrona.

Per altre informazioni, vedere i seguenti argomenti:

-   [Esecuzione di una chiamata asincrona](making-an-asynchronous-call.md)
-   [Annullamento di una chiamata asincrona](canceling-an-asynchronous-call.md)
-   [Annullamento di chiamate al metodo](canceling-method-calls.md)
-   [Sincronizzazione delle chiamate](call-synchronization.md)

 

 