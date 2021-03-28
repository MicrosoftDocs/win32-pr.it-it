---
title: Metodi sul ID3D11DeviceContext di 10Level9
description: Questa sezione elenca le differenze tra ogni livello di funzionalità 10Level9 e il livello di funzionalità D3D \_ \_ \_ 11 \_ 0 e un livello di funzionalità superiore per i metodi sul ID3D11DeviceContext.
ms.assetid: 84478b56-0306-491a-9545-0849b06d8342
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb3dc46aeeb5d629c4bf50492083d09b34de1b08
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044250"
---
# <a name="10level9-id3d11devicecontext-methods"></a><span data-ttu-id="27534-103">Metodi sul ID3D11DeviceContext di 10Level9</span><span class="sxs-lookup"><span data-stu-id="27534-103">10Level9 ID3D11DeviceContext Methods</span></span>

<span data-ttu-id="27534-104">Questa sezione elenca le differenze tra ogni livello di funzionalità 10Level9 e il livello di funzionalità D3D \_ \_ \_ 11 \_ 0 e un livello di funzionalità superiore per i metodi [**sul ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) .</span><span class="sxs-lookup"><span data-stu-id="27534-104">This section lists the differences between each 10Level9 feature level and the D3D\_FEATURE\_LEVEL\_11\_0 and higher feature level for the [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) methods.</span></span>

