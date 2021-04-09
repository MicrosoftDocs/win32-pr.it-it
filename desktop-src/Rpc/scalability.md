---
title: Scalabilità
description: Scalabilità
ms.assetid: 39327621-b536-4494-9319-9e9d4f534123
keywords:
- Scalabilità
- Remote Procedure Call RPC, procedure consigliate, scalabilità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0728e35d9c9b27494014363c448be9965e39eea7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856737"
---
# <a name="scalability"></a>Scalabilità

Il termine, la scalabilità, viene spesso utilizzato in parte. Per questa sezione viene fornita una doppia definizione:

-   La scalabilità è la capacità di usare completamente la potenza di elaborazione disponibile in un sistema multiprocessore (2, 4, 8, 32 o più processori).
-   La scalabilità è la capacità di servire un numero elevato di client.

Queste due definizioni correlate sono comunemente definite *scalabilità verticale*. Alla fine di questo argomento vengono forniti suggerimenti sulla *scalabilità orizzontale*.

Questo argomento è incentrato esclusivamente sulla scrittura di server scalabili, non di client scalabili, perché i server scalabili sono requisiti più comuni. Questa sezione risolve anche la scalabilità solo nel contesto dei server RPC e RPC. Le procedure consigliate per la scalabilità, ad esempio la riduzione della contesa, l'evitare i frequenti mancati riscontri nella cache nelle posizioni di memoria globale o l'evitare la falsa condivisione non vengono discusse qui

## <a name="rpc-threading-model"></a>Modello di threading RPC

Quando una chiamata RPC viene ricevuta da un server, la routine del server (routine Manager) viene chiamata su un thread fornito da RPC. RPC utilizza un pool di thread adattivo che aumenta e diminuisce man mano che il carico di lavoro fluttua. A partire da Windows 2000, il nucleo del pool di thread RPC è una porta di completamento. La porta di completamento e l'utilizzo da parte di RPC sono ottimizzate per le routine del server con conflitti limitati. Ciò significa che il pool di thread RPC aumenta in modo aggressivo il numero di thread di manutenzione se alcuni vengono bloccati. Opera sulla supposizione che il blocco sia raro e se un thread viene bloccato, si tratta di una condizione temporanea che viene rapidamente risolta. Questo approccio consente l'efficienza per i server con conflitti limitati. Ad esempio, un server RPC di chiamata void che opera su un server 550MHz a otto processori a cui si accede tramite una System Area Network ad alta velocità (SAN) serve oltre 30.000 chiamate void al secondo da oltre 200 client remoti. Rappresenta più di 108 milioni chiamate all'ora.

Il risultato è che il pool di thread aggressivi viene effettivamente visualizzato quando la contesa sul server è elevata. Per illustrare, si supponga di dover usare un server pesante per accedere ai file in modalità remota. Si supponga che il server adotti l'approccio più semplice: legge/scrive semplicemente il file in modo sincrono sul thread sul quale RPC richiama la routine del server. Si supponga inoltre di disporre di un server a quattro processori che serve molti client.

Il server inizierà con cinque thread, che in realtà variano, ma per semplicità vengono usati cinque thread. Quando RPC preleva la prima chiamata RPC, Invia la chiamata alla routine del server e la routine del server emette l'i/O. Raramente manca la cache dei file e quindi si blocca in attesa del risultato. Non appena si blocca, il quinto thread viene rilasciato per prelevare una richiesta e un sesto thread viene creato come hot standby. Supponendo che ogni singola operazione di I/O riscontri la cache e si blocchi per 100 millisecondi (un valore di ora arbitrario) e presupponendo che il server a quattro processori serva circa 20.000 chiamate al secondo (5.000 chiamate per processore), una modellazione semplicistica stima che ogni processore genererà circa 50 thread. Si presuppone che una chiamata che verrà bloccata ogni 2 millisecondi e, dopo 100 millisecondi, il primo thread venga liberato nuovamente, in modo che il pool si stabilizzi a circa 200 thread (50 per processore).

Il comportamento effettivo è più complesso, poiché il numero elevato di thread provocherà cambi di contesto aggiuntivi che rallentano il server e rallentano anche la frequenza di creazione di nuovi thread, ma l'idea di base è chiara. Il numero di thread aumenta rapidamente, perché i thread nel server iniziano a bloccarsi e in attesa di un elemento, ovvero un I/O o l'accesso a una risorsa.

