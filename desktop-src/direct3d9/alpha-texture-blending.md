---
description: Il motore di illuminazione combina il colore del materiale, il colore del vertice e le informazioni sull'illuminazione per generare un colore per ogni vertice.
ms.assetid: 1e7c31cb-dc63-4f4a-9ddc-d1d1d0b69085
title: Fusione di trame alfa (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ad394b70b96e17b2ce858f871fb869afde0d122
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304996"
---
# <a name="alpha-texture-blending-direct3d-9"></a><span data-ttu-id="a6d49-103">Fusione di trame alfa (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="a6d49-103">Alpha Texture Blending (Direct3D 9)</span></span>

<span data-ttu-id="a6d49-104">Il motore di illuminazione combina il colore del materiale, il colore del vertice e le informazioni sull'illuminazione per generare un colore per ogni vertice.</span><span class="sxs-lookup"><span data-stu-id="a6d49-104">The lighting engine combines material color, vertex color, and lighting information to generate a per-vertex color.</span></span> <span data-ttu-id="a6d49-105">Una volta interpolata, viene generato un colore per pixel che viene scritto nel buffer del frame.</span><span class="sxs-lookup"><span data-stu-id="a6d49-105">Once interpolated, this generates a per-pixel color that is written to the frame buffer.</span></span> <span data-ttu-id="a6d49-106">Se un'applicazione Abilita la fusione di trame, il colore del pixel diventerà una combinazione del pixel corrente nel buffer del frame e di un colore della trama.</span><span class="sxs-lookup"><span data-stu-id="a6d49-106">If an application enables texture blending, the pixel color will become a combination of the current pixel in the frame buffer and a texture color.</span></span>

<span data-ttu-id="a6d49-107">Questa formula determina il colore finale del pixel Blend:</span><span class="sxs-lookup"><span data-stu-id="a6d49-107">This formula determines the final blended pixel color:</span></span>


```
Color = TexelColor x SourceBlend + CurrentPixelColor x DestBlend
```



<span data-ttu-id="a6d49-108">Dove:</span><span class="sxs-lookup"><span data-stu-id="a6d49-108">Where:</span></span>

-   <span data-ttu-id="a6d49-109">Color è il colore del pixel di output.</span><span class="sxs-lookup"><span data-stu-id="a6d49-109">Color is the output pixel color.</span></span>
-   <span data-ttu-id="a6d49-110">TexelColor è il colore di input dopo il filtro della trama.</span><span class="sxs-lookup"><span data-stu-id="a6d49-110">TexelColor is the input color after texture filtering.</span></span>
-   <span data-ttu-id="a6d49-111">SourceBlend è la percentuale del colore finale del pixel che è costituita dal colore di Texel di origine.</span><span class="sxs-lookup"><span data-stu-id="a6d49-111">SourceBlend is the percentage of the final pixel color that is made up of the source texel color.</span></span>
-   <span data-ttu-id="a6d49-112">CurrentPixelColor è il colore del pixel corrente.</span><span class="sxs-lookup"><span data-stu-id="a6d49-112">CurrentPixelColor is the color of the current pixel.</span></span>
-   <span data-ttu-id="a6d49-113">DestBlend è la percentuale del colore finale del pixel che è costituita dal colore del pixel corrente.</span><span class="sxs-lookup"><span data-stu-id="a6d49-113">DestBlend is the percentage of the final pixel color that is made up of the current pixel color.</span></span>

<span data-ttu-id="a6d49-114">L'equazione di Blend finale viene impostata chiamando [**IDirect3DDevice9:: SetRenderState**](/windows/desktop/api) e specificando lo stato di rendering di Blend (D3DRS \_ BLENDXXX) con un fattore di fusione corrispondente ([**D3DBLEND**](./d3dblend.md)).</span><span class="sxs-lookup"><span data-stu-id="a6d49-114">The final blending equation is set by calling [**IDirect3DDevice9::SetRenderState**](/windows/desktop/api) and specifying the blend render state (D3DRS\_BLENDXXX) with a corresponding blending factor ([**D3DBLEND**](./d3dblend.md)).</span></span> <span data-ttu-id="a6d49-115">I valori di SourceBlend e DestBlend variano da 0,0 (trasparente) a 1,0 (opaco) inclusi.</span><span class="sxs-lookup"><span data-stu-id="a6d49-115">The values of SourceBlend and DestBlend range from 0.0 (transparent) to 1.0 (opaque) inclusive.</span></span> <span data-ttu-id="a6d49-116">Inoltre, un'applicazione può controllare la trasparenza di un pixel impostando il valore alfa in una trama.</span><span class="sxs-lookup"><span data-stu-id="a6d49-116">In addition, an application can control the transparency of a pixel by setting the alpha value in a texture.</span></span> <span data-ttu-id="a6d49-117">In questo caso, utilizzare quanto segue:</span><span class="sxs-lookup"><span data-stu-id="a6d49-117">In this case, use the following:</span></span>


```
SourceBlend = D3DBLEND_ZERO 
DestBlend = D3DBLEND_ONE
```



<span data-ttu-id="a6d49-118">L'equazione di fusione provocherà la trasparenza del pixel sottoposto a rendering.</span><span class="sxs-lookup"><span data-stu-id="a6d49-118">The blending equation will cause the rendered pixel to be transparent.</span></span> <span data-ttu-id="a6d49-119">I valori predefiniti sono:</span><span class="sxs-lookup"><span data-stu-id="a6d49-119">The default values are:</span></span>


```
SourceBlend = D3DBLEND_SRCALPHA 
DestBlend = D3DBLEND_INVSRCALPHA
```



## <a name="related-topics"></a><span data-ttu-id="a6d49-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a6d49-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a6d49-121">Combinazione di trame</span><span class="sxs-lookup"><span data-stu-id="a6d49-121">Texture Blending</span></span>](texture-blending.md)
</dt> <dt>

[<span data-ttu-id="a6d49-122">Filtraggio delle trame (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="a6d49-122">Texture Filtering (Direct3D 9)</span></span>](texture-filtering.md)
</dt> <dt>

[<span data-ttu-id="a6d49-123">**D3DRENDERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="a6d49-123">**D3DRENDERSTATETYPE**</span></span>](./d3drenderstatetype.md)
</dt> </dl>

 

 
