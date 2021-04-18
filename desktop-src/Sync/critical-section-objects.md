---
description: Un oggetto sezione critica fornisce una sincronizzazione simile a quella fornita da un oggetto mutex, ad eccezione del fatto che una sezione critica può essere usata solo dai thread di un singolo processo.
ms.assetid: 2ec11a42-3d12-4d60-9dd7-dc38926d56e1
title: Oggetti sezione critica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbcada1f2ddbc6d370445f36a3dbd51c5c9f54bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315307"
---
# <a name="critical-section-objects"></a>Oggetti sezione critica

Un *oggetto sezione critica* fornisce una sincronizzazione simile a quella fornita da un oggetto mutex, ad eccezione del fatto che una sezione critica può essere usata solo dai thread di un singolo processo. Gli oggetti sezione critici non possono essere condivisi tra più processi.

Gli oggetti Event, mutex e Semaphore possono essere utilizzati anche in un'applicazione a processo singolo, ma gli oggetti sezione critici forniscono un meccanismo leggermente più veloce e più efficiente per la sincronizzazione con esclusione reciproca (test specifici del processore e istruzioni set). Analogamente a un oggetto mutex, un oggetto sezione critica può essere di proprietà di un solo thread alla volta, in modo da renderlo utile per la protezione di una risorsa condivisa dall'accesso simultaneo. A differenza di un oggetto mutex, non è possibile stabilire se una sezione critica è stata abbandonata.

A partire da Windows Server 2003 con Service Pack 1 (SP1), i thread in attesa di una sezione critica non acquisiscono la sezione critica in base alla prima, prima di tutto. Questa modifica migliora significativamente le prestazioni per la maggior parte del codice. Tuttavia, alcune applicazioni dipendono dall'ordinamento First-in, First-out (FIFO) e possono essere eseguite in modo non corretto o non in tutte le versioni correnti di Windows (ad esempio, le applicazioni che hanno usato sezioni critiche come un limite di velocità). Per assicurarsi che il codice continui a funzionare correttamente, potrebbe essere necessario aggiungere un ulteriore livello di sincronizzazione. Si supponga, ad esempio, di avere un thread producer e un thread consumer che usano un oggetto sezione critica per sincronizzare il lavoro. Creare due oggetti evento, uno per ogni thread da usare per segnalare che è pronto per continuare l'altro thread. Il thread consumer attenderà che il producer segnali il proprio evento prima di entrare nella sezione critica e il thread producer attenderà che il thread consumer segnali il proprio evento prima di immettere la sezione critica. Quando ogni thread esce dalla sezione critica, segnala l'evento per rilasciare l'altro thread.

**Windows Server 2003 e Windows XP:** I thread in attesa di una sezione critica vengono aggiunti a una coda di attesa. vengono riattivate e in genere acquisiscono la sezione critica nell'ordine in cui sono state aggiunte alla coda. Tuttavia, se i thread vengono aggiunti a questa coda a una velocità sufficientemente elevata, le prestazioni possono risultare ridotte a causa del tempo necessario per riattivare ogni thread in attesa.

Il processo è responsabile dell'allocazione della memoria utilizzata da una sezione critica. Questa operazione viene in genere eseguita semplicemente dichiarando una variabile di **tipo \_ sezione critica**. Prima che i thread del processo possano utilizzarlo, inizializzare la sezione critica utilizzando la funzione [**InitializeCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-initializecriticalsection) o [**InitializeCriticalSectionAndSpinCount**](/windows/win32/api/synchapi/nf-synchapi-initializecriticalsectionandspincount) .

Un thread usa la funzione [**EnterCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-entercriticalsection) o [**TryEnterCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-tryentercriticalsection) per richiedere la proprietà di una sezione critica. Usa la funzione [**LeaveCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-leavecriticalsection) per rilasciare la proprietà di una sezione critica. Se l'oggetto sezione critica è attualmente di proprietà di un altro thread, **EnterCriticalSection** attende indefinitamente per la proprietà. Al contrario, quando un oggetto mutex viene utilizzato per l'esclusione reciproca, le [funzioni di attesa](wait-functions.md) accettano un intervallo di timeout specificato. La funzione **TryEnterCriticalSection** tenta di immettere una sezione critica senza bloccare il thread chiamante.

Quando un thread è proprietario di una sezione critica, può effettuare chiamate aggiuntive a [**EnterCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-entercriticalsection) o [**TryEnterCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-tryentercriticalsection) senza bloccarne l'esecuzione. In questo modo si impedisce a un thread di verificarsi un deadlock durante l'attesa di una sezione critica di cui è già proprietario. Per rilasciare la proprietà, il thread deve chiamare [**LeaveCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-leavecriticalsection) una volta per ogni volta in cui è stata immessa la sezione critica. Non esiste alcuna garanzia sull'ordine in cui i thread in attesa acquisiscono la proprietà della sezione critica.

Un thread usa la funzione [**InitializeCriticalSectionAndSpinCount**](/windows/win32/api/synchapi/nf-synchapi-initializecriticalsectionandspincount) o [**SetCriticalSectionSpinCount**](/windows/win32/api/synchapi/nf-synchapi-setcriticalsectionspincount) per specificare un numero di spin per l'oggetto sezione critica. La rotazione significa che quando un thread tenta di acquisire una sezione critica bloccata, il thread entra in un ciclo, verifica se il blocco viene rilasciato e se il blocco non viene rilasciato, il thread passa alla modalità di sospensione. Nei sistemi a processore singolo, il numero di spin viene ignorato e il conteggio delle sezioni critiche è impostato su 0 (zero). Nei sistemi multiprocessore, se la sezione critica non è disponibile, il thread chiamante gira *dwSpinCount* volte prima di eseguire un'operazione di attesa su un semaforo associato alla sezione critica. Se la sezione critica diventa disponibile durante l'operazione di rotazione, il thread chiamante evita l'operazione di attesa.

Qualsiasi thread del processo può utilizzare la funzione [**DeleteCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-deletecriticalsection) per rilasciare le risorse di sistema allocate quando viene inizializzato l'oggetto sezione critica. Dopo la chiamata a questa funzione, l'oggetto sezione critica non può essere utilizzato per la sincronizzazione.

Quando un oggetto sezione critico è di proprietà, gli unici altri thread interessati sono i thread in attesa di proprietà in una chiamata a [**EnterCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-entercriticalsection). I thread che non sono in attesa possono continuare l'esecuzione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Oggetti mutex](mutex-objects.md)
</dt> <dt>

[Utilizzo di oggetti sezione critici](using-critical-section-objects.md)
</dt> </dl>

 

 
