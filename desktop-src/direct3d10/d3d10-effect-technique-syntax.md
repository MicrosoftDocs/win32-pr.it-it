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
# <a name="effect-technique-syntax-direct3d-10"></a>Sintassi della tecnica degli effetti (Direct3D 10)

Una tecnica degli effetti viene dichiarata con la sintassi seguente.

annotazioni di technique10 *techniquename* \[  <  > \]

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

<dl> <dt>

<span id="technique10"></span><span id="TECHNIQUE10"></span>technique10
</dt> <dd>

Parola chiave required.

</dd> <dt>

<span id="TechniqueName"></span><span id="techniquename"></span><span id="TECHNIQUENAME"></span>*Techniquename*
</dt> <dd>

facoltativo. Stringa ASCII che identifica in modo univoco il nome della tecnica degli effetti.

</dd> <dt>

<span id="Annotations"></span><span id="annotations"></span><span id="ANNOTATIONS"></span>*Annotazioni*
</dt> <dd>

\[in \] facoltativo. Una o più parti di informazioni (metadati) fornite dall'utente ignorate dal sistema di effetti. Per la sintassi, vedere [sintassi delle annotazioni (Direct3D 10)](d3d10-effect-annotation-syntax.md).

</dd> <dt>

<span id="pass"></span><span id="PASS"></span>passare
</dt> <dd>

Parola chiave required.

</dd> <dt>

<span id="PassName"></span><span id="passname"></span><span id="PASSNAME"></span>*Passname*
</dt> <dd>

\[in \] facoltativo. Stringa ASCII che identifica in modo univoco il nome del passaggio.

</dd> <dt>

<span id="SetStateGroup"></span><span id="setstategroup"></span><span id="SETSTATEGROUP"></span>*SetStateGroup*
</dt> <dd>

\[in \] impostare uno o più gruppi di stato, ad esempio:



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

<p>Vedere [<strong>OMSetBlendState</strong>] (/Windows/Desktop/API/D3D10/NF-D3D10-id3d10device-omsetblendstate) per l'elenco di argomenti.</p></td>
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
<p>Vedere <a href="/windows/desktop/api/D3D10/nf-d3d10-id3d10device-omsetdepthstencilstate"><strong>OMSetDepthStencilState</strong></a> per l'elenco di argomenti.</p></td>
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
<p>Vedere [<strong>RSSetState</strong>] (/Windows/Desktop/API/D3D10/NF-D3D10-id3d10device-rssetstate) per l'elenco di argomenti.</p></td>
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
<td><pre><code>SetXXXShader( CompileShader( shader_profile, ShaderFunction( args ) ) );</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p>oppure</p>
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
<p>oppure</p>
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
<p>SetXXXShader è uno dei <strong>SetVertexShader</strong>, <strong>SetGeometryShader</strong>o <strong>SetPixelShader</strong> , che sono simili ai metodi API <a href="/windows/desktop/api/D3D10/nf-d3d10-id3d10device-vssetshader"><strong>VSSetShader</strong></a>, <a href="/windows/desktop/api/D3D10/nf-d3d10-id3d10device-gssetshader"><strong>GSSetShader</strong></a>e <a href="/windows/desktop/api/D3D10/nf-d3d10-id3d10device-pssetshader"><strong>PSSetShader</strong></a>.</p></td>
</tr>
</tbody>
</table>



 

</dd> </dl>

I gruppi di stati effetti sono elencati in [stato di effetto](d3d10-effect-states.md).

## <a name="examples"></a>Esempio

Questo esempio (dall' [esempio CubeMapGS](https://msdn.microsoft.com/library/Ee416398(v=VS.85).aspx)) imposta lo stato di fusione.


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



Questo esempio imposta lo stato dello shader (dall' [esempio BasicHLSL10](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx)); che usa un vertice e pixel shader.


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

[Formato effetto](d3d10-effect-format.md)
</dt> </dl>

 

 



