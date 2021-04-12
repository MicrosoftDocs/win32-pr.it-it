---
description: Dopo la creazione di una query e l'aggiunta di contatori, chiamare la funzione PdhCollectQueryData per recuperare i dati non elaborati correnti per tutti i contatori nella query.
ms.assetid: 2534d387-a280-4716-9a9d-3e42f40e2f92
title: Raccolta dei dati sulle prestazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e99bd2c0e22553245e87d3844694051c88c57895
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345521"
---
# <a name="collecting-performance-data"></a>Raccolta dei dati sulle prestazioni

Dopo la [creazione di una query](creating-a-query.md) e l'aggiunta di contatori, chiamare la funzione [**PdhCollectQueryData**](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydata) per recuperare i dati non elaborati correnti per tutti i contatori nella query.

Molti contatori, ad esempio i contatori di frequenza, richiedono due esempi di dati per calcolare un valore di dati formattato. PDH gestisce i dati per l'esempio corrente e l'esempio precedentemente raccolto. Nella procedura seguente viene descritto come raccogliere i valori dei contatori che richiedono due esempi per calcolare un valore visualizzabile.

**Per raccogliere i valori dei contatori che richiedono due esempi per calcolare un valore visualizzabile**

1.  Chiamare [**PdhCollectQueryData**](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydata) per raccogliere il primo esempio.
2.  Chiamare la funzione [**Sleep**](/windows/desktop/api/synchapi/nf-synchapi-sleep) per attendere un minimo di un secondo tra le raccolte.
3.  Chiamare nuovamente [**PdhCollectQueryData**](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydata) per raccogliere il secondo campione.
4.  Chiamare la funzione [**PdhGetFormattedCounterValue**](/windows/desktop/api/Pdh/nf-pdh-pdhgetformattedcountervalue) per calcolare un valore visualizzabile.
5.  Ripetere i passaggi da 2 a 4.

In alternativa all'implementazione autonoma di un periodo di attesa, è possibile chiamare la funzione [**PdhCollectQueryDataEx**](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydataex) , che crea un thread di temporizzazione che attende una quantità di tempo specificata, raccoglie l'esempio e quindi attiva un evento definito dall'applicazione.

Se si desidera eseguire query sui dati sulle prestazioni da un file di log, è anche possibile definire un intervallo di tempo. L'intervallo di tempo limita la query agli esempi raccolti nell'intervallo di tempo (ogni campione contiene un timestamp per il momento in cui è stato raccolto). Per ulteriori informazioni su come impostare e recuperare gli intervalli di tempo, vedere [impostazione di un intervallo di tempo per una query](setting-a-time-range-for-a-query.md).

Se si desidera raccogliere i dati sulle prestazioni e scriverli in un file di log, è necessario chiamare la funzione [**PdhUpdateLog**](/windows/desktop/api/Pdh/nf-pdh-pdhupdateloga) invece di chiamare [**PdhCollectQueryData**](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydata). Per informazioni dettagliate, vedere [utilizzo di file di log](working-with-log-files.md) e [scrittura di dati sulle prestazioni in un file di log](writing-performance-data-to-a-log-file.md).

Per informazioni dettagliate sul calcolo di un valore di esempio visualizzabile, vedere [visualizzazione dei dati sulle prestazioni](displaying-performance-data.md).

## <a name="understanding-multiple-processor-counters"></a>Informazioni sui contatori di più processori

Alcuni contatori delle prestazioni sono stati progettati per sistemi a processore singolo e potrebbero non essere accurati per i computer multiprocessore. Un processo, ad esempio, è limitato al 100% di un singolo processore. Tuttavia, i thread possono usare più processori, per un totale superiore al 100%.

Il \\ valore del contatore "processore ( \_ totale) \\ % tempo processore" indica l'utilizzo medio di tutti i processori. Se, ad esempio, si dispone di due processori, uno con un 100% e un altro allo 0%, questo contatore segnalerà il 50%. Quindi l'intervallo è compreso tra 0 e 100.

Il \\ valore del contatore "processo (X) \\ % tempo di elaborazione" è la somma dell'utilizzo del processore da parte di tutti i thread del processo X. Ad esempio, in un computer con due processori, se un processo dispone di due thread, uno che occupa il 75% di una CPU e l'altro impiega il 80% di un'altra CPU, questo contatore segnalerà il 155%. L'intervallo per questo contatore è compreso tra 0 e 100 \* ProcessorCount.

* * Windows Server 2003 e Windows XP: * *

È possibile ricevere valori non compresi nell'intervallo di valori previsto per l'utilizzo della CPU. Per calcolare la percentuale di utilizzo della CPU, PDH richiede due campioni (ognuno con un valore non elaborato e un timestamp). Poiché PDH utilizza solo il nome dell'istanza per trovare la corrispondenza con i processi, può talvolta utilizzare due esempi di processi diversi. Se, ad esempio, si campionano tre processi e un processo viene terminato dopo il terzo campione, un altro processo verrà spostato nello slot sgomberato da tale processo terminato. Di conseguenza, un contatore formattato fornisce un valore non corretto quando si formatta il quarto campione, perché usa il terzo esempio del processo terminato e il quarto campione dal processo che è stato spostato nello slot del processo terminato.

La tabella seguente illustra come questa situazione può verificarsi se un processo viene terminato durante la raccolta dei dati. La tabella mostra cinque esempi di valore del contatore per tre istanze del processo X. Gli esempi vengono raccolti in intervalli di un secondo. Dopo la raccolta del terzo campione, viene terminato il processo X nello slot 1. Quando il processo X nello slot 1 viene terminato, il processo X nello slot 2 si sposta nello slot 1. Quando si raccoglie il quarto esempio per il processo X nello slot 2, il primo valore è ora 20 anziché 1.000 e il secondo valore è 1.500. Quando si formatta il valore del contatore, si ottengono 1.480 millisecondi anziché i 500 millisecondi previsti. Quando si formatta il quinto valore di esempio, è necessario ottenere il valore previsto.

| Esempio   | Slot 0 per il processo X | Slot 1 per il processo X           | Slot 2 per il processo X                     |
|----------|----------------------|--------------------------------|------------------------------------------|
| Esempio 1 | 0                    | 0                              | 0                                        |
| Esempio 2 | 20                   | 10                             | 500                                      |
| Esempio 3 | 40                   | 20                             | 1\.000                                    |
| Esempio 4 | 60                   | 1.500 (dallo slot precedente 2) | Non applicabile. Ora raccolti nello slot 1. |
| Esempio 5 | 80                   | 2\.000                          | Non applicabile. Ora raccolti nello slot 1. |



 

 

 
