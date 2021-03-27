---
title: Accesso alla pipeline alle risorse affiancate
description: Le risorse affiancate possono essere usate in visualizzazioni di risorse shader (SRV), visualizzazioni di destinazione di rendering (RTV), viste depth stencil (DSV) e viste di accesso non ordinate (UAV), nonché alcuni punti di binding in cui non vengono usate le visualizzazioni, ad esempio le associazioni del buffer dei vertici.
ms.assetid: D0BC0B6C-2325-4EAF-9E80-E748F58045B1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef4a183fcaee90d84985a09c83826a4ad0b6d646
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729255"
---
# <a name="pipeline-access-to-tiled-resources"></a><span data-ttu-id="0d751-103">Accesso alla pipeline alle risorse affiancate</span><span class="sxs-lookup"><span data-stu-id="0d751-103">Pipeline access to tiled resources</span></span>

<span data-ttu-id="0d751-104">Le risorse affiancate possono essere usate in visualizzazioni di risorse shader (SRV), visualizzazioni di destinazione di rendering (RTV), viste depth stencil (DSV) e viste di accesso non ordinate (UAV), nonché alcuni punti di binding in cui non vengono usate le visualizzazioni, ad esempio le associazioni del buffer dei vertici.</span><span class="sxs-lookup"><span data-stu-id="0d751-104">Tiled resources can be used in shader resource views (SRV), render target views (RTV), depth stencil views (DSV) and unordered access views (UAV), as well as some bind points where views aren't used, such as vertex buffer bindings.</span></span> <span data-ttu-id="0d751-105">Per l'elenco dei binding supportati, vedere [parametri di creazione di risorse affiancati](tiled-resource-creation-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="0d751-105">For the list of supported bindings, see [Tiled resource creation parameters](tiled-resource-creation-parameters.md).</span></span> <span data-ttu-id="0d751-106">\*Le operazioni di copia funzionano anche con le risorse affiancate.</span><span class="sxs-lookup"><span data-stu-id="0d751-106">Copy\* operations also work on tiled resources.</span></span>

<span data-ttu-id="0d751-107">Se più coordinate del riquadro in una o più visualizzazioni sono vincolate alla stessa posizione di memoria, le letture e le Scritture da percorsi diversi alla stessa memoria si verificheranno in un ordine non deterministico e non ripetibile di accessi alla memoria.</span><span class="sxs-lookup"><span data-stu-id="0d751-107">If multiple tile coordinates in one or more views is bound to the same memory location, reads and writes from different paths to the same memory will occur in a non-deterministic and non-repeatable order of memory accesses.</span></span>

<span data-ttu-id="0d751-108">Se tutti i riquadri dietro un footprint di accesso alla memoria da uno shader vengono mappati a tessere univoche, il comportamento è identico in tutte le implementazioni della superficie con lo stesso contenuto della memoria in modalità non affiancata.</span><span class="sxs-lookup"><span data-stu-id="0d751-108">If all tiles behind a memory access footprint from a shader are mapped to unique tiles, behavior is identical on all implementations to the surface having the same memory contents in a non-tiled fashion.</span></span>

<span data-ttu-id="0d751-109">In questa sezione vengono fornite ulteriori informazioni sull'accesso alla pipeline per le risorse affiancate.</span><span class="sxs-lookup"><span data-stu-id="0d751-109">This section provides more info about pipeline access to tiled resources.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="0d751-110">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="0d751-110">In this section</span></span>



| <span data-ttu-id="0d751-111">Argomento</span><span class="sxs-lookup"><span data-stu-id="0d751-111">Topic</span></span>                                                                                                              | <span data-ttu-id="0d751-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0d751-112">Description</span></span>                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0d751-113">Comportamento di SRV con riquadri non mappati</span><span class="sxs-lookup"><span data-stu-id="0d751-113">SRV behavior with non-mapped tiles</span></span>](srv-behavior-with-non-mapped-tiles.md)<br/>                            | <span data-ttu-id="0d751-114">Il comportamento delle letture di visualizzazione risorse shader (SRV) che coinvolgono i riquadri non mappati dipende dal livello di supporto hardware.</span><span class="sxs-lookup"><span data-stu-id="0d751-114">Behavior of shader resource view (SRV) reads that involve non-mapped tiles depends on the level of hardware support.</span></span> <br/>                                          |
| [<span data-ttu-id="0d751-115">Comportamento di UAV con riquadri non mappati</span><span class="sxs-lookup"><span data-stu-id="0d751-115">UAV behavior with non-mapped tiles</span></span>](uav-behavior-with-non-mapped-tiles.md)<br/>                            | <span data-ttu-id="0d751-116">Il comportamento delle letture e scritture degli accessi (UAV) non ordinati dipende dal livello di supporto hardware.</span><span class="sxs-lookup"><span data-stu-id="0d751-116">Behavior of unordered access view (UAV) reads and writes depends on the level of hardware support.</span></span> <br/>                                                            |
| [<span data-ttu-id="0d751-117">Comportamento del rasterizzatore con riquadri non mappati</span><span class="sxs-lookup"><span data-stu-id="0d751-117">Rasterizer behavior with non-mapped tiles</span></span>](rasterizer-behavior-with-non-mapped-tiles.md)<br/>              | <span data-ttu-id="0d751-118">Questa sezione descrive il comportamento di rasterizzazione con riquadri non mappati.</span><span class="sxs-lookup"><span data-stu-id="0d751-118">This section describes rasterizer behavior with non-mapped tiles.</span></span><br/>                                                                                              |
| [<span data-ttu-id="0d751-119">Limitazioni di accesso ai riquadri con mapping duplicati</span><span class="sxs-lookup"><span data-stu-id="0d751-119">Tile access limitations with duplicate mappings</span></span>](tile-access-limitations-with-duplicate-mappings-.md)<br/> | <span data-ttu-id="0d751-120">Questa sezione descrive le limitazioni di accesso ai riquadri con mapping duplicati.</span><span class="sxs-lookup"><span data-stu-id="0d751-120">This section describes tile access limitations with duplicate mappings.</span></span><br/>                                                                                        |
| [<span data-ttu-id="0d751-121">Funzionalità di campionamento della trama delle risorse affiancate</span><span class="sxs-lookup"><span data-stu-id="0d751-121">Tiled resources texture sampling features</span></span>](tiled-resources-texture-sampling-features.md)<br/>              | <span data-ttu-id="0d751-122">Questa sezione descrive le funzionalità di campionamento delle trame di risorse affiancate.</span><span class="sxs-lookup"><span data-stu-id="0d751-122">This section describes tiled resources texture sampling features.</span></span><br/>                                                                                              |
| [<span data-ttu-id="0d751-123">Esposizione delle risorse affiancate HLSL</span><span class="sxs-lookup"><span data-stu-id="0d751-123">HLSL tiled resources exposure</span></span>](hlsl-tiled-resources-exposure.md)<br/>                                      | <span data-ttu-id="0d751-124">Per supportare le risorse affiancate nel [modello di shader 5](/windows/desktop/direct3dhlsl/d3d11-graphics-reference-sm5)è necessaria la nuova sintassi Microsoft High Level Shader Language (HLSL).</span><span class="sxs-lookup"><span data-stu-id="0d751-124">New Microsoft High Level Shader Language (HLSL) syntax is required to support tiled resources in [Shader Model 5](/windows/desktop/direct3dhlsl/d3d11-graphics-reference-sm5).</span></span> <br/> |



 

## <a name="related-topics"></a><span data-ttu-id="0d751-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0d751-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0d751-126">Risorse affiancate</span><span class="sxs-lookup"><span data-stu-id="0d751-126">Tiled resources</span></span>](tiled-resources.md)
</dt> </dl>

 

