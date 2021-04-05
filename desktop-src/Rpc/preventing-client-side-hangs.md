---
title: Prevenzione degli blocchi lato client
description: Esistono due modi in cui il client può bloccare la connettività di rete può causare la perdita delle richieste del server oppure il server stesso può arrestarsi in modo anomalo. Con le opzioni predefinite, la chiamata RPC non condurrà mai il timeout di una chiamata e il thread del client rimarrà in attesa di una risposta.
ms.assetid: 2c201e29-9d9c-48e6-b0b5-68e4b25c3fb7
keywords:
- RPC (Remote Procedure Call), procedure consigliate, impedire blocchi del client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18d4b5fc92ca18b575d081cd7b5abf90929e7df5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727786"
---
# <a name="preventing-client-side-hangs"></a>Prevenzione degli blocchi lato client

È possibile bloccare il client in due modi: la connettività di rete può comportare la perdita delle richieste server oppure il server stesso può arrestarsi in modo anomalo. Con le opzioni predefinite, la chiamata RPC non condurrà mai il timeout di una chiamata e il thread del client rimarrà in attesa di una risposta.

Esistono due metodi per evitare questo problema: Keep-Alive e timeout.

## <a name="tcp-keep-alives"></a>Keep-alive TCP

Il client può essere configurato per eseguire periodicamente il ping del server per verificare che il server sia attivo e in esecuzione. I ping sono Keep-alive TCP per le sequenze del protocollo [**\_ http**](/windows/desktop/Midl/ncacn-http) [**ncacn \_ \_ TCP**](/windows/desktop/Midl/ncacn-ip-tcp) e ncacn e, di conseguenza, sono efficienti nell'utilizzo della CPU e della larghezza di banda di rete. Per abilitare Keep Alive in una determinata chiamata di procedura remota, usare la funzione [**RpcMgmtSetComTimeout**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetcomtimeout) prima dell'avvio della chiamata. Questa funzione accetta un handle di binding e un timeout come argomenti. Ogni chiamata di procedura remota su questo handle di binding dopo **RpcMgmtSetComTimeout** usa il timeout specificato.

Il parametro timeout per la funzione [**RpcMgmtSetComTimeout**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetcomtimeout) specifica il tempo di attesa del tempo di esecuzione RPC prima che venga attivato Keep Alive. Il timeout è un valore compreso tra 0 e 10, dove 0 indica il timeout minimo e 10 è il timeout infinito (nessun timeout). Il timeout non è in secondi; la conversione dal valore di timeout fornito alla funzione **RpcMgmtSetComTimeout** ai secondi viene eseguita dal tempo di esecuzione RPC ed è specifica dell'implementazione.

La tabella seguente fornisce la traduzione in secondi per Windows 2000 e Windows XP. Le versioni future di Windows potrebbero modificare il mapping tra il parametro timeout e il valore di timeout in secondi:

| Parametro timeout                       | Timeout effettivo in secondi |
|-----------------------------------------|----------------------------|
| 0 ( \_ \_ timeout minimo binding RPC c \_ \_ )       | 120                        |
| 1                                       | 240                        |
| 2                                       | 360                        |
| 3                                       | 480                        |
| 4                                       | 600                        |
| 5 ( \_ \_ timeout predefinito associazione RPC C \_ \_ )   | 720                        |
| 6                                       | 840                        |
| 7                                       | 960                        |
| 8                                       | 1080                       |
| 9 ( \_ \_ timeout massimo associazione RPC C \_ \_ )       | 1200                       |
| 10 ( \_ \_ timeout infinito associazione RPC C \_ \_ ) | Timeout infinito          |



 

Una volta attivati i keep-alive, il client invia un pacchetto Keep-Alive ogni secondo. Se non è presente alcun riconoscimento dal server per tre o più Keep Alive, il client dichiara la connessione inattiva e non riesce a chiamare la procedura remota. Se il server invia una risposta entro il timeout specificato, Keep Alive non verrà attivato. Se il server risponde per restare attivo, ma non risponde alla chiamata di procedura remota, il client continua a inviare keep alive. Una volta che il server risponde alla chiamata RPC, il Keep Alive viene disattivato. Per Windows 2000, Keep Alive viene attivato solo per le chiamate RPC sincrone. Per Windows XP, i Keep Alive sono attivati anche per le chiamate RPC asincrone.

