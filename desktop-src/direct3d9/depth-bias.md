---
description: È possibile fare in modo che i poligoni complanari nello spazio 3D appaiano come se non fossero complanari aggiungendo una distorsione z a ciascuna di esse.
ms.assetid: 0ab4f63b-49de-4bd0-a10f-6f90b9706c58
title: Distorsione profondità (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ce605ea1df161e5ebfed95c214c3dd180ab7ee6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481564"
---
# <a name="depth-bias-direct3d-9"></a><span data-ttu-id="630df-103">Distorsione profondità (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="630df-103">Depth Bias (Direct3D 9)</span></span>

<span data-ttu-id="630df-104">È possibile fare in modo che i poligoni complanari nello spazio 3D appaiano come se non fossero complanari aggiungendo una distorsione z a ciascuna di esse.</span><span class="sxs-lookup"><span data-stu-id="630df-104">Polygons that are coplanar in your 3D space can be made to appear as if they are not coplanar by adding a z-bias to each one.</span></span> <span data-ttu-id="630df-105">Si tratta di una tecnica comunemente utilizzata per garantire che le ombre in una scena vengano visualizzate correttamente.</span><span class="sxs-lookup"><span data-stu-id="630df-105">This is a technique commonly used to ensure that shadows in a scene are displayed properly.</span></span> <span data-ttu-id="630df-106">Ad esempio, un'ombreggiatura su una parete avrà probabilmente lo stesso valore di profondità del muro.</span><span class="sxs-lookup"><span data-stu-id="630df-106">For instance, a shadow on a wall will likely have the same depth value as the wall does.</span></span> <span data-ttu-id="630df-107">Se si esegue il rendering del muro per primo e poi l'ombreggiatura, l'ombreggiatura potrebbe non essere visibile oppure gli artefatti di profondità potrebbero essere visibili.</span><span class="sxs-lookup"><span data-stu-id="630df-107">If you render the wall first and then the shadow, the shadow might not be visible, or depth artifacts might be visible.</span></span> <span data-ttu-id="630df-108">È possibile invertire l'ordine in cui si esegue il rendering degli oggetti complanari nella speranza di inversare l'effetto, ma è probabile che gli artefatti di profondità siano ancora disponibili.</span><span class="sxs-lookup"><span data-stu-id="630df-108">You can reverse the order in which you render the coplanar objects in hopes of reversing the effect, but depth artifacts are still likely.</span></span>

<span data-ttu-id="630df-109">Un'applicazione può garantire che i poligoni compostivi vengano sottoposti a rendering correttamente aggiungendo una distorsione ai valori z usati dal sistema durante il rendering dei set di poligoni complanari.</span><span class="sxs-lookup"><span data-stu-id="630df-109">An application can help ensure that coplanar polygons are rendered properly by adding a bias to the z-values that the system uses when rendering the sets of coplanar polygons.</span></span> <span data-ttu-id="630df-110">Per aggiungere una polarizzazione z a un set di poligoni, chiamare il metodo [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) immediatamente prima di eseguirne il rendering, impostando il parametro *state* su D3DRS \_ DEPTHBIAS e il parametro *value* su un valore float adatto (ad esempio, un valore appropriato può essere compreso tra-1,0 e 1,0). per passare questo valore a **SetRenderState**, è necessario eseguire il cast del valore a **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="630df-110">To add a z-bias to a set of polygons, call the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method just before rendering them, setting the *State* parameter to D3DRS\_DEPTHBIAS, and the *Value* parameter to a suitable float value (for example, a suitable value might be from -1.0 to 1.0); to pass this value to **SetRenderState**, you must also cast the value to a **DWORD**.</span></span> <span data-ttu-id="630df-111">Un valore di distorsione z superiore aumenta la probabilità che i poligoni di cui viene eseguito il rendering siano visibili quando vengono visualizzati con altri poligoni complanari.</span><span class="sxs-lookup"><span data-stu-id="630df-111">A higher z-bias value increases the likelihood that the polygons you render will be visible when displayed with other coplanar polygons.</span></span>


```
Offset = m * D3DRS_SLOPESCALEDEPTHBIAS + D3DRS_DEPTHBIAS
```



<span data-ttu-id="630df-112">dove m è la pendenza massima della profondità del triangolo sottoposto a rendering.</span><span class="sxs-lookup"><span data-stu-id="630df-112">where m is the maximum depth slope of the triangle being rendered.</span></span>


```
m = max(abs(delta z / delta x), abs(delta z / delta y)) 
```



<span data-ttu-id="630df-113">Le unità per gli \_ Stati di rendering D3DRS DEPTHBIAS e D3DRS \_ SLOPESCALEDEPTHBIAS variano a seconda che sia abilitata la funzionalità di buffering z o w.</span><span class="sxs-lookup"><span data-stu-id="630df-113">The units for the D3DRS\_DEPTHBIAS and D3DRS\_SLOPESCALEDEPTHBIAS render states depend on whether z-buffering or w-buffering is enabled.</span></span> <span data-ttu-id="630df-114">L'applicazione deve fornire valori appropriati.</span><span class="sxs-lookup"><span data-stu-id="630df-114">The application must provide suitable values.</span></span>

<span data-ttu-id="630df-115">La distorsione non viene applicata a nessuna primitiva di linea e punto.</span><span class="sxs-lookup"><span data-stu-id="630df-115">The bias is not applied to any line and point primitive.</span></span> <span data-ttu-id="630df-116">Questa distorsione deve tuttavia essere applicata a triangoli disegnati in modalità wireframe.</span><span class="sxs-lookup"><span data-stu-id="630df-116">However, this bias needs to be applied to triangles drawn in wireframe mode.</span></span>


```
// RenderStates
D3DRS_SLOPESCALEDEPTHBIAS, // Defaults to zero
D3DRS_DEPTHBIAS,           // Defaults to zero
```




```
// Caps
D3DPRASTERCAPS_DEPTHBIAS           
D3DPRASTERCAPS_SLOPESCALEDEPTHBIAS 
```



## <a name="related-topics"></a><span data-ttu-id="630df-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="630df-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="630df-118">Pipeline pixel</span><span class="sxs-lookup"><span data-stu-id="630df-118">Pixel Pipeline</span></span>](pixel-pipeline.md)
</dt> </dl>

 

 
