---
description: Tutta la memoria allocata da un processo usando le funzioni di allocazione di memoria ( HeapAlloc, VirtualAlloc, GlobalAlloc o LocalAlloc) è accessibile solo al processo.
ms.assetid: b47200dc-6824-4fd8-8d9f-2aaa439a74ff
title: Ambito della memoria allocata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f06b0ee3f9446962bb508c23d4c5542fd16168027c5913b63438d16b6cea910
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067671"
---
# <a name="scope-of-allocated-memory"></a>Ambito della memoria allocata

Tutta la memoria allocata da un processo usando le funzioni di allocazione di memoria ( [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc), [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc), [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc) [**o LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc)) è accessibile solo al processo. Tuttavia, la memoria allocata da una DLL viene allocata nello spazio indirizzi del processo che ha chiamato la DLL e non è accessibile ad altri processi che usano la stessa DLL. Per creare la memoria condivisa, è necessario usare il mapping dei file.

Il mapping di file denominato offre un modo semplice per creare un blocco di memoria condivisa. Un processo può specificare un nome quando usa la [**funzione CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) per creare un oggetto di mapping file. Altri processi possono specificare lo stesso nome per la **funzione CreateFileMapping** o [**OpenFileMapping**](/windows/desktop/api/WinBase/nf-winbase-openfilemappinga) per ottenere un handle per l'oggetto mapping.

Ogni processo specifica l'handle per l'oggetto di mapping dei file nella funzione [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) per eseguire il mapping di una vista del file nel proprio spazio indirizzi. Le visualizzazioni di tutti i processi per un singolo oggetto di mapping di file vengono mappate nelle stesse pagine di archiviazione fisica. Tuttavia, gli indirizzi virtuali delle viste mappate possono variare da un processo a un altro, a meno che non venga usata la funzione [**MapViewOfFileEx**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffileex) per eseguire il mapping della vista a un indirizzo specificato. Sebbene sia possibile eseguire la condivisione, le pagine di archiviazione fisica usate per una visualizzazione di file mappata non sono globali. non sono accessibili ai processi che non hanno eseguito il mapping di una visualizzazione del file.

Tutte le pagine di cui è stato eseguito il mapping tramite mapping di una visualizzazione di un file vengono rilasciate quando l'ultimo processo con una visualizzazione dell'oggetto mapping termina o annulla il mapping della visualizzazione chiamando la funzione [**UnmapViewOfFile.**](/windows/win32/api/memoryapi/nf-memoryapi-unmapviewoffile) Al momento, viene aggiornato il file specificato (se presente) associato all'oggetto mapping. È anche possibile forzare l'aggiornamento di un file specificato chiamando la [**funzione FlushViewOfFile.**](/windows/win32/api/memoryapi/nf-memoryapi-flushviewoffile)

Per altre informazioni, vedere [Mapping dei file](file-mapping.md). Per un esempio di memoria condivisa in una DLL, vedere [Using Shared Memory in a Dynamic-Link Library](../dlls/using-shared-memory-in-a-dynamic-link-library.md).

Se più processi hanno accesso in scrittura alla memoria condivisa, è necessario sincronizzare l'accesso alla memoria. Per altre informazioni, vedere [Sincronizzazione](../sync/synchronization.md).

 

 
