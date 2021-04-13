---
title: Esecuzione di una chiamata asincrona
description: La procedura per eseguire una chiamata sincrona è semplice, il client ottiene un puntatore a interfaccia sull'oggetto server e chiama i metodi tramite tale puntatore. La chiamata asincrona comporta un oggetto chiamata, quindi comporta alcuni passaggi.
ms.assetid: ab65d38d-836a-48d4-87c1-8812cbc8ff92
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22dcd7a6509cd07e12357a96222baa04f9e4c942
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104399791"
---
# <a name="making-an-asynchronous-call"></a>Esecuzione di una chiamata asincrona

La procedura per eseguire una chiamata sincrona è semplice: il client ottiene un puntatore a interfaccia sull'oggetto server e chiama i metodi tramite tale puntatore. La chiamata asincrona comporta un oggetto chiamata, quindi comporta alcuni passaggi.

Per ogni metodo su un'interfaccia sincrona, l'interfaccia asincrona corrispondente implementa due metodi. Questi metodi alleghino i prefissi iniziano \_ e terminano \_ con il nome del metodo sincrono. Se, ad esempio, un'interfaccia denominata ISimpleStream dispone di un metodo Read, l'interfaccia AsyncISimpleStream disporrà di un \_ metodo Begin Read e Finish \_ Read. Per iniziare una chiamata asincrona, il client chiama il \_ metodo Begin.

**Per iniziare una chiamata asincrona**

1.  Eseguire una query sull'oggetto server per l'interfaccia [**ICallFactory**](/windows/win32/api/objidlbase/nn-objidlbase-icallfactory) . Se [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) restituisce E \_ nointerface, l'oggetto server non supporta la chiamata asincrona.

2.  Chiamare [**ICallFactory:: CreateCall**](/windows/win32/api/objidlbase/nf-objidlbase-icallfactory-createcall) per creare un oggetto chiamata corrispondente all'interfaccia desiderata, quindi rilasciare il puntatore a [**ICallFactory**](/windows/win32/api/objidlbase/nn-objidlbase-icallfactory).

3.  Se non è stato richiesto un puntatore all'interfaccia asincrona dalla chiamata a [**CreateCall**](/windows/win32/api/objidlbase/nf-objidlbase-icallfactory-createcall), eseguire una query sull'oggetto chiamata per l'interfaccia asincrona.

4.  Chiamare il metodo Begin appropriato \_ .

L'oggetto server sta ora elaborando la chiamata asincrona e il client è libero di eseguire altre operazioni fino a quando non sono necessari i risultati della chiamata.

Un oggetto call può elaborare una sola chiamata asincrona alla volta. Se lo stesso o un secondo client chiama un \_ metodo Begin prima del completamento di una chiamata asincrona in sospeso, il \_ metodo Begin restituirà la \_ chiamata RPC E \_ \_ in sospeso.

Se il client non richiede i risultati del \_ metodo Begin, può rilasciare l'oggetto call alla fine di questa procedura. COM rileva questa condizione e pulisce la chiamata. Il \_ Metodo Finish non viene chiamato e il client non ottiene alcun parametro out o un valore restituito.

Quando l'oggetto server è pronto per essere restituito dal \_ metodo Begin, segnala l'oggetto chiamata che è stato eseguito. Quando il client è pronto, verifica se l'oggetto chiamata è stato segnalato. In tal caso, il client può completare la chiamata asincrona.

Il meccanismo per la segnalazione e il controllo tra client e server è l'interfaccia [**ISynchronize**](/windows/win32/api/objidlbase/nn-objidlbase-isynchronize) nell'oggetto call. L'oggetto call normalmente implementa questa interfaccia aggregando un oggetto di sincronizzazione fornito dal sistema. L'oggetto di sincronizzazione esegue il wrapping di un handle di evento, che il server segnala immediatamente prima \_ di restituire il metodo Begin chiamando [**ISynchronize:: Signal**](/windows/win32/api/objidlbase/nf-objidlbase-isynchronize-signal).

**Per completare una chiamata asincrona**

1.  Eseguire una query sull'oggetto chiamata per l'interfaccia [**ISynchronize**](/windows/win32/api/objidlbase/nn-objidlbase-isynchronize) .

2.  Chiamare [**ISynchronize:: wait**](/windows/win32/api/objidlbase/nf-objidlbase-isynchronize-wait).

3.  Se [**wait**](/windows/win32/api/objidlbase/nf-objidlbase-isynchronize-wait) restituisce \_ \_ il timeout RPC e, l' \_ elaborazione del metodo Begin non è terminata. Il client può continuare con altre attività e chiamare di nuovo **Attendi** in un secondo momento. Non può chiamare il \_ Metodo Finish finché **wait** restituisce S \_ OK.

    Se [**wait**](/windows/win32/api/objidlbase/nf-objidlbase-isynchronize-wait) restituisce S \_ OK, \_ viene restituito il metodo Begin. Chiamare il metodo Finish appropriato \_ .

Il \_ Metodo Finish passa al client tutti i parametri out. Il comportamento dei metodi asincroni, incluso il valore restituito del \_ Metodo Finish, deve corrispondere esattamente a quello del metodo sincrono corrispondente.

Il client può rilasciare l'oggetto chiamata non appena il metodo Finish \_ restituisce oppure un puntatore all'oggetto call per effettuare chiamate aggiuntive. In entrambi i casi, il client è responsabile del rilascio dell'oggetto chiamata quando l'oggetto non è più necessario.

Se si chiama un \_ Metodo Finish quando non è in corso alcuna chiamata, il metodo restituirà la \_ chiamata RPC E \_ \_ complete.

> [!Note]  
> Se gli oggetti client e server si trovano nello stesso Apartment, non è garantito che le chiamate a [**ICallFactory:: CreateCall**](/windows/win32/api/objidlbase/nf-objidlbase-icallfactory-createcall) abbiano esito positivo. Se l'oggetto server non supporta la chiamata asincrona su una particolare interfaccia, il tentativo di creare un oggetto chiamata avrà esito negativo e il client deve utilizzare l'interfaccia sincrona.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Annullamento di una chiamata asincrona](canceling-an-asynchronous-call.md)
</dt> <dt>

[Sicurezza del client durante una chiamata asincrona](client-security-during-an-asynchronous-call.md)
</dt> <dt>

[Rappresentazione e chiamate asincrone](impersonation-and-asynchronous-calls.md)
</dt> </dl>

 

 