---
description: Gli Stati degli effetti sono coppie nome-valore sotto forma di espressione.
ms.assetid: 4612c6bd-bc1f-42ad-8465-c0d4b577d1db
title: Gruppi di stati effetti (Direct3D 10)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c132db3a5258cbe3573ddc5103df8b3cbcf2085d
ms.sourcegitcommit: 628fda3e63fd1d513ce9a5f55be8bbc4af4b2a4b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "104351741"
---
# <a name="effect-state-groups-direct3d-10"></a><span data-ttu-id="56c28-103">Gruppi di stati effetti (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="56c28-103">Effect state groups (Direct3D 10)</span></span>

<span data-ttu-id="56c28-104">Gli Stati degli effetti sono coppie nome-valore sotto forma di espressione.</span><span class="sxs-lookup"><span data-stu-id="56c28-104">Effect states are name-value pairs in the form of an expression.</span></span>

## <a name="blend-state"></a><span data-ttu-id="56c28-105">Stato di Blend</span><span class="sxs-lookup"><span data-stu-id="56c28-105">Blend state</span></span>

| | |
|-|-|
| <span data-ttu-id="56c28-106">**ALPHATOCOVERAGEENABLE**, **BLENDENABLE**, **SRCBLEND**, **DESTBLEND**, **BLENDOP**, **SRCBLENDALPHA**, **DESTBLENDALPHA**, **BLENDOPALPHA**, **RENDERTARGETWRITEMASK**</span><span class="sxs-lookup"><span data-stu-id="56c28-106">**ALPHATOCOVERAGEENABLE**, **BLENDENABLE**, **SRCBLEND**, **DESTBLEND**, **BLENDOP**, **SRCBLENDALPHA**, **DESTBLENDALPHA**, **BLENDOPALPHA**, **RENDERTARGETWRITEMASK**</span></span> | <span data-ttu-id="56c28-107">Membri di [ **D3D10 \_ Blend \_ desc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_blend_desc)</span><span class="sxs-lookup"><span data-stu-id="56c28-107">Members of [**D3D10\_BLEND\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_blend_desc)</span></span> |

## <a name="depth-and-stencil-state"></a><span data-ttu-id="56c28-108">Stato profondità e stencil</span><span class="sxs-lookup"><span data-stu-id="56c28-108">Depth and stencil state</span></span>

| | |
|-|-|
| <span data-ttu-id="56c28-109">**DEPTHENABLE**, **DEPTHWRITEMASK**, **DEPTHFUNC**, **STENCILENABLE**, **STENCILREADMASK**, **STENCILWRITEMASK**</span><span class="sxs-lookup"><span data-stu-id="56c28-109">**DEPTHENABLE**, **DEPTHWRITEMASK**, **DEPTHFUNC**, **STENCILENABLE**, **STENCILREADMASK**, **STENCILWRITEMASK**</span></span> | <span data-ttu-id="56c28-110">Membri di [ **D3D10 \_ Depth \_ stencil \_ desc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_desc)</span><span class="sxs-lookup"><span data-stu-id="56c28-110">Members of [**D3D10\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_desc)</span></span> |
| <span data-ttu-id="56c28-111">FRONTFACESTENCILFAIL \* \*, **FRONTFACESTENCILZFAIL**, **FRONTFACESTENCILPASS**, **FRONTFACESTENCILFUNC**, **BACKFACESTENCILFAIL**, **BACKFACESTENCILZFAIL**, **BACKFACESTENCILPASS, BACKFACESTENCILFUNC** </span><span class="sxs-lookup"><span data-stu-id="56c28-111">FRONTFACESTENCILFAIL\*\*, **FRONTFACESTENCILZFAIL**, **FRONTFACESTENCILPASS**, **FRONTFACESTENCILFUNC**, **BACKFACESTENCILFAIL**, **BACKFACESTENCILZFAIL**, **BACKFACESTENCILPASS**, **BACKFACESTENCILFUNC**</span></span> | <span data-ttu-id="56c28-112">Membro di [ **D3D10 \_ Depth \_ STENCILOP \_ desc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencilop_desc)</span><span class="sxs-lookup"><span data-stu-id="56c28-112">Member of [**D3D10\_DEPTH\_STENCILOP\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencilop_desc)</span></span> |

## <a name="rasterizer-state"></a><span data-ttu-id="56c28-113">Stato rasterizzazione</span><span class="sxs-lookup"><span data-stu-id="56c28-113">Rasterizer state</span></span>

