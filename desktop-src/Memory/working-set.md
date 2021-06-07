---
description: Il working set di un processo è il set di pagine nello spazio degli indirizzi virtuali del processo attualmente residenti nella memoria fisica.
ms.assetid: ff05276a-1d40-4844-b649-10e32e3f1937
title: Working Set
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4985e7eb526d5dda8469ccc2f46bfe6fd050c745
ms.sourcegitcommit: b01ad017c152c6756f3638623fe335877644d414
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/06/2021
ms.locfileid: "111549893"
---
# <a name="working-set"></a>Working Set

Il working set di un processo è il set di pagine nello spazio degli indirizzi virtuali del processo attualmente residenti nella memoria fisica. Il working set contiene solo allocazioni di memoria paginabile. Le allocazioni di memoria non paginabile, ad [](large-page-support.md) esempio [Address Windowing Extensions](address-windowing-extensions.md) (AWE) o le allocazioni di pagine di grandi dimensioni, non sono incluse nel working set.

Quando un processo fa riferimento a una memoria paginabile che non è attualmente working set, si verifica *un errore di* pagina. Il gestore degli errori di pagina di sistema tenta di risolvere l'errore di pagina e, se ha esito positivo, la pagina viene aggiunta al working set. L'accesso ad AWE o alle allocazioni di pagine di grandi dimensioni non causa mai un errore di pagina, perché queste allocazioni non sono paginabili.

Un *errore di* pagina hardware deve essere risolto leggendo il contenuto della pagina dall'archivio di backup della pagina, ovvero il file di paging di sistema o un file mappato alla memoria creato dal processo.  Un *errore di pagina soft* può essere risolto senza accedere all'archivio di backup. Si verifica un errore di pagina soft quando:

-   La pagina si trova nel working set di un altro processo, quindi è già in memoria.
-   La pagina è in transizione, perché è stata rimossa dai working set di tutti i processi che usavano la pagina e non è ancora stata reimpienita oppure è già residenti come risultato di un'operazione di prelettura del gestore della memoria.
-   Un processo fa riferimento a una pagina virtuale allocata per la prima volta (talvolta denominata *errore di tipo demand-zero).*

Le pagine possono essere rimosse da working set processo come risultato delle azioni seguenti:

-   Il processo riduce o svuota il working set chiamando la funzione [**SetProcessWorkingSetSize,**](/windows/win32/api/memoryapi/nf-memoryapi-setprocessworkingsetsize) [**SetProcessWorkingSetSizeEx**](/windows/win32/api/memoryapi/nf-memoryapi-setprocessworkingsetsizeex) o [**EmptyWorkingSet.**](/windows/win32/api/psapi/nf-psapi-emptyworkingset)
-   Il processo chiama la [**funzione VirtualUnlock**](/windows/win32/api/memoryapi/nf-memoryapi-virtualunlock) su un intervallo di memoria non bloccato.
-   Il processo annulla il mapping di una visualizzazione mappata di un file usando [**la funzione UnmapViewOfFile.**](/windows/win32/api/memoryapi/nf-memoryapi-unmapviewoffile)
-   Il gestore della memoria taglia le pagine dal working set per creare più memoria disponibile.
-   Il gestore della memoria deve rimuovere una pagina dal working set per creare spazio per una nuova pagina, ad esempio perché la working set ha le dimensioni massime.

Se più processi condividono una pagina, la rimozione della pagina dal working set di un processo non influisce sugli altri processi. Dopo la rimozione di una pagina dai working set di tutti i processi che la usavano, la pagina diventa una *pagina di transizione*. Le pagine di transizione rimangono memorizzate nella cache nella RAM fino a quando un processo non fa di nuovo riferimento alla pagina o non viene reimpiego (ad esempio, riempito con zeri e assegnato a un altro processo). Se una pagina di transizione è stata modificata dopo l'ultima scrittura su disco (ovvero se la pagina è "dirty"), la pagina deve essere scritta nel relativo archivio di backup prima di poter essere reimpienita. Il sistema può iniziare a scrivere pagine di transizione dirty nell'archivio di backup non appena tali pagine diventano disponibili.

Ogni processo ha dimensioni minime e massime working set che influiscono sul comportamento di paging della memoria virtuale del processo. Per ottenere la dimensione corrente del working set di un processo specificato, usare la [**funzione GetProcessMemoryInfo.**](/windows/win32/api/psapi/nf-psapi-getprocessmemoryinfo) Per ottenere o modificare le dimensioni minime e massime working set, usare le [**funzioni GetProcessWorkingSetSizeEx**](/windows/win32/api/memoryapi/nf-memoryapi-getprocessworkingsetsizeex) [**e SetProcessWorkingSetSizeEx.**](/windows/win32/api/memoryapi/nf-memoryapi-setprocessworkingsetsizeex)

L'interfaccia PSAPI (Process Status Application Programming Interface) fornisce una serie di funzioni che restituiscono informazioni dettagliate sulla working set di un processo. Per informazioni dettagliate, vedere [Informazioni sul working set.](../psapi/working-set-information.md)

 

 
