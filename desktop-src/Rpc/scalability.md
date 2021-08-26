---
title: Scalabilità
description: Scalabilità
ms.assetid: 39327621-b536-4494-9319-9e9d4f534123
keywords:
- Scalabilità
- RPC Remote Procedure Call, procedure consigliate, scalabilità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec2a004a5ce3adb0f27e2e31071cac69fc1c34bfc650c618dcf39b3c8ebc954f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120018061"
---
# <a name="scalability"></a>Scalabilità

Il termine scalabilità viene spesso usato in modo improprio. Per questa sezione viene fornita una definizione doppia:

-   La scalabilità è la possibilità di sfruttare appieno la potenza di elaborazione disponibile in un sistema multiprocessore (2, 4, 8, 32 o più processori).
-   La scalabilità è la possibilità di gestire un numero elevato di client.

Queste due definizioni correlate sono comunemente definite *scalabilità verticale.* Alla fine di questo argomento vengono forniti suggerimenti sulla *scalabilità orizzontale di*.

Questa discussione è incentrata esclusivamente sulla scrittura di server scalabili, non di client scalabili, perché i server scalabili sono requisiti più comuni. In questa sezione viene inoltre trattata la scalabilità solo nel contesto dei server RPC e RPC. Le procedure consigliate per la scalabilità, ad esempio ridurre i conflitti, evitare frequenti mancati riscontri nella cache nelle posizioni di memoria globale o evitare false condivisioni, non sono descritte qui.

## <a name="rpc-threading-model"></a>Modello di threading RPC

Quando un server riceve una chiamata RPC, la routine del server (routine di gestione) viene chiamata su un thread fornito da RPC. RPC usa un pool di thread adattivi che aumenta e diminuisce con la fluttuazione del carico di lavoro. A partire Windows 2000, il nucleo del pool di thread RPC è una porta di completamento. La porta di completamento e il relativo utilizzo da rpc sono ottimizzati per le routine del server da zero a a bassa contentione. Ciò significa che il pool di thread RPC aumenta in modo aggressivo il numero di thread di manutenzione se alcuni vengono bloccati. Opera sulla presunzione che il blocco è raro e, se un thread viene bloccato, si tratta di una condizione temporanea che viene risolta rapidamente. Questo approccio consente l'efficienza per i server a bassa contentione. Ad esempio, un server RPC void call che opera su un server a otto processori a 550 MHz a cui si accede tramite una rete san (System Area Network) ad alta velocità serve oltre 30.000 chiamate void al secondo da oltre 200 client remoti. Rappresenta più di 108 milioni di chiamate all'ora.

Il risultato è che il pool di thread aggressivo diventa effettivamente insodduttiva quando la contentione nel server è elevata. A titolo di esempio, si immagini un server di lavoro pesante usato per accedere in remoto ai file. Si supponga che il server adotti l'approccio più semplice: legge/scrive semplicemente il file in modo sincrono nel thread in cui tale RPC richiama la routine del server. Si supponga inoltre di avere un server a quattro processori che serve molti client.

Il server verrà avviato con cinque thread (varia effettivamente, ma cinque thread vengono usati per semplicità). Quando RPC preleva la prima chiamata RPC, invia la chiamata alla routine del server e la routine del server emette l'I/O. Raramente manca la cache dei file e quindi si blocca in attesa del risultato. Non appena si blocca, il quinto thread viene rilasciato per prelevare una richiesta e viene creato un sesto thread come hot standby. Supponendo che ogni decima operazione di I/O non rilevi la cache e si blocchi per 100 millisecondi (un valore di tempo arbitrario) e supponendo che il server a quattro processori rilasci circa 20.000 chiamate al secondo (5.000 chiamate per processore), una modellazione semplicistica prevede che ogni processore genererà circa 50 thread. Si presuppone che una chiamata che si blocca ogni 2 millisecondi e che dopo 100 millisecondi il primo thread venga liberato nuovamente in modo che il pool si stabilizzi a circa 200 thread (50 per processore).

Il comportamento effettivo è più complicato, perché l'elevato numero di thread causerà commutatori di contesto aggiuntivi che rallentano il server e rallentano anche la velocità di creazione di nuovi thread, ma l'idea di base è chiara. Il numero di thread si alza rapidamente quando i thread nel server iniziano a bloccarsi e in attesa di un elemento (si tratta di un I/O o di accesso a una risorsa).

