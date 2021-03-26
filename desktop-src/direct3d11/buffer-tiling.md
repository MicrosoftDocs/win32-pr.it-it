---
title: Divisione in riquadri di buffer
description: Una risorsa buffer è divisa in riquadri 64KB, con uno spazio vuoto nell'ultimo riquadro se la dimensione non è un multiplo di 64KB.
ms.assetid: 979EFCF3-1FE1-412A-A19D-F1B1CF86423B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 061fafa009e554499822c90c8fb6c0c8f34e47f9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872585"
---
# <a name="buffer-tiling"></a><span data-ttu-id="bf002-103">Divisione in riquadri di buffer</span><span class="sxs-lookup"><span data-stu-id="bf002-103">Buffer tiling</span></span>

<span data-ttu-id="bf002-104">Una risorsa [buffer](overviews-direct3d-11-resources-buffers.md) è divisa in riquadri 64KB, con uno spazio vuoto nell'ultimo riquadro se la dimensione non è un multiplo di 64KB.</span><span class="sxs-lookup"><span data-stu-id="bf002-104">A [Buffer](overviews-direct3d-11-resources-buffers.md) resource is divided into 64KB tiles, with some empty space in the last tile if the size is not a multiple of 64KB.</span></span>

<span data-ttu-id="bf002-105">I buffer strutturati non devono avere vincoli sullo stride da affiancare.</span><span class="sxs-lookup"><span data-stu-id="bf002-105">Structured buffers must have no constraint on the stride to be tiled.</span></span> <span data-ttu-id="bf002-106">Tuttavia, le possibili ottimizzazioni delle prestazioni nell'hardware per l'uso di [**StructuredBuffers**](/windows/desktop/direct3dhlsl/sm5-object-structuredbuffer) possono essere sacrificate, rendendole in primo luogo affiancate.</span><span class="sxs-lookup"><span data-stu-id="bf002-106">But possible performance optimizations in hardware for using [**StructuredBuffers**](/windows/desktop/direct3dhlsl/sm5-object-structuredbuffer) can be sacrificed by making them tiled in the first place.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bf002-107">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bf002-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bf002-108">Come affiancare l'area di una risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="bf002-108">How a tiled resource's area is tiled</span></span>](how-a-tiled-resource-s-area-is-tiled.md)
</dt> </dl>

 

 