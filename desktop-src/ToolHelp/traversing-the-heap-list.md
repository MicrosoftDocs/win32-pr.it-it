---
title: Attraversamento dell'elenco di heap
description: Esempi che illustrano come ottenere un elenco di heap per il processo corrente.
ms.assetid: cfa1d2a4-fec0-4089-9351-e0a26f9ecfe3
ms.topic: article
ms.date: 03/23/2021
ms.openlocfilehash: 5cc555f9a94166fa181309985d8a49c686baf06c
ms.sourcegitcommit: 4af3e9ec3142ba499d20ed8b174c2b219c5eacd2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/30/2021
ms.locfileid: "106334294"
---
# <a name="traversing-the-heap-list"></a><span data-ttu-id="40a08-103">Attraversamento dell'elenco di heap</span><span class="sxs-lookup"><span data-stu-id="40a08-103">Traversing the Heap List</span></span>

<span data-ttu-id="40a08-104">Nell'esempio seguente viene ottenuto un elenco di heap per il processo corrente.</span><span class="sxs-lookup"><span data-stu-id="40a08-104">The following example obtains a list of heaps for the current process.</span></span> <span data-ttu-id="40a08-105">Acquisisce uno snapshot degli heap usando la funzione [**CreateToolhelp32Snapshot**](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot) e quindi esamina l'elenco usando le funzioni [**Heap32ListFirst**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listfirst) e [**Heap32ListNext**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listnext) .</span><span class="sxs-lookup"><span data-stu-id="40a08-105">It takes a snapshot of the heaps using the [**CreateToolhelp32Snapshot**](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot) function, and then walks through the list using the [**Heap32ListFirst**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listfirst) and [**Heap32ListNext**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listnext) functions.</span></span> <span data-ttu-id="40a08-106">Per ogni heap, USA le funzioni [**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first) e [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) per esaminare i blocchi dell'heap.</span><span class="sxs-lookup"><span data-stu-id="40a08-106">For each heap, it uses the [**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first) and [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) functions to walk the heap blocks.</span></span>

> [!NOTE]
> <span data-ttu-id="40a08-107">[**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first) e [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) sono inefficienti, in particolare per gli heap di grandi dimensioni.</span><span class="sxs-lookup"><span data-stu-id="40a08-107">[**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first) and [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) are inefficient, particularly for large heaps.</span></span> <span data-ttu-id="40a08-108">Tuttavia, sono utili per eseguire query in altri processi in cui in genere è necessario inserire un thread nell'altro processo per raccogliere le informazioni. queste API eseguono questa operazione.</span><span class="sxs-lookup"><span data-stu-id="40a08-108">However, they are useful for querying other processes where you'd typically have to inject a thread into the other process to gather the information (these APIs do this for you).</span></span>

<span data-ttu-id="40a08-109">Vedere il secondo esempio per un'alternativa equivalente, molto più efficiente, che usa [**HEAPWALK**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) anziché [**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first) e [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next).</span><span class="sxs-lookup"><span data-stu-id="40a08-109">See the second example for an equivalent, much more efficient, alternative that uses [**HeapWalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) instead of [**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first) and [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next).</span></span> <span data-ttu-id="40a08-110">Si noti che [**HEAPWALK**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) può essere usato solo per lo stesso processo.</span><span class="sxs-lookup"><span data-stu-id="40a08-110">Note that [**HeapWalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) can only be used for the same process.</span></span>

```C++
#include <windows.h>
#include <tlhelp32.h>
#include <stdio.h>

int main( void )
{
   HEAPLIST32 hl;
   
   HANDLE hHeapSnap = CreateToolhelp32Snapshot(TH32CS_SNAPHEAPLIST, GetCurrentProcessId());
   
   hl.dwSize = sizeof(HEAPLIST32);
   
   if ( hHeapSnap == INVALID_HANDLE_VALUE )
   {
      printf ("CreateToolhelp32Snapshot failed (%d)\n", GetLastError());
      return 1;
   }
   
   if( Heap32ListFirst( hHeapSnap, &hl ) )
   {
      do
      {
         HEAPENTRY32 he;
         ZeroMemory(&he, sizeof(HEAPENTRY32));
         he.dwSize = sizeof(HEAPENTRY32);

         if( Heap32First( &he, GetCurrentProcessId(), hl.th32HeapID ) )
         {
            printf( "\nHeap ID: %d\n", hl.th32HeapID );
            do
            {
               printf( "Block size: %d\n", he.dwBlockSize );
               
               he.dwSize = sizeof(HEAPENTRY32);
            } while( Heap32Next(&he) );
         }
         hl.dwSize = sizeof(HEAPLIST32);
      } while (Heap32ListNext( hHeapSnap, &hl ));
   }
   else printf ("Cannot list first heap (%d)\n", GetLastError());
   
   CloseHandle(hHeapSnap); 

   return 0;
}
```