RPC e la porta di completamento che gestisce le richieste in ingresso tenteranno di mantenere il numero di thread RPC utilizzabili nel server in modo che sia uguale al numero di processori nel computer. Ciò significa che in un server a quattro processori, quando un thread torna a RPC, se sono presenti quattro o più thread RPC utilizzabili, il quinto thread non è autorizzato a prelevare una nuova richiesta e si trova invece in uno stato hot standby nel caso in cui uno dei blocchi di thread attualmente utilizzabili. Se il quinto thread attende abbastanza a lungo come hot standby senza il numero di thread RPC utilizzabili che screndono al di sotto del numero di processori, verrà rilasciato, in altri modo il pool di thread diminuisce.

Imagine un server con molti thread. Come spiegato in precedenza, un server RPC ha molti thread, ma solo se i thread si bloccano spesso. In un server in cui i thread spesso si bloccano, un thread che torna a RPC viene presto estratto dall'elenco di hot standby, perché tutti i thread attualmente utilizzabili si bloccano e viene inviata una richiesta di elaborazione. Quando un thread si blocca, il dispatcher di thread nel kernel passa il contesto a un altro thread. Questo cambio di contesto usa da solo i cicli della CPU. Il thread successivo eseguirà codice diverso, accederà a strutture di dati diverse e avrà uno stack diverso, il che significa che la frequenza di riscontri nella cache di memoria (le cache L1 e L2) sarà molto inferiore, con conseguente rallentamento dell'esecuzione. I numerosi thread in esecuzione simultaneamente aumentano i problemi di risorse esistenti, ad esempio heap, sezioni critiche nel codice del server e così via. Questo aumenta ulteriormente il numero di richieste di risorse. Se la memoria è bassa, l'utilizzo elevato della memoria da parte del numero elevato e crescente di thread causerà errori di pagina, che aumentano ulteriormente la frequenza con cui i thread si bloccano e causano la creazione di un numero ancora maggiore di thread. A seconda della frequenza con cui si blocca e della quantità di memoria fisica disponibile, il server può stabilizzarsi a un livello inferiore di prestazioni con una frequenza di cambio di contesto elevata oppure può peggiorare fino al punto in cui accede solo ripetutamente al disco rigido e al cambio di contesto senza eseguire alcuna operazione effettiva. Questa situazione non verrà visualizzata in condizioni di carico di lavoro leggero, ma un carico di lavoro elevato porta rapidamente il problema in superficie.

Come è possibile evitare questo problema? Se si prevede che i thread si blocchino, dichiarare le chiamate come asincrone e una volta che la richiesta entra nella routine del server, accodarla a un pool di thread di lavoro che usano le funzionalità asincrone del sistema di I/O e/o RPC. Se il server esegue a sua volta chiamate RPC, tali chiamate vengono effettuate in modo asincrono e assicurarsi che le dimensioni della coda non siano troppo grandi. Se la routine del server esegue l'I/O dei file, usare l'I/O di file asincrono per accodare più richieste al sistema di I/O e fare in modo che solo pochi thread le accodino e prelevino i risultati. Se la routine del server esegue l'I/O di rete, usare anche in questo caso le funzionalità asincrone del sistema per inviare le richieste e prelevare le risposte in modo asincrono e usare il maggior numero possibile di thread. Al termine dell'I/O o al termine della chiamata RPC eseguita dal server, completare la chiamata RPC asincrona che ha recapitato la richiesta. In questo modo il server verrà eseguito con il numero di thread più limitato possibile, con un aumento delle prestazioni e del numero di client che un server può usare.

## <a name="scale-out"></a>Aumento del numero di istanze

Rpc può essere configurato per l'utilizzo con Bilanciamento carico di rete se Bilanciamento carico di rete è configurato in modo che tutte le richieste provenienti da un determinato indirizzo client siano indirizzate allo stesso server. Poiché ogni client RPC apre un pool di connessioni (per altre informazioni, vedere [RPC](rpc-and-the-network.md)e rete), è essenziale che tutte le connessioni dal pool del client specificato finitino nello stesso computer server. Se questa condizione viene soddisfatta, un cluster di Bilanciamento carico di rete può essere configurato per funzionare come un server RPC di grandi dimensioni con una scalabilità potenzialmente eccellente.

 

 




