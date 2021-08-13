---
title: Process Walking
description: Uno snapshot che include l'elenco di processi contiene informazioni su ogni processo attualmente in esecuzione.
ms.assetid: 4fb55763-2206-48ad-8b1f-ed2c33b6f56b
keywords:
- enumerazione
- enumerazione, processi
- processes
- processi,enumerazione di processi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6efa129182da256a6ce62b3754ea422df908248f7b0ecc30d3b690c29ffaf9d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119419661"
---
# <a name="process-walking"></a>Process Walking

Uno snapshot che include l'elenco di processi contiene informazioni su ogni processo attualmente in esecuzione. È possibile recuperare informazioni per il primo processo nell'elenco usando la [**funzione Process32First.**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32first) Dopo aver recuperato il primo processo nell'elenco, è possibile attraversare l'elenco di processi per le voci successive usando la [**funzione Process32Next.**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32next) **Process32First** e **Process32Next** riempiono una [**struttura PROCESSENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-processentry32) con informazioni su un processo nello snapshot. Per un esempio, vedere [Creazione di uno snapshot e Visualizzazione di processi](taking-a-snapshot-and-viewing-processes.md).

È possibile recuperare un codice di stato di errore esteso per [**Process32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32first) e [**Process32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32next) usando la [**funzione GetLastError.**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)

È possibile leggere la memoria in un processo specifico in un buffer usando la funzione [**Toolhelp32ReadProcessMemory**](/windows/desktop/api/TlHelp32/nf-tlhelp32-toolhelp32readprocessmemory) (o [**la funzione VirtualQueryEx).**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualqueryex)

> [!Note]  
> I contenuti dei membri **th32ProcessID** e **th32ParentProcessID** di [**PROCESSENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-processentry32) sono identificatori di processo e possono essere usati da qualsiasi funzione che richiede un identificatore di processo.

 

 

 