<span data-ttu-id="40a08-111">Il frammento di codice seguente usa la funzione [**HEAPWALK**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) per esaminare gli heap del processo, producendo un output identico all'esempio precedente, ma in modo molto più efficiente:</span><span class="sxs-lookup"><span data-stu-id="40a08-111">The following code snippet uses the [**HeapWalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) function to walk the process heaps, producing identical output to the previous example, but much more efficiently:</span></span>

```C++
#include <windows.h>
#include <stdio.h>

int main( void )
{
    DWORD heapIndex;
    DWORD heapCount = 0;
    PHANDLE heaps = NULL;
    while (TRUE)
    {
        DWORD actualHeapCount = GetProcessHeaps(heapCount, heaps);
        if (actualHeapCount <= heapCount)
        {
            break;
        }
        heapCount = actualHeapCount;
        free(heaps);
        heaps = (HANDLE*)malloc(heapCount * sizeof(HANDLE));
        if (heaps == NULL)
        {
            printf("Unable to allocate memory for list of heaps\n");
            return 1;
        }
    }

    for (heapIndex = 0; heapIndex < heapCount; heapIndex++)
    {
        PROCESS_HEAP_ENTRY entry;

        printf("Heap ID: %d\n", (DWORD)(ULONG_PTR)heaps[heapIndex]);
        entry.lpData = NULL;
        while (HeapWalk(heaps[heapIndex], &entry))
        {
            // Heap32First and Heap32Next ignore entries
            // with the PROCESS_HEAP_REGION flag
            if (!(entry.wFlags & PROCESS_HEAP_REGION))
            {
                printf("Block size: %d\n", entry.cbData + entry.cbOverhead);
            }
        }
    }

    free(heaps);
    return 0;
}
```

<span data-ttu-id="40a08-112">L'analisi di un heap con la funzione [**HEAPWALK**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) è approssimativamente lineare nelle dimensioni dell'heap, mentre l'esplorazione di un heap con la funzione [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) è approssimativamente quadratica nelle dimensioni dell'heap.</span><span class="sxs-lookup"><span data-stu-id="40a08-112">Walking a heap with the [**HeapWalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) function is roughly linear in the size of the heap, whereas walking a heap with the [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) function is roughly quadratic in the size of the heap.</span></span>
<span data-ttu-id="40a08-113">Anche per un heap modesto con allocazioni di 10.000, [**HEAPWALK**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) esegue 10.000 volte più velocemente rispetto a [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) e fornisce informazioni più dettagliate.</span><span class="sxs-lookup"><span data-stu-id="40a08-113">Even for a modest heap with 10,000 allocations, [**HeapWalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) runs 10,000 times faster than [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) while providing more detailed information.</span></span> <span data-ttu-id="40a08-114">La differenza nelle prestazioni diventa ancora più drammatica Man mano che aumentano le dimensioni dell'heap.</span><span class="sxs-lookup"><span data-stu-id="40a08-114">The difference in performance becomes even more dramatic as the heap size increases.</span></span>

<span data-ttu-id="40a08-115">Per un esempio più dettagliato di analisi dell'heap con la funzione [**HEAPWALK**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) , vedere [enumerazione di un heap](/windows/win32/memory/enumerating-a-heap).</span><span class="sxs-lookup"><span data-stu-id="40a08-115">For a more detailed example of walking the heap with the [**HeapWalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) function, see [Enumerating a Heap](/windows/win32/memory/enumerating-a-heap).</span></span>
