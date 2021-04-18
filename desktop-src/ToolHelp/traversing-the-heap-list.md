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
# <a name="traversing-the-heap-list"></a>Attraversamento dell'elenco di heap

Nell'esempio seguente viene ottenuto un elenco di heap per il processo corrente. Acquisisce uno snapshot degli heap usando la funzione [**CreateToolhelp32Snapshot**](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot) e quindi esamina l'elenco usando le funzioni [**Heap32ListFirst**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listfirst) e [**Heap32ListNext**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listnext) . Per ogni heap, USA le funzioni [**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first) e [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) per esaminare i blocchi dell'heap.

> [!NOTE]
> [**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first) e [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) sono inefficienti, in particolare per gli heap di grandi dimensioni. Tuttavia, sono utili per eseguire query in altri processi in cui in genere è necessario inserire un thread nell'altro processo per raccogliere le informazioni. queste API eseguono questa operazione.

Vedere il secondo esempio per un'alternativa equivalente, molto più efficiente, che usa [**HEAPWALK**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) anziché [**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first) e [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next). Si noti che [**HEAPWALK**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) può essere usato solo per lo stesso processo.

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

Il frammento di codice seguente usa la funzione [**HEAPWALK**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) per esaminare gli heap del processo, producendo un output identico all'esempio precedente, ma in modo molto più efficiente:

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

L'analisi di un heap con la funzione [**HEAPWALK**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) è approssimativamente lineare nelle dimensioni dell'heap, mentre l'esplorazione di un heap con la funzione [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) è approssimativamente quadratica nelle dimensioni dell'heap.
Anche per un heap modesto con allocazioni di 10.000, [**HEAPWALK**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) esegue 10.000 volte più velocemente rispetto a [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) e fornisce informazioni più dettagliate. La differenza nelle prestazioni diventa ancora più drammatica Man mano che aumentano le dimensioni dell'heap.

Per un esempio più dettagliato di analisi dell'heap con la funzione [**HEAPWALK**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) , vedere [enumerazione di un heap](/windows/win32/memory/enumerating-a-heap).
