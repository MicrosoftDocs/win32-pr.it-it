---
description: È anche possibile specificare Alpha in un materiale. Per abilitare il materiale Alfa, impostare lo stato di rendering del materiale diffuso in modo che il runtime utilizzerà i componenti dei colori a diffusione del materiale anziché i componenti dei colori con diffusione del vertice.
ms.assetid: fd477d8f-d838-4a08-a8c6-38678798e0b0
title: Materiale Alfa (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f07ac2c28b497167f7bd742ecd8176b82b61e8f8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123339"
---
# <a name="material-alpha-direct3d-9"></a><span data-ttu-id="73f02-104">Materiale Alfa (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="73f02-104">Material Alpha (Direct3D 9)</span></span>

<span data-ttu-id="73f02-105">È anche possibile specificare Alpha in un materiale.</span><span class="sxs-lookup"><span data-stu-id="73f02-105">Alpha can also be supplied in a material.</span></span> <span data-ttu-id="73f02-106">Per abilitare il materiale Alfa, impostare lo stato di rendering del materiale diffuso in modo che il runtime utilizzerà i componenti dei colori a diffusione del materiale anziché i componenti dei colori con diffusione del vertice.</span><span class="sxs-lookup"><span data-stu-id="73f02-106">To enable material alpha, set the diffuse material render state so that the runtime will use the material diffuse color components rather than the vertex diffuse color components.</span></span>


```
m_pd3dDevice->SetRenderState( D3DRS_DIFFUSEMATERIALSOURCE, D3DMCS_MATERIAL );
```



<span data-ttu-id="73f02-107">Inizializzare il materiale con un valore alfa e impostare il materiale prima del disegno.</span><span class="sxs-lookup"><span data-stu-id="73f02-107">Initialize the material with an alpha value, and set the material before drawing.</span></span>


```
D3DMATERIAL9 mtrl;
mtrl.Diffuse = mtrl.Ambient = mtrl.Specular = mtrl.Emissive = 
    D3DCOLORVALUE(255,0,0,0.5f)

m_pd3dDevice->SetMaterial(&mtrl);     
```



## <a name="related-topics"></a><span data-ttu-id="73f02-108">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="73f02-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="73f02-109">Fusione alfa</span><span class="sxs-lookup"><span data-stu-id="73f02-109">Alpha Blending</span></span>](alpha-blending.md)
</dt> </dl>

 

 



