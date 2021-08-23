---
description: Il riciclo delle applicazioni può aumentare significativamente la stabilità complessiva delle applicazioni COM+, offrendo una rapida correzione per i problemi noti e contribuendo alla protezione da quelli imprevisti.
ms.assetid: bf98318b-4d87-44cc-85a1-68faf5547e06
title: Concetti relativi al riciclo delle applicazioni COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba6a635487427fce3f17203f11426261996348a5e4057ab8bceebcae552d51bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129263"
---
# <a name="com-application-recycling-concepts"></a>Concetti relativi al riciclo delle applicazioni COM+

Il riciclo delle applicazioni può aumentare significativamente la stabilità complessiva delle applicazioni COM+, offrendo una rapida correzione per i problemi noti e contribuendo alla protezione da quelli imprevisti. Ad esempio, le prestazioni dell'applicazione possono peggiorare nel tempo a causa di problemi quali perdite di memoria, utilizzo non ascalabile delle risorse e errori del processo. COM+ fornisce il riciclo delle applicazioni come soluzione a questi problemi. È possibile usare il riciclo delle applicazioni per arrestare automaticamente un processo e riavviarlo, reinizializzando un processo non riuscito e riallocando la memoria utilizzata.

Il riciclo delle applicazioni funziona creando un duplicato del processo Dllhost associato a un'applicazione. Questo processo Dllhost duplicato consente di elaborare tutte le richieste di oggetti future, lasciando il vecchio Dllhost per completare la manutenzione delle richieste di oggetti rimanenti. Il processo Dllhost precedente viene arrestato quando rileva il rilascio di tutti i riferimenti esterni agli oggetti nel processo o quando viene raggiunto il valore di timeout della scadenza. Grazie a questo comportamento, il riciclo delle applicazioni garantisce che un'applicazione client non si verifichi un'interruzione del servizio.

> [!Note]  
> Non è possibile riciclare un'applicazione COM+ configurata per l'esecuzione come Windows servizio. Inoltre, le applicazioni di libreria hanno le proprietà di riciclo e pooling del processo host.

 

È possibile configurare il riciclo delle applicazioni a livello amministrativo, tramite lo strumento amministrativo Servizi componenti o a livello di codice, tramite l'SDK amministrativo COM+. È possibile riciclare i processi in base a diversi criteri, determinati dalle proprietà seguenti di un oggetto [**COMAdminCatalogObject**](comadmincatalogobject.md) nella [**raccolta Applications:**](applications.md)

-   **RecycleLifetimeLimit.** Numero massimo di minuti di esecuzione di un processo prima che venga riciclato. L'intervallo valido è compreso tra 0 e 30.240 minuti (21 giorni). Il numero predefinito di minuti è 0, che indica che il processo non verrà riciclato dal raggiungimento di un limite di durata.
-   **RecycleMemoryLimit.** Quantità massima di utilizzo della memoria del processo (in kilobyte) prima del riciclo del processo. Se l'utilizzo della memoria del processo supera il numero specificato per più di un minuto, il processo viene riciclato. L'intervallo valido è compreso tra 0 e 1.048.576 KB. La quantità predefinita di utilizzo della memoria è 0 KB, che indica che il processo non verrà riciclato dal raggiungimento di un limite di memoria.
-   **RecycleCallLimit.** Numero massimo di chiamate che gli oggetti applicazione possono accettare prima di riciclare il processo. L'intervallo valido è compreso tra 0 e 1.048.576 chiamate. Il numero predefinito di chiamate è 0, che indica che il processo non verrà riciclato dal raggiungimento di un limite di chiamate.
-   **RecycleActivationLimit.** Numero massimo di attivazioni di oggetti applicazione da accettare prima del riciclo del processo. L'intervallo valido è compreso tra 0 e 1.048.576 attivazioni. Il numero predefinito di attivazioni è 0, che indica che il processo non verrà riciclato dal raggiungimento di un limite di attivazione.

Inoltre, la proprietà RecycleExpirationTimeout dell'oggetto [**COMAdminCatalogObject**](comadmincatalogobject.md) viene usata per forzare l'arresto di un processo riciclato. Indica il numero di minuti di attesa del rilascio di tutti i riferimenti esterni agli oggetti nel processo riciclato prima di arrestare forzatamente il processo. L'intervallo valido è compreso tra 1 e 1440 minuti (24 ore) e il timeout di scadenza predefinito è di 15 minuti. Questo valore viene usato solo quando è già stato determinato che un processo verrà riciclato in base agli altri criteri.

È possibile selezionare più criteri per il riciclo di un'applicazione. COM+ ricicla l'applicazione dopo aver soddisfatto il primo set di criteri. È possibile impostare il valore di timeout della scadenza per determinare per quanto tempo un vecchio processo Dllhost può trascorrere completando le richieste di servizio rimanenti prima di essere arrestato forzatamente.

La [**raccolta ApplicationInstances**](applicationinstances.md) fornisce la proprietà HasRecycled, che consente di determinare se l'applicazione è stata riciclata.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attività di riciclo delle applicazioni COM+](com--application-recycling-tasks.md)
</dt> <dt>

[**RecycleSurrogate**](/windows/desktop/api/ComSvcs/nf-comsvcs-recyclesurrogate)
</dt> </dl>

 

 



