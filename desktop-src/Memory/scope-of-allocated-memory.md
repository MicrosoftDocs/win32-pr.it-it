---
description: Tutta la memoria allocata da un processo usando le funzioni di allocazione della memoria (HeapAlloc, VirtualAlloc, GlobalAlloc o LocalAlloc) è accessibile solo al processo.
ms.assetid: b47200dc-6824-4fd8-8d9f-2aaa439a74ff
title: Ambito della memoria allocata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8d2db67a04c019683e737d0f9c581ce8d16b800
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226254"
---
# <a name="scope-of-allocated-memory"></a>Ambito della memoria allocata

Tutta la memoria allocata da un processo usando le funzioni di allocazione della memoria ( [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc), [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc), [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc)o [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc)) è accessibile solo al processo. Tuttavia, la memoria allocata da una DLL viene allocata nello spazio degli indirizzi del processo che ha chiamato la DLL e non è accessibile ad altri processi che usano la stessa DLL. Per creare la memoria condivisa, è necessario utilizzare il mapping dei file.

Il mapping dei file denominati fornisce un modo semplice per creare un blocco di memoria condivisa. Un processo può specificare un nome quando usa la funzione [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) per creare un oggetto mapping di file. Altri processi possono specificare lo stesso nome per la funzione **CreateFileMapping** o [**OpenFileMapping**](/windows/desktop/api/WinBase/nf-winbase-openfilemappinga) per ottenere un handle per l'oggetto di mapping.

Ogni processo specifica il relativo handle per l'oggetto di mapping dei file nella funzione [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) per eseguire il mapping di una visualizzazione del file nel proprio spazio degli indirizzi. Le visualizzazioni di tutti i processi per un singolo oggetto mapping di file sono mappate alle stesse pagine condivisibili di archiviazione fisica. Tuttavia, gli indirizzi virtuali delle visualizzazioni mappate possono variare da un processo a un altro, a meno che non venga usata la funzione [**MapViewOfFileEx**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffileex) per eseguire il mapping della vista in corrispondenza di un indirizzo specificato. Sebbene condivisibili, le pagine di archiviazione fisica utilizzate per una visualizzazione file mappata non sono globali. non sono accessibili ai processi che non hanno eseguito il mapping di una visualizzazione del file.

Tutte le pagine sottoposte a commit eseguendo il mapping di una vista di un file vengono rilasciate quando l'ultimo processo con una vista dell'oggetto di mapping termina o rimuove il mapping della vista chiamando la funzione [**UnmapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-unmapviewoffile) . Al momento, viene aggiornato il file specificato, se presente, associato all'oggetto di mapping. È anche possibile forzare l'aggiornamento di un file specificato chiamando la funzione [**FlushViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-flushviewoffile) .

Per ulteriori informazioni, vedere [mapping di file](file-mapping.md). Per un esempio di memoria condivisa in una DLL, vedere [uso della memoria condivisa in una libreria di Dynamic-Link](../dlls/using-shared-memory-in-a-dynamic-link-library.md).

Se più processi hanno accesso in scrittura alla memoria condivisa, è necessario sincronizzare l'accesso alla memoria. Per ulteriori informazioni, vedere [sincronizzazione](../sync/synchronization.md).

 

 
