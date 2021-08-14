---
title: Gestione della durata degli oggetti tramite il conteggio dei riferimenti
description: Gestione della durata degli oggetti tramite il conteggio dei riferimenti
ms.assetid: 7f9da5a9-0435-431c-8f90-56e2e489c431
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 292f2c75352eef5680eb9a4d8367f76f88c19138dd834b71068740bee18f2315
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118310561"
---
# <a name="managing-object-lifetimes-through-reference-counting"></a>Gestione della durata degli oggetti tramite il conteggio dei riferimenti

Nei sistemi a oggetti tradizionali, il ciclo di vita degli oggetti, ovvero i problemi relativi alla creazione e all'eliminazione di oggetti, viene gestito in modo implicito dal linguaggio (o dalla fase di esecuzione del linguaggio) o in modo esplicito dai programmatori dell'applicazione.

In un sistema in evoluzione e costruito in modo decente costituito da componenti riutilizzati, non è più vero che qualsiasi client, o anche qualsiasi programmatore, sa sempre come gestire la durata di un componente. Per un client con i privilegi di sicurezza necessari, è ancora relativamente semplice creare oggetti tramite una semplice richiesta, ma l'eliminazione di oggetti è un'altra questione completamente diversa. Non è necessariamente chiaro quando un oggetto non è più necessario e deve essere eliminato. I lettori che hanno familiarità con gli ambienti di programmazione garbage collection, ad esempio Java, possono non essere d'accordo. Tuttavia, gli oggetti Java non si estendono ai limiti del computer o del processo e pertanto l'operazione di Garbage Collection è limitata agli oggetti che si trova all'interno di uno spazio a processo singolo. Java impone inoltre l'uso di un singolo linguaggio di programmazione. Anche quando il client originale viene eseguito con l'oggetto , non può semplicemente arrestare l'oggetto, perché alcuni altri client o client potrebbero comunque avere un riferimento ad esso.

Un modo per garantire che un oggetto non sia più necessario è dipendere interamente da un canale di comunicazione sottostante per informare il sistema quando tutte le connessioni a un oggetto tra processi o tra canali sono scomparse. Tuttavia, gli schemi che usano questo metodo sono inaccettabili per diversi motivi. Un problema è che potrebbe richiedere una differenza sostanziale tra il modello di programmazione tra processi/reti e il modello di programmazione a processo singolo. Nel modello di programmazione tra processi/reti, il sistema di comunicazione fornisce gli hook necessari per la gestione della durata degli oggetti, mentre nel modello di programmazione a processo singolo gli oggetti sono connessi direttamente senza alcun canale di comunicazione interviene. Un altro problema è che questo schema potrebbe anche comportare un livello di software fornito dal sistema che interferirebbe con le prestazioni dei componenti nel caso in-process. Inoltre, un meccanismo basato sul monitoraggio esplicito non tende a raggiungere molte migliaia o milioni di oggetti.

COM offre un approccio scalabile e distribuito a questo set di problemi. I client possono indicare a un oggetto quando lo usano e al termine, mentre gli oggetti si eliminano quando non sono più necessari. Questo approccio impone a tutti gli oggetti di contare i riferimenti a se stessi. I linguaggi di programmazione come Java, che hanno intrinsecamente i propri schemi di gestione della durata, ad esempio Garbage Collection, possono usare il conteggio dei riferimenti com per implementare e usare gli oggetti COM internamente, consentendo al programmatore di evitare di gestirlo.

Proprio come un'applicazione deve liberare memoria allocata quando la memoria non è più in uso, un client di un oggetto è responsabile di liberare i riferimenti all'oggetto quando tale oggetto non è più necessario. In un sistema orientato a oggetti, il client può eseguire questa operazione solo fornendo all'oggetto un'istruzione per liberarsi.

È importante che un oggetto venga deallocato quando non viene più usato. La difficoltà consiste nel determinare quando è appropriato deallocare un oggetto. Questo è facile con le variabili automatiche (quelle allocate nello stack): non possono essere usate all'esterno del blocco in cui vengono dichiarate, quindi il compilatore le dealloca quando viene raggiunta la fine del blocco. Per gli oggetti COM, allocati dinamicamente, è ai client di un oggetto decidere quando non devono più usare l'oggetto, in particolare gli oggetti locali o remoti che potrebbero essere in uso da più client contemporaneamente. L'oggetto deve attendere il completamento di tutti i client prima di liberarsi. Poiché gli oggetti COM vengono manipolati tramite puntatori a interfaccia e possono essere usati da oggetti in processi diversi o in altri computer, il sistema non può tenere traccia dei client di un oggetto.

Il metodo COM per determinare quando è appropriato deallocare un oggetto è il conteggio manuale dei riferimenti. Ogni oggetto mantiene un conteggio dei riferimenti che tiene traccia del numero di client connessi, ad esempio il numero di puntatori presenti in qualsiasi interfaccia in qualsiasi client.

Per altre informazioni, vedere i seguenti argomenti:

-   [Implementazione del conteggio dei riferimenti](implementing-reference-counting.md)
-   [Regole per la gestione dei conteggi dei riferimenti](rules-for-managing-reference-counts.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso e implementazione di IUnknown](using-and-implementing-iunknown.md)
</dt> </dl>

 

 




