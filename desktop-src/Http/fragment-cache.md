---
title: Cache frammenti
description: L'API server HTTP fornisce agli utenti la funzionalità per archiviare i frammenti di dati in una cache da utilizzare per la creazione rapida di risposte HTTP.
ms.assetid: 0f9a768e-723c-4c7b-a746-6b817441409c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3979fb03c4f8898644329fd27eafb7007adbcc9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955258"
---
# <a name="fragment-cache"></a>Cache frammenti

L'API server HTTP fornisce agli utenti la funzionalità per archiviare i frammenti di dati in una cache da utilizzare per la creazione rapida di risposte HTTP.

I frammenti possono essere aggiunti alla cache chiamando la funzione [**HttpAddFragmentToCache**](/windows/desktop/api/Http/nf-http-httpaddfragmenttocache) . Un frammento viene identificato da un URL contenuto nel parametro *pUrlPrefix* . Una chiamata a questa funzione con l'URL di un frammento esistente sovrascrive il frammento esistente.

Un frammento può essere eliminato o sovrascritto dal proprietario della coda di richieste che ha inizialmente aggiunto il frammento. La funzione [**HttpFlushResponseCache**](/windows/desktop/api/Http/nf-http-httpflushresponsecache) chiamata con un URLPrefix Elimina tutti i frammenti all'interno di tale prefisso, nonché i discendenti gerarchici di tale URLPrefix. La funzione [**HttpReadFragmentFromCache**](/windows/desktop/api/Http/nf-http-httpreadfragmentfromcache) legge nell'intero frammento o in un intervallo di byte specificato all'interno del frammento.

> [!Note]  
> L'aggiunta di un frammento alla cache non garantisce che sia disponibile per le chiamate future per inviare una risposta. Le voci della cache dei frammenti possono non essere più disponibili in qualsiasi momento. Una chiamata che utilizza un frammento non disponibile ha esito negativo. Le applicazioni che usano la cache dei frammenti devono essere pronte a gestire questo errore.

 

## <a name="sending-a-response-with-a-fragment"></a>Invio di una risposta con un frammento

I frammenti possono essere usati per formare tutte o parti di un corpo dell'entità di risposte HTTP. È possibile inviare una risposta e il corpo dell'entità in una chiamata alla funzione [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) specificando una matrice di strutture di [**\_ \_ blocco di dati http**](/windows/desktop/api/Http/ns-http-http_data_chunk) nella struttura della [**\_ risposta http**](http-response.md) .

Un blocco di [**\_ dati \_ http**](/windows/desktop/api/Http/ns-http-http_data_chunk) può specificare un blocco di memoria, un handle per un file già aperto o una voce della cache del frammento. Questi corrispondono ai tipi **di \_ \_ blocchi di dati http** : **HttpDataChunkFromMemory**, **HttpDataChunkFromFileHandle** e **HttpDataChunkFromFragmentCache**, rispettivamente. Le risposte complete nella cache HTTP possono essere utilizzate anche come frammenti nella struttura della [**\_ risposta http**](http-response.md) , sebbene questa procedura non sia consigliata.

La struttura della [**\_ risposta http**](http-response.md) contiene un puntatore a una matrice di strutture di [**\_ \_ blocchi di dati http**](/windows/desktop/api/Http/ns-http-http_data_chunk) che comprendono il corpo dell'entità della risposta. La struttura della **\_ risposta http** contiene anche un conteggio delle corrispondenze che specifica la dimensione della matrice di strutture dei **\_ \_ blocchi di dati http** . Il valore HttpDataChunkFromFragmentCache nella struttura **dei \_ \_ blocchi di dati http** specifica il tipo di cache del frammento del blocco di dati. La **struttura \_ dei \_ blocchi di dati http** specifica anche il nome del frammento.

Una risposta che contiene un frammento memorizzato nella cache ha esito negativo e \_ \_ non \_ viene trovato un percorso di errore se le voci della cache dei frammenti non sono disponibili. Poiché non è garantito che le voci della cache dei frammenti siano disponibili, le applicazioni devono essere preparate per la gestione di questo caso. Un modo per gestire questo caso consiste nel tentare di aggiungere nuovamente la voce della cache del frammento e di inviare nuovamente la risposta. Se si verificano ripetuti errori, l'applicazione può usare blocchi di dati archiviati in buffer di memoria anziché voci della cache di frammenti.

È inoltre possibile specificare voci della cache di frammenti nella funzione [**HttpSendResponseEntityBody**](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody) . Il frammento viene aggiunto al corpo dell'entità nella [**struttura \_ dei \_ blocchi di dati http**](/windows/desktop/api/Http/ns-http-http_data_chunk) come descritto in precedenza. Anche in questo caso, l'invio può avere esito negativo se una delle voci della cache di frammenti specificata non è disponibile.

 

 




