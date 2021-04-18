---
description: Nell'esempio seguente viene usata la funzione InitializeSListHead per inizializzare un elenco collegato singolarmente e la funzione InterlockedPushEntrySList per inserire 10 elementi.
ms.assetid: 5608f84f-9211-4043-bb53-60339191ee29
title: Uso di elenchi collegati singolarmente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95af2e8da519026731bf6fc461b193978d179cd8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316065"
---
# <a name="using-singly-linked-lists"></a>Uso di elenchi collegati singolarmente

Nell'esempio seguente viene usata la funzione [**InitializeSListHead**](/windows/win32/api/interlockedapi/nf-interlockedapi-initializeslisthead) per inizializzare un [elenco collegato singolarmente](interlocked-singly-linked-lists.md) e la funzione [**InterlockedPushEntrySList**](/windows/win32/api/interlockedapi/nf-interlockedapi-interlockedpushentryslist) per inserire 10 elementi. Nell'esempio viene usata la funzione [**InterlockedPopEntrySList**](/windows/win32/api/interlockedapi/nf-interlockedapi-interlockedpopentryslist) per rimuovere 10 elementi e la funzione [**InterlockedFlushSList**](/windows/win32/api/interlockedapi/nf-interlockedapi-interlockedflushslist) per verificare che l'elenco sia vuoto.


```C++
#include <windows.h>
#include <malloc.h>
#include <stdio.h>

// Structure to be used for a list item; the first member is the 
// SLIST_ENTRY structure, and additional members are used for data.
// Here, the data is simply a signature for testing purposes. 


typedef struct _PROGRAM_ITEM {
    SLIST_ENTRY ItemEntry;
    ULONG Signature; 
} PROGRAM_ITEM, *PPROGRAM_ITEM;

int main( )
{
    ULONG Count;
    PSLIST_ENTRY pFirstEntry, pListEntry;
    PSLIST_HEADER pListHead;
    PPROGRAM_ITEM pProgramItem;

    // Initialize the list header to a MEMORY_ALLOCATION_ALIGNMENT boundary.
    pListHead = (PSLIST_HEADER)_aligned_malloc(sizeof(SLIST_HEADER),
       MEMORY_ALLOCATION_ALIGNMENT);
    if( NULL == pListHead )
    {
        printf("Memory allocation failed.\n");
        return -1;
    }
    InitializeSListHead(pListHead);

    // Insert 10 items into the list.
    for( Count = 1; Count <= 10; Count += 1 )
    {
        pProgramItem = (PPROGRAM_ITEM)_aligned_malloc(sizeof(PROGRAM_ITEM),
            MEMORY_ALLOCATION_ALIGNMENT);
        if( NULL == pProgramItem )
        {
            printf("Memory allocation failed.\n");
            return -1;
        }
        pProgramItem->Signature = Count;
        pFirstEntry = InterlockedPushEntrySList(pListHead, 
                       &(pProgramItem->ItemEntry)); 
    }

    // Remove 10 items from the list and display the signature.
    for( Count = 10; Count >= 1; Count -= 1 )
    {
        pListEntry = InterlockedPopEntrySList(pListHead);

        if( NULL == pListEntry )
        {
            printf("List is empty.\n");
            return -1;
        }
  
        pProgramItem = (PPROGRAM_ITEM)pListEntry;
        printf("Signature is %d\n", pProgramItem->Signature);

    // This example assumes that the SLIST_ENTRY structure is the 
    // first member of the structure. If your structure does not 
    // follow this convention, you must compute the starting address 
    // of the structure before calling the free function.

        _aligned_free(pListEntry);
    }

    // Flush the list and verify that the items are gone.
    pListEntry = InterlockedFlushSList(pListHead);
    pFirstEntry = InterlockedPopEntrySList(pListHead);
    if (pFirstEntry != NULL)
    {
        printf("Error: List is not empty.\n");
        return -1;
    }

    _aligned_free(pListHead);

    return 1;
}

```



 

 
