---
Description: Di seguito è riportato un breve confronto tra i vari metodi di allocazione della memoria.
ms.assetid: b6101014-02d2-4b19-aec6-8772a2793d38
title: Confronto tra i metodi di allocazione della memoria
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: 541b314c4ff0553ff8812e591c47c87962866bbe
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/10/2021
ms.locfileid: "103969287"
---
# <a name="comparing-memory-allocation-methods"></a>Confronto tra i metodi di allocazione della memoria

Di seguito è riportato un breve confronto tra i vari metodi di allocazione della memoria:

-   [**CoTaskMemAlloc**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc)
-   [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc)
-   [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc)
-   [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc)
-   **malloc**
-   **Nuovo**
-   [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc)

Sebbene le funzioni [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc), [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc)e [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) riallocano la memoria dallo stesso heap, ognuna fornisce un set di funzionalità leggermente diverso. Ad esempio, è possibile indicare a **HeapAlloc** di generare un'eccezione se non è stato possibile allocare memoria, una funzionalità non disponibile con **LocalAlloc**. **LocalAlloc** supporta l'allocazione di handle che consentono lo spostamento della memoria sottostante da parte di una riallocazione senza modificare il valore dell'handle, una funzionalità non disponibile con **HeapAlloc**.

A partire da Windows a 32 bit, [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc) e [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc) vengono implementati come funzioni wrapper che chiamano [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) usando un handle per l'heap predefinito del processo. Pertanto, **GlobalAlloc** e **LocalAlloc** hanno un overhead maggiore di **HeapAlloc**.

Poiché i diversi allocatori di heap forniscono funzionalità distintive usando meccanismi diversi, è necessario liberare memoria con la funzione corretta. Ad esempio, la memoria allocata con [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) deve essere liberata con [**HeapFree**](/windows/desktop/api/HeapApi/nf-heapapi-heapfree) e non con [**LocalFree**](/windows/desktop/api/WinBase/nf-winbase-localfree) o [**GlobalFree**](/windows/desktop/api/WinBase/nf-winbase-globalfree). La memoria allocata con [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc) o [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc) deve essere sottoposta a query, convalidata e rilasciata con la funzione globale o locale corrispondente.

La funzione [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) consente di specificare opzioni aggiuntive per l'allocazione di memoria. Tuttavia, le relative allocazioni utilizzano una granularità di pagina, pertanto l'utilizzo di **VirtualAlloc** può comportare un utilizzo maggiore della memoria.

La funzione **malloc** presenta lo svantaggio di essere dipendente dalla fase di esecuzione. L'operatore **New** presenta lo svantaggio di essere dipendente dal compilatore e dipendente dalla lingua.

La funzione [**CoTaskMemAlloc**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc) offre il vantaggio di funzionare correttamente in C, C++ o Visual Basic. È anche l'unico modo per condividere memoria in un'applicazione basata su COM, perché MIDL USA **CoTaskMemAlloc** e [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) per effettuare il marshalling della memoria.


## <a name="examples"></a>Esempio

* [Riserva e commit della memoria](./reserving-and-committing-memory.md)

* [Esempio AWE](./awe-example.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Funzioni globali e locali](global-and-local-functions.md)
</dt> <dt>

[Funzioni heap](heap-functions.md)
</dt> <dt>

[Funzioni di memoria virtuale](virtual-memory-functions.md)
</dt> </dl>

 

 