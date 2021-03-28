---
title: Livelli di funzionalità delle risorse affiancate
description: Direct3D 11,2 espone il supporto di risorse affiancate in due livelli con i \_ valori del livello di risorse affiancati d3d11 \_ \_ .
ms.assetid: E6A6565B-079B-47DB-A80C-CA5B5413BA32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2282cde1dfc8c4249672d18e303a4529338d4fbf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955224"
---
# <a name="tiled-resources-features-tiers"></a><span data-ttu-id="77f11-103">Livelli di funzionalità delle risorse affiancate</span><span class="sxs-lookup"><span data-stu-id="77f11-103">Tiled resources features tiers</span></span>

<span data-ttu-id="77f11-104">Direct3D 11,2 espone il supporto di risorse affiancate in due livelli con i valori del [**\_ \_ \_ livello di risorse affiancati d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier) .</span><span class="sxs-lookup"><span data-stu-id="77f11-104">Direct3D 11.2 exposes tiled resources support in two tiers with the [**D3D11\_TILED\_RESOURCES\_TIER**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier) values.</span></span>

<span data-ttu-id="77f11-105">Per eseguire una query per determinare se l'hardware e il driver supportano le risorse affiancate e a quale livello di livello, passare la [**\_ funzionalità d3d11 \_ d3d11 \_ OPTIONS1**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature) valore al parametro *feature* di [**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport).</span><span class="sxs-lookup"><span data-stu-id="77f11-105">To query whether the hardware and driver support tiled resources and at what tier level, pass the [**D3D11\_FEATURE\_D3D11\_OPTIONS1**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature) value to the *Feature* parameter of [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport).</span></span> <span data-ttu-id="77f11-106">Inoltre, passare un puntatore alla struttura [**d3d11 \_ \_ data \_ d3d11 \_ OPTIONS1**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options1) al parametro *pFeatureSupportData* e passare la dimensione **della struttura d3d11 d3d11 OPTIONS1 al parametro \_ \_ \_ \_** *FeatureSupportDataSize* .</span><span class="sxs-lookup"><span data-stu-id="77f11-106">Also, pass a pointer to the [**D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS1**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options1) structure to the *pFeatureSupportData* parameter, and pass the size of the **D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS1** structure to the *FeatureSupportDataSize* parameter.</span></span> <span data-ttu-id="77f11-107">**CheckFeatureSupport** restituisce il livello di livello come valore del [**\_ \_ \_ livello di risorse affiancato d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier) nel membro **TiledResourcesTier** dei **dati della \_ funzionalità d3d11 \_ \_ d3d11 \_** OPTIONS1.</span><span class="sxs-lookup"><span data-stu-id="77f11-107">**CheckFeatureSupport** returns the tier level as a [**D3D11\_TILED\_RESOURCES\_TIER**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier) value in the **TiledResourcesTier** member of **D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS1**.</span></span>

<span data-ttu-id="77f11-108">In questa sezione vengono descritti questi due livelli.</span><span class="sxs-lookup"><span data-stu-id="77f11-108">This section describes these two tiers.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="77f11-109">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="77f11-109">In this section</span></span>



| <span data-ttu-id="77f11-110">Argomento</span><span class="sxs-lookup"><span data-stu-id="77f11-110">Topic</span></span>                           | <span data-ttu-id="77f11-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="77f11-111">Description</span></span>                                       |
|---------------------------------|---------------------------------------------------|
| [<span data-ttu-id="77f11-112">Livello 1</span><span class="sxs-lookup"><span data-stu-id="77f11-112">Tier 1</span></span>](tier-1.md)<br/> | <span data-ttu-id="77f11-113">In questa sezione viene descritto il supporto di livello 1.</span><span class="sxs-lookup"><span data-stu-id="77f11-113">This section describes tier 1 support.</span></span><br/> |
| [<span data-ttu-id="77f11-114">Livello 2</span><span class="sxs-lookup"><span data-stu-id="77f11-114">Tier 2</span></span>](tier-2.md)<br/> | <span data-ttu-id="77f11-115">In questa sezione viene descritto il supporto di livello 2.</span><span class="sxs-lookup"><span data-stu-id="77f11-115">This section describes tier 2 support.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="77f11-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="77f11-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="77f11-117">Risorse affiancate</span><span class="sxs-lookup"><span data-stu-id="77f11-117">Tiled resources</span></span>](tiled-resources.md)
</dt> </dl>

 

 





