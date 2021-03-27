---
title: Comportamento di SRV con riquadri non mappati
description: Il comportamento delle letture di visualizzazione risorse shader (SRV) che coinvolgono i riquadri non mappati dipende dal livello di supporto hardware.
ms.assetid: 9B720BEE-AB0C-4B75-92AD-3F382A107D48
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e086a4db869c3204fc560e64002ba04e8bd8ba9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104220899"
---
# <a name="srv-behavior-with-non-mapped-tiles"></a><span data-ttu-id="15d3d-103">Comportamento di SRV con riquadri non mappati</span><span class="sxs-lookup"><span data-stu-id="15d3d-103">SRV behavior with non-mapped tiles</span></span>

<span data-ttu-id="15d3d-104">Il comportamento delle letture di visualizzazione risorse shader (SRV) che coinvolgono i riquadri non mappati dipende dal livello di supporto hardware.</span><span class="sxs-lookup"><span data-stu-id="15d3d-104">Behavior of shader resource view (SRV) reads that involve non-mapped tiles depends on the level of hardware support.</span></span> <span data-ttu-id="15d3d-105">Per una suddivisione dei requisiti, vedere il comportamento di lettura per [le funzionalità di risorse affiancate livelli](tiled-resources-features-tiers.md).</span><span class="sxs-lookup"><span data-stu-id="15d3d-105">For a breakdown of requirements, see read behavior for [Tiled resources features tiers](tiled-resources-features-tiers.md).</span></span> <span data-ttu-id="15d3d-106">Questa sezione riepiloga il comportamento ideale, che richiede il [livello 2](tier-2.md) .</span><span class="sxs-lookup"><span data-stu-id="15d3d-106">This section summarizes the ideal behavior, which [Tier 2](tier-2.md) requires.</span></span>

<span data-ttu-id="15d3d-107">Si consideri un'operazione di filtro di trama che legge da un set di Texel in un SRV.</span><span class="sxs-lookup"><span data-stu-id="15d3d-107">Consider a texture filter operation that reads from a set of texels in an SRV.</span></span> <span data-ttu-id="15d3d-108">I Texel che rientrano in riquadri non mappati contribuiscono 0 in tutti i componenti non mancanti del formato (e l'impostazione predefinita per i componenti mancanti) nell'operazione di filtro complessiva insieme ai contributi provenienti da Texel mappati.</span><span class="sxs-lookup"><span data-stu-id="15d3d-108">Texels that fall on non-mapped tiles contribute 0 in all non-missing components of the format (and the default for missing components) into the overall filter operation alongside contributions from mapped texels.</span></span> <span data-ttu-id="15d3d-109">I Texel sono tutti ponderati e combinati insieme indipendentemente dal fatto che i dati provengano da tessere mappate o non mappate.</span><span class="sxs-lookup"><span data-stu-id="15d3d-109">The texels are all weighted and combined together independent of whether the data came from mapped or non-mapped tiles.</span></span>

<span data-ttu-id="15d3d-110">Alcuni componenti hardware di livello [2](tier-2.md) di primo livello non soddisfano questo requisito della specifica e restituisce 0 con i valori predefiniti descritti in precedenza come risultato del filtro generale se i Texel (con peso diverso da zero) rientrano in riquadri non mappati.</span><span class="sxs-lookup"><span data-stu-id="15d3d-110">Some first generation [Tier 2](tier-2.md) level hardware does not meet this spec requirement and returns the 0 with defaults described preceding as the overall filter result if any texels (with nonzero weight) fall on non-mapped tiles.</span></span> <span data-ttu-id="15d3d-111">Nessun altro hardware potrà perdere il requisito di includere tutti i Texel (valore diverso da zero) nel filtro.</span><span class="sxs-lookup"><span data-stu-id="15d3d-111">No other hardware will be allowed to miss the requirement to include all (nonzero weight) texels in the filter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="15d3d-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="15d3d-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="15d3d-113">Accesso alla pipeline alle risorse affiancate</span><span class="sxs-lookup"><span data-stu-id="15d3d-113">Pipeline access to tiled resources</span></span>](pipeline-access-to-tiled-resources.md)
</dt> </dl>

 

 




