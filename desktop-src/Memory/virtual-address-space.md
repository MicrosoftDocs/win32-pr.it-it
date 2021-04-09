---
description: Lo spazio degli indirizzi virtuali per un processo è il set di indirizzi di memoria virtuale che può utilizzare. Lo spazio degli indirizzi per ogni processo è privato e non è possibile accedervi da altri processi, a meno che non sia condiviso.
ms.assetid: 747f9f53-a595-4f4b-8b81-3123d59edb2f
title: Spazio degli indirizzi virtuali (gestione della memoria)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6584d0404799e6b0e5ab343c7d8b39d7f8d741a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966835"
---
# <a name="virtual-address-space-memory-management"></a><span data-ttu-id="d47ac-104">Spazio degli indirizzi virtuali (gestione della memoria)</span><span class="sxs-lookup"><span data-stu-id="d47ac-104">Virtual Address Space (Memory Management)</span></span>

<span data-ttu-id="d47ac-105">Lo spazio degli indirizzi virtuali per un processo è il set di indirizzi di memoria virtuale che può utilizzare.</span><span class="sxs-lookup"><span data-stu-id="d47ac-105">The virtual address space for a process is the set of virtual memory addresses that it can use.</span></span> <span data-ttu-id="d47ac-106">Lo spazio degli indirizzi per ogni processo è privato e non è possibile accedervi da altri processi, a meno che non sia condiviso.</span><span class="sxs-lookup"><span data-stu-id="d47ac-106">The address space for each process is private and cannot be accessed by other processes unless it is shared.</span></span>

<span data-ttu-id="d47ac-107">Un indirizzo virtuale non rappresenta la posizione fisica effettiva di un oggetto in memoria. il sistema gestisce invece una *tabella di pagine* per ogni processo, ovvero una struttura di dati interna utilizzata per convertire gli indirizzi virtuali nei rispettivi indirizzi fisici corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="d47ac-107">A virtual address does not represent the actual physical location of an object in memory; instead, the system maintains a *page table* for each process, which is an internal data structure used to translate virtual addresses into their corresponding physical addresses.</span></span> <span data-ttu-id="d47ac-108">Ogni volta che un thread fa riferimento a un indirizzo, il sistema converte l'indirizzo virtuale in un indirizzo fisico.</span><span class="sxs-lookup"><span data-stu-id="d47ac-108">Each time a thread references an address, the system translates the virtual address to a physical address.</span></span>

<span data-ttu-id="d47ac-109">Lo spazio degli indirizzi virtuali per Windows a 32 bit è di 4 gigabyte (GB) e diviso in due partizioni: uno per l'utilizzo da parte del processo e l'altro riservato per l'utilizzo da parte del sistema.</span><span class="sxs-lookup"><span data-stu-id="d47ac-109">The virtual address space for 32-bit Windows is 4 gigabytes (GB) in size and divided into two partitions: one for use by the process and the other reserved for use by the system.</span></span> <span data-ttu-id="d47ac-110">Per altre informazioni sullo spazio degli indirizzi virtuali in Windows a 64 bit, vedere [spazio degli indirizzi virtuali in Windows a 64 bit](../winprog64/virtual-address-space.md).</span><span class="sxs-lookup"><span data-stu-id="d47ac-110">For more information about the virtual address space in 64-bit Windows, see [Virtual Address Space in 64-bit Windows](../winprog64/virtual-address-space.md).</span></span>

<span data-ttu-id="d47ac-111">Per ulteriori informazioni sulla memoria virtuale, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="d47ac-111">For more information about virtual memory, see the following topics:</span></span>

