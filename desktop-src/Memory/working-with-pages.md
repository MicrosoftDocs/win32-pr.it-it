---
description: Per determinare le dimensioni di una pagina nel computer corrente, utilizzare la funzione GetSystemInfo.
ms.assetid: 953ddfc4-6126-41fb-81a3-0ce1f0fb223f
title: Uso delle pagine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66c12c99ada03dca1e17c72c2a5f0d5360b6a98d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527264"
---
# <a name="working-with-pages"></a>Uso delle pagine

Per determinare le dimensioni di una pagina nel computer corrente, utilizzare la funzione [**GetSystemInfo**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) .

Le funzioni [**VirtualQuery**](/windows/win32/api/memoryapi/nf-memoryapi-virtualquery) e [**VirtualQueryEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualqueryex) restituiscono informazioni su un'area di pagine consecutive a partire da un indirizzo specificato nello spazio degli indirizzi di un processo. **VirtualQuery** restituisce informazioni sulla memoria nel processo chiamante. **VirtualQueryEx** restituisce informazioni sulla memoria in un processo specificato e viene utilizzato per supportare i debugger che necessitano di informazioni su un processo di cui è in corso il debug. L'area delle pagine è vincolata dall'indirizzo specificato arrotondato per difetto al limite di pagina più vicino. Si estende attraverso tutte le pagine successive con gli attributi seguenti in comune:

-   Lo stato di tutte le pagine è lo stesso: commit, riservato o gratuito.
-   Se la pagina iniziale non è disponibile, tutte le pagine dell'area fanno parte della stessa allocazione iniziale delle pagine riservate da una chiamata a [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc).
-   La protezione degli accessi di tutte le pagine è la stessa, ovvero **pagina \_ ReadOnly**, **pagina \_ ReadWrite** o **pagina \_ NoAccess**.

La funzione [**VirtualLock**](/windows/win32/api/memoryapi/nf-memoryapi-virtuallock) consente a un processo di bloccare una o più pagine di memoria di cui è stato eseguito il commit nella memoria fisica (RAM), impedendo al sistema di scambiare le pagine nel file di paging. Può essere usato per garantire che i dati critici siano accessibili senza l'accesso al disco. Il blocco di pagine in memoria è pericoloso perché limita la capacità di gestione della memoria da parte del sistema. Un utilizzo eccessivo di **VirtualLock** può influire negativamente sulle prestazioni del sistema, causando lo swapping del codice eseguibile nel file di paging. La funzione [**VirtualUnlock**](/windows/win32/api/memoryapi/nf-memoryapi-virtualunlock) Sblocca la memoria bloccata da **VirtualLock**.

La funzione [**VirtualProtect**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotect) consente a un processo di modificare la protezione dell'accesso di qualsiasi pagina di cui è stato eseguito il commit nello spazio degli indirizzi di un processo. Un processo, ad esempio, può allocare pagine di lettura/scrittura per archiviare dati sensibili, quindi può modificare l'accesso in sola lettura o nessun accesso per la protezione da sovrascrittura accidentale. **VirtualProtect** viene in genere usato con le pagine allocate da [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc), ma funziona anche con le pagine di cui è stato eseguito il commit da qualsiasi altra funzione di allocazione. Tuttavia, **VirtualProtect** modifica la protezione di intere pagine e i puntatori restituiti dalle altre funzioni non sono necessariamente allineati ai limiti della pagina. La funzione [**VirtualProtectEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotectex) è simile a **VirtualProtect**, con la differenza che modifica la protezione della memoria in un processo specificato. La modifica della protezione è utile per i debugger che accedono alla memoria di un processo di cui è in corso il debug.

 

 
