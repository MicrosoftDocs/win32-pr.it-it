---
title: Semantica degli errori per gli handle di contesto
description: In questo argomento viene illustrata la semantica degli errori per gli handle di contesto.
ms.assetid: fcf28519-39ad-4823-bc27-f3502e4d540c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4528b3f5160b92a4e6f10dbcf877e9fec59f81b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044777"
---
# <a name="failure-semantics-for-context-handles"></a>Semantica degli errori per gli handle di contesto

In questo argomento viene illustrata la semantica degli errori per gli handle di contesto.

## <a name="failure-semantics-when-closing-the-context-handle-fails"></a>Semantica degli errori durante la chiusura dell'handle del contesto non riuscita

Si supponga che un'applicazione client tenti di chiudere un handle di contesto aperto sul server, senza arrestare il processo client. Si supponga inoltre che la chiamata al server per chiudere l'handle di contesto abbia esito negativo, ad esempio se il client ha esaurito la memoria. Il modo corretto per gestire questa situazione consiste nel chiamare la funzione [**RpcSsDestroyClientContext**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdestroyclientcontext) . In tal caso il client pulisce il proprio lato dell'handle di contesto e abortively chiude la connessione al server. Poiché la connessione è effettivamente un pool di connessioni (vedere [RPC e la rete](rpc-and-the-network.md)), che è conteggiato come riferimento con un riferimento per ogni binding aperto o handle di contesto, la distruzione dell'handle del contesto chiamando la funzione **RpcSsDestroyClientContext** non elimina effettivamente la connessione. Ma decrementa il conteggio dei riferimenti per il pool di connessioni. Per chiudere le connessioni nel pool, è necessario che il client chiuda tutti gli handle di binding e gli handle di contesto al server dal processo client. Tutte le connessioni nel pool vengono chiuse e il meccanismo di esecuzione del server viene avviato e pulito.

## <a name="failure-semantics-during-change-of-state-of-the-context-handle"></a>Semantica degli errori durante la modifica dello stato dell'handle di contesto

Le informazioni contenute in questa sezione si riferiscono a piattaforme Windows XP e versioni successive.

Gli handle di contesto sono semplicemente parametri di una funzione. Tutte le modifiche apportate allo stato di un handle di contesto si verificano quando viene eseguito il marshalling o l'unmarshalling dei parametri. Se, ad esempio, un client apre un handle del contesto (lo modifica da **null** a non **null**), la fase di esecuzione RPC non apre effettivamente la parte RPC dell'handle fino a quando non viene eseguito il marshalling degli argomenti per l'invio al client. Possono verificarsi errori durante il frattempo. A causa di una varietà di possibili condizioni di rete o risorse insufficienti, la trasmissione del pacchetto al client potrebbe non riuscire. In alternativa, la routine del server può generare un'eccezione durante il tentativo di modificare un handle di contesto. In queste o in altre situazioni di errore, il client e il server possono ottenere visualizzazioni incoerenti dell'handle di contesto. Questa sezione illustra la regola per lo stato dell'handle di contesto e la responsabilità del codice client e server durante le varie condizioni di errore.

-   Arriva un handle di contesto **null** , ma la routine del server rileva un errore e genera un'eccezione.

    La routine del server è responsabile della pulizia di qualsiasi stato correlato all'handle di contesto creato. Il tempo di esecuzione RPC pulisce il proprio stato.

-   Arrivano gli handle di contesto non **null** , ma la routine del server rileva un errore e genera un'eccezione.

    Se la routine del server ha chiuso l'handle del contesto, il client non sarà in grado di conoscerlo, perché la chiamata avrà esito negativo. un ulteriore utilizzo dell'handle di contesto comporterà un \_ \_ errore di \_ mancata corrispondenza del contesto RPC X SS nel \_ client. Se la routine del server non modifica l'handle del contesto, il client può comunque utilizzarlo. Se la routine del server modifica le informazioni archiviate nel contesto del server, le nuove chiamate del client utilizzeranno tali informazioni.

-   Arriva un handle di contesto non **null** e la routine del server chiude l'handle, ma il marshalling dopo il marshalling dell'handle di contesto non è riuscito o l'elaborazione dopo il marshalling non è riuscita.

    L'handle del contesto viene chiuso e le chiamate successive da questo client usando questo handle di contesto generano \_ un \_ \_ errore di mancata corrispondenza del contesto RPC X SS nel \_ client.

-   Viene ricevuto un handle di contesto **null** e il server crea il contesto per questo handle, ma il marshalling dopo il marshalling dell'handle di contesto non è riuscito o l'elaborazione dopo il marshalling non è riuscita.

    In questo caso, il tempo di esecuzione RPC richiama l'esecuzione per questo handle di contesto e pulisce lo stato RPC per questo handle di contesto. L'handle del contesto non verrà creato sul lato client.

-   Viene ricevuto un handle di contesto non **null** e il server non modifica l'handle del contesto o modifica le informazioni archiviate nel contesto del server e il marshalling ha esito negativo dopo il marshalling dell'handle di contesto.

    Le nuove chiamate dal client utilizzeranno l'handle di contesto del server.

-   Arriva un handle di contesto **null** e il server non lo imposta su un valore diverso da **null**, ma la chiamata ha esito negativo prima del marshalling dell'handle di contesto.

    In questo caso, non viene creato alcun handle di contesto nel client.

-   Arriva un handle di contesto non **null** e il server lo imposta su **null**, ma il marshalling ha esito negativo prima del marshalling dell'handle di contesto.

    In questo caso, l'handle di contesto rimane chiuso sul server e il client ottiene gli \_ \_ \_ errori di contesto RPC X SS \_ quando tenta di usare l'handle di contesto.

-   Un handle di contesto **null** arriva sul server e il server lo imposta su un valore diverso da **null**, ma il marshalling ha esito negativo prima del marshalling dell'handle di contesto.

    È necessario richiamare l'handle del contesto in modo che sia possibile eseguire la pulizia del server e non venga creato alcun handle di contesto nel client.

-   Viene ricevuto un handle di contesto non **null** e il server non modifica l'handle del contesto o modifica le informazioni archiviate nel contesto del server e il marshalling ha esito negativo prima del marshalling dell'handle di contesto.

    Le nuove chiamate dal client utilizzeranno lo stato nel server.

-   Un handle di contesto viene dichiarato come valore restituito e la routine del server restituisce **null** per l'handle del contesto e il marshalling ha esito negativo prima del marshalling dell'handle di contesto.

    In questo caso, non viene creato alcun nuovo contesto nel client.

-   Un handle di contesto viene dichiarato come valore restituito e la routine del server restituisce un valore diverso da **null** per l'handle del contesto e il marshalling ha esito negativo prima del marshalling dell'handle di contesto.

    Il tempo di esecuzione RPC chiama la routine di esecuzione dell'handle di contesto per dare la possibilità di eseguire la pulizia e non viene creato alcun nuovo contesto nel client.

 

 




