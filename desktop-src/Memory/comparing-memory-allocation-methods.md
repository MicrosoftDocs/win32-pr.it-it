---
Description: Di seguito è riportato un breve confronto tra i vari metodi di allocazione della memoria.
ms.assetid: b6101014-02d2-4b19-aec6-8772a2793d38
title: Confronto dei metodi di allocazione di memoria
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: 418ebbf96b1d6f714e1ae7f23f1c15e918ea0c6fa7eabdf7bb9157bb14808bb2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067901"
---
# <a name="comparing-memory-allocation-methods"></a>Confronto dei metodi di allocazione di memoria

Di seguito è riportato un breve confronto tra i vari metodi di allocazione della memoria:

-   [**Cotaskmemalloc**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc)
-   [**Globalalloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc)
-   [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc)
-   [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc)
-   **malloc**
-   **Nuovo**
-   [**Virtualalloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc)

Anche se [**le funzioni GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc), [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc)e [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) allocano infine memoria dallo stesso heap, ognuna offre un set leggermente diverso di funzionalità. Ad esempio, è possibile indicare a **HeapAlloc** di generare un'eccezione se non è stato possibile allocare memoria, una funzionalità non disponibile con **LocalAlloc**. **LocalAlloc** supporta l'allocazione di handle che consentono lo spostamento della memoria sottostante da una riallocazione senza modificare il valore dell'handle, una funzionalità non disponibile con **HeapAlloc**.

A partire da Windows a 32 bit, [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc) e [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc) vengono implementati come funzioni wrapper che chiamano [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) usando un handle per l'heap predefinito del processo. Pertanto, **GlobalAlloc** e **LocalAlloc** hanno un sovraccarico maggiore rispetto **a HeapAlloc**.

Poiché i diversi allocatori di heap forniscono funzionalità distintive usando meccanismi diversi, è necessario liberare memoria con la funzione corretta. Ad esempio, la memoria allocata [**con HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) deve essere liberata [**con HeapFree**](/windows/desktop/api/HeapApi/nf-heapapi-heapfree) e non [**con LocalFree**](/windows/desktop/api/WinBase/nf-winbase-localfree) [**o GlobalFree**](/windows/desktop/api/WinBase/nf-winbase-globalfree). La memoria [**allocata con GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc) o [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc) deve essere eseguita una query, convalidata e rilasciata con la funzione globale o locale corrispondente.

La [**funzione VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) consente di specificare opzioni aggiuntive per l'allocazione della memoria. Tuttavia, le allocazioni usano una granularità di pagina, quindi l'uso **di VirtualAlloc** può comportare un utilizzo più elevato della memoria.

La **funzione malloc** presenta lo svantaggio di essere dipendente dal run-time. **L'operatore new** presenta lo svantaggio di essere dipendente dal compilatore e dipendente dal linguaggio.

La [**funzione CoTaskMemAlloc**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc) ha il vantaggio di funzionare correttamente in C, C++ o Visual Basic. È anche l'unico modo per condividere la memoria in un'applicazione basata su COM, poiché MIDL usa **CoTaskMemAlloc** e [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) per effettuare il marshalling della memoria.


## <a name="examples"></a>Esempio

* [Prenotazione e commit della memoria](./reserving-and-committing-memory.md)

* [Esempio AWE](./awe-example.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Funzioni globali e locali](global-and-local-functions.md)
</dt> <dt>

[Funzioni heap](heap-functions.md)
</dt> <dt>

[Funzioni di memoria virtuale](virtual-memory-functions.md)
</dt> </dl>

 

 