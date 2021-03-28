---
title: Sintassi della tecnica degli effetti (Direct3D 11)
description: Una tecnica degli effetti viene dichiarata con la sintassi descritta in questa sezione.
ms.assetid: 54a6ebd1-a6b4-473b-bf53-a3323445de71
keywords:
- Effetto technique11, Direct3D 11
- Effetto Pass, Direct3D 11
- Effetto CompileShader, Direct3D 11
- Effetto SetStateGroup, Direct3D 11
- Effetto SetBlendState, Direct3D 11
- Effetto SetDepthStencilState, Direct3D 11
- Effetto SetRasterizerState, Direct3D 11
- Effetto SetVertexShader, Direct3D 11
- Effetto SetGeometryShader, Direct3D 11
- Effetto SetPixelShader, Direct3D 11
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73fb668f308869ef9cca5cce99d522f18a287f3c
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104117225"
---
# <a name="effect-technique-syntax-direct3d-11"></a><span data-ttu-id="91f32-113">Sintassi della tecnica degli effetti (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="91f32-113">Effect Technique Syntax (Direct3D 11)</span></span>

<span data-ttu-id="91f32-114">Una tecnica degli effetti viene dichiarata con la sintassi descritta in questa sezione.</span><span class="sxs-lookup"><span data-stu-id="91f32-114">An effect technique is declared with the syntax described in this section.</span></span>

<span data-ttu-id="91f32-115">Annotazioni di TechniqueVersion *techniquename* \[  <  > \]</span><span class="sxs-lookup"><span data-stu-id="91f32-115">TechniqueVersion *TechniqueName* \[ <*Annotations* > \]</span></span>

