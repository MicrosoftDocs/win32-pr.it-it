---
title: Gestione della perdita di connettività
description: Gestione della perdita di connettività
ms.assetid: a90fcb5a-773e-4c21-bf6c-c3519ec13a09
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4eac02c4440cb2e31a29e810d78dfd51764be3ba0ed5a6dc32f8c3e10824bd70
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101681"
---
# <a name="dealing-with-loss-of-connectivity"></a>Gestione della perdita di connettività

Al termine di una chiamata RPC, la connessione non viene chiusa. è contrassegnato come gratuito. Di conseguenza, il server può non essere più disponibile o la connettività di rete può andare persa durante o tra una chiamata e l'altro, mentre una connessione si trova nel pool. In base ai criteri, il tempo di esecuzione RPC tenta nuovamente tali chiamate solo se vengono soddisfatte le due condizioni seguenti:

-   Il server non può eseguire la chiamata oppure la chiamata è idempotente.
-   Il client può implementare i tentativi in modo efficiente in termini di prestazioni.

I paragrafi seguenti espandono e chiariscono le due condizioni.

Una chiamata idempotente è una chiamata che può essere eseguita più volte sul server senza effetti collaterali indesiderati. Ad esempio, la presenza di una chiamata RPC che esegue una query sul saldo della banca per un determinato account è idempotente. Se questa chiamata viene eseguita due volte a causa della perdita di connettività, non viene eseguito alcun danno. Un altro esempio di chiamata idempotente è la modifica dell'indirizzo di un cliente in un database. L'esecuzione di due volte è buona, perché la seconda esecuzione sostituisce semplicemente l'indirizzo già corrente con lo stesso indirizzo. Un'operazione come "sottrarre 50 dollari dall'account xyz" non è idempotente. La perdita della connettività di rete non deve comportare più esecuzioni di una chiamata di questo tipo.

Per essere sicuri, il tempo di esecuzione RPC considera tutte le chiamate come non idempotenti. \[L'attributo idempotent \] non è supportato per [**ncacn \_ ip \_ tcp**](/windows/desktop/Midl/ncacn-ip-tcp)e viene ignorato. Di conseguenza, la prima condizione nell'elenco precedente viene ridotta al server che non può eseguire *la chiamata .*

In molti casi il tempo di esecuzione RPC non è in grado di determinare in modo definitivo che la chiamata non è già stata eseguita nel server. In questi casi, il client non ripeterà l'esecuzione della chiamata.

Gli esempi seguenti illustrano quando il tempo di esecuzione RPC esegue o meno un nuovo tentativo di chiamata:

-   Un server viene riavviato.

    Una semplice chiamata RPC senza sicurezza viene effettuata su un'interfaccia in cui non è stata effettuata alcuna chiamata precedente dopo il riavvio. Poiché non sono state effettuate chiamate su questa interfaccia, il tempo di esecuzione RPC tenta prima di negoziare l'uso dell'interfaccia. Invia un pacchetto usando una connessione nel pool. Poiché il server è stato riavviato e la connessione non è più valida, viene restituito un errore. Poiché il tempo di esecuzione RPC sul lato client non ha ancora iniziato a inviare i dati per la chiamata effettiva, il client determina che il server non avrebbe potuto essere eseguito su tali dati. Di conseguenza, chiude la connessione e cerca un'altra connessione nel pool. Se non riesce a trovare una connessione, apre una nuova connessione e tenta di negoziare nuovamente l'uso dell'interfaccia. Se l'operazione ha esito positivo, viene eseguita la chiamata, ovvero viene eseguito un nuovo tentativo, perché l'errore è stato rilevato prima dell'avvio della chiamata.

-   Una chiamata RPC con sicurezza a livello di privacy (crittografia) viene effettuata su una connessione con un contesto di sicurezza già negoziato.

    Per garantire prestazioni efficienti, il tempo di esecuzione RPC crittografa il pacchetto sottoposto a marshalling inline (sui dati non crittografati). Se il tentativo di inviare i dati ha esito negativo, il tempo di esecuzione RPC non può ripetere la chiamata, perché i dati non crittografati sono stati sovrascritti con i dati crittografati e non possono crittografare nuovamente i dati con un nuovo contesto di sicurezza. Di conseguenza, non viene eseguito alcun tentativo.

-   L'invio di un frammento non first ha esito negativo.

    Non viene eseguito alcun tentativo, poiché il tempo di esecuzione RPC può scegliere di eliminare il contenuto del primo frammento al termine e non è possibile riprovare a inviare il primo frammento.

-   La richiesta RPC viene inviata.

    Il server interrompe la connessione. Non viene effettuato alcun tentativo, poiché RPC non è in grado di riconoscere se il server ha ricevuto la chiamata e ha iniziato a eseguirla.

Se il server usa un endpoint dinamico, RPC non risolverà nuovamente l'endpoint durante i tentativi. Ciò significa che se un server viene arrestato e viene rieperto, potrebbe risiedere in un endpoint diverso e RPC non risolverà in modo trasparente l'endpoint quando viene ritentata una chiamata. Per forzare la risoluzione dell'endpoint, il client RPC deve chiamare [**RpcBindingReset**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset) prima di ritentare una chiamata.

In molti di questi casi, se un client RPC può determinare se una chiamata è idempotente o se mantiene i dati eliminati da RPC, può scegliere di creare un meccanismo di ripetizione dei tentativi su RPC.

> [!Note]  
> Se il server è un cluster e i diversi nodi del cluster eseguono versioni diverse del software del server, un nuovo tentativo RPC può determinare la chiamata su un nodo diverso del cluster in caso di failover e potenzialmente su una versione diversa del server. In questi scenari di distribuzione, assicurarsi che il client non si affidi a una determinata versione del software server per eseguire una determinata chiamata. In caso contrario, il client deve compilare un meccanismo su RPC che rileva e gestisce tali condizioni.

 

 

 