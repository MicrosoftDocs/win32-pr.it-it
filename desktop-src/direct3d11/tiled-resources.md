---
title: Risorse affiancate
description: Le risorse affiancate possono essere considerate come risorse logiche di grandi dimensioni che utilizzano piccole quantità di memoria fisica.
ms.assetid: 03083460-192b-40cb-8ee1-76df6d95f72b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7c7e6aaf60f58f55274c9d7a135b9107933f640
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855549"
---
# <a name="tiled-resources"></a><span data-ttu-id="5abb4-103">Risorse affiancate</span><span class="sxs-lookup"><span data-stu-id="5abb4-103">Tiled resources</span></span>

<span data-ttu-id="5abb4-104">Le risorse affiancate possono essere considerate come risorse logiche di grandi dimensioni che utilizzano piccole quantità di memoria fisica.</span><span class="sxs-lookup"><span data-stu-id="5abb4-104">Tiled resources can be thought of as large logical resources that use small amounts of physical memory.</span></span>

<span data-ttu-id="5abb4-105">In questa sezione viene descritto il motivo per cui sono necessarie risorse affiancate e la modalità di creazione e utilizzo di risorse affiancate.</span><span class="sxs-lookup"><span data-stu-id="5abb4-105">This section describes why tiled resources are needed and how you create and use tiled resources.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="5abb4-106">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="5abb4-106">In this section</span></span>



| <span data-ttu-id="5abb4-107">Argomento</span><span class="sxs-lookup"><span data-stu-id="5abb4-107">Topic</span></span>                                                                                   | <span data-ttu-id="5abb4-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5abb4-108">Description</span></span>                                                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5abb4-109">Perché sono necessarie risorse affiancate?</span><span class="sxs-lookup"><span data-stu-id="5abb4-109">Why are tiled resources needed?</span></span>](why-are-tiled-resources-needed-.md)<br/>       | <span data-ttu-id="5abb4-110">Le risorse affiancate sono necessarie, in modo che la memoria dell'unità di elaborazione grafica (GPU) venga sprecata per l'archiviazione di aree di superfici che l'applicazione sa non sarà accessibile e l'hardware possa comprendere come filtrare tra i riquadri adiacenti.</span><span class="sxs-lookup"><span data-stu-id="5abb4-110">Tiled resources are needed so less graphics processing unit (GPU) memory is wasted storing regions of surfaces that the application knows will not be accessed, and the hardware can understand how to filter across adjacent tiles.</span></span><br/>     |
| [<span data-ttu-id="5abb4-111">Creazione di risorse affiancate</span><span class="sxs-lookup"><span data-stu-id="5abb4-111">Creating tiled resources</span></span>](creating-tiled-resources.md)<br/>                     | <span data-ttu-id="5abb4-112">Quando si crea una risorsa, le risorse affiancate vengono create specificando il flag di [**\_ \_ varie \_ risorse di d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) .</span><span class="sxs-lookup"><span data-stu-id="5abb4-112">Tiled resources are created by specifying the [**D3D11\_RESOURCE\_MISC\_TILED**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) flag when you create a resource.</span></span><br/>                                                                                          |
| [<span data-ttu-id="5abb4-113">API di risorse affiancate</span><span class="sxs-lookup"><span data-stu-id="5abb4-113">Tiled Resource APIs</span></span>](tiled-resource-apis.md)<br/>                               | <span data-ttu-id="5abb4-114">Le API descritte in questa sezione funzionano con le risorse affiancate e il pool di sezioni.</span><span class="sxs-lookup"><span data-stu-id="5abb4-114">The APIs described in this section work with tiled resources and tile pool.</span></span><br/>                                                                                                                                                              |
| [<span data-ttu-id="5abb4-115">Accesso alla pipeline alle risorse affiancate</span><span class="sxs-lookup"><span data-stu-id="5abb4-115">Pipeline access to tiled resources</span></span>](pipeline-access-to-tiled-resources.md)<br/> | <span data-ttu-id="5abb4-116">Le risorse affiancate possono essere usate in visualizzazioni di risorse shader (SRV), visualizzazioni di destinazione di rendering (RTV), viste depth stencil (DSV) e viste di accesso non ordinate (UAV), nonché alcuni punti di binding in cui non vengono usate le visualizzazioni, ad esempio le associazioni del buffer dei vertici.</span><span class="sxs-lookup"><span data-stu-id="5abb4-116">Tiled resources can be used in shader resource views (SRV), render target views (RTV), depth stencil views (DSV) and unordered access views (UAV), as well as some bind points where views aren't used, such as vertex buffer bindings.</span></span> <br/> |
| [<span data-ttu-id="5abb4-117">Livelli di funzionalità delle risorse affiancate</span><span class="sxs-lookup"><span data-stu-id="5abb4-117">Tiled resources features tiers</span></span>](tiled-resources-features-tiers.md)<br/>         | <span data-ttu-id="5abb4-118">Direct3D 11,2 espone il supporto di risorse affiancate in due livelli con i valori del [**\_ \_ \_ livello di risorse affiancati d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier) .</span><span class="sxs-lookup"><span data-stu-id="5abb4-118">Direct3D 11.2 exposes tiled resources support in two tiers with the [**D3D11\_TILED\_RESOURCES\_TIER**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier) values.</span></span> <br/>                                                                                         |



 

## <a name="related-topics"></a><span data-ttu-id="5abb4-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5abb4-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5abb4-120">Risorse</span><span class="sxs-lookup"><span data-stu-id="5abb4-120">Resources</span></span>](overviews-direct3d-11-resources.md)
</dt> </dl>

 

 