-   [<span data-ttu-id="d47ac-112">Spazio degli indirizzi virtuali e archiviazione fisica</span><span class="sxs-lookup"><span data-stu-id="d47ac-112">Virtual Address Space and Physical Storage</span></span>](virtual-address-space-and-physical-storage.md)
-   [<span data-ttu-id="d47ac-113">Working Set</span><span class="sxs-lookup"><span data-stu-id="d47ac-113">Working Set</span></span>](working-set.md)
-   [<span data-ttu-id="d47ac-114">Stato della pagina</span><span class="sxs-lookup"><span data-stu-id="d47ac-114">Page State</span></span>](page-state.md)
-   [<span data-ttu-id="d47ac-115">Ambito della memoria allocata</span><span class="sxs-lookup"><span data-stu-id="d47ac-115">Scope of Allocated Memory</span></span>](scope-of-allocated-memory.md)
-   [<span data-ttu-id="d47ac-116">Protezione esecuzione programmi</span><span class="sxs-lookup"><span data-stu-id="d47ac-116">Data Execution Prevention</span></span>](data-execution-prevention.md)
-   [<span data-ttu-id="d47ac-117">Protezione della memoria</span><span class="sxs-lookup"><span data-stu-id="d47ac-117">Memory Protection</span></span>](memory-protection.md)
-   [<span data-ttu-id="d47ac-118">Limiti di memoria per le versioni di Windows</span><span class="sxs-lookup"><span data-stu-id="d47ac-118">Memory Limits for Windows Releases</span></span>](memory-limits-for-windows-releases.md)

## <a name="default-virtual-address-space-for-32-bit-windows"></a><span data-ttu-id="d47ac-119">Spazio degli indirizzi virtuali predefinito per Windows a 32 bit</span><span class="sxs-lookup"><span data-stu-id="d47ac-119">Default Virtual Address Space for 32-bit Windows</span></span>

<span data-ttu-id="d47ac-120">La tabella seguente mostra l'intervallo di memoria predefinito per ogni partizione.</span><span class="sxs-lookup"><span data-stu-id="d47ac-120">The following table shows the default memory range for each partition.</span></span>



| <span data-ttu-id="d47ac-121">Intervallo di memoria</span><span class="sxs-lookup"><span data-stu-id="d47ac-121">Memory range</span></span>                             | <span data-ttu-id="d47ac-122">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="d47ac-122">Usage</span></span>                |
|------------------------------------------|----------------------|
| <span data-ttu-id="d47ac-123">2GB Bassi (da 0x00000000 a 0x7FFFFFFF)</span><span class="sxs-lookup"><span data-stu-id="d47ac-123">Low 2GB (0x00000000 through 0x7FFFFFFF)</span></span>  | <span data-ttu-id="d47ac-124">Utilizzato dal processo.</span><span class="sxs-lookup"><span data-stu-id="d47ac-124">Used by the process.</span></span> |
| <span data-ttu-id="d47ac-125">2 GB elevati (da 0x80000000 a 0xFFFFFFFF)</span><span class="sxs-lookup"><span data-stu-id="d47ac-125">High 2GB (0x80000000 through 0xFFFFFFFF)</span></span> | <span data-ttu-id="d47ac-126">Utilizzato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="d47ac-126">Used by the system.</span></span>  |



 

## <a name="virtual-address-space-for-32-bit-windows-with-4gt"></a><span data-ttu-id="d47ac-127">Spazio degli indirizzi virtuali per Windows a 32 bit con 4GT</span><span class="sxs-lookup"><span data-stu-id="d47ac-127">Virtual Address Space for 32-bit Windows with 4GT</span></span>

<span data-ttu-id="d47ac-128">Se è abilitata l' [ottimizzazione 4 gigabyte](4-gigabyte-tuning.md) (4GT), l'intervallo di memoria per ogni partizione è il seguente.</span><span class="sxs-lookup"><span data-stu-id="d47ac-128">If [4-gigabyte tuning](4-gigabyte-tuning.md) (4GT) is enabled, the memory range for each partition is as follows.</span></span>



| <span data-ttu-id="d47ac-129">Intervallo di memoria</span><span class="sxs-lookup"><span data-stu-id="d47ac-129">Memory range</span></span>                             | <span data-ttu-id="d47ac-130">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="d47ac-130">Usage</span></span>                |
|------------------------------------------|----------------------|
| <span data-ttu-id="d47ac-131">Basso 3GB (da 0x00000000 a 0xBFFFFFFF)</span><span class="sxs-lookup"><span data-stu-id="d47ac-131">Low 3GB (0x00000000 through 0xBFFFFFFF)</span></span>  | <span data-ttu-id="d47ac-132">Utilizzato dal processo.</span><span class="sxs-lookup"><span data-stu-id="d47ac-132">Used by the process.</span></span> |
| <span data-ttu-id="d47ac-133">Da 1 GB ad alto (da 0xC0000000 a 0xFFFFFFFF)</span><span class="sxs-lookup"><span data-stu-id="d47ac-133">High 1GB (0xC0000000 through 0xFFFFFFFF)</span></span> | <span data-ttu-id="d47ac-134">Utilizzato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="d47ac-134">Used by the system.</span></span>  |



 

