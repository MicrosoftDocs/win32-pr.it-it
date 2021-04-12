---
title: Gestione dei set di connessioni di rete (associazioni)
description: A partire da Windows 2000, il tempo di esecuzione RPC può mantenere più di una connessione tra il client e il server.
ms.assetid: 9b9c42e9-8ed5-46a6-b6ec-4093ce0128bb
keywords:
- Gestione dei set di connessioni di rete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81e99afe23d90e44d85dc7a2ec9301b45e1f20b1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221785"
---
# <a name="managing-network-connection-sets-associations"></a>Gestione dei set di connessioni di rete (associazioni)

A partire da Windows 2000, il tempo di esecuzione RPC può mantenere più di una connessione tra il client e il server. Ciò semplifica l'operazione sui trasporti che non supportano la modifica dell'identità client senza ristabilire la connessione, i client multithread e i client asincroni. Il set di connessioni tra un processo client e un endpoint server è detto *associazione* nella terminologia RPC. La comprensione delle associazioni può migliorare l'implementazione di RPC.

In uno scenario di identità a singolo thread e singolo client, RPC apre una connessione tra un processo client e un endpoint server per eseguire chiamate RPC. Quando viene eseguita una chiamata RPC sincrona, il client invia la richiesta al server in questa connessione e riceve anche la risposta. Quando aumenta il numero di thread che effettuano chiamate RPC nel processo client, l'identità di sicurezza del client può cambiare. Quando le chiamate asincrone/pipe vengono combinate con chiamate sincrone sul client, RPC potrebbe richiedere più di una connessione di rete. Tutte le connessioni nel set vengono inserite in un pool di connessioni denominato associazione.

Una chiamata di procedura remota sincrona usa esclusivamente una determinata connessione per essere conforme agli standard RPC. Una connessione utilizzata da una chiamata RPC sincrona è considerata occupata se è stata inviata una richiesta, ma non è stata ricevuta alcuna risposta. Nessun altro traffico consentito sulla connessione fino a quando non viene ricevuta la risposta. Il tempo di esecuzione RPC tenta di eseguire il multiplexing di chiamate RPC asincrone e pipe sulla stessa connessione. Le chiamate sincrone e asincrone/pipe non possono essere combinate nella stessa connessione, il che significa che una determinata connessione può essere utilizzata per chiamate RPC sincrone o per chiamate RPC asincrone/pipe.

RPC tenta di riutilizzare in modo aggressivo le connessioni dal pool. Quando viene effettuata una nuova chiamata RPC, RPC tenta di trovare una connessione appropriata dal pool e crea una nuova connessione solo se non è possibile trovare una connessione appropriata. Affinché una connessione venga considerata adatta, è necessario:

-   Essere del tipo appropriato (sincrono o asincrono/pipe).
-   È gratuito.
-   Avere la stessa identità di sicurezza dell'handle di associazione in cui viene effettuata la chiamata. Se viene utilizzato il rilevamento dinamico delle identità, l'identità dell'handle di associazione viene aggiornata dal token del thread all'inizio della chiamata. Se viene utilizzato il rilevamento statico delle identità, viene utilizzata l'identità del client contrassegnata sull'handle di associazione.

Quando la chiamata è completa, una volta ricevuta la risposta, la connessione viene contrassegnata come disponibile e può essere utilizzata per altre chiamate RPC.

Impossibile modificare l'identità di sicurezza di una connessione. Se, ad esempio, un numero elevato di chiamate allo stesso server viene eseguito con diverse identità di sicurezza, il numero di connessioni nel pool di thread aumenta. L'associazione stessa è conteggiata come riferimento e, quando tutti i riferimenti sono finiti, arresta e chiude tutte le connessioni. Ogni handle di binding e ogni handle di contesto contengono un riferimento nell'associazione. Quando tutti sono chiusi, l'associazione scompare. In Windows XP le associazioni non devono necessariamente scomparire immediatamente; potrebbero rimanere per un breve periodo di tempo (il periodo di destinazione è di 20 secondi, ma il tempo di esecuzione RPC può scegliere di ritardare l'eliminazione dell'associazione se non sono disponibili thread per l'esecuzione dell'attività). Se non si desidera che l'associazione resti attiva dopo la chiusura dell'ultimo handle di contesto/binding, utilizzare l' \_ \_ opzione relativa al consenso esplicito di RPC C \_ \_ per forzare il runtime RPC alla chiusura immediata della connessione.

 

 




