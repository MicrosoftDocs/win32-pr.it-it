---
description: Il working set di un processo è il set di pagine nello spazio degli indirizzi virtuali del processo che attualmente risiede nella memoria fisica.
ms.assetid: ff05276a-1d40-4844-b649-10e32e3f1937
title: Working Set
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f54ed26e9809ebffd01edb30f48f36d398689e88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313821"
---
# <a name="working-set"></a>Working Set

Il working set di un processo è il set di pagine nello spazio degli indirizzi virtuali del processo che attualmente risiede nella memoria fisica. Il working set contiene solo allocazioni di memoria paginabili; le allocazioni di memoria non paginabili come AWE ( [Address Windowing Extensions](address-windowing-extensions.md) ) o le [allocazioni di pagine di grandi dimensioni](large-page-support.md) non sono incluse nel working set.

Quando un processo fa riferimento a una memoria paginabile che non si trova attualmente nella working set, si verifica un *errore di pagina* . Il gestore errori di pagina sistema tenta di risolvere l'errore di pagina e, in caso di esito positivo, la pagina viene aggiunta al working set. L'accesso a AWE o alle allocazioni di pagine di grandi dimensioni non provoca mai un errore di pagina, perché queste allocazioni non sono paginabili.

È necessario risolvere un *errore di pagina hardware* leggendo il contenuto della pagina dall' *Archivio di backup* della pagina, ovvero il file di paging di sistema o un file mappato alla memoria creato dal processo. È possibile risolvere un *errore di pagina software* senza accedere all'archivio di backup. Si verifica un errore di pagina software quando:

-   La pagina si trova nel working set di un altro processo, quindi è già residente in memoria.
-   La pagina è in fase di transizione, perché è stata rimossa dal working set di tutti i processi che stavano usando la pagina e non è ancora stata reimpiegata oppure è già residente in seguito a un'operazione di prelettura di gestione memoria.
-   Un processo fa riferimento a una pagina virtuale allocata per la prima volta (talvolta denominato *errore di richiesta-zero*).

Le pagine possono essere rimosse da un processo working set come risultato delle azioni seguenti:

-   Il processo riduce o svuota il working set chiamando la funzione [**SetProcessWorkingSetSize**](/windows/win32/api/winbase/nf-winbase-setprocessworkingsetsize), [**SetProcessWorkingSetSizeEx**](/windows/win32/api/memoryapi/nf-memoryapi-setprocessworkingsetsizeex) o [**EmptyWorkingSet**](/windows/win32/api/psapi/nf-psapi-emptyworkingset) .
-   Il processo chiama la funzione [**VirtualUnlock**](/windows/win32/api/memoryapi/nf-memoryapi-virtualunlock) su un intervallo di memoria non bloccato.
-   Il processo esegue l'unmapping di una visualizzazione mappata di un file tramite la funzione [**UnmapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-unmapviewoffile) .
-   Il gestore della memoria taglia le pagine dalla working set per creare una maggiore quantità di memoria disponibile.
-   Il gestore della memoria deve rimuovere una pagina dal working set per creare spazio per una nuova pagina, ad esempio perché il working set è alla dimensione massima.

Se più processi condividono una pagina, la rimozione della pagina dalla working set di un processo non influisce su altri processi. Quando una pagina viene rimossa dai working set di tutti i processi che lo stavano utilizzando, la pagina diventa una *pagina di transizione*. Le pagine di transizione rimangono memorizzate nella cache fino a quando non viene fatto nuovamente riferimento a una pagina da parte di un processo o riproposta, ad esempio riempita con zeri e assegnata a un altro processo. Se una pagina di transizione è stata modificata dopo l'ultima scrittura su disco (ovvero, se la pagina è "Dirty"), la pagina deve essere scritta nell'archivio di backup prima di poterla reimpiegare. Il sistema può iniziare a scrivere pagine di transizione Dirty nell'archivio di backup non appena tali pagine diventano disponibili.

Ogni processo ha dimensioni minime e massime working set che influiscono sul comportamento di paging della memoria virtuale del processo. Per ottenere le dimensioni correnti del working set di un processo specificato, utilizzare la funzione [**GetProcessMemoryInfo**](/windows/win32/api/psapi/nf-psapi-getprocessmemoryinfo) . Per ottenere o modificare le dimensioni working set minime e massime, usare le funzioni [**GetProcessWorkingSetSizeEx**](/windows/win32/api/memoryapi/nf-memoryapi-getprocessworkingsetsizeex) e [**SetProcessWorkingSetSizeEx**](/windows/win32/api/memoryapi/nf-memoryapi-setprocessworkingsetsizeex) .

Il Application Programming Interface di stato del processo (PSAPI) fornisce una serie di funzioni che restituiscono informazioni dettagliate sul working set di un processo. Per informazioni dettagliate, vedere [working set information](../psapi/working-set-information.md).

 

 