RPC e la porta di completamento che consente di gestire le richieste in ingresso proveranno a mantenere il numero di thread RPC utilizzabili nel server in modo che corrispondano al numero di processori nel computer. Ciò significa che in un server a quattro processori, una volta che un thread torna a RPC, se sono presenti quattro o più thread RPC utilizzabili, il quinto thread non è autorizzato a prelevare una nuova richiesta e si troverà in uno stato di hot standby nel caso in cui uno dei blocchi di thread attualmente utilizzabili. Se il quinto thread è in attesa di un tempo sufficiente come hot standby senza il numero di thread RPC utilizzabili che diminuiscono al di sotto del numero di processori, verrà rilasciato, ovvero, il pool di thread ridurrà.

Immaginate un server con molti thread. Come spiegato in precedenza, un server RPC termina con molti thread, ma solo se i thread si bloccano spesso. In un server in cui i thread si bloccano spesso, un thread che torna a RPC viene presto eliminato dall'elenco hot standby, perché tutti i thread attualmente utilizzabili vengono bloccati e viene fornita una richiesta di elaborazione. Quando un thread si blocca, il dispatcher del thread nel kernel passa il contesto a un altro thread. Questo cambio di contesto usa i cicli della CPU. Il thread successivo eseguirà codice diverso, accederà a diverse strutture di dati e avrà uno stack diverso, il che significa che la percentuale di riscontri nella cache di memoria (le cache L1 e L2) sarà molto inferiore, causando un'esecuzione più lenta. I numerosi thread in esecuzione contemporaneamente aumentano la contesa per le risorse esistenti, ad esempio heap, sezioni critiche nel codice del server e così via. Questo aumenta ulteriormente la contesa come serie di istruzioni sul modulo delle risorse. Se la memoria è insufficiente, la quantità di memoria utilizzata dal numero elevato e crescente di thread provocherà errori di pagina che aumentano ulteriormente la velocità con cui i thread vengono bloccati e comportano la creazione di più thread. A seconda della frequenza con cui si blocca e della quantità di memoria fisica disponibile, è possibile che il server si stabilizzi a un livello inferiore di prestazioni con una frequenza di cambio di contesto elevata o che si verifichi un peggioramento fino al momento in cui si accede solo ripetutamente al disco rigido e al cambio di contesto senza eseguire alcuna operazione effettiva. Questa situazione non verrà mostrata sotto un carico di lavoro leggero, ovviamente, ma un carico di lavoro pesante ridurrà rapidamente il problema alla superficie.

Come è possibile evitare questo problema? Se si prevede che i thread si blocchino, dichiarano chiamate come asincrone e una volta che la richiesta entra nella routine del server, accodarla a un pool di thread di lavoro che usano le funzionalità asincrone del sistema di I/o e/o RPC. Se il server è a sua volta, le chiamate RPC le rendono asincrone e assicurano che la coda non diventi troppo grande. Se la routine del server esegue l'I/O dei file, utilizzare l'I/O di file asincrono per accodare più richieste al sistema di I/O e fare in modo che solo pochi thread vengano accodati e prelevino i risultati. Se la routine del server sta eseguendo l'I/O di rete, utilizzare di nuovo le funzionalità asincrone del sistema per emettere le richieste e prelevare le risposte in modo asincrono e utilizzare il minor numero di thread possibile. Quando viene eseguita l'operazione di i/O o la chiamata RPC eseguita dal server è stata completata, completare la chiamata RPC asincrona che ha recapitato la richiesta. Ciò consentirà al server di essere eseguito con il minor numero di thread possibile, aumentando così le prestazioni e il numero di client che un server è in grado di gestire.

## <a name="scale-out"></a>Aumento del numero di istanze

È possibile configurare RPC per l'utilizzo di bilanciamento carico di rete (NLB) se NLB è configurato in modo tale che tutte le richieste provenienti da un determinato indirizzo client vadano allo stesso server. Poiché ogni client RPC apre un pool di connessioni (per altre informazioni, vedere [RPC e la rete](rpc-and-the-network.md)), è essenziale che tutte le connessioni dal pool del client specificato si trovino nello stesso computer server. Fino a quando questa condizione viene soddisfatta, è possibile configurare un cluster NLB in modo che funzioni come un server RPC di grandi dimensioni con scalabilità potenzialmente eccellente.

 

 




