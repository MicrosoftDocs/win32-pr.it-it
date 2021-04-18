---
description: Miglioramento delle prestazioni con il pool di oggetti
ms.assetid: 7a8a38d8-6549-4686-a298-f3b427b380e3
title: Miglioramento delle prestazioni con il pool di oggetti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 398b9140080d3a439293b5152b4da7251978e800
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304947"
---
# <a name="improving-performance-with-object-pooling"></a>Miglioramento delle prestazioni con il pool di oggetti

Il pool di oggetti può essere estremamente efficace in determinate circostanze, ottenendo un aumento sostanziale delle prestazioni. L'idea generale di riutilizzare gli oggetti per sfruttare al meglio il maggior numero possibile consiste nel raggruppare il maggior numero possibile di risorse, escludendo l'inizializzazione dal lavoro effettivo eseguito e quindi adattando in modo amministrativo le caratteristiche del pool all'hardware effettivo in fase di distribuzione. Ovvero, è necessario procedere in base ai passaggi seguenti:

1.  Scrivere l'oggetto in modo da fattorizzare l'inizializzazione costosa e l'acquisizione delle risorse eseguita per qualsiasi client come prerequisito per eseguire il lavoro effettivo per conto del client. Scrivere i costruttori di oggetti pesanti nel pool del maggior numero possibile di risorse, in modo che vengano mantenuti dall'oggetto e immediatamente disponibili quando i client ottengono un oggetto dal pool.
2.  Configurare il pool in modo amministrativo per ottenere il migliore equilibrio nelle risorse hardware disponibili, in genere negoziando la memoria dedicata alla gestione di un pool di una determinata dimensione in Exchange per un accesso client più rapido e l'utilizzo di oggetti. A un certo punto, i pool otterranno ritorni ridotti ed è possibile ottenere prestazioni soddisfacenti, limitando il possibile utilizzo delle risorse da parte di un particolare componente.

## <a name="doing-actual-work-or-acquiring-resources"></a>Lavoro effettivo o acquisizione delle risorse

Se si dispone di un componente che i client utilizzeranno brevemente e in rapida successione, in cui una parte significativa del tempo di utilizzo dell'oggetto viene impiegata per l'acquisizione di risorse o l'inizializzazione prima dell'esecuzione di operazioni specifiche per il client, è probabile che la scrittura del componente per l'utilizzo del pool di oggetti sia una grande vittoria.

È possibile scrivere il componente in modo che nel costruttore dell'oggetto venga eseguita la maggior parte del lavoro dispendioso in termini di tempo che è uniforme per tutti i client, acquisendo una o più connessioni, eseguendo script, recuperando i dati di inizializzazione dai file o attraverso una rete e così via. Questo ha l'effetto di raggruppare ogni risorsa. È necessario raggruppare la combinazione di risorse e lo stato generico necessario per eseguire alcune operazioni.

In questa circostanza, quando i client ottengono un oggetto dal pool, queste risorse sono immediatamente disponibili. In genere, useranno l'oggetto per eseguire una piccola unità di lavoro, il push o il pull dei dati, quindi l'oggetto chiamerà [**IObjectContext:: Tocomplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) o [**IObjectContext:: SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort) e return. Con i modelli di utilizzo rapidi come questo, il pool produce vantaggi ottimali in merito alle prestazioni. È possibile sfruttare appieno la semplicità del modello di programmazione automatica delle transazioni senza stato, ottenendo al tempo stesso prestazioni analoghe ai tradizionali componenti con stato.

Tuttavia, se i client usano un oggetto per un lungo periodo di tempo ogni volta che la chiamano, i pool avranno un significato minore. Il vantaggio di velocità che si ottiene è marginale perché il tempo di utilizzo aumenta rispetto al tempo di inizializzazione. Vengono restituiti ritorni che potrebbero non giustificare il costo della memoria necessaria per mantenere un pool di oggetti attivi.

## <a name="sharing-cost-across-multiple-clients"></a>Condivisione dei costi tra più client

Una variante dell'inizializzazione del factoring è che è possibile usare il pool per ammortizzare statisticamente il costo di acquisizione di risorse costose. Se si esegue l'acquisizione o l'inizializzazione una volta e quindi si riutilizza l'oggetto, si condivide tale costo tra tutti i client che utilizzano l'oggetto durante la relativa durata. Il tempo di costruzione elevato viene eseguito una sola volta per oggetto.

## <a name="preallocating-objects"></a>Preallocazione di oggetti

Se si specifica una dimensione del pool minima diversa da zero, il numero minimo di oggetti verrà creato e in pool all'avvio dell'applicazione, pronto per tutti i client che chiamano l'applicazione.

## <a name="governing-resource-use-with-pool-management"></a>Governare l'uso delle risorse con la gestione del pool

È possibile utilizzare le dimensioni massime del pool per governare con precisione la modalità di utilizzo delle risorse. Ad esempio, se si dispone di una licenza per un certo numero di connessioni di database, è possibile controllare il numero di connessioni aperte in qualsiasi momento.

Quando si prendono in considerazione i modelli di utilizzo dei client, le caratteristiche di utilizzo degli oggetti e le risorse fisiche, ad esempio la memoria e le connessioni, è probabile che si trovi un punto di bilanciamento ottimale quando si esegue l'ottimizzazione delle prestazioni. Gli oggetti di pooling restituiranno risultati decrescenti dopo un determinato punto. È possibile determinare il livello di prestazioni necessario e bilanciarlo rispetto alle risorse necessarie per ottenerlo.

Per semplificare l'ottimizzazione delle prestazioni quando si configura il pool di oggetti, è possibile monitorare le statistiche degli oggetti per i componenti di un'applicazione. Per informazioni dettagliate, vedere [monitoraggio delle statistiche degli oggetti](monitoring-object-statistics.md).

## <a name="improve-performance-of-jit-activated-components"></a>Migliorare le prestazioni dei componenti di JIT-Activated

Il pool di oggetti funziona molto bene con il servizio di [attivazione JIT (just-in-Time) com+](com--just-in-time-activation.md) . Raggruppando gli oggetti che vengono attivati tramite JIT, è possibile velocizzare la riattivazione degli oggetti. Si ottengono i vantaggi derivanti dal mantenimento del canale aperto dall'attivazione JIT, riducendo al tempo stesso il costo della riattivazione. In questo caso è possibile usare il pool per controllare la quantità di memoria da allocare a oggetti con riferimenti attivi.

È probabile che si stiano raggruppando i componenti attivati tramite JIT quando sono transazionali. Il pool di oggetti è ottimizzato per la gestione dei componenti transazionali. Per ulteriori informazioni, vedere la pagina relativa al [pool di oggetti transazionali](pooling-transactional-objects.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Stringhe del costruttore di oggetti COM+](com--object-constructor-strings.md)
</dt> <dt>

[Controllo della durata e dello stato degli oggetti](controlling-object-lifetime-and-state.md)
</dt> <dt>

[Funzionamento del pool di oggetti](how-object-pooling-works.md)
</dt> <dt>

[Raggruppamento di oggetti transazionali](pooling-transactional-objects.md)
</dt> <dt>

[Requisiti per gli oggetti pool](requirements-for-poolable-objects.md)
</dt> </dl>

 

 



