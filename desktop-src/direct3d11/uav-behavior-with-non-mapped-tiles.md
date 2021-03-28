---
title: Comportamento di UAV con riquadri non mappati
description: Il comportamento delle letture e scritture degli accessi (UAV) non ordinati dipende dal livello di supporto hardware.
ms.assetid: 26C40D1F-983B-4E5B-99F3-FD4E47BE1D7D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a9909f8faecd3345761ae26e60835c77aae9ab3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955223"
---
# <a name="uav-behavior-with-non-mapped-tiles"></a><span data-ttu-id="89606-103">Comportamento di UAV con riquadri non mappati</span><span class="sxs-lookup"><span data-stu-id="89606-103">UAV behavior with non-mapped tiles</span></span>

<span data-ttu-id="89606-104">Il comportamento delle letture e scritture degli accessi (UAV) non ordinati dipende dal livello di supporto hardware.</span><span class="sxs-lookup"><span data-stu-id="89606-104">Behavior of unordered access view (UAV) reads and writes depends on the level of hardware support.</span></span> <span data-ttu-id="89606-105">Per una suddivisione dei requisiti, vedere il comportamento complessivo di lettura e scrittura per [le risorse affiancate livelli di funzionalità](tiled-resources-features-tiers.md).</span><span class="sxs-lookup"><span data-stu-id="89606-105">For a breakdown of requirements, see overall read and write behavior for [Tiled resources features tiers](tiled-resources-features-tiers.md).</span></span> <span data-ttu-id="89606-106">In questa sezione viene riepilogato il comportamento ideale.</span><span class="sxs-lookup"><span data-stu-id="89606-106">This section summarizes the ideal behavior.</span></span>

<span data-ttu-id="89606-107">Le operazioni dello shader che leggono da un riquadro non mappato in un UAV restituiscono 0 in tutti i componenti non mancanti del formato e l'impostazione predefinita per i componenti mancanti.</span><span class="sxs-lookup"><span data-stu-id="89606-107">Shader operations that read from a non-mapped tile in a UAV return 0 in all non-missing components of the format, and the default for missing components.</span></span>

<span data-ttu-id="89606-108">Le operazioni dello shader che tentano di scrivere in un riquadro non mappato non comportano la scrittura di elementi nell'area non mappata (mentre le Scritture in un'area mappata procedono).</span><span class="sxs-lookup"><span data-stu-id="89606-108">Shader operations that attempt to write to a non-mapped tile cause nothing to be written to the non-mapped area (while writes to a mapped area proceed).</span></span> <span data-ttu-id="89606-109">Questa definizione ideale per la gestione delle Scritture non è richiesta dal [livello 2](tier-2.md). le scritture nei riquadri non mappati possono finire in una cache che le letture successive potrebbero prelevare.</span><span class="sxs-lookup"><span data-stu-id="89606-109">This ideal definition for write handling is not required by [Tier 2](tier-2.md); writes to non-mapped tiles can end up in a cache that subsequent reads could pick up.</span></span>

## <a name="related-topics"></a><span data-ttu-id="89606-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="89606-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="89606-111">Accesso alla pipeline alle risorse affiancate</span><span class="sxs-lookup"><span data-stu-id="89606-111">Pipeline access to tiled resources</span></span>](pipeline-access-to-tiled-resources.md)
</dt> </dl>

 

 




