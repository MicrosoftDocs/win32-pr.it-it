---
title: Gruppi di stati effetti (Direct3D 11)
description: Gli Stati degli effetti sono coppie nome-valore sotto forma di espressione.
ms.assetid: 87883483-4fa6-4362-807e-53b79b7d1370
keywords:
- effetti, gruppi di stato (Direct3D 11)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58def71b6362706eb831129b1d222ef3d1cc9341
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963110"
---
# <a name="effect-state-groups-direct3d-11"></a><span data-ttu-id="afb91-104">Gruppi di stati effetti (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="afb91-104">Effect State Groups (Direct3D 11)</span></span>

<span data-ttu-id="afb91-105">Gli Stati degli effetti sono coppie nome-valore sotto forma di espressione.</span><span class="sxs-lookup"><span data-stu-id="afb91-105">Effect states are name value pairs in the form of an expression.</span></span>

-   [<span data-ttu-id="afb91-106">Stato di Blend</span><span class="sxs-lookup"><span data-stu-id="afb91-106">Blend State</span></span>](#blend-state)
-   [<span data-ttu-id="afb91-107">Stato profondità e stencil</span><span class="sxs-lookup"><span data-stu-id="afb91-107">Depth and Stencil State</span></span>](#depth-and-stencil-state)
-   [<span data-ttu-id="afb91-108">Stato rasterizzazione</span><span class="sxs-lookup"><span data-stu-id="afb91-108">Rasterizer State</span></span>](#rasterizer-state)
-   [<span data-ttu-id="afb91-109">Stato campionatore</span><span class="sxs-lookup"><span data-stu-id="afb91-109">Sampler State</span></span>](#sampler-state)
-   [<span data-ttu-id="afb91-110">Stato dell'oggetto effetto</span><span class="sxs-lookup"><span data-stu-id="afb91-110">Effect Object State</span></span>](#effect-object-state)
-   [<span data-ttu-id="afb91-111">Definizione e utilizzo di oggetti stato</span><span class="sxs-lookup"><span data-stu-id="afb91-111">Defining and using state objects</span></span>](#defining-and-using-state-objects)
-   [<span data-ttu-id="afb91-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="afb91-112">Related topics</span></span>](#related-topics)

## <a name="blend-state"></a><span data-ttu-id="afb91-113">Stato di Blend</span><span class="sxs-lookup"><span data-stu-id="afb91-113">Blend State</span></span>



|                                                                                                                       |                                                           |
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <span data-ttu-id="afb91-114">ALPHATOCOVERAGEENABLEBLENDENABLESRCBLENDDESTBLENDBLENDOP SRCBLENDALPHADESTBLENDALPHABLENDOPALPHARENDERTARGETWRITEMASK</span><span class="sxs-lookup"><span data-stu-id="afb91-114">ALPHATOCOVERAGEENABLEBLENDENABLESRCBLENDDESTBLENDBLENDOP SRCBLENDALPHADESTBLENDALPHABLENDOPALPHARENDERTARGETWRITEMASK</span></span> | <span data-ttu-id="afb91-115">Membri di [ **d3d11 \_ Blend \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc)</span><span class="sxs-lookup"><span data-stu-id="afb91-115">Members of [**D3D11\_BLEND\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc)</span></span> |



 

## <a name="depth-and-stencil-state"></a><span data-ttu-id="afb91-116">Stato profondità e stencil</span><span class="sxs-lookup"><span data-stu-id="afb91-116">Depth and Stencil State</span></span>



|                                                                                                                                                                |                                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="afb91-117">DEPTHENABLEDEPTHWRITEMASKDEPTHFUNCSTENCILENABLESTENCILREADMASKSTENCILWRITEMASK</span><span class="sxs-lookup"><span data-stu-id="afb91-117">DEPTHENABLEDEPTHWRITEMASKDEPTHFUNCSTENCILENABLESTENCILREADMASKSTENCILWRITEMASK</span></span>                                                                                 | <span data-ttu-id="afb91-118">Membri di [ **d3d11 \_ Depth \_ stencil \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc)</span><span class="sxs-lookup"><span data-stu-id="afb91-118">Members of [**D3D11\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc)</span></span>    |
| <span data-ttu-id="afb91-119">FRONTFACESTENCILFAILFRONTFACESTENCILZFAILFRONTFACESTENCILPASSFRONTFACESTENCILFUNCBACKFACESTENCILFAILBACKFACESTENCILZFAILBACKFACESTENCILPASSBACKFACESTENCILFUNC</span><span class="sxs-lookup"><span data-stu-id="afb91-119">FRONTFACESTENCILFAILFRONTFACESTENCILZFAILFRONTFACESTENCILPASSFRONTFACESTENCILFUNCBACKFACESTENCILFAILBACKFACESTENCILZFAILBACKFACESTENCILPASSBACKFACESTENCILFUNC</span></span> | <span data-ttu-id="afb91-120">Membro di [ **d3d11 \_ Depth \_ STENCILOP \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencilop_desc)</span><span class="sxs-lookup"><span data-stu-id="afb91-120">Member of [**D3D11\_DEPTH\_STENCILOP\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencilop_desc)</span></span> |



 

## <a name="rasterizer-state"></a><span data-ttu-id="afb91-121">Stato rasterizzazione</span><span class="sxs-lookup"><span data-stu-id="afb91-121">Rasterizer State</span></span>



|                                                                                                                                 |                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="afb91-122">FILLMODE</span><span class="sxs-lookup"><span data-stu-id="afb91-122">FILLMODE</span></span>                                                                                                                        | [<span data-ttu-id="afb91-123">**\_Modalità di riempimento d3d11 \_**</span><span class="sxs-lookup"><span data-stu-id="afb91-123">**D3D11\_FILL\_MODE**</span></span>](/windows/desktop/api/D3D11/ne-d3d11-d3d11_fill_mode)                        |
| <span data-ttu-id="afb91-124">CULLMODE</span><span class="sxs-lookup"><span data-stu-id="afb91-124">CULLMODE</span></span>                                                                                                                        | [<span data-ttu-id="afb91-125">**\_Modalità di eliminazione d3d11 \_**</span><span class="sxs-lookup"><span data-stu-id="afb91-125">**D3D11\_CULL\_MODE**</span></span>](/windows/desktop/api/D3D11/ne-d3d11-d3d11_cull_mode)                        |
| <span data-ttu-id="afb91-126">FRONTCOUNTERCLOCKWISEDEPTHBIASDEPTHBIASCLAMPSLOPESCALEDDEPTHBIAS ZCLIPENABLESCISSORENABLEMULTISAMPLEENABLEANTIALIASEDLINEENABLE</span><span class="sxs-lookup"><span data-stu-id="afb91-126">FRONTCOUNTERCLOCKWISEDEPTHBIASDEPTHBIASCLAMPSLOPESCALEDDEPTHBIAS ZCLIPENABLESCISSORENABLEMULTISAMPLEENABLEANTIALIASEDLINEENABLE</span></span> | <span data-ttu-id="afb91-127">Membri di [ **d3d11 \_ rasterizzator \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_rasterizer_desc)</span><span class="sxs-lookup"><span data-stu-id="afb91-127">Members of [**D3D11\_RASTERIZER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_rasterizer_desc)</span></span> |



 

## <a name="sampler-state"></a><span data-ttu-id="afb91-128">Stato campionatore</span><span class="sxs-lookup"><span data-stu-id="afb91-128">Sampler State</span></span>



|                                                                                                     |                                                               |
|-----------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="afb91-129">Filter Address AddressV AddressW MipLODBias MaxAnisotropy ComparisonFunc BorderColor MinLOD MaxLOD</span><span class="sxs-lookup"><span data-stu-id="afb91-129">Filter AddressU AddressV AddressW MipLODBias MaxAnisotropy ComparisonFunc BorderColor MinLOD MaxLOD</span></span> | <span data-ttu-id="afb91-130">Membri del [ **\_ campionatore d3d11 \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_sampler_desc)</span><span class="sxs-lookup"><span data-stu-id="afb91-130">Members of [**D3D11\_SAMPLER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_sampler_desc)</span></span> |



 

<span data-ttu-id="afb91-131">Per esempi, vedere [Sampler Type (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-sampler) .</span><span class="sxs-lookup"><span data-stu-id="afb91-131">See [Sampler Type (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-sampler) for examples.</span></span>

## <a name="effect-object-state"></a><span data-ttu-id="afb91-132">Stato dell'oggetto effetto</span><span class="sxs-lookup"><span data-stu-id="afb91-132">Effect Object State</span></span>



| <span data-ttu-id="afb91-133">Questo oggetto effetto</span><span class="sxs-lookup"><span data-stu-id="afb91-133">This Effect Object</span></span>                          | <span data-ttu-id="afb91-134">Mapping a</span><span class="sxs-lookup"><span data-stu-id="afb91-134">Maps to</span></span>                                                             |
|---------------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="afb91-135">RASTERIZERSTATE</span><span class="sxs-lookup"><span data-stu-id="afb91-135">RASTERIZERSTATE</span></span>                             | <span data-ttu-id="afb91-136">Oggetto stato di [rasterizzazione dello stato](#rasterizer-state) .</span><span class="sxs-lookup"><span data-stu-id="afb91-136">A [Rasterizer State](#rasterizer-state) state object.</span></span>               |
| <span data-ttu-id="afb91-137">DEPTHSTENCILSTATE</span><span class="sxs-lookup"><span data-stu-id="afb91-137">DEPTHSTENCILSTATE</span></span>                           | <span data-ttu-id="afb91-138">Oggetto di stato di [profondità e stencil](#depth-and-stencil-state) .</span><span class="sxs-lookup"><span data-stu-id="afb91-138">A [Depth and Stencil State](#depth-and-stencil-state) state object.</span></span> |
| <span data-ttu-id="afb91-139">BLENDSTATE</span><span class="sxs-lookup"><span data-stu-id="afb91-139">BLENDSTATE</span></span>                                  | <span data-ttu-id="afb91-140">Oggetto di stato di [Blend](#blend-state) .</span><span class="sxs-lookup"><span data-stu-id="afb91-140">A [Blend State](#blend-state) state object.</span></span>                         |
| <span data-ttu-id="afb91-141">VERTEXSHADER</span><span class="sxs-lookup"><span data-stu-id="afb91-141">VERTEXSHADER</span></span>                                | <span data-ttu-id="afb91-142">Oggetto vertex shader compilato.</span><span class="sxs-lookup"><span data-stu-id="afb91-142">A compiled vertex shader object.</span></span>                                    |
| <span data-ttu-id="afb91-143">PIXELSHADER</span><span class="sxs-lookup"><span data-stu-id="afb91-143">PIXELSHADER</span></span>                                 | <span data-ttu-id="afb91-144">Oggetto pixel shader compilato.</span><span class="sxs-lookup"><span data-stu-id="afb91-144">A compiled pixel shader object.</span></span>                                     |
| <span data-ttu-id="afb91-145">GEOMETRYSHADER</span><span class="sxs-lookup"><span data-stu-id="afb91-145">GEOMETRYSHADER</span></span>                              | <span data-ttu-id="afb91-146">Oggetto Geometry shader compilato.</span><span class="sxs-lookup"><span data-stu-id="afb91-146">A compiled geometry shader object.</span></span>                                  |
| <span data-ttu-id="afb91-147">DS \_ STENCILREFAB \_ BLENDFACTORAB \_ SAMPLEMASK</span><span class="sxs-lookup"><span data-stu-id="afb91-147">DS\_STENCILREFAB\_BLENDFACTORAB\_SAMPLEMASK</span></span> | <span data-ttu-id="afb91-148">Membri di [**D3DX11 \_ pass \_ desc**](d3dx11-pass-desc.md).</span><span class="sxs-lookup"><span data-stu-id="afb91-148">Members of [**D3DX11\_PASS\_DESC**](d3dx11-pass-desc.md).</span></span>          |



 

## <a name="defining-and-using-state-objects"></a><span data-ttu-id="afb91-149">Definizione e utilizzo di oggetti stato</span><span class="sxs-lookup"><span data-stu-id="afb91-149">Defining and using state objects</span></span>

<span data-ttu-id="afb91-150">Gli oggetti di stato vengono dichiarati in file FX nel formato seguente.</span><span class="sxs-lookup"><span data-stu-id="afb91-150">State objects are declared in FX files in the following format.</span></span> <span data-ttu-id="afb91-151">StateObjectType è uno degli Stati elencati sopra e MemberName è il nome di qualsiasi membro che avrà un valore non predefinito.</span><span class="sxs-lookup"><span data-stu-id="afb91-151">StateObjectType is one of the states listed above and MemberName is the name of any member that will have a non-default value.</span></span>


```
StateObjectType ObjectName {
  MemberName = value;
  ...
  MemberName = value;
};
    
```



<span data-ttu-id="afb91-152">Per impostare, ad esempio, un oggetto di stato Blend con AlphaToCoverageEnable e BlendEnable \[ 0 \] impostato su **false** , viene utilizzato il codice seguente.</span><span class="sxs-lookup"><span data-stu-id="afb91-152">For example, to set up a blend state object with AlphaToCoverageEnable and BlendEnable\[0\] set to **FALSE** the following code would be used.</span></span>


```
BlendState NoBlend {
  AlphaToCoverageEnable = FALSE;
  BlendEnable[0] = FALSE;
};
    
```



<span data-ttu-id="afb91-153">L'oggetto di stato viene applicato a un passaggio di tecnica usando una delle funzioni SetStateGroup descritte in [Effect Technique Syntax (Direct3D 11)](d3d11-effect-technique-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="afb91-153">The state object is applied to a technique pass using one of the SetStateGroup functions described in [Effect Technique Syntax (Direct3D 11)](d3d11-effect-technique-syntax.md).</span></span> <span data-ttu-id="afb91-154">Per applicare, ad esempio, l'oggetto BlendState descritto sopra, verrebbe utilizzato il codice seguente.</span><span class="sxs-lookup"><span data-stu-id="afb91-154">For example, to apply the BlendState object described above the following code would be used.</span></span>


```
SetBlendState( NoBlend, float4( 0.0f, 0.0f, 0.0f, 0.0f ), 0xFFFFFFFF );
    
```



## <a name="related-topics"></a><span data-ttu-id="afb91-155">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="afb91-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="afb91-156">Sintassi della tecnica degli effetti</span><span class="sxs-lookup"><span data-stu-id="afb91-156">Effect Technique Syntax</span></span>](d3d11-effect-technique-syntax.md)
</dt> <dt>

[<span data-ttu-id="afb91-157">Formato effetto (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="afb91-157">Effect Format (Direct3D 11)</span></span>](d3d11-effect-format.md)
</dt> </dl>

 

 