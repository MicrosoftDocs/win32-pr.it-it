---
title: Metodi ID3D11Device di 10Level9
description: Questa sezione elenca le differenze tra ogni livello di funzionalità 10Level9 e il livello di funzionalità D3D \_ \_ \_ 11 \_ 0 e un livello di funzionalità superiore per i metodi ID3D11Device.
ms.assetid: c3bc32a9-8d97-430b-be6a-b4935d7ac56c
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 400c7f321981f13b3e184a25139782c8a9d9a2ba
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399466"
---
# <a name="10level9-id3d11device-methods"></a><span data-ttu-id="46d53-103">Metodi ID3D11Device di 10Level9</span><span class="sxs-lookup"><span data-stu-id="46d53-103">10Level9 ID3D11Device Methods</span></span>

<span data-ttu-id="46d53-104">Questa sezione elenca le differenze tra ogni livello di funzionalità 10Level9 e il livello di funzionalità D3D \_ \_ \_ 11 \_ 0 e un livello di funzionalità superiore per i metodi [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) .</span><span class="sxs-lookup"><span data-stu-id="46d53-104">This section lists the differences between each 10Level9 feature level and the D3D\_FEATURE\_LEVEL\_11\_0 and higher feature level for the [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) methods.</span></span>

-   [<span data-ttu-id="46d53-105">ID3D11Device:: CheckCounter</span><span class="sxs-lookup"><span data-stu-id="46d53-105">ID3D11Device::CheckCounter</span></span>](#id3d11devicecheckcounter)
-   [<span data-ttu-id="46d53-106">ID3D11Device:: CheckFormatSupport</span><span class="sxs-lookup"><span data-stu-id="46d53-106">ID3D11Device::CheckFormatSupport</span></span>](#id3d11devicecheckformatsupport)
-   [<span data-ttu-id="46d53-107">ID3D11Device:: CheckMultisampleQualityLevels</span><span class="sxs-lookup"><span data-stu-id="46d53-107">ID3D11Device::CheckMultisampleQualityLevels</span></span>](#id3d11devicecheckmultisamplequalitylevels)
-   [<span data-ttu-id="46d53-108">ID3D11Device:: CreateBlendState</span><span class="sxs-lookup"><span data-stu-id="46d53-108">ID3D11Device::CreateBlendState</span></span>](#id3d11devicecreateblendstate)
-   [<span data-ttu-id="46d53-109">ID3D11Device:: CreateBlendState1</span><span class="sxs-lookup"><span data-stu-id="46d53-109">ID3D11Device::CreateBlendState1</span></span>](#id3d11devicecreateblendstate1)
-   [<span data-ttu-id="46d53-110">ID3D11Device:: CreateBuffer</span><span class="sxs-lookup"><span data-stu-id="46d53-110">ID3D11Device::CreateBuffer</span></span>](#id3d11devicecreatebuffer)
-   [<span data-ttu-id="46d53-111">ID3D11Device:: CreateCounter</span><span class="sxs-lookup"><span data-stu-id="46d53-111">ID3D11Device::CreateCounter</span></span>](#id3d11devicecreatecounter)
-   [<span data-ttu-id="46d53-112">ID3D11Device:: CreateDepthStencilView</span><span class="sxs-lookup"><span data-stu-id="46d53-112">ID3D11Device::CreateDepthStencilView</span></span>](#id3d11devicecreatedepthstencilview)
-   [<span data-ttu-id="46d53-113">ID3D11Device:: CreateDomainShader</span><span class="sxs-lookup"><span data-stu-id="46d53-113">ID3D11Device::CreateDomainShader</span></span>](#id3d11devicecreatedomainshader)
-   [<span data-ttu-id="46d53-114">ID3D11Device:: CreateGeometryShader</span><span class="sxs-lookup"><span data-stu-id="46d53-114">ID3D11Device::CreateGeometryShader</span></span>](#id3d11devicecreategeometryshader)
-   [<span data-ttu-id="46d53-115">ID3D11Device:: CreateGeometryShaderWithStreamOutput</span><span class="sxs-lookup"><span data-stu-id="46d53-115">ID3D11Device::CreateGeometryShaderWithStreamOutput</span></span>](#id3d11devicecreategeometryshaderwithstreamoutput)
-   [<span data-ttu-id="46d53-116">ID3D11Device:: CreateHullShader</span><span class="sxs-lookup"><span data-stu-id="46d53-116">ID3D11Device::CreateHullShader</span></span>](#id3d11devicecreatehullshader)
-   [<span data-ttu-id="46d53-117">ID3D11Device:: CreateInputLayout</span><span class="sxs-lookup"><span data-stu-id="46d53-117">ID3D11Device::CreateInputLayout</span></span>](#id3d11devicecreateinputlayout)
-   [<span data-ttu-id="46d53-118">ID3D11Device:: CreatePixelShader</span><span class="sxs-lookup"><span data-stu-id="46d53-118">ID3D11Device::CreatePixelShader</span></span>](#id3d11devicecreatepixelshader)
-   [<span data-ttu-id="46d53-119">ID3D11Device:: CreatePredicate</span><span class="sxs-lookup"><span data-stu-id="46d53-119">ID3D11Device::CreatePredicate</span></span>](#id3d11devicecreatepredicate)
-   [<span data-ttu-id="46d53-120">ID3D11Device:: CreateQuery</span><span class="sxs-lookup"><span data-stu-id="46d53-120">ID3D11Device::CreateQuery</span></span>](#id3d11devicecreatequery)
-   [<span data-ttu-id="46d53-121">ID3D11Device:: CreateRasterizerState</span><span class="sxs-lookup"><span data-stu-id="46d53-121">ID3D11Device::CreateRasterizerState</span></span>](#id3d11devicecreaterasterizerstate)
-   [<span data-ttu-id="46d53-122">ID3D11Device:: CreateRenderTargetView</span><span class="sxs-lookup"><span data-stu-id="46d53-122">ID3D11Device::CreateRenderTargetView</span></span>](#id3d11devicecreaterendertargetview)
-   [<span data-ttu-id="46d53-123">ID3D11Device:: CreateSamplerState</span><span class="sxs-lookup"><span data-stu-id="46d53-123">ID3D11Device::CreateSamplerState</span></span>](#id3d11devicecreatesamplerstate)
-   [<span data-ttu-id="46d53-124">ID3D11Device:: CreateShaderResourceView</span><span class="sxs-lookup"><span data-stu-id="46d53-124">ID3D11Device::CreateShaderResourceView</span></span>](#id3d11devicecreateshaderresourceview)
-   [<span data-ttu-id="46d53-125">ID3D11Device:: CreateTexture1D</span><span class="sxs-lookup"><span data-stu-id="46d53-125">ID3D11Device::CreateTexture1D</span></span>](#id3d11devicecreatetexture1d)
-   [<span data-ttu-id="46d53-126">ID3D11Device:: CreateTexture2D</span><span class="sxs-lookup"><span data-stu-id="46d53-126">ID3D11Device::CreateTexture2D</span></span>](#id3d11devicecreatetexture2d)
-   [<span data-ttu-id="46d53-127">ID3D11Device:: CreateTexture3D</span><span class="sxs-lookup"><span data-stu-id="46d53-127">ID3D11Device::CreateTexture3D</span></span>](#id3d11devicecreatetexture3d)
-   [<span data-ttu-id="46d53-128">ID3D11Device:: CreateUnorderedAccessView</span><span class="sxs-lookup"><span data-stu-id="46d53-128">ID3D11Device::CreateUnorderedAccessView</span></span>](#id3d11devicecreateunorderedaccessview)
-   [<span data-ttu-id="46d53-129">ID3D11Device:: CreateVertexShader</span><span class="sxs-lookup"><span data-stu-id="46d53-129">ID3D11Device::CreateVertexShader</span></span>](#id3d11devicecreatevertexshader)
-   [<span data-ttu-id="46d53-130">ID3D11Device:: OpenSharedResource</span><span class="sxs-lookup"><span data-stu-id="46d53-130">ID3D11Device::OpenSharedResource</span></span>](#id3d11deviceopensharedresource)
-   [<span data-ttu-id="46d53-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="46d53-131">Related topics</span></span>](#related-topics)

## <a name="id3d11devicecheckcounter"></a><span data-ttu-id="46d53-132">ID3D11Device:: CheckCounter</span><span class="sxs-lookup"><span data-stu-id="46d53-132">ID3D11Device::CheckCounter</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="46d53-133">Livello funzionalità</span><span class="sxs-lookup"><span data-stu-id="46d53-133">Feature Level</span></span></th>
<th><span data-ttu-id="46d53-134">Differenze di comportamento</span><span class="sxs-lookup"><span data-stu-id="46d53-134">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="46d53-135">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="46d53-135">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="46d53-136">I contatori dipendenti dal dispositivo sono facoltativamente supportati.</span><span class="sxs-lookup"><span data-stu-id="46d53-136">Device-dependent counters are optionally supported.</span></span> <span data-ttu-id="46d53-137">Usare <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkcounterinfo"><strong>ID3D11Device:: CheckCounterInfo</strong></a> per determinare il supporto. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="46d53-137">Use <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkcounterinfo"><strong>ID3D11Device::CheckCounterInfo</strong></a> to determine support.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="46d53-138">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="46d53-138">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="46d53-139">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="46d53-139">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecheckformatsupport"></a><span data-ttu-id="46d53-140">ID3D11Device:: CheckFormatSupport</span><span class="sxs-lookup"><span data-stu-id="46d53-140">ID3D11Device::CheckFormatSupport</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="46d53-141">Livello funzionalità</span><span class="sxs-lookup"><span data-stu-id="46d53-141">Feature Level</span></span></th>
<th><span data-ttu-id="46d53-142">Differenze di comportamento</span><span class="sxs-lookup"><span data-stu-id="46d53-142">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="46d53-143">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="46d53-143">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="46d53-144">Vedere supporto del formato in base al <a href="overviews-direct3d-11-devices-downlevel-intro.md">livello di funzionalità</a>$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="46d53-144">See format support by <a href="overviews-direct3d-11-devices-downlevel-intro.md">feature level</a>${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="46d53-145">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="46d53-145">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="46d53-146">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="46d53-146">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecheckmultisamplequalitylevels"></a><span data-ttu-id="46d53-147">ID3D11Device:: CheckMultisampleQualityLevels</span><span class="sxs-lookup"><span data-stu-id="46d53-147">ID3D11Device::CheckMultisampleQualityLevels</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="46d53-148">Livello funzionalità</span><span class="sxs-lookup"><span data-stu-id="46d53-148">Feature Level</span></span></th>
<th><span data-ttu-id="46d53-149">Differenze di comportamento</span><span class="sxs-lookup"><span data-stu-id="46d53-149">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="46d53-150">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="46d53-150">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="46d53-151">I livelli di funzionalità non offrono alcuna garanzia sul supporto MSAA. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="46d53-151">Feature levels make no guarantees concerning MSAA support.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="46d53-152">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="46d53-152">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="46d53-153">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="46d53-153">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreateblendstate"></a><span data-ttu-id="46d53-154">ID3D11Device:: CreateBlendState</span><span class="sxs-lookup"><span data-stu-id="46d53-154">ID3D11Device::CreateBlendState</span></span>



| <span data-ttu-id="46d53-155">Livello funzionalità</span><span class="sxs-lookup"><span data-stu-id="46d53-155">Feature Level</span></span>              | <span data-ttu-id="46d53-156">Differenze di comportamento</span><span class="sxs-lookup"><span data-stu-id="46d53-156">Behavior Differences</span></span>                                                                                                                                                                                                                                                                                                                                             |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46d53-157">\_Livello di funzionalità D3D \_ \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="46d53-157">D3D\_FEATURE\_LEVEL\_9\_1</span></span>  | <span data-ttu-id="46d53-158">AlphaToCoverageEnable deve essere **false**.</span><span class="sxs-lookup"><span data-stu-id="46d53-158">AlphaToCoverageEnable must be **FALSE**.</span></span><br/> <span data-ttu-id="46d53-159">I primi quattro BlendEnables devono avere lo stesso valore.</span><span class="sxs-lookup"><span data-stu-id="46d53-159">The first four BlendEnables must all have the same value.</span></span><br/> <span data-ttu-id="46d53-160">D3D11 \_ di \_ Blend \_ ALPHASAT src non supportato.</span><span class="sxs-lookup"><span data-stu-id="46d53-160">D3D11\_BLEND\_SRC\_ALPHASAT not supported.</span></span><br/> <span data-ttu-id="46d53-161">La combinazione di colori dual source non è supportata (qualsiasi SrcBlend o DestBlend con SRC1 nel nome)</span><span class="sxs-lookup"><span data-stu-id="46d53-161">Dual-source color blend not supported (any SrcBlend or DestBlend with SRC1 in the name)</span></span><br/>                                                                                |
| <span data-ttu-id="46d53-162">\_Livello di funzionalità D3D \_ \_ 9 \_ 2</span><span class="sxs-lookup"><span data-stu-id="46d53-162">D3D\_FEATURE\_LEVEL\_9\_2</span></span>  | <span data-ttu-id="46d53-163">AlphaToCoverageEnable deve essere **false**.</span><span class="sxs-lookup"><span data-stu-id="46d53-163">AlphaToCoverageEnable must be **FALSE**.</span></span><br/> <span data-ttu-id="46d53-164">I primi quattro BlendEnables devono avere lo stesso valore.</span><span class="sxs-lookup"><span data-stu-id="46d53-164">The first four BlendEnables must all have the same value.</span></span><br/> <span data-ttu-id="46d53-165">I primi quattro RenderTargetWriteMasks devono avere lo stesso valore.</span><span class="sxs-lookup"><span data-stu-id="46d53-165">The first four RenderTargetWriteMasks must all have the same value.</span></span><br/> <span data-ttu-id="46d53-166">D3D11 \_ di \_ Blend \_ ALPHASAT src non supportato.</span><span class="sxs-lookup"><span data-stu-id="46d53-166">D3D11\_BLEND\_SRC\_ALPHASAT not supported.</span></span><br/> <span data-ttu-id="46d53-167">La combinazione di colori dual source non è supportata (qualsiasi SrcBlend o DestBlend con SRC1 nel nome)</span><span class="sxs-lookup"><span data-stu-id="46d53-167">Dual-source color blend not supported (any SrcBlend or DestBlend with SRC1 in the name)</span></span><br/> |
| <span data-ttu-id="46d53-168">\_Livello di funzionalità D3D \_ \_ 9 \_ 3</span><span class="sxs-lookup"><span data-stu-id="46d53-168">D3D\_FEATURE\_LEVEL\_9\_3</span></span>  | <span data-ttu-id="46d53-169">AlphaToCoverageEnable deve essere **false**.</span><span class="sxs-lookup"><span data-stu-id="46d53-169">AlphaToCoverageEnable must be **FALSE**.</span></span><br/> <span data-ttu-id="46d53-170">I primi quattro BlendEnables devono avere lo stesso valore.</span><span class="sxs-lookup"><span data-stu-id="46d53-170">The first four BlendEnables must all have the same value.</span></span><br/> <span data-ttu-id="46d53-171">D3D11 \_ di \_ Blend \_ ALPHASAT src non supportato.</span><span class="sxs-lookup"><span data-stu-id="46d53-171">D3D11\_BLEND\_SRC\_ALPHASAT not supported.</span></span><br/> <span data-ttu-id="46d53-172">La combinazione di colori dual source non è supportata (qualsiasi SrcBlend o DestBlend con SRC1 nel nome)</span><span class="sxs-lookup"><span data-stu-id="46d53-172">Dual-source color blend not supported (any SrcBlend or DestBlend with SRC1 in the name)</span></span><br/>                                                                                |
| <span data-ttu-id="46d53-173">\_Livello di funzionalità D3D \_ \_ 10 \_ 0</span><span class="sxs-lookup"><span data-stu-id="46d53-173">D3D\_FEATURE\_LEVEL\_10\_0</span></span> | <span data-ttu-id="46d53-174">Aggiunge l'alfa al code coverage</span><span class="sxs-lookup"><span data-stu-id="46d53-174">Adds alpha-to-coverage</span></span>                                                                                                                                                                                                                                                                                                                                           |



 

## <a name="id3d11devicecreateblendstate1"></a><span data-ttu-id="46d53-175">ID3D11Device:: CreateBlendState1</span><span class="sxs-lookup"><span data-stu-id="46d53-175">ID3D11Device::CreateBlendState1</span></span>



| <span data-ttu-id="46d53-176">Livello funzionalità</span><span class="sxs-lookup"><span data-stu-id="46d53-176">Feature Level</span></span>              | <span data-ttu-id="46d53-177">Differenze di comportamento</span><span class="sxs-lookup"><span data-stu-id="46d53-177">Behavior Differences</span></span>                                                                                                                                                                                                                                                                                                                                         |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46d53-178">\_Livello di funzionalità D3D \_ \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="46d53-178">D3D\_FEATURE\_LEVEL\_9\_1</span></span>  | <span data-ttu-id="46d53-179">Non supportato</span><span class="sxs-lookup"><span data-stu-id="46d53-179">Unsupported</span></span><br/>                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="46d53-180">\_Livello di funzionalità D3D \_ \_ 9 \_ 2</span><span class="sxs-lookup"><span data-stu-id="46d53-180">D3D\_FEATURE\_LEVEL\_9\_2</span></span>  | <span data-ttu-id="46d53-181">Non supportato</span><span class="sxs-lookup"><span data-stu-id="46d53-181">Unsupported</span></span><br/>                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="46d53-182">\_Livello di funzionalità D3D \_ \_ 9 \_ 3</span><span class="sxs-lookup"><span data-stu-id="46d53-182">D3D\_FEATURE\_LEVEL\_9\_3</span></span>  | <span data-ttu-id="46d53-183">Non supportato</span><span class="sxs-lookup"><span data-stu-id="46d53-183">Unsupported</span></span><br/>                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="46d53-184">\_Livello di funzionalità D3D \_ \_ 10 \_ 0</span><span class="sxs-lookup"><span data-stu-id="46d53-184">D3D\_FEATURE\_LEVEL\_10\_0</span></span> | <span data-ttu-id="46d53-185">Il membro *OutputMergerLogicOp* è stato aggiunto alle [**\_ \_ \_ \_ Opzioni d3d11 dei dati della funzionalità d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options)per determinare il supporto per le operazioni logiche (operazioni logiche bit per bit tra pixel shader output e il contenuto della destinazione di rendering, fare riferimento a [**d3d11 \_ Render \_ target \_ Blend \_ DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-d3d11_render_target_blend_desc1)).</span><span class="sxs-lookup"><span data-stu-id="46d53-185">The *OutputMergerLogicOp* member has been added to [**D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options), to determine support for logical operations (bitwise logic operations between pixel shader output and render target contents, refer to [**D3D11\_RENDER\_TARGET\_BLEND\_DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-d3d11_render_target_blend_desc1)).</span></span> |



 

## <a name="id3d11devicecreatebuffer"></a><span data-ttu-id="46d53-186">ID3D11Device:: CreateBuffer</span><span class="sxs-lookup"><span data-stu-id="46d53-186">ID3D11Device::CreateBuffer</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="46d53-187">Livello funzionalità</span><span class="sxs-lookup"><span data-stu-id="46d53-187">Feature Level</span></span></th>
<th><span data-ttu-id="46d53-188">Differenze di comportamento</span><span class="sxs-lookup"><span data-stu-id="46d53-188">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="46d53-189">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="46d53-189">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td><span data-ttu-id="46d53-190">I buffer non possono avere visualizzazioni di destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="46d53-190">Buffers can't have render target views.</span></span><br/> <span data-ttu-id="46d53-191">I buffer devono avere esattamente uno dei D3D11_BIND_VERTEX_BUFFER, D3D11_BIND_INDEX_BUFFER o D3D11_BIND_CONSTANT_BUFFER.</span><span class="sxs-lookup"><span data-stu-id="46d53-191">Buffers must have exactly one of D3D11_BIND_VERTEX_BUFFER, D3D11_BIND_INDEX_BUFFER, or D3D11_BIND_CONSTANT_BUFFER.</span></span><br/> <span data-ttu-id="46d53-192">Consente solo buffer di indice con il formato DXGI_FORMAT_R16_UINT.</span><span class="sxs-lookup"><span data-stu-id="46d53-192">Only allows index buffers with the DXGI_FORMAT_R16_UINT format.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="46d53-193">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="46d53-193">D3D_FEATURE_LEVEL_9_2</span></span></td>
<td rowspan="2"> <span data-ttu-id="46d53-194">I buffer non possono avere visualizzazioni di destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="46d53-194">Buffers can't have render target views.</span></span><br/> <span data-ttu-id="46d53-195">I buffer devono avere esattamente uno dei D3D11_BIND_VERTEX_BUFFER, D3D11_BIND_INDEX_BUFFER o D3D11_BIND_CONSTANT_BUFFER.</span><span class="sxs-lookup"><span data-stu-id="46d53-195">Buffers must have exactly one of D3D11_BIND_VERTEX_BUFFER, D3D11_BIND_INDEX_BUFFER, or D3D11_BIND_CONSTANT_BUFFER.</span></span><br/> <span data-ttu-id="46d53-196">Consente i buffer di indice con i formati DXGI_FORMAT_R16_UINT e DXGI_FORMAT_R32_UINT come D3D_FEATURE_LEVEL_10_0 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="46d53-196">Allows index buffers with the DXGI_FORMAT_R16_UINT and DXGI_FORMAT_R32_UINT formats like D3D_FEATURE_LEVEL_10_0 and higher.</span></span> <br/> <span data-ttu-id="46d53-197">$ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="46d53-197">${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="odd">
<td><span data-ttu-id="46d53-198">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="46d53-198">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreatecounter"></a><span data-ttu-id="46d53-199">ID3D11Device:: CreateCounter</span><span class="sxs-lookup"><span data-stu-id="46d53-199">ID3D11Device::CreateCounter</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="46d53-200">Livello funzionalità</span><span class="sxs-lookup"><span data-stu-id="46d53-200">Feature Level</span></span></th>
<th><span data-ttu-id="46d53-201">Differenze di comportamento</span><span class="sxs-lookup"><span data-stu-id="46d53-201">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="46d53-202">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="46d53-202">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="46d53-203">Non supportato in alcun livello di funzionalità 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="46d53-203">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="46d53-204">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="46d53-204">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="46d53-205">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="46d53-205">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreatedepthstencilview"></a><span data-ttu-id="46d53-206">ID3D11Device:: CreateDepthStencilView</span><span class="sxs-lookup"><span data-stu-id="46d53-206">ID3D11Device::CreateDepthStencilView</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="46d53-207">Livello funzionalità</span><span class="sxs-lookup"><span data-stu-id="46d53-207">Feature Level</span></span></th>
<th><span data-ttu-id="46d53-208">Differenze di comportamento</span><span class="sxs-lookup"><span data-stu-id="46d53-208">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="46d53-209">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="46d53-209">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="46d53-210">Non supporta lo stencil a due lati. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="46d53-210">Does not support two-sided stencil.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="46d53-211">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="46d53-211">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="46d53-212">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="46d53-212">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreatedomainshader"></a><span data-ttu-id="46d53-213">ID3D11Device:: CreateDomainShader</span><span class="sxs-lookup"><span data-stu-id="46d53-213">ID3D11Device::CreateDomainShader</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="46d53-214">Livello funzionalità</span><span class="sxs-lookup"><span data-stu-id="46d53-214">Feature Level</span></span></th>
<th><span data-ttu-id="46d53-215">Differenze di comportamento</span><span class="sxs-lookup"><span data-stu-id="46d53-215">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="46d53-216">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="46d53-216">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="5"><span data-ttu-id="46d53-217">Non supportato in alcun livello di funzionalità 9. \* o 10. \*.</span><span class="sxs-lookup"><span data-stu-id="46d53-217">Not supported on any 9.\* or 10.\* feature level.</span></span> <span data-ttu-id="46d53-218">$ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="46d53-218">${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="46d53-219">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="46d53-219">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="46d53-220">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="46d53-220">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="46d53-221">D3D_FEATURE_LEVEL_10_0</span><span class="sxs-lookup"><span data-stu-id="46d53-221">D3D_FEATURE_LEVEL_10_0</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="46d53-222">D3D_FEATURE_LEVEL_10_1</span><span class="sxs-lookup"><span data-stu-id="46d53-222">D3D_FEATURE_LEVEL_10_1</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreategeometryshader"></a><span data-ttu-id="46d53-223">ID3D11Device:: CreateGeometryShader</span><span class="sxs-lookup"><span data-stu-id="46d53-223">ID3D11Device::CreateGeometryShader</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="46d53-224">Livello funzionalità</span><span class="sxs-lookup"><span data-stu-id="46d53-224">Feature Level</span></span></th>
<th><span data-ttu-id="46d53-225">Differenze di comportamento</span><span class="sxs-lookup"><span data-stu-id="46d53-225">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="46d53-226">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="46d53-226">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="46d53-227">Non supportato in alcun livello di funzionalità 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="46d53-227">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="46d53-228">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="46d53-228">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="46d53-229">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="46d53-229">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreategeometryshaderwithstreamoutput"></a><span data-ttu-id="46d53-230">ID3D11Device:: CreateGeometryShaderWithStreamOutput</span><span class="sxs-lookup"><span data-stu-id="46d53-230">ID3D11Device::CreateGeometryShaderWithStreamOutput</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="46d53-231">Livello funzionalità</span><span class="sxs-lookup"><span data-stu-id="46d53-231">Feature Level</span></span></th>
<th><span data-ttu-id="46d53-232">Differenze di comportamento</span><span class="sxs-lookup"><span data-stu-id="46d53-232">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="46d53-233">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="46d53-233">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="46d53-234">Non supportato in alcun livello di funzionalità 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="46d53-234">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="46d53-235">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="46d53-235">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="46d53-236">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="46d53-236">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreatehullshader"></a><span data-ttu-id="46d53-237">ID3D11Device:: CreateHullShader</span><span class="sxs-lookup"><span data-stu-id="46d53-237">ID3D11Device::CreateHullShader</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="46d53-238">Livello funzionalità</span><span class="sxs-lookup"><span data-stu-id="46d53-238">Feature Level</span></span></th>
<th><span data-ttu-id="46d53-239">Differenze di comportamento</span><span class="sxs-lookup"><span data-stu-id="46d53-239">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="46d53-240">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="46d53-240">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="5"><span data-ttu-id="46d53-241">Non supportato in alcun livello di funzionalità 9. \* o 10. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="46d53-241">Not supported on any 9.\* or 10.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="46d53-242">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="46d53-242">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="46d53-243">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="46d53-243">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="46d53-244">D3D_FEATURE_LEVEL_10_0</span><span class="sxs-lookup"><span data-stu-id="46d53-244">D3D_FEATURE_LEVEL_10_0</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="46d53-245">D3D_FEATURE_LEVEL_10_1</span><span class="sxs-lookup"><span data-stu-id="46d53-245">D3D_FEATURE_LEVEL_10_1</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreateinputlayout"></a><span data-ttu-id="46d53-246">ID3D11Device:: CreateInputLayout</span><span class="sxs-lookup"><span data-stu-id="46d53-246">ID3D11Device::CreateInputLayout</span></span>



| <span data-ttu-id="46d53-247">Livello funzionalità</span><span class="sxs-lookup"><span data-stu-id="46d53-247">Feature Level</span></span>             | <span data-ttu-id="46d53-248">Differenze di comportamento</span><span class="sxs-lookup"><span data-stu-id="46d53-248">Behavior Differences</span></span>                                                                                              |
|---------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46d53-249">\_Livello di funzionalità D3D \_ \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="46d53-249">D3D\_FEATURE\_LEVEL\_9\_1</span></span> | <span data-ttu-id="46d53-250">Non supporta \_ i dati di input d3d11 \_ per \_ istanza \_</span><span class="sxs-lookup"><span data-stu-id="46d53-250">Does not support D3D11\_INPUT\_PER\_INSTANCE\_DATA</span></span>                                                                |
| <span data-ttu-id="46d53-251">\_Livello di funzionalità D3D \_ \_ 9 \_ 2</span><span class="sxs-lookup"><span data-stu-id="46d53-251">D3D\_FEATURE\_LEVEL\_9\_2</span></span> | <span data-ttu-id="46d53-252">Non supporta \_ i dati di input d3d11 \_ per \_ istanza \_</span><span class="sxs-lookup"><span data-stu-id="46d53-252">Does not support D3D11\_INPUT\_PER\_INSTANCE\_DATA</span></span>                                                                |
| <span data-ttu-id="46d53-253">\_Livello di funzionalità D3D \_ \_ 9 \_ 3</span><span class="sxs-lookup"><span data-stu-id="46d53-253">D3D\_FEATURE\_LEVEL\_9\_3</span></span> | <span data-ttu-id="46d53-254">Il flusso di vertici zero deve avere \_ input d3d11 \_ per \_ \_ i dati del vertice, se i flussi hanno input di d3d11 \_ \_ per \_ dati del vertice \_</span><span class="sxs-lookup"><span data-stu-id="46d53-254">Vertex stream zero must have D3D11\_INPUT\_PER\_VERTEX\_DATA, if any streams have D3D11\_INPUT\_PER\_VERTEX\_DATA</span></span> |



 

<span data-ttu-id="46d53-255">Per informazioni dettagliate sui formati che possono essere usati per i dati dei vertici a ogni livello di funzionalità, vedere il formato supporto per [grafico a livello di funzionalità](overviews-direct3d-11-devices-downlevel-intro.md) .</span><span class="sxs-lookup"><span data-stu-id="46d53-255">See the format support by [feature level chart](overviews-direct3d-11-devices-downlevel-intro.md) for details on what formats can be used for vertex data at each feature level.</span></span>

## <a name="id3d11devicecreatepixelshader"></a><span data-ttu-id="46d53-256">ID3D11Device:: CreatePixelShader</span><span class="sxs-lookup"><span data-stu-id="46d53-256">ID3D11Device::CreatePixelShader</span></span>



| <span data-ttu-id="46d53-257">Livello funzionalità</span><span class="sxs-lookup"><span data-stu-id="46d53-257">Feature Level</span></span>             | <span data-ttu-id="46d53-258">Differenze di comportamento</span><span class="sxs-lookup"><span data-stu-id="46d53-258">Behavior Differences</span></span>                                    |
|---------------------------|---------------------------------------------------------|
| <span data-ttu-id="46d53-259">\_Livello di funzionalità D3D \_ \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="46d53-259">D3D\_FEATURE\_LEVEL\_9\_1</span></span> | <span data-ttu-id="46d53-260">Usare PS \_ 4 \_ 0 \_ level \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="46d53-260">Must use ps\_4\_0\_level\_9\_1</span></span>                          |
| <span data-ttu-id="46d53-261">\_Livello di funzionalità D3D \_ \_ 9 \_ 2</span><span class="sxs-lookup"><span data-stu-id="46d53-261">D3D\_FEATURE\_LEVEL\_9\_2</span></span> | <span data-ttu-id="46d53-262">Usare PS \_ 4 \_ 0 \_ level \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="46d53-262">Must use ps\_4\_0\_level\_9\_1</span></span>                          |
| <span data-ttu-id="46d53-263">\_Livello di funzionalità D3D \_ \_ 9 \_ 3</span><span class="sxs-lookup"><span data-stu-id="46d53-263">D3D\_FEATURE\_LEVEL\_9\_3</span></span> | <span data-ttu-id="46d53-264">È necessario usare PS \_ 4 \_ 0 \_ level \_ 9 \_ 3 o PS \_ 4 \_ 0 \_ level \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="46d53-264">Must use ps\_4\_0\_level\_9\_3 or ps\_4\_0\_level\_9\_1</span></span> |



 

## <a name="id3d11devicecreatepredicate"></a><span data-ttu-id="46d53-265">ID3D11Device:: CreatePredicate</span><span class="sxs-lookup"><span data-stu-id="46d53-265">ID3D11Device::CreatePredicate</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="46d53-266">Livello funzionalità</span><span class="sxs-lookup"><span data-stu-id="46d53-266">Feature Level</span></span></th>
<th><span data-ttu-id="46d53-267">Differenze di comportamento</span><span class="sxs-lookup"><span data-stu-id="46d53-267">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="46d53-268">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="46d53-268">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="46d53-269">Non supportato in alcun livello di funzionalità 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="46d53-269">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="46d53-270">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="46d53-270">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="46d53-271">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="46d53-271">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreatequery"></a><span data-ttu-id="46d53-272">ID3D11Device:: CreateQuery</span><span class="sxs-lookup"><span data-stu-id="46d53-272">ID3D11Device::CreateQuery</span></span>



| <span data-ttu-id="46d53-273">Livello funzionalità</span><span class="sxs-lookup"><span data-stu-id="46d53-273">Feature Level</span></span>             | <span data-ttu-id="46d53-274">Differenze di comportamento</span><span class="sxs-lookup"><span data-stu-id="46d53-274">Behavior Differences</span></span>                                                                                                                                  |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46d53-275">\_Livello di funzionalità D3D \_ \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="46d53-275">D3D\_FEATURE\_LEVEL\_9\_1</span></span> | <span data-ttu-id="46d53-276">Sono supportate le query di eventi.</span><span class="sxs-lookup"><span data-stu-id="46d53-276">Event queries are supported.</span></span> <span data-ttu-id="46d53-277">Le query timestamp sono facoltative: chiamare [**CreateQuery**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createquery) per determinare il supporto.</span><span class="sxs-lookup"><span data-stu-id="46d53-277">Timestamp queries are optional: call [**CreateQuery**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createquery) to determine support.</span></span>               |
| <span data-ttu-id="46d53-278">\_Livello di funzionalità D3D \_ \_ 9 \_ 2</span><span class="sxs-lookup"><span data-stu-id="46d53-278">D3D\_FEATURE\_LEVEL\_9\_2</span></span> | <span data-ttu-id="46d53-279">Sono supportate le query di eventi e occlusioni.</span><span class="sxs-lookup"><span data-stu-id="46d53-279">Event and occlusion queries are supported.</span></span> <span data-ttu-id="46d53-280">Le query timestamp sono facoltative: chiamare [**CreateQuery**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createquery) per determinare il supporto.</span><span class="sxs-lookup"><span data-stu-id="46d53-280">Timestamp queries are optional: call [**CreateQuery**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createquery) to determine support.</span></span> |
| <span data-ttu-id="46d53-281">\_Livello di funzionalità D3D \_ \_ 9 \_ 3</span><span class="sxs-lookup"><span data-stu-id="46d53-281">D3D\_FEATURE\_LEVEL\_9\_3</span></span> | <span data-ttu-id="46d53-282">Sono supportate le query di eventi e occlusioni.</span><span class="sxs-lookup"><span data-stu-id="46d53-282">Event and occlusion queries are supported.</span></span> <span data-ttu-id="46d53-283">Le query timestamp sono facoltative: chiamare [**CreateQuery**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createquery) per determinare il supporto.</span><span class="sxs-lookup"><span data-stu-id="46d53-283">Timestamp queries are optional: call [**CreateQuery**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createquery) to determine support.</span></span> |



 

## <a name="id3d11devicecreaterasterizerstate"></a><span data-ttu-id="46d53-284">ID3D11Device:: CreateRasterizerState</span><span class="sxs-lookup"><span data-stu-id="46d53-284">ID3D11Device::CreateRasterizerState</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="46d53-285">Livello funzionalità</span><span class="sxs-lookup"><span data-stu-id="46d53-285">Feature Level</span></span></th>
<th><span data-ttu-id="46d53-286">Differenze di comportamento</span><span class="sxs-lookup"><span data-stu-id="46d53-286">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="46d53-287">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="46d53-287">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="46d53-288">DepthClipEnable deve essere <strong>true</strong>.</span><span class="sxs-lookup"><span data-stu-id="46d53-288">DepthClipEnable must be <strong>TRUE</strong>.</span></span> <span data-ttu-id="46d53-289">DepthBiasClamp deve essere impostato su 0. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="46d53-289">DepthBiasClamp must be set to 0.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="46d53-290">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="46d53-290">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="46d53-291">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="46d53-291">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreaterendertargetview"></a><span data-ttu-id="46d53-292">ID3D11Device:: CreateRenderTargetView</span><span class="sxs-lookup"><span data-stu-id="46d53-292">ID3D11Device::CreateRenderTargetView</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="46d53-293">Livello funzionalità</span><span class="sxs-lookup"><span data-stu-id="46d53-293">Feature Level</span></span></th>
<th><span data-ttu-id="46d53-294">Differenze di comportamento</span><span class="sxs-lookup"><span data-stu-id="46d53-294">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="46d53-295">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="46d53-295">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="46d53-296">Può supportare solo visualizzazioni di destinazione di rendering di oggetti Texture2D. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="46d53-296">Can only support render target views of Texture2D objects.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="46d53-297">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="46d53-297">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="46d53-298">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="46d53-298">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreatesamplerstate"></a><span data-ttu-id="46d53-299">ID3D11Device:: CreateSamplerState</span><span class="sxs-lookup"><span data-stu-id="46d53-299">ID3D11Device::CreateSamplerState</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="46d53-300">Livello funzionalità</span><span class="sxs-lookup"><span data-stu-id="46d53-300">Feature Level</span></span></th>
<th><span data-ttu-id="46d53-301">Differenze di comportamento</span><span class="sxs-lookup"><span data-stu-id="46d53-301">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="46d53-302">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="46d53-302">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td><span data-ttu-id="46d53-303">Il filtro di confronto non è supportato.</span><span class="sxs-lookup"><span data-stu-id="46d53-303">Comparison filter is not supported.</span></span><br/> <span data-ttu-id="46d53-304">Il colore del bordo deve essere compreso tra [0,1]</span><span class="sxs-lookup"><span data-stu-id="46d53-304">Border color must be within [0,1]</span></span><br/> <span data-ttu-id="46d53-305">Min LOD non può essere frazionario</span><span class="sxs-lookup"><span data-stu-id="46d53-305">Min LOD cannot be fractional</span></span><br/> <span data-ttu-id="46d53-306">Il numero massimo di LOD deve essere FLT_MAX</span><span class="sxs-lookup"><span data-stu-id="46d53-306">Max LOD must be FLT_MAX</span></span><br/> <span data-ttu-id="46d53-307">Il numero massimo di anisotropia è 2.</span><span class="sxs-lookup"><span data-stu-id="46d53-307">Maximum anisotropy is 2.</span></span><br/> <span data-ttu-id="46d53-308">D3D11_TEXTURE_ADDRESS_MIRRORONCE non supportato.</span><span class="sxs-lookup"><span data-stu-id="46d53-308">D3D11_TEXTURE_ADDRESS_MIRRORONCE not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="46d53-309">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="46d53-309">D3D_FEATURE_LEVEL_9_2</span></span></td>
<td rowspan="2"> <span data-ttu-id="46d53-310">Il filtro di confronto non è supportato.</span><span class="sxs-lookup"><span data-stu-id="46d53-310">Comparison filter is not supported.</span></span><br/> <span data-ttu-id="46d53-311">Il colore del bordo deve essere compreso tra [0,1]</span><span class="sxs-lookup"><span data-stu-id="46d53-311">Border color must be within [0,1]</span></span><br/> <span data-ttu-id="46d53-312">Min LOD non può essere frazionario</span><span class="sxs-lookup"><span data-stu-id="46d53-312">Min LOD cannot be fractional</span></span><br/> <span data-ttu-id="46d53-313">Il numero massimo di LOD deve essere FLT_MAX</span><span class="sxs-lookup"><span data-stu-id="46d53-313">Max LOD must be FLT_MAX</span></span><br/> <span data-ttu-id="46d53-314">Il numero massimo di anisotropia è 16.</span><span class="sxs-lookup"><span data-stu-id="46d53-314">Maximum anisotropy is 16.</span></span><br/> <span data-ttu-id="46d53-315">$ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="46d53-315">${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="odd">
<td><span data-ttu-id="46d53-316">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="46d53-316">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreateshaderresourceview"></a><span data-ttu-id="46d53-317">ID3D11Device:: CreateShaderResourceView</span><span class="sxs-lookup"><span data-stu-id="46d53-317">ID3D11Device::CreateShaderResourceView</span></span>



| <span data-ttu-id="46d53-318">Livello funzionalità</span><span class="sxs-lookup"><span data-stu-id="46d53-318">Feature Level</span></span>             | <span data-ttu-id="46d53-319">MostDetailedMip Plus MipLevels deve includere il valore LOD minimo (subresource più piccolo)</span><span class="sxs-lookup"><span data-stu-id="46d53-319">MostDetailedMip plus MipLevels must include lowest LOD (smallest subresource</span></span> | <span data-ttu-id="46d53-320">La vista deve includere tutti gli elementi della matrice di risorse</span><span class="sxs-lookup"><span data-stu-id="46d53-320">View must include all resource array elements</span></span> |
|---------------------------|------------------------------------------------------------------------------|-----------------------------------------------|
| <span data-ttu-id="46d53-321">\_Livello di funzionalità D3D \_ \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="46d53-321">D3D\_FEATURE\_LEVEL\_9\_1</span></span> | <span data-ttu-id="46d53-322">Sì</span><span class="sxs-lookup"><span data-stu-id="46d53-322">Yes</span></span>                                                                          | <span data-ttu-id="46d53-323">sì</span><span class="sxs-lookup"><span data-stu-id="46d53-323">yes</span></span>                                           |
| <span data-ttu-id="46d53-324">\_Livello di funzionalità D3D \_ \_ 9 \_ 2</span><span class="sxs-lookup"><span data-stu-id="46d53-324">D3D\_FEATURE\_LEVEL\_9\_2</span></span> | <span data-ttu-id="46d53-325">Sì</span><span class="sxs-lookup"><span data-stu-id="46d53-325">Yes</span></span>                                                                          | <span data-ttu-id="46d53-326">Sì</span><span class="sxs-lookup"><span data-stu-id="46d53-326">Yes</span></span>                                           |
| <span data-ttu-id="46d53-327">\_Livello di funzionalità D3D \_ \_ 9 \_ 3</span><span class="sxs-lookup"><span data-stu-id="46d53-327">D3D\_FEATURE\_LEVEL\_9\_3</span></span> | <span data-ttu-id="46d53-328">Sì</span><span class="sxs-lookup"><span data-stu-id="46d53-328">Yes</span></span>                                                                          | <span data-ttu-id="46d53-329">Sì</span><span class="sxs-lookup"><span data-stu-id="46d53-329">Yes</span></span>                                           |



 

## <a name="id3d11devicecreatetexture1d"></a><span data-ttu-id="46d53-330">ID3D11Device:: CreateTexture1D</span><span class="sxs-lookup"><span data-stu-id="46d53-330">ID3D11Device::CreateTexture1D</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="46d53-331">Livello funzionalità</span><span class="sxs-lookup"><span data-stu-id="46d53-331">Feature Level</span></span></th>
<th><span data-ttu-id="46d53-332">Differenze di comportamento</span><span class="sxs-lookup"><span data-stu-id="46d53-332">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="46d53-333">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="46d53-333">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="46d53-334">Non supportato in alcun livello di funzionalità 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="46d53-334">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="46d53-335">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="46d53-335">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="46d53-336">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="46d53-336">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreatetexture2d"></a><span data-ttu-id="46d53-337">ID3D11Device:: CreateTexture2D</span><span class="sxs-lookup"><span data-stu-id="46d53-337">ID3D11Device::CreateTexture2D</span></span>

<span data-ttu-id="46d53-338">Le risorse di Texture2D presentano limiti per la larghezza e l'altezza che variano in base ai [livelli di funzionalità](overviews-direct3d-11-devices-downlevel-intro.md).</span><span class="sxs-lookup"><span data-stu-id="46d53-338">Texture2D resources have limits on their width and height that differ across [feature levels](overviews-direct3d-11-devices-downlevel-intro.md).</span></span> <span data-ttu-id="46d53-339">Nei livelli di funzionalità 9 \_ 3, di seguito sono riportate le garanzie minime e le singole implementazioni possono superare i requisiti.</span><span class="sxs-lookup"><span data-stu-id="46d53-339">In feature levels 9\_3, the following are guaranteed minima, and individual implementations may exceed the requirements.</span></span>



| <span data-ttu-id="46d53-340">Livello funzionalità</span><span class="sxs-lookup"><span data-stu-id="46d53-340">Feature Level</span></span>             | <span data-ttu-id="46d53-341">Se MipCount > 1, le dimensioni devono essere una potenza integrale di due</span><span class="sxs-lookup"><span data-stu-id="46d53-341">If MipCount > 1, Dimensions must be integral power of two</span></span> | <span data-ttu-id="46d53-342">Dimensione di trama minima supportata</span><span class="sxs-lookup"><span data-stu-id="46d53-342">Minimum supported texture dimension</span></span> | <span data-ttu-id="46d53-343">Le dimensioni delle trame del cubo devono essere una potenza di due</span><span class="sxs-lookup"><span data-stu-id="46d53-343">Cube textures dimensions must be power of two</span></span> | <span data-ttu-id="46d53-344">Se \_ è impostata la TEXTURECUBE misc, ArraySize è:</span><span class="sxs-lookup"><span data-stu-id="46d53-344">If MISC\_TEXTURECUBE is set, the ArraySize is:</span></span> | <span data-ttu-id="46d53-345">Se varie \_ TEXTURECUBE non è impostata, ArraySize è.</span><span class="sxs-lookup"><span data-stu-id="46d53-345">If MISC\_TEXTURECUBE is not set, the ArraySize is.</span></span> |
|---------------------------|--------------------------------------------------------------|-------------------------------------|-----------------------------------------------|------------------------------------------------|----------------------------------------------------|
| <span data-ttu-id="46d53-346">\_Livello di funzionalità D3D \_ \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="46d53-346">D3D\_FEATURE\_LEVEL\_9\_1</span></span> | <span data-ttu-id="46d53-347">Sì</span><span class="sxs-lookup"><span data-stu-id="46d53-347">Yes</span></span>                                                          | <span data-ttu-id="46d53-348">2048</span><span class="sxs-lookup"><span data-stu-id="46d53-348">2048</span></span>                                | <span data-ttu-id="46d53-349">Sì</span><span class="sxs-lookup"><span data-stu-id="46d53-349">Yes</span></span>                                           | <span data-ttu-id="46d53-350">6</span><span class="sxs-lookup"><span data-stu-id="46d53-350">6</span></span>                                              | <span data-ttu-id="46d53-351">1</span><span class="sxs-lookup"><span data-stu-id="46d53-351">1</span></span>                                                  |
| <span data-ttu-id="46d53-352">\_Livello di funzionalità D3D \_ \_ 9 \_ 2</span><span class="sxs-lookup"><span data-stu-id="46d53-352">D3D\_FEATURE\_LEVEL\_9\_2</span></span> | <span data-ttu-id="46d53-353">Sì</span><span class="sxs-lookup"><span data-stu-id="46d53-353">Yes</span></span>                                                          | <span data-ttu-id="46d53-354">2048</span><span class="sxs-lookup"><span data-stu-id="46d53-354">2048</span></span>                                | <span data-ttu-id="46d53-355">Sì</span><span class="sxs-lookup"><span data-stu-id="46d53-355">Yes</span></span>                                           | <span data-ttu-id="46d53-356">6</span><span class="sxs-lookup"><span data-stu-id="46d53-356">6</span></span>                                              | <span data-ttu-id="46d53-357">1</span><span class="sxs-lookup"><span data-stu-id="46d53-357">1</span></span>                                                  |
| <span data-ttu-id="46d53-358">\_Livello di funzionalità D3D \_ \_ 9 \_ 3</span><span class="sxs-lookup"><span data-stu-id="46d53-358">D3D\_FEATURE\_LEVEL\_9\_3</span></span> | <span data-ttu-id="46d53-359">Sì</span><span class="sxs-lookup"><span data-stu-id="46d53-359">Yes</span></span>                                                          | <span data-ttu-id="46d53-360">4096</span><span class="sxs-lookup"><span data-stu-id="46d53-360">4096</span></span>                                | <span data-ttu-id="46d53-361">Sì</span><span class="sxs-lookup"><span data-stu-id="46d53-361">Yes</span></span>                                           | <span data-ttu-id="46d53-362">6</span><span class="sxs-lookup"><span data-stu-id="46d53-362">6</span></span>                                              | <span data-ttu-id="46d53-363">1</span><span class="sxs-lookup"><span data-stu-id="46d53-363">1</span></span>                                                  |



 

<span data-ttu-id="46d53-364">Nella tabella precedente il nome completo di **varie \_ TEXTURECUBE** è [**d3d11 \_ Resource \_ varie \_ TEXTURECUBE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag).</span><span class="sxs-lookup"><span data-stu-id="46d53-364">In the previous table, the full name of **MISC\_TEXTURECUBE** is [**D3D11\_RESOURCE\_MISC\_TEXTURECUBE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag).</span></span>

<span data-ttu-id="46d53-365">Per tutti i 9 livelli di funzionalità sono soddisfatte le condizioni seguenti \_ \* [](overviews-direct3d-11-devices-downlevel-intro.md):</span><span class="sxs-lookup"><span data-stu-id="46d53-365">The following are true for all 9\_\* [feature levels](overviews-direct3d-11-devices-downlevel-intro.md):</span></span>

-   <span data-ttu-id="46d53-366">Quando si usa \_ il \_ valore predefinito di utilizzo D3D11 o l' \_ utilizzo \_ di d3d11 non è modificabile, BindFlags non può essere zero</span><span class="sxs-lookup"><span data-stu-id="46d53-366">When using D3D11\_USAGE\_DEFAULT or D3D11\_USAGE\_IMMUTABLE, BindFlags cannot be zero.</span></span>
-   <span data-ttu-id="46d53-367">Quando si usa \_ lo \_ \_ stencil di profondità di binding d3d11, MipLevels deve essere 1.</span><span class="sxs-lookup"><span data-stu-id="46d53-367">When using D3D11\_BIND\_DEPTH\_STENCIL, MipLevels must be 1.</span></span>
-   <span data-ttu-id="46d53-368">Quando si usa \_ la \_ risorsa shader bind d3d11 \_ , SampleDesc. Count deve essere 1.</span><span class="sxs-lookup"><span data-stu-id="46d53-368">When using D3D11\_BIND\_SHADER\_RESOURCE, SampleDesc.Count must be 1.</span></span>
-   <span data-ttu-id="46d53-369">Quando si usa il \_ Binding d3d11 \_ presente, la risorsa non può avere una \_ \_ risorsa shader bind d3d11 \_ .</span><span class="sxs-lookup"><span data-stu-id="46d53-369">When using D3D11\_BIND\_PRESENT, resource cannot have D3D11\_BIND\_SHADER\_RESOURCE.</span></span>
-   <span data-ttu-id="46d53-370">Quando si usa \_ la \_ risorsa D3D10 DDI \_ \_ Shared, il formato non può essere DXGI \_ Format \_ R8G8B8A8 \_ UNORM o DXGI \_ Format R8G8B8A8 \_ \_ UNORM \_ sRGB.</span><span class="sxs-lookup"><span data-stu-id="46d53-370">When using D3D10\_DDI\_RESOURCE\_MISC\_SHARED, Format cannot be DXGI\_FORMAT\_R8G8B8A8\_UNORM or DXGI\_FORMAT\_R8G8B8A8\_UNORM\_SRGB.</span></span>

## <a name="id3d11devicecreatetexture3d"></a><span data-ttu-id="46d53-371">ID3D11Device:: CreateTexture3D</span><span class="sxs-lookup"><span data-stu-id="46d53-371">ID3D11Device::CreateTexture3D</span></span>



| <span data-ttu-id="46d53-372">Livello funzionalità</span><span class="sxs-lookup"><span data-stu-id="46d53-372">Feature Level</span></span>             | <span data-ttu-id="46d53-373">Dimensione massima (qualsiasi asse)</span><span class="sxs-lookup"><span data-stu-id="46d53-373">Maximum Dimension (any axis)</span></span> | <span data-ttu-id="46d53-374">Le dimensioni devono essere una potenza di due</span><span class="sxs-lookup"><span data-stu-id="46d53-374">Dimensions must be power of two</span></span> |
|---------------------------|------------------------------|---------------------------------|
| <span data-ttu-id="46d53-375">\_Livello di funzionalità D3D \_ \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="46d53-375">D3D\_FEATURE\_LEVEL\_9\_1</span></span> | <span data-ttu-id="46d53-376">256</span><span class="sxs-lookup"><span data-stu-id="46d53-376">256</span></span>                          | <span data-ttu-id="46d53-377">Sì</span><span class="sxs-lookup"><span data-stu-id="46d53-377">Yes</span></span>                             |
| <span data-ttu-id="46d53-378">\_Livello di funzionalità D3D \_ \_ 9 \_ 2</span><span class="sxs-lookup"><span data-stu-id="46d53-378">D3D\_FEATURE\_LEVEL\_9\_2</span></span> | <span data-ttu-id="46d53-379">512</span><span class="sxs-lookup"><span data-stu-id="46d53-379">512</span></span>                          | <span data-ttu-id="46d53-380">Sì</span><span class="sxs-lookup"><span data-stu-id="46d53-380">Yes</span></span>                             |
| <span data-ttu-id="46d53-381">\_Livello di funzionalità D3D \_ \_ 9 \_ 3</span><span class="sxs-lookup"><span data-stu-id="46d53-381">D3D\_FEATURE\_LEVEL\_9\_3</span></span> | <span data-ttu-id="46d53-382">512</span><span class="sxs-lookup"><span data-stu-id="46d53-382">512</span></span>                          | <span data-ttu-id="46d53-383">Sì</span><span class="sxs-lookup"><span data-stu-id="46d53-383">Yes</span></span>                             |



 

<span data-ttu-id="46d53-384">Se la risorsa è \_ un \_ valore predefinito di utilizzo D3D11 o l' \_ utilizzo \_ di d3d11 non è modificabile, BindFlags non può essere zero.</span><span class="sxs-lookup"><span data-stu-id="46d53-384">If resource is D3D11\_USAGE\_DEFAULT or D3D11\_USAGE\_IMMUTABLE, BindFlags cannot be zero.</span></span>

## <a name="id3d11devicecreateunorderedaccessview"></a><span data-ttu-id="46d53-385">ID3D11Device:: CreateUnorderedAccessView</span><span class="sxs-lookup"><span data-stu-id="46d53-385">ID3D11Device::CreateUnorderedAccessView</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="46d53-386">Livello funzionalità</span><span class="sxs-lookup"><span data-stu-id="46d53-386">Feature Level</span></span></th>
<th><span data-ttu-id="46d53-387">Differenze di comportamento</span><span class="sxs-lookup"><span data-stu-id="46d53-387">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="46d53-388">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="46d53-388">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="46d53-389">Non supportato in alcun livello di funzionalità 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="46d53-389">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="46d53-390">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="46d53-390">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="46d53-391">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="46d53-391">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreatevertexshader"></a><span data-ttu-id="46d53-392">ID3D11Device:: CreateVertexShader</span><span class="sxs-lookup"><span data-stu-id="46d53-392">ID3D11Device::CreateVertexShader</span></span>



| <span data-ttu-id="46d53-393">Livello funzionalità</span><span class="sxs-lookup"><span data-stu-id="46d53-393">Feature Level</span></span>             | <span data-ttu-id="46d53-394">Differenze di comportamento</span><span class="sxs-lookup"><span data-stu-id="46d53-394">Behavior Differences</span></span>                                    |
|---------------------------|---------------------------------------------------------|
| <span data-ttu-id="46d53-395">\_Livello di funzionalità D3D \_ \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="46d53-395">D3D\_FEATURE\_LEVEL\_9\_1</span></span> | <span data-ttu-id="46d53-396">È necessario usare vs \_ 4 \_ 0 \_ livello \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="46d53-396">Must use vs\_4\_0\_level\_9\_1</span></span>                          |
| <span data-ttu-id="46d53-397">\_Livello di funzionalità D3D \_ \_ 9 \_ 2</span><span class="sxs-lookup"><span data-stu-id="46d53-397">D3D\_FEATURE\_LEVEL\_9\_2</span></span> | <span data-ttu-id="46d53-398">È necessario usare vs \_ 4 \_ 0 \_ livello \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="46d53-398">Must use vs\_4\_0\_level\_9\_1</span></span>                          |
| <span data-ttu-id="46d53-399">\_Livello di funzionalità D3D \_ \_ 9 \_ 3</span><span class="sxs-lookup"><span data-stu-id="46d53-399">D3D\_FEATURE\_LEVEL\_9\_3</span></span> | <span data-ttu-id="46d53-400">È necessario usare vs \_ 4 \_ 0 \_ livello \_ 9 \_ 3 o vs \_ 4 \_ 0 \_ livello \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="46d53-400">Must use vs\_4\_0\_level\_9\_3 or vs\_4\_0\_level\_9\_1</span></span> |



 

## <a name="id3d11deviceopensharedresource"></a><span data-ttu-id="46d53-401">ID3D11Device:: OpenSharedResource</span><span class="sxs-lookup"><span data-stu-id="46d53-401">ID3D11Device::OpenSharedResource</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="46d53-402">Livello funzionalità</span><span class="sxs-lookup"><span data-stu-id="46d53-402">Feature Level</span></span></th>
<th><span data-ttu-id="46d53-403">Differenze di comportamento</span><span class="sxs-lookup"><span data-stu-id="46d53-403">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="46d53-404">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="46d53-404">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"> <span data-ttu-id="46d53-405">Usare <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport"><strong>ID3D11Device:: CheckFeatureSupport</strong></a> con il valore <a href="/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature"><strong>D3D11_FEATURE_FORMAT_SUPPORT2</strong></a> e la struttura <a href="/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_format_support2"><strong>D3D11_FEATURE_DATA_FORMAT_SUPPORT2</strong></a> per determinare se un formato può essere condiviso.</span><span class="sxs-lookup"><span data-stu-id="46d53-405">Use <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport"><strong>ID3D11Device::CheckFeatureSupport</strong></a> with the <a href="/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature"><strong>D3D11_FEATURE_FORMAT_SUPPORT2</strong></a> value and the <a href="/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_format_support2"><strong>D3D11_FEATURE_DATA_FORMAT_SUPPORT2</strong></a> structure to determine if a format can be shared.</span></span> <span data-ttu-id="46d53-406">Se il formato può essere condiviso, <strong>CheckFeatureSupport</strong> restituisce il flag <a href="/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2_SHAREABLE</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="46d53-406">If the format can be shared, <strong>CheckFeatureSupport</strong> returns the <a href="/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2_SHAREABLE</strong></a> flag.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="46d53-407">[<strong>DXGI_FORMAT_R8G8B8A8_UNORM</strong>] (/Windows/Desktop/API/dxgiformat/ne-dxgiformat-dxgi_format) e <strong>DXGI_FORMAT_R8G8B8A8_UNORM_SRGB</strong> non sono mai condivisibili quando si usa il livello di funzionalità 9, anche se il dispositivo indica il supporto della funzionalità facoltativo per <strong>D3D11_FORMAT_SUPPORT_SHAREABLE</strong>.</span><span class="sxs-lookup"><span data-stu-id="46d53-407">[<strong>DXGI_FORMAT_R8G8B8A8_UNORM</strong>](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) and <strong>DXGI_FORMAT_R8G8B8A8_UNORM_SRGB</strong> are never shareable when using feature level 9, even if the device indicates optional feature support for <strong>D3D11_FORMAT_SUPPORT_SHAREABLE</strong>.</span></span> <span data-ttu-id="46d53-408">Il tentativo di creare risorse condivise con formati DXGI <strong>DXGI_FORMAT_R8G8B8A8_UNORM</strong> e <strong>DXGI_FORMAT_R8G8B8A8_UNORM_SRGB</strong> avrà sempre esito negativo a meno che il livello di funzionalità non sia 10_0 o superiore.</span><span class="sxs-lookup"><span data-stu-id="46d53-408">Attempting to create shared resources with DXGI formats <strong>DXGI_FORMAT_R8G8B8A8_UNORM</strong> and <strong>DXGI_FORMAT_R8G8B8A8_UNORM_SRGB</strong> will always fail unless the feature level is 10_0 or higher.</span></span>
</blockquote>
<br/> <span data-ttu-id="46d53-409">$ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="46d53-409">${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="46d53-410">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="46d53-410">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="46d53-411">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="46d53-411">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="46d53-412">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="46d53-412">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="46d53-413">Riferimento a 10Level9</span><span class="sxs-lookup"><span data-stu-id="46d53-413">10Level9 Reference</span></span>](d3d11-graphics-reference-10level9.md)
</dt> </dl>

 

