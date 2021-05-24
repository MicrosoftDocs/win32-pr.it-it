---
description: Gli stati degli effetti sono coppie nome-valore sotto forma di espressione.
ms.assetid: 4612c6bd-bc1f-42ad-8465-c0d4b577d1db
title: Gruppi di stati degli effetti (Direct3D 10)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4617f786b984c96b271600e05b3ea8da9b5701fd
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335570"
---
# <a name="effect-state-groups-direct3d-10"></a><span data-ttu-id="4961b-103">Gruppi di stati degli effetti (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="4961b-103">Effect state groups (Direct3D 10)</span></span>

<span data-ttu-id="4961b-104">Gli stati dell'effetto sono coppie nome-valore sotto forma di espressione.</span><span class="sxs-lookup"><span data-stu-id="4961b-104">Effect states are name-value pairs in the form of an expression.</span></span>

## <a name="blend-state"></a><span data-ttu-id="4961b-105">Stato di fusione</span><span class="sxs-lookup"><span data-stu-id="4961b-105">Blend state</span></span>

| <span data-ttu-id="4961b-106">Stato dell'effetto</span><span class="sxs-lookup"><span data-stu-id="4961b-106">Effect state</span></span> | <span data-ttu-id="4961b-107">Gruppo</span><span class="sxs-lookup"><span data-stu-id="4961b-107">Group</span></span> |
|-|-|
| <span data-ttu-id="4961b-108">**ALPHATOCOVERAGEENABLE,** **BLENDENABLE,** **SRCBLEND,** **DESTBLEND,** **BLENDOP,** **SRCBLENDALPHA,** **DESTBLENDALPHA,** **BLENDOPALPHA,** **RENDERTARGETWRITEMASK**</span><span class="sxs-lookup"><span data-stu-id="4961b-108">**ALPHATOCOVERAGEENABLE**, **BLENDENABLE**, **SRCBLEND**, **DESTBLEND**, **BLENDOP**, **SRCBLENDALPHA**, **DESTBLENDALPHA**, **BLENDOPALPHA**, **RENDERTARGETWRITEMASK**</span></span> | <span data-ttu-id="4961b-109">Membri di [ **D3D10 \_ BLEND \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_blend_desc)</span><span class="sxs-lookup"><span data-stu-id="4961b-109">Members of [**D3D10\_BLEND\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_blend_desc)</span></span> |

## <a name="depth-and-stencil-state"></a><span data-ttu-id="4961b-110">Stato di profondità e stencil</span><span class="sxs-lookup"><span data-stu-id="4961b-110">Depth and stencil state</span></span>

| <span data-ttu-id="4961b-111">Stato dell'effetto</span><span class="sxs-lookup"><span data-stu-id="4961b-111">Effect state</span></span>| <span data-ttu-id="4961b-112">Gruppo</span><span class="sxs-lookup"><span data-stu-id="4961b-112">Group</span></span> |
|-|-|
| <span data-ttu-id="4961b-113">**DEPTHENABLE,** **DEPTHWRITEMASK,** **DEPTHFUNC,** **STENCILENABLE,** **STENCILREADMASK,** **STENCILWRITEMASK**</span><span class="sxs-lookup"><span data-stu-id="4961b-113">**DEPTHENABLE**, **DEPTHWRITEMASK**, **DEPTHFUNC**, **STENCILENABLE**, **STENCILREADMASK**, **STENCILWRITEMASK**</span></span> | <span data-ttu-id="4961b-114">Membri di [ **D3D10 \_ DEPTH \_ STENCIL \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_desc)</span><span class="sxs-lookup"><span data-stu-id="4961b-114">Members of [**D3D10\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_desc)</span></span> |
| <span data-ttu-id="4961b-115">**FRONTFACESTENCILFAIL,** **FRONTFACESTENCILZFAIL,** **FRONTFACESTENCILPASS,** **FRONTFACESTENCILFUNC,** **BACKFACESTENCILFAIL,** **BACKFACESTENCILZFAIL,** **BACKFACESTENCILPASS,** **BACKFACESTENCILFUNC**</span><span class="sxs-lookup"><span data-stu-id="4961b-115">**FRONTFACESTENCILFAIL**, **FRONTFACESTENCILZFAIL**, **FRONTFACESTENCILPASS**, **FRONTFACESTENCILFUNC**, **BACKFACESTENCILFAIL**, **BACKFACESTENCILZFAIL**, **BACKFACESTENCILPASS**, **BACKFACESTENCILFUNC**</span></span> | <span data-ttu-id="4961b-116">Membro di [ **D3D10 \_ DEPTH \_ STENCILOP \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencilop_desc)</span><span class="sxs-lookup"><span data-stu-id="4961b-116">Member of [**D3D10\_DEPTH\_STENCILOP\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencilop_desc)</span></span> |