<span data-ttu-id="91f32-116">{</span><span class="sxs-lookup"><span data-stu-id="91f32-116">{</span></span>

<dl> <span data-ttu-id="91f32-117">passare *le* \[  < *annotazioni* passname > \]</span><span class="sxs-lookup"><span data-stu-id="91f32-117">pass *PassName* \[ <*Annotations* > \]</span></span>  
<span data-ttu-id="91f32-118">{</span><span class="sxs-lookup"><span data-stu-id="91f32-118">{</span></span>
<dl> <span data-ttu-id="91f32-119">\[*SetStateGroup*; \] \[ *SetStateGroup*;\]</span><span class="sxs-lookup"><span data-stu-id="91f32-119">\[ *SetStateGroup*; \] \[ *SetStateGroup*; \]</span></span>  
<span data-ttu-id="91f32-120">...</span><span class="sxs-lookup"><span data-stu-id="91f32-120">...</span></span>  
<span data-ttu-id="91f32-121">\[*SetStateGroup*;\]</span><span class="sxs-lookup"><span data-stu-id="91f32-121">\[ *SetStateGroup*; \]</span></span>
</dl> </dd> }  
</dl>

<span data-ttu-id="91f32-122">}</span><span class="sxs-lookup"><span data-stu-id="91f32-122">}</span></span>

## <a name="parameters"></a><span data-ttu-id="91f32-123">Parametri</span><span class="sxs-lookup"><span data-stu-id="91f32-123">Parameters</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="91f32-124">Elemento</span><span class="sxs-lookup"><span data-stu-id="91f32-124">Item</span></span></th>
<th><span data-ttu-id="91f32-125">Descrizione</span><span class="sxs-lookup"><span data-stu-id="91f32-125">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="91f32-126"><span id="TechniqueVersion"></span><span id="techniqueversion"></span><span id="TECHNIQUEVERSION"></span>TechniqueVersion</span><span class="sxs-lookup"><span data-stu-id="91f32-126"><span id="TechniqueVersion"></span><span id="techniqueversion"></span><span id="TECHNIQUEVERSION"></span>TechniqueVersion</span></span><br/></td>
<td><span data-ttu-id="91f32-127">Technique10 o technique11.</span><span class="sxs-lookup"><span data-stu-id="91f32-127">Either technique10 or technique11.</span></span> <span data-ttu-id="91f32-128">Le tecniche che usano la nuova funzionalità di Direct3D 11 (5_0 shader, BindInterfaces e così via) devono usare technique11.</span><span class="sxs-lookup"><span data-stu-id="91f32-128">Techniques which use functionality new to Direct3D 11 (5_0 shaders, BindInterfaces, etc) must use technique11.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="91f32-129"><span id="TechniqueName"></span><span id="techniquename"></span><span id="TECHNIQUENAME"></span><em>Techniquename</em></span><span class="sxs-lookup"><span data-stu-id="91f32-129"><span id="TechniqueName"></span><span id="techniquename"></span><span id="TECHNIQUENAME"></span><em>TechniqueName</em></span></span><br/></td>
<td><span data-ttu-id="91f32-130">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="91f32-130">Optional.</span></span> <span data-ttu-id="91f32-131">Stringa ASCII che identifica in modo univoco il nome della tecnica degli effetti.</span><span class="sxs-lookup"><span data-stu-id="91f32-131">An ASCII string that uniquely identifies the name of the effect technique.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="91f32-132"><span id="______________Annotations__"></span><span id="______________annotations__"></span><span id="______________ANNOTATIONS__"></span> <<em>Annotazioni</em> ></span><span class="sxs-lookup"><span data-stu-id="91f32-132"><span id="______________Annotations__"></span><span id="______________annotations__"></span><span id="______________ANNOTATIONS__"></span> <<em>Annotations</em> ></span></span><br/></td>
<td><span data-ttu-id="91f32-133">[in] Facoltativo.</span><span class="sxs-lookup"><span data-stu-id="91f32-133">[in] Optional.</span></span> <span data-ttu-id="91f32-134">Una o più parti di informazioni (metadati) fornite dall'utente ignorate dal sistema di effetti.</span><span class="sxs-lookup"><span data-stu-id="91f32-134">One or more pieces of user-supplied information (metadata) that is ignored by the effect system.</span></span> <span data-ttu-id="91f32-135">Per la sintassi, vedere <a href="d3d11-effect-annotation-syntax.md">sintassi delle annotazioni (Direct3D 11)</a>.</span><span class="sxs-lookup"><span data-stu-id="91f32-135">For syntax, see <a href="d3d11-effect-annotation-syntax.md">Annotation Syntax (Direct3D 11)</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="91f32-136"><span id="pass"></span><span id="PASS"></span>passare</span><span class="sxs-lookup"><span data-stu-id="91f32-136"><span id="pass"></span><span id="PASS"></span>pass</span></span><br/></td>
<td><span data-ttu-id="91f32-137">Parola chiave required.</span><span class="sxs-lookup"><span data-stu-id="91f32-137">Required keyword.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="91f32-138"><span id="PassName"></span><span id="passname"></span><span id="PASSNAME"></span><em>Passname</em></span><span class="sxs-lookup"><span data-stu-id="91f32-138"><span id="PassName"></span><span id="passname"></span><span id="PASSNAME"></span><em>PassName</em></span></span><br/></td>
<td><span data-ttu-id="91f32-139">[in] Facoltativo.</span><span class="sxs-lookup"><span data-stu-id="91f32-139">[in] Optional.</span></span> <span data-ttu-id="91f32-140">Stringa ASCII che identifica in modo univoco il nome del passaggio.</span><span class="sxs-lookup"><span data-stu-id="91f32-140">An ASCII string that uniquely identifies the name of the pass.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="91f32-141"><span id="SetStateGroup"></span><span id="setstategroup"></span><span id="SETSTATEGROUP"></span><em>SetStateGroup</em></span><span class="sxs-lookup"><span data-stu-id="91f32-141"><span id="SetStateGroup"></span><span id="setstategroup"></span><span id="SETSTATEGROUP"></span><em>SetStateGroup</em></span></span><br/></td>
<td><span data-ttu-id="91f32-142">in Impostare uno o più gruppi di Stati, ad esempio:</span><span class="sxs-lookup"><span data-stu-id="91f32-142">[in] Set one or more state groups such as:</span></span> <br/> 
<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="91f32-143">StateGroup</span><span class="sxs-lookup"><span data-stu-id="91f32-143">StateGroup</span></span></th>
<th><span data-ttu-id="91f32-144">Sintassi</span><span class="sxs-lookup"><span data-stu-id="91f32-144">Syntax</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="91f32-145">Stato di Blend</span><span class="sxs-lookup"><span data-stu-id="91f32-145">Blend State</span></span></td>
<td><span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>SetBlendState( arguments ); </code></pre></td>
</tr>
</tbody>
</table>

<p><span data-ttu-id="91f32-146">Vedere [<strong>sul ID3D11DeviceContext:: OMSetBlendState</strong>] (/Windows/Desktop/API/d3d11/NF-d3d11-ID3D11DeviceContext-omsetblendstate) per l'elenco di argomenti.</span><span class="sxs-lookup"><span data-stu-id="91f32-146">See [<strong>ID3D11DeviceContext::OMSetBlendState</strong>](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetblendstate) for the argument list.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="91f32-147">Stato stencil profondità</span><span class="sxs-lookup"><span data-stu-id="91f32-147">Depth-stencil State</span></span></td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>SetDepthStencilState( arguments ); </code></pre></td>
</tr>
</tbody>
</table>

</div>
<p><span data-ttu-id="91f32-148">Vedere <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetdepthstencilstate"><strong>sul ID3D11DeviceContext:: OMSetDepthStencilState</strong></a> per l'elenco di argomenti.</span><span class="sxs-lookup"><span data-stu-id="91f32-148">See <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetdepthstencilstate"><strong>ID3D11DeviceContext::OMSetDepthStencilState</strong></a> for the argument list.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="91f32-149">Stato rasterizzazione</span><span class="sxs-lookup"><span data-stu-id="91f32-149">Rasterizer State</span></span></td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>SetRasterizerState( arguments ); </code></pre></td>
</tr>
</tbody>
</table>

</div>
<p><span data-ttu-id="91f32-150">Vedere [<strong>sul ID3D11DeviceContext:: RSSetState</strong>] (/Windows/Desktop/API/d3d11/NF-d3d11-ID3D11DeviceContext-rssetstate) per l'elenco di argomenti.</span><span class="sxs-lookup"><span data-stu-id="91f32-150">See [<strong>ID3D11DeviceContext::RSSetState</strong>](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetstate) for the argument list.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="91f32-151">Stato dello shader</span><span class="sxs-lookup"><span data-stu-id="91f32-151">Shader State</span></span></td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>SetXXXShader( Shader );</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p><span data-ttu-id="91f32-152">SetXXXShader è uno dei SetVertexShader, SetDomainShader, SetHullShader, SetGeometryShader, SetPixelShader o SetComputeShader (che sono simili ai metodi API <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-vssetshader"><strong>sul ID3D11DeviceContext:: VSSetShader</strong></a>, <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dssetshader"><strong>sul ID3D11DeviceContext::D ssetshader</strong></a>, <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetshader"><strong>sul ID3D11DeviceContext:: HSSetShader</strong></a>, <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-gssetshader"><strong>sul id3d11devicecontext:: GSSetShader</strong></a>, <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetshader"><strong>sul ID3D11DeviceContext::P ssetshader</strong></a> e <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-cssetshader"><strong>sul ID3D11DeviceContext:: CSSetShader</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="91f32-152">SetXXXShader is one of SetVertexShader, SetDomainShader, SetHullShader, SetGeometryShader, SetPixelShader or SetComputeShader (which are similar to the API methods <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-vssetshader"><strong>ID3D11DeviceContext::VSSetShader</strong></a>, <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dssetshader"><strong>ID3D11DeviceContext::DSSetShader</strong></a>, <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetshader"><strong>ID3D11DeviceContext::HSSetShader</strong></a>, <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-gssetshader"><strong>ID3D11DeviceContext::GSSetShader</strong></a>, <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetshader"><strong>ID3D11DeviceContext::PSSetShader</strong></a> and <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-cssetshader"><strong>ID3D11DeviceContext::CSSetShader</strong></a>).</span></span></p>
<p><span data-ttu-id="91f32-153">Shader è una variabile shader, che può essere ottenuta in molti modi:</span><span class="sxs-lookup"><span data-stu-id="91f32-153">Shader is a shader variable, which can be obtained in many ways:</span></span></p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>SetXXXShader( CompileShader( shader_profile, ShaderFunction( args ) ) );
SetXXXShader( CompileShader( NULL ) );
SetXXXShader( NULL );
SetXXXShader( myShaderVar );
SetXXXShader( myShaderArray[2] );
SetXXXShader( myShaderArray[uIndex] );
SetGeometryShader( ConstructGSWithSO( Shader, strStream0 ) );
SetGeometryShader( ConstructGSWithSO( Shader, strStream0, strStream1, strStream2, strStream3, RastStream ) );</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="91f32-154">Stato destinazione rendering</span><span class="sxs-lookup"><span data-stu-id="91f32-154">Render Target State</span></span></td>
<td><span data-ttu-id="91f32-155">Uno dei valori possibili:</span><span class="sxs-lookup"><span data-stu-id="91f32-155">One of:</span></span>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>SetRenderTargets( RTV0, DSV );
SetRenderTargets( RTV0, RTV1, DSV );
...
SetRenderTargets( RTV0, RTV1, RTV2, RTV3, RTV4, RTV5, RTV6, RTV7, DSV );</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p><span data-ttu-id="91f32-156">Simile a <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetrendertargets"><strong>sul ID3D11DeviceContext:: OMSetRenderTargets</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="91f32-156">Similar to <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetrendertargets"><strong>ID3D11DeviceContext::OMSetRenderTargets</strong></a>.</span></span></p></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="examples"></a><span data-ttu-id="91f32-157">Esempio</span><span class="sxs-lookup"><span data-stu-id="91f32-157">Examples</span></span>

<span data-ttu-id="91f32-158">Questo esempio imposta lo stato di fusione.</span><span class="sxs-lookup"><span data-stu-id="91f32-158">This example sets blending state.</span></span>


```
BlendState NoBlend
{ 
    BlendEnable[0] = False;
};

...

technique10
{
    pass p2 
    {
        ...
        SetBlendState( NoBlend, float4( 0.0f, 0.0f, 0.0f, 0.0f ), 0xFFFFFFFF );
    }
}
```



<span data-ttu-id="91f32-159">In questo esempio viene impostato lo stato di rasterizzazione per eseguire il rendering di un oggetto in wireframe.</span><span class="sxs-lookup"><span data-stu-id="91f32-159">This example sets up the rasterizer state to render an object in wireframe.</span></span>


```
RasterizerState rsWireframe { FillMode = WireFrame; };

...

technique10
{
    pass p1 
    {
        ....
        SetRasterizerState( rsWireframe );
    }
}
```



<span data-ttu-id="91f32-160">Questo esempio imposta lo stato dello shader.</span><span class="sxs-lookup"><span data-stu-id="91f32-160">This example sets shader state.</span></span>


```
technique10 RenderSceneWithTexture1Light
{
    pass P0
    {
        SetVertexShader( CompileShader( vs_4_0, RenderSceneVS( 1, true, true ) ) );
        SetGeometryShader( NULL );
        SetPixelShader( CompileShader( ps_4_0, RenderScenePS( true ) ) );
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="91f32-161">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="91f32-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="91f32-162">Formato effetto</span><span class="sxs-lookup"><span data-stu-id="91f32-162">Effect Format</span></span>](d3d11-effect-format.md)
</dt> <dt>

[<span data-ttu-id="91f32-163">Sintassi del gruppo di effetti (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="91f32-163">Effect Group Syntax (Direct3D 11)</span></span>](d3d11-effect-group-syntax.md)
</dt> <dt>

[<span data-ttu-id="91f32-164">Gruppi di stati effetti</span><span class="sxs-lookup"><span data-stu-id="91f32-164">Effect State Groups</span></span>](d3d11-effect-states.md)
</dt> </dl>

 

 





