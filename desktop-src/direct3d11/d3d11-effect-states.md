---
title: Gruppi di stati degli effetti (Direct3D 11)
description: Gli stati dell'effetto sono coppie nome-valore sotto forma di espressione.
ms.assetid: 87883483-4fa6-4362-807e-53b79b7d1370
keywords:
- effect, state groups (Direct3D 11)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5a757926d8c4c259adc94f505a778cf73233b5a
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335335"
---
# <a name="effect-state-groups-direct3d-11"></a><span data-ttu-id="9bdae-104">Gruppi di stati degli effetti (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="9bdae-104">Effect State Groups (Direct3D 11)</span></span>

<span data-ttu-id="9bdae-105">Gli stati dell'effetto sono coppie nome-valore sotto forma di espressione.</span><span class="sxs-lookup"><span data-stu-id="9bdae-105">Effect states are name value pairs in the form of an expression.</span></span>

-   [<span data-ttu-id="9bdae-106">Stato di blend</span><span class="sxs-lookup"><span data-stu-id="9bdae-106">Blend State</span></span>](#blend-state)
-   [<span data-ttu-id="9bdae-107">Profondità e stato dello stencil</span><span class="sxs-lookup"><span data-stu-id="9bdae-107">Depth and Stencil State</span></span>](#depth-and-stencil-state)
-   [<span data-ttu-id="9bdae-108">Stato rasterizzazione</span><span class="sxs-lookup"><span data-stu-id="9bdae-108">Rasterizer State</span></span>](#rasterizer-state)
-   [<span data-ttu-id="9bdae-109">Stato del campionatore</span><span class="sxs-lookup"><span data-stu-id="9bdae-109">Sampler State</span></span>](#sampler-state)
-   [<span data-ttu-id="9bdae-110">Stato dell'oggetto effect</span><span class="sxs-lookup"><span data-stu-id="9bdae-110">Effect Object State</span></span>](#effect-object-state)
-   [<span data-ttu-id="9bdae-111">Definizione e uso di oggetti di stato</span><span class="sxs-lookup"><span data-stu-id="9bdae-111">Defining and using state objects</span></span>](#defining-and-using-state-objects)
-   [<span data-ttu-id="9bdae-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9bdae-112">Related topics</span></span>](#related-topics)

## <a name="blend-state"></a><span data-ttu-id="9bdae-113">Stato di blend</span><span class="sxs-lookup"><span data-stu-id="9bdae-113">Blend State</span></span>



| <span data-ttu-id="9bdae-114">Stato dell'effetto</span><span class="sxs-lookup"><span data-stu-id="9bdae-114">Effect state</span></span>                                                                                                                      | <span data-ttu-id="9bdae-115">Gruppo</span><span class="sxs-lookup"><span data-stu-id="9bdae-115">Group</span></span>                                                          |
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <span data-ttu-id="9bdae-116">ALPHATOCOVERAGEENABLEBLENDENABLESRCBLENDDESTBLENDBLENDOP SRCBLENDALPHADESTBLENDALPHABLENDOPALPHARENDERTARGETWRITEMASK</span><span class="sxs-lookup"><span data-stu-id="9bdae-116">ALPHATOCOVERAGEENABLEBLENDENABLESRCBLENDDESTBLENDBLENDOP SRCBLENDALPHADESTBLENDALPHABLENDOPALPHARENDERTARGETWRITEMASK</span></span> | <span data-ttu-id="9bdae-117">Membri di [ **D3D11 \_ BLEND \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc)</span><span class="sxs-lookup"><span data-stu-id="9bdae-117">Members of [**D3D11\_BLEND\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc)</span></span> |



 

## <a name="depth-and-stencil-state"></a><span data-ttu-id="9bdae-118">Profondità e stato dello stencil</span><span class="sxs-lookup"><span data-stu-id="9bdae-118">Depth and Stencil State</span></span>



|  <span data-ttu-id="9bdae-119">Stato dell'effetto</span><span class="sxs-lookup"><span data-stu-id="9bdae-119">Effect state</span></span>                                                                                                                                                              | <span data-ttu-id="9bdae-120">Gruppo</span><span class="sxs-lookup"><span data-stu-id="9bdae-120">Group</span></span>                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="9bdae-121">DEPTHENABLEDEPTHWRITEMASKDEPTHFUNCSTENCILENABLESTENCILREADMASKSTENCILWRITEMASK</span><span class="sxs-lookup"><span data-stu-id="9bdae-121">DEPTHENABLEDEPTHWRITEMASKDEPTHFUNCSTENCILENABLESTENCILREADMASKSTENCILWRITEMASK</span></span>                                                                                 | <span data-ttu-id="9bdae-122">Membri di [ **D3D11 \_ DEPTH \_ STENCIL \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc)</span><span class="sxs-lookup"><span data-stu-id="9bdae-122">Members of [**D3D11\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc)</span></span>    |
| <span data-ttu-id="9bdae-123">FRONTFACESTENCILFAILFRONTFACESTENCILZFAILFRONTFACESTENCILPASSFRONTFACESTENCILFUNCBACKFACESTENCILFAILBACKFACESTENCILZFAILBACKFACESTENCILPASSBACKFACESTENCILFUNC</span><span class="sxs-lookup"><span data-stu-id="9bdae-123">FRONTFACESTENCILFAILFRONTFACESTENCILZFAILFRONTFACESTENCILPASSFRONTFACESTENCILFUNCBACKFACESTENCILFAILBACKFACESTENCILZFAILBACKFACESTENCILPASSBACKFACESTENCILFUNC</span></span> | <span data-ttu-id="9bdae-124">Membro di [ **D3D11 \_ DEPTH \_ STENCILOP \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencilop_desc)</span><span class="sxs-lookup"><span data-stu-id="9bdae-124">Member of [**D3D11\_DEPTH\_STENCILOP\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencilop_desc)</span></span> |



 

## <a name="rasterizer-state"></a><span data-ttu-id="9bdae-125">Stato rasterizzazione</span><span class="sxs-lookup"><span data-stu-id="9bdae-125">Rasterizer State</span></span>



| <span data-ttu-id="9bdae-126">Stato dell'effetto</span><span class="sxs-lookup"><span data-stu-id="9bdae-126">Effect state</span></span>                                                                                                                                | <span data-ttu-id="9bdae-127">Gruppo</span><span class="sxs-lookup"><span data-stu-id="9bdae-127">Group</span></span>                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="9bdae-128">Fillmode</span><span class="sxs-lookup"><span data-stu-id="9bdae-128">FILLMODE</span></span>                                                                                                                        | [<span data-ttu-id="9bdae-129">**MODALITÀ RIEMPIMENTO D3D11 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="9bdae-129">**D3D11\_FILL\_MODE**</span></span>](/windows/desktop/api/D3D11/ne-d3d11-d3d11_fill_mode)                        |
| <span data-ttu-id="9bdae-130">CULLMODE</span><span class="sxs-lookup"><span data-stu-id="9bdae-130">CULLMODE</span></span>                                                                                                                        | [<span data-ttu-id="9bdae-131">**MODALITÀ CULL D3D11 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="9bdae-131">**D3D11\_CULL\_MODE**</span></span>](/windows/desktop/api/D3D11/ne-d3d11-d3d11_cull_mode)                        |
| <span data-ttu-id="9bdae-132">FRONTCOUNTERCLOCKWISEDEPTHBIASDEPTHBIASCLAMPSLOPESCALEDDEPTHBIAS ZCLIPENABLESCISSORENABLEMULTISAMPLEENABLEANTIALIASEDLINEENABLE</span><span class="sxs-lookup"><span data-stu-id="9bdae-132">FRONTCOUNTERCLOCKWISEDEPTHBIASDEPTHBIASCLAMPSLOPESCALEDDEPTHBIAS ZCLIPENABLESCISSORENABLEMULTISAMPLEENABLEANTIALIASEDLINEENABLE</span></span> | <span data-ttu-id="9bdae-133">Membri di [ **D3D11 \_ RASTERIZER \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_rasterizer_desc)</span><span class="sxs-lookup"><span data-stu-id="9bdae-133">Members of [**D3D11\_RASTERIZER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_rasterizer_desc)</span></span> |



 

## <a name="sampler-state"></a><span data-ttu-id="9bdae-134">Stato del campionatore</span><span class="sxs-lookup"><span data-stu-id="9bdae-134">Sampler State</span></span>



| <span data-ttu-id="9bdae-135">Stato dell'effetto</span><span class="sxs-lookup"><span data-stu-id="9bdae-135">Effect state</span></span>                                                                                                    | <span data-ttu-id="9bdae-136">Gruppo</span><span class="sxs-lookup"><span data-stu-id="9bdae-136">Group</span></span>                                                              |
|-----------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="9bdae-137">Filtro AddressU AddressV AddressW MipLODBias MaxAnisotropy ComparisonFunc BorderColor MinLOD MaxLOD</span><span class="sxs-lookup"><span data-stu-id="9bdae-137">Filter AddressU AddressV AddressW MipLODBias MaxAnisotropy ComparisonFunc BorderColor MinLOD MaxLOD</span></span> | <span data-ttu-id="9bdae-138">Membri di [ **D3D11 \_ SAMPLER \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_sampler_desc)</span><span class="sxs-lookup"><span data-stu-id="9bdae-138">Members of [**D3D11\_SAMPLER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_sampler_desc)</span></span> |



 

<span data-ttu-id="9bdae-139">Per [esempi, vedere Sampler Type (DirectX HLSL) (Tipo](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-sampler) di campionatore - DirectX HLSL).</span><span class="sxs-lookup"><span data-stu-id="9bdae-139">See [Sampler Type (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-sampler) for examples.</span></span>

## <a name="effect-object-state"></a><span data-ttu-id="9bdae-140">Stato dell'oggetto Effect</span><span class="sxs-lookup"><span data-stu-id="9bdae-140">Effect Object State</span></span>



| <span data-ttu-id="9bdae-141">Questo oggetto Effect</span><span class="sxs-lookup"><span data-stu-id="9bdae-141">This Effect Object</span></span>                          | <span data-ttu-id="9bdae-142">Mapping a</span><span class="sxs-lookup"><span data-stu-id="9bdae-142">Maps to</span></span>                                                             |
|---------------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="9bdae-143">RASTERIZERSTATE</span><span class="sxs-lookup"><span data-stu-id="9bdae-143">RASTERIZERSTATE</span></span>                             | <span data-ttu-id="9bdae-144">Oggetto [stato rasterizzatore.](#rasterizer-state)</span><span class="sxs-lookup"><span data-stu-id="9bdae-144">A [Rasterizer State](#rasterizer-state) state object.</span></span>               |
| <span data-ttu-id="9bdae-145">DEPTHSTENCILSTATE</span><span class="sxs-lookup"><span data-stu-id="9bdae-145">DEPTHSTENCILSTATE</span></span>                           | <span data-ttu-id="9bdae-146">Oggetto [di stato Depth e Stencil State.](#depth-and-stencil-state)</span><span class="sxs-lookup"><span data-stu-id="9bdae-146">A [Depth and Stencil State](#depth-and-stencil-state) state object.</span></span> |
| <span data-ttu-id="9bdae-147">BLENDSTATE</span><span class="sxs-lookup"><span data-stu-id="9bdae-147">BLENDSTATE</span></span>                                  | <span data-ttu-id="9bdae-148">Oggetto [stato blend.](#blend-state)</span><span class="sxs-lookup"><span data-stu-id="9bdae-148">A [Blend State](#blend-state) state object.</span></span>                         |
| <span data-ttu-id="9bdae-149">VERTEXSHADER</span><span class="sxs-lookup"><span data-stu-id="9bdae-149">VERTEXSHADER</span></span>                                | <span data-ttu-id="9bdae-150">Oggetto vertex shader compilato.</span><span class="sxs-lookup"><span data-stu-id="9bdae-150">A compiled vertex shader object.</span></span>                                    |
| <span data-ttu-id="9bdae-151">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="9bdae-151">PIXELSHADER</span></span>                                 | <span data-ttu-id="9bdae-152">Oggetto pixel shader compilato.</span><span class="sxs-lookup"><span data-stu-id="9bdae-152">A compiled pixel shader object.</span></span>                                     |
| <span data-ttu-id="9bdae-153">GEOMETRYSHADER</span><span class="sxs-lookup"><span data-stu-id="9bdae-153">GEOMETRYSHADER</span></span>                              | <span data-ttu-id="9bdae-154">Oggetto geometry shader compilato.</span><span class="sxs-lookup"><span data-stu-id="9bdae-154">A compiled geometry shader object.</span></span>                                  |
| <span data-ttu-id="9bdae-155">DS \_ STENCILREFAB \_ BLENDFACTORAB \_ SAMPLEMASK</span><span class="sxs-lookup"><span data-stu-id="9bdae-155">DS\_STENCILREFAB\_BLENDFACTORAB\_SAMPLEMASK</span></span> | <span data-ttu-id="9bdae-156">Membri di [**D3DX11 \_ PASS \_ DESC**](d3dx11-pass-desc.md).</span><span class="sxs-lookup"><span data-stu-id="9bdae-156">Members of [**D3DX11\_PASS\_DESC**](d3dx11-pass-desc.md).</span></span>          |



 

## <a name="defining-and-using-state-objects"></a><span data-ttu-id="9bdae-157">Definizione e uso di oggetti di stato</span><span class="sxs-lookup"><span data-stu-id="9bdae-157">Defining and using state objects</span></span>

<span data-ttu-id="9bdae-158">Gli oggetti di stato vengono dichiarati nei file FX nel formato seguente.</span><span class="sxs-lookup"><span data-stu-id="9bdae-158">State objects are declared in FX files in the following format.</span></span> <span data-ttu-id="9bdae-159">StateObjectType è uno degli stati elencati in precedenza e MemberName è il nome di qualsiasi membro che avrà un valore non predefinito.</span><span class="sxs-lookup"><span data-stu-id="9bdae-159">StateObjectType is one of the states listed above and MemberName is the name of any member that will have a non-default value.</span></span>


```
StateObjectType ObjectName {
  MemberName = value;
  ...
  MemberName = value;
};
    
```



<span data-ttu-id="9bdae-160">Ad esempio, per impostare un oggetto stato di blend con AlphaToCoverageEnable e BlendEnable 0 impostato su FALSE, verrà usato \[ \] il codice seguente. </span><span class="sxs-lookup"><span data-stu-id="9bdae-160">For example, to set up a blend state object with AlphaToCoverageEnable and BlendEnable\[0\] set to **FALSE** the following code would be used.</span></span>


```
BlendState NoBlend {
  AlphaToCoverageEnable = FALSE;
  BlendEnable[0] = FALSE;
};
    
```



<span data-ttu-id="9bdae-161">L'oggetto state viene applicato a un passaggio di tecnica usando una delle funzioni SetStateGroup descritte in [Effect Technique Syntax (Direct3D 11)](d3d11-effect-technique-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="9bdae-161">The state object is applied to a technique pass using one of the SetStateGroup functions described in [Effect Technique Syntax (Direct3D 11)](d3d11-effect-technique-syntax.md).</span></span> <span data-ttu-id="9bdae-162">Ad esempio, per applicare l'oggetto BlendState descritto sopra, verrà usato il codice seguente.</span><span class="sxs-lookup"><span data-stu-id="9bdae-162">For example, to apply the BlendState object described above the following code would be used.</span></span>


```
SetBlendState( NoBlend, float4( 0.0f, 0.0f, 0.0f, 0.0f ), 0xFFFFFFFF );
    
```



## <a name="related-topics"></a><span data-ttu-id="9bdae-163">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9bdae-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9bdae-164">Sintassi della tecnica degli effetti</span><span class="sxs-lookup"><span data-stu-id="9bdae-164">Effect Technique Syntax</span></span>](d3d11-effect-technique-syntax.md)
</dt> <dt>

[<span data-ttu-id="9bdae-165">Formato effetto (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="9bdae-165">Effect Format (Direct3D 11)</span></span>](d3d11-effect-format.md)
</dt> </dl>

 

 