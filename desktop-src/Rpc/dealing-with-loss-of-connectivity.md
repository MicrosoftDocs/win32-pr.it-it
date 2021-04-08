---
title: Gestione della perdita di connettività
description: Gestione della perdita di connettività
ms.assetid: a90fcb5a-773e-4c21-bf6c-c3519ec13a09
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de8e7a8088cfe09a4c4026c16cc3dc5ea36b3430
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728866"
---
# <a name="dealing-with-loss-of-connectivity"></a>Gestione della perdita di connettività

Al termine della chiamata RPC la connessione non viene chiusa. è contrassegnato come disponibile. Di conseguenza, il server può essere disattivato o la connettività di rete può andare persa durante o tra le chiamate, mentre una connessione è situata nel pool. Per quanto riguarda i criteri, il tempo di esecuzione RPC esegue un nuovo tentativo di tali chiamate solo se vengono soddisfatte le due condizioni seguenti:

-   Il server non può eventualmente eseguire la chiamata o la chiamata è idempotente.
-   Il client può implementare i tentativi in modo efficiente dalle prestazioni.

I paragrafi seguenti espandono e chiariscono le due condizioni.

Una chiamata idempotente è una chiamata che può essere eseguita più di una volta nel server senza effetti collaterali indesiderati. Ad esempio, la presenza di una chiamata RPC che esegue query sul saldo della banca per un determinato account è idempotente. Se questa chiamata viene eseguita due volte a causa della perdita di connettività, non viene eseguito alcun danno. Un altro esempio di chiamata idempotente è la modifica dell'indirizzo di un cliente in un database. L'esecuzione di due volte è corretta, perché la seconda esecuzione sostituisce semplicemente l'indirizzo già corrente con lo stesso indirizzo. Un'operazione come "sottrazione di 50 dollari dall'account XYZ" non è idempotente. La perdita della connettività di rete non dovrebbe comportare più esecuzioni di una chiamata di questo tipo.

Per essere sicuri, il tempo di esecuzione RPC considera tutte le chiamate come non idempotente. L' \[ \] attributo idempotente non è supportato per [**\_ \_ TCP IP ncacn**](/windows/desktop/Midl/ncacn-ip-tcp)e viene ignorato. Di conseguenza, la prima condizione nell'elenco precedente viene ridotta al *server che non è possibile eseguire la chiamata*.

In molti casi, il tempo di esecuzione RPC non è in grado di determinare definitivamente la chiamata non è già stata eseguita nel server. In questi casi, il client non tenterà di eseguire la chiamata.

Negli esempi seguenti viene illustrato quando il runtime RPC esegue o non tenta una chiamata:

-   Un server è stato riavviato.

    Viene eseguita una chiamata RPC semplice senza sicurezza su un'interfaccia in cui non è stata effettuata alcuna chiamata precedente dopo il riavvio. Poiché non sono state effettuate chiamate a questa interfaccia, il tempo di esecuzione RPC tenta innanzitutto di negoziare l'utilizzo dell'interfaccia. Invia un pacchetto usando una connessione nel pool. Poiché il server è stato riavviato e la connessione non è più valida, viene restituito un errore. Poiché il tempo di esecuzione RPC sul lato client non ha ancora iniziato a inviare i dati per la chiamata effettiva, il client determina che il server potrebbe non essere stato eseguito su tali dati. Quindi, chiude la connessione e cerca un'altra connessione nel pool. Se non riesce a trovare una connessione, apre una nuova connessione e tenta di negoziare nuovamente l'uso dell'interfaccia. Se l'operazione ha esito positivo, viene eseguita la chiamata, ovvero viene eseguito un nuovo tentativo, perché l'errore è stato rilevato prima dell'avvio della chiamata.

-   Una chiamata RPC con sicurezza a livello di privacy (crittografia) viene eseguita su una connessione con un contesto di sicurezza già negoziato.

    Per garantire prestazioni efficienti, il tempo di esecuzione RPC crittografa il pacchetto inline con marshalling (sui dati di testo non crittografato). Se il tentativo di inviare i dati ha esito negativo, il tempo di esecuzione RPC non può ripetere la chiamata, perché i dati di testo non crittografato sono stati sovrascritti con i dati crittografati e non è possibile crittografarli nuovamente con un nuovo contesto di sicurezza. Non viene quindi eseguito alcun tentativo.

-   L'invio di un frammento non primo ha esito negativo.

    Il nuovo tentativo non viene eseguito perché il tempo di esecuzione RPC può scegliere di rimuovere il contenuto del primo frammento una volta completato e non è in grado di ritentare l'invio del primo frammento.

-   La richiesta RPC viene inviata.

    Il server interrompe la connessione. Non viene effettuato alcun tentativo, poiché RPC non è in grado di discernere se il server ha ricevuto la chiamata e ha iniziato a eseguirla.

Se il server utilizza un endpoint dinamico, RPC non risolverà di nuovo l'endpoint durante i tentativi. Ciò significa che se un server viene disattivato e viene riavviato, può risiedere in un endpoint diverso e RPC non risolvono in modo trasparente l'endpoint quando viene ritentata una chiamata. Per forzare la ririsoluzione dell'endpoint, il client RPC deve chiamare [**RpcBindingReset**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset) prima di eseguire un nuovo tentativo di chiamata.

In molti di questi casi, se un client RPC è in grado di determinare se una chiamata è idempotente o se mantiene i dati ignorati da RPC, può scegliere di compilare un meccanismo di ripetizione dei tentativi in RPC.

> [!Note]  
> Se il server è un cluster e i diversi nodi del cluster eseguono versioni diverse del software server, un nuovo tentativo RPC può causare la chiamata su un nodo diverso del cluster in caso di failover e potenzialmente su una versione diversa del server. In questi scenari di distribuzione, assicurarsi che il client non si basi su una versione specifica del software server per eseguire una determinata chiamata. In caso contrario, il client deve compilare un meccanismo su RPC che rileva e gestisce tali condizioni.

 

 

 