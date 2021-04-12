---
title: Procedura dettagliata
description: Uno snapshot che include l'elenco dei processi contiene informazioni su ogni processo attualmente in esecuzione.
ms.assetid: 4fb55763-2206-48ad-8b1f-ed2c33b6f56b
keywords:
- enumerazione
- Enumerazione, processi
- processi
- processi, enumerazione dei processi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbc95f0de4021ce3c355286376decbdecef2c883
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473550"
---
# <a name="process-walking"></a><span data-ttu-id="451a6-107">Procedura dettagliata</span><span class="sxs-lookup"><span data-stu-id="451a6-107">Process Walking</span></span>

<span data-ttu-id="451a6-108">Uno snapshot che include l'elenco dei processi contiene informazioni su ogni processo attualmente in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="451a6-108">A snapshot that includes the process list contains information about each currently executing process.</span></span> <span data-ttu-id="451a6-109">È possibile recuperare le informazioni per il primo processo nell'elenco usando la funzione [**Process32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32first) .</span><span class="sxs-lookup"><span data-stu-id="451a6-109">You can retrieve information for the first process in the list by using the [**Process32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32first) function.</span></span> <span data-ttu-id="451a6-110">Dopo aver recuperato il primo processo nell'elenco, è possibile attraversare l'elenco dei processi per le voci successive utilizzando la funzione [**Process32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32next) .</span><span class="sxs-lookup"><span data-stu-id="451a6-110">After retrieving the first process in the list, you can traverse the process list for subsequent entries by using the [**Process32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32next) function.</span></span> <span data-ttu-id="451a6-111">**Process32First** e **Process32Next** riempiono una struttura [**PROCESSENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-processentry32) con informazioni su un processo nello snapshot.</span><span class="sxs-lookup"><span data-stu-id="451a6-111">**Process32First** and **Process32Next** fill a [**PROCESSENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-processentry32) structure with information about a process in the snapshot.</span></span> <span data-ttu-id="451a6-112">Per un esempio, vedere [acquisizione di uno snapshot e visualizzazione dei processi](taking-a-snapshot-and-viewing-processes.md).</span><span class="sxs-lookup"><span data-stu-id="451a6-112">For an example, see [Taking a Snapshot and Viewing Processes](taking-a-snapshot-and-viewing-processes.md).</span></span>

<span data-ttu-id="451a6-113">È possibile recuperare un codice di stato di errore esteso per [**Process32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32first) e [**Process32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32next) utilizzando la funzione [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .</span><span class="sxs-lookup"><span data-stu-id="451a6-113">You can retrieve an extended error status code for [**Process32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32first) and [**Process32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32next) by using the [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function.</span></span>

<span data-ttu-id="451a6-114">È possibile leggere la memoria in un processo specifico in un buffer usando la funzione [**Toolhelp32ReadProcessMemory**](/windows/desktop/api/TlHelp32/nf-tlhelp32-toolhelp32readprocessmemory) (o la funzione [**VirtualQueryEx**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualqueryex) ).</span><span class="sxs-lookup"><span data-stu-id="451a6-114">You can read the memory in a specific process into a buffer by using the [**Toolhelp32ReadProcessMemory**](/windows/desktop/api/TlHelp32/nf-tlhelp32-toolhelp32readprocessmemory) function (or the [**VirtualQueryEx**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualqueryex) function).</span></span>

> [!Note]  
> <span data-ttu-id="451a6-115">Il contenuto dei membri **th32ProcessID** e **th32ParentProcessID** di [**PROCESSENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-processentry32) è costituito da identificatori di processo e può essere usato da qualsiasi funzione che richiede un identificatore di processo.</span><span class="sxs-lookup"><span data-stu-id="451a6-115">The contents of the **th32ProcessID** and **th32ParentProcessID** members of [**PROCESSENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-processentry32) are process identifiers and can be used by any functions that require a process identifier.</span></span>

 

 

 