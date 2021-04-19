---
description: 'Il gestore della memoria crea i pool di memoria seguenti usati dal sistema per allocare memoria: pool non di paging e pool di paging.'
ms.assetid: 68ee9c72-f3a3-4f1f-a827-ed4210a665e4
title: Pool di memoria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60987b43347e55d8ee2d01672dbb8173ffc8dd5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319449"
---
# <a name="memory-pools"></a><span data-ttu-id="a099b-103">Pool di memoria</span><span class="sxs-lookup"><span data-stu-id="a099b-103">Memory Pools</span></span>

<span data-ttu-id="a099b-104">Il gestore della memoria crea i pool di memoria seguenti usati dal sistema per allocare memoria: pool non di paging e pool di paging.</span><span class="sxs-lookup"><span data-stu-id="a099b-104">The memory manager creates the following memory pools that the system uses to allocate memory: nonpaged pool and paged pool.</span></span> <span data-ttu-id="a099b-105">Entrambi i pool di memoria si trovano nell'area dello spazio degli indirizzi riservata al sistema e mappati allo spazio degli indirizzi virtuali di ogni processo.</span><span class="sxs-lookup"><span data-stu-id="a099b-105">Both memory pools are located in the region of the address space that is reserved for the system and mapped into the virtual address space of each process.</span></span> <span data-ttu-id="a099b-106">Il pool non di paging è costituito da indirizzi di memoria virtuale che devono risiedere nella memoria fisica finché vengono allocati gli oggetti kernel corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="a099b-106">The nonpaged pool consists of virtual memory addresses that are guaranteed to reside in physical memory as long as the corresponding kernel objects are allocated.</span></span> <span data-ttu-id="a099b-107">Il pool di paging è costituito da memoria virtuale di cui è possibile effettuare il paging all'interno e all'esterno del sistema.</span><span class="sxs-lookup"><span data-stu-id="a099b-107">The paged pool consists of virtual memory that can be paged in and out of the system.</span></span> <span data-ttu-id="a099b-108">Per migliorare le prestazioni, i sistemi con un solo processore hanno tre pool di paging e i sistemi multiprocessore hanno cinque pool di paging.</span><span class="sxs-lookup"><span data-stu-id="a099b-108">To improve performance, systems with a single processor have three paged pools, and multiprocessor systems have five paged pools.</span></span>

<span data-ttu-id="a099b-109">Gli handle per [gli oggetti kernel](../sysinfo/kernel-objects.md) vengono archiviati nel pool di paging, quindi il numero di handle che è possibile creare è basato sulla memoria disponibile.</span><span class="sxs-lookup"><span data-stu-id="a099b-109">The handles for [kernel objects](../sysinfo/kernel-objects.md) are stored in the paged pool, so the number of handles you can create is based on available memory.</span></span>

<span data-ttu-id="a099b-110">Il sistema registra i limiti e i valori correnti per il pool non di paging, il pool di paging e l'utilizzo del file di paging.</span><span class="sxs-lookup"><span data-stu-id="a099b-110">The system records the limits and current values for its nonpaged pool, paged pool, and page file usage.</span></span> <span data-ttu-id="a099b-111">Per ulteriori informazioni, vedere [informazioni sulle prestazioni della memoria](memory-performance-information.md).</span><span class="sxs-lookup"><span data-stu-id="a099b-111">For more information, see [Memory Performance Information](memory-performance-information.md).</span></span>

 

 
