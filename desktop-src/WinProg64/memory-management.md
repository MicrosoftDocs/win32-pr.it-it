---
title: Gestione della memoria in WOW64
description: La gestione della memoria in WOW64 dipende dall'architettura del processore.
ms.assetid: a3fa6e51-2895-4941-9304-5939208e8102
keywords:
- Programmazione Windows WOW64 a 64 bit, gestione della memoria
- gestione della memoria-programmazione Windows a 64 bit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8602bf6e7e7d9e55894215938932559cfadc6848
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399584"
---
# <a name="memory-management-under-wow64"></a><span data-ttu-id="62897-105">Gestione della memoria in WOW64</span><span class="sxs-lookup"><span data-stu-id="62897-105">Memory Management Under WOW64</span></span>

<span data-ttu-id="62897-106">La gestione della memoria in WOW64 dipende dall'architettura del processore.</span><span class="sxs-lookup"><span data-stu-id="62897-106">Memory management under WOW64 depends on the processor architecture.</span></span>

## <a name="itanium-support"></a><span data-ttu-id="62897-107">Supporto di Itanium</span><span class="sxs-lookup"><span data-stu-id="62897-107">Itanium Support</span></span>

<span data-ttu-id="62897-108">WOW64 simula le pagine da 4 KB nella parte superiore delle pagine native da 8 KB utilizzate dal processore Itanium.</span><span class="sxs-lookup"><span data-stu-id="62897-108">WOW64 simulates 4 KB pages on top of the native 8 KB pages that the Itanium processor uses.</span></span> <span data-ttu-id="62897-109">Il processore contribuisce a offrire una simulazione eccellente con sovraccarico ridotto.</span><span class="sxs-lookup"><span data-stu-id="62897-109">The processor assists by providing excellent simulation with low overhead.</span></span> <span data-ttu-id="62897-110">Il codice di simulazione non può gestire i casi seguenti:</span><span class="sxs-lookup"><span data-stu-id="62897-110">The simulation code cannot handle the following cases:</span></span>

-   <span data-ttu-id="62897-111">Rilevamento delle Scritture.</span><span class="sxs-lookup"><span data-stu-id="62897-111">Write tracking.</span></span> <span data-ttu-id="62897-112">Le funzioni [**GetWriteWatch**](/windows/desktop/api/memoryapi/nf-memoryapi-getwritewatch) e [**ResetWriteWatch**](/windows/desktop/api/memoryapi/nf-memoryapi-resetwritewatch) sono implementate nel kernel usando la granularità nativa della dimensione della pagina, il che significa che la simulazione della pagina di WOW64 4 KB non è in grado di determinare quali pagine simulate da 4 KB vengono scritte nella pagina di 8 KB sottostante.</span><span class="sxs-lookup"><span data-stu-id="62897-112">The [**GetWriteWatch**](/windows/desktop/api/memoryapi/nf-memoryapi-getwritewatch) and [**ResetWriteWatch**](/windows/desktop/api/memoryapi/nf-memoryapi-resetwritewatch) functions are implemented in the kernel using native page-size granularity, which means the WOW64 4 KB page simulation cannot determine which simulated 4 KB pages are written within the underlying 8 KB page.</span></span>
-   <span data-ttu-id="62897-113">[Address Windowing Extensions (AWE)](/windows/desktop/Memory/address-windowing-extensions).</span><span class="sxs-lookup"><span data-stu-id="62897-113">[Address Windowing Extensions (AWE)](/windows/desktop/Memory/address-windowing-extensions).</span></span> <span data-ttu-id="62897-114">Le funzioni AWE operano sui numeri di pagina e non è possibile eseguire il mapping dei numeri di pagina a 64 bit ai numeri di pagina a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="62897-114">The AWE functions operate on page numbers, and there is no way to map 64-bit page numbers to 32-bit page numbers.</span></span>
-   <span data-ttu-id="62897-115">Allineamento della sezione.</span><span class="sxs-lookup"><span data-stu-id="62897-115">Section alignment.</span></span> <span data-ttu-id="62897-116">Per le immagini eseguibili con allineamento della sezione inferiore a 8 KB (il valore predefinito è 4 KB per le immagini x86), WOW64 deve Dirty all image Pages.</span><span class="sxs-lookup"><span data-stu-id="62897-116">For executable images with section alignment smaller than 8 KB (the default is 4 KB for x86 images), WOW64 must dirty all image pages.</span></span> <span data-ttu-id="62897-117">In questo modo, ogni pagina viene copiata nel file di paging e le pagine di immagine di sola lettura non vengono condivise tra i processi.</span><span class="sxs-lookup"><span data-stu-id="62897-117">This effectively copies each page to the page file, and prevents read-only image pages from being shared between processes.</span></span>
-   <span data-ttu-id="62897-118">Le funzioni [**ReadFileScatter**](/windows/desktop/api/fileapi/nf-fileapi-readfilescatter) e [**WriteFileGather**](/windows/desktop/api/fileapi/nf-fileapi-writefilegather) non sono supportate.</span><span class="sxs-lookup"><span data-stu-id="62897-118">The [**ReadFileScatter**](/windows/desktop/api/fileapi/nf-fileapi-readfilescatter) and [**WriteFileGather**](/windows/desktop/api/fileapi/nf-fileapi-writefilegather) functions are not supported.</span></span>

