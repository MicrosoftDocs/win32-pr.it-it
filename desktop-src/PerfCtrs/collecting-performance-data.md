---
description: Dopo aver creato una query e aver aggiunto contatori, chiamare la funzione PdhCollectQueryData per recuperare i dati non elaborati correnti per tutti i contatori nella query.
ms.assetid: 2534d387-a280-4716-9a9d-3e42f40e2f92
title: Raccolta dei dati sulle prestazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79f65280190e67e27783ea7e7387eac0e348aad1a53ad016df3010ae0bfd2ea9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061239"
---
# <a name="collecting-performance-data"></a>Raccolta dei dati sulle prestazioni

Dopo [aver creato una query](creating-a-query.md) e aver aggiunto contatori, chiamare la funzione [**PdhCollectQueryData**](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydata) per recuperare i dati non elaborati correnti per tutti i contatori nella query.

Molti contatori, ad esempio i contatori delle frequenze, richiedono due campioni di dati per calcolare un valore di dati formattato. PDH gestisce i dati per l'esempio corrente e l'esempio raccolto in precedenza. La procedura seguente descrive come raccogliere i valori dei contatori che richiedono due campioni per calcolare un valore visualizzabile.

**Per raccogliere i valori dei contatori che richiedono due campioni per calcolare un valore visualizzabile**

1.  Chiamare [**PdhCollectQueryData**](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydata) per raccogliere il primo esempio.
2.  Chiamare la [**funzione Sleep**](/windows/desktop/api/synchapi/nf-synchapi-sleep) per attendere almeno un secondo tra le raccolte.
3.  Chiamare [**di nuovo PdhCollectQueryData**](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydata) per raccogliere il secondo esempio.
4.  Chiamare la [**funzione PdhGetFormattedCounterValue**](/windows/desktop/api/Pdh/nf-pdh-pdhgetformattedcountervalue) per calcolare un valore visualizzabile.
5.  Ripetere i passaggi da 2 a 4.

In alternativa all'implementazione di un periodo di attesa, è possibile chiamare la funzione [**PdhCollectQueryDataEx,**](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydataex) che crea un thread di intervallo che attende una quantità di tempo specificata, raccoglie l'esempio e quindi attiva un evento definito dall'applicazione.

Se si desidera eseguire query sui dati sulle prestazioni da un file di log, è anche possibile definire un intervallo di tempo. L'intervallo di tempo limita la query ai campioni raccolti nell'intervallo di tempo (ogni campione contiene un timestamp per la raccolta). Per altre informazioni su come impostare e recuperare intervalli di tempo, vedere [Impostazione di un intervallo di tempo per una query](setting-a-time-range-for-a-query.md).

Se si desidera raccogliere dati sulle prestazioni e scriverlo in un file di log, chiamare la funzione [**PdhUpdateLog**](/windows/desktop/api/Pdh/nf-pdh-pdhupdateloga) anziché [**chiamare PdhCollectQueryData**](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydata). Per informazioni dettagliate, vedere [Uso dei file di log e](working-with-log-files.md) Scrittura di dati sulle prestazioni in un file di [log](writing-performance-data-to-a-log-file.md).

Per informazioni dettagliate sul calcolo di un valore di esempio visualizzabile, vedere [Visualizzazione dei dati sulle prestazioni](displaying-performance-data.md).

## <a name="understanding-multiple-processor-counters"></a>Informazioni sui contatori di più processori

Alcuni contatori delle prestazioni sono stati progettati per sistemi a processore singolo e potrebbero non essere accurati per i computer multiprocessore. Ad esempio, un processo è limitato al 100% di un singolo processore. Tuttavia, i thread possono usare diversi processori, per un totale di oltre il 100%.

Il valore del contatore " \\ Processor( \_ Total) \\ % Processor Time" è l'utilizzo medio di tutti i processori. Ad esempio, se si dispone di due processori, uno al 100% e l'altro allo 0%, questo contatore segnala il 50%. L'intervallo è quindi compreso tra 0 e 100.

Il valore \\ del contatore "Process(X) % Process Time" è la somma dell'utilizzo del processore da parte di \\ tutti i thread del processo X. Ad esempio, in un computer con due processori, se un processo ha due thread, uno che occupa il 75% di una CPU e l'altro l'80% di un'altra CPU, questo contatore segnala il 155%. L'intervallo per questo contatore è compreso tra 0 e 100 \* ProcessorCount.

**Windows Server 2003 e Windows XP: **

È possibile ricevere valori al di fuori dell'intervallo di valori previsto per l'utilizzo della CPU. Per calcolare la percentuale di utilizzo della CPU, PDH richiede due campioni,ognuno con un valore non elaborato e un timestamp. Poiché PDH usa solo il nome dell'istanza per corrispondere ai processi, a volte può usare due esempi di processi diversi. Ad esempio, se vengono campionati tre processi e un processo viene terminato dopo il terzo esempio, un altro processo verrà spostato nello slot liberato da tale processo terminato. Di conseguenza, un contatore formattato fornirà un valore non corretto quando si formatta il quarto esempio, perché usa il terzo esempio del processo terminato e il quarto esempio del processo spostato nello slot del processo terminato.

La tabella seguente illustra come questo problema può verificarsi se un processo viene terminato durante la raccolta dei dati. La tabella mostra cinque esempi di valori del contatore per tre istanze del processo X. Gli esempi vengono raccolti a intervalli di un secondo. Dopo la raccolta del terzo esempio, il processo X nello slot 1 viene terminato. Quando il processo X nello slot 1 viene terminato, il processo X nello slot 2 viene spostato nello slot 1. Quando si raccoglie il quarto esempio per il processo X nello slot 2, il primo valore è ora 20 anziché 1.000 e il secondo valore è 1.500. Quando si formatta il valore del contatore, si ottengono 1.480 millisecondi anziché i 500 millisecondi previsti. Quando si formatta il quinto valore di esempio, si dovrebbe ottenere il valore previsto.

| Esempio   | Slot 0 per il processo X | Slot 1 per il processo X           | Slot 2 per il processo X                     |
|----------|----------------------|--------------------------------|------------------------------------------|
| Esempio 1 | 0                    | 0                              | 0                                        |
| Esempio 2 | 20                   | 10                             | 500                                      |
| Esempio 3 | 40                   | 20                             | 1\.000                                    |
| Esempio 4 | 60                   | 1.500 (dal primo slot 2) | Non applicabile. Ora raccolti nello slot 1. |
| Esempio 5 | 80                   | 2.000                          | Non applicabile. Ora raccolti nello slot 1. |



 

 

 
