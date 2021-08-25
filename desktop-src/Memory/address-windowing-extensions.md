---
description: Address Windowing Extensions (AWE) è un set di estensioni che consente a un'applicazione di modificare rapidamente la memoria fisica superiore a 4 GB.
ms.assetid: 48a29922-8130-4540-86b0-0faa120566a6
title: Estensioni address windowing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c5f0c68e9609834a9065a919d12c23c40521e99ede94feb96889050b6873654
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764411"
---
# <a name="address-windowing-extensions"></a>Estensioni address windowing

Address Windowing Extensions (AWE) è un set di estensioni che consente a un'applicazione di modificare rapidamente la memoria fisica superiore a 4 GB. Alcune applicazioni a elevato utilizzo di dati, ad esempio sistemi di gestione di database e software scientifico e tecnico, devono accedere a cache di dati molto grandi. Nel caso di set di dati di dimensioni molto grandi, limitare la cache in modo che si adatti a 2 GB di spazio degli indirizzi utente di un'applicazione è una restrizione grave. In queste situazioni, la cache è troppo piccola per supportare correttamente l'applicazione.

AWE risolve questo problema consentendo alle applicazioni di risolvere direttamente grandi quantità di memoria continuando a usare puntatori a 32 bit. AWE consente alle applicazioni di avere cache di dati superiori a 4 GB (dove è presente memoria fisica sufficiente). AWE usa la memoria fisica non di pagina e le visualizzazioni finestra di varie parti di questa memoria fisica all'interno di uno spazio di indirizzi virtuali a 32 bit.

AWE pone alcune restrizioni sul modo in cui questa memoria può essere usata, principalmente perché queste restrizioni consentono il mapping estremamente veloce, il nuovo mapping e la liberazione. La gestione rapida della memoria è importante per questi spazi indirizzi potenzialmente enormi.

-   Gli intervalli di indirizzi virtuali allocati per AWE non sono sharable con altri processi e pertanto non possono essere ereditati. Infatti, due indirizzi virtuali AWE diversi all'interno dello stesso processo non possono eseguire il mapping della stessa pagina fisica. Queste restrizioni consentono di eseguire rapidamente il mapping e la pulizia quando viene liberata la memoria.
-   Le pagine fisiche che possono essere allocate per un'area AWE sono limitate dal numero di pagine fisiche presenti nel computer, dal momento che la memoria non viene mai paginata, perché viene bloccata fino a quando l'applicazione non la libera o si chiude in modo esplicito. Le pagine fisiche allocate per un determinato processo possono essere mappate in qualsiasi area virtuale AWE all'interno dello stesso processo. Le applicazioni che usano AWE devono prestare attenzione a non usare una quantità di memoria fisica tale da causare un numero eccessivo di pagine da parte di altre applicazioni o impedire la creazione di nuovi processi o thread a causa della mancanza di risorse. Usare la [**funzione GlobalMemoryStatusEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-globalmemorystatusex) per monitorare l'uso della memoria fisica.
-   Gli indirizzi virtuali AWE sono sempre di lettura/scrittura e non possono essere protetti tramite chiamate a [**VirtualProtect,**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotect) ovvero non è possibile specificare memoria di sola lettura, memoria noaccess, pagine guard e simili.
-   Gli intervalli di indirizzi AWE non possono essere usati per il buffer dei dati per chiamate grafiche o video.
-   Un intervallo di memoria AWE non può essere suddiviso né può essere eliminato. Al contrario, l'intero intervallo di indirizzi virtuali deve essere eliminato come unità quando è necessaria l'eliminazione. Ciò significa che è necessario specificare **MEM \_ RELEASE** quando si [**chiama VirtualFree**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfree).
-   Le applicazioni possono eseguire il mapping di più aree contemporaneamente, a condizione che non si sovrappongano.
-   Le applicazioni che usano AWE non sono supportate in modalità di emulazione. In altre parole, un'applicazione x86 che usa funzioni AWE deve essere ricompilata per l'esecuzione in un altro processore, mentre la maggior parte delle applicazioni può essere eseguita senza ricompilazione in un emulatore in altre piattaforme.

Questa soluzione consente di risolvere i problemi di memoria fisica in modo molto generale e ampiamente applicabile. Alcuni dei vantaggi di AWE sono:

-   Viene definito un piccolo gruppo di nuove funzioni per modificare la memoria AWE.
-   AWE offre una funzionalità di remapping molto veloce. Il nuovo mapping viene eseguito modificando le tabelle di memoria virtuale, non spostando i dati nella memoria fisica.
-   AWE offre la granularità delle dimensioni della pagina appropriata per il processore (ad esempio, 4 KB in x86), che è più utile per le applicazioni rispetto alle pagine di grandi dimensioni (ad esempio, 2 MB o 4 MB in x86).

Un'applicazione deve avere il privilegio Blocco di pagine in memoria per usare AWE. Per ottenere questo privilegio, un amministratore deve aggiungere **Blocco di pagine in** memoria alle assegnazioni dei diritti utente **dell'utente.** Per altre informazioni su come eseguire questa operazione, vedere "Diritti utente" nella Guida del sistema operativo.

Le funzioni seguenti costituiscono l'API Address Windowing Extensions (AWE).



| Funzione                                                                          | Descrizione                                                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) e [ **VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex) | Riservare una parte dello spazio indirizzi virtuali da usare per AWE, usando **MEM \_ PHYSICAL.**                                                                                                                                                                       |
| [**AllocateUserPhysicalPages**](/windows/win32/api/memoryapi/nf-memoryapi-allocateuserphysicalpages)                    | Allocare memoria fisica per l'uso con AWE.                                                                                                                                                                                                                |
| [**MapUserPhysicalPages**](/windows/win32/api/memoryapi/nf-memoryapi-mapuserphysicalpages)                              | Eseguire il mapping (o invalidare) gli indirizzi virtuali AWE in qualsiasi set di pagine fisiche ottenuto con [**AllocateUserPhysicalPages.**](/windows/win32/api/memoryapi/nf-memoryapi-allocateuserphysicalpages)                                                                                                    |
| [**MapUserPhysicalPagesScatter**](/windows/desktop/api/WinBase/nf-winbase-mapuserphysicalpagesscatter)                | Eseguire il mapping (o invalidare) gli indirizzi virtuali AWE in qualsiasi set di pagine fisiche ottenute con [**AllocateUserPhysicalPages,**](/windows/win32/api/memoryapi/nf-memoryapi-allocateuserphysicalpages)ma con un controllo più fine rispetto a quello fornito da [**MapUserPhysicalPages.**](/windows/win32/api/memoryapi/nf-memoryapi-mapuserphysicalpages) |
| [**FreeUserPhysicalPages**](/windows/win32/api/memoryapi/nf-memoryapi-freeuserphysicalpages)                            | Memoria fisica libera usata per AWE.                                                                                                                                                                                                               |



 

 

 
