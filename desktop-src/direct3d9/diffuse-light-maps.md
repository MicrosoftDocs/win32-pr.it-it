---
description: Quando illuminato da una sorgente di luce, le superfici opache visualizzano la reflection chiara diffusa.
ms.assetid: a6ed351a-7889-4993-96bf-b03352a815da
title: Mappe chiare diffuse (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ab6a85fb93bc1ebcc15735431c1d54be4482a1f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481541"
---
# <a name="diffuse-light-maps-direct3d-9"></a><span data-ttu-id="b24b6-103">Mappe chiare diffuse (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="b24b6-103">Diffuse Light Maps (Direct3D 9)</span></span>

<span data-ttu-id="b24b6-104">Quando illuminato da una sorgente di luce, le superfici opache visualizzano la reflection chiara diffusa.</span><span class="sxs-lookup"><span data-stu-id="b24b6-104">When illuminated by a light source, matte surfaces display diffuse light reflection.</span></span> <span data-ttu-id="b24b6-105">La luminosità della luce diffusa dipende dalla distanza dalla sorgente di luce e dall'angolo tra la normale della superficie e il vettore di direzione della sorgente di luce.</span><span class="sxs-lookup"><span data-stu-id="b24b6-105">The brightness of diffuse light depends on the distance from the light source and the angle between the surface normal and the light source direction vector.</span></span> <span data-ttu-id="b24b6-106">Gli effetti di illuminazione diffusi simulati dai calcoli di illuminazione producono solo effetti generali.</span><span class="sxs-lookup"><span data-stu-id="b24b6-106">The diffuse lighting effects simulated by lighting calculations produce only general effects.</span></span>

<span data-ttu-id="b24b6-107">L'applicazione è in grado di simulare un'illuminazione diffusa più complessa con texture Light maps.</span><span class="sxs-lookup"><span data-stu-id="b24b6-107">Your application can simulate more complex diffuse lighting with texture light maps.</span></span> <span data-ttu-id="b24b6-108">A tale scopo, aggiungere il mapping della luce diffusa alla trama di base, come illustrato nell'esempio di codice C++ riportato di seguito.</span><span class="sxs-lookup"><span data-stu-id="b24b6-108">Do this by adding the diffuse light map to the base texture, as shown in the following C++ code example.</span></span>


```
// This example assumes that d3dDevice is a valid pointer to an
// IDirect3DDevice9 interface.
// lptexBaseTexture is a valid pointer to a texture.
// lptexDiffuseLightMap is a valid pointer to a texture that contains 
// RGB diffuse light map data.

// Set the base texture.
d3dDevice->SetTexture(0,lptexBaseTexture );

// Set the base texture operation and args.
d3dDevice->SetTextureStageState(0,D3DTSS_COLOROP,
                                D3DTOP_MODULATE );
d3dDevice->SetTextureStageState(0,D3DTSS_COLORARG1, D3DTA_TEXTURE );
d3dDevice->SetTextureStageState(0,D3DTSS_COLORARG2, D3DTA_DIFFUSE );

// Set the diffuse light map.
d3dDevice->SetTexture(1,lptexDiffuseLightMap );

// Set the blend stage.
d3dDevice->SetTextureStageState(1, D3DTSS_COLOROP, D3DTOP_MODULATE );
d3dDevice->SetTextureStageState(1, D3DTSS_COLORARG1, D3DTA_TEXTURE );
d3dDevice->SetTextureStageState(1, D3DTSS_COLORARG2, D3DTA_CURRENT );
```



## <a name="related-topics"></a><span data-ttu-id="b24b6-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b24b6-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b24b6-110">Mapping chiaro con trame</span><span class="sxs-lookup"><span data-stu-id="b24b6-110">Light Mapping with Textures</span></span>](light-mapping-with-textures.md)
</dt> </dl>

 

 



