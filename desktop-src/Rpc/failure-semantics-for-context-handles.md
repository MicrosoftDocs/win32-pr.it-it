---
title: Semantica degli errori per gli handle di contesto
description: Questo argomento illustra la semantica degli errori per gli handle di contesto.
ms.assetid: fcf28519-39ad-4823-bc27-f3502e4d540c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9549a659c56c4761de8df4f43c54b823d32f74786af928821ba82b6effc3bba7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120021271"
---
# <a name="failure-semantics-for-context-handles"></a>Semantica degli errori per gli handle di contesto

Questo argomento illustra la semantica degli errori per gli handle di contesto.

## <a name="failure-semantics-when-closing-the-context-handle-fails"></a>Semantica degli errori durante la chiusura dell'handle di contesto non riuscita

Imagine un'applicazione client sta tentando di chiudere un handle di contesto aperto nel server, senza arrestare il processo client. Si supponga inoltre che la chiamata al server per chiudere l'handle di contesto non riesca(ad esempio, la memoria del client è insufficiente). Il modo corretto per gestire questa situazione è chiamare la [**funzione RpcSsDestroyClientContext.**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdestroyclientcontext) In tal caso, il client pulisce il lato dell'handle di contesto e chiude in modo abortivo la connessione al server. Poiché la connessione è effettivamente un pool di connessioni (vedere [RPC](rpc-and-the-network.md)e rete ), che viene conteggiato come riferimento con un riferimento per ogni handle di contesto o associazione aperto, l'eliminazione dell'handle di contesto chiamando la funzione **RpcSsDestroyClientContext** non elimina effettivamente la connessione. Invece, decrementa il conteggio dei riferimenti per il pool di connessioni. Per chiudere le connessioni nel pool, il client deve chiudere tutti gli handle di associazione e gli handle di contesto per il server dal processo client. Quindi tutte le connessioni nel pool vengono chiuse e viene avviato il meccanismo di run-down del server e viene eseguita la pulizia.

## <a name="failure-semantics-during-change-of-state-of-the-context-handle"></a>Semantica degli errori durante la modifica dello stato dell'handle di contesto

Le informazioni contenute in questa sezione si riferiscono Windows xp e piattaforme successive.

Gli handle di contesto sono semplicemente parametri di una funzione. Tutte le modifiche nello stato di un handle di contesto si verificano quando viene effettuato il marshalling o l'unmarssing dei parametri. Ad esempio, se un client apre un handle di contesto (lo modifica da **NULL** a non **NULL),** il run-time RPC non apre effettivamente la parte RPC dell'handle fino a quando non viene effettuato il marshalling degli argomenti per l'invio al client. Gli errori possono verificarsi durante la fase intermedia. A causa di un'ampia gamma di possibili condizioni di rete o di risorse basse, la trasmissione del pacchetto al client potrebbe non riuscire. Oppure la routine del server può generare un'eccezione durante il tentativo di modificare un handle di contesto. In queste o in altre situazioni di errore, il client e il server possono ottenere visualizzazioni incoerenti dell'handle di contesto. In questa sezione viene illustrata la regola per lo stato dell'handle di contesto e la responsabilità del codice client e del server durante varie condizioni di errore.

-   Arriva un handle di contesto **NULL,** ma la routine del server rileva un errore e genera un'eccezione.

    È responsabilità della routine del server pulire qualsiasi stato correlato all'handle di contesto creato. Il tempo di esecuzione RPC ne pulisce lo stato.

-   Arriva un handle di contesto non **NULL,** ma la routine del server rileva un errore e genera un'eccezione.

    Se la routine del server ha chiuso l'handle di contesto, il client non lo saprà, poiché la chiamata non avrà esito positivo. Un ulteriore uso dell'handle di contesto restituirà un errore RPC \_ X \_ SS \_ CONTEXT \_ MISMATCH nel client. Se la routine del server non modifica l'handle di contesto, il client può comunque usarlo. Se la routine del server modifica le informazioni archiviate nel contesto del server, le nuove chiamate dal client useranno tali informazioni.

-   Arriva un handle di contesto non **NULL** e la routine del server chiude l'handle, ma il marshalling dopo il marshalling dell'handle di contesto non è riuscito o l'elaborazione dopo il marshalling non è riuscita.

    L'handle di contesto viene chiuso e altre chiamate da parte di questo client che usano questo handle di contesto comportano un errore RPC \_ X \_ SS \_ CONTEXT \_ MISMATCH nel client.

-   Arriva un handle di contesto **NULL** e il server crea il contesto per questo handle, ma il marshalling dopo il marshalling dell'handle di contesto non è riuscito o l'elaborazione dopo il marshalling non è riuscita.

    In questo caso, il run-time RPC richiama l'esecuzione per questo handle di contesto e pulisce lo stato RPC per questo handle di contesto. L'handle di contesto non verrà creato sul lato client.

-   Arriva un handle di contesto non **NULL** e il server non modifica l'handle di contesto oppure modifica le informazioni archiviate nel contesto del server e il marshalling ha esito negativo dopo il marshalling dell'handle di contesto.

    Le nuove chiamate dal client useranno l'handle di contesto del server.

-   Arriva un handle di contesto **NULL** e il server non lo imposta su un valore diverso da **NULL,** ma la chiamata ha esito negativo prima del marshalling dell'handle di contesto.

    In questo caso, non viene creato alcun handle di contesto nel client.

-   Arriva un handle di contesto non **NULL** e il server lo imposta su **NULL,** ma il marshalling ha esito negativo prima del marshalling dell'handle di contesto.

    In questo caso, l'handle di contesto rimane chiuso nel server e il client ottiene errori RPC X SS CONTEXT MISMATCH quando tenta di \_ \_ usare \_ \_ l'handle di contesto.

-   Un **handle di** contesto NULL arriva sul server e il server lo imposta su non **NULL,** ma il marshalling ha esito negativo prima del marshalling dell'handle di contesto.

    L'handle di contesto deve essere richiamato in modo che il server possa eseguire la pulizia e non verrà creato alcun handle di contesto nel client.

-   Arriva un handle di contesto non **NULL** e il server non modifica l'handle di contesto oppure modifica le informazioni archiviate nel contesto del server e il marshalling ha esito negativo prima del marshalling dell'handle di contesto.

    Le nuove chiamate dal client useranno lo stato nel server.

-   Un handle di contesto viene dichiarato come valore restituito e la routine del server restituisce **NULL** per l'handle di contesto e il marshalling ha esito negativo prima del marshalling dell'handle di contesto.

    In questo caso, non viene creato alcun nuovo contesto nel client.

-   Un handle di contesto viene dichiarato come valore restituito e la routine del server restituisce non **NULL** per l'handle di contesto e il marshalling ha esito negativo prima del marshalling dell'handle di contesto.

    La fase di esecuzione RPC chiama la routine di run-down dell'handle di contesto per offrire la possibilità di eseguire la pulizia e non viene creato alcun nuovo contesto nel client.

 

 




