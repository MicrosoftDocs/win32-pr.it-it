---
title: Annullamento di chiamate al metodo
description: Con l'introduzione di applicazioni distribuite e basate sul Web, la restituzione di alcune chiamate al metodo può richiedere un tempo inaccettabile.
ms.assetid: 18228ff1-8c1c-430a-ae5f-0e9a56b0fe3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59ea089f257527dfd31d7120170c8749a2d1b4d60ba006843c7ff5d43403b352
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118311085"
---
# <a name="canceling-method-calls"></a>Annullamento di chiamate al metodo

Con l'introduzione di applicazioni distribuite e basate sul Web, la restituzione di alcune chiamate al metodo può richiedere un tempo inaccettabile. La latenza della connessione di rete può essere elevata, il computer server potrebbe servire molti client o il componente server potrebbe passare una grande quantità di dati, ad esempio un file multimediale. Gli utenti devono essere in grado di annullare una richiesta che richiede troppo tempo e l'applicazione deve essere in grado di gestire le richieste di annullamento e continuare con le altre operazioni. In COM è possibile usare [**l'interfaccia IMessageFilter**](/windows/desktop/api/ObjIdl/nn-objidl-imessagefilter) per annullare una chiamata in sospeso proveniente da un apartment a thread singolo.

Quando viene effettuato il marshalling di una chiamata, il proxy crea un oggetto cancel, che implementa [**l'interfaccia ICancelMethodCalls.**](/windows/win32/api/objidlbase/nn-objidlbase-icancelmethodcalls) L'oggetto cancel è associato sia alla chiamata che al thread in cui la chiamata è in sospeso.

Per annullare la chiamata in sospeso, il client passa una richiesta di annullamento tramite l'oggetto cancel, che gestisce i dettagli della notifica all'oggetto server che la chiamata è stata annullata. Se il metodo chiamato non è stato restituito, l'oggetto server, al rilevamento della richiesta di annullamento, pulisce tutte le risorse di programma allocate e notifica al client, tramite la restituzione di un valore **HRESULT** appropriato, che ha annullato l'esecuzione della chiamata. Se il metodo chiamato è già stato restituito, l'oggetto cancel invia una notifica al client. In entrambi i casi, il thread client è sbloccato e può continuare l'elaborazione.

Il modo in cui l'oggetto server risponde a una richiesta di annullamento è a discrezione dell'implementatore del server, ma il thread chiamante nel client verrà sempre sbloccato e ignorerà i risultati che il server tenta di passare. Gli oggetti Cancel consentono di richiedere l'annullamento di un metodo attualmente in esecuzione, ma non è garantito che l'oggetto server interrompi l'elaborazione della chiamata. Ad esempio, è possibile che la chiamata sia già stata restituita o che l'oggetto server non supporti gli oggetti cancel.

COM fornisce automaticamente un'implementazione standard di oggetti cancel per oggetti client e interfacce che utilizzano il marshalling standard. Per gli oggetti e le interfacce che usano il marshalling personalizzato, è necessario implementare un oggetto cancel personalizzato.

Al momento, gli oggetti cancel gestiscono solo chiamate sincrone.

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

 

 