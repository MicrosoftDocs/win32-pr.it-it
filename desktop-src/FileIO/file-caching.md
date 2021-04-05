---
description: Windows memorizza nella cache i dati del file letti dai dischi e scritti nei dischi.
ms.assetid: 0865c741-63e3-4246-ba69-801b02153e4a
title: Memorizzazione nella cache dei file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a14fb668af16cfb8a4e42b59b25b73ecefbb7cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884893"
---
# <a name="file-caching"></a>Memorizzazione nella cache dei file

Per impostazione predefinita, Windows memorizza nella cache i dati di file che vengono letti dai dischi e scritti sui dischi. Ciò implica che le operazioni di lettura leggono i dati dei file da un'area della memoria di sistema nota come cache dei file di sistema, invece che dal disco fisico. Analogamente, le operazioni di scrittura scrivono i dati dei file nella cache dei file di sistema anziché sul disco e questo tipo di cache è noto come cache write-back. La memorizzazione nella cache viene gestita per ogni oggetto file.

La memorizzazione nella cache si verifica in base alla direzione del *gestore della cache*, che funziona continuamente mentre è in esecuzione Windows. I dati dei file nella cache dei file di sistema vengono scritti sul disco a intervalli determinati dal sistema operativo e la memoria utilizzata in precedenza da tali dati viene liberata. questa operazione viene definita *scaricamento* della cache. Il criterio di ritardare la scrittura dei dati nel file e di mantenerlo nella cache finché la cache non viene scaricata è chiamato Lazy writing e viene attivato dal gestore della cache a un intervallo di tempo determinato. Il momento in cui un blocco di dati del file viene scaricato dipende in parte da quanto tempo è rimasto memorizzato nella cache e da quanto tempo è trascorso dall'ultima volta in cui si è avuto accesso ai dati in un'operazione di lettura. Questo garantisce che i dati del file letti frequentemente restino accessibili nella cache dei file di sistema per il massimo intervallo di tempo previsto.

Questo processo di memorizzazione nella cache dei dati del file è illustrato nella figura seguente.

![processo di memorizzazione nella cache dei dati di file](images/fig3.png)

Come illustrato dalle frecce solide nella figura precedente, un'area di dati di 256 KB viene letta in uno slot della cache da 256 KB nello spazio degli indirizzi del sistema quando viene richiesta per la prima volta dal gestore della cache durante un'operazione di lettura del file. Un processo in modalità utente quindi copia i dati di questo slot nel proprio spazio indirizzi. Quando il processo ha completato l'accesso ai dati, riscrive i dati modificati nello stesso slot nella cache di sistema, come indicato dalla freccia tratteggiata tra lo spazio indirizzi del processo e la cache di sistema. Quando il gestore della cache ha determinato che i dati non saranno più necessari per un determinato periodo di tempo, i dati modificati vengono scritti nuovamente nel file su disco, come illustrato dalla freccia tratteggiata tra la cache di sistema e il disco.

La quantità di miglioramento delle prestazioni di I/O che la memorizzazione nella cache dei dati del file dipende dalla dimensione del blocco di dati file letto o scritto. Quando si leggono e scrivono blocchi di dati di file di grandi dimensioni, è più probabile che le letture e le Scritture del disco siano necessarie per completare l'operazione di I/O. Le prestazioni di i/O saranno sempre più disaccoppiate, perché si verifica un maggior numero di questo tipo di operazione di I/O.

In queste situazioni, la memorizzazione nella cache può essere disattivata. Questa operazione viene eseguita al momento dell'apertura del file passando il **flag di file \_ \_ nessun \_ buffering** come valore per il parametro *dwFlagsAndAttributes* di [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea). Quando la memorizzazione nella cache è disabilitata, tutte le operazioni di lettura e scrittura accedono direttamente al disco fisico. Tuttavia, i metadati del file possono essere ancora memorizzati nella cache. Per svuotare i metadati su disco, usare la funzione [**FlushFileBuffers**](/windows/desktop/api/FileAPI/nf-fileapi-flushfilebuffers) .

La frequenza con cui si verifica lo svuotamento è una considerazione importante che bilancia le prestazioni del sistema con l'affidabilità del sistema. Se la cache viene scaricata troppo spesso dal sistema, il numero di operazioni di scrittura di grandi dimensioni che lo scaricamento comporta un calo significativo delle prestazioni del sistema. Se il sistema non viene svuotato abbastanza spesso, la probabilità è maggiore che la memoria di sistema verrà esaurita dalla cache o un errore di sistema improvviso, ad esempio una perdita di energia al computer, avverrà prima dello scaricamento. Nel secondo caso, i dati memorizzati nella cache andranno persi.

Per assicurarsi che venga eseguita la quantità corretta di scaricamento, il gestore della cache genera un processo ogni secondo chiamato Lazy Writer. Il processo Lazy Writer Accoda un ottavo di pagine che non sono state scaricate di recente per essere scritte su disco. Rivaluta costantemente la quantità di dati scaricati per ottimizzare le prestazioni del sistema e, se è necessario scrivere più dati, Accoda più dati. I writer lazy non scaricano i file temporanei, perché il presupposto è che vengano eliminati dall'applicazione o dal sistema.

Per alcune applicazioni, ad esempio il software di controllo dei virus, è necessario che le operazioni di scrittura vengano scaricate immediatamente su disco; Windows offre questa possibilità attraverso la memorizzazione nella cache write-through. Un processo consente la memorizzazione nella cache write-through per un'operazione di I/O specifica passando il flag **\_ \_ Write \_ through del flag file** alla chiamata a [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea). Con la memorizzazione nella cache write-through abilitata, i dati vengono ancora scritti nella cache, ma il gestore della cache scrive immediatamente i dati su disco anziché incorrere in un ritardo utilizzando il writer Lazy. Un processo può anche forzare lo scaricamento di un file aperto chiamando la funzione [**FlushFileBuffers**](/windows/desktop/api/FileAPI/nf-fileapi-flushfilebuffers) .

I metadati del file System vengono sempre memorizzati nella cache. Pertanto, per archiviare le modifiche dei metadati sul disco, è necessario scaricare il file o aprirlo con il **\_ flag file \_ Write \_ through**.

 

 



