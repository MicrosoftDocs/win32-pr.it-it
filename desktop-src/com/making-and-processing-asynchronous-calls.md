---
title: Creazione ed elaborazione di chiamate asincrone
description: Gli oggetti COM possono supportare la chiamata asincrona.
ms.assetid: bf7f9f8e-66ce-41a4-854c-62dbe840a89e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 059f55cc64a70f130e7fb654426803edbe8b7209
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "106300526"
---
# <a name="making-and-processing-asynchronous-calls"></a>Creazione ed elaborazione di chiamate asincrone

Gli oggetti COM possono supportare la chiamata asincrona. Quando un client effettua una chiamata asincrona, il controllo torna immediatamente al client. Mentre il server elabora la chiamata, il client è libero di eseguire altre operazioni. Quando il client non può più procedere senza i risultati della chiamata, può ottenere i risultati della chiamata in quel momento.

Ad esempio, una richiesta di un recordset di grandi dimensioni o complessi può richiedere molto tempo. Un client può richiedere il recordset mediante una chiamata asincrona e quindi eseguire altre operazioni. Quando il recordset è disponibile, il client può ottenerlo rapidamente senza bloccarsi.

I client non eseguono chiamate asincrone direttamente nell'oggetto server. Ottengono invece un oggetto chiamata che implementa una versione asincrona di un'interfaccia sincrona nell'oggetto server. L'interfaccia asincrona nell'oggetto chiamata ha un nome con formato asincrono *intervisore*. Se, ad esempio, un oggetto server implementa un'interfaccia sincrona denominata IMyInterface, sarà presente un oggetto chiamata che implementa un'interfaccia asincrona denominata AsyncIMyInterface.

> [!Note]  
> Il supporto asincrono non è disponibile per **IDispatch** o per le interfacce che ereditano **IDispatch**.

 

Gli oggetti server che supportano le chiamate asincrone implementano l'interfaccia [**ICallFactory**](/windows/win32/api/objidlbase/nn-objidlbase-icallfactory) . Questa interfaccia espone un solo metodo, [**CreateCall**](/windows/win32/api/objidlbase/nf-objidlbase-icallfactory-createcall), che crea un'istanza di un oggetto chiamata specificato. I client possono eseguire query per **ICallFactory** per determinare se un oggetto supporta la chiamata asincrona.

Per ogni metodo su un'interfaccia sincrona, l'interfaccia asincrona corrispondente implementa due metodi. Questi metodi alleghino i prefissi iniziano \_ e terminano \_ con il nome del metodo sincrono. Se, ad esempio, un'interfaccia denominata ISimpleStream dispone di un metodo Read, l'interfaccia AsyncISimpleStream disporrà di un \_ metodo Begin Read e Finish \_ Read. Per iniziare una chiamata asincrona, il client chiama il \_ metodo Begin.

Quando si implementa un oggetto server, non è necessario fornire un oggetto chiamata per ogni interfaccia implementata dall'oggetto. Se l'oggetto server implementa l'interfaccia [**ICallFactory**](/windows/win32/api/objidlbase/nn-objidlbase-icallfactory) e utilizza il marshalling standard, un client sottoposto a marshalling può sempre ottenere un oggetto chiamata proxy, anche se non è presente alcun oggetto chiamata sul lato server. Questo proxy effettuerà il marshalling del \_ metodo Begin come chiamata sincrona, il server elaborerà la chiamata in modo sincrono e il client potrà ottenere i parametri out chiamando il \_ Metodo Finish.

Viceversa, se un client esegue una chiamata sincrona con marshalling su un'interfaccia per la quale è presente un oggetto chiamata sul lato server, il server elaborerà sempre la chiamata in modo asincrono. Questo comportamento non sarà visibile al client, perché il client riceverà gli stessi parametri out e lo stesso valore restituito che avrebbe ricevuto dal metodo sincrono.

In entrambi i casi, l'interazione tra client e server viene sottoposta a marshalling come se la chiamata fosse sincrona: l'output dei proxy sincroni e asincroni non è distinguibile, così come l'output degli stub corrispondenti. Questo comportamento semplifica notevolmente il modello di programmazione di client e server. Se un oggetto server implementa [**ICallFactory**](/windows/win32/api/objidlbase/nn-objidlbase-icallfactory), un client sottoposto a marshalling non deve tentare di creare un oggetto chiamata che potrebbe non essere disponibile: per il client, un oggetto chiamata è sempre disponibile.

Quando il client e il server si trovano nello stesso Apartment, l'oggetto server elaborerà qualsiasi chiamata effettuata dal client. Se un oggetto chiamata non è disponibile, il client deve ottenere in modo esplicito l'interfaccia sincrona ed effettuare una chiamata sincrona.

Per altre informazioni, vedere i seguenti argomenti:

-   [Esecuzione di una chiamata asincrona](making-an-asynchronous-call.md)
-   [Annullamento di una chiamata asincrona](canceling-an-asynchronous-call.md)
-   [Annullamento di chiamate al metodo](canceling-method-calls.md)
-   [Sincronizzazione delle chiamate](call-synchronization.md)

 

 