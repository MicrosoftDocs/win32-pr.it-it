---
title: Spazio degli indirizzi disponibile per le risorse affiancate
description: In questa sezione viene specificato lo spazio degli indirizzi virtuale disponibile per le risorse affiancate.
ms.assetid: A3D08564-3C7A-4578-BC38-EE202045580A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c774c697cf5d3bf575d01ce5751dc413c1d14b0
ms.sourcegitcommit: 4dcafeb002cbee4f6028b32a956ec22cb95cbc44
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/13/2019
ms.locfileid: "103719327"
---
# <a name="address-space-available-for-tiled-resources"></a><span data-ttu-id="59e71-103">Spazio degli indirizzi disponibile per le risorse affiancate</span><span class="sxs-lookup"><span data-stu-id="59e71-103">Address space available for tiled resources</span></span>

<span data-ttu-id="59e71-104">In questa sezione viene specificato lo spazio degli indirizzi virtuale disponibile per le risorse affiancate.</span><span class="sxs-lookup"><span data-stu-id="59e71-104">This section specifies the virtual address space that is available for tiled resources.</span></span>

<span data-ttu-id="59e71-105">Nei sistemi operativi a 64 bit sono disponibili almeno 40 bit di spazio degli indirizzi virtuali (1 terabyte).</span><span class="sxs-lookup"><span data-stu-id="59e71-105">On 64-bit operating systems, at least 40 bits of virtual address space (1 Terabyte) is available.</span></span>

<span data-ttu-id="59e71-106">Per i sistemi operativi a 32 bit, lo spazio degli indirizzi è 32 bit (4 GB).</span><span class="sxs-lookup"><span data-stu-id="59e71-106">For 32-bit operating systems, the address space is 32 bit (4 GB).</span></span> <span data-ttu-id="59e71-107">Per i sistemi ARM a 32 bit, la creazione di singole risorse affiancate può non riuscire se l'allocazione utilizzerà più di 27 bit di spazio degli indirizzi (128 MB).</span><span class="sxs-lookup"><span data-stu-id="59e71-107">For 32-bit ARM systems, individual tiled resource creation can fail if the allocation would use more than 27 bits of address space (128 MB).</span></span> <span data-ttu-id="59e71-108">Sono incluse eventuali spaziatura interna nascosta nello spazio degli indirizzi che l'hardware può usare per mipmap, riempimento affiancato e possibilmente dimensioni della superficie di riempimento a potenze di 2.</span><span class="sxs-lookup"><span data-stu-id="59e71-108">This includes any hidden padding in the address space the hardware may use for mipmaps, packed tile padding, and possibly padding surface dimensions to powers of 2.</span></span>

<span data-ttu-id="59e71-109">Nei sistemi grafici con una tabella di pagina separata per l'unità di elaborazione grafica (GPU), la maggior parte di questo spazio di indirizzi sarà disponibile per le risorse GPU eseguite dall'applicazione, sebbene le allocazioni GPU eseguite dal driver di visualizzazione rientrino nello stesso spazio.</span><span class="sxs-lookup"><span data-stu-id="59e71-109">On graphics systems with a separate page table for the graphics processing unit (GPU), most of this address space will be available to GPU resources made by the application, though GPU allocations made by the display driver fit in the same space.</span></span>

<span data-ttu-id="59e71-110">Nei sistemi futuri con una tabella di pagina condivisa tra la CPU e la GPU, lo spazio degli indirizzi disponibile viene condiviso tra tutte le allocazioni di CPU e GPU in un processo.</span><span class="sxs-lookup"><span data-stu-id="59e71-110">On future systems with a page table shared between the CPU and GPU, the available address space is shared between all CPU and GPU allocations in a process.</span></span>

## <a name="related-topics"></a><span data-ttu-id="59e71-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="59e71-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="59e71-112">Parametri per la creazione di risorse affiancate</span><span class="sxs-lookup"><span data-stu-id="59e71-112">Tiled resource creation parameters</span></span>](tiled-resource-creation-parameters.md)
</dt> </dl>

 

 