## <a name="rasterizer-state"></a><span data-ttu-id="4961b-117">Stato del rasterizzatore</span><span class="sxs-lookup"><span data-stu-id="4961b-117">Rasterizer state</span></span>

| <span data-ttu-id="4961b-118">Stato dell'effetto</span><span class="sxs-lookup"><span data-stu-id="4961b-118">Effect state</span></span>| <span data-ttu-id="4961b-119">Gruppo</span><span class="sxs-lookup"><span data-stu-id="4961b-119">Group</span></span> |
|-|-|
| <span data-ttu-id="4961b-120">Fillmode</span><span class="sxs-lookup"><span data-stu-id="4961b-120">FILLMODE</span></span> | [<span data-ttu-id="4961b-121">**MODALITÀ DI RIEMPIMENTO D3D10 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4961b-121">**D3D10\_FILL\_MODE**</span></span>](/windows/desktop/api/D3D10/ne-d3d10-d3d10_fill_mode) |
| <span data-ttu-id="4961b-122">CULLMODE</span><span class="sxs-lookup"><span data-stu-id="4961b-122">CULLMODE</span></span> | [<span data-ttu-id="4961b-123">**MODALITÀ CULL D3D10 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4961b-123">**D3D10\_CULL\_MODE**</span></span>](/windows/desktop/api/D3D10/ne-d3d10-d3d10_cull_mode) |
| <span data-ttu-id="4961b-124">**FRONTCOUNTERCLOCKWISE,** **DEPTHBIAS,** **DEPTHBIASCLAMP,** **SLOPESCALEDDEPTHBIAS,** **ZCLIPENABLE,** **SCISSORENABLE,** **MULTISAMPLEENABLE,** **ANTIALIASEDLINEENABLE**</span><span class="sxs-lookup"><span data-stu-id="4961b-124">**FRONTCOUNTERCLOCKWISE**, **DEPTHBIAS**, **DEPTHBIASCLAMP**, **SLOPESCALEDDEPTHBIAS**, **ZCLIPENABLE**, **SCISSORENABLE**, **MULTISAMPLEENABLE**, **ANTIALIASEDLINEENABLE**</span></span> | <span data-ttu-id="4961b-125">Membri di [ **D3D10 \_ RASTERIZER \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_rasterizer_desc)</span><span class="sxs-lookup"><span data-stu-id="4961b-125">Members of [**D3D10\_RASTERIZER\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_rasterizer_desc)</span></span> |

## <a name="sampler-state"></a><span data-ttu-id="4961b-126">Stato del campionatore</span><span class="sxs-lookup"><span data-stu-id="4961b-126">Sampler state</span></span>

| <span data-ttu-id="4961b-127">Stato dell'effetto</span><span class="sxs-lookup"><span data-stu-id="4961b-127">Effect state</span></span> | <span data-ttu-id="4961b-128">Gruppo</span><span class="sxs-lookup"><span data-stu-id="4961b-128">Group</span></span> |
|-|-|
| <span data-ttu-id="4961b-129">**Filter**, **AddressU**, **AddressV**, **AddressW**, **MipLODBias**, **MaxAnisotropy**, **ComparisonFunc**, **BorderColor**, **MinLOD**, **MaxLOD**</span><span class="sxs-lookup"><span data-stu-id="4961b-129">**Filter**, **AddressU**, **AddressV**, **AddressW**, **MipLODBias**, **MaxAnisotropy**, **ComparisonFunc**, **BorderColor**, **MinLOD**, **MaxLOD**</span></span> | <span data-ttu-id="4961b-130">Membri di [ **D3D10 \_ SAMPLER \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_sampler_desc)</span><span class="sxs-lookup"><span data-stu-id="4961b-130">Members of [**D3D10\_SAMPLER\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_sampler_desc)</span></span> |

<span data-ttu-id="4961b-131">Per [esempi, vedere Sampler type (DirectX HLSL) (Tipo](../direct3dhlsl/dx-graphics-hlsl-sampler.md) di campionatore ( DirectX HLSL).</span><span class="sxs-lookup"><span data-stu-id="4961b-131">See [Sampler type (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-sampler.md) for examples.</span></span>

## <a name="effect-object-state"></a><span data-ttu-id="4961b-132">Stato dell'oggetto Effect</span><span class="sxs-lookup"><span data-stu-id="4961b-132">Effect object state</span></span>

| <span data-ttu-id="4961b-133">Questo oggetto effetto</span><span class="sxs-lookup"><span data-stu-id="4961b-133">This effect object</span></span> | <span data-ttu-id="4961b-134">Mapping a</span><span class="sxs-lookup"><span data-stu-id="4961b-134">Maps to</span></span> |
|-|-|
| <span data-ttu-id="4961b-135">RASTERIZERSTATE</span><span class="sxs-lookup"><span data-stu-id="4961b-135">RASTERIZERSTATE</span></span> | <span data-ttu-id="4961b-136">Oggetto [stato rasterizzatore.](#rasterizer-state)</span><span class="sxs-lookup"><span data-stu-id="4961b-136">A [Rasterizer State](#rasterizer-state) state object.</span></span> |
| <span data-ttu-id="4961b-137">DEPTHSTENCILSTATE</span><span class="sxs-lookup"><span data-stu-id="4961b-137">DEPTHSTENCILSTATE</span></span> | <span data-ttu-id="4961b-138">Oggetto [di stato Depth e Stencil State.](#depth-and-stencil-state)</span><span class="sxs-lookup"><span data-stu-id="4961b-138">A [Depth and Stencil State](#depth-and-stencil-state) state object.</span></span> |
| <span data-ttu-id="4961b-139">BLENDSTATE</span><span class="sxs-lookup"><span data-stu-id="4961b-139">BLENDSTATE</span></span> | <span data-ttu-id="4961b-140">Oggetto [stato blend.](#blend-state)</span><span class="sxs-lookup"><span data-stu-id="4961b-140">A [Blend State](#blend-state) state object.</span></span> |
| <span data-ttu-id="4961b-141">VERTEXSHADER</span><span class="sxs-lookup"><span data-stu-id="4961b-141">VERTEXSHADER</span></span> | <span data-ttu-id="4961b-142">Oggetto vertex shader compilato.</span><span class="sxs-lookup"><span data-stu-id="4961b-142">A compiled vertex shader object.</span></span> |
| <span data-ttu-id="4961b-143">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="4961b-143">PIXELSHADER</span></span> | <span data-ttu-id="4961b-144">Oggetto pixel shader compilato.</span><span class="sxs-lookup"><span data-stu-id="4961b-144">A compiled pixel shader object.</span></span> |
| <span data-ttu-id="4961b-145">GEOMETRYSHADER</span><span class="sxs-lookup"><span data-stu-id="4961b-145">GEOMETRYSHADER</span></span> | <span data-ttu-id="4961b-146">Oggetto geometry shader compilato.</span><span class="sxs-lookup"><span data-stu-id="4961b-146">A compiled geometry shader object.</span></span> |
| <span data-ttu-id="4961b-147">DS \_ STENCILREF AB \_ BLENDFACTOR AB \_ SAMPLEMASK</span><span class="sxs-lookup"><span data-stu-id="4961b-147">DS\_STENCILREF AB\_BLENDFACTOR AB\_SAMPLEMASK</span></span> | <span data-ttu-id="4961b-148">Membri di [**D3D10 \_ PASS \_ DESC**](/windows/desktop/api/d3d10effect/ns-d3d10effect-d3d10_pass_desc).</span><span class="sxs-lookup"><span data-stu-id="4961b-148">Members of [**D3D10\_PASS\_DESC**](/windows/desktop/api/d3d10effect/ns-d3d10effect-d3d10_pass_desc).</span></span> |

## <a name="defining-and-using-state-objects"></a><span data-ttu-id="4961b-149">Definizione e uso di oggetti di stato</span><span class="sxs-lookup"><span data-stu-id="4961b-149">Defining and using state objects</span></span>

<span data-ttu-id="4961b-150">Gli oggetti di stato vengono dichiarati nei file FX nel formato seguente.</span><span class="sxs-lookup"><span data-stu-id="4961b-150">State objects are declared in FX files in the following format.</span></span> <span data-ttu-id="4961b-151">*StateObjectType* è uno degli stati elencati in precedenza e *MemberName* è il nome di qualsiasi membro che avrà un valore non predefinito.</span><span class="sxs-lookup"><span data-stu-id="4961b-151">*StateObjectType* is one of the states listed above, and *MemberName* is the name of any member that will have a non-default value.</span></span>

```
StateObjectType ObjectName {
 MemberName = value;
 ...
 MemberName = value;
};
```

<span data-ttu-id="4961b-152">Ad esempio, per impostare un oggetto stato di blend con AlphaToCoverageEnable e BlendEnable 0 impostato su FALSE, verrà usato \[ \] il codice seguente. </span><span class="sxs-lookup"><span data-stu-id="4961b-152">For example, to set up a blend state object with AlphaToCoverageEnable and BlendEnable\[0\] set to **FALSE**, the following code would be used.</span></span>

```
BlendState NoBlend {
 AlphaToCoverageEnable = FALSE;
 BlendEnable[0] = FALSE;
};
```

<span data-ttu-id="4961b-153">L'oggetto stato viene applicato a un passaggio di tecnica usando una delle funzioni SetStateGroup descritte in Sintassi della tecnica degli effetti [(Direct3D 10).](d3d10-effect-technique-syntax.md)</span><span class="sxs-lookup"><span data-stu-id="4961b-153">The state object is applied to a technique pass using one of the SetStateGroup functions described in [Effect Technique Syntax (Direct3D 10)](d3d10-effect-technique-syntax.md).</span></span> <span data-ttu-id="4961b-154">Ad esempio, per applicare l'oggetto BlendState descritto sopra, verrà usato il codice seguente.</span><span class="sxs-lookup"><span data-stu-id="4961b-154">For example, to apply the BlendState object described above the following code would be used.</span></span>

```
SetBlendState( NoBlend, float4( 0.0f, 0.0f, 0.0f, 0.0f ), 0xFFFFFFFF );
```

<span data-ttu-id="4961b-155">Per un'esercitazione che descrive l'uso degli stati, vedere [Gestione dello stato](https://msdn.microsoft.com/library/Ee416550(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="4961b-155">For a tutorial describing the use of states see [State management](https://msdn.microsoft.com/library/Ee416550(v=VS.85).aspx).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4961b-156">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4961b-156">Related topics</span></span>

* [<span data-ttu-id="4961b-157">Sintassi della tecnica degli effetti</span><span class="sxs-lookup"><span data-stu-id="4961b-157">Effect Technique Syntax</span></span>](d3d10-effect-technique-syntax.md)
* [<span data-ttu-id="4961b-158">Formato effetto (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="4961b-158">Effect Format (Direct3D 10)</span></span>](d3d10-effect-format.md)
