---
description: L'esempio seguente illustra l'uso della funzione HeapWalk per enumerare un heap.
ms.assetid: ef37d644-473f-4e51-9785-5b44fe0dce42
title: Enumerazione di un heap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c8e995dde36911947e1c510103503a99a307219bc2661a7efb9569fdab4ca20
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869841"
---
# <a name="enumerating-a-heap"></a>Enumerazione di un heap

L'esempio seguente illustra l'uso della [**funzione HeapWalk**](/windows/desktop/api/HeapApi/nf-heapapi-heapwalk) per enumerare un heap.

In primo luogo, l'esempio crea un heap privato con la [**funzione HeapCreate.**](/windows/desktop/api/HeapApi/nf-heapapi-heapcreate) Usa quindi [**HeapLock per bloccare**](/windows/desktop/api/HeapApi/nf-heapapi-heaplock) l'heap in modo che altri thread non possono accedere all'heap durante l'enumerazione. L'esempio chiama [**quindi HeapWalk**](/windows/desktop/api/HeapApi/nf-heapapi-heapwalk) con un puntatore a una struttura [**PROCESS HEAP \_ \_ ENTRY**](/windows/win32/api/minwinbase/ns-minwinbase-process_heap_entry) e scorre l'heap, stampando ogni voce nella console.

Al termine dell'enumerazione, l'esempio usa [**HeapUnlock**](/windows/desktop/api/HeapApi/nf-heapapi-heapunlock) per sbloccare l'heap in modo che altri thread possano accedervi. Infine, l'esempio chiama [**HeapDestroy per**](/windows/desktop/api/HeapApi/nf-heapapi-heapdestroy) eliminare definitivamente l'heap privato.


```C++
#include <windows.h>
#include <tchar.h>
#include <stdio.h>

int __cdecl _tmain()
{
    DWORD LastError;
    HANDLE hHeap;
    PROCESS_HEAP_ENTRY Entry;

    //
    // Create a new heap with default parameters.
    //
    hHeap = HeapCreate(0, 0, 0);
    if (hHeap == NULL) {
        _tprintf(TEXT("Failed to create a new heap with LastError %d.\n"),
                 GetLastError());
        return 1;
    }

    //
    // Lock the heap to prevent other threads from accessing the heap 
    // during enumeration.
    //
    if (HeapLock(hHeap) == FALSE) {
        _tprintf(TEXT("Failed to lock heap with LastError %d.\n"),
                 GetLastError());
        return 1;
    }

    _tprintf(TEXT("Walking heap %#p...\n\n"), hHeap);

    Entry.lpData = NULL;
    while (HeapWalk(hHeap, &Entry) != FALSE) {
        if ((Entry.wFlags & PROCESS_HEAP_ENTRY_BUSY) != 0) {
            _tprintf(TEXT("Allocated block"));

            if ((Entry.wFlags & PROCESS_HEAP_ENTRY_MOVEABLE) != 0) {
                _tprintf(TEXT(", movable with HANDLE %#p"), Entry.Block.hMem);
            }

            if ((Entry.wFlags & PROCESS_HEAP_ENTRY_DDESHARE) != 0) {
                _tprintf(TEXT(", DDESHARE"));
            }
        }
        else if ((Entry.wFlags & PROCESS_HEAP_REGION) != 0) {
            _tprintf(TEXT("Region\n  %d bytes committed\n") \
                     TEXT("  %d bytes uncommitted\n  First block address: %#p\n") \
                     TEXT("  Last block address: %#p\n"),
                     Entry.Region.dwCommittedSize,
                     Entry.Region.dwUnCommittedSize,
                     Entry.Region.lpFirstBlock,
                     Entry.Region.lpLastBlock);
        }
        else if ((Entry.wFlags & PROCESS_HEAP_UNCOMMITTED_RANGE) != 0) {
            _tprintf(TEXT("Uncommitted range\n"));
        }
        else {
            _tprintf(TEXT("Block\n"));
        }

        _tprintf(TEXT("  Data portion begins at: %#p\n  Size: %d bytes\n") \
                 TEXT("  Overhead: %d bytes\n  Region index: %d\n\n"),
                 Entry.lpData,
                 Entry.cbData,
                 Entry.cbOverhead,
                 Entry.iRegionIndex);
    }
    LastError = GetLastError();
    if (LastError != ERROR_NO_MORE_ITEMS) {
        _tprintf(TEXT("HeapWalk failed with LastError %d.\n"), LastError);
    }

    //
    // Unlock the heap to allow other threads to access the heap after 
    // enumeration has completed.
    //
    if (HeapUnlock(hHeap) == FALSE) {
        _tprintf(TEXT("Failed to unlock heap with LastError %d.\n"),
                 GetLastError());
    }

    //
    // When a process terminates, allocated memory is reclaimed by the operating
    // system so it is not really necessary to call HeapDestroy in this example.
    // However, it may be advisable to call HeapDestroy in a longer running
    // application.
    //
    if (HeapDestroy(hHeap) == FALSE) {
        _tprintf(TEXT("Failed to destroy heap with LastError %d.\n"),
                 GetLastError());
    }

    return 0;
}
```



L'output seguente mostra i risultati tipici per un heap appena creato.

``` syntax
Walking heap 0X00530000...

Region
  4096 bytes committed
  258048 bytes uncommitted
  First block address: 0X00530598
  Last block address: 0X00570000
  Data portion begins at: 0X00530000
  Size: 1416 bytes
  Overhead: 0 bytes
  Region index: 0

Block
  Data portion begins at: 0X005307D8
  Size: 2056 bytes
  Overhead: 16 bytes
  Region index: 0

Uncommitted range
  Data portion begins at: 0X00531000
  Size: 258048 bytes
  Overhead: 0 bytes
  Region index: 0
```

 

 