-   [<span data-ttu-id="27534-105">Sul ID3D11DeviceContext:: CopySubresourceRegion</span><span class="sxs-lookup"><span data-stu-id="27534-105">ID3D11DeviceContext::CopySubresourceRegion</span></span>](#id3d11devicecontextcopysubresourceregion)
-   [<span data-ttu-id="27534-106">Sul ID3D11DeviceContext:: CopyResource</span><span class="sxs-lookup"><span data-stu-id="27534-106">ID3D11DeviceContext::CopyResource</span></span>](#id3d11devicecontextcopyresource)
-   [<span data-ttu-id="27534-107">Sul ID3D11DeviceContext:: CopyStructureCount</span><span class="sxs-lookup"><span data-stu-id="27534-107">ID3D11DeviceContext::CopyStructureCount</span></span>](#id3d11devicecontextcopystructurecount)
-   [<span data-ttu-id="27534-108">Sul ID3D11DeviceContext:: ClearUnorderedAccessViewFloat</span><span class="sxs-lookup"><span data-stu-id="27534-108">ID3D11DeviceContext::ClearUnorderedAccessViewFloat</span></span>](#id3d11devicecontextclearunorderedaccessviewfloat)
-   [<span data-ttu-id="27534-109">Sul ID3D11DeviceContext:: ClearUnorderedAccessViewUint</span><span class="sxs-lookup"><span data-stu-id="27534-109">ID3D11DeviceContext::ClearUnorderedAccessViewUint</span></span>](#id3d11devicecontextclearunorderedaccessviewuint)
-   [<span data-ttu-id="27534-110">Sul ID3D11DeviceContext:: ClearRenderTargetView</span><span class="sxs-lookup"><span data-stu-id="27534-110">ID3D11DeviceContext::ClearRenderTargetView</span></span>](#id3d11devicecontextclearrendertargetview)
-   [<span data-ttu-id="27534-111">Sul ID3D11DeviceContext:: CSSetConstantBuffers</span><span class="sxs-lookup"><span data-stu-id="27534-111">ID3D11DeviceContext::CSSetConstantBuffers</span></span>](#id3d11devicecontextcssetconstantbuffers)
-   [<span data-ttu-id="27534-112">Sul ID3D11DeviceContext:: CSSetSamplers</span><span class="sxs-lookup"><span data-stu-id="27534-112">ID3D11DeviceContext::CSSetSamplers</span></span>](#id3d11devicecontextcssetsamplers)
-   [<span data-ttu-id="27534-113">Sul ID3D11DeviceContext:: CSSetShader</span><span class="sxs-lookup"><span data-stu-id="27534-113">ID3D11DeviceContext::CSSetShader</span></span>](#id3d11devicecontextcssetshader)
-   [<span data-ttu-id="27534-114">Sul ID3D11DeviceContext:: CSSetShaderResources</span><span class="sxs-lookup"><span data-stu-id="27534-114">ID3D11DeviceContext::CSSetShaderResources</span></span>](#id3d11devicecontextcssetshaderresources)
-   [<span data-ttu-id="27534-115">Sul ID3D11DeviceContext:: CSSetUnorderedAccessViews</span><span class="sxs-lookup"><span data-stu-id="27534-115">ID3D11DeviceContext::CSSetUnorderedAccessViews</span></span>](#id3d11devicecontextcssetunorderedaccessviews)
-   [<span data-ttu-id="27534-116">Sul ID3D11DeviceContext::D patch</span><span class="sxs-lookup"><span data-stu-id="27534-116">ID3D11DeviceContext::Dispatch</span></span>](#id3d11devicecontextdispatch)
-   [<span data-ttu-id="27534-117">Sul ID3D11DeviceContext::D ispatchIndirect</span><span class="sxs-lookup"><span data-stu-id="27534-117">ID3D11DeviceContext::DispatchIndirect</span></span>](#id3d11devicecontextdispatchindirect)
-   [<span data-ttu-id="27534-118">Sul ID3D11DeviceContext::D RAW</span><span class="sxs-lookup"><span data-stu-id="27534-118">ID3D11DeviceContext::Draw</span></span>](#id3d11devicecontextdraw)
-   [<span data-ttu-id="27534-119">Sul ID3D11DeviceContext::D rawAuto</span><span class="sxs-lookup"><span data-stu-id="27534-119">ID3D11DeviceContext::DrawAuto</span></span>](#id3d11devicecontextdrawauto)
-   [<span data-ttu-id="27534-120">Sul ID3D11DeviceContext::D rawIndexed</span><span class="sxs-lookup"><span data-stu-id="27534-120">ID3D11DeviceContext::DrawIndexed</span></span>](#id3d11devicecontextdrawindexed)
-   [<span data-ttu-id="27534-121">Sul ID3D11DeviceContext::D rawIndexedInstanced</span><span class="sxs-lookup"><span data-stu-id="27534-121">ID3D11DeviceContext::DrawIndexedInstanced</span></span>](#id3d11devicecontextdrawindexedinstanced)
-   [<span data-ttu-id="27534-122">Sul ID3D11DeviceContext::D rawIndexedInstancedIndirect</span><span class="sxs-lookup"><span data-stu-id="27534-122">ID3D11DeviceContext::DrawIndexedInstancedIndirect</span></span>](#id3d11devicecontextdrawindexedinstancedindirect)
-   [<span data-ttu-id="27534-123">Sul ID3D11DeviceContext::D rawInstanced</span><span class="sxs-lookup"><span data-stu-id="27534-123">ID3D11DeviceContext::DrawInstanced</span></span>](#id3d11devicecontextdrawinstanced)
-   [<span data-ttu-id="27534-124">Sul ID3D11DeviceContext::D rawInstancedIndirect</span><span class="sxs-lookup"><span data-stu-id="27534-124">ID3D11DeviceContext::DrawInstancedIndirect</span></span>](#id3d11devicecontextdrawinstancedindirect)
-   [<span data-ttu-id="27534-125">Sul ID3D11DeviceContext::D SSetConstantBuffers</span><span class="sxs-lookup"><span data-stu-id="27534-125">ID3D11DeviceContext::DSSetConstantBuffers</span></span>](#id3d11devicecontextdssetconstantbuffers)
-   [<span data-ttu-id="27534-126">Sul ID3D11DeviceContext::D SSetSamplers</span><span class="sxs-lookup"><span data-stu-id="27534-126">ID3D11DeviceContext::DSSetSamplers</span></span>](#id3d11devicecontextdssetsamplers)
-   [<span data-ttu-id="27534-127">Sul ID3D11DeviceContext::D SSetShader</span><span class="sxs-lookup"><span data-stu-id="27534-127">ID3D11DeviceContext::DSSetShader</span></span>](#id3d11devicecontextdssetshader)
-   [<span data-ttu-id="27534-128">Sul ID3D11DeviceContext::D SSetShaderResources</span><span class="sxs-lookup"><span data-stu-id="27534-128">ID3D11DeviceContext::DSSetShaderResources</span></span>](#id3d11devicecontextdssetshaderresources)
-   [<span data-ttu-id="27534-129">Sul ID3D11DeviceContext:: GSSetConstantBuffers</span><span class="sxs-lookup"><span data-stu-id="27534-129">ID3D11DeviceContext::GSSetConstantBuffers</span></span>](#id3d11devicecontextgssetconstantbuffers)
-   [<span data-ttu-id="27534-130">Sul ID3D11DeviceContext:: GSSetSamplers</span><span class="sxs-lookup"><span data-stu-id="27534-130">ID3D11DeviceContext::GSSetSamplers</span></span>](#id3d11devicecontextgssetsamplers)
-   [<span data-ttu-id="27534-131">Sul ID3D11DeviceContext:: GSSetShader</span><span class="sxs-lookup"><span data-stu-id="27534-131">ID3D11DeviceContext::GSSetShader</span></span>](#id3d11devicecontextgssetshader)
-   [<span data-ttu-id="27534-132">Sul ID3D11DeviceContext:: GSSetShaderResources</span><span class="sxs-lookup"><span data-stu-id="27534-132">ID3D11DeviceContext::GSSetShaderResources</span></span>](#id3d11devicecontextgssetshaderresources)
-   [<span data-ttu-id="27534-133">Sul ID3D11DeviceContext:: HSSetConstantBuffers</span><span class="sxs-lookup"><span data-stu-id="27534-133">ID3D11DeviceContext::HSSetConstantBuffers</span></span>](#id3d11devicecontexthssetconstantbuffers)
-   [<span data-ttu-id="27534-134">Sul ID3D11DeviceContext:: HSSetSamplers</span><span class="sxs-lookup"><span data-stu-id="27534-134">ID3D11DeviceContext::HSSetSamplers</span></span>](#id3d11devicecontexthssetsamplers)
-   [<span data-ttu-id="27534-135">Sul ID3D11DeviceContext:: HSSetShader</span><span class="sxs-lookup"><span data-stu-id="27534-135">ID3D11DeviceContext::HSSetShader</span></span>](#id3d11devicecontexthssetshader)
-   [<span data-ttu-id="27534-136">Sul ID3D11DeviceContext:: HSSetShaderResources</span><span class="sxs-lookup"><span data-stu-id="27534-136">ID3D11DeviceContext::HSSetShaderResources</span></span>](#id3d11devicecontexthssetshaderresources)
-   [<span data-ttu-id="27534-137">ID3D11DeviceContext::IASetIndexBuffer</span><span class="sxs-lookup"><span data-stu-id="27534-137">ID3D11DeviceContext::IASetIndexBuffer</span></span>](#id3d11devicecontextiasetindexbuffer)
-   [<span data-ttu-id="27534-138">Sul ID3D11DeviceContext:: IASetPrimitiveTopology</span><span class="sxs-lookup"><span data-stu-id="27534-138">ID3D11DeviceContext::IASetPrimitiveTopology</span></span>](#id3d11devicecontextiasetprimitivetopology)
-   [<span data-ttu-id="27534-139">Sul ID3D11DeviceContext:: OMSetBlendState</span><span class="sxs-lookup"><span data-stu-id="27534-139">ID3D11DeviceContext::OMSetBlendState</span></span>](#id3d11devicecontextomsetblendstate)
-   [<span data-ttu-id="27534-140">Sul ID3D11DeviceContext:: OMSetRenderTargets</span><span class="sxs-lookup"><span data-stu-id="27534-140">ID3D11DeviceContext::OMSetRenderTargets</span></span>](#id3d11devicecontextomsetrendertargets)
-   [<span data-ttu-id="27534-141">Sul ID3D11DeviceContext:: OMSetRenderTargetsAndUnorderedAccessViews</span><span class="sxs-lookup"><span data-stu-id="27534-141">ID3D11DeviceContext::OMSetRenderTargetsAndUnorderedAccessViews</span></span>](#id3d11devicecontextomsetrendertargetsandunorderedaccessviews)
-   [<span data-ttu-id="27534-142">Sul ID3D11DeviceContext::P SSetConstantBuffers</span><span class="sxs-lookup"><span data-stu-id="27534-142">ID3D11DeviceContext::PSSetConstantBuffers</span></span>](#id3d11devicecontextpssetconstantbuffers)
-   [<span data-ttu-id="27534-143">Sul ID3D11DeviceContext::P SSetSamplers</span><span class="sxs-lookup"><span data-stu-id="27534-143">ID3D11DeviceContext::PSSetSamplers</span></span>](#id3d11devicecontextpssetsamplers)
-   [<span data-ttu-id="27534-144">Sul ID3D11DeviceContext::P SSetShader</span><span class="sxs-lookup"><span data-stu-id="27534-144">ID3D11DeviceContext::PSSetShader</span></span>](#id3d11devicecontextpssetshader)
-   [<span data-ttu-id="27534-145">Sul ID3D11DeviceContext::P SSetShaderResources</span><span class="sxs-lookup"><span data-stu-id="27534-145">ID3D11DeviceContext::PSSetShaderResources</span></span>](#id3d11devicecontextpssetshaderresources)
-   [<span data-ttu-id="27534-146">Sul ID3D11DeviceContext:: RSSetScissorRects</span><span class="sxs-lookup"><span data-stu-id="27534-146">ID3D11DeviceContext::RSSetScissorRects</span></span>](#id3d11devicecontextrssetscissorrects)
-   [<span data-ttu-id="27534-147">Sul ID3D11DeviceContext:: RSSetViewports</span><span class="sxs-lookup"><span data-stu-id="27534-147">ID3D11DeviceContext::RSSetViewports</span></span>](#id3d11devicecontextrssetviewports)
-   [<span data-ttu-id="27534-148">Sul ID3D11DeviceContext:: SetPredication</span><span class="sxs-lookup"><span data-stu-id="27534-148">ID3D11DeviceContext::SetPredication</span></span>](#id3d11devicecontextsetpredication)
-   [<span data-ttu-id="27534-149">Sul ID3D11DeviceContext:: SOSetTargets</span><span class="sxs-lookup"><span data-stu-id="27534-149">ID3D11DeviceContext::SOSetTargets</span></span>](#id3d11devicecontextsosettargets)
-   [<span data-ttu-id="27534-150">Sul ID3D11DeviceContext:: VSSetConstantBuffers</span><span class="sxs-lookup"><span data-stu-id="27534-150">ID3D11DeviceContext::VSSetConstantBuffers</span></span>](#id3d11devicecontextvssetconstantbuffers)
-   [<span data-ttu-id="27534-151">Sul ID3D11DeviceContext:: VSSetSamplers</span><span class="sxs-lookup"><span data-stu-id="27534-151">ID3D11DeviceContext::VSSetSamplers</span></span>](#id3d11devicecontextvssetsamplers)
-   [<span data-ttu-id="27534-152">Sul ID3D11DeviceContext:: VSSetShader</span><span class="sxs-lookup"><span data-stu-id="27534-152">ID3D11DeviceContext::VSSetShader</span></span>](#id3d11devicecontextvssetshader)
-   [<span data-ttu-id="27534-153">Sul ID3D11DeviceContext:: VSSetShaderResources</span><span class="sxs-lookup"><span data-stu-id="27534-153">ID3D11DeviceContext::VSSetShaderResources</span></span>](#id3d11devicecontextvssetshaderresources)
-   [<span data-ttu-id="27534-154">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="27534-154">Related topics</span></span>](#related-topics)

## <a name="id3d11devicecontextcopysubresourceregion"></a><span data-ttu-id="27534-155">Sul ID3D11DeviceContext:: CopySubresourceRegion</span><span class="sxs-lookup"><span data-stu-id="27534-155">ID3D11DeviceContext::CopySubresourceRegion</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="27534-156">Livello funzionalità</span><span class="sxs-lookup"><span data-stu-id="27534-156">Feature Level</span></span></th>
<th><span data-ttu-id="27534-157">Differenze di comportamento</span><span class="sxs-lookup"><span data-stu-id="27534-157">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="27534-158">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="27534-158">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"> <span data-ttu-id="27534-159">Solo Texture2D e buffer possono essere copiati nella memoria accessibile dalla GPU.</span><span class="sxs-lookup"><span data-stu-id="27534-159">Only Texture2D and buffers may be copied within GPU-accessible memory.</span></span><br/> <span data-ttu-id="27534-160">Non è possibile copiare Texture3D dalla memoria accessibile dalla GPU alla memoria accessibile dalla CPU.</span><span class="sxs-lookup"><span data-stu-id="27534-160">Texture3D cannot be copied from GPU-accessible memory to CPU-accessible memory.</span></span><br/> <span data-ttu-id="27534-161">Tutte le risorse che hanno solo D3D10_BIND_SHADER_RESOURCE non possono essere copiate dalla memoria accessibile dalla GPU alla memoria accessibile dalla CPU.</span><span class="sxs-lookup"><span data-stu-id="27534-161">Any resource that has only D3D10_BIND_SHADER_RESOURCE cannot be copied from GPU-accessible memory to CPU-accessible memory.</span></span><br/> <span data-ttu-id="27534-162">Non è possibile copiare le trame del volume mipmap.</span><span class="sxs-lookup"><span data-stu-id="27534-162">You can't copy mipmapped volume textures.</span></span> <br/> <span data-ttu-id="27534-163">$ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="27534-163">${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="27534-164">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="27534-164">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="27534-165">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="27534-165">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextcopyresource"></a><span data-ttu-id="27534-166">Sul ID3D11DeviceContext:: CopyResource</span><span class="sxs-lookup"><span data-stu-id="27534-166">ID3D11DeviceContext::CopyResource</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="27534-167">Livello funzionalità</span><span class="sxs-lookup"><span data-stu-id="27534-167">Feature Level</span></span></th>
<th><span data-ttu-id="27534-168">Differenze di comportamento</span><span class="sxs-lookup"><span data-stu-id="27534-168">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="27534-169">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="27534-169">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"> <span data-ttu-id="27534-170">Solo Texture2D e buffer possono essere copiati nella memoria accessibile dalla GPU.</span><span class="sxs-lookup"><span data-stu-id="27534-170">Only Texture2D and buffers may be copied within GPU-accessible memory.</span></span><br/> <span data-ttu-id="27534-171">Non è possibile copiare Texture3D dalla memoria accessibile dalla GPU alla memoria accessibile dalla CPU.</span><span class="sxs-lookup"><span data-stu-id="27534-171">Texture3D cannot be copied from GPU-accessible memory to CPU-accessible memory.</span></span><br/> <span data-ttu-id="27534-172">Tutte le risorse che hanno solo D3D10_BIND_SHADER_RESOURCE non possono essere copiate dalla memoria accessibile dalla GPU alla memoria accessibile dalla CPU.</span><span class="sxs-lookup"><span data-stu-id="27534-172">Any resource that has only D3D10_BIND_SHADER_RESOURCE cannot be copied from GPU-accessible memory to CPU-accessible memory.</span></span><br/> <span data-ttu-id="27534-173">$ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="27534-173">${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="27534-174">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="27534-174">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="27534-175">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="27534-175">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextcopystructurecount"></a><span data-ttu-id="27534-176">Sul ID3D11DeviceContext:: CopyStructureCount</span><span class="sxs-lookup"><span data-stu-id="27534-176">ID3D11DeviceContext::CopyStructureCount</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="27534-177">Livello funzionalità</span><span class="sxs-lookup"><span data-stu-id="27534-177">Feature Level</span></span></th>
<th><span data-ttu-id="27534-178">Differenze di comportamento</span><span class="sxs-lookup"><span data-stu-id="27534-178">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="27534-179">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="27534-179">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="27534-180">Non supportato in alcun livello di funzionalità 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="27534-180">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="27534-181">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="27534-181">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="27534-182">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="27534-182">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextclearunorderedaccessviewfloat"></a><span data-ttu-id="27534-183">Sul ID3D11DeviceContext:: ClearUnorderedAccessViewFloat</span><span class="sxs-lookup"><span data-stu-id="27534-183">ID3D11DeviceContext::ClearUnorderedAccessViewFloat</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="27534-184">Livello funzionalità</span><span class="sxs-lookup"><span data-stu-id="27534-184">Feature Level</span></span></th>
<th><span data-ttu-id="27534-185">Differenze di comportamento</span><span class="sxs-lookup"><span data-stu-id="27534-185">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="27534-186">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="27534-186">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="27534-187">Non supportato in alcun livello di funzionalità 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="27534-187">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="27534-188">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="27534-188">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="27534-189">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="27534-189">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextclearunorderedaccessviewuint"></a><span data-ttu-id="27534-190">Sul ID3D11DeviceContext:: ClearUnorderedAccessViewUint</span><span class="sxs-lookup"><span data-stu-id="27534-190">ID3D11DeviceContext::ClearUnorderedAccessViewUint</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="27534-191">Livello funzionalità</span><span class="sxs-lookup"><span data-stu-id="27534-191">Feature Level</span></span></th>
<th><span data-ttu-id="27534-192">Differenze di comportamento</span><span class="sxs-lookup"><span data-stu-id="27534-192">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="27534-193">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="27534-193">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="27534-194">Non supportato in alcun livello di funzionalità 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="27534-194">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="27534-195">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="27534-195">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="27534-196">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="27534-196">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextclearrendertargetview"></a><span data-ttu-id="27534-197">Sul ID3D11DeviceContext:: ClearRenderTargetView</span><span class="sxs-lookup"><span data-stu-id="27534-197">ID3D11DeviceContext::ClearRenderTargetView</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="27534-198">Livello funzionalità</span><span class="sxs-lookup"><span data-stu-id="27534-198">Feature Level</span></span></th>
<th><span data-ttu-id="27534-199">Differenze di comportamento</span><span class="sxs-lookup"><span data-stu-id="27534-199">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="27534-200">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="27534-200">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="27534-201">Solo la prima sezione della matrice verrà cancellata.</span><span class="sxs-lookup"><span data-stu-id="27534-201">Only the first array slice will be cleared.</span></span> <span data-ttu-id="27534-202">Le applicazioni devono creare una visualizzazione della destinazione di rendering per ogni sezione della faccia o della matrice, quindi deselezionare singolarmente ogni visualizzazione. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="27534-202">Applications should create a render target view for each face or array slice, then clear each view individually.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="27534-203">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="27534-203">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="27534-204">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="27534-204">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextcssetconstantbuffers"></a><span data-ttu-id="27534-205">Sul ID3D11DeviceContext:: CSSetConstantBuffers</span><span class="sxs-lookup"><span data-stu-id="27534-205">ID3D11DeviceContext::CSSetConstantBuffers</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="27534-206">Livello funzionalità</span><span class="sxs-lookup"><span data-stu-id="27534-206">Feature Level</span></span></th>
<th><span data-ttu-id="27534-207">Differenze di comportamento</span><span class="sxs-lookup"><span data-stu-id="27534-207">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="27534-208">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="27534-208">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="27534-209">Non supportato in alcun livello di funzionalità 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="27534-209">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="27534-210">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="27534-210">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="27534-211">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="27534-211">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextcssetsamplers"></a><span data-ttu-id="27534-212">Sul ID3D11DeviceContext:: CSSetSamplers</span><span class="sxs-lookup"><span data-stu-id="27534-212">ID3D11DeviceContext::CSSetSamplers</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="27534-213">Livello funzionalità</span><span class="sxs-lookup"><span data-stu-id="27534-213">Feature Level</span></span></th>
<th><span data-ttu-id="27534-214">Differenze di comportamento</span><span class="sxs-lookup"><span data-stu-id="27534-214">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="27534-215">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="27534-215">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="27534-216">Non supportato in alcun livello di funzionalità 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="27534-216">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="27534-217">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="27534-217">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="27534-218">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="27534-218">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextcssetshader"></a><span data-ttu-id="27534-219">Sul ID3D11DeviceContext:: CSSetShader</span><span class="sxs-lookup"><span data-stu-id="27534-219">ID3D11DeviceContext::CSSetShader</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="27534-220">Livello funzionalità</span><span class="sxs-lookup"><span data-stu-id="27534-220">Feature Level</span></span></th>
<th><span data-ttu-id="27534-221">Differenze di comportamento</span><span class="sxs-lookup"><span data-stu-id="27534-221">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="27534-222">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="27534-222">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="27534-223">Non supportato in alcun livello di funzionalità 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="27534-223">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="27534-224">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="27534-224">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="27534-225">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="27534-225">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextcssetshaderresources"></a><span data-ttu-id="27534-226">Sul ID3D11DeviceContext:: CSSetShaderResources</span><span class="sxs-lookup"><span data-stu-id="27534-226">ID3D11DeviceContext::CSSetShaderResources</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="27534-227">Livello funzionalità</span><span class="sxs-lookup"><span data-stu-id="27534-227">Feature Level</span></span></th>
<th><span data-ttu-id="27534-228">Differenze di comportamento</span><span class="sxs-lookup"><span data-stu-id="27534-228">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="27534-229">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="27534-229">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="27534-230">Non supportato in alcun livello di funzionalità 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="27534-230">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="27534-231">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="27534-231">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="27534-232">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="27534-232">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextcssetunorderedaccessviews"></a><span data-ttu-id="27534-233">Sul ID3D11DeviceContext:: CSSetUnorderedAccessViews</span><span class="sxs-lookup"><span data-stu-id="27534-233">ID3D11DeviceContext::CSSetUnorderedAccessViews</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="27534-234">Livello funzionalità</span><span class="sxs-lookup"><span data-stu-id="27534-234">Feature Level</span></span></th>
<th><span data-ttu-id="27534-235">Differenze di comportamento</span><span class="sxs-lookup"><span data-stu-id="27534-235">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="27534-236">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="27534-236">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="27534-237">Non supportato in alcun livello di funzionalità 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="27534-237">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="27534-238">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="27534-238">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="27534-239">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="27534-239">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdispatch"></a><span data-ttu-id="27534-240">Sul ID3D11DeviceContext::D patch</span><span class="sxs-lookup"><span data-stu-id="27534-240">ID3D11DeviceContext::Dispatch</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="27534-241">Livello funzionalità</span><span class="sxs-lookup"><span data-stu-id="27534-241">Feature Level</span></span></th>
<th><span data-ttu-id="27534-242">Differenze di comportamento</span><span class="sxs-lookup"><span data-stu-id="27534-242">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="27534-243">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="27534-243">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="27534-244">Non supportato in alcun livello di funzionalità 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="27534-244">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="27534-245">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="27534-245">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="27534-246">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="27534-246">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdispatchindirect"></a><span data-ttu-id="27534-247">Sul ID3D11DeviceContext::D ispatchIndirect</span><span class="sxs-lookup"><span data-stu-id="27534-247">ID3D11DeviceContext::DispatchIndirect</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="27534-248">Livello funzionalità</span><span class="sxs-lookup"><span data-stu-id="27534-248">Feature Level</span></span></th>
<th><span data-ttu-id="27534-249">Differenze di comportamento</span><span class="sxs-lookup"><span data-stu-id="27534-249">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="27534-250">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="27534-250">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="27534-251">Non supportato in alcun livello di funzionalità 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="27534-251">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="27534-252">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="27534-252">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="27534-253">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="27534-253">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdraw"></a><span data-ttu-id="27534-254">Sul ID3D11DeviceContext::D RAW</span><span class="sxs-lookup"><span data-stu-id="27534-254">ID3D11DeviceContext::Draw</span></span>



| <span data-ttu-id="27534-255">Livello funzionalità</span><span class="sxs-lookup"><span data-stu-id="27534-255">Feature Level</span></span>             | <span data-ttu-id="27534-256">Differenze di comportamento</span><span class="sxs-lookup"><span data-stu-id="27534-256">Behavior Differences</span></span>                                                                                                               |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27534-257">\_Livello di funzionalità D3D \_ \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="27534-257">D3D\_FEATURE\_LEVEL\_9\_1</span></span> | <span data-ttu-id="27534-258">Il numero di primitive non può essere maggiore di 65535.</span><span class="sxs-lookup"><span data-stu-id="27534-258">Number of primitives may not exceed 65535.</span></span><br/> <span data-ttu-id="27534-259">Le trame non possono essere ripetute su una primitiva più di 128 volte.</span><span class="sxs-lookup"><span data-stu-id="27534-259">Textures cannot repeat over one primitive more than 128 times.</span></span><br/>    |
| <span data-ttu-id="27534-260">\_Livello di funzionalità D3D \_ \_ 9 \_ 2</span><span class="sxs-lookup"><span data-stu-id="27534-260">D3D\_FEATURE\_LEVEL\_9\_2</span></span> | <span data-ttu-id="27534-261">Il numero di primitive non può essere maggiore di 1048575.</span><span class="sxs-lookup"><span data-stu-id="27534-261">Number of primitives may not exceed 1048575.</span></span><br/> <span data-ttu-id="27534-262">Le trame non possono essere ripetute su una primitiva più di 2048 volte.</span><span class="sxs-lookup"><span data-stu-id="27534-262">Textures cannot repeat over one primitive more than 2048 times.</span></span><br/> |
| <span data-ttu-id="27534-263">\_Livello di funzionalità D3D \_ \_ 9 \_ 3</span><span class="sxs-lookup"><span data-stu-id="27534-263">D3D\_FEATURE\_LEVEL\_9\_3</span></span> | <span data-ttu-id="27534-264">Il numero di primitive non può essere maggiore di 1048575.</span><span class="sxs-lookup"><span data-stu-id="27534-264">Number of primitives may not exceed 1048575.</span></span><br/> <span data-ttu-id="27534-265">Le trame non possono essere ripetute su una primitiva più di 8192 volte.</span><span class="sxs-lookup"><span data-stu-id="27534-265">Textures cannot repeat over one primitive more than 8192 times.</span></span><br/> |



 

## <a name="id3d11devicecontextdrawauto"></a><span data-ttu-id="27534-266">Sul ID3D11DeviceContext::D rawAuto</span><span class="sxs-lookup"><span data-stu-id="27534-266">ID3D11DeviceContext::DrawAuto</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="27534-267">Livello funzionalità</span><span class="sxs-lookup"><span data-stu-id="27534-267">Feature Level</span></span></th>
<th><span data-ttu-id="27534-268">Differenze di comportamento</span><span class="sxs-lookup"><span data-stu-id="27534-268">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="27534-269">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="27534-269">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="27534-270">Non supportato in alcun livello di funzionalità 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="27534-270">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="27534-271">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="27534-271">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="27534-272">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="27534-272">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdrawindexed"></a><span data-ttu-id="27534-273">Sul ID3D11DeviceContext::D rawIndexed</span><span class="sxs-lookup"><span data-stu-id="27534-273">ID3D11DeviceContext::DrawIndexed</span></span>



| <span data-ttu-id="27534-274">Livello funzionalità</span><span class="sxs-lookup"><span data-stu-id="27534-274">Feature Level</span></span>             | <span data-ttu-id="27534-275">Differenze di comportamento</span><span class="sxs-lookup"><span data-stu-id="27534-275">Behavior Differences</span></span>                                                                                                                                                                                                            |
|---------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27534-276">\_Livello di funzionalità D3D \_ \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="27534-276">D3D\_FEATURE\_LEVEL\_9\_1</span></span> | <span data-ttu-id="27534-277">Il numero di primitive non può essere maggiore di 65535.</span><span class="sxs-lookup"><span data-stu-id="27534-277">Number of primitives may not exceed 65535.</span></span><br/> <span data-ttu-id="27534-278">Le trame non possono essere ripetute su una primitiva più di 128 volte.</span><span class="sxs-lookup"><span data-stu-id="27534-278">Textures cannot repeat over one primitive more than 128 times.</span></span><br/> <span data-ttu-id="27534-279">I valori di indice non possono superare 65534.</span><span class="sxs-lookup"><span data-stu-id="27534-279">Index values cannot exceed 65534.</span></span><br/> <span data-ttu-id="27534-280">Gli elenchi di punti indicizzati non sono supportati.</span><span class="sxs-lookup"><span data-stu-id="27534-280">Indexed point lists not supported.</span></span><br/>      |
| <span data-ttu-id="27534-281">\_Livello di funzionalità D3D \_ \_ 9 \_ 2</span><span class="sxs-lookup"><span data-stu-id="27534-281">D3D\_FEATURE\_LEVEL\_9\_2</span></span> | <span data-ttu-id="27534-282">Il numero di primitive non può essere maggiore di 1048575.</span><span class="sxs-lookup"><span data-stu-id="27534-282">Number of primitives may not exceed 1048575.</span></span><br/> <span data-ttu-id="27534-283">Le trame non possono essere ripetute su una primitiva più di 2048 volte.</span><span class="sxs-lookup"><span data-stu-id="27534-283">Textures cannot repeat over one primitive more than 2048 times.</span></span><br/> <span data-ttu-id="27534-284">I valori di indice non possono superare 1048575.</span><span class="sxs-lookup"><span data-stu-id="27534-284">Index values cannot exceed 1048575.</span></span><br/> <span data-ttu-id="27534-285">Gli elenchi di punti indicizzati non sono supportati.</span><span class="sxs-lookup"><span data-stu-id="27534-285">Indexed point lists not supported.</span></span><br/> |
| <span data-ttu-id="27534-286">\_Livello di funzionalità D3D \_ \_ 9 \_ 3</span><span class="sxs-lookup"><span data-stu-id="27534-286">D3D\_FEATURE\_LEVEL\_9\_3</span></span> | <span data-ttu-id="27534-287">Il numero di primitive non può essere maggiore di 1048575.</span><span class="sxs-lookup"><span data-stu-id="27534-287">Number of primitives may not exceed 1048575.</span></span><br/> <span data-ttu-id="27534-288">Le trame non possono essere ripetute su una primitiva più di 8192 volte.</span><span class="sxs-lookup"><span data-stu-id="27534-288">Textures cannot repeat over one primitive more than 8192 times.</span></span><br/> <span data-ttu-id="27534-289">I valori di indice non possono superare 1048575.</span><span class="sxs-lookup"><span data-stu-id="27534-289">Index values cannot exceed 1048575.</span></span><br/> <span data-ttu-id="27534-290">Gli elenchi di punti indicizzati non sono supportati.</span><span class="sxs-lookup"><span data-stu-id="27534-290">Indexed point lists not supported.</span></span><br/> |



 

## <a name="id3d11devicecontextdrawindexedinstanced"></a><span data-ttu-id="27534-291">Sul ID3D11DeviceContext::D rawIndexedInstanced</span><span class="sxs-lookup"><span data-stu-id="27534-291">ID3D11DeviceContext::DrawIndexedInstanced</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="27534-292">Livello funzionalità</span><span class="sxs-lookup"><span data-stu-id="27534-292">Feature Level</span></span></th>
<th><span data-ttu-id="27534-293">Differenze di comportamento</span><span class="sxs-lookup"><span data-stu-id="27534-293">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="27534-294">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="27534-294">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="2"><span data-ttu-id="27534-295">Non supportato $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="27534-295">Not supported${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="27534-296">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="27534-296">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="27534-297">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="27534-297">D3D_FEATURE_LEVEL_9_3</span></span></td>
<td><span data-ttu-id="27534-298">Il numero di primitive non può essere maggiore di 1048575.</span><span class="sxs-lookup"><span data-stu-id="27534-298">Number of primitives may not exceed 1048575.</span></span><br/> <span data-ttu-id="27534-299">Le trame non possono essere ripetute su una primitiva più di 8192 volte.</span><span class="sxs-lookup"><span data-stu-id="27534-299">Textures cannot repeat over one primitive more than 8192 times.</span></span><br/> <span data-ttu-id="27534-300">I valori di indice non possono superare 1048575.</span><span class="sxs-lookup"><span data-stu-id="27534-300">Index values cannot exceed 1048575.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="27534-301">Quando si chiama il metodo <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexedinstanced"><strong>DrawIndexedInstanced</strong></a> con un vertex shader associato alla pipeline e che non importa dati per istanza, è possibile che alcuni componenti hardware della grafica Direct3D 9 non disegnino nulla.</span><span class="sxs-lookup"><span data-stu-id="27534-301">When you call the <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexedinstanced"><strong>DrawIndexedInstanced</strong></a> method with a vertex shader that is bound to the pipeline and that doesn't import any per-instance data, some Direct3D 9 graphics hardware might not draw anything.</span></span> <span data-ttu-id="27534-302">In particolare, se il vertex shader non utilizza dati per istanza, la chiamata a <strong>DrawIndexedInstanced</strong> con 1 istanza non è equivalente alla chiamata di di <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-draw"><strong>estrazione</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="27534-302">In particular, if the vertex shader does not use any per-instance data, calling <strong>DrawIndexedInstanced</strong> with 1 instance is not equivalent to calling <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-draw"><strong>Draw</strong></a>.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdrawindexedinstancedindirect"></a><span data-ttu-id="27534-303">Sul ID3D11DeviceContext::D rawIndexedInstancedIndirect</span><span class="sxs-lookup"><span data-stu-id="27534-303">ID3D11DeviceContext::DrawIndexedInstancedIndirect</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="27534-304">Livello funzionalità</span><span class="sxs-lookup"><span data-stu-id="27534-304">Feature Level</span></span></th>
<th><span data-ttu-id="27534-305">Differenze di comportamento</span><span class="sxs-lookup"><span data-stu-id="27534-305">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="27534-306">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="27534-306">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="5"><span data-ttu-id="27534-307">Non supportato in alcun livello di funzionalità 9. \* o 10. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="27534-307">Not supported on any 9.\* or 10.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="27534-308">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="27534-308">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="27534-309">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="27534-309">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="27534-310">D3D_FEATURE_LEVEL_10_0</span><span class="sxs-lookup"><span data-stu-id="27534-310">D3D_FEATURE_LEVEL_10_0</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="27534-311">D3D_FEATURE_LEVEL_10_1</span><span class="sxs-lookup"><span data-stu-id="27534-311">D3D_FEATURE_LEVEL_10_1</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdrawinstanced"></a><span data-ttu-id="27534-312">Sul ID3D11DeviceContext::D rawInstanced</span><span class="sxs-lookup"><span data-stu-id="27534-312">ID3D11DeviceContext::DrawInstanced</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="27534-313">Livello funzionalità</span><span class="sxs-lookup"><span data-stu-id="27534-313">Feature Level</span></span></th>
<th><span data-ttu-id="27534-314">Differenze di comportamento</span><span class="sxs-lookup"><span data-stu-id="27534-314">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="27534-315">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="27534-315">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="27534-316">Non supportato in alcun livello di funzionalità 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="27534-316">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="27534-317">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="27534-317">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="27534-318">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="27534-318">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdrawinstancedindirect"></a><span data-ttu-id="27534-319">Sul ID3D11DeviceContext::D rawInstancedIndirect</span><span class="sxs-lookup"><span data-stu-id="27534-319">ID3D11DeviceContext::DrawInstancedIndirect</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="27534-320">Livello funzionalità</span><span class="sxs-lookup"><span data-stu-id="27534-320">Feature Level</span></span></th>
<th><span data-ttu-id="27534-321">Differenze di comportamento</span><span class="sxs-lookup"><span data-stu-id="27534-321">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="27534-322">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="27534-322">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="5"><span data-ttu-id="27534-323">Non supportato in alcun livello di funzionalità 9. \* o 10. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="27534-323">Not supported on any 9.\* or 10.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="27534-324">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="27534-324">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="27534-325">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="27534-325">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="27534-326">D3D_FEATURE_LEVEL_10_0</span><span class="sxs-lookup"><span data-stu-id="27534-326">D3D_FEATURE_LEVEL_10_0</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="27534-327">D3D_FEATURE_LEVEL_10_1</span><span class="sxs-lookup"><span data-stu-id="27534-327">D3D_FEATURE_LEVEL_10_1</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdssetconstantbuffers"></a><span data-ttu-id="27534-328">Sul ID3D11DeviceContext::D SSetConstantBuffers</span><span class="sxs-lookup"><span data-stu-id="27534-328">ID3D11DeviceContext::DSSetConstantBuffers</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="27534-329">Livello funzionalità</span><span class="sxs-lookup"><span data-stu-id="27534-329">Feature Level</span></span></th>
<th><span data-ttu-id="27534-330">Differenze di comportamento</span><span class="sxs-lookup"><span data-stu-id="27534-330">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="27534-331">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="27534-331">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="5"><span data-ttu-id="27534-332">Non supportato in alcun livello di funzionalità 9. \* o 10. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="27534-332">Not supported on any 9.\* or 10.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="27534-333">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="27534-333">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="27534-334">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="27534-334">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="27534-335">D3D_FEATURE_LEVEL_10_0</span><span class="sxs-lookup"><span data-stu-id="27534-335">D3D_FEATURE_LEVEL_10_0</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="27534-336">D3D_FEATURE_LEVEL_10_1</span><span class="sxs-lookup"><span data-stu-id="27534-336">D3D_FEATURE_LEVEL_10_1</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdssetsamplers"></a><span data-ttu-id="27534-337">Sul ID3D11DeviceContext::D SSetSamplers</span><span class="sxs-lookup"><span data-stu-id="27534-337">ID3D11DeviceContext::DSSetSamplers</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="27534-338">Livello funzionalità</span><span class="sxs-lookup"><span data-stu-id="27534-338">Feature Level</span></span></th>
<th><span data-ttu-id="27534-339">Differenze di comportamento</span><span class="sxs-lookup"><span data-stu-id="27534-339">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="27534-340">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="27534-340">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="5"><span data-ttu-id="27534-341">Non supportato in alcun livello di funzionalità 9. \* o 10. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="27534-341">Not supported on any 9.\* or 10.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="27534-342">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="27534-342">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="27534-343">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="27534-343">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="27534-344">D3D_FEATURE_LEVEL_10_0</span><span class="sxs-lookup"><span data-stu-id="27534-344">D3D_FEATURE_LEVEL_10_0</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="27534-345">D3D_FEATURE_LEVEL_10_1</span><span class="sxs-lookup"><span data-stu-id="27534-345">D3D_FEATURE_LEVEL_10_1</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdssetshader"></a><span data-ttu-id="27534-346">Sul ID3D11DeviceContext::D SSetShader</span><span class="sxs-lookup"><span data-stu-id="27534-346">ID3D11DeviceContext::DSSetShader</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="27534-347">Livello funzionalità</span><span class="sxs-lookup"><span data-stu-id="27534-347">Feature Level</span></span></th>
<th><span data-ttu-id="27534-348">Differenze di comportamento</span><span class="sxs-lookup"><span data-stu-id="27534-348">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="27534-349">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="27534-349">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="5"><span data-ttu-id="27534-350">Non supportato in alcun livello di funzionalità 9. \* o 10. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="27534-350">Not supported on any 9.\* or 10.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="27534-351">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="27534-351">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="27534-352">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="27534-352">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="27534-353">D3D_FEATURE_LEVEL_10_0</span><span class="sxs-lookup"><span data-stu-id="27534-353">D3D_FEATURE_LEVEL_10_0</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="27534-354">D3D_FEATURE_LEVEL_10_1</span><span class="sxs-lookup"><span data-stu-id="27534-354">D3D_FEATURE_LEVEL_10_1</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdssetshaderresources"></a><span data-ttu-id="27534-355">Sul ID3D11DeviceContext::D SSetShaderResources</span><span class="sxs-lookup"><span data-stu-id="27534-355">ID3D11DeviceContext::DSSetShaderResources</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="27534-356">Livello funzionalità</span><span class="sxs-lookup"><span data-stu-id="27534-356">Feature Level</span></span></th>
<th><span data-ttu-id="27534-357">Differenze di comportamento</span><span class="sxs-lookup"><span data-stu-id="27534-357">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="27534-358">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="27534-358">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="5"><span data-ttu-id="27534-359">Non supportato in alcun livello di funzionalità 9. \* o 10. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="27534-359">Not supported on any 9.\* or 10.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="27534-360">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="27534-360">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="27534-361">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="27534-361">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="27534-362">D3D_FEATURE_LEVEL_10_0</span><span class="sxs-lookup"><span data-stu-id="27534-362">D3D_FEATURE_LEVEL_10_0</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="27534-363">D3D_FEATURE_LEVEL_10_1</span><span class="sxs-lookup"><span data-stu-id="27534-363">D3D_FEATURE_LEVEL_10_1</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextgssetconstantbuffers"></a><span data-ttu-id="27534-364">Sul ID3D11DeviceContext:: GSSetConstantBuffers</span><span class="sxs-lookup"><span data-stu-id="27534-364">ID3D11DeviceContext::GSSetConstantBuffers</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="27534-365">Livello funzionalità</span><span class="sxs-lookup"><span data-stu-id="27534-365">Feature Level</span></span></th>
<th><span data-ttu-id="27534-366">Differenze di comportamento</span><span class="sxs-lookup"><span data-stu-id="27534-366">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="27534-367">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="27534-367">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="27534-368">Non supportato in alcun livello di funzionalità 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="27534-368">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="27534-369">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="27534-369">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="27534-370">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="27534-370">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextgssetsamplers"></a><span data-ttu-id="27534-371">Sul ID3D11DeviceContext:: GSSetSamplers</span><span class="sxs-lookup"><span data-stu-id="27534-371">ID3D11DeviceContext::GSSetSamplers</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="27534-372">Livello funzionalità</span><span class="sxs-lookup"><span data-stu-id="27534-372">Feature Level</span></span></th>
<th><span data-ttu-id="27534-373">Differenze di comportamento</span><span class="sxs-lookup"><span data-stu-id="27534-373">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="27534-374">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="27534-374">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="27534-375">Non supportato in alcun livello di funzionalità 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="27534-375">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="27534-376">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="27534-376">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="27534-377">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="27534-377">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextgssetshader"></a><span data-ttu-id="27534-378">Sul ID3D11DeviceContext:: GSSetShader</span><span class="sxs-lookup"><span data-stu-id="27534-378">ID3D11DeviceContext::GSSetShader</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="27534-379">Livello funzionalità</span><span class="sxs-lookup"><span data-stu-id="27534-379">Feature Level</span></span></th>
<th><span data-ttu-id="27534-380">Differenze di comportamento</span><span class="sxs-lookup"><span data-stu-id="27534-380">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="27534-381">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="27534-381">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="27534-382">Non supportato in alcun livello di funzionalità 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="27534-382">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="27534-383">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="27534-383">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="27534-384">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="27534-384">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextgssetshaderresources"></a><span data-ttu-id="27534-385">Sul ID3D11DeviceContext:: GSSetShaderResources</span><span class="sxs-lookup"><span data-stu-id="27534-385">ID3D11DeviceContext::GSSetShaderResources</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="27534-386">Livello funzionalità</span><span class="sxs-lookup"><span data-stu-id="27534-386">Feature Level</span></span></th>
<th><span data-ttu-id="27534-387">Differenze di comportamento</span><span class="sxs-lookup"><span data-stu-id="27534-387">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="27534-388">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="27534-388">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="27534-389">Non supportato in alcun livello di funzionalità 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="27534-389">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="27534-390">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="27534-390">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="27534-391">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="27534-391">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontexthssetconstantbuffers"></a><span data-ttu-id="27534-392">Sul ID3D11DeviceContext:: HSSetConstantBuffers</span><span class="sxs-lookup"><span data-stu-id="27534-392">ID3D11DeviceContext::HSSetConstantBuffers</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="27534-393">Livello funzionalità</span><span class="sxs-lookup"><span data-stu-id="27534-393">Feature Level</span></span></th>
<th><span data-ttu-id="27534-394">Differenze di comportamento</span><span class="sxs-lookup"><span data-stu-id="27534-394">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="27534-395">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="27534-395">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="5"><span data-ttu-id="27534-396">Non supportato in alcun livello di funzionalità 9. \* o 10. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="27534-396">Not supported on any 9.\* or 10.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="27534-397">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="27534-397">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="27534-398">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="27534-398">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="27534-399">D3D_FEATURE_LEVEL_10_0</span><span class="sxs-lookup"><span data-stu-id="27534-399">D3D_FEATURE_LEVEL_10_0</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="27534-400">D3D_FEATURE_LEVEL_10_1</span><span class="sxs-lookup"><span data-stu-id="27534-400">D3D_FEATURE_LEVEL_10_1</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontexthssetsamplers"></a><span data-ttu-id="27534-401">Sul ID3D11DeviceContext:: HSSetSamplers</span><span class="sxs-lookup"><span data-stu-id="27534-401">ID3D11DeviceContext::HSSetSamplers</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="27534-402">Livello funzionalità</span><span class="sxs-lookup"><span data-stu-id="27534-402">Feature Level</span></span></th>
<th><span data-ttu-id="27534-403">Differenze di comportamento</span><span class="sxs-lookup"><span data-stu-id="27534-403">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="27534-404">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="27534-404">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="5"><span data-ttu-id="27534-405">Non supportato in alcun livello di funzionalità 9. \* o 10. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="27534-405">Not supported on any 9.\* or 10.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="27534-406">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="27534-406">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="27534-407">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="27534-407">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="27534-408">D3D_FEATURE_LEVEL_10_0</span><span class="sxs-lookup"><span data-stu-id="27534-408">D3D_FEATURE_LEVEL_10_0</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="27534-409">D3D_FEATURE_LEVEL_10_1</span><span class="sxs-lookup"><span data-stu-id="27534-409">D3D_FEATURE_LEVEL_10_1</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontexthssetshader"></a><span data-ttu-id="27534-410">Sul ID3D11DeviceContext:: HSSetShader</span><span class="sxs-lookup"><span data-stu-id="27534-410">ID3D11DeviceContext::HSSetShader</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="27534-411">Livello funzionalità</span><span class="sxs-lookup"><span data-stu-id="27534-411">Feature Level</span></span></th>
<th><span data-ttu-id="27534-412">Differenze di comportamento</span><span class="sxs-lookup"><span data-stu-id="27534-412">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="27534-413">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="27534-413">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="5"><span data-ttu-id="27534-414">Non supportato in alcun livello di funzionalità 9. \* o 10. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="27534-414">Not supported on any 9.\* or 10.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="27534-415">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="27534-415">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="27534-416">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="27534-416">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="27534-417">D3D_FEATURE_LEVEL_10_0</span><span class="sxs-lookup"><span data-stu-id="27534-417">D3D_FEATURE_LEVEL_10_0</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="27534-418">D3D_FEATURE_LEVEL_10_1</span><span class="sxs-lookup"><span data-stu-id="27534-418">D3D_FEATURE_LEVEL_10_1</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontexthssetshaderresources"></a><span data-ttu-id="27534-419">Sul ID3D11DeviceContext:: HSSetShaderResources</span><span class="sxs-lookup"><span data-stu-id="27534-419">ID3D11DeviceContext::HSSetShaderResources</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="27534-420">Livello funzionalità</span><span class="sxs-lookup"><span data-stu-id="27534-420">Feature Level</span></span></th>
<th><span data-ttu-id="27534-421">Differenze di comportamento</span><span class="sxs-lookup"><span data-stu-id="27534-421">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="27534-422">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="27534-422">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="5"><span data-ttu-id="27534-423">Non supportato in alcun livello di funzionalità 9. \* o 10. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="27534-423">Not supported on any 9.\* or 10.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="27534-424">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="27534-424">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="27534-425">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="27534-425">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="27534-426">D3D_FEATURE_LEVEL_10_0</span><span class="sxs-lookup"><span data-stu-id="27534-426">D3D_FEATURE_LEVEL_10_0</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="27534-427">D3D_FEATURE_LEVEL_10_1</span><span class="sxs-lookup"><span data-stu-id="27534-427">D3D_FEATURE_LEVEL_10_1</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextiasetindexbuffer"></a><span data-ttu-id="27534-428">ID3D11DeviceContext::IASetIndexBuffer</span><span class="sxs-lookup"><span data-stu-id="27534-428">ID3D11DeviceContext::IASetIndexBuffer</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="27534-429">Livello funzionalità</span><span class="sxs-lookup"><span data-stu-id="27534-429">Feature Level</span></span></th>
<th><span data-ttu-id="27534-430">Differenze di comportamento</span><span class="sxs-lookup"><span data-stu-id="27534-430">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="27534-431">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="27534-431">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td><span data-ttu-id="27534-432">Il formato può essere diverso da quello specificato al momento della creazione del buffer, ma verrà subita una traduzione costosa.</span><span class="sxs-lookup"><span data-stu-id="27534-432">Format is allowed to be different from that specified at buffer creation, but an expensive translation will be incurred.</span></span><br/> <span data-ttu-id="27534-433">Consente solo buffer di indice con il formato DXGI_FORMAT_R16_UINT.</span><span class="sxs-lookup"><span data-stu-id="27534-433">Only allows index buffers with the DXGI_FORMAT_R16_UINT format.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="27534-434">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="27534-434">D3D_FEATURE_LEVEL_9_2</span></span></td>
<td rowspan="2"> <span data-ttu-id="27534-435">Il formato può essere diverso da quello specificato al momento della creazione del buffer, ma verrà subita una traduzione costosa.</span><span class="sxs-lookup"><span data-stu-id="27534-435">Format is allowed to be different from that specified at buffer creation, but an expensive translation will be incurred.</span></span><br/> <span data-ttu-id="27534-436">Consente i buffer di indice con i formati DXGI_FORMAT_R16_UINT e DXGI_FORMAT_R32_UINT come D3D_FEATURE_LEVEL_10_0 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="27534-436">Allows index buffers with the DXGI_FORMAT_R16_UINT and DXGI_FORMAT_R32_UINT formats like D3D_FEATURE_LEVEL_10_0 and higher.</span></span> <br/> <span data-ttu-id="27534-437">$ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="27534-437">${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="odd">
<td><span data-ttu-id="27534-438">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="27534-438">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextiasetprimitivetopology"></a><span data-ttu-id="27534-439">Sul ID3D11DeviceContext:: IASetPrimitiveTopology</span><span class="sxs-lookup"><span data-stu-id="27534-439">ID3D11DeviceContext::IASetPrimitiveTopology</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="27534-440">Livello funzionalità</span><span class="sxs-lookup"><span data-stu-id="27534-440">Feature Level</span></span></th>
<th><span data-ttu-id="27534-441">Differenze di comportamento</span><span class="sxs-lookup"><span data-stu-id="27534-441">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="27534-442">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="27534-442">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="27534-443">Le topologie primitive con adiacenza non sono supportate $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="27534-443">Primitive topologies with adjacency are not supported${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="27534-444">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="27534-444">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="27534-445">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="27534-445">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextomsetblendstate"></a><span data-ttu-id="27534-446">Sul ID3D11DeviceContext:: OMSetBlendState</span><span class="sxs-lookup"><span data-stu-id="27534-446">ID3D11DeviceContext::OMSetBlendState</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="27534-447">Livello funzionalità</span><span class="sxs-lookup"><span data-stu-id="27534-447">Feature Level</span></span></th>
<th><span data-ttu-id="27534-448">Differenze di comportamento</span><span class="sxs-lookup"><span data-stu-id="27534-448">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="27534-449">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="27534-449">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="27534-450">SampleMask non può essere zero $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="27534-450">SampleMask cannot be zero${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="27534-451">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="27534-451">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="27534-452">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="27534-452">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextomsetrendertargets"></a><span data-ttu-id="27534-453">Sul ID3D11DeviceContext:: OMSetRenderTargets</span><span class="sxs-lookup"><span data-stu-id="27534-453">ID3D11DeviceContext::OMSetRenderTargets</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="27534-454">Livello funzionalità</span><span class="sxs-lookup"><span data-stu-id="27534-454">Feature Level</span></span></th>
<th><span data-ttu-id="27534-455">Differenze di comportamento</span><span class="sxs-lookup"><span data-stu-id="27534-455">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="27534-456">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="27534-456">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="2"><span data-ttu-id="27534-457">Una sola destinazione di rendering supporta $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="27534-457">Only one render target supported${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="27534-458">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="27534-458">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="27534-459">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="27534-459">D3D_FEATURE_LEVEL_9_3</span></span></td>
<td><span data-ttu-id="27534-460">Sono supportate solo quattro destinazioni di rendering e tutte le risorse con binding devono avere la stessa profondità dei bit.</span><span class="sxs-lookup"><span data-stu-id="27534-460">Only four render targets supported, and all bound resources must have same bit depth.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextomsetrendertargetsandunorderedaccessviews"></a><span data-ttu-id="27534-461">Sul ID3D11DeviceContext:: OMSetRenderTargetsAndUnorderedAccessViews</span><span class="sxs-lookup"><span data-stu-id="27534-461">ID3D11DeviceContext::OMSetRenderTargetsAndUnorderedAccessViews</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="27534-462">Livello funzionalità</span><span class="sxs-lookup"><span data-stu-id="27534-462">Feature Level</span></span></th>
<th><span data-ttu-id="27534-463">Differenze di comportamento</span><span class="sxs-lookup"><span data-stu-id="27534-463">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="27534-464">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="27534-464">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="27534-465">Non supportato in alcun livello di funzionalità 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="27534-465">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="27534-466">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="27534-466">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="27534-467">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="27534-467">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextpssetconstantbuffers"></a><span data-ttu-id="27534-468">Sul ID3D11DeviceContext::P SSetConstantBuffers</span><span class="sxs-lookup"><span data-stu-id="27534-468">ID3D11DeviceContext::PSSetConstantBuffers</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="27534-469">Livello funzionalità</span><span class="sxs-lookup"><span data-stu-id="27534-469">Feature Level</span></span></th>
<th><span data-ttu-id="27534-470">Differenze di comportamento</span><span class="sxs-lookup"><span data-stu-id="27534-470">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="27534-471">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="27534-471">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="27534-472">Vedere il livello di funzionalità 10,0, ma il numero totale di costanti usate da shader non può superare 32 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="27534-472">See feature level 10.0, but total number of constants used by shader cannot exceed 32${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="27534-473">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="27534-473">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="27534-474">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="27534-474">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextpssetsamplers"></a><span data-ttu-id="27534-475">Sul ID3D11DeviceContext::P SSetSamplers</span><span class="sxs-lookup"><span data-stu-id="27534-475">ID3D11DeviceContext::PSSetSamplers</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="27534-476">Livello funzionalità</span><span class="sxs-lookup"><span data-stu-id="27534-476">Feature Level</span></span></th>
<th><span data-ttu-id="27534-477">Differenze di comportamento</span><span class="sxs-lookup"><span data-stu-id="27534-477">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="27534-478">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="27534-478">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="27534-479">Non è possibile associare più di 16 campionatori $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="27534-479">No more than 16 samplers can be bound${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="27534-480">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="27534-480">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="27534-481">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="27534-481">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextpssetshader"></a><span data-ttu-id="27534-482">Sul ID3D11DeviceContext::P SSetShader</span><span class="sxs-lookup"><span data-stu-id="27534-482">ID3D11DeviceContext::PSSetShader</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="27534-483">Livello funzionalità</span><span class="sxs-lookup"><span data-stu-id="27534-483">Feature Level</span></span></th>
<th><span data-ttu-id="27534-484">Differenze di comportamento</span><span class="sxs-lookup"><span data-stu-id="27534-484">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="27534-485">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="27534-485">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="2"><span data-ttu-id="27534-486">Solo ps_4_0_level_9_1 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="27534-486">Only ps_4_0_level_9_1${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="27534-487">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="27534-487">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="27534-488">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="27534-488">D3D_FEATURE_LEVEL_9_3</span></span></td>
<td><span data-ttu-id="27534-489">Solo ps_4_0_level_9_3 o ps_4_0_level_9_1</span><span class="sxs-lookup"><span data-stu-id="27534-489">Only ps_4_0_level_9_3 or ps_4_0_level_9_1</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextpssetshaderresources"></a><span data-ttu-id="27534-490">Sul ID3D11DeviceContext::P SSetShaderResources</span><span class="sxs-lookup"><span data-stu-id="27534-490">ID3D11DeviceContext::PSSetShaderResources</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="27534-491">Livello funzionalità</span><span class="sxs-lookup"><span data-stu-id="27534-491">Feature Level</span></span></th>
<th><span data-ttu-id="27534-492">Differenze di comportamento</span><span class="sxs-lookup"><span data-stu-id="27534-492">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="27534-493">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="27534-493">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="27534-494">Non più di 8 risorse dello shader con binding simultaneo $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="27534-494">No more than 8 simultaneously bound shader resources${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="27534-495">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="27534-495">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="27534-496">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="27534-496">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextrssetscissorrects"></a><span data-ttu-id="27534-497">Sul ID3D11DeviceContext:: RSSetScissorRects</span><span class="sxs-lookup"><span data-stu-id="27534-497">ID3D11DeviceContext::RSSetScissorRects</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="27534-498">Livello funzionalità</span><span class="sxs-lookup"><span data-stu-id="27534-498">Feature Level</span></span></th>
<th><span data-ttu-id="27534-499">Differenze di comportamento</span><span class="sxs-lookup"><span data-stu-id="27534-499">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="27534-500">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="27534-500">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="27534-501">Sono disponibili solo zero Scissor Rect, $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="27534-501">Only the zeroth scissor rect is available${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="27534-502">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="27534-502">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="27534-503">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="27534-503">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextrssetviewports"></a><span data-ttu-id="27534-504">Sul ID3D11DeviceContext:: RSSetViewports</span><span class="sxs-lookup"><span data-stu-id="27534-504">ID3D11DeviceContext::RSSetViewports</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="27534-505">Livello funzionalità</span><span class="sxs-lookup"><span data-stu-id="27534-505">Feature Level</span></span></th>
<th><span data-ttu-id="27534-506">Differenze di comportamento</span><span class="sxs-lookup"><span data-stu-id="27534-506">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="27534-507">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="27534-507">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="27534-508">È disponibile solo il viewport zero $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="27534-508">Only the zeroth viewport is available${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="27534-509">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="27534-509">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="27534-510">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="27534-510">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

<span data-ttu-id="27534-511">Anche se si specificano valori float per i membri della struttura del [**\_ viewport d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_viewport) per la matrice *pViewports* in una chiamata a [**sul ID3D11DeviceContext:: RSSetViewports**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetviewports) per i [livelli di funzionalità](overviews-direct3d-11-devices-downlevel-intro.md) 9 \_ x, **RSSetViewports** usa i valori DWORD internamente.</span><span class="sxs-lookup"><span data-stu-id="27534-511">Even though you specify float values to the members of the [**D3D11\_VIEWPORT**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_viewport) structure for the *pViewports* array in a call to [**ID3D11DeviceContext::RSSetViewports**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetviewports) for [feature levels](overviews-direct3d-11-devices-downlevel-intro.md) 9\_x, **RSSetViewports** uses DWORDs internally.</span></span> <span data-ttu-id="27534-512">A causa di questo comportamento, quando si usa un angolo superiore sinistro negativo per il viewport, la chiamata a **RSSetViewports** per i livelli di funzionalità 9 \_ x ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="27534-512">Because of this behavior, when you use a negative top left corner for the viewport, the call to **RSSetViewports** for feature levels 9\_x fails.</span></span> <span data-ttu-id="27534-513">Questo errore si verifica perché **RSSetViewports** per 9 \_ x esegue il cast dei valori a virgola mobile in interi senza segno senza convalida, che comporta un overflow di Integer.</span><span class="sxs-lookup"><span data-stu-id="27534-513">This failure occurs because **RSSetViewports** for 9\_x casts the floating point values into unsigned integers without validation, which results in integer overflow.</span></span>

<span data-ttu-id="27534-514">La chiamata a [**sul ID3D11DeviceContext:: RSSetViewports**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetviewports) per i [livelli di funzionalità](overviews-direct3d-11-devices-downlevel-intro.md) 10 \_ x e 11 \_ x funziona come previsto anche quando si usa un angolo superiore sinistro negativo per il viewport.</span><span class="sxs-lookup"><span data-stu-id="27534-514">The call to [**ID3D11DeviceContext::RSSetViewports**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetviewports) for [feature levels](overviews-direct3d-11-devices-downlevel-intro.md) 10\_x and 11\_x works as you expect even when you use a negative top left corner for the viewport.</span></span>

## <a name="id3d11devicecontextsetpredication"></a><span data-ttu-id="27534-515">Sul ID3D11DeviceContext:: SetPredication</span><span class="sxs-lookup"><span data-stu-id="27534-515">ID3D11DeviceContext::SetPredication</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="27534-516">Livello funzionalità</span><span class="sxs-lookup"><span data-stu-id="27534-516">Feature Level</span></span></th>
<th><span data-ttu-id="27534-517">Differenze di comportamento</span><span class="sxs-lookup"><span data-stu-id="27534-517">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="27534-518">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="27534-518">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="27534-519">Non supportato in alcun livello di funzionalità 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="27534-519">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="27534-520">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="27534-520">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="27534-521">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="27534-521">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextsosettargets"></a><span data-ttu-id="27534-522">Sul ID3D11DeviceContext:: SOSetTargets</span><span class="sxs-lookup"><span data-stu-id="27534-522">ID3D11DeviceContext::SOSetTargets</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="27534-523">Livello funzionalità</span><span class="sxs-lookup"><span data-stu-id="27534-523">Feature Level</span></span></th>
<th><span data-ttu-id="27534-524">Differenze di comportamento</span><span class="sxs-lookup"><span data-stu-id="27534-524">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="27534-525">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="27534-525">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="27534-526">Non supportato in alcun livello di funzionalità 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="27534-526">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="27534-527">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="27534-527">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="27534-528">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="27534-528">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextvssetconstantbuffers"></a><span data-ttu-id="27534-529">Sul ID3D11DeviceContext:: VSSetConstantBuffers</span><span class="sxs-lookup"><span data-stu-id="27534-529">ID3D11DeviceContext::VSSetConstantBuffers</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="27534-530">Livello funzionalità</span><span class="sxs-lookup"><span data-stu-id="27534-530">Feature Level</span></span></th>
<th><span data-ttu-id="27534-531">Differenze di comportamento</span><span class="sxs-lookup"><span data-stu-id="27534-531">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="27534-532">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="27534-532">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="27534-533">Vedere il livello di funzionalità 10,0, ma il numero totale di costanti usate da shader non può superare 255 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="27534-533">See feature level 10.0, but total number of constants used by shader cannot exceed 255${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="27534-534">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="27534-534">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="27534-535">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="27534-535">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextvssetsamplers"></a><span data-ttu-id="27534-536">Sul ID3D11DeviceContext:: VSSetSamplers</span><span class="sxs-lookup"><span data-stu-id="27534-536">ID3D11DeviceContext::VSSetSamplers</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="27534-537">Livello funzionalità</span><span class="sxs-lookup"><span data-stu-id="27534-537">Feature Level</span></span></th>
<th><span data-ttu-id="27534-538">Differenze di comportamento</span><span class="sxs-lookup"><span data-stu-id="27534-538">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="27534-539">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="27534-539">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="27534-540">Non supportato in alcun livello di funzionalità 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="27534-540">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="27534-541">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="27534-541">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="27534-542">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="27534-542">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextvssetshader"></a><span data-ttu-id="27534-543">Sul ID3D11DeviceContext:: VSSetShader</span><span class="sxs-lookup"><span data-stu-id="27534-543">ID3D11DeviceContext::VSSetShader</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="27534-544">Livello funzionalità</span><span class="sxs-lookup"><span data-stu-id="27534-544">Feature Level</span></span></th>
<th><span data-ttu-id="27534-545">Differenze di comportamento</span><span class="sxs-lookup"><span data-stu-id="27534-545">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="27534-546">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="27534-546">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="2"><span data-ttu-id="27534-547">Solo vs_4_0_level_9_1 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="27534-547">Only vs_4_0_level_9_1${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="27534-548">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="27534-548">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="27534-549">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="27534-549">D3D_FEATURE_LEVEL_9_3</span></span></td>
<td><span data-ttu-id="27534-550">Solo vs_4_0_level_9_3 o vs_4_0_level_9_1</span><span class="sxs-lookup"><span data-stu-id="27534-550">Only vs_4_0_level_9_3 or vs_4_0_level_9_1</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextvssetshaderresources"></a><span data-ttu-id="27534-551">Sul ID3D11DeviceContext:: VSSetShaderResources</span><span class="sxs-lookup"><span data-stu-id="27534-551">ID3D11DeviceContext::VSSetShaderResources</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="27534-552">Livello funzionalità</span><span class="sxs-lookup"><span data-stu-id="27534-552">Feature Level</span></span></th>
<th><span data-ttu-id="27534-553">Differenze di comportamento</span><span class="sxs-lookup"><span data-stu-id="27534-553">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="27534-554">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="27534-554">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="27534-555">Non supportato in alcun livello di funzionalità 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="27534-555">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="27534-556">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="27534-556">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="27534-557">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="27534-557">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="27534-558">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="27534-558">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="27534-559">Riferimento a 10Level9</span><span class="sxs-lookup"><span data-stu-id="27534-559">10Level9 Reference</span></span>](d3d11-graphics-reference-10level9.md)
</dt> </dl>

 

 





