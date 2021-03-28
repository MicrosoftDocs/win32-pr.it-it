---
title: Formati stencil non supportati con le risorse affiancate
description: I formati che contengono stencil non sono supportati con le risorse affiancate.
ms.assetid: 1B675245-F21F-47B5-B3B4-C8307DAC575B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ce07b64e54808a2b4b730f6ed9c5321956f6bf5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104043993"
---
# <a name="stencil-formats-not-supported-with-tiled-resources"></a><span data-ttu-id="2b96c-103">Formati stencil non supportati con le risorse affiancate</span><span class="sxs-lookup"><span data-stu-id="2b96c-103">Stencil formats not supported with tiled resources</span></span>

<span data-ttu-id="2b96c-104">I formati che contengono stencil non sono supportati con le risorse affiancate.</span><span class="sxs-lookup"><span data-stu-id="2b96c-104">Formats that contain stencil aren't supported with tiled resources.</span></span>

<span data-ttu-id="2b96c-105">I formati che contengono stencil includono DXGI \_ Format \_ D24 \_ UNORM \_ S8 \_ uint (e i formati correlati nella famiglia R24G8) e DXGI \_ Format \_ D32 \_ float \_ S8X24 \_ uint (e i formati correlati nella famiglia R32G8X24).</span><span class="sxs-lookup"><span data-stu-id="2b96c-105">Formats that contain stencil include DXGI\_FORMAT\_D24\_UNORM\_S8\_UINT (and related formats in the R24G8 family) and DXGI\_FORMAT\_D32\_FLOAT\_S8X24\_UINT (and related formats in the R32G8X24 family).</span></span>

<span data-ttu-id="2b96c-106">Alcune implementazioni archiviano la profondità e lo stencil in allocazioni separate mentre altre le archiviano insieme.</span><span class="sxs-lookup"><span data-stu-id="2b96c-106">Some implementations store depth and stencil in separate allocations while others store them together.</span></span> <span data-ttu-id="2b96c-107">La gestione dei riquadri per i due schemi dovrebbe essere diversa e nessuna API singola può astrarre o razionalizzare le differenze.</span><span class="sxs-lookup"><span data-stu-id="2b96c-107">Tile management for the two schemes would have to be different, and no single API can abstract or rationalize the differences.</span></span> <span data-ttu-id="2b96c-108">Si consiglia di usare un hardware futuro per supportare superfici di profondità e stencil indipendenti, ognuna affiancata in modo indipendente.</span><span class="sxs-lookup"><span data-stu-id="2b96c-108">We recommend for future hardware to support independent depth and stencil surfaces, each independently tiled.</span></span> <span data-ttu-id="2b96c-109">32 i riquadri di profondità di bit 128x128 e gli stencil a 8 bit avrebbero riquadri 256x256.</span><span class="sxs-lookup"><span data-stu-id="2b96c-109">32 bit depth would have 128x128 tiles, and 8 bit stencil would have 256x256 tiles.</span></span> <span data-ttu-id="2b96c-110">Pertanto, le applicazioni devono vivere con un errato allineamento delle forme dei riquadri tra profondità e stencil.</span><span class="sxs-lookup"><span data-stu-id="2b96c-110">Therefore, applications would have to live with tile shape misalignment between depth and stencil.</span></span> <span data-ttu-id="2b96c-111">Tuttavia, lo stesso problema esiste già con formati di superficie di destinazione di rendering diversi.</span><span class="sxs-lookup"><span data-stu-id="2b96c-111">But the same problem exists with different render target surface formats already.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2b96c-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2b96c-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2b96c-113">Condivisione tra processi e dispositivi affiancati per le risorse</span><span class="sxs-lookup"><span data-stu-id="2b96c-113">Tiled resource cross process and device sharing</span></span>](tiled-resource-cross-process-and-device-sharing.md)
</dt> </dl>

 

 




