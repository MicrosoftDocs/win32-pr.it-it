---
title: Elenchi di heap e camminamenti dell'heap
description: Uno snapshot che include l'elenco di heap per un processo specificato contiene informazioni di identificazione per ogni heap associato al processo specificato e informazioni dettagliate su ogni heap.
ms.assetid: 631096fd-cb2c-4b19-aa71-d47060e2715c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b5a9b8d30e2de1bf5ab37de03fdcb3fde663417
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727970"
---
# <a name="heap-lists-and-heap-walking"></a>Elenchi di heap e camminamenti dell'heap

Uno snapshot che include l'elenco di heap per un processo specificato contiene informazioni di identificazione per ogni heap associato al processo specificato e informazioni dettagliate su ogni heap. È possibile recuperare un identificatore per il primo heap dell'elenco di heap usando la funzione [**Heap32ListFirst**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listfirst) . Dopo il recupero del primo heap nell'elenco, è possibile attraversare l'elenco di heap per gli heap successivi associati al processo tramite la funzione [**Heap32ListNext**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listnext) . **Heap32ListFirst** e **Heap32ListNext** riempiono una struttura [**HEAPLIST32**](/windows/win32/api/tlhelp32/ns-tlhelp32-heaplist32) con l'identificatore del processo, l'identificatore dell'heap e i flag che descrivono l'heap.

È possibile recuperare informazioni sul primo blocco di un heap usando la funzione [**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first) . Dopo il recupero del primo blocco di un heap, è possibile recuperare informazioni sui blocchi successivi dello stesso heap utilizzando la funzione [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) . **Heap32First** e **Heap32Next** riempiono una struttura [**HEAPENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-heapentry32) con le informazioni per il blocco appropriato di un heap.

È possibile recuperare un codice di stato di errore esteso per [**Heap32ListFirst**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listfirst), [**Heap32ListNext**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listnext), [**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first)e [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) tramite la funzione [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .

> [!Note]  
> L'identificatore dell'heap, specificato nel membro **th32HeapID** della struttura [**HEAPENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-heapentry32) , ha significato solo per le funzioni della guida dello strumento. Non è un handle, né può essere utilizzato da altre funzioni.

 

 

 