## <a name="x64-and-arm64-support"></a><span data-ttu-id="62897-119">Supporto per x64 e ARM64</span><span class="sxs-lookup"><span data-stu-id="62897-119">x64 and ARM64 Support</span></span>

<span data-ttu-id="62897-120">Le dimensioni della pagina nativa sono pari a 4 KB.</span><span class="sxs-lookup"><span data-stu-id="62897-120">The native page size is 4 KB.</span></span> <span data-ttu-id="62897-121">Di conseguenza, sono supportati gli elementi seguenti:</span><span class="sxs-lookup"><span data-stu-id="62897-121">Therefore, the following are supported:</span></span>

-   <span data-ttu-id="62897-122">Sono supportate le funzioni [**GetWriteWatch**](/windows/desktop/api/memoryapi/nf-memoryapi-getwritewatch) e [**ResetWriteWatch**](/windows/desktop/api/memoryapi/nf-memoryapi-resetwritewatch) .</span><span class="sxs-lookup"><span data-stu-id="62897-122">The [**GetWriteWatch**](/windows/desktop/api/memoryapi/nf-memoryapi-getwritewatch) and [**ResetWriteWatch**](/windows/desktop/api/memoryapi/nf-memoryapi-resetwritewatch) functions are supported.</span></span>
-   <span data-ttu-id="62897-123">Sono supportate le funzioni [**ReadFileScatter**](/windows/desktop/api/fileapi/nf-fileapi-readfilescatter) e [**WriteFileGather**](/windows/desktop/api/fileapi/nf-fileapi-writefilegather) .</span><span class="sxs-lookup"><span data-stu-id="62897-123">The [**ReadFileScatter**](/windows/desktop/api/fileapi/nf-fileapi-readfilescatter) and [**WriteFileGather**](/windows/desktop/api/fileapi/nf-fileapi-writefilegather) functions are supported.</span></span>
-   <span data-ttu-id="62897-124">L'uso di indirizzi di grandi dimensioni è vantaggioso perché x64 WOW64 supporta uno spazio degli indirizzi virtuali da 4 GB.</span><span class="sxs-lookup"><span data-stu-id="62897-124">There are advantages to using large addresses because x64 WOW64 supports a 4 GB virtual address space.</span></span>

## <a name="related-topics"></a><span data-ttu-id="62897-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="62897-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="62897-126">Limiti di memoria per le versioni di Windows</span><span class="sxs-lookup"><span data-stu-id="62897-126">Memory Limits for Windows Releases</span></span>](/windows/desktop/Memory/memory-limits-for-windows-releases)
</dt> <dt>

[<span data-ttu-id="62897-127">Ottimizzazione della RAM 4GT</span><span class="sxs-lookup"><span data-stu-id="62897-127">4GT RAM Tuning</span></span>](/windows/desktop/Memory/4-gigabyte-tuning)
</dt> </dl>

 

 