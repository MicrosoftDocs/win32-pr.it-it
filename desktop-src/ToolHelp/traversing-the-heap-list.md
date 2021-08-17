---
title: Attraversamento dell'elenco di heap
description: Esempi che illustrano come ottenere un elenco di heap per il processo corrente.
ms.assetid: cfa1d2a4-fec0-4089-9351-e0a26f9ecfe3
ms.topic: article
ms.date: 03/23/2021
ms.openlocfilehash: 868526c76ee85095f5b52cc9238e9e16015bfb3a81c9888da148f1d5ecc644aa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119419251"
---
# <a name="traversing-the-heap-list"></a>Attraversamento dell'elenco di heap

Nell'esempio seguente viene ottenuto un elenco di heap per il processo corrente. Crea uno snapshot degli heap usando la funzione [**CreateToolhelp32Snapshot**](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot) e quindi illustra l'elenco usando le funzioni [**Heap32ListFirst**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listfirst) e [**Heap32ListNext.**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listnext) Per ogni heap, usa le funzioni [**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first) e [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) per eseguire il percorso dei blocchi heap.

> [!NOTE]
> [**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first) e [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) sono inefficienti, in particolare per heap di grandi dimensioni. Tuttavia, sono utili per l'esecuzione di query su altri processi in cui in genere è necessario inserire un thread nell'altro processo per raccogliere le informazioni (queste API lo fanno automaticamente).

Vedere il secondo esempio per un'alternativa equivalente, molto più efficiente, che usa [**HeapWalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) anziché [**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first) [**e Heap32Next.**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) Si noti [**che HeapWalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) può essere usato solo per lo stesso processo.

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

Il frammento di codice seguente usa la funzione [**HeapWalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) per tracciare gli heap dei processi, producendo un output identico all'esempio precedente, ma molto più efficiente:

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

L'analisi di un heap con la funzione [**HeapWalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) è approssimativamente lineare nelle dimensioni dell'heap, mentre l'analisi di un heap con la funzione [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) è approssimativamente quadratica nelle dimensioni dell'heap.
Anche per un heap modere con 10.000 allocazioni, [**HeapWalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) viene eseguito 10.000 volte più veloce di [**Heap32Next,**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) fornendo al tempo stesso informazioni più dettagliate. La differenza di prestazioni diventa ancora più significativa con l'aumentare delle dimensioni dell'heap.

Per un esempio più dettagliato dell'analisi dell'heap con la [**funzione HeapWalk,**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) vedere [Enumerazione di un heap.](/windows/win32/memory/enumerating-a-heap)
