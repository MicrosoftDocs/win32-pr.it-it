---
title: Gestione degli errori (RPC)
description: In RPC sincrono, un client esegue una chiamata remota che restituisce un codice di esito positivo o negativo.
ms.assetid: 7dfc9f84-ce3c-49f3-8f72-b212095133fd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 017892b94438cc73f88cbfe60c03c088bf3ebcc9
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104047768"
---
# <a name="error-handling-rpc"></a>Gestione degli errori (RPC)

In RPC sincrono, un client esegue una chiamata remota che restituisce un codice di esito positivo o negativo. Il RPC asincrono offre più possibilità di errore di una chiamata e questi errori vengono gestiti in modo diverso, a seconda di dove e quando si verificano. Nella tabella seguente vengono descritte le modalità con cui una chiamata può avere esito negativo e il modo in cui viene gestita.

## <a name="client-side-cleanup"></a>Pulizia lato client



| Sintomo errore                                                                                                                                  | Pulizia                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Il client rileva un'eccezione quando chiama la procedura remota.                                                                                  | Non sono necessarie chiamate API RPC. È stato eliminato tutto lo stato RPC.                                                              |
| Il client riceve una notifica di completamento chiamata, ma quando chiama [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall), riceve un codice di errore. | Non sono necessarie chiamate API RPC. È stato eliminato tutto lo stato RPC.                                                              |
| Il client genera un annullamento non interrotto o interrotto.                                                                                                   | Il client deve attendere la notifica e chiamare [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) all'arrivo della notifica. |



 

In pulizia lato server, un concetto chiave è il punto di partenza. Durante l'elaborazione lato server di una chiamata asincrona, alcune elaborazioni vengono in genere eseguite sul thread che ha ricevuto la chiamata (noto anche come *thread Dispatcher*) e, facoltativamente, il thread Dispatcher inserisce uno stato sufficiente in un blocco di memoria e segnala a un altro thread (noto anche come *thread di lavoro*) di continuare l'elaborazione per la chiamata. Momento in cui il thread del dispatcher segnala correttamente che il thread di lavoro è denominato *punto di consegna*.

## <a name="server-side-cleanup"></a>Pulizia lato server



| Errore rilevato      | Pulizia                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Prima di passare al punto di partenza. | Genera un'eccezione. Non è necessaria alcuna chiamata a [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) .                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Dopo il punto di consegna.  | Chiamare [**RpcAsyncAbortCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall) o, se l'errore non è irreversibile e i risultati possono comunque essere restituiti al client, [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall). Se la chiamata alla funzione **RpcAsyncCompleteCall** ha esito negativo, il runtime RPC libera i parametri. L'utente non deve accedere a tali parametri. Il thread Dispatcher non deve eseguire alcuna elaborazione sostanziale che può avere esito negativo dopo il punto di partenza, perché non è più in grado di interrompere in modo sicuro la chiamata. In particolare, non deve generare un'eccezione dopo la consegna del punto o il server potrebbe arrestarsi in modo anomalo. |



 

## <a name="special-error-handling-cases-for-pipes"></a>Casi speciali di gestione degli errori per le pipe

Quando si usano le pipe, esistono casi speciali per la gestione degli errori. Nell'elenco seguente viene illustrata l'origine dell'errore e viene illustrato come gestire l'errore.



| Origine dell'errore                                                                                                 | Modalità di gestione                                                                                                |
|-------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| Il client chiama push e la chiamata ha esito negativo.                                                                             | Non sono necessarie chiamate API RPC. È stato eliminato tutto lo stato RPC.                                         |
| Il client chiama [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) prima che il [**in**](/windows/desktop/Midl/in) Pipes venga svuotato. | La chiamata ha esito negativo con il codice di errore di riempimento pipe appropriato.                                                   |
| Il client chiama pull e la chiamata ha esito negativo.                                                                             | Non sono necessarie chiamate API RPC. È stato eliminato tutto lo stato RPC.                                         |
| Il client o il server chiama push o pull nell'ordine errato.                                                    | Run-Time restituisce lo stato di errore di riempimento della pipe.                                                                |
| Il server chiama push o pull e la chiamata ha esito negativo.                                                                     | Push restituisce un codice di errore. Non è necessaria alcuna chiamata a [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) . |
| Il server chiama **RpcAsyncCompleteCall** prima che le pipe siano state svuotate.                                         | La chiamata pipe restituisce uno stato di errore di riempimento della pipe.                                                         |
| Dopo l'invio, un'operazione di ricezione ha esito negativo.                                                                    | La volta successiva che il server chiama pull per ricevere i dati della pipe, viene restituito un errore.                            |



 

 

 
