---
title: Gestione dei set di connessioni di rete (associazioni)
description: A partire Windows 2000, il tempo di esecuzione RPC può mantenere più di una connessione tra il client e il server.
ms.assetid: 9b9c42e9-8ed5-46a6-b6ec-4093ce0128bb
keywords:
- Gestione dei set di connessioni di rete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: def88053639c2911dca26d57a080c7fbcbd71728000bee2f12ca7440cb56320b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118928387"
---
# <a name="managing-network-connection-sets-associations"></a>Gestione dei set di connessioni di rete (associazioni)

A partire Windows 2000, il tempo di esecuzione RPC può mantenere più di una connessione tra il client e il server. Ciò facilita l'operazione sui trasporti che non supportano la modifica dell'identità del client senza ristabilire la connessione, i client multithreading e i client asincroni. Il set di connessioni tra un processo client e un endpoint server è detto *associazione* nella terminologia RPC. La comprensione delle associazioni può migliorare l'implementazione di RPC.

In uno scenario di identità a thread singolo e client singolo, RPC apre una connessione tra un processo client e un endpoint server per effettuare chiamate RPC. Quando viene effettuata una chiamata RPC sincrona, il client invia la richiesta al server su questa connessione e riceve anche la risposta. Quando il numero di thread che effettuano chiamate RPC nel processo client aumenta, l'identità di sicurezza del client può cambiare. Quando le chiamate asincrone/pipe vengono miste con chiamate sincrone sul client, RPC potrebbe richiedere più di una connessione di rete. Tutte le connessioni nel set vengono inserite in un pool di connessioni denominato associazione.

Una chiamata di procedura remota sincrona usa esclusivamente una determinata connessione per essere conforme agli standard RPC. Una connessione usata da una chiamata RPC sincrona viene considerata occupata se è stata inviata una richiesta, ma non è stata ricevuta una risposta. Non è consentito altro traffico su tale connessione fino a quando non viene ricevuta la risposta. Il tempo di esecuzione RPC tenta di eseguire chiamate RPC asincrone multiplex e pipe sulla stessa connessione. Le chiamate sincrone e asincrone/pipe non possono essere miste nella stessa connessione. Ciò significa che una determinata connessione può essere usata per chiamate RPC sincrone o per chiamate RPC asincrone/pipe.

RPC tenta in modo aggressivo di riutilizzare le connessioni dal pool. Quando viene effettuata una nuova chiamata RPC, RPC tenta di trovare una connessione appropriata dal pool e crea una nuova connessione solo se non è possibile trovare una connessione appropriata. Perché una connessione sia considerata adatta, deve:

-   Essere del tipo appropriato (sincrono o asincrono/pipe).
-   Essere gratuiti.
-   Avere la stessa identità di sicurezza dell'handle di associazione su cui viene effettuata la chiamata. Se si usa il rilevamento dinamico delle identità, l'identità dell'handle di associazione viene aggiornata dal token del thread all'inizio della chiamata. Se si usa il rilevamento delle identità statiche, viene usata l'identità client contrassegnata sull'handle di associazione.

Al termine della chiamata, una volta ricevuta la risposta, la connessione viene contrassegnata come gratuita e può essere usata per altre chiamate RPC.

L'identità di sicurezza in una connessione non può cambiare. Ad esempio, se un numero elevato di chiamate allo stesso server viene effettuato con identità di sicurezza diverse, il numero di connessioni nel pool di thread aumenta. L'associazione stessa viene conteggiata in base ai riferimenti e, quando tutti i riferimenti non sono più disponibili, arresta e chiude tutte le connessioni. Ogni handle di associazione e ogni handle di contesto contengono un riferimento all'associazione. Quando tutti gli elementi sono chiusi, l'associazione scompare. In Windows XP, le associazioni non scompaiono necessariamente immediatamente; possono rimanere per un breve periodo (il periodo di destinazione è 20 secondi, ma il tempo di esecuzione RPC può scegliere di ritardare l'eliminazione dell'associazione se non sono disponibili thread per eseguire l'attività). Se non si vuole che l'associazione rimanga attiva dopo la chiusura dell'ultimo handle di contesto/associazione, usare l'opzione RPC \_ C \_ OPT \_ DONT LINGER per forzare il runtime RPC a chiudere immediatamente la \_ connessione.

 

 




