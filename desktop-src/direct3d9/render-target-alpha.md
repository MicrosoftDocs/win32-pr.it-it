---
description: Il Blend buffer frame è ora in grado di fondere i canali alfa indipendentemente dalla combinazione del canale dei colori nelle destinazioni di rendering. Questo controllo è abilitato con un nuovo stato di rendering, D3DRS \_ SEPARATEALPHABLENDENABLE.
ms.assetid: 6d30b13e-f4c6-4bc4-8735-15c398c099f1
title: Alfa destinazione rendering (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b70f395406559782172448b5555daff056ffd54c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520474"
---
# <a name="render-target-alpha-direct3d-9"></a><span data-ttu-id="a85c0-104">Alfa destinazione rendering (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="a85c0-104">Render Target Alpha (Direct3D 9)</span></span>

<span data-ttu-id="a85c0-105">Il Blend buffer frame è ora in grado di fondere i canali alfa indipendentemente dalla combinazione del canale dei colori nelle destinazioni di rendering.</span><span class="sxs-lookup"><span data-stu-id="a85c0-105">The frame buffer blender can now blend alpha channels independent from color-channel blending on render targets.</span></span> <span data-ttu-id="a85c0-106">Questo controllo è abilitato con un nuovo stato di rendering, D3DRS \_ SEPARATEALPHABLENDENABLE.</span><span class="sxs-lookup"><span data-stu-id="a85c0-106">This control is enabled with a new render state, D3DRS\_SEPARATEALPHABLENDENABLE.</span></span>

<span data-ttu-id="a85c0-107">Quando D3DRS \_ SEPARATEALPHABLENDENABLE è impostato su **false** (condizione predefinita), le operazioni e i fattori di combinazione della destinazione di rendering applicati ad Alpha corrispondono a quelli definiti per la fusione dei canali dei colori.</span><span class="sxs-lookup"><span data-stu-id="a85c0-107">When D3DRS\_SEPARATEALPHABLENDENABLE is set to **FALSE** (which is the default condition), the render-target blending factors and operations applied to alpha are the same as those defined for blending color channels.</span></span> <span data-ttu-id="a85c0-108">Un driver deve impostare D3DPMISCCAPS \_ SEPARATEALPHABLEND Cap per indicare che può supportare la fusione alfa di destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="a85c0-108">A driver needs to set the D3DPMISCCAPS\_SEPARATEALPHABLEND cap to indicate that it can support render-target alpha blending.</span></span> <span data-ttu-id="a85c0-109">Assicurarsi di abilitare D3DRS \_ AlphaBlend per indicare alla pipeline che è necessaria la fusione alfa.</span><span class="sxs-lookup"><span data-stu-id="a85c0-109">Be sure to enable D3DRS\_ALPHABLEND to tell the pipeline that alpha blending is needed.</span></span>

<span data-ttu-id="a85c0-110">Per controllare i fattori nel canale alfa dei Blender di destinazione di rendering, due nuovi Stati di rendering vengono definiti come segue:</span><span class="sxs-lookup"><span data-stu-id="a85c0-110">To control the factors in the alpha channel of the render-target blenders, two new render states are defined as follows:</span></span>


```
D3DRS_SRCBLENDALPHA 
D3DRS_DESTBLENDALPHA 
```



<span data-ttu-id="a85c0-111">Come D3DRS \_ SRCBLEND e D3DRS \_ DESTBLEND, questi possono essere impostati su uno dei valori nell'enumerazione [**D3DBLEND**](./d3dblend.md) .</span><span class="sxs-lookup"><span data-stu-id="a85c0-111">Like the D3DRS\_SRCBLEND and D3DRS\_DESTBLEND, these can be set to one of the values in the [**D3DBLEND**](./d3dblend.md) enumeration.</span></span> <span data-ttu-id="a85c0-112">Le impostazioni di Blend di origine e di destinazione possono essere combinate in diversi modi, a seconda delle impostazioni nei membri SrcBlendCaps e DestBlendCaps di [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="a85c0-112">The source and destination blend settings can be combined in several ways, depending on the settings in the SrcBlendCaps and DestBlendCaps members of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

<span data-ttu-id="a85c0-113">La fusione alfa viene eseguita come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="a85c0-113">The alpha blending is done as follows:</span></span>

<span data-ttu-id="a85c0-114">renderTargetAlpha = (Alpha<sub>in</sub> \* srcBlendOp) BlendOp (Alpha<sub>RT</sub> \* destBlendOp)</span><span class="sxs-lookup"><span data-stu-id="a85c0-114">renderTargetAlpha = (alpha<sub>in</sub> \* srcBlendOp) BlendOp (alpha<sub>rt</sub> \* destBlendOp)</span></span>

<span data-ttu-id="a85c0-115">Dove:</span><span class="sxs-lookup"><span data-stu-id="a85c0-115">Where:</span></span>

-   <span data-ttu-id="a85c0-116">alfa<sub>in</sub> è il valore alfa di input.</span><span class="sxs-lookup"><span data-stu-id="a85c0-116">alpha<sub>in</sub> is the input alpha value.</span></span>
-   <span data-ttu-id="a85c0-117">srcBlendOp è uno dei fattori di Blend in [**D3DBLEND**](./d3dblend.md).</span><span class="sxs-lookup"><span data-stu-id="a85c0-117">srcBlendOp is one of the blend factors in [**D3DBLEND**](./d3dblend.md).</span></span>
-   <span data-ttu-id="a85c0-118">BlendOp è uno dei fattori di Blend in [**D3DBLENDOP**](./d3dblendop.md).</span><span class="sxs-lookup"><span data-stu-id="a85c0-118">BlendOp is one of the blend factors in [**D3DBLENDOP**](./d3dblendop.md).</span></span>
-   <span data-ttu-id="a85c0-119">alfa<sub>RT</sub> è il valore alfa della destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="a85c0-119">alpha<sub>rt</sub> is the render-target alpha value.</span></span>
-   <span data-ttu-id="a85c0-120">destBlendOp è uno dei fattori di Blend in [**D3DBLEND**](./d3dblend.md).</span><span class="sxs-lookup"><span data-stu-id="a85c0-120">destBlendOp is one of the blend factors in [**D3DBLEND**](./d3dblend.md).</span></span>
-   <span data-ttu-id="a85c0-121">renderTargetAlpha è il valore alfa blend finale.</span><span class="sxs-lookup"><span data-stu-id="a85c0-121">renderTargetAlpha is the final blended alpha value.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a85c0-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a85c0-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a85c0-123">Fusione alfa</span><span class="sxs-lookup"><span data-stu-id="a85c0-123">Alpha Blending</span></span>](alpha-blending.md)
</dt> </dl>

 

 
