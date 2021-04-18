---
title: Annullamento di chiamate al metodo
description: Con l'introduzione di applicazioni distribuite e basate sul Web, alcune chiamate al metodo possono richiedere un tempo inaccettabile per la restituzione.
ms.assetid: 18228ff1-8c1c-430a-ae5f-0e9a56b0fe3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2e2a78f042e528036135df4865e8a454cd687da
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "106300520"
---
# <a name="canceling-method-calls"></a>Annullamento di chiamate al metodo

Con l'introduzione di applicazioni distribuite e basate sul Web, alcune chiamate al metodo possono richiedere un tempo inaccettabile per la restituzione. La latenza della connessione di rete potrebbe essere elevata, il computer server potrebbe servire molti client o il componente server può passare una grande quantità di dati, ad esempio un file multimediale. Gli utenti devono essere in grado di annullare una richiesta che sta richiedendo troppo tempo e l'applicazione deve essere in grado di gestire le richieste di annullamento e continuare con le altre attività. In COM, è possibile usare l'interfaccia [**IMessageFilter**](/windows/desktop/api/ObjIdl/nn-objidl-imessagefilter) per annullare una chiamata in sospeso originata da un Apartment a thread singolo.

Quando viene effettuato il marshalling di una chiamata, il proxy crea un oggetto Cancel, che implementa l'interfaccia [**ICancelMethodCalls**](/windows/win32/api/objidlbase/nn-objidlbase-icancelmethodcalls) . L'oggetto Cancel è associato sia alla chiamata che al thread in cui la chiamata è in sospeso.

Per annullare la chiamata in sospeso, il client passa una richiesta di annullamento tramite l'oggetto Cancel, che gestisce i dettagli della notifica all'oggetto server che la chiamata è stata annullata. Se il metodo chiamato non ha restituito, l'oggetto server, durante il rilevamento della richiesta di annullamento, pulisce tutte le risorse del programma che ha allocato e invia una notifica al client, restituendo un valore **HRESULT** appropriato, che ha annullato l'esecuzione della chiamata. Se il metodo chiamato è già stato restituito, l'oggetto Cancel invia una notifica al client. In entrambi i casi, il thread client viene sbloccato e può continuare l'elaborazione.

Il modo in cui l'oggetto server risponde a una richiesta di annullamento è a discrezione dell'implementatore del server, ma il thread chiamante sul client sarà sempre sbloccato e ignorerà i risultati che il server tenterà di passare. Gli oggetti Cancel forniscono un mezzo per richiedere che un metodo attualmente in esecuzione venga annullato, ma non vi è alcuna garanzia che l'oggetto server arresterà l'elaborazione della chiamata. Ad esempio, è possibile che la chiamata sia già stata restituita oppure che l'oggetto server non supporti l'annullamento degli oggetti.

COM fornisce automaticamente un'implementazione standard degli oggetti Cancel per gli oggetti e le interfacce client che utilizzano il marshalling standard. Per gli oggetti e le interfacce che usano il marshalling personalizzato, sarà necessario implementare un oggetto Cancel personalizzato.

Al momento, gli oggetti Cancel gestiscono solo le chiamate sincrone.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Annullamento di una chiamata asincrona](canceling-an-asynchronous-call.md)
</dt> <dt>

[**CoGetCancelObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcancelobject)
</dt> <dt>

[**CoSetCancelObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetcancelobject)
</dt> <dt>

[**CoTestCancel**](/windows/desktop/api/combaseapi/nf-combaseapi-cotestcancel)
</dt> </dl>

 

 