<span data-ttu-id="d47ac-135">Dopo l'abilitazione di 4GT, un processo con il flag di rilevamento degli [**\_ \_ \_ indirizzi \_ grande**](/windows/win32/api/dbghelp/ns-dbghelp-loaded_image) per il file di immagine impostato nell'intestazione dell'immagine avrà accesso agli altri 1 GB di memoria oltre i 2 GB più bassi.</span><span class="sxs-lookup"><span data-stu-id="d47ac-135">After 4GT is enabled, a process that has the [**IMAGE\_FILE\_LARGE\_ADDRESS\_AWARE**](/windows/win32/api/dbghelp/ns-dbghelp-loaded_image) flag set in its image header will have access to the additional 1 GB of memory above the low 2 GB.</span></span>

## <a name="adjusting-the-virtual-address-space-for-32-bit-windows"></a><span data-ttu-id="d47ac-136">Regolazione dello spazio degli indirizzi virtuali per Windows a 32 bit</span><span class="sxs-lookup"><span data-stu-id="d47ac-136">Adjusting the Virtual Address Space for 32-bit Windows</span></span>

<span data-ttu-id="d47ac-137">È possibile usare il comando seguente per impostare un'opzione per la voce di avvio che configura la dimensione della partizione disponibile per l'uso da parte del processo su un valore compreso tra 2048 (2 GB) e 3072 (3 GB):</span><span class="sxs-lookup"><span data-stu-id="d47ac-137">You can use the following command to set a boot entry option that configures the size of the partition that is available for use by the process to a value between 2048 (2 GB) and 3072 (3 GB):</span></span>

<span data-ttu-id="d47ac-138">[Bcdedit/set](/windows-hardware/drivers/devtest/bcdedit--set) **increaseuserva** *megabyte*</span><span class="sxs-lookup"><span data-stu-id="d47ac-138">[BCDEdit /set](/windows-hardware/drivers/devtest/bcdedit--set) **increaseuserva** *Megabytes*</span></span>

<span data-ttu-id="d47ac-139">Dopo aver impostato l'opzione relativa alla voce di avvio, l'intervallo di memoria per ogni partizione è il seguente.</span><span class="sxs-lookup"><span data-stu-id="d47ac-139">After the boot entry option is set, the memory range for each partition is as follows.</span></span>



| <span data-ttu-id="d47ac-140">Intervallo di memoria</span><span class="sxs-lookup"><span data-stu-id="d47ac-140">Memory range</span></span>                            | <span data-ttu-id="d47ac-141">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="d47ac-141">Usage</span></span>                |
|-----------------------------------------|----------------------|
| <span data-ttu-id="d47ac-142">Bassa (da 0x00000000 a *megabyte*)</span><span class="sxs-lookup"><span data-stu-id="d47ac-142">Low (0x00000000 through *Megabytes*)</span></span>    | <span data-ttu-id="d47ac-143">Utilizzato dal processo.</span><span class="sxs-lookup"><span data-stu-id="d47ac-143">Used by the process.</span></span> |
| <span data-ttu-id="d47ac-144">Alto (*megabyte*+ 1 a 0xFFFFFFFF)</span><span class="sxs-lookup"><span data-stu-id="d47ac-144">High (*Megabytes*+1 through 0xFFFFFFFF)</span></span> | <span data-ttu-id="d47ac-145">Utilizzato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="d47ac-145">Used by the system.</span></span>  |



 

<span data-ttu-id="d47ac-146">**Windows Server 2003:** Impostare l'opzione **parametro/userva** boot.ini su un valore compreso tra 2048 e 3072.</span><span class="sxs-lookup"><span data-stu-id="d47ac-146">**Windows Server 2003:** Set the **/USERVA** switch in boot.ini to a value between 2048 and 3072.</span></span>

 

 
