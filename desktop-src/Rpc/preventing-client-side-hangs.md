---
title: Prevenzione dei blocchi sul lato client
description: Esistono due modi in cui il client può bloccarsi la connettività di rete può causare la perdita delle richieste del server o l'arresto anomalo del server stesso. Con le opzioni predefinite, RPC non timeoutrà mai una chiamata e il thread client attenderà una risposta per sempre.
ms.assetid: 2c201e29-9d9c-48e6-b0b5-68e4b25c3fb7
keywords:
- RPC remote procedure call , procedure consigliate, prevenzione dei blocchi del client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5da79573e59e30c58a7c236b35293b678c93dde6bf999b477de054d6f3c62971
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118927296"
---
# <a name="preventing-client-side-hangs"></a>Prevenzione dei blocchi sul lato client

Il client può bloccarsi in due modi: la connettività di rete può causare la perdita delle richieste del server o l'arresto anomalo del server stesso. Con le opzioni predefinite, RPC non timeoutrà mai una chiamata e il thread client attenderà una risposta per sempre.

Esistono due metodi per evitare questo problema: mantenere attivi e timeout.

## <a name="tcp-keep-alives"></a>Keep-Alive TCP

Il client può essere configurato per eseguire periodicamente il ping del server per assicurarsi che il server sia attivo e in esecuzione. I ping sono keep-alive TCP per le sequenze di protocollo [**HTTP ncacn \_ ip \_ e**](/windows/desktop/Midl/ncacn-ip-tcp) [**ncacn \_**](/windows/desktop/Midl/ncacn-http) e, di conseguenza, sono efficienti nell'utilizzo della CPU e nella larghezza di banda di rete. Per abilitare i keep-alive in una determinata chiamata di procedura remota, usare la [**funzione RpcMgmtSetComTimeout**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetcomtimeout) prima dell'avvio della chiamata. Questa funzione accetta un handle di associazione e un timeout come argomenti. Ogni chiamata di procedura remota su questo handle di associazione dopo **RpcMgmtSetComTimeout** usa il timeout specificato.

Il parametro Timeout per la [**funzione RpcMgmtSetComTimeout**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetcomtimeout) specifica per quanto tempo il tempo di esecuzione RPC attende prima di attivare i keep-alive. Il timeout è un valore compreso tra 0 e 10, dove 0 è il timeout minimo e 10 è un timeout infinito (nessun timeout). Il timeout non è espresso in secondi. La conversione dal valore di timeout fornito alla funzione **RpcMgmtSetComTimeout** in secondi viene eseguita dal tempo di esecuzione RPC ed è specifica dell'implementazione.

La tabella seguente fornisce la traduzione in secondi per Windows 2000 e Windows XP. Le versioni future Windows modificare il mapping tra il parametro Timeout e il valore di timeout in secondi:

| Parametro timeout                       | Timeout effettivo in secondi |
|-----------------------------------------|----------------------------|
| 0 (TIMEOUT \_ MIN BINDING RPC \_ \_ \_ C)       | 120                        |
| 1                                       | 240                        |
| 2                                       | 360                        |
| 3                                       | 480                        |
| 4                                       | 600                        |
| 5 (TIMEOUT \_ PREDEFINITO ASSOCIAZIONE RPC \_ \_ \_ C)   | 720                        |
| 6                                       | 840                        |
| 7                                       | 960                        |
| 8                                       | 1080                       |
| 9 (TIMEOUT \_ MASSIMO BINDING RPC \_ \_ \_ C)       | 1200                       |
| 10 (TIMEOUT \_ INFINITO ASSOCIAZIONE RPC \_ \_ \_ C) | Timeout infinito          |



 

Una volta attivati i keep-alive, il client invia un pacchetto keep-alive al secondo. Se non viene ricevuto alcun riconoscimento dal server per tre o più keep-alive, il client dichiara la connessione non riuscita e non riesce la chiamata di procedura remota. Se il server invia una risposta entro il timeout specificato, i keep-alive non verranno attivati. Se il server risponde ai keep-alive, ma non risponde alla chiamata di procedura remota, il client continua a inviare keep-alive. Quando il server risponde alla chiamata RPC, i keep-alive vengono disattivati. Per Windows 2000, i keep-alive sono attivati solo per le chiamate RPC sincrone. Per Windows XP, i keep-alive sono attivati anche per le chiamate RPC asincrone.

