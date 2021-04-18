---
title: Gestione della durata degli oggetti tramite il conteggio dei riferimenti
description: Gestione della durata degli oggetti tramite il conteggio dei riferimenti
ms.assetid: 7f9da5a9-0435-431c-8f90-56e2e489c431
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7aac184baea9198721e6cdf9c0444a8c6431db08
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/17/2020
ms.locfileid: "106299540"
---
# <a name="managing-object-lifetimes-through-reference-counting"></a>Gestione della durata degli oggetti tramite il conteggio dei riferimenti

Nei sistemi a oggetti tradizionali, il ciclo di vita degli oggetti, ovvero i problemi relativi alla creazione e all'eliminazione di oggetti, viene gestito in modo implicito dalla lingua (o dal tempo di esecuzione del linguaggio) o in modo esplicito dai programmatori di applicazioni.

In un sistema in continua evoluzione, costruito in modo decentrato, costituito da componenti riutilizzati, non è più vero che qualsiasi client, o anche un programmatore, sempre "sa" come gestire la durata di un componente. Per un client con i privilegi di sicurezza corretti, è ancora relativamente semplice creare oggetti tramite una semplice richiesta, ma l'eliminazione degli oggetti è interamente un altro aspetto. Non è necessariamente chiaro quando un oggetto non è più necessario e deve essere eliminato. I lettori che hanno familiarità con gli ambienti di programmazione sottoposti a Garbage Collection, ad esempio Java, potrebbero non essere d'accordo. gli oggetti Java, tuttavia, non si estendono sul computer o persino i limiti del processo e pertanto la Garbage Collection è limitata agli oggetti che risiedono in uno spazio a processo Inoltre, Java impone l'uso di un singolo linguaggio di programmazione. Anche quando il client originale viene eseguito con l'oggetto, non può semplicemente arrestare l'oggetto, perché è possibile che altri client o client abbiano ancora un riferimento a tale oggetto.

Un modo per garantire che un oggetto non è più necessario dipende interamente da un canale di comunicazione sottostante per informare il sistema quando tutte le connessioni a un oggetto tra processi o tra canali sono scomparse. Tuttavia, gli schemi che utilizzano questo metodo sono inaccettabili per diversi motivi. Un problema consiste nel fatto che potrebbe essere necessaria una differenza sostanziale tra il modello di programmazione tra processi e tra più reti e il modello di programmazione a processo singolo. Nel modello di programmazione tra più processi e tra più reti, il sistema di comunicazione fornirebbe gli hook necessari per la gestione della durata degli oggetti, mentre nel modello di programmazione a processo singolo gli oggetti vengono connessi direttamente senza alcun canale di comunicazione corrispondente. Un altro problema è che questo schema può comportare anche un livello di software fornito dal sistema che interferisce con le prestazioni dei componenti nel caso in-process. Inoltre, un meccanismo basato sul monitoraggio esplicito non tenderebbe a ridimensionarsi verso molte migliaia o milioni di oggetti.

COM offre un approccio scalabile e distribuito a questo set di problemi. I client indicano un oggetto quando lo usano e quando vengono eseguiti e gli oggetti vengono eliminati quando non sono più necessari. Questo approccio impone che tutti gli oggetti conteggino i riferimenti a se stessi. I linguaggi di programmazione, ad esempio Java, che hanno intrinsecamente i propri schemi di gestione della durata, ad esempio Garbage Collection, possono utilizzare il conteggio dei riferimenti di COM per implementare e utilizzare internamente gli oggetti COM, consentendo al programmatore di evitare di gestirlo.

Proprio come un'applicazione deve liberare memoria, quando l'oggetto non è più in uso, un client di un oggetto è responsabile di liberare i relativi riferimenti all'oggetto quando tale oggetto non è più necessario. In un sistema orientato a oggetti, il client può eseguire questa operazione solo assegnando all'oggetto un'istruzione per liberarsi.

È importante deallocare un oggetto quando non è più usato. La difficoltà consiste nel determinare quando è appropriato deallocare un oggetto. Questa operazione è facile con le variabili automatiche (quelle allocate nello stack), che non possono essere usate all'esterno del blocco in cui sono dichiarate, quindi il compilatore le dealloca quando viene raggiunta la fine del blocco. Per gli oggetti COM, che vengono allocati dinamicamente, spetta ai client di un oggetto decidere quando non è più necessario utilizzare l'oggetto, in particolare oggetti locali o remoti che potrebbero essere utilizzati da più client nello stesso momento. L'oggetto deve attendere il completamento di tutti i client prima che venga liberato. Poiché gli oggetti COM vengono modificati tramite puntatori di interfaccia e possono essere usati da oggetti in processi diversi o in altri computer, il sistema non può tenere traccia dei client di un oggetto.

Il metodo COM per determinare quando è appropriato deallocare un oggetto è il conteggio manuale dei riferimenti. Ogni oggetto mantiene un conteggio dei riferimenti che tiene traccia del numero di client connessi, ovvero il numero di puntatori a una qualsiasi delle sue interfacce in qualsiasi client.

Per altre informazioni, vedere i seguenti argomenti:

-   [Implementazione del conteggio dei riferimenti](implementing-reference-counting.md)
-   [Regole per la gestione dei conteggi dei riferimenti](rules-for-managing-reference-counts.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso e implementazione di IUnknown](using-and-implementing-iunknown.md)
</dt> </dl>

 

 




