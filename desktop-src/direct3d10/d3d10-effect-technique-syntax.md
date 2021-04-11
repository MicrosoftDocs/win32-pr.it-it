---
description: Una tecnica degli effetti viene dichiarata con la sintassi seguente.
ms.assetid: 84f9b74d-8397-4cd5-91a0-7f910ba7b19e
title: Sintassi della tecnica degli effetti (Direct3D 10)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f781a0e1ea247e9ffae02e6afc9de77c8e0c6b68
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126561"
---
# <a name="effect-technique-syntax-direct3d-10"></a><span data-ttu-id="9b089-103">Sintassi della tecnica degli effetti (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="9b089-103">Effect Technique Syntax (Direct3D 10)</span></span>

<span data-ttu-id="9b089-104">Una tecnica degli effetti viene dichiarata con la sintassi seguente.</span><span class="sxs-lookup"><span data-stu-id="9b089-104">An effect technique is declared with the following syntax.</span></span>

<span data-ttu-id="9b089-105">annotazioni di technique10 *techniquename* \[  <  > \]</span><span class="sxs-lookup"><span data-stu-id="9b089-105">technique10 *TechniqueName* \[ <*Annotations* > \]</span></span>

<span data-ttu-id="9b089-106">{</span><span class="sxs-lookup"><span data-stu-id="9b089-106">{</span></span>

<dl> <span data-ttu-id="9b089-107">passare *le* \[  < *annotazioni* passname > \]</span><span class="sxs-lookup"><span data-stu-id="9b089-107">pass *PassName* \[ <*Annotations* > \]</span></span>  
<span data-ttu-id="9b089-108">{</span><span class="sxs-lookup"><span data-stu-id="9b089-108">{</span></span>
<dl> <span data-ttu-id="9b089-109">\[*SetStateGroup*; \] \[ *SetStateGroup*;\]</span><span class="sxs-lookup"><span data-stu-id="9b089-109">\[ *SetStateGroup*; \] \[ *SetStateGroup*; \]</span></span>  
<span data-ttu-id="9b089-110">...</span><span class="sxs-lookup"><span data-stu-id="9b089-110">...</span></span>  
<span data-ttu-id="9b089-111">\[*SetStateGroup*;\]</span><span class="sxs-lookup"><span data-stu-id="9b089-111">\[ *SetStateGroup*; \]</span></span>
</dl> </dd> }  
</dl>

<span data-ttu-id="9b089-112">}</span><span class="sxs-lookup"><span data-stu-id="9b089-112">}</span></span>

## <a name="parameters"></a><span data-ttu-id="9b089-113">Parametri</span><span class="sxs-lookup"><span data-stu-id="9b089-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b089-114"><span id="technique10"></span><span id="TECHNIQUE10"></span>technique10</span><span class="sxs-lookup"><span data-stu-id="9b089-114"><span id="technique10"></span><span id="TECHNIQUE10"></span>technique10</span></span>
</dt> <dd>

<span data-ttu-id="9b089-115">Parola chiave required.</span><span class="sxs-lookup"><span data-stu-id="9b089-115">Required keyword.</span></span>

</dd> <dt>

<span data-ttu-id="9b089-116"><span id="TechniqueName"></span><span id="techniquename"></span><span id="TECHNIQUENAME"></span>*Techniquename*</span><span class="sxs-lookup"><span data-stu-id="9b089-116"><span id="TechniqueName"></span><span id="techniquename"></span><span id="TECHNIQUENAME"></span>*TechniqueName*</span></span>
</dt> <dd>

<span data-ttu-id="9b089-117">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="9b089-117">Optional.</span></span> <span data-ttu-id="9b089-118">Stringa ASCII che identifica in modo univoco il nome della tecnica degli effetti.</span><span class="sxs-lookup"><span data-stu-id="9b089-118">An ASCII string that uniquely identifies the name of the effect technique.</span></span>

</dd> <dt>

<span data-ttu-id="9b089-119"><span id="Annotations"></span><span id="annotations"></span><span id="ANNOTATIONS"></span>*Annotazioni*</span><span class="sxs-lookup"><span data-stu-id="9b089-119"><span id="Annotations"></span><span id="annotations"></span><span id="ANNOTATIONS"></span>*Annotations*</span></span>
</dt> <dd>

<span data-ttu-id="9b089-120">\[in \] facoltativo.</span><span class="sxs-lookup"><span data-stu-id="9b089-120">\[in\] Optional.</span></span> <span data-ttu-id="9b089-121">Una o più parti di informazioni (metadati) fornite dall'utente ignorate dal sistema di effetti.</span><span class="sxs-lookup"><span data-stu-id="9b089-121">One or more pieces of user-supplied information (metadata) that is ignored by the effect system.</span></span> <span data-ttu-id="9b089-122">Per la sintassi, vedere [sintassi delle annotazioni (Direct3D 10)](d3d10-effect-annotation-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="9b089-122">For syntax, see [Annotation Syntax (Direct3D 10)](d3d10-effect-annotation-syntax.md).</span></span>

</dd> <dt>

<span data-ttu-id="9b089-123"><span id="pass"></span><span id="PASS"></span>passare</span><span class="sxs-lookup"><span data-stu-id="9b089-123"><span id="pass"></span><span id="PASS"></span>pass</span></span>
</dt> <dd>

<span data-ttu-id="9b089-124">Parola chiave required.</span><span class="sxs-lookup"><span data-stu-id="9b089-124">Required keyword.</span></span>

</dd> <dt>

<span data-ttu-id="9b089-125"><span id="PassName"></span><span id="passname"></span><span id="PASSNAME"></span>*Passname*</span><span class="sxs-lookup"><span data-stu-id="9b089-125"><span id="PassName"></span><span id="passname"></span><span id="PASSNAME"></span>*PassName*</span></span>
</dt> <dd>

<span data-ttu-id="9b089-126">\[in \] facoltativo.</span><span class="sxs-lookup"><span data-stu-id="9b089-126">\[in\] Optional.</span></span> <span data-ttu-id="9b089-127">Stringa ASCII che identifica in modo univoco il nome del passaggio.</span><span class="sxs-lookup"><span data-stu-id="9b089-127">An ASCII string that uniquely identifies the name of the pass.</span></span>

</dd> <dt>

<span data-ttu-id="9b089-128"><span id="SetStateGroup"></span><span id="setstategroup"></span><span id="SETSTATEGROUP"></span>*SetStateGroup*</span><span class="sxs-lookup"><span data-stu-id="9b089-128"><span id="SetStateGroup"></span><span id="setstategroup"></span><span id="SETSTATEGROUP"></span>*SetStateGroup*</span></span>
</dt> <dd>

<span data-ttu-id="9b089-129">\[in \] impostare uno o più gruppi di stato, ad esempio:</span><span class="sxs-lookup"><span data-stu-id="9b089-129">\[in\] Set one or more state groups such as:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9b089-130">StateGroup</span><span class="sxs-lookup"><span data-stu-id="9b089-130">StateGroup</span></span></th>
<th><span data-ttu-id="9b089-131">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9b089-131">Syntax</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9b089-132">Stato di Blend</span><span class="sxs-lookup"><span data-stu-id="9b089-132">Blend State</span></span></td>
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

<p><span data-ttu-id="9b089-133">Vedere [<strong>OMSetBlendState</strong>] (/Windows/Desktop/API/D3D10/NF-D3D10-id3d10device-omsetblendstate) per l'elenco di argomenti.</span><span class="sxs-lookup"><span data-stu-id="9b089-133">See [<strong>OMSetBlendState</strong>](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-omsetblendstate) for the argument list.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b089-134">Stato stencil profondità</span><span class="sxs-lookup"><span data-stu-id="9b089-134">Depth-stencil State</span></span></td>
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
<p><span data-ttu-id="9b089-135">Vedere <a href="/windows/desktop/api/D3D10/nf-d3d10-id3d10device-omsetdepthstencilstate"><strong>OMSetDepthStencilState</strong></a> per l'elenco di argomenti.</span><span class="sxs-lookup"><span data-stu-id="9b089-135">See <a href="/windows/desktop/api/D3D10/nf-d3d10-id3d10device-omsetdepthstencilstate"><strong>OMSetDepthStencilState</strong></a> for the argument list.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9b089-136">Stato rasterizzazione</span><span class="sxs-lookup"><span data-stu-id="9b089-136">Rasterizer State</span></span></td>
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
<p><span data-ttu-id="9b089-137">Vedere [<strong>RSSetState</strong>] (/Windows/Desktop/API/D3D10/NF-D3D10-id3d10device-rssetstate) per l'elenco di argomenti.</span><span class="sxs-lookup"><span data-stu-id="9b089-137">See [<strong>RSSetState</strong>](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-rssetstate) for the argument list.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b089-138">Stato dello shader</span><span class="sxs-lookup"><span data-stu-id="9b089-138">Shader State</span></span></td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>SetXXXShader( CompileShader( shader_profile, ShaderFunction( args ) ) );</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p><span data-ttu-id="9b089-139">oppure</span><span class="sxs-lookup"><span data-stu-id="9b089-139">or</span></span></p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>SetXXXShader( CompileShader( NULL ) );</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p><span data-ttu-id="9b089-140">oppure</span><span class="sxs-lookup"><span data-stu-id="9b089-140">or</span></span></p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>SetXXXShader( NULL );</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p><span data-ttu-id="9b089-141">SetXXXShader è uno dei <strong>SetVertexShader</strong>, <strong>SetGeometryShader</strong>o <strong>SetPixelShader</strong> , che sono simili ai metodi API <a href="/windows/desktop/api/D3D10/nf-d3d10-id3d10device-vssetshader"><strong>VSSetShader</strong></a>, <a href="/windows/desktop/api/D3D10/nf-d3d10-id3d10device-gssetshader"><strong>GSSetShader</strong></a>e <a href="/windows/desktop/api/D3D10/nf-d3d10-id3d10device-pssetshader"><strong>PSSetShader</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="9b089-141">SetXXXShader is one of <strong>SetVertexShader</strong>, <strong>SetGeometryShader</strong>, or <strong>SetPixelShader</strong> (which are similar to the API methods <a href="/windows/desktop/api/D3D10/nf-d3d10-id3d10device-vssetshader"><strong>VSSetShader</strong></a>, <a href="/windows/desktop/api/D3D10/nf-d3d10-id3d10device-gssetshader"><strong>GSSetShader</strong></a>, and <a href="/windows/desktop/api/D3D10/nf-d3d10-id3d10device-pssetshader"><strong>PSSetShader</strong></a>).</span></span></p></td>
</tr>
</tbody>
</table>



 

</dd> </dl>

<span data-ttu-id="9b089-142">I gruppi di stati effetti sono elencati in [stato di effetto](d3d10-effect-states.md).</span><span class="sxs-lookup"><span data-stu-id="9b089-142">Effect state groups are listed in [effect state](d3d10-effect-states.md).</span></span>

## <a name="examples"></a><span data-ttu-id="9b089-143">Esempio</span><span class="sxs-lookup"><span data-stu-id="9b089-143">Examples</span></span>

<span data-ttu-id="9b089-144">Questo esempio (dall' [esempio CubeMapGS](https://msdn.microsoft.com/library/Ee416398(v=VS.85).aspx)) imposta lo stato di fusione.</span><span class="sxs-lookup"><span data-stu-id="9b089-144">This example (from [CubeMapGS sample](https://msdn.microsoft.com/library/Ee416398(v=VS.85).aspx)) sets blending state.</span></span>


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



<span data-ttu-id="9b089-145">In questo esempio viene impostato lo stato di rasterizzazione per eseguire il rendering di un oggetto in wireframe.</span><span class="sxs-lookup"><span data-stu-id="9b089-145">This example sets up the rasterizer state to render an object in wireframe.</span></span>


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



<span data-ttu-id="9b089-146">Questo esempio imposta lo stato dello shader (dall' [esempio BasicHLSL10](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx)); che usa un vertice e pixel shader.</span><span class="sxs-lookup"><span data-stu-id="9b089-146">This example sets shader state (from [BasicHLSL10 sample](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx)); which uses a vertex and pixel shader.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="9b089-147">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9b089-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b089-148">Formato effetto</span><span class="sxs-lookup"><span data-stu-id="9b089-148">Effect Format</span></span>](d3d10-effect-format.md)
</dt> </dl>

 

 



