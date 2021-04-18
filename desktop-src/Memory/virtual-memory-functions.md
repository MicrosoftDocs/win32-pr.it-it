---
description: Le funzioni di memoria virtuale consentono a un processo di modificare o determinare lo stato delle pagine nello spazio degli indirizzi virtuali.
ms.assetid: 9488a854-1ef0-488f-b3d1-57c1acb82a88
title: Funzioni di memoria virtuale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c76866fd10dac01315622e8a4faef7bea436a61
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308199"
---
# <a name="virtual-memory-functions"></a><span data-ttu-id="f3ef8-103">Funzioni di memoria virtuale</span><span class="sxs-lookup"><span data-stu-id="f3ef8-103">Virtual Memory Functions</span></span>

<span data-ttu-id="f3ef8-104">Le funzioni di memoria virtuale consentono a un processo di modificare o determinare lo stato delle pagine nello spazio degli indirizzi virtuali.</span><span class="sxs-lookup"><span data-stu-id="f3ef8-104">The virtual memory functions enable a process to manipulate or determine the status of pages in its virtual address space.</span></span> <span data-ttu-id="f3ef8-105">Possono eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="f3ef8-105">They can perform the following operations:</span></span>

-   <span data-ttu-id="f3ef8-106">Riservare un intervallo di spazio degli indirizzi virtuali di un processo.</span><span class="sxs-lookup"><span data-stu-id="f3ef8-106">Reserve a range of a process's virtual address space.</span></span> <span data-ttu-id="f3ef8-107">La riserva dello spazio degli indirizzi non alloca alcuna risorsa di archiviazione fisica, ma impedisce ad altre operazioni di allocazione di utilizzare l'intervallo specificato.</span><span class="sxs-lookup"><span data-stu-id="f3ef8-107">Reserving address space does not allocate any physical storage, but it prevents other allocation operations from using the specified range.</span></span> <span data-ttu-id="f3ef8-108">Non influisce sugli spazi degli indirizzi virtuali di altri processi.</span><span class="sxs-lookup"><span data-stu-id="f3ef8-108">It does not affect the virtual address spaces of other processes.</span></span> <span data-ttu-id="f3ef8-109">La prenotazione di pagine impedisce il consumo di spazio di archiviazione fisico necessario, consentendo a un processo di riservare un intervallo di spazio degli indirizzi in cui è possibile aumentare la struttura dei dati dinamica.</span><span class="sxs-lookup"><span data-stu-id="f3ef8-109">Reserving pages prevents needless consumption of physical storage, while enabling a process to reserve a range of its address space into which a dynamic data structure can grow.</span></span> <span data-ttu-id="f3ef8-110">Il processo può allocare spazio di archiviazione fisico per lo spazio in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="f3ef8-110">The process can allocate physical storage for this space, as needed.</span></span>
-   <span data-ttu-id="f3ef8-111">Eseguire il commit di un intervallo di pagine riservate nello spazio degli indirizzi virtuali di un processo, in modo che l'archiviazione fisica (in RAM o su disco) sia accessibile solo al processo di allocazione.</span><span class="sxs-lookup"><span data-stu-id="f3ef8-111">Commit a range of reserved pages in a process's virtual address space so that physical storage (either in RAM or on disk) is accessible only to the allocating process.</span></span>
-   <span data-ttu-id="f3ef8-112">Specificare in lettura/scrittura, in sola lettura o nessun accesso per un intervallo di pagine di cui è stato eseguito il commit.</span><span class="sxs-lookup"><span data-stu-id="f3ef8-112">Specify read/write, read-only, or no access for a range of committed pages.</span></span> <span data-ttu-id="f3ef8-113">Questo comportamento è diverso dalle funzioni di allocazione standard che allocano sempre pagine con accesso in lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="f3ef8-113">This differs from the standard allocation functions that always allocate pages with read/write access.</span></span>
-   <span data-ttu-id="f3ef8-114">Liberare un intervallo di pagine riservate, rendendo l'intervallo di indirizzi virtuali disponibili per le successive operazioni di allocazione da parte del processo chiamante.</span><span class="sxs-lookup"><span data-stu-id="f3ef8-114">Free a range of reserved pages, making the range of virtual addresses available for subsequent allocation operations by the calling process.</span></span>
-   <span data-ttu-id="f3ef8-115">Eseguire il decommit di un intervallo di pagine di cui è stato eseguito il commit, rilasciando l'archiviazione fisica e rendendola disponibile per l'allocazione successiva da qualsiasi processo.</span><span class="sxs-lookup"><span data-stu-id="f3ef8-115">Decommit a range of committed pages, releasing their physical storage and making it available for subsequent allocation by any process.</span></span>
-   <span data-ttu-id="f3ef8-116">Bloccare una o più pagine di memoria di cui è stato eseguito il commit nella memoria fisica (RAM), in modo che il sistema non possa scambiare le pagine nel file di paging.</span><span class="sxs-lookup"><span data-stu-id="f3ef8-116">Lock one or more pages of committed memory into physical memory (RAM) so that the system cannot swap the pages out to the paging file.</span></span>
-   <span data-ttu-id="f3ef8-117">Ottenere informazioni su un intervallo di pagine nello spazio degli indirizzi virtuali del processo chiamante o di un processo specificato.</span><span class="sxs-lookup"><span data-stu-id="f3ef8-117">Obtain information about a range of pages in the virtual address space of the calling process or a specified process.</span></span>
-   <span data-ttu-id="f3ef8-118">Modificare la protezione dell'accesso per un intervallo specificato di pagine di cui è stato eseguito il commit nello spazio degli indirizzi virtuali del processo chiamante o in un processo specificato.</span><span class="sxs-lookup"><span data-stu-id="f3ef8-118">Change the access protection for a specified range of committed pages in the virtual address space of the calling process or a specified process.</span></span>

<span data-ttu-id="f3ef8-119">Per ulteriori informazioni, vedere gli argomenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="f3ef8-119">For more information, see the following topics.</span></span>

-   [<span data-ttu-id="f3ef8-120">Allocazione della memoria virtuale</span><span class="sxs-lookup"><span data-stu-id="f3ef8-120">Allocating Virtual Memory</span></span>](allocating-virtual-memory.md)
-   [<span data-ttu-id="f3ef8-121">Confronto tra i metodi di allocazione della memoria</span><span class="sxs-lookup"><span data-stu-id="f3ef8-121">Comparing Memory Allocation Methods</span></span>](comparing-memory-allocation-methods.md)
-   [<span data-ttu-id="f3ef8-122">Liberare memoria virtuale</span><span class="sxs-lookup"><span data-stu-id="f3ef8-122">Freeing Virtual Memory</span></span>](freeing-virtual-memory.md)
-   [<span data-ttu-id="f3ef8-123">Uso delle pagine</span><span class="sxs-lookup"><span data-stu-id="f3ef8-123">Working With Pages</span></span>](working-with-pages.md)
-   [<span data-ttu-id="f3ef8-124">Funzioni di gestione della memoria</span><span class="sxs-lookup"><span data-stu-id="f3ef8-124">Memory Management Functions</span></span>](memory-management-functions.md)

 

 



