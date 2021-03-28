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
# <a name="effect-technique-syntax-direct3d-11"></a>Sintassi della tecnica degli effetti (Direct3D 11)

Una tecnica degli effetti viene dichiarata con la sintassi descritta in questa sezione.

Annotazioni di TechniqueVersion *techniquename* \[  <  > \]

{

<dl> passare *le* \[  < *annotazioni* passname > \]  
{
<dl> \[*SetStateGroup*; \] \[ *SetStateGroup*;\]  
...  
\[*SetStateGroup*;\]
</dl> </dd> }  
</dl>

}

## <a name="parameters"></a>Parametri



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Elemento</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="TechniqueVersion"></span><span id="techniqueversion"></span><span id="TECHNIQUEVERSION"></span>TechniqueVersion<br/></td>
<td>Technique10 o technique11. Le tecniche che usano la nuova funzionalità di Direct3D 11 (5_0 shader, BindInterfaces e così via) devono usare technique11.<br/></td>
</tr>
<tr class="even">
<td><span id="TechniqueName"></span><span id="techniquename"></span><span id="TECHNIQUENAME"></span><em>Techniquename</em><br/></td>
<td>facoltativo. Stringa ASCII che identifica in modo univoco il nome della tecnica degli effetti.<br/></td>
</tr>
<tr class="odd">
<td><span id="______________Annotations__"></span><span id="______________annotations__"></span><span id="______________ANNOTATIONS__"></span> <<em>Annotazioni</em> ><br/></td>
<td>[in] Facoltativo. Una o più parti di informazioni (metadati) fornite dall'utente ignorate dal sistema di effetti. Per la sintassi, vedere <a href="d3d11-effect-annotation-syntax.md">sintassi delle annotazioni (Direct3D 11)</a>.<br/></td>
</tr>
<tr class="even">
<td><span id="pass"></span><span id="PASS"></span>passare<br/></td>
<td>Parola chiave required.<br/></td>
</tr>
<tr class="odd">
<td><span id="PassName"></span><span id="passname"></span><span id="PASSNAME"></span><em>Passname</em><br/></td>
<td>[in] Facoltativo. Stringa ASCII che identifica in modo univoco il nome del passaggio.<br/></td>
</tr>
<tr class="even">
<td><span id="SetStateGroup"></span><span id="setstategroup"></span><span id="SETSTATEGROUP"></span><em>SetStateGroup</em><br/></td>
<td>in Impostare uno o più gruppi di Stati, ad esempio: <br/> 
<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>StateGroup</th>
<th>Sintassi</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Stato di Blend</td>
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

<p>Vedere [<strong>sul ID3D11DeviceContext:: OMSetBlendState</strong>] (/Windows/Desktop/API/d3d11/NF-d3d11-ID3D11DeviceContext-omsetblendstate) per l'elenco di argomenti.</p></td>
</tr>
<tr class="even">
<td>Stato stencil profondità</td>
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
<p>Vedere <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetdepthstencilstate"><strong>sul ID3D11DeviceContext:: OMSetDepthStencilState</strong></a> per l'elenco di argomenti.</p></td>
</tr>
<tr class="odd">
<td>Stato rasterizzazione</td>
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
<p>Vedere [<strong>sul ID3D11DeviceContext:: RSSetState</strong>] (/Windows/Desktop/API/d3d11/NF-d3d11-ID3D11DeviceContext-rssetstate) per l'elenco di argomenti.</p></td>
</tr>
<tr class="even">
<td>Stato dello shader</td>
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
<p>SetXXXShader è uno dei SetVertexShader, SetDomainShader, SetHullShader, SetGeometryShader, SetPixelShader o SetComputeShader (che sono simili ai metodi API <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-vssetshader"><strong>sul ID3D11DeviceContext:: VSSetShader</strong></a>, <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dssetshader"><strong>sul ID3D11DeviceContext::D ssetshader</strong></a>, <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetshader"><strong>sul ID3D11DeviceContext:: HSSetShader</strong></a>, <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-gssetshader"><strong>sul id3d11devicecontext:: GSSetShader</strong></a>, <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetshader"><strong>sul ID3D11DeviceContext::P ssetshader</strong></a> e <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-cssetshader"><strong>sul ID3D11DeviceContext:: CSSetShader</strong></a>).</p>
<p>Shader è una variabile shader, che può essere ottenuta in molti modi:</p>
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
<td>Stato destinazione rendering</td>
<td>Uno dei valori possibili:
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
<p>Simile a <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetrendertargets"><strong>sul ID3D11DeviceContext:: OMSetRenderTargets</strong></a>.</p></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="examples"></a>Esempio

Questo esempio imposta lo stato di fusione.


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



In questo esempio viene impostato lo stato di rasterizzazione per eseguire il rendering di un oggetto in wireframe.


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



Questo esempio imposta lo stato dello shader.


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Formato effetto](d3d11-effect-format.md)
</dt> <dt>

[Sintassi del gruppo di effetti (Direct3D 11)](d3d11-effect-group-syntax.md)
</dt> <dt>

[Gruppi di stati effetti](d3d11-effect-states.md)
</dt> </dl>

 

 