| | |
|-|-|
| <span data-ttu-id="56c28-114">FILLMODE</span><span class="sxs-lookup"><span data-stu-id="56c28-114">FILLMODE</span></span> | [<span data-ttu-id="56c28-115">**\_Modalità di riempimento D3D10 \_**</span><span class="sxs-lookup"><span data-stu-id="56c28-115">**D3D10\_FILL\_MODE**</span></span>](/windows/desktop/api/D3D10/ne-d3d10-d3d10_fill_mode) |
| <span data-ttu-id="56c28-116">CULLMODE</span><span class="sxs-lookup"><span data-stu-id="56c28-116">CULLMODE</span></span> | [<span data-ttu-id="56c28-117">**\_Modalità di eliminazione D3D10 \_**</span><span class="sxs-lookup"><span data-stu-id="56c28-117">**D3D10\_CULL\_MODE**</span></span>](/windows/desktop/api/D3D10/ne-d3d10-d3d10_cull_mode) |
| <span data-ttu-id="56c28-118">**FRONTCOUNTERCLOCKWISE**, **DEPTHBIAS**, **DEPTHBIASCLAMP**, **SLOPESCALEDDEPTHBIAS**, **ZCLIPENABLE**, **SCISSORENABLE**, **MULTISAMPLEENABLE**, **ANTIALIASEDLINEENABLE**</span><span class="sxs-lookup"><span data-stu-id="56c28-118">**FRONTCOUNTERCLOCKWISE**, **DEPTHBIAS**, **DEPTHBIASCLAMP**, **SLOPESCALEDDEPTHBIAS**, **ZCLIPENABLE**, **SCISSORENABLE**, **MULTISAMPLEENABLE**, **ANTIALIASEDLINEENABLE**</span></span> | <span data-ttu-id="56c28-119">Membri di [ **D3D10 \_ rasterizzator \_ desc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_rasterizer_desc)</span><span class="sxs-lookup"><span data-stu-id="56c28-119">Members of [**D3D10\_RASTERIZER\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_rasterizer_desc)</span></span> |

## <a name="sampler-state"></a><span data-ttu-id="56c28-120">Stato campionatore</span><span class="sxs-lookup"><span data-stu-id="56c28-120">Sampler state</span></span>

| | |
|-|-|
| <span data-ttu-id="56c28-121">**Filter**, **AddressList**, **AddressV**, **AddressW**, **MipLODBias**, **MaxAnisotropy**, **ComparisonFunc**, **BorderColor**, **MinLOD**, **MaxLOD**</span><span class="sxs-lookup"><span data-stu-id="56c28-121">**Filter**, **AddressU**, **AddressV**, **AddressW**, **MipLODBias**, **MaxAnisotropy**, **ComparisonFunc**, **BorderColor**, **MinLOD**, **MaxLOD**</span></span> | <span data-ttu-id="56c28-122">Membri del [ **\_ campionatore D3D10 \_ desc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_sampler_desc)</span><span class="sxs-lookup"><span data-stu-id="56c28-122">Members of [**D3D10\_SAMPLER\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_sampler_desc)</span></span> |

