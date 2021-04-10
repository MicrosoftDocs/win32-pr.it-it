---
description: Il working set di un programma è una raccolta di tali pagine nello spazio degli indirizzi virtuali a cui è stato fatto riferimento di recente.
ms.assetid: 6017ef59-d2e9-4245-a406-8965024dbb35
title: Working set di processo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 900b5d8a19c756a9087a9b2c006259857691dc11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104231515"
---
# <a name="process-working-set"></a><span data-ttu-id="22728-103">Working set di processo</span><span class="sxs-lookup"><span data-stu-id="22728-103">Process Working Set</span></span>

<span data-ttu-id="22728-104">Il *working set* di un programma è una raccolta di tali pagine nello spazio degli indirizzi virtuali a cui è stato fatto riferimento di recente.</span><span class="sxs-lookup"><span data-stu-id="22728-104">The *working set* of a program is a collection of those pages in its virtual address space that have been recently referenced.</span></span> <span data-ttu-id="22728-105">Include sia i dati condivisi che quelli privati.</span><span class="sxs-lookup"><span data-stu-id="22728-105">It includes both shared and private data.</span></span> <span data-ttu-id="22728-106">I dati condivisi includono pagine che contengono tutte le istruzioni eseguite dall'applicazione, incluse quelle nelle DLL e nelle DLL di sistema.</span><span class="sxs-lookup"><span data-stu-id="22728-106">The shared data includes pages that contain all instructions your application executes, including those in your DLLs and the system DLLs.</span></span> <span data-ttu-id="22728-107">Man mano che aumentano le dimensioni del working set, aumenta la richiesta di memoria.</span><span class="sxs-lookup"><span data-stu-id="22728-107">As the working set size increases, memory demand increases.</span></span>

<span data-ttu-id="22728-108">A un processo sono associate dimensioni minime working set e dimensioni massime working set.</span><span class="sxs-lookup"><span data-stu-id="22728-108">A process has an associated minimum working set size and maximum working set size.</span></span> <span data-ttu-id="22728-109">Ogni volta che si chiama [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa), vengono riservate le dimensioni minime working set per il processo.</span><span class="sxs-lookup"><span data-stu-id="22728-109">Each time you call [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa), it reserves the minimum working set size for the process.</span></span> <span data-ttu-id="22728-110">Il gestore della memoria virtuale tenta di conservare memoria sufficiente per il working set residente minimo quando il processo è attivo, ma non supera la dimensione massima.</span><span class="sxs-lookup"><span data-stu-id="22728-110">The virtual memory manager attempts to keep enough memory for the minimum working set resident when the process is active, but keeps no more than the maximum size.</span></span>

<span data-ttu-id="22728-111">Per ottenere le dimensioni minime e massime richieste del working set per l'applicazione, chiamare la funzione [**GetProcessWorkingSetSize**](/windows/desktop/api/WinBase/nf-winbase-getprocessworkingsetsize) .</span><span class="sxs-lookup"><span data-stu-id="22728-111">To get the requested minimum and maximum sizes of the working set for your application, call the [**GetProcessWorkingSetSize**](/windows/desktop/api/WinBase/nf-winbase-getprocessworkingsetsize) function.</span></span>

<span data-ttu-id="22728-112">Il sistema imposta le dimensioni working set predefinite.</span><span class="sxs-lookup"><span data-stu-id="22728-112">The system sets the default working set sizes.</span></span> <span data-ttu-id="22728-113">È anche possibile modificare le dimensioni working set usando la funzione [**SetProcessWorkingSetSize**](/windows/desktop/api/WinBase/nf-winbase-setprocessworkingsetsize) .</span><span class="sxs-lookup"><span data-stu-id="22728-113">You can also modify the working set sizes using the [**SetProcessWorkingSetSize**](/windows/desktop/api/WinBase/nf-winbase-setprocessworkingsetsize) function.</span></span> <span data-ttu-id="22728-114">L'impostazione di questi valori non garantisce che la memoria sarà riservata o residente.</span><span class="sxs-lookup"><span data-stu-id="22728-114">Setting these values is not a guarantee that the memory will be reserved or resident.</span></span> <span data-ttu-id="22728-115">Prestare attenzione alla richiesta di dimensioni minime o massime di working set, perché questa operazione può influire negativamente sulle prestazioni del sistema.</span><span class="sxs-lookup"><span data-stu-id="22728-115">Be careful about requesting too large a minimum or maximum working set size, because doing so can degrade system performance.</span></span>

<span data-ttu-id="22728-116">Per ottenere le dimensioni correnti o massime del working set per il processo, usare la funzione [**GetProcessMemoryInfo**](/windows/win32/api/psapi/nf-psapi-getprocessmemoryinfo) .</span><span class="sxs-lookup"><span data-stu-id="22728-116">To obtain the current or peak size of the working set for your process, use the [**GetProcessMemoryInfo**](/windows/win32/api/psapi/nf-psapi-getprocessmemoryinfo) function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="22728-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="22728-117">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="22728-118">[Informazioni sulle prestazioni della memoria](/previous-versions/windows/desktop/legacy/aa965225(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="22728-118">[Memory Performance Information](/previous-versions/windows/desktop/legacy/aa965225(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="22728-119">Working Set</span><span class="sxs-lookup"><span data-stu-id="22728-119">Working Set</span></span>](../memory/working-set.md)
</dt> </dl>

 

 
