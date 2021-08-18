---
description: Questo esempio illustra l'uso della funzione GetProcessHeaps per recuperare gli handle per l'heap del processo predefinito ed eventuali heap privati attivi per il processo corrente.
ms.assetid: 00f69593-f03b-4f30-aeec-db3fda0ac356
title: Recupero degli heap dei processi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52b055bd558d12506d5a900c369365cb497e3817dbfa1fd53dd6506f6a919eab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067841"
---
# <a name="getting-process-heaps"></a>Recupero degli heap dei processi

Questo esempio illustra l'uso della funzione [**GetProcessHeaps**](/windows/desktop/api/HeapApi/nf-heapapi-getprocessheaps) per recuperare gli handle per l'heap del processo predefinito ed eventuali heap privati attivi per il processo corrente.

L'esempio [**chiama GetProcessHeaps**](/windows/desktop/api/HeapApi/nf-heapapi-getprocessheaps) due volte, prima per calcolare le dimensioni del buffer necessario e di nuovo per recuperare gli handle nel buffer. Il buffer viene allocato dall'heap del processo predefinito, usando l'handle restituito da [**GetProcessHeap.**](/windows/desktop/api/HeapApi/nf-heapapi-getprocessheap) L'esempio stampa l'indirizzo iniziale di ogni heap nella console. Usa quindi la funzione [**HeapFree**](/windows/desktop/api/HeapApi/nf-heapapi-heapfree) per liberare la memoria allocata per il buffer.

Il numero di heap in un processo può variare. Un processo ha sempre almeno un heap, ovvero l'heap del processo predefinito, e può avere uno o più heap privati creati dall'applicazione o dalle DLL caricate nello spazio degli indirizzi del processo.

Si noti che un'applicazione deve chiamare le funzioni heap solo nell'heap del processo predefinito o negli heap privati creati dall'applicazione. La chiamata di funzioni heap su un heap privato di proprietà di un altro componente può causare un comportamento indefinito.


```C++
#include <windows.h>
#include <tchar.h>
#include <stdio.h>
#include <intsafe.h>

int __cdecl _tmain()
{
    DWORD NumberOfHeaps;
    DWORD HeapsIndex;
    DWORD HeapsLength;
    HANDLE hDefaultProcessHeap;
    HRESULT Result;
    PHANDLE aHeaps;
    SIZE_T BytesToAllocate;

    //
    // Retrieve the number of active heaps for the current process
    // so we can calculate the buffer size needed for the heap handles.
    //
    NumberOfHeaps = GetProcessHeaps(0, NULL);
    if (NumberOfHeaps == 0) {
        _tprintf(TEXT("Failed to retrieve the number of heaps with LastError %d.\n"),
                 GetLastError());
        return 1;
    }

    //
    // Calculate the buffer size.
    //
    Result = SIZETMult(NumberOfHeaps, sizeof(*aHeaps), &BytesToAllocate);
    if (Result != S_OK) {
        _tprintf(TEXT("SIZETMult failed with HR %d.\n"), Result);
        return 1;
    }

    //
    // Get a handle to the default process heap.
    //
    hDefaultProcessHeap = GetProcessHeap();
    if (hDefaultProcessHeap == NULL) {
        _tprintf(TEXT("Failed to retrieve the default process heap with LastError %d.\n"),
                 GetLastError());
        return 1;
    }

    //
    // Allocate the buffer from the default process heap.
    //
    aHeaps = (PHANDLE)HeapAlloc(hDefaultProcessHeap, 0, BytesToAllocate);
    if (aHeaps == NULL) {
        _tprintf(TEXT("HeapAlloc failed to allocate %d bytes.\n"),
                 BytesToAllocate);
        return 1;
    }

    // 
    // Save the original number of heaps because we are going to compare it
    // to the return value of the next GetProcessHeaps call.
    //
    HeapsLength = NumberOfHeaps;

    //
    // Retrieve handles to the process heaps and print them to stdout. 
    // Note that heap functions should be called only on the default heap of the process
    // or on private heaps that your component creates by calling HeapCreate.
    //
    NumberOfHeaps = GetProcessHeaps(HeapsLength, aHeaps);
    if (NumberOfHeaps == 0) {
        _tprintf(TEXT("Failed to retrieve heaps with LastError %d.\n"),
                 GetLastError());
        return 1;
    }
    else if (NumberOfHeaps > HeapsLength) {

        //
        // Compare the latest number of heaps with the original number of heaps.
        // If the latest number is larger than the original number, another
        // component has created a new heap and the buffer is too small.
        //
        _tprintf(TEXT("Another component created a heap between calls. ") \
                 TEXT("Please try again.\n"));
        return 1;
    }

    _tprintf(TEXT("Process has %d heaps.\n"), HeapsLength);
    for (HeapsIndex = 0; HeapsIndex < HeapsLength; ++HeapsIndex) {
        _tprintf(TEXT("Heap %d at address: %#p.\n"),
                 HeapsIndex,
                 aHeaps[HeapsIndex]);
    }
  
    //
    // Release memory allocated from default process heap.
    //
    if (HeapFree(hDefaultProcessHeap, 0, aHeaps) == FALSE) {
        _tprintf(TEXT("Failed to free allocation from default process heap.\n"));
    }

    return 0;
}
```



 

 



