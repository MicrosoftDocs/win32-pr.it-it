---
title: Esecuzione di una chiamata asincrona
description: "La procedura per eseguire una chiamata sincrona è semplice: il client ottiene un puntatore a interfaccia sull'oggetto server e chiama i metodi tramite tale puntatore. La chiamata asincrona comporta un oggetto di chiamata, quindi richiede alcuni passaggi aggiuntivi."
ms.assetid: ab65d38d-836a-48d4-87c1-8812cbc8ff92
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 384a153b826e570920fca2a92f5b53ed2079c561cbcda899b793cef1f39473bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755991"
---
# <a name="making-an-asynchronous-call"></a>Esecuzione di una chiamata asincrona

La procedura per eseguire una chiamata sincrona è semplice: il client ottiene un puntatore a interfaccia sull'oggetto server e chiama i metodi tramite tale puntatore. La chiamata asincrona comporta un oggetto di chiamata, quindi richiede alcuni passaggi aggiuntivi.

Per ogni metodo in un'interfaccia sincrona, l'interfaccia asincrona corrispondente implementa due metodi. Questi metodi associano i prefissi Begin e \_ Finish al nome del metodo \_ sincrono. Ad esempio, se un'interfaccia denominata ISimpleStream ha un metodo Read, l'interfaccia AsyncISimpleStream avrà un metodo Begin Read e \_ un \_ metodo Finish Read. Per iniziare una chiamata asincrona, il client chiama il metodo \_ Begin.

**Per iniziare una chiamata asincrona**

1.  Eseguire una query sull'oggetto server per [**l'interfaccia ICallFactory.**](/windows/win32/api/objidlbase/nn-objidlbase-icallfactory) Se [**QueryInterface restituisce**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) E \_ NOINTERFACE, l'oggetto server non supporta la chiamata asincrona.

2.  Chiamare [**ICallFactory::CreateCall**](/windows/win32/api/objidlbase/nf-objidlbase-icallfactory-createcall) per creare un oggetto chiamata corrispondente all'interfaccia desiderata e quindi rilasciare il puntatore a [**ICallFactory**](/windows/win32/api/objidlbase/nn-objidlbase-icallfactory).

3.  Se non è stato richiesto un puntatore all'interfaccia asincrona dalla chiamata a [**CreateCall**](/windows/win32/api/objidlbase/nf-objidlbase-icallfactory-createcall), eseguire una query sull'oggetto chiamata per l'interfaccia asincrona.

4.  Chiamare il metodo Begin \_ appropriato.

L'oggetto server sta ora elaborando la chiamata asincrona e il client è libero di eseguire altre operazioni finché non richiede i risultati della chiamata.

Un oggetto chiamata può elaborare una sola chiamata asincrona alla volta. Se lo stesso client o un secondo client chiama un metodo Begin prima del completamento di una chiamata asincrona in sospeso, il \_ metodo Begin \_ restituirà RPC E CALL \_ \_ \_ PENDING.

Se il client non richiede i risultati del metodo Begin, può rilasciare l'oggetto chiamata \_ alla fine di questa procedura. COM rileva questa condizione e pulisce la chiamata. Il metodo \_ Finish non viene chiamato e il client non ottiene parametri out o un valore restituito.

Quando l'oggetto server è pronto per la restituzione dal metodo Begin, segnala all'oggetto di chiamata \_ che l'operazione è stata eseguita. Quando il client è pronto, verifica se l'oggetto chiamata è stato segnalato. In tal caso, il client può completare la chiamata asincrona.

Il meccanismo per la segnalazione e il controllo tra client e server è [**l'interfaccia ISynchronize**](/windows/win32/api/objidlbase/nn-objidlbase-isynchronize) nell'oggetto chiamata. L'oggetto chiamata implementa in genere questa interfaccia aggregando un oggetto di sincronizzazione fornito dal sistema. L'oggetto di sincronizzazione esegue il wrapping di un handle di evento segnalato dal server poco prima della restituzione dal metodo Begin chiamando \_ [**ISynchronize::Signal**](/windows/win32/api/objidlbase/nf-objidlbase-isynchronize-signal).

**Per completare una chiamata asincrona**

1.  Eseguire una query sull'oggetto chiamata per [**l'interfaccia ISynchronize.**](/windows/win32/api/objidlbase/nn-objidlbase-isynchronize)

2.  Chiamare [**ISynchronize::Wait**](/windows/win32/api/objidlbase/nf-objidlbase-isynchronize-wait).

3.  Se [**Wait**](/windows/win32/api/objidlbase/nf-objidlbase-isynchronize-wait) restituisce RPC \_ E \_ TIMEOUT, l'elaborazione del metodo Begin \_ non è stata completata. Il client può continuare con altre operazioni e chiamare **di nuovo Wait** in un secondo momento. Non può chiamare il metodo Finish \_ finché Wait non **restituisce** S \_ OK.

    Se [**Wait restituisce**](/windows/win32/api/objidlbase/nf-objidlbase-isynchronize-wait) S \_ OK, viene \_ restituito il metodo Begin. Chiamare il metodo Finish \_ appropriato.

Il metodo Finish \_ passa al client tutti i parametri out. Il comportamento dei metodi asincroni, incluso il valore restituito del metodo Finish, deve corrispondere esattamente a quello \_ del metodo sincrono corrispondente.

Il client può rilasciare l'oggetto chiamata non appena viene restituito il metodo Finish oppure può contenere un puntatore all'oggetto chiamata \_ per effettuare chiamate aggiuntive. In entrambi i casi, il client è responsabile del rilascio dell'oggetto chiamata quando l'oggetto non è più necessario.

Se si chiama un metodo Finish quando non è in corso alcuna chiamata, il \_ metodo restituirà RPC \_ E CALL \_ \_ COMPLETE.

> [!Note]  
> Se gli oggetti client e server sono nello stesso apartment, non è garantito che le chiamate a [**ICallFactory::CreateCall**](/windows/win32/api/objidlbase/nf-objidlbase-icallfactory-createcall) riescano. Se l'oggetto server non supporta la chiamata asincrona su una particolare interfaccia, il tentativo di creare un oggetto chiamata avrà esito negativo e il client deve usare l'interfaccia sincrona.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Annullamento di una chiamata asincrona](canceling-an-asynchronous-call.md)
</dt> <dt>

[Sicurezza client durante una chiamata asincrona](client-security-during-an-asynchronous-call.md)
</dt> <dt>

[Rappresentazione e chiamate asincrone](impersonation-and-asynchronous-calls.md)
</dt> </dl>

 

 