Si tenta di impostare Keep-Alive sul valore più basso per garantire che l'applicazione client risponda tempestivamente ai problemi di rete. È necessario prestare particolare attenzione a tale tentazione e verificare che venga applicato un valore aggressivo. Una volta ripristinato la connettività, un server che perde temporaneamente la connettività potrebbe trovarsi allagato con Keep-Alive da numerosi client. Inoltre, le attività di calcolo lunghe possono richiedere più di due minuti e il server potrebbe trovarsi a dover spendere più tempo della CPU rispondendo a Keep-Alive rispetto all'esecuzione di operazioni utili. Pertanto, è consigliabile utilizzare Keep Alive con moderazione. Se il client non è in grado di tollerare che il thread venga associato per periodi prolungati, è necessario prendere in considerazione la RPC asincrona.

Altre sequenze di protocollo possono implementare meccanismi diversi per il rilevamento di server che non rispondono, a seconda del trasporto usato. Il trasporto [**ncalrpc**](/windows/desktop/Midl/ncalrpc) non utilizza keep alive. Poiché tutte le comunicazioni in **ncalrpc** sono locali, se il server smette di rispondere mentre è in corso una chiamata, il tempo di esecuzione RPC sul client ha immediatamente esito negativo.

## <a name="call-time-outs"></a>Timeout chiamata

I keep-alive TCP sono buoni se la connettività di rete viene persa o se il server si arresta in modo anomalo. Tuttavia, se il server si blocca in modalità utente, TCP Keep Alive viene restituito correttamente, ma la chiamata non viene mai restituita. Per gestire questo scenario, è stata aggiunta una nuova opzione di run-time per Windows XP: \_ timeout RPC C \_ opt \_ Call \_ . Questa opzione indica al runtime RPC di impostare un timer ogni volta che invia una richiesta al server. Se il timer scade, la chiamata viene annullata automaticamente e completata con la \_ chiamata RPC S \_ \_ annullata. Fino a quando il server risponde entro il limite di tempo specificato, il client non annulla la chiamata. Ciò significa che una chiamata a più frammenti può richiedere più del periodo di timeout per il completamento, in quanto ogni risposta dal server viene ricevuta entro il periodo di timeout, anche se il periodo di tempo per tutte le risposte da raggiungere è maggiore del periodo di timeout.

Inoltre, quando viene annullata una chiamata, il server non riceve alcuna notifica dell'annullamento. Il server, pertanto, eseguirà probabilmente la chiamata in un determinato momento e il client ignorerà semplicemente la risposta dal server.

L'insidia più pericolosa con i timeout delle chiamate è la definizione di un breve timeout e l'esecuzione di un nuovo tentativo di chiamata sullo stesso server. Nello scenario seguente vengono illustrati i pericoli di questo approccio:

Immaginate un server che opera in prossimità della capacità. Dispone di un numero di client con timeout molto brevi, ad esempio cinque secondi. Una perdita temporanea della connettività di rete o della congestione a un router causa un lasso di tempo nelle risposte del server per alcuni secondi. Nelle reti Ethernet questa situazione può essere facilmente causata da un picco di attività su un collegamento condiviso dal server con un altro computer. Il server non è in grado di inviare tutte le risposte prima del timeout di cinque secondi. I client ottengono le chiamate annullate e riprovano immediatamente. Il server non è in grado di riconoscere che le chiamate sono tentativi e li esegue anche. Quindi, anziché eseguire il normale carico di lavoro delle chiamate, vengono eseguite 30-50% più chiamate, a seconda del numero di client che hanno raggiunto il timeout. Se questo supera la capacità e il server non è in grado di rispondere a tutti i client entro cinque secondi, al server viene inviato un altro round di chiamate. I client continuano a riemettere le stesse chiamate e, poiché il server è in overload per l'elaborazione delle chiamate precedenti, non è in grado di rispondere entro il timeout. Una volta risposto, i client hanno raggiunto il timeout, ha emesso una nuova chiamata ed eliminato la risposta. Nel peggiore dei casi, il server non verrà ripristinato fino al riavvio e, a seconda del modello di accesso client, potrebbe non essere ripristinato fino a quando non viene arrestato un numero sufficiente di client.

> [!Note]  
> I timeout delle chiamate funzionano solo sulle sequenze di protocollo http [**\_ \_ TCP**](/windows/desktop/Midl/ncacn-ip-tcp) e [**ncacn \_ http**](/windows/desktop/Midl/ncacn-http) ncacn.

 

 

 