<span data-ttu-id="56c28-123">Per esempi, vedere [Sampler Type (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-sampler.md) .</span><span class="sxs-lookup"><span data-stu-id="56c28-123">See [Sampler type (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-sampler.md) for examples.</span></span>

## <a name="effect-object-state"></a><span data-ttu-id="56c28-124">Stato dell'oggetto effetto</span><span class="sxs-lookup"><span data-stu-id="56c28-124">Effect object state</span></span>

| <span data-ttu-id="56c28-125">Questo oggetto effetto</span><span class="sxs-lookup"><span data-stu-id="56c28-125">This effect object</span></span> | <span data-ttu-id="56c28-126">Mapping a</span><span class="sxs-lookup"><span data-stu-id="56c28-126">Maps to</span></span> |
|-|-|
| <span data-ttu-id="56c28-127">RASTERIZERSTATE</span><span class="sxs-lookup"><span data-stu-id="56c28-127">RASTERIZERSTATE</span></span> | <span data-ttu-id="56c28-128">Oggetto stato di [rasterizzazione dello stato](#rasterizer-state) .</span><span class="sxs-lookup"><span data-stu-id="56c28-128">A [Rasterizer State](#rasterizer-state) state object.</span></span> |
| <span data-ttu-id="56c28-129">DEPTHSTENCILSTATE</span><span class="sxs-lookup"><span data-stu-id="56c28-129">DEPTHSTENCILSTATE</span></span> | <span data-ttu-id="56c28-130">Oggetto di stato di [profondità e stencil](#depth-and-stencil-state) .</span><span class="sxs-lookup"><span data-stu-id="56c28-130">A [Depth and Stencil State](#depth-and-stencil-state) state object.</span></span> |
| <span data-ttu-id="56c28-131">BLENDSTATE</span><span class="sxs-lookup"><span data-stu-id="56c28-131">BLENDSTATE</span></span> | <span data-ttu-id="56c28-132">Oggetto di stato di [Blend](#blend-state) .</span><span class="sxs-lookup"><span data-stu-id="56c28-132">A [Blend State](#blend-state) state object.</span></span> |
| <span data-ttu-id="56c28-133">VERTEXSHADER</span><span class="sxs-lookup"><span data-stu-id="56c28-133">VERTEXSHADER</span></span> | <span data-ttu-id="56c28-134">Oggetto vertex shader compilato.</span><span class="sxs-lookup"><span data-stu-id="56c28-134">A compiled vertex shader object.</span></span> |
| <span data-ttu-id="56c28-135">PIXELSHADER</span><span class="sxs-lookup"><span data-stu-id="56c28-135">PIXELSHADER</span></span> | <span data-ttu-id="56c28-136">Oggetto pixel shader compilato.</span><span class="sxs-lookup"><span data-stu-id="56c28-136">A compiled pixel shader object.</span></span> |
| <span data-ttu-id="56c28-137">GEOMETRYSHADER</span><span class="sxs-lookup"><span data-stu-id="56c28-137">GEOMETRYSHADER</span></span> | <span data-ttu-id="56c28-138">Oggetto Geometry shader compilato.</span><span class="sxs-lookup"><span data-stu-id="56c28-138">A compiled geometry shader object.</span></span> |
| <span data-ttu-id="56c28-139">DS \_ STENCILREF AB \_ BLENDFACTOR AB \_ SAMPLEMASK</span><span class="sxs-lookup"><span data-stu-id="56c28-139">DS\_STENCILREF AB\_BLENDFACTOR AB\_SAMPLEMASK</span></span> | <span data-ttu-id="56c28-140">Membri di [**D3D10 \_ pass \_ desc**](/windows/desktop/api/d3d10effect/ns-d3d10effect-d3d10_pass_desc).</span><span class="sxs-lookup"><span data-stu-id="56c28-140">Members of [**D3D10\_PASS\_DESC**](/windows/desktop/api/d3d10effect/ns-d3d10effect-d3d10_pass_desc).</span></span> |

## <a name="defining-and-using-state-objects"></a><span data-ttu-id="56c28-141">Definizione e utilizzo di oggetti stato</span><span class="sxs-lookup"><span data-stu-id="56c28-141">Defining and using state objects</span></span>

<span data-ttu-id="56c28-142">Gli oggetti di stato vengono dichiarati in file FX nel formato seguente.</span><span class="sxs-lookup"><span data-stu-id="56c28-142">State objects are declared in FX files in the following format.</span></span> <span data-ttu-id="56c28-143">*StateObjectType* è uno degli Stati elencati sopra e *memberName* è il nome di qualsiasi membro che avrà un valore non predefinito.</span><span class="sxs-lookup"><span data-stu-id="56c28-143">*StateObjectType* is one of the states listed above, and *MemberName* is the name of any member that will have a non-default value.</span></span>

```
StateObjectType ObjectName {
 MemberName = value;
 ...
 MemberName = value;
};
```

<span data-ttu-id="56c28-144">Per impostare, ad esempio, un oggetto di stato Blend con AlphaToCoverageEnable e BlendEnable \[ 0 \] impostato su **false**, viene utilizzato il codice seguente.</span><span class="sxs-lookup"><span data-stu-id="56c28-144">For example, to set up a blend state object with AlphaToCoverageEnable and BlendEnable\[0\] set to **FALSE**, the following code would be used.</span></span>

```
BlendState NoBlend {
 AlphaToCoverageEnable = FALSE;
 BlendEnable[0] = FALSE;
};
```

<span data-ttu-id="56c28-145">L'oggetto di stato viene applicato a un passaggio di tecnica usando una delle funzioni SetStateGroup descritte in [effetto della sintassi tecnica (Direct3D 10)](d3d10-effect-technique-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="56c28-145">The state object is applied to a technique pass using one of the SetStateGroup functions described in [Effect Technique Syntax (Direct3D 10)](d3d10-effect-technique-syntax.md).</span></span> <span data-ttu-id="56c28-146">Per applicare, ad esempio, l'oggetto BlendState descritto sopra, verrebbe utilizzato il codice seguente.</span><span class="sxs-lookup"><span data-stu-id="56c28-146">For example, to apply the BlendState object described above the following code would be used.</span></span>

```
SetBlendState( NoBlend, float4( 0.0f, 0.0f, 0.0f, 0.0f ), 0xFFFFFFFF );
```

<span data-ttu-id="56c28-147">Per un'esercitazione che descrive l'uso degli Stati, vedere la pagina relativa alla [gestione dello stato](https://msdn.microsoft.com/library/Ee416550(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="56c28-147">For a tutorial describing the use of states see [State management](https://msdn.microsoft.com/library/Ee416550(v=VS.85).aspx).</span></span>

## <a name="related-topics"></a><span data-ttu-id="56c28-148">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="56c28-148">Related topics</span></span>

* [<span data-ttu-id="56c28-149">Sintassi della tecnica degli effetti</span><span class="sxs-lookup"><span data-stu-id="56c28-149">Effect Technique Syntax</span></span>](d3d10-effect-technique-syntax.md)
* [<span data-ttu-id="56c28-150">Formato effetto (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="56c28-150">Effect Format (Direct3D 10)</span></span>](d3d10-effect-format.md)
