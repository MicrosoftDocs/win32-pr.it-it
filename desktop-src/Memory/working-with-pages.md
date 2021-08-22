---
description: Per determinare le dimensioni di una pagina nel computer corrente, usare la funzione GetSystemInfo.
ms.assetid: 953ddfc4-6126-41fb-81a3-0ce1f0fb223f
title: Uso delle pagine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e47e8a352b13c12b38acca1a93f12886d83d24c4d43faa213a88cf5855b18c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067661"
---
# <a name="working-with-pages"></a>Uso delle pagine

Per determinare le dimensioni di una pagina nel computer corrente, usare la [**funzione GetSystemInfo.**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo)

Le [**funzioni VirtualQuery**](/windows/win32/api/memoryapi/nf-memoryapi-virtualquery) [**e VirtualQueryEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualqueryex) restituiscono informazioni su un'area di pagine consecutive che iniziano in corrispondenza di un indirizzo specificato nello spazio indirizzi di un processo. **VirtualQuery** restituisce informazioni sulla memoria nel processo chiamante. **VirtualQueryEx restituisce** informazioni sulla memoria in un processo specificato e viene usato per supportare i debugger che necessitano di informazioni su un processo in fase di debug. L'area delle pagine è delimitata dall'indirizzo specificato arrotondato per e per intero al limite di pagina più vicino. Si estende in tutte le pagine successive con gli attributi seguenti in comune:

-   Lo stato di tutte le pagine è lo stesso: commit, riservato o gratuito.
-   Se la pagina iniziale non è libera, tutte le pagine nell'area fanno parte della stessa allocazione iniziale di pagine riservate da una chiamata a [**VirtualAlloc.**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc)
-   La protezione dell'accesso di tutte le pagine è la stessa, ovvero **PAGE \_ READONLY,** **PAGE \_ READWRITE** o **PAGE \_ NOACCESS.**

La [**funzione VirtualLock**](/windows/win32/api/memoryapi/nf-memoryapi-virtuallock) consente a un processo di bloccare una o più pagine di memoria di cui è stato eseguito il commit nella memoria fisica (RAM), impedendo al sistema di scambiare le pagine nel file di paging. Può essere usato per garantire che i dati critici siano accessibili senza accesso al disco. Bloccare le pagine in memoria è pericoloso perché limita la capacità del sistema di gestire la memoria. Un uso eccessivo di **VirtualLock** può ridurre le prestazioni del sistema causando lo scambio del codice eseguibile nel file di paging. La [**funzione VirtualUnlock**](/windows/win32/api/memoryapi/nf-memoryapi-virtualunlock) sblocca la memoria bloccata da **VirtualLock**.

La [**funzione VirtualProtect**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotect) consente a un processo di modificare la protezione dell'accesso di qualsiasi pagina di cui è stato eseguito il commit nello spazio indirizzi di un processo. Ad esempio, un processo può allocare pagine di lettura/scrittura per archiviare dati sensibili e quindi può modificare l'accesso in sola lettura o nessun accesso per proteggersi dalla sovrascrittura accidentale. **VirtualProtect viene** in genere usato con le pagine allocate da [**VirtualAlloc,**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc)ma funziona anche con le pagine di cui è stato eseguito il commit da una delle altre funzioni di allocazione. Tuttavia, **VirtualProtect** modifica la protezione di intere pagine e i puntatori restituiti dalle altre funzioni non sono necessariamente allineati ai limiti della pagina. La [**funzione VirtualProtectEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotectex) è simile a **VirtualProtect,** ad eccezione del fatto che modifica la protezione della memoria in un processo specificato. La modifica della protezione è utile per i debugger nell'accesso alla memoria di un processo in fase di debug.

 

 
