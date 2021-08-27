---
title: Cache dei frammenti
description: L'API server HTTP offre agli utenti funzionalità per archiviare frammenti di dati in una cache da usare per formare rapidamente risposte HTTP.
ms.assetid: 0f9a768e-723c-4c7b-a746-6b817441409c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6659ead1139bd1b35a466a56c44357dd1f7f30cbac5fad8669445208be0e5136
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047251"
---
# <a name="fragment-cache"></a>Cache dei frammenti

L'API server HTTP offre agli utenti funzionalità per archiviare frammenti di dati in una cache da usare per formare rapidamente risposte HTTP.

È possibile aggiungere frammenti alla cache chiamando la [**funzione HttpAddFragmentToCache.**](/windows/desktop/api/Http/nf-http-httpaddfragmenttocache) Un frammento è identificato da un URL contenuto nel *parametro pUrlPrefix.* Una chiamata a questa funzione con l'URL di un frammento esistente sovrascrive il frammento esistente.

Un frammento può essere eliminato o sovrascritto dal proprietario della coda di richieste che ha inizialmente aggiunto il frammento. La [**funzione HttpFlushResponseCache**](/windows/desktop/api/Http/nf-http-httpflushresponsecache) chiamata con UrlPrefix elimina tutti i frammenti all'interno di tale prefisso, nonché i discendenti gerarchici di tale UrlPrefix. La [**funzione HttpReadFragmentFromCache**](/windows/desktop/api/Http/nf-http-httpreadfragmentfromcache) legge l'intero frammento o un intervallo di byte specificato all'interno del frammento.

> [!Note]  
> L'aggiunta di un frammento alla cache non garantisce che sia disponibile per le chiamate future per l'invio di una risposta. Le voci della cache dei frammenti possono diventare non disponibili in qualsiasi momento. Una chiamata che usa un frammento non disponibile ha esito negativo. Le applicazioni che usano la cache dei frammenti devono essere preparate per gestire questo errore.

 

## <a name="sending-a-response-with-a-fragment"></a>Invio di una risposta con un frammento

I frammenti possono essere usati per formare tutto o parti del corpo di un'entità di risposte HTTP. È possibile inviare una risposta e il corpo dell'entità in una chiamata alla funzione [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) specificando una matrice di strutture [**HTTP DATA \_ \_ CHUNK**](/windows/desktop/api/Http/ns-http-http_data_chunk) nella [**struttura HTTP \_ RESPONSE.**](http-response.md)

Un [**BLOCCO \_ DI \_ DATI HTTP**](/windows/desktop/api/Http/ns-http-http_data_chunk) può specificare un blocco di memoria, un handle per un file già aperto o una voce della cache di frammenti. Corrispondono rispettivamente ai tipi CHUNK di DATI **HTTP: \_ \_** **HttpDataChunkFromMemory**, **HttpDataChunkFromFileHandle** e **HttpDataChunkFromFragmentCache**. Le risposte complete nella cache HTTP possono essere usate anche come frammenti nella struttura [**DI RISPOSTA HTTP, \_**](http-response.md) anche se questa procedura non è consigliata.

La [**struttura \_ HTTP RESPONSE**](http-response.md) contiene un puntatore a una matrice di strutture HTTP DATA [**\_ \_ CHUNK**](/windows/desktop/api/Http/ns-http-http_data_chunk) che comprendono il corpo dell'entità della risposta. La **struttura \_ HTTP RESPONSE** contiene anche un conteggio corrispondente che specifica la dimensione della matrice di strutture HTTP DATA **\_ \_ CHUNK.** Il valore HttpDataChunkFromFragmentCache nella struttura **HTTP \_ DATA \_ CHUNK** specifica il tipo di cache dei frammenti del blocco di dati. La **struttura HTTP DATA \_ \_ CHUNK** specifica anche il nome del frammento.

Una risposta che contiene un frammento memorizzato nella cache ha esito negativo e viene restituito ERROR PATH NOT FOUND se una delle voci della \_ \_ cache del \_ frammento non è disponibile. Poiché non è garantito che le voci della cache dei frammenti siano disponibili, le applicazioni devono essere preparate per gestire questo caso. Un modo per gestire questo caso è tentare di aggiungere nuovamente la voce della cache del frammento e inviare nuovamente la risposta. Se si verificano errori ripetuti, l'applicazione può usare blocchi di dati archiviati in buffer di memoria anziché voci della cache di frammenti.

Le voci della cache dei frammenti possono essere specificate anche nella [**funzione HttpSendResponseEntityBody.**](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody) Il frammento viene aggiunto al corpo dell'entità nella [**struttura HTTP \_ DATA \_ CHUNK**](/windows/desktop/api/Http/ns-http-http_data_chunk) come descritto in precedenza. Anche in questo caso, l'invio può avere esito negativo se una delle voci della cache dei frammenti specificate non è disponibile.

 

 