È allettante impostare keep-alive sul valore più basso per garantire che l'applicazione client risponda ai problemi di rete in modo temporale. È necessario prestare attenzione a tale tentazione e verificare se è giustificato un valore aggressivo. Un server che perde temporaneamente la connettività potrebbe essere inondato di keep-alive da numerosi client dopo il ripristino della connettività. Inoltre, le attività di calcolo lunghe possono richiedere più di due minuti e il server può trovare di trascorrere più tempo della CPU a rispondere ai keep-alive rispetto all'esecuzione di operazioni utili. Pertanto, i keep-alive devono essere usati con moderazione. Se il client non può tollerare che il thread sia legato per lunghi periodi, è necessario considerare RPC asincrono.

Altre sequenze di protocollo possono implementare meccanismi diversi per rilevare i server che non rispondono, a seconda del trasporto usato. Il [**trasporto ncalrpc**](/windows/desktop/Midl/ncalrpc) non usa keep-alive. Poiché tutte le comunicazioni in **ncalrpc** sono locali, se il server non risponde mentre è in corso una chiamata, la fase di esecuzione RPC sul client non riesce immediatamente.

## <a name="call-time-outs"></a>Timeout delle chiamate

I keep-alive TCP sono a posto se la connettività di rete viene persa o se il server si arresta in modo anomalo. Se tuttavia il server si deadlock in modalità utente, i keep-alive TCP restituiscono correttamente, ma la chiamata non restituirà mai . Per gestire questo scenario, è stata aggiunta una nuova opzione di run-time per Windows XP: RPC \_ C \_ OPT CALL \_ \_ TIMEOUT. Questa opzione indica al tempo di esecuzione RPC di configurare un timer ogni volta che invia una richiesta al server. Se il timer scade, la chiamata viene annullata automaticamente e viene completata con RPC \_ S \_ CALL \_ CANCELLED. Finché il server risponde entro il limite di tempo specificato, il client non annullerà la chiamata. Ciò significa che una chiamata a più deframmentazione può richiedere più del periodo di timeout per il completamento, poiché ogni risposta dal server viene ricevuta entro il periodo di timeout, anche se il periodo di tempo per l'arrivo di tutte le risposte è superiore al periodo di timeout.

Inoltre, quando una chiamata viene annullata, il server non viene informato dell'annullamento. Il server, pertanto, probabilmente eseguirà la chiamata a un certo punto e il client ignorerà semplicemente la risposta dal server.

Il problema più pericoloso con i timeout delle chiamate è stabilire un breve timeout e ripetere la chiamata nello stesso server. Lo scenario seguente illustra i rischi di questo approccio:

Imagine un server che opera vicino alla capacità. Ha un numero di client con timeout molto brevi, ad esempio cinque secondi. Una perdita temporanea di connettività di rete o congestione in un router causa un ritardo nelle risposte del server per alcuni secondi. Nelle reti Ethernet questa situazione può essere facilmente causata da un burst di attività su un collegamento che il server condivide con un altro computer. Il server non riesce a inviare tutte le risposte prima del timeout di cinque secondi. I client ottengono le chiamate annullate e riprovano immediatamente. Il server non è a conoscenza che le chiamate sono tentativi e le esegue. Pertanto, invece di eseguire il normale carico di lavoro di chiamate, esegue il 30-50% in più di chiamate, a seconda del timeout dei client. Se questa operazione supera la capacità e il server non può rispondere a tutti i client entro cinque secondi, viene inviato un altro round di chiamate al server. I client continuano a eseguire di nuovo le stesse chiamate e, poiché il server è sovraccarico nell'elaborazione delle chiamate precedenti, non è in grado di rispondere entro il timeout. Una volta che risponde, i client hanno raggiunto il timeout, hanno emesso una nuova chiamata e hanno eliminato la risposta. In uno scenario peggiore, il server non verrà ripristinato fino al riavvio e, a seconda del modello di accesso client, potrebbe non essere ripristinato fino a quando non viene arrestato un numero sufficiente di client.

> [!Note]  
> I timeout delle chiamate funzionano solo nelle sequenze del protocollo [**HTTP ncacn \_ ip \_ e**](/windows/desktop/Midl/ncacn-ip-tcp) [**ncacn. \_**](/windows/desktop/Midl/ncacn-http)

 

 

 