---
description: Lo spazio dell'indirizzo virtuale di sistema (VA) nei sistemi a 32 bit può esaurirsi a causa della frammentazione. È possibile utilizzare diverse chiavi del registro di sistema per configurare i limiti di memoria nei sistemi a 32 bit in cui si verifica questo problema.
ms.assetid: ec2a8c6b-cd8e-4085-b337-02f78a210bb5
title: Chiavi del registro di sistema di gestione della memoria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48e8c53bd54f8caeb82aad58ceed61cc5644c112
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885709"
---
# <a name="memory-management-registry-keys"></a><span data-ttu-id="47a75-104">Chiavi del registro di sistema di gestione della memoria</span><span class="sxs-lookup"><span data-stu-id="47a75-104">Memory Management Registry Keys</span></span>

<span data-ttu-id="47a75-105">Lo spazio dell'indirizzo virtuale di sistema (VA) nei sistemi a 32 bit può esaurirsi a causa della frammentazione.</span><span class="sxs-lookup"><span data-stu-id="47a75-105">System virtual address (VA) space on 32-bit systems can become exhausted due to fragmentation.</span></span> <span data-ttu-id="47a75-106">È possibile utilizzare diverse chiavi del registro di sistema per configurare i limiti di memoria nei sistemi a 32 bit in cui si verifica questo problema.</span><span class="sxs-lookup"><span data-stu-id="47a75-106">Several registry keys can be used to configure memory limits on 32-bit systems that experience this issue.</span></span> <span data-ttu-id="47a75-107">Lo spazio di sistema VA nei sistemi a 64 bit non è soggetto all'esaurimento della frammentazione. Pertanto, queste chiavi non hanno alcun effetto sui sistemi a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="47a75-107">System VA space on 64-bit systems is not subject to exhaustion by fragmentation; therefore, these keys have no effect on 64-bit systems.</span></span>

<span data-ttu-id="47a75-108">Per i sistemi a 32 bit, queste chiavi del registro di sistema di gestione della memoria devono essere create in modo esplicito nella seguente chiave del registro di sistema:</span><span class="sxs-lookup"><span data-stu-id="47a75-108">For 32-bit systems, these memory management registry keys must be explicitly created under the following registry key:</span></span>

<span data-ttu-id="47a75-109">**HKEY \_ \_** \\  \\  \\  \\  \\ **Gestione della memoria** del controllo del sistema di gestione delle sessioni del computer locale</span><span class="sxs-lookup"><span data-stu-id="47a75-109">**HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**Current Control Set**\\**Control**\\**Session Manager**\\**Memory Management**</span></span>

<span data-ttu-id="47a75-110">**Windows Server 2008 e Windows Vista:** Queste chiavi del registro di sistema sono disponibili nei sistemi a 32 bit a partire da Windows Server 2008 e Windows Vista con Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="47a75-110">**Windows Server 2008 and Windows Vista:** These registry keys are available on 32-bit systems starting with Windows Server 2008 and Windows Vista with Service Pack 1 (SP1).</span></span>

<span data-ttu-id="47a75-111">Per i limiti di memoria e spazio degli indirizzi predefiniti per i sistemi a 32 bit e a 64 bit, vedere [limiti di memoria per le versioni di Windows](memory-limits-for-windows-releases.md).</span><span class="sxs-lookup"><span data-stu-id="47a75-111">For default memory and address space limits on both 32-bit and 64-bit systems, see [Memory Limits for Windows Releases](memory-limits-for-windows-releases.md).</span></span>

<span data-ttu-id="47a75-112">La tabella seguente descrive le chiavi del registro di sistema di gestione della memoria che possono essere usate per configurare i limiti di memoria nei sistemi a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="47a75-112">The following table describes the memory management registry keys that can be used to configure memory limits on 32-bit systems.</span></span> <span data-ttu-id="47a75-113">Tutte queste chiavi hanno un tipo REG \_ DWORD e i valori possibili sono compresi tra 0 e 2.048 MB.</span><span class="sxs-lookup"><span data-stu-id="47a75-113">All of these keys have a REG\_DWORD type and possible values that range from 0 through 2,048 MB.</span></span> <span data-ttu-id="47a75-114">Il valore predefinito è 0, che indica che non viene applicato alcun limite.</span><span class="sxs-lookup"><span data-stu-id="47a75-114">The default is 0, which means no limit is enforced.</span></span> <span data-ttu-id="47a75-115">I valori vengono arrotondati automaticamente per eccesso al limite di allocazione del sistema successivo, ovvero 2 MB nei sistemi a 32 bit con [estensione di indirizzo fisico](physical-address-extension.md) (PAE) abilitata e 4 MB su sistemi a 32 bit in cui non è abilitata la funzionalità PAE.</span><span class="sxs-lookup"><span data-stu-id="47a75-115">Values are automatically rounded up to the next system VA allocation boundary, which is 2 MB on 32-bit systems that have [Physical Address Extension](physical-address-extension.md) (PAE) enabled and 4 MB on 32-bit systems that do not have PAE enabled.</span></span>



| <span data-ttu-id="47a75-116">Chiave</span><span class="sxs-lookup"><span data-stu-id="47a75-116">Key</span></span>                   | <span data-ttu-id="47a75-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="47a75-117">Description</span></span>                                                                                                                                                    |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47a75-118">**NonPagedPoolLimit**</span><span class="sxs-lookup"><span data-stu-id="47a75-118">**NonPagedPoolLimit**</span></span> | <span data-ttu-id="47a75-119">Specifica la quantità massima di spazio VA del sistema che può essere utilizzato dal pool non di paging.</span><span class="sxs-lookup"><span data-stu-id="47a75-119">Specifies the maximum amount of system VA space that can be used by the nonpaged pool.</span></span> <span data-ttu-id="47a75-120">In determinate condizioni, questo limite può essere superato da un importo ridotto.</span><span class="sxs-lookup"><span data-stu-id="47a75-120">Under certain conditions, this limit may be exceeded by a small amount.</span></span> |
| <span data-ttu-id="47a75-121">**PagedPoolLimit**</span><span class="sxs-lookup"><span data-stu-id="47a75-121">**PagedPoolLimit**</span></span>    | <span data-ttu-id="47a75-122">Specifica la quantità massima di spazio VA del sistema che può essere utilizzato dal pool di paging.</span><span class="sxs-lookup"><span data-stu-id="47a75-122">Specifies the maximum amount of system VA space that can be used by the paged pool.</span></span>                                                                            |
| <span data-ttu-id="47a75-123">**SessionSpaceLimit**</span><span class="sxs-lookup"><span data-stu-id="47a75-123">**SessionSpaceLimit**</span></span> | <span data-ttu-id="47a75-124">Specifica la quantità massima di spazio VA del sistema che può essere usata dalle allocazioni dello spazio di sessione.</span><span class="sxs-lookup"><span data-stu-id="47a75-124">Specifies the maximum amount of system VA space that can be used by session space allocations.</span></span>                                                                 |
| <span data-ttu-id="47a75-125">**SystemCacheLimit**</span><span class="sxs-lookup"><span data-stu-id="47a75-125">**SystemCacheLimit**</span></span>  | <span data-ttu-id="47a75-126">Specifica la quantità massima di spazio VA del sistema che può essere usata dalla cache di sistema.</span><span class="sxs-lookup"><span data-stu-id="47a75-126">Specifies the maximum amount of system VA space that can be used by the system cache.</span></span> <span data-ttu-id="47a75-127">In determinate condizioni, questo limite può essere superato da un importo ridotto.</span><span class="sxs-lookup"><span data-stu-id="47a75-127">Under certain conditions, this limit may be exceeded by a small amount.</span></span>  |
| <span data-ttu-id="47a75-128">**SystemPtesLimit**</span><span class="sxs-lookup"><span data-stu-id="47a75-128">**SystemPtesLimit**</span></span>   | <span data-ttu-id="47a75-129">Specifica la quantità massima di spazio di sistema che può essere utilizzato dai mapping I/O e da altre risorse che utilizzano le voci della tabella delle pagine di sistema (PTE).</span><span class="sxs-lookup"><span data-stu-id="47a75-129">Specifies the maximum amount of system VA space that can be used by I/O mappings and other resources that consume system page table entries (PTEs).</span></span>            |



 

<span data-ttu-id="47a75-130">Per determinare se lo spazio di sistema VA esaurito, è necessario usare un debugger del kernel.</span><span class="sxs-lookup"><span data-stu-id="47a75-130">Determining whether system VA space is being exhausted requires the use of a kernel debugger.</span></span> <span data-ttu-id="47a75-131">Per altre informazioni, vedere [Strumenti di debug per Windows](https://msdn.microsoft.com/library/cc267445.aspx).</span><span class="sxs-lookup"><span data-stu-id="47a75-131">For more information, see [Debugging Tools for Windows](https://msdn.microsoft.com/library/cc267445.aspx).</span></span>

 

 



