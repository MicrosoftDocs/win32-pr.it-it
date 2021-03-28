---
title: Comportamento del rasterizzatore con riquadri non mappati
description: Questa sezione descrive il comportamento di rasterizzazione con riquadri non mappati.
ms.assetid: 3477A621-7051-4585-AB58-523EE64CDC5C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54230321f4286b92a3444e3f74167ee7b8711c3f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104992813"
---
# <a name="rasterizer-behavior-with-non-mapped-tiles"></a><span data-ttu-id="99d2f-103">Comportamento del rasterizzatore con riquadri non mappati</span><span class="sxs-lookup"><span data-stu-id="99d2f-103">Rasterizer behavior with non-mapped tiles</span></span>

<span data-ttu-id="99d2f-104">Questa sezione descrive il comportamento di rasterizzazione con riquadri non mappati.</span><span class="sxs-lookup"><span data-stu-id="99d2f-104">This section describes rasterizer behavior with non-mapped tiles.</span></span>

## <a name="depthstencilview"></a><span data-ttu-id="99d2f-105">DepthStencilView</span><span class="sxs-lookup"><span data-stu-id="99d2f-105">DepthStencilView</span></span>

<span data-ttu-id="99d2f-106">Il comportamento delle letture e scritture di depth stencil (DSV) dipende dal livello di supporto hardware.</span><span class="sxs-lookup"><span data-stu-id="99d2f-106">Behavior of depth stencil view (DSV) reads and writes depends on the level of hardware support.</span></span> <span data-ttu-id="99d2f-107">Per una suddivisione dei requisiti, vedere il comportamento complessivo di lettura e scrittura per [le risorse affiancate livelli di funzionalità](tiled-resources-features-tiers.md).</span><span class="sxs-lookup"><span data-stu-id="99d2f-107">For a breakdown of requirements, see overall read and write behavior for [Tiled resources features tiers](tiled-resources-features-tiers.md).</span></span>

<span data-ttu-id="99d2f-108">Ecco il comportamento ideale:</span><span class="sxs-lookup"><span data-stu-id="99d2f-108">Here is the ideal behavior:</span></span>

<span data-ttu-id="99d2f-109">Se non è stato eseguito il mapping di un riquadro in DepthStencilView, il valore restituito dalla profondità di lettura è 0, che viene quindi inserito in qualsiasi operazione configurata per il valore di lettura profondità.</span><span class="sxs-lookup"><span data-stu-id="99d2f-109">If a tile isn't mapped in the DepthStencilView, the return value from reading depth is 0, which is then fed into whatever operations are configured for the depth read value.</span></span> <span data-ttu-id="99d2f-110">Le Scritture nel riquadro di profondità mancante vengono rimosse.</span><span class="sxs-lookup"><span data-stu-id="99d2f-110">Writes to the missing depth tile are dropped.</span></span> <span data-ttu-id="99d2f-111">Questa definizione ideale per la gestione delle Scritture non è richiesta dal [livello 2](tier-2.md). le scritture nei riquadri non mappati possono finire in una cache che le letture successive potrebbero prelevare.</span><span class="sxs-lookup"><span data-stu-id="99d2f-111">This ideal definition for write handling is not required by [Tier 2](tier-2.md); writes to non-mapped tiles can end up in a cache that subsequent reads could pick up.</span></span>

## <a name="rendertargetview"></a><span data-ttu-id="99d2f-112">RenderTargetView</span><span class="sxs-lookup"><span data-stu-id="99d2f-112">RenderTargetView</span></span>

<span data-ttu-id="99d2f-113">Il comportamento delle letture e scritture di visualizzazione della destinazione di rendering (RTV) dipende dal livello di supporto hardware.</span><span class="sxs-lookup"><span data-stu-id="99d2f-113">Behavior of render target view (RTV) reads and writes depends on the level of hardware support.</span></span> <span data-ttu-id="99d2f-114">Per una suddivisione dei requisiti, vedere il comportamento complessivo di lettura e scrittura per [le risorse affiancate livelli di funzionalità](tiled-resources-features-tiers.md).</span><span class="sxs-lookup"><span data-stu-id="99d2f-114">For a breakdown of requirements, see overall read and write behavior for [Tiled resources features tiers](tiled-resources-features-tiers.md).</span></span>

<span data-ttu-id="99d2f-115">In tutte le implementazioni, i diversi RTVs (e vista origine dati) associati simultaneamente possono avere aree diverse mappate rispetto a quelle non mappate e possono avere formati di superficie di dimensioni diverse, ovvero diverse forme affiancate.</span><span class="sxs-lookup"><span data-stu-id="99d2f-115">On all implementations, different RTVs (and DSV) bound simultaneously can have different areas mapped versus non-mapped and can have different sized surface formats (which means different tile shapes).</span></span>

<span data-ttu-id="99d2f-116">Ecco il comportamento ideale:</span><span class="sxs-lookup"><span data-stu-id="99d2f-116">Here is the ideal behavior:</span></span>

<span data-ttu-id="99d2f-117">Le letture da RTVs restituiscono 0 nei riquadri mancanti e le scritture vengono rimosse.</span><span class="sxs-lookup"><span data-stu-id="99d2f-117">Reads from RTVs return 0 in missing tiles and writes are dropped.</span></span> <span data-ttu-id="99d2f-118">Questa definizione ideale per la gestione delle Scritture non è richiesta dal [livello 2](tier-2.md). le scritture nei riquadri non mappati possono finire in una cache che le letture successive potrebbero prelevare.</span><span class="sxs-lookup"><span data-stu-id="99d2f-118">This ideal definition for write handling is not required by [Tier 2](tier-2.md); writes to non-mapped tiles can end up in a cache that subsequent reads could pick up.</span></span>

## <a name="related-topics"></a><span data-ttu-id="99d2f-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="99d2f-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="99d2f-120">Accesso alla pipeline alle risorse affiancate</span><span class="sxs-lookup"><span data-stu-id="99d2f-120">Pipeline access to tiled resources</span></span>](pipeline-access-to-tiled-resources.md)
</dt> </dl>

 

 




