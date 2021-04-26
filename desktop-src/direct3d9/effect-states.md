---
description: Gli stati degli effetti vengono usati per inizializzare gli stati della pipeline in preparazione per l'elaborazione di vertici e pixel.
ms.assetid: b62a6ccc-a1ea-455c-9659-544d4bcaf6a2
title: Stati di effetto (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fe92661fda82bd7dfa47ead0061ef8606e422a2
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998868"
---
# <a name="effect-states-direct3d-9"></a>Stati di effetto (Direct3D 9)

Gli stati degli effetti vengono usati per inizializzare gli stati della pipeline in preparazione per l'elaborazione di vertici e pixel.


```
effect state [ [index] ] = expression;
```



Dove:

-   stato dell'effetto: simile agli stati tradizionali della pipeline di funzioni fisse. Di seguito è riportato un elenco completo degli stati.
-   \[\[ \] index \] - Indice integer facoltativo. L'indice identifica uno stato specifico all'interno di una matrice di stati di effetto. Le parentesi esterne indicano che un indice è facoltativo. Se viene usato un indice, assicurarsi di usare le parentesi interne.
-   expression : espressione di assegnazione di stato. Vedere [Espressioni (Direct3D 9).](expressions.md)

Ogni stato ha un tipo di dati nativo. Si tratta del tipo di dati in cui lo stato prevede valori quando vengono assegnati dall'effetto. I tipi di dati previsti per ogni stato sono elencati di seguito.

Si noti che l'interfaccia dell'effetto tenterà di eseguire il cast dei valori nel tipo appropriato il prima possibile. È possibile eseguire il cast dei valori letterali in fase di compilazione. Quando vengono chiamati i metodi Set appropriati, è necessario eseguire il cast dei valori non letterali (ad esempio variabili regolari). Ad esempio, l'interfaccia dell'effetto esegue il cast dei valori impostati usando [**SetBool**](id3dxbaseeffect--setbool.md), [**SetValue**](id3dxbaseeffect--setvalue.md)e altre funzioni simili, se necessario. Per ottenere prestazioni migliori, assicurarsi che i valori passati all'interfaccia dell'effetto siano già del tipo corretto e che non sia necessario eseguire il cast. Se il runtime non è in grado di eseguire il cast di un valore, viene restituito un errore.

Gli stati degli effetti possono essere suddivisi nelle categorie seguenti:

-   [Stati di luce](#light-states)
-   [Stati dei materiali](#material-states)
-   [Stati di rendering](#render-states)
    -   [Stati di rendering della pipe pixel](#pixel-pipe-render-states)
    -   [Stati di rendering della pipe di vertice](#vertex-pipe-render-states)
-   [Stati del campionatore](#sampler-states)
-   [Stati della fase del campionatore](#sampler-stage-states)
-   [Stati dello shader](#shader-states)
-   [Stati costanti shader](#shader-constant-states)
-   [Stati di trama](#texture-states)
-   [Stati della fase di trama](#texture-stage-states)
-   [Stati di trasformazione](#transform-states)

## <a name="light-states"></a>Stati di luce

Per abilitare le prestazioni migliori per l'applicazione di un effetto, tutti i componenti di una luce o di un materiale devono essere specificati nel file dell'effetto. Gli stati che non è possibile dichiarare sono impostati su un valore predefinito perché Direct3D non è in grado di impostare singolarmente gli stati di luce.



| Stato chiaro            | Tipo   | Valori                                                                                                              |
|------------------------|--------|---------------------------------------------------------------------------------------------------------------------|
| LightAmbient \[ n\]      | float4 | Vedere il membro ambiente di [**D3DLIGHT9**](d3dlight9.md).                                                           |
| LightAttenuation0 \[ n\] | float  | Vedere il membro Attenuation0 di [**D3DLIGHT9.**](d3dlight9.md)                                                      |
| LightAttenuation1 \[ n\] | float  | Vedere il membro Attenuation1 di [**D3DLIGHT9.**](d3dlight9.md)                                                      |
| LightAttenuation2 \[ n\] | float  | Vedere il membro Attenuation2 di [**D3DLIGHT9.**](d3dlight9.md)                                                      |
| LightDiffuse \[ n\]      | float4 | Vedere il membro Diffuse di [**D3DLIGHT9.**](d3dlight9.md)                                                           |
| LightDirection \[ n\]    | float3 | Vedere il membro Direction di [**D3DLIGHT9.**](d3dlight9.md)                                                         |
| LightEnable \[ n\]       | bool   | **TRUE** o **FALSE.** Vedere l'argomento bEnable in [**LightEnable**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-lightenable).            |
| LightFalloff \[ n\]      | float  | [**D3DCOLORVALUE**](d3dcolorvalue.md). Vedere il membro Falloff di [**D3DLIGHT9.**](d3dlight9.md)                   |
| LightPhi \[ n\]          | float  | Vedere il membro Phi di [**D3DLIGHT9.**](d3dlight9.md)                                                               |
| LightPosition \[ n\]     | float3 | Vedere il membro Position di [**D3DLIGHT9.**](d3dlight9.md)                                                          |
| LightRange \[ n\]        | float  | Vedere il membro Range di [**D3DLIGHT9.**](d3dlight9.md)                                                             |
| LightSpecular \[ n\]     | float4 | Vedere il membro Specular di [**D3DLIGHT9.**](d3dlight9.md)                                                          |
| LightTheta \[ n\]        | float  | Vedere il membro Theta di [**D3DLIGHT9.**](d3dlight9.md)                                                             |
| LightType \[ n\]         | dword  | Stesso valore della matrice di un massimo di n [**valori D3DLIGHTTYPE**](./d3dlighttype.md) senza il prefisso D3DLIGHT. \_ |



 

Esempio:


```
LightEnable[0] = TRUE;
LightType[0] = POINT;
LightPosition[0] = float3<10.0f, 1.0f, 23.0f>;
LightAmbient[0] = float4<0.7f, 0.0f, 0.0f, 1.0f>;
```



In questo modo si abiliterà l'illuminazione, si accenderà il tipo, si imposta la posizione della luce su float3<10.0f, 1.0f, 23.0f> e si imposta il colore di ambiente su float4<0,7f, 0,0f, 0,0f, 1,0f>.

## <a name="material-states"></a>Stati dei materiali

Gli stati che non è possibile dichiarare sono impostati su un valore predefinito perché Direct3D non può impostare gli stati dei materiali singolarmente.



| Stato del materiale   | Tipo   | Valori                                         |
|------------------|--------|------------------------------------------------|
| MaterialAmbient  | float4 | Stesso valore di [ **Ambiente**](d3dmaterial9.md)  |
| MaterialDiffuse  | float4 | Stesso valore di [ **Diffuse**](d3dmaterial9.md)  |
| MaterialEmissive | float4 | Stesso valore di [ **Emissive**](d3dmaterial9.md) |
| MaterialPower    | float  | Stesso valore di [ **Power**](d3dmaterial9.md)    |
| MaterialSpecular | float4 | Stesso valore di [ **Specular**](d3dmaterial9.md) |



 

Esempio:


```
MaterialDiffuse = float4<0.7f, 0.0f, 0.0f, 1.0f>;
MaterialPower = 3.0f;
```



Il colore diffuso verrà impostato su float4<0,7f, 0,0f, 0,0f, 1,0f> e la potenza del materiale sarà 3,0f.

## <a name="render-states"></a>Stati di rendering

Esistono due tipi di stati di rendering:

-   [Stati di rendering della pipe pixel](#pixel-pipe-render-states)
-   [Stati di rendering delle pipe dei vertici](#vertex-pipe-render-states)

### <a name="pixel-pipe-render-states"></a>Stati di rendering della pipe pixel

Gli stati di rendering dei file degli effetti hanno nomi simili agli stati della pipeline di funzioni fisse, spesso con il prefisso rimosso.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Stato di rendering</td>
<td>Tipo</td>
<td>Valori</td>
</tr>
<tr class="even">
<td>AlphaBlendEnable</td>
<td>bool</td>
<td>Vero o falso. Gli stessi valori D3DRS_ALPHABLENDENABLE in <a href="/windows/desktop/direct3d9/d3drenderstatetype"><strong>D3DRENDERSTATETYPE</strong></a>.</td>
</tr>
<tr class="odd">
<td>AlphaFunc</td>
<td>dword</td>
<td>Stessi valori di <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> senza il D3DCMP_ predefinito. Vedere D3DRS_ALPHAFUNC.</td>
</tr>
<tr class="even">
<td>AlphaRef</td>
<td>dword</td>
<td>Stessi valori di D3DRS_ALPHAREF.</td>
</tr>
<tr class="odd">
<td>AlphaTestEnable</td>
<td>dword</td>
<td>Vero o falso. Vedere D3DRS_ALPHATESTENABLE.</td>
</tr>
<tr class="even">
<td>BlendOp</td>
<td>dword</td>
<td>Stessi valori di <a href="/windows/desktop/direct3d9/d3dblendop"><strong>D3DBLENDOP</strong></a> senza il D3DBLENDOP_ prefisso.</td>
</tr>
<tr class="odd">
<td>ColorWriteEnable</td>
<td>dword</td>
<td>Combinazione bit per bit di RED| VERDE| BLU| Alfa. Vedere D3DRS_COLORWRITEENABLE.</td>
</tr>
<tr class="even">
<td>DepthBias</td>
<td>float</td>
<td>Stessi valori di D3DRS_DEPTHBIAS.</td>
</tr>
<tr class="odd">
<td>DestBlend</td>
<td>dword</td>
<td>Stessi valori di <a href="/windows/desktop/direct3d9/d3dblend"><strong>D3DBLEND</strong></a> senza il prefisso D3DBLEND_.</td>
</tr>
<tr class="even">
<td>DitherEnable</td>
<td>bool</td>
<td>Vero o falso. Stessi valori di D3DRS_DITHERENABLE.</td>
</tr>
<tr class="odd">
<td>Fillmode</td>
<td>dword</td>
<td>Stessi valori di <a href="/windows/desktop/direct3d9/d3dfillmode"><strong>D3DFILLMODE</strong></a> senza il D3DFILL_ predefinito.</td>
</tr>
<tr class="even">
<td>LastPixel</td>
<td>dword</td>
<td>Vero o falso. Vedere D3DRS_LASTPIXEL.</td>
</tr>
<tr class="odd">
<td>ShadeMode</td>
<td>dword</td>
<td>Stessi valori di <a href="/windows/desktop/direct3d9/d3dshademode"><strong>D3DSHADEMODE</strong></a> senza D3DSHADE_ prefisso.</td>
</tr>
<tr class="even">
<td>SlopeScaleDepthBias</td>
<td>float</td>
<td>Stessi valori di D3DRS_SLOPESCALEDEPTHBIAS.</td>
</tr>
<tr class="odd">
<td>SrcBlend</td>
<td>dword</td>
<td>Stessi valori di <a href="/windows/desktop/direct3d9/d3dblend"><strong>D3DBLEND</strong></a> senza il prefisso D3DBLEND_.</td>
</tr>
<tr class="even">
<td>SRGBWriteEnable</td>
<td>bool</td>
<td>Vero o falso. Stessi valori di D3DRS_SRGBWRITEENABLE.</td>
</tr>
<tr class="odd">
<td>StencilEnable</td>
<td>bool</td>
<td>Vero o falso. Stessi valori di D3DRS_STENCILENABLE.</td>
</tr>
<tr class="even">
<td>StencilFail</td>
<td>dword</td>
<td>Stessi valori di <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> senza il D3DSTENCILCAP_ prefisso. Vedere D3DRS_STENCILFAIL.</td>
</tr>
<tr class="odd">
<td>StencilFunc</td>
<td>dword</td>
<td>Stessi valori di <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> senza il D3DCMP_ predefinito. Vedere D3DRS_STENCILFUNC.</td>
</tr>
<tr class="even">
<td>Maschera di stencil</td>
<td>dword</td>
<td>Stessi valori di D3DRS_STENCILMASK.</td>
</tr>
<tr class="odd">
<td>StencilPass</td>
<td>dword</td>
<td>Stessi valori di <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> senza il D3DSTENCILCAP_ prefisso. Vedere D3DRS_STENCILPASS.</td>
</tr>
<tr class="even">
<td>StencilRef</td>
<td>INT</td>
<td>Stessi valori di D3DRS_STENCILREF.</td>
</tr>
<tr class="odd">
<td>StencilWriteMask</td>
<td>dword</td>
<td>Stessi valori di D3DRS_STENCILWRITEMASK.</td>
</tr>
<tr class="even">
<td>StencilZFail</td>
<td>dword</td>
<td>Stessi valori di <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> senza D3DSTENCILCAP_ prefisso. Vedere D3DRS_STENCILZFAIL.</td>
</tr>
<tr class="odd">
<td>TextureFactor</td>
<td>dword</td>
<td>Stessi valori di <a href="d3dcolor.md"><strong>D3DCOLOR</strong></a>. Stessi valori di D3DRS_TEXTUREFACTOR.</td>
</tr>
<tr class="even">
<td>Wrap0 - Wrap15</td>
<td>dword</td>
<td>I valori sono gli stessi usati da D3DRS_WRAP0. I valori validi sono:
<ul>
<li>COORD0 (che corrisponde a D3DWRAPCOORD_0)</li>
<li>COORD1 (che corrisponde a D3DWRAPCOORD_1)</li>
<li>COORD2 (che corrisponde a D3DWRAPCOORD_2)</li>
<li>COORD3 (che corrisponde a D3DWRAPCOORD_3)</li>
<li>U (che corrisponde a D3DWRAP_U)</li>
<li>V (che corrisponde a D3DWRAP_V)</li>
<li>W (che corrisponde a D3DWRAP_W)</li>
</ul></td>
</tr>
<tr class="odd">
<td>ZEnable</td>
<td>dword</td>
<td>Stessi valori di <a href="/windows/desktop/direct3d9/d3dzbuffertype"><strong>D3DZBUFFERTYPE</strong></a> senza D3DZB_ prefisso.</td>
</tr>
<tr class="even">
<td>ZFunc</td>
<td>dword</td>
<td>Stessi valori di <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> senza il D3DCMP_ predefinito. Vedere D3DRS_ZFUNC.</td>
</tr>
<tr class="odd">
<td>ZWriteEnable</td>
<td>bool</td>
<td>Vero o falso. Vedere D3DRS_ZWRITEENABLE.</td>
</tr>
</tbody>
</table>



 

Esempio:


```
AlphaBlendEnable = TRUE;
FillMode = WIREFRAME;
```



In questo modo verrà abilitata la fusione alfa e verrà eseguito il rendering di tutte le geometrie in wireframe.

### <a name="vertex-pipe-render-states"></a>Stati di rendering delle pipe dei vertici

Gli stati di rendering dei file degli effetti hanno nomi simili agli stati della pipeline di funzioni fisse, spesso con il prefisso rimosso.



| Stato di rendering             | Tipo   | Valori                                                                                                                                        |
|--------------------------|--------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| Di ambiente                  | float4 | Stessi valori dell'ambiente D3DRS \_ AMBIENT.                                                                                                                |
| AmbientMaterialSource    | dword  | Stessi valori di [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) senza il prefisso D3DMCS. \_ Vedere D3DRS \_ AMBIENTMATERIALSOURCE.  |
| Ritaglio                 | bool   | Vero o falso. Stessi valori di D3DRS \_ CLIPPING.                                                                                                |
| ClipPlaneEnable          | dword  | Combinazione bit per bit delle macro D3DCLIPPLANE0 - D3DCLIPPLANE5. Vedere [**D3DCLIPPLANEn**](d3dclipplanen.md) e D3DRS \_ CLIPPLANEENABLE.           |
| ColorVertex              | bool   | Vero o falso. Stessi valori di D3DRS \_ COLORVERTEX.                                                                                             |
| CullMode                 | dword  | Stessi valori di [**D3DCULL**](./d3dcull.md) senza il prefisso D3DCULL. \_                                                                 |
| DiffuseMaterialSource    | dword  | Stessi valori di [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) senza il prefisso D3DMCS. \_ Vedere D3DRS \_ DIFFUSEMATERIALSOURCE.  |
| EmissiveMaterialSource   | dword  | Stessi valori di [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) senza il prefisso D3DMCS. \_ Vedere D3DRS \_ EMISSIVEMATERIALSOURCE. |
| Colore della taschia                 | dword  | Stessi valori di [**D3DCOLOR**](d3dcolor.md). Vedere D3DRS \_ FOGCOLOR.                                                                             |
| FogDensity               | float  | Stessi valori di D3DRS \_ FOGDENSITY.                                                                                                             |
| Non si può fare altro che non essere in tempo                | bool   | Vero o falso. Stessi valori di D3DRS \_ FOGENABLE.                                                                                               |
| NebbieEnd                   | float  | Stessi valori di D3DRS \_ FOGEND.                                                                                                                 |
| NebbieStart                 | float  | Stessi valori di D3DRS \_ FOGSTART.                                                                                                               |
| Modalità tabella di gonfiabili             | dword  | Stessi valori di [**D3DFOGMODE**](./d3dfogmode.md). Vedere D3DRS \_ FOGTABLEMODE in [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md).     |
| FogVertexMode            | dword  | Stessi valori di [**D3DFOGMODE**](./d3dfogmode.md) senza il prefisso D3DFOG. \_                                                            |
| IndexedVertexBlendEnable | bool   | Vero o falso. Stessi valori di D3DRS \_ INDEXEDVERTEXBLENDENABLE.                                                                                |
| Luce                 | bool   | Vero o falso. Stessi valori dell'illuminazione \_ D3DRS.                                                                                                |
| Controllo LocalViewer              | bool   | Vero o falso. Stessi valori di D3DRS \_ LOCALVIEWER.                                                                                             |
| MultiSampleAntialias     | bool   | Stessi valori di D3DRS \_ MULTISAMPLEANTIALIAS.                                                                                                   |
| MultiSampleMask          | dword  | Stessi valori di D3DRS \_ MULTISAMPLEMASK.                                                                                                        |
| NormalizeNormals         | bool   | Vero o falso. Stessi valori di D3DRS \_ NORMALIZENORMALS.                                                                                        |
| PatchSegments            | float  | Stessi valori di nSegments in [**SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode).                                                         |
| PointScale \_ A            | float  | Stessi valori di D3DRS \_ POINTSCALE \_ A.                                                                                                          |
| PointScale \_ B            | float  | Stessi valori di D3DRS \_ POINTSCALE \_ B.                                                                                                          |
| PointScale \_ C            | float  | Stessi valori di D3DRS \_ POINTSCALE \_ C.                                                                                                          |
| PointScaleEnable         | bool   | Stessi valori di D3DRS \_ POINTSCALEENABLE.                                                                                                       |
| PointSize                | float  | Stessi valori di D3DRS \_ POINTSIZE.                                                                                                              |
| PointSize \_ Min           | float  | Stessi valori di D3DRS \_ POINTSIZE \_ MIN.                                                                                                         |
| PointSize \_ Max           | float  | Stessi valori di D3DRS \_ POINTSIZE \_ MAX senza il prefisso D3DRS. \_                                                                              |
| PointSpriteEnable        | bool   | Vero o falso. Stessi valori di D3DRS \_ POINTSPRITEENABLE.                                                                                       |
| RangeFogEnable           | bool   | Vero o falso. Stessi valori di D3DRS \_ RANGEFOGENABLE.                                                                                          |
| SpecularEnable           | bool   | Vero o falso. Stessi valori di D3DRS \_ SPECULARENABLE.                                                                                          |
| SpecularMaterialSource   | dword  | Stessi valori di [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) senza il prefisso D3DMCS. \_ Vedere \_ SPECULARMATERIALSOURCE D3DRS. |
| TweenFactor              | float  | Stessi valori di D3DRS \_ TWEENFACTOR.                                                                                                            |
| VertexBlend              | dword  | Stessi valori di [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) senza il prefisso D3DVBF. \_ Vedere \_ VERTEXBLEND D3DRS.                  |



 

Esempio:


```
Ambient = float4<0.7f, 0.0f, 0.0f, 1.0f>;
CullMode = CCW;
FogColor = 0xff0000;
```



In questo modo, il colore di ambiente float4<0.7f, 0.0f, 0.0f, 1.0f>, imposta la modalità di culling del backface in senso antiorario e imposta il colore del colore blu su rosso.

## <a name="sampler-states"></a>Stati del campionatore

Uno stato del campionatore rappresenta un oggetto campionatore.



| State   | Tipo    | Valori                              |
|---------|---------|-------------------------------------|
| Campionatore | Campionatore | **NULL** o blocco di stato del campionatore. |



 

## <a name="sampler-stage-states"></a>Stati delle fasi del campionatore

Gli stati della fase del campionatore vengono usati per campionare le trame. Lo stato del campionatore determina i tipi di filtro e le modalità di indirizzamento della trama.



| Stato del campionatore       | Tipo                         | Valori                                                                                                                            |
|---------------------|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| AddressU \[ 16\]      | dword                        | Stessi valori di [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) senza il prefisso D3DTADDRESS. \_ Vedere D3DSAMP \_ ADDRESSU.      |
| AddressV \[ 16\]      | dword                        | Stessi valori di [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) senza il prefisso D3DTADDRESS. \_ Vedere D3DSAMP \_ ADDRESSV.      |
| AddressW \[ 16\]      | dword                        | Stessi valori di [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) senza il prefisso D3DTADDRESS. \_ Vedere D3DSAMP \_ ADDRESSW.      |
| BorderColor \[ 16\]   | [**D3DCOLOR**](d3dcolor.md) | Stessi valori di [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md) senza il prefisso D3DTEXF. \_ Vedere D3DSAMP \_ BORDERCOLOR. |
| MagFilter \[ 16\]     | dword                        | Stessi valori di [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md) senza il prefisso D3DTEXF. \_ Vedere D3DSAMP \_ MAGFILTER.   |
| MaxAnisotropy \[ 16\] | dword                        | Stessi valori di D3DSAMP \_ MAXANISOTROPY senza il prefisso \_ D3DSAMP.                                                               |
| MaxMipLevel \[ 16\]   | INT                          | Stessi valori di D3DSAMP \_ MAXMIPLEVEL senza il prefisso D3DSAMP. \_                                                                 |
| MinFilter \[ 16\]     | dword                        | Stessi valori di D3DSAMP \_ MINFILTER senza il prefisso D3DSAMP. \_                                                                   |
| MipFilter \[ 16\]     | dword                        | Stessi valori di D3DSAMP \_ MIPFILTER senza il prefisso D3DSAMP. \_                                                                   |
| MipMapLodBias \[ 16\] | float                        | Stessi valori di D3DSAMP \_ MIPMAPLODBIAS senza il prefisso \_ D3DSAMP.                                                               |
| SRGBTexture         | bool                         | Stesso valore di D3DSAMP \_ SRGBTEXTURE senza il prefisso D3DSAMP. \_                                                                   |



 

Esempio:


```
AddressU[0] = CLAMP;
AddressV[0] = CLAMP;
AddressW[0] = CLAMP;
```



Questo fa in modo che i valori UVW siano compresi tra 0 e 1.

## <a name="shader-states"></a>Stati dello shader

Esistono solo due stati di effetto shader: uno associato a un oggetto vertex shader e l'altro associato a un oggetto pixel shader corrente.



| Stato shader | Tipo         | Valori                                                                      |
|--------------|--------------|-----------------------------------------------------------------------------|
| Pixelshader  | Pixelshader  | **NULL,** blocco di assembly, destinazione di compilazione o pixel shader parametro. |
| VertexShader | vertexshader | **NULL,** blocco di assembly, destinazione di compilazione o pixel shader parametro. |



 

Esempio:


```
VertexShader = compile vs_1_1 VSTexture();
PixelShader  = NULL;
```



Verrà compilato VSTexture, un vertex shader definito in precedenza nel file con estensione fx, nel vertex shader versione 1.1 e quindi lo shader compilato verrà impostato come vertex shader. Il pixel shader viene assegnato a **NULL.**

## <a name="shader-constant-states"></a>Stati costanti shader

Gli stati delle costanti shader vengono usati per accedere ai parametri costanti dello shader.



| Stato costante shader | Tipo            | Valori                                       |
|-----------------------|-----------------|----------------------------------------------|
| PixelShaderConstant   | float \[ m \[ n\]\] | m x n matrice di float; m e n sono facoltativi. |
| PixelShaderConstant1  | float4          | Un float 4D.                                |
| PixelShaderConstant2  | float4x2        | Due float 4D.                               |
| PixelShaderConstant3  | float4x3        | Tre float 4D.                             |
| PixelShaderConstant4  | float4x4        | Quattro float 4D.                              |
| PixelShaderConstantB  | bool \[ m \[ n\]\]  | m x n matrice di tipi di dati; m e n sono facoltativi.  |
| PixelShaderConstantI  | int \[ m \[ n\]\]   | m x n matrice di ints. m e n sono facoltativi.   |
| PixelShaderConstantF  | float \[ m \[ n\]\] | m x n matrice di valori float. m e n sono facoltativi. |
| VertexShaderConstant  | float \[ m \[ n\]\] | m x n matrice di valori float. m e n sono facoltativi. |
| VertexShaderConstant1 | float4          | Un float 4D.                                |
| VertexShaderConstant2 | float4x2        | Due float 4D.                               |
| VertexShaderConstant3 | float4x3        | Tre float 4D.                             |
| VertexShaderConstant4 | float4x4        | Quattro float 4D.                              |
| VertexShaderConstantB | bool \[ m \[ n\]\]  | m x n matrice di liste. m e n sono facoltativi.  |
| VertexShaderConstantI | int \[ m \[ n\]\]   | m x n matrice di valori ints. m e n sono facoltativi.   |
| VertexShaderConstantF | float \[ m \[ n\]\] | m x n matrice di valori float. m e n sono facoltativi. |



 

## <a name="texture-states"></a>Stati di trama

Gli stati di trama inizializzano le trame usate dal blender multitexture.



| Stato trama | Tipo    | Valori                            |
|---------------|---------|-----------------------------------|
| Trama \[ 8\]  | trama | **NULL** o un parametro di trama. |



 

## <a name="texture-stage-states"></a>Stati della fase di trama

Gli stati della fase trama configurano le trame e le fasi della trama nel blender multitexture.



| Stato della fase di trama        | Tipo  | Valori                                                                                                                                                    |
|----------------------------|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| AlphaOp \[ 8\]               | dword | Uguale a [**D3DTEXTUREOP**](./d3dtextureop.md) senza il prefisso D3DTOP. \_ Vedere D3DTSS \_ ALPHAOP.                                                      |
| AlphaArg0 \[ 8\]             | dword | Uguale a [D3DTA](d3dta.md) senza il prefisso D3DTA. \_ Vedere D3DTSS \_ ALPHAARG0.                                                                             |
| AlphaArg1 \[ 8\]             | dword | Uguale a [D3DTA](d3dta.md) senza il prefisso D3DTA. \_ Vedere D3DTSS \_ ALPHAARG1.                                                                             |
| AlphaArg2 \[ 8\]             | dword | Uguale a [D3DTA](d3dta.md) senza il prefisso D3DTA. \_ Vedere D3DTSS \_ ALPHAARG2.                                                                             |
| ColorArg0 \[ 8\]             | dword | Uguale a [D3DTA](d3dta.md) senza il prefisso D3DTA. \_ Vedere D3DTSS \_ COLORARG0.                                                                             |
| ColorArg1 \[ 8\]             | dword | Uguale a [D3DTA](d3dta.md) senza il prefisso D3DTA. \_ Vedere D3DTSS \_ COLORARG1.                                                                             |
| ColorArg2 \[ 8\]             | dword | Uguale a [D3DTA](d3dta.md) senza il prefisso D3DTA. \_ Vedere D3DTSS \_ COLORARG2.                                                                             |
| ColorOp \[ 8\]               | dword | Uguale a [**D3DTEXTUREOP**](./d3dtextureop.md) senza il prefisso D3DTOP. \_ Vedere D3DTSS \_ COLOROP.                                                      |
| BumpEnvLScale \[ 8\]         | float | Stessi valori di D3DTSS \_ BUMPENVLSCALE senza il prefisso \_ TCI D3DTSS.                                                                                      |
| BumpEnvLOffset \[ 8\]        | float | Stessi valori di D3DTSS \_ BUMPENVLOFFSET senza il prefisso \_ TCI D3DTSS.                                                                                     |
| BumpEnvMat00 \[ 8\]          | float | Stessi valori di D3DTSS \_ BUMPENVMAT00.                                                                                                                      |
| BumpEnvMat01 \[ 8\]          | float | Stessi valori di D3DTSS \_ BUMPENVMAT01.                                                                                                                      |
| BumpEnvMat10 \[ 8\]          | float | Stessi valori di D3DTSS \_ BUMPENVMAT10.                                                                                                                      |
| BumpEnvMat11 \[ 8\]          | float | Stessi valori di D3DTSS \_ BUMPENVMAT11.                                                                                                                      |
| ResultArg \[ 8\]             | dword | Uguale a [D3DTA](d3dta.md) senza il prefisso D3DTA. \_ Vedere D3DTSS \_ RESULTARG.                                                                             |
| TexCoordIndex \[ 8\]         | dword | Stessi valori di D3DTSS \_ TEXCOORDINDEX senza il prefisso \_ TCI D3DTSS.                                                                                      |
| TextureTransformFlags \[ 8\] | dword | Stessi valori dei [**valori D3DTEXTURETRANSFORMFLAGS**](./d3dtexturetransformflags.md) senza il prefisso D3DTTFF. \_ Vedere \_ TEXTURETRANSFORMFLAGS D3DTSS. |



 

## <a name="transform-states"></a>Stati di trasformazione

Impostare gli stati di trasformazione per inizializzare le matrici di trasformazione. Gli effetti usano matrici trasposte per migliorare l'efficienza. È possibile fornire matrici trasposte a un effetto oppure un effetto trassporrà automaticamente le matrici prima di usarle.



| Stato trasformazione       | Tipo     | Valori                                                                                                                          |
|-----------------------|----------|---------------------------------------------------------------------------------------------------------------------------------|
| ProjectionTransform   | float4x4 | Matrice 4x4 di valori float. Stessi valori di D3DTS \_ PROJECTION senza il prefisso D3DTS. \_                                            |
| TextureTransform \[ 8\] | float4x4 | Matrice 4x4 di valori float. Stessi valori di [**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md) senza il prefisso D3DTS. \_ |
| ViewTransform         | float4x4 | Matrice 4x4 di valori float. Stessi valori di D3DTS \_ VIEW senza il prefisso D3DTS. \_                                                  |
| WorldTransform        | float4x4 | Matrice 4x4 di valori float.                                                                                                         |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Formato effetto](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 
