---
description: Il working set di un programma è una raccolta di tali pagine nello spazio indirizzi virtuale a cui è stato fatto riferimento di recente.
ms.assetid: 6017ef59-d2e9-4245-a406-8965024dbb35
title: Elabora working set
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aaded3d0b5f8c6ad552cc728c68ad0407391c343
ms.sourcegitcommit: b01ad017c152c6756f3638623fe335877644d414
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/06/2021
ms.locfileid: "111549903"
---
# <a name="process-working-set"></a><span data-ttu-id="dc48e-103">Elabora working set</span><span class="sxs-lookup"><span data-stu-id="dc48e-103">Process Working Set</span></span>

<span data-ttu-id="dc48e-104">Il *working set* di un programma è una raccolta di tali pagine nello spazio indirizzi virtuale a cui è stato fatto riferimento di recente.</span><span class="sxs-lookup"><span data-stu-id="dc48e-104">The *working set* of a program is a collection of those pages in its virtual address space that have been recently referenced.</span></span> <span data-ttu-id="dc48e-105">Include dati condivisi e privati.</span><span class="sxs-lookup"><span data-stu-id="dc48e-105">It includes both shared and private data.</span></span> <span data-ttu-id="dc48e-106">I dati condivisi includono pagine che contengono tutte le istruzioni eseguite dall'applicazione, incluse quelle nelle DLL e nelle DLL di sistema.</span><span class="sxs-lookup"><span data-stu-id="dc48e-106">The shared data includes pages that contain all instructions your application executes, including those in your DLLs and the system DLLs.</span></span> <span data-ttu-id="dc48e-107">Con l'working set aumentano le dimensioni, aumenta la richiesta di memoria.</span><span class="sxs-lookup"><span data-stu-id="dc48e-107">As the working set size increases, memory demand increases.</span></span>

<span data-ttu-id="dc48e-108">A un processo sono associate dimensioni minime working set e dimensioni working set massime.</span><span class="sxs-lookup"><span data-stu-id="dc48e-108">A process has an associated minimum working set size and maximum working set size.</span></span> <span data-ttu-id="dc48e-109">Ogni volta che si chiama [**CreateProcess,**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa)riserva le dimensioni minime working set per il processo.</span><span class="sxs-lookup"><span data-stu-id="dc48e-109">Each time you call [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa), it reserves the minimum working set size for the process.</span></span> <span data-ttu-id="dc48e-110">Il gestore della memoria virtuale tenta di mantenere una quantità di memoria sufficiente per il working set minimo quando il processo è attivo, ma non oltre le dimensioni massime.</span><span class="sxs-lookup"><span data-stu-id="dc48e-110">The virtual memory manager attempts to keep enough memory for the minimum working set resident when the process is active, but keeps no more than the maximum size.</span></span>

<span data-ttu-id="dc48e-111">Per ottenere le dimensioni minime e massime richieste del working set per l'applicazione, chiamare la [**funzione GetProcessWorkingSetSize.**](/windows/desktop/api/memoryapi/nf-memoryapi-getprocessworkingsetsize)</span><span class="sxs-lookup"><span data-stu-id="dc48e-111">To get the requested minimum and maximum sizes of the working set for your application, call the [**GetProcessWorkingSetSize**](/windows/desktop/api/memoryapi/nf-memoryapi-getprocessworkingsetsize) function.</span></span>

<span data-ttu-id="dc48e-112">Il sistema imposta le dimensioni working set predefinite.</span><span class="sxs-lookup"><span data-stu-id="dc48e-112">The system sets the default working set sizes.</span></span> <span data-ttu-id="dc48e-113">È anche possibile modificare le dimensioni working set usando la [**funzione SetProcessWorkingSetSize.**](/windows/desktop/api/memoryapi/nf-memoryapi-setprocessworkingsetsize)</span><span class="sxs-lookup"><span data-stu-id="dc48e-113">You can also modify the working set sizes using the [**SetProcessWorkingSetSize**](/windows/desktop/api/memoryapi/nf-memoryapi-setprocessworkingsetsize) function.</span></span> <span data-ttu-id="dc48e-114">L'impostazione di questi valori non garantisce che la memoria sia riservata o residente.</span><span class="sxs-lookup"><span data-stu-id="dc48e-114">Setting these values is not a guarantee that the memory will be reserved or resident.</span></span> <span data-ttu-id="dc48e-115">Prestare attenzione a richiedere dimensioni minime o massime troppo grandi working set, perché questa operazione può compromettere le prestazioni del sistema.</span><span class="sxs-lookup"><span data-stu-id="dc48e-115">Be careful about requesting too large a minimum or maximum working set size, because doing so can degrade system performance.</span></span>

<span data-ttu-id="dc48e-116">Per ottenere la dimensione corrente o massima del working set per il processo, usare la [**funzione GetProcessMemoryInfo.**](/windows/win32/api/psapi/nf-psapi-getprocessmemoryinfo)</span><span class="sxs-lookup"><span data-stu-id="dc48e-116">To obtain the current or peak size of the working set for your process, use the [**GetProcessMemoryInfo**](/windows/win32/api/psapi/nf-psapi-getprocessmemoryinfo) function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dc48e-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="dc48e-117">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="dc48e-118">[Informazioni sulle prestazioni della memoria](/previous-versions/windows/desktop/legacy/aa965225(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="dc48e-118">[Memory Performance Information](/previous-versions/windows/desktop/legacy/aa965225(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="dc48e-119">Working Set</span><span class="sxs-lookup"><span data-stu-id="dc48e-119">Working Set</span></span>](../memory/working-set.md)
</dt> </dl>

 

 
