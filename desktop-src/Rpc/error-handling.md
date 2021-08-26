---
title: Gestione degli errori (RPC)
description: In RPC sincrono, un client esegue una chiamata remota che restituisce con un codice di esito positivo o negativo.
ms.assetid: 7dfc9f84-ce3c-49f3-8f72-b212095133fd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6daf29091602c36a23c0ed7e08eb0459985e13ca26ec128f401754f64c2329ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120021660"
---
# <a name="error-handling-rpc"></a>Gestione degli errori (RPC)

In RPC sincrono, un client esegue una chiamata remota che restituisce con un codice di esito positivo o negativo. Rpc asincrono offre più opportunità di esito negativo di una chiamata e questi errori vengono gestiti in modo diverso, a seconda della posizione e del momento in cui si verificano. Nella tabella seguente vengono descritti i modi in cui una chiamata può avere esito negativo e come viene gestita.

## <a name="client-side-cleanup"></a>Pulizia lato client



| Sintomo dell'errore                                                                                                                                  | Pulizia                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Il client rileva un'eccezione quando chiama la procedura remota.                                                                                  | Non sono necessarie chiamate API RPC. Tutto lo stato RPC è stato pulito.                                                              |
| Il client riceve una notifica di completamento della chiamata, ma quando chiama [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall)riceve un codice di errore. | Non sono necessarie chiamate API RPC. Tutto lo stato RPC è stato pulito.                                                              |
| Il client ha problemi di annullamento non abortivo o abortivo.                                                                                                   | Il client deve attendere la notifica e chiamare [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) all'arrivo della notifica. |



 

Nella pulizia lato server, un concetto chiave è il punto di consegna. Durante l'elaborazione lato server di una chiamata asincrona, alcune elaborazioni vengono in genere eseguite sul thread che ha ricevuto la chiamata (nota anche come *thread del dispatcher*) e quindi, facoltativamente, il thread del dispatcher inserisce uno stato sufficiente in un blocco di memoria e segnala a un altro thread (noto anche come *thread* di lavoro ) di continuare l'elaborazione per la chiamata. Momento in cui il thread del dispatcher segnala correttamente che il thread di lavoro viene chiamato *punto di consegna*.

## <a name="server-side-cleanup"></a>Pulizia lato server



| Si è verificato un errore      | Pulizia                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Prima del punto di consegna. | Genera un'eccezione. Non è necessaria [**alcuna chiamata a RpcAsyncCompleteCall.**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Dopo il punto di consegna.  | Chiamare [**RpcAsyncAbortCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall) o, se l'errore non è irreversibile e i risultati possono comunque essere restituiti al client, [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall). Se la **chiamata di funzione RpcAsyncCompleteCall** ha esito negativo, il runtime RPC libera i parametri. L'utente non deve accedere a tali parametri. Il thread del dispatcher non deve eseguire alcuna elaborazione sostanziale che potrebbe non riuscire dopo il punto di consegna, perché non può più interrompere in modo sicuro la chiamata. In particolare, non deve generare un'eccezione dopo il punto di consegna o il server potrebbe bloccarsi. |



 

## <a name="special-error-handling-cases-for-pipes"></a>Casi speciali di gestione degli errori per le pipe

Esistono casi speciali per la gestione degli errori quando si usano le pipe. L'elenco seguente illustra l'origine dell'errore e come gestirlo.



| Origine dell'errore                                                                                                 | Modalità di gestione                                                                                                |
|-------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| Il client chiama push e la chiamata ha esito negativo.                                                                             | Non sono necessarie chiamate API RPC. Tutto lo stato RPC è stato pulito.                                         |
| Il client [**chiama RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) prima che le pipe [**in**](/windows/desktop/Midl/in) siano svuotate. | La chiamata ha esito negativo con il codice di errore di riempimento della pipe appropriato.                                                   |
| Il client chiama pull e la chiamata ha esito negativo.                                                                             | Non sono necessarie chiamate API RPC. Tutto lo stato RPC è stato pulito.                                         |
| Il client o il server chiama push o pull nell'ordine errato.                                                    | La fase di esecuzione restituisce lo stato di errore di riempimento della pipe.                                                                |
| Il server chiama push o pull e la chiamata ha esito negativo.                                                                     | Push restituisce un codice di errore. Non è necessaria [**alcuna chiamata a RpcAsyncCompleteCall.**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) |
| Il server **chiama RpcAsyncCompleteCall** prima che le pipe siano state svuotate.                                         | La chiamata pipe restituisce uno stato di errore di riempimento della pipe.                                                         |
| Dopo l'invio, un'operazione di ricezione ha esito negativo.                                                                    | Alla successiva chiamata pull da parte del server per ricevere i dati della pipe, viene restituito un errore.                            |



 

 

 
