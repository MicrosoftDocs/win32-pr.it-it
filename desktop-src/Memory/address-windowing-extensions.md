---
description: Address Windowing Extensions (AWE) è un set di estensioni che consente a un'applicazione di modificare rapidamente la memoria fisica superiore a 4 GB.
ms.assetid: 48a29922-8130-4540-86b0-0faa120566a6
title: Estensioni della finestra degli indirizzi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8cb311bf9ecef2de334018ca3f9982a31f0b072
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881510"
---
# <a name="address-windowing-extensions"></a>Estensioni della finestra degli indirizzi

Address Windowing Extensions (AWE) è un set di estensioni che consente a un'applicazione di modificare rapidamente la memoria fisica superiore a 4 GB. Alcune applicazioni con utilizzo intensivo di dati, ad esempio sistemi di gestione di database e software scientifico e ingegneristico, devono accedere a cache di dati di dimensioni molto grandi. Nel caso di set di dati di grandi dimensioni, la limitazione della cache per adattarsi ai 2 GB di spazio degli indirizzi utente di un'applicazione è una restrizione grave. In queste situazioni, la cache è troppo piccola per supportare correttamente l'applicazione.

AWE risolve questo problema consentendo alle applicazioni di affrontare direttamente grandi quantità di memoria pur continuando a usare puntatori a 32 bit. AWE consente alle applicazioni di avere cache di dati di dimensioni superiori a 4 GB (in cui è presente memoria fisica sufficiente). AWE utilizza la memoria fisica non di paging e le visualizzazioni finestra di diverse parti di questa memoria fisica in uno spazio degli indirizzi virtuali a 32 bit.

AWE pone alcune restrizioni sulla modalità di utilizzo di questa memoria, principalmente perché queste restrizioni consentono un mapping estremamente rapido, un nuovo mapping e una liberazione. La gestione rapida della memoria è importante per questi spazi di indirizzi potenzialmente enormi.

-   Gli intervalli di indirizzi virtuali allocati per AWE non sono condivisibili con altri processi (e pertanto non possono essere ereditati). Infatti, non è consentito eseguire il mapping della stessa pagina fisica a due diversi indirizzi virtuali AWE all'interno dello stesso processo. Queste restrizioni garantiscono una rapida rimappatura e pulizia quando la memoria viene liberata.
-   Le pagine fisiche che è possibile allocare per un'area AWE sono limitate dal numero di pagine fisiche presenti nel computer, poiché la memoria non viene mai sottoposta a paging, ma viene bloccata fino a quando l'applicazione non la libera esplicitamente o non viene chiusa. Le pagine fisiche allocate per un determinato processo possono essere mappate in qualsiasi area virtuale AWE all'interno dello stesso processo. Per le applicazioni che utilizzano AWE è necessario prestare attenzione a non richiedere una quantità eccessiva di memoria fisica che causi la pagina di altre applicazioni o impedisca la creazione di nuovi processi o thread a causa di risorse insufficienti. Utilizzare la funzione [**GlobalMemoryStatusEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-globalmemorystatusex) per monitorare l'utilizzo della memoria fisica.
-   Gli indirizzi virtuali AWE sono sempre di lettura/scrittura e non possono essere protetti tramite chiamate a [**VirtualProtect**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotect) (ovvero non è possibile specificare la memoria di sola lettura, la memoria NoAccess, le pagine di Guard e la like).
-   Non è possibile usare gli intervalli di indirizzi AWE per memorizzare nel buffer i dati per le chiamate grafica o video.
-   Un intervallo di memoria AWE non può essere suddiviso, né può essere eliminato. Al contrario, l'intero intervallo di indirizzi virtuali deve essere eliminato come unità quando è necessaria l'eliminazione. Ciò significa che è necessario specificare la **\_ versione di MEM** quando si chiama [**VirtualFree**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfree).
-   Le applicazioni possono eseguire il mapping di più aree contemporaneamente, a condizione che non si sovrappongano.
-   Le applicazioni che utilizzano AWE non sono supportate in modalità di emulazione. Ovvero un'applicazione x86 che utilizza funzioni AWE deve essere ricompilata per l'esecuzione in un altro processore, mentre la maggior parte delle applicazioni può essere eseguita senza ricompilare in un emulatore su altre piattaforme.

Questa soluzione risolve i problemi di memoria fisica in modo molto generale e ampiamente applicabile. Di seguito sono elencati alcuni dei vantaggi offerti da AWE:

-   Per modificare la memoria AWE viene definito un piccolo gruppo di nuove funzioni.
-   AWE fornisce una funzionalità di rimapping molto rapida. Il mapping viene eseguito modificando le tabelle di memoria virtuale, non spostando i dati nella memoria fisica.
-   AWE fornisce la granularità delle dimensioni di pagina appropriata per il processore (ad esempio, 4 KB su x86), che è più utile per le applicazioni rispetto a pagine di grandi dimensioni, ad esempio 2MB o 4 MB su x86.

Per utilizzare AWE, un'applicazione deve disporre del privilegio blocco di pagine in memoria. Per ottenere questo privilegio, un amministratore deve aggiungere le **pagine di blocco in memoria** alle **assegnazioni dei diritti utente** dell'utente. Per ulteriori informazioni su come eseguire questa operazione, vedere "diritti utente" nella guida del sistema operativo.

Le funzioni seguenti costituiscono l'API AWE (Address Windowing Extensions).



| Funzione                                                                          | Descrizione                                                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) e [ **VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex) | Riservare una parte dello spazio degli indirizzi virtuali da usare per AWE, usando la memoria **\_ fisica di MEM**.                                                                                                                                                                       |
| [**AllocateUserPhysicalPages**](/windows/win32/api/memoryapi/nf-memoryapi-allocateuserphysicalpages)                    | Allocare memoria fisica per l'utilizzo con AWE.                                                                                                                                                                                                                |
| [**MapUserPhysicalPages**](/windows/win32/api/memoryapi/nf-memoryapi-mapuserphysicalpages)                              | Mappare (o invalidare) gli indirizzi virtuali AWE su qualsiasi set di pagine fisiche ottenute con [**AllocateUserPhysicalPages**](/windows/win32/api/memoryapi/nf-memoryapi-allocateuserphysicalpages).                                                                                                    |
| [**MapUserPhysicalPagesScatter**](/windows/desktop/api/WinBase/nf-winbase-mapuserphysicalpagesscatter)                | Mappare (o invalidare) gli indirizzi virtuali AWE su qualsiasi set di pagine fisiche ottenute con [**AllocateUserPhysicalPages**](/windows/win32/api/memoryapi/nf-memoryapi-allocateuserphysicalpages), ma con un controllo più preciso rispetto a quello fornito da [**MapUserPhysicalPages**](/windows/win32/api/memoryapi/nf-memoryapi-mapuserphysicalpages). |
| [**FreeUserPhysicalPages**](/windows/win32/api/memoryapi/nf-memoryapi-freeuserphysicalpages)                            | Memoria fisica libera utilizzata per AWE.                                                                                                                                                                                                               |



 

 

 
