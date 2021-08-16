---
description: Miglioramento delle prestazioni con il pooling di oggetti
ms.assetid: 7a8a38d8-6549-4686-a298-f3b427b380e3
title: Miglioramento delle prestazioni con il pooling di oggetti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68ce6a86e76f7a97395973cc9cab4c4e9e81177f4312a389c2b01ec2d88eb7a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118547848"
---
# <a name="improving-performance-with-object-pooling"></a>Miglioramento delle prestazioni con il pooling di oggetti

Il pool di oggetti può essere estremamente efficace in determinate circostanze, con un notevole aumento delle prestazioni. L'idea generale per riutilizzare al meglio gli oggetti è quella di creare un pool del maggior numero possibile di risorse, di effettuare il factoring dell'inizializzazione dal lavoro effettivo eseguito e quindi di personalizzare a livello amministrativo le caratteristiche del pool in base all'hardware effettivo in fase di distribuzione. Ciò significa che è necessario procedere in base alla procedura seguente:

1.  Scrivere l'oggetto in modo da eseguire un'inizializzazione dispendiosa e l'acquisizione delle risorse che viene eseguita per qualsiasi client come prerequisito per eseguire il lavoro effettivo per conto del client. Scrivere costruttori di oggetti pesanti nel pool il maggior numero possibile di risorse in modo che siano mantenute dall'oggetto e immediatamente disponibili quando i client ottengono un oggetto dal pool.
2.  Configurare a livello amministrativo il pool per ottenere il miglior equilibrio tra le risorse hardware disponibili, in genere scambiando la memoria dedicata alla gestione di un pool di una determinata dimensione in cambio di un accesso client più rapido e l'uso degli oggetti. A un certo punto, il pooling otterrà un calo dei risultati ed è possibile ottenere prestazioni sufficienti limitando al tempo stesso il possibile utilizzo delle risorse da parte di un determinato componente.

## <a name="doing-actual-work-or-acquiring-resources"></a>Esecuzione di lavoro effettivo o acquisizione di risorse

Se si dispone di un componente che i client useranno brevemente e in rapida successione, in cui una parte significativa del tempo di utilizzo degli oggetti viene impiegato per l'acquisizione di risorse o l'inizializzazione prima di eseguire operazioni specifiche per il client, è probabile che la scrittura del componente per usare il pool di oggetti sia una grande opportunità per l'utente.

È possibile scrivere il componente in modo che nel costruttore dell'oggetto sia possibile eseguire la maggior parte del lavoro dispendioso in termini di tempo che è uniforme per tutti i client, ovvero l'acquisizione di una o più connessioni, l'esecuzione di script, il recupero dei dati di inizializzazione da file o attraverso una rete e così via. Ciò ha l'effetto di creare un pool per ogni risorsa di questo tipo. Si sta combinando la combinazione di risorse e stato generico necessario per eseguire alcune operazioni.

In questo caso, quando i client ottengono un oggetto dal pool, hanno tali risorse immediatamente disponibili. In genere, useranno l'oggetto per eseguire una piccola unità di lavoro, eseguire il push o il pull dei dati e quindi l'oggetto chiamerà [**IObjectContext::SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) o [**IObjectContext::SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort) e restituirà . Con modelli di uso rapido come questo, il pooling offre ottimi vantaggi in termini di prestazioni. È possibile sfruttare appieno la semplicità del modello di programmazione automatica delle transazioni senza stato, ma ottenere prestazioni pari a quelli dei componenti con stato tradizionali.

Tuttavia, se i client usano un oggetto per molto tempo ogni volta che lo chiamano, il pooling sarà meno sensato. Il vantaggio della velocità che si ottiene è marginale in quanto il tempo di utilizzo aumenta rispetto al tempo di inizializzazione. Si ottengono resi in diminuzione che potrebbero non giustificare il costo della memoria necessaria per contenere un pool di oggetti attivi.

## <a name="sharing-cost-across-multiple-clients"></a>Condivisione dei costi tra più client

Una variazione nel factoring dell'inizializzazione è che è possibile usare il pooling per ammortizzare statisticamente il costo dell'acquisizione di risorse costose. Se si prende l'acquisizione o l'inizializzazione una sola volta e quindi si riutilizza l'oggetto, si condivide tale costo tra tutti i client che usano l'oggetto durante la sua durata. Un tempo di costruzione intenso viene incorso una sola volta per ogni oggetto.

## <a name="preallocating-objects"></a>Preallocazione di oggetti

Se si specifica una dimensione minima del pool diversa da zero, il numero minimo di oggetti verrà creato e in pool all'avvio dell'applicazione, pronto per tutti i client che chiamano l'applicazione.

## <a name="governing-resource-use-with-pool-management"></a>Governance dell'uso delle risorse con la gestione dei pool

È possibile usare le dimensioni massime del pool per gestire con precisione il modo in cui si usano le risorse. Ad esempio, se si dispone di una licenza per un determinato numero di connessioni di database, è possibile controllare il numero di connessioni aperte in qualsiasi momento.

Quando si prendono in considerazione i modelli di utilizzo del client, le caratteristiche di utilizzo degli oggetti e le risorse fisiche, ad esempio la memoria e le connessioni, è probabile che si trovi un punto di equilibrio ottimale quando si esegue l'ottimizzazione delle prestazioni. Il pooling di oggetti restituirà risultati in diminuzione dopo un determinato punto. È possibile determinare il livello di prestazioni necessario e bilanciarlo con le risorse necessarie per raggiungerlo.

Per facilitare l'ottimizzazione delle prestazioni quando si configura il pool di oggetti, è possibile monitorare le statistiche degli oggetti per i componenti di un'applicazione. Per informazioni dettagliate, vedere [Monitoraggio delle statistiche degli oggetti.](monitoring-object-statistics.md)

## <a name="improve-performance-of-jit-activated-components"></a>Migliorare le prestazioni dei JIT-Activated componenti

Il pool di oggetti funziona molto bene con [il servizio di attivazione JUST-In-Time COM+.](com--just-in-time-activation.md) Il pooling di oggetti attivati tramite JIT consente di velocizzare la riattivazione degli oggetti. È possibile ottenere i vantaggi derivanti dal mantenere aperto il canale tramite l'attivazione JIT, attenuando al tempo stesso il costo della riattivazione. In questo caso è possibile usare il pooling per determinare la quantità di memoria da allocare agli oggetti con riferimenti attivi.

È molto probabile che i componenti attivati da JIT siano in pool quando sono transazionali. Il pool di oggetti è ottimizzato per gestire i componenti transazionali. Per altre informazioni, vedere [Pooling Transactional Objects](pooling-transactional-objects.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Stringhe del costruttore di oggetti COM+](com--object-constructor-strings.md)
</dt> <dt>

[Controllo della durata e dello stato degli oggetti](controlling-object-lifetime-and-state.md)
</dt> <dt>

[Funzionamento del pool di oggetti](how-object-pooling-works.md)
</dt> <dt>

[Pooling di oggetti transazionali](pooling-transactional-objects.md)
</dt> <dt>

[Requisiti per gli oggetti in pool](requirements-for-poolable-objects.md)
</dt> </dl>

 

 



