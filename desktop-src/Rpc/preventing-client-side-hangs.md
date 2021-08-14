---
title: Prevenzione dei blocchi sul lato client
description: Esistono due modi in cui il client può bloccarsi la connettività di rete può causare la perdita delle richieste del server o l'arresto anomalo del server stesso. Con le opzioni predefinite, RPC non timeoutrà mai una chiamata e il thread client attenderà all'infinito una risposta.
ms.assetid: 2c201e29-9d9c-48e6-b0b5-68e4b25c3fb7
keywords:
- RPC Remote Procedure Call, procedure consigliate, prevenzione dei blocchi del client
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

Il client può bloccarsi in due modi: la connettività di rete può causare la perdita delle richieste del server o l'arresto anomalo del server stesso. Con le opzioni predefinite, RPC non timeoutrà mai una chiamata e il thread client attenderà all'infinito una risposta.

Esistono due metodi per evitare questo problema: keep-alive e timeout.

## <a name="tcp-keep-alives"></a>Keep-alive TCP

Il client può essere configurato per effettuare periodicamente il ping del server per assicurarsi che il server sia attivo e in esecuzione. I ping sono keep-alive TCP per le sequenze dei protocolli TCP e [**ncacn \_ http ncacn**](/windows/desktop/Midl/ncacn-http) e, di conseguenza, sono efficienti in termini di utilizzo della CPU e larghezza di banda di rete. [**\_ \_**](/windows/desktop/Midl/ncacn-ip-tcp) Per abilitare i keep-alive in una determinata chiamata di procedura remota, usare la [**funzione RpcMgmtSetComTimeout**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetcomtimeout) prima dell'avvio della chiamata. Questa funzione accetta un handle di associazione e un timeout come argomenti. Ogni chiamata di procedura remota su questo handle di associazione dopo **RpcMgmtSetComTimeout** usa il timeout specificato.

Il parametro Timeout per la [**funzione RpcMgmtSetComTimeout**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetcomtimeout) specifica per quanto tempo il tempo di esecuzione RPC attende prima di attivare i keep-alive. Il timeout è un valore compreso tra 0 e 10, dove 0 è il timeout minimo e 10 è un timeout infinito (nessun timeout). Il timeout non è espresso in secondi. La conversione dal valore di timeout fornito alla funzione **RpcMgmtSetComTimeout** in secondi viene eseguita dal tempo di esecuzione RPC ed è specifica dell'implementazione.

La tabella seguente fornisce la conversione in secondi per Windows 2000 e Windows XP. Le versioni future Windows possibile modificare il mapping tra il parametro Timeout e il valore di timeout in secondi:

| Parametro timeout                       | Timeout effettivo in secondi |
|-----------------------------------------|----------------------------|
| 0 (RPC \_ C \_ BINDING MIN \_ \_ TIMEOUT)       | 120                        |
| 1                                       | 240                        |
| 2                                       | 360                        |
| 3                                       | 480                        |
| 4                                       | 600                        |
| 5 (TIMEOUT \_ PREDEFINITO \_ DELL'ASSOCIAZIONE RPC \_ \_ C)   | 720                        |
| 6                                       | 840                        |
| 7                                       | 960                        |
| 8                                       | 1080                       |
| 9 (TIMEOUT \_ MASSIMO BINDING RPC \_ \_ \_ C)       | 1200                       |
| 10 (RPC \_ C \_ BINDING INFINITE \_ \_ TIMEOUT) | Timeout infinito          |



 

Una volta attivati i keep-alive, il client invia un pacchetto keep-alive al secondo. Se non viene ricevuto alcun riconoscimento dal server per tre o più keep-alive, il client dichiara la connessione non attiva e non riesce la chiamata di procedura remota. Se il server invia una risposta entro il timeout specificato, i keep-alive non verranno attivati. Se il server risponde ai keep-alive, ma non risponde alla chiamata di procedura remota, il client continua a inviare keep-alive. Quando il server risponde alla chiamata RPC, i keep-alive vengono disattivati. Per Windows 2000, i keep-alive sono attivati solo per le chiamate RPC sincrone. Per Windows XP, i keep-alive sono attivati anche per le chiamate RPC asincrone.

È allettante impostare i keep-alive sul valore più basso per garantire che l'applicazione client risponda ai problemi di rete in modo temporaneo. È necessario prestare particolare attenzione a questo tipo di sfasamento e verificare se è garantito un valore aggressivo. Un server che perde temporaneamente la connettività può risultare inondato da keep-alive da numerosi client dopo il ripristino della connettività. Inoltre, le attività di calcolo di lunga durata possono richiedere più di due minuti e il server potrebbe essere in grado di trascorrere più tempo della CPU a rispondere ai keep-alive rispetto all'esecuzione di operazioni utili. Pertanto, i keep-alive devono essere usati con la moderazione. Se il client non può tollerare che il thread sia associato per lunghi periodi, è consigliabile prendere in considerazione la rpc asincrona.

Altre sequenze di protocollo possono implementare meccanismi diversi per rilevare i server che non rispondono, a seconda del trasporto utilizzato. Il [**trasporto ncalrpc**](/windows/desktop/Midl/ncalrpc) non usa keep-alive. Poiché tutte le comunicazioni in **ncalrpc** sono locali, se il server non risponde mentre è in corso una chiamata, il tempo di esecuzione RPC sul client non riesce immediatamente.

## <a name="call-time-outs"></a>Timeout delle chiamate

I keep-alive TCP sono disponibili in caso di perdita della connettività di rete o in caso di arresto anomalo del server. Tuttavia, se il server si deadlock in modalità utente, i keep-alive TCP restituiscono correttamente, ma la chiamata non verrà mai restituita. Per gestire questo scenario, è stata aggiunta una nuova opzione di run-time per Windows XP: RPC \_ C \_ OPT CALL \_ \_ TIMEOUT. Questa opzione indica al tempo di esecuzione RPC di configurare un timer ogni volta che invia una richiesta al server. Se il timer scade, la chiamata viene annullata automaticamente e viene completata con RPC \_ S \_ CALL \_ CANCELLED. Finché il server risponde entro il limite di tempo specificato, il client non annullerà la chiamata. Ciò significa che una chiamata a più deframmentazione può richiedere più del periodo di timeout per il completamento, perché ogni risposta dal server viene ricevuta entro il periodo di timeout, anche se il periodo di tempo per l'arrivo di tutte le risposte è superiore al periodo di timeout.

Inoltre, quando una chiamata viene annullata, il server non viene informato dell'annullamento. Il server, pertanto, probabilmente eseguirà la chiamata a un certo punto e il client ignorerà semplicemente la risposta dal server.

Il problema più pericoloso con i timeout delle chiamate è stabilire un breve timeout e ripetere la chiamata sullo stesso server. Lo scenario seguente illustra i rischi di questo approccio:

Imagine un server che opera in prossimità della capacità. Ha un numero di client con timeout molto brevi, ad esempio cinque secondi. Una perdita temporanea di connettività di rete o congestione in un router causa un ritardo nelle risposte del server per alcuni secondi. Nelle reti Ethernet questa situazione può essere facilmente causata da un burst di attività in un collegamento che il server condivide con un altro computer. Il server non riesce a inviare tutte le risposte prima del timeout di cinque secondi. I client ottengono le chiamate annullate e riprovano immediatamente. Il server non è in grado di riconoscere che le chiamate sono tentativi e le esegue. Pertanto, invece di eseguire il normale carico di lavoro delle chiamate, esegue il 30-50% in più di chiamate, a seconda del numero di client che hanno timeout. Se questa operazione supera la capacità e il server non può rispondere a tutti i client entro cinque secondi, viene inviato un altro ciclo di chiamate al server. I client continuano a eseguire le stesse chiamate e, poiché il server è sovraccarico nell'elaborazione delle chiamate precedenti, non è in grado di rispondere entro il timeout. Una volta che risponde, i client hanno raggiunto il timeout, hanno emesso una nuova chiamata e hanno eliminato la risposta. Nel peggiore dei casi, il server non verrà ripristinato fino al riavvio e, a seconda del modello di accesso client, potrebbe non essere ripristinato fino a quando non viene arrestato un numero sufficiente di client.

> [!Note]  
> I timeout delle chiamate funzionano solo nelle sequenze del protocollo [**HTTP ncacn \_ ip \_ tcp**](/windows/desktop/Midl/ncacn-ip-tcp) e [**ncacn. \_**](/windows/desktop/Midl/ncacn-http)

 

 

 