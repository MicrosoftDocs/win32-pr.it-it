---
description: Viene creata un'istanza di questo modello in base a mesh solo in mesh che contengono informazioni di skinning esportate. Lo scopo di questo modello è fornire informazioni sulla natura delle informazioni di skinning esportate.
ms.assetid: 95a4fa45-63d1-4931-9c91-b26807d2b043
title: XSkinMeshHeader
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 306f8c183086846fca020040af00b9ccef2665cc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104401291"
---
# <a name="xskinmeshheader"></a><span data-ttu-id="4b773-104">XSkinMeshHeader</span><span class="sxs-lookup"><span data-stu-id="4b773-104">XSkinMeshHeader</span></span>

<span data-ttu-id="4b773-105">Viene creata un'istanza di questo modello in base a mesh solo in mesh che contengono informazioni di skinning esportate.</span><span class="sxs-lookup"><span data-stu-id="4b773-105">This template is instantiated on a per-mesh basis only in meshes that contain exported skinning information.</span></span> <span data-ttu-id="4b773-106">Lo scopo di questo modello è fornire informazioni sulla natura delle informazioni di skinning esportate.</span><span class="sxs-lookup"><span data-stu-id="4b773-106">The purpose of this template is to provide information about the nature of the skinning information that was exported.</span></span>

``` syntax
template XSkinMeshHeader 
{ 
    < 3CF169CE-FF7C-44ab-93C0-F78F62D172E2 >  
    WORD nMaxSkinWeightsPerVertex; 
    WORD nMaxSkinWeightsPerFace; 
    WORD nBones; 
}
```

<span data-ttu-id="4b773-107">Dove:</span><span class="sxs-lookup"><span data-stu-id="4b773-107">Where:</span></span>

-   <span data-ttu-id="4b773-108">nMaxSkinWeightsPerVertex: numero massimo di trasformazioni che interessano un vertice nella mesh.</span><span class="sxs-lookup"><span data-stu-id="4b773-108">nMaxSkinWeightsPerVertex - Maximum number of transforms that affect a vertex in the mesh.</span></span>
-   <span data-ttu-id="4b773-109">nMaxSkinWeightsPerFace: numero massimo di trasformazioni univoche che interessano i tre vertici di qualsiasi faccia.</span><span class="sxs-lookup"><span data-stu-id="4b773-109">nMaxSkinWeightsPerFace - Maximum number of unique transforms that affect the three vertices of any face.</span></span>
-   <span data-ttu-id="4b773-110">nBones: numero di ossa che interessano i vertici in questa mesh.</span><span class="sxs-lookup"><span data-stu-id="4b773-110">nBones - Number of bones that affect vertices in this mesh.</span></span>

## <a name="see-also"></a><span data-ttu-id="4b773-111">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4b773-111">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b773-112">Modelli</span><span class="sxs-lookup"><span data-stu-id="4b773-112">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



