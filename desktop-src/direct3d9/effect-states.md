---
description: Gli Stati degli effetti vengono utilizzati per inizializzare gli Stati della pipeline in preparazione all'elaborazione dei vertici e dei pixel.
ms.assetid: b62a6ccc-a1ea-455c-9659-544d4bcaf6a2
title: Stati degli effetti (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 674e72d818cd280bfe75a2cb02733576bc68319e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104048996"
---
# <a name="effect-states-direct3d-9"></a>Stati degli effetti (Direct3D 9)

Gli Stati degli effetti vengono utilizzati per inizializzare gli Stati della pipeline in preparazione all'elaborazione dei vertici e dei pixel.


```
effect state [ [index] ] = expression;
```



Dove:

-   stato dell'effetto, simile agli Stati tradizionali della pipeline della funzione fissa. Di seguito è riportato un elenco completo di Stati.
-   \[\[ \] indice \] di -Indice integer facoltativo. L'indice identifica un determinato stato all'interno di una matrice di Stati di effetto. Le parentesi esterne indicano che un indice è facoltativo. Se viene utilizzato un indice, assicurarsi di utilizzare le parentesi interne.
-   espressione di assegnazione dello stato di espressione. Vedere [espressioni (Direct3D 9)](expressions.md).

Ogni stato ha un tipo di dati nativo. Si tratta del tipo di dati in cui lo stato prevede che i valori siano presenti quando vengono assegnati dall'effetto. Di seguito sono elencati i tipi di dati previsti da ogni stato.

Si noti che l'interfaccia Effect tenterà di eseguire il cast dei valori nel tipo appropriato il prima possibile. È possibile eseguire il cast dei valori letterali in fase di compilazione. Quando vengono chiamati i metodi set appropriati, è necessario eseguire il cast delle variabili non letterali, ad esempio le variabili regolari. Ad esempio, l'interfaccia Effect eseguirà il cast dei valori impostati utilizzando SetValue, [**SetValue**](id3dxbaseeffect--setvalue.md)e altre funzioni [**simili, se**](id3dxbaseeffect--setbool.md)necessario. Per prestazioni ottimali, assicurarsi che i valori passati all'interfaccia effetto siano già del tipo corretto e che non sia necessario eseguire il cast. Se il runtime non è in grado di eseguire il cast di un valore, viene restituito un errore.

Gli Stati degli effetti possono essere suddivisi nelle categorie seguenti:

-   [Stati leggeri](#light-states)
-   [Stati del materiale](#material-states)
-   [Stati di rendering](#render-states)
    -   [Stati di rendering della pipe pixel](#pixel-pipe-render-states)
    -   [Stati di rendering della pipe del vertice](#vertex-pipe-render-states)
-   [Stati campionatore](#sampler-states)
-   [Stati fase campionatore](#sampler-stage-states)
-   [Stati shader](#shader-states)
-   [Stati costanti shader](#shader-constant-states)
-   [Stati di trama](#texture-states)
-   [Stati della fase trama](#texture-stage-states)
-   [Stati di trasformazione](#transform-states)

## <a name="light-states"></a>Stati leggeri

Per garantire prestazioni ottimali per l'applicazione di un effetto, è necessario specificare nel file degli effetti tutti i componenti di una luce o di un materiale. Gli Stati che non vengono dichiarati sono impostati su un valore predefinito perché non è possibile impostare gli Stati di luce singolarmente da Direct3D.



|                        |        |                                                                                                                     |
|------------------------|--------|---------------------------------------------------------------------------------------------------------------------|
| Stato chiaro            | Tipo   | Valori                                                                                                              |
| LightAmbient \[ n\]      | float4 | Vedere il membro di ambiente di [**D3DLIGHT9**](d3dlight9.md).                                                           |
| LightAttenuation0 \[ n\] | float  | Vedere il membro Attenuation0 di [**D3DLIGHT9**](d3dlight9.md).                                                      |
| LightAttenuation1 \[ n\] | float  | Vedere il membro Attenuation1 di [**D3DLIGHT9**](d3dlight9.md).                                                      |
| LightAttenuation2 \[ n\] | float  | Vedere il membro Attenuation2 di [**D3DLIGHT9**](d3dlight9.md).                                                      |
| LightDiffuse \[ n\]      | float4 | Vedere il membro Diffusion di [**D3DLIGHT9**](d3dlight9.md).                                                           |
| LightDirection \[ n\]    | float3 | Vedere il membro direction di [**D3DLIGHT9**](d3dlight9.md).                                                         |
| N Alleggeribile \[\]       | bool   | **True** o **false**. Vedere l'argomento bEnable in [**schiarente**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-lightenable).            |
| LightFalloff \[ n\]      | float  | [**D3DCOLORVALUE**](d3dcolorvalue.md). Vedere il membro di interruzione di [**D3DLIGHT9**](d3dlight9.md).                   |
| LightPhi \[ n\]          | float  | Vedere il membro Phi di [**D3DLIGHT9**](d3dlight9.md).                                                               |
| Posizioneilluminazione \[ n\]     | float3 | Vedere il membro Position di [**D3DLIGHT9**](d3dlight9.md).                                                          |
| LightRange \[ n\]        | float  | Vedere il membro di intervallo di [**D3DLIGHT9**](d3dlight9.md).                                                             |
| LightSpecular \[ n\]     | float4 | Vedere il membro speculare di [**D3DLIGHT9**](d3dlight9.md).                                                          |
| LightTheta \[ n\]        | float  | Vedere il membro theta di [**D3DLIGHT9**](d3dlight9.md).                                                             |
| LightType \[ n\]         | dword  | Stesso valore della matrice di un massimo di n valori [**D3DLIGHTTYPE**](./d3dlighttype.md) senza il \_ prefisso D3DLIGHT. |



 

Esempio:


```
LightEnable[0] = TRUE;
LightType[0] = POINT;
LightPosition[0] = float3<10.0f, 1.0f, 23.0f>;
LightAmbient[0] = float4<0.7f, 0.0f, 0.0f, 1.0f>;
```



Questa operazione consentirà di accendere il tipo, impostare la posizione della luce su float3<10.0 f, 1.0 f, 23.0 f> e impostare il colore di ambiente su float4<0.7 f, 0,0 f, 0,0 f, 1.0 f>.

## <a name="material-states"></a>Stati del materiale

Gli Stati che non vengono dichiarati sono impostati su un valore predefinito perché non è possibile impostare gli Stati del materiale singolarmente tramite Direct3D.



|                  |        |                                                |
|------------------|--------|------------------------------------------------|
| Stato del materiale   | Tipo   | Valori                                         |
| MaterialAmbient  | float4 | Stesso valore di [ **ambiente**](d3dmaterial9.md)  |
| MaterialDiffuse  | float4 | Stesso valore di [ **Diffusion**](d3dmaterial9.md)  |
| MaterialEmissive | float4 | Stesso valore di [ **emissivo**](d3dmaterial9.md) |
| MaterialPower    | float  | Stesso valore di [ **Power**](d3dmaterial9.md)    |
| MaterialSpecular | float4 | Stesso valore di [ **speculare**](d3dmaterial9.md) |



 

Esempio:


```
MaterialDiffuse = float4<0.7f, 0.0f, 0.0f, 1.0f>;
MaterialPower = 3.0f;
```



Il colore di diffusione verrà impostato su float4<0.7 f, 0,0 f, 0,0 f, 1.0 f> e apporterà la potenza del materiale 3.0 f.

## <a name="render-states"></a>Stati di rendering

Esistono due tipi di Stati di rendering:

-   [Stati di rendering della pipe pixel](#pixel-pipe-render-states)
-   [Stati di rendering della pipe del vertice](#vertex-pipe-render-states)

### <a name="pixel-pipe-render-states"></a>Stati di rendering della pipe pixel

Gli Stati di rendering dei file degli effetti hanno nomi simili agli Stati della pipeline della funzione fissa, spesso con il prefisso rimosso.



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
<td>Vero o falso. Gli stessi valori di D3DRS_ALPHABLENDENABLE in <a href="/windows/desktop/direct3d9/d3drenderstatetype"><strong>D3DRENDERSTATETYPE</strong></a>.</td>
</tr>
<tr class="odd">
<td>AlphaFunc</td>
<td>dword</td>
<td>Gli stessi valori di <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> senza il prefisso D3DCMP_. Vedere D3DRS_ALPHAFUNC.</td>
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
<td>Gli stessi valori di <a href="/windows/desktop/direct3d9/d3dblendop"><strong>D3DBLENDOP</strong></a> senza il prefisso D3DBLENDOP_.</td>
</tr>
<tr class="odd">
<td>ColorWriteEnable</td>
<td>dword</td>
<td>Combinazione bit per bit di rosso | VERDE | BLU | Alfa. Vedere D3DRS_COLORWRITEENABLE.</td>
</tr>
<tr class="even">
<td>DepthBias</td>
<td>float</td>
<td>Stessi valori di D3DRS_DEPTHBIAS.</td>
</tr>
<tr class="odd">
<td>DestBlend</td>
<td>dword</td>
<td>Gli stessi valori di <a href="/windows/desktop/direct3d9/d3dblend"><strong>D3DBLEND</strong></a> senza il prefisso D3DBLEND_.</td>
</tr>
<tr class="even">
<td>DitherEnable</td>
<td>bool</td>
<td>Vero o falso. Stessi valori di D3DRS_DITHERENABLE.</td>
</tr>
<tr class="odd">
<td>FillMode</td>
<td>dword</td>
<td>Gli stessi valori di <a href="/windows/desktop/direct3d9/d3dfillmode"><strong>D3DFILLMODE</strong></a> senza il prefisso D3DFILL_.</td>
</tr>
<tr class="even">
<td>LastPixel</td>
<td>dword</td>
<td>Vero o falso. Vedere D3DRS_LASTPIXEL.</td>
</tr>
<tr class="odd">
<td>MODOOMBRA</td>
<td>dword</td>
<td>Gli stessi valori di <a href="/windows/desktop/direct3d9/d3dshademode"><strong>D3DSHADEMODE</strong></a> senza il prefisso D3DSHADE_.</td>
</tr>
<tr class="even">
<td>SlopeScaleDepthBias</td>
<td>float</td>
<td>Stessi valori di D3DRS_SLOPESCALEDEPTHBIAS.</td>
</tr>
<tr class="odd">
<td>SrcBlend</td>
<td>dword</td>
<td>Gli stessi valori di <a href="/windows/desktop/direct3d9/d3dblend"><strong>D3DBLEND</strong></a> senza il prefisso D3DBLEND_.</td>
</tr>
<tr class="even">
<td>StencilEnable</td>
<td>bool</td>
<td>Vero o falso. Stessi valori di D3DRS_STENCILENABLE.</td>
</tr>
<tr class="odd">
<td>StencilFail</td>
<td>dword</td>
<td>Gli stessi valori di <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> senza il prefisso D3DSTENCILCAP_. Vedere D3DRS_STENCILFAIL.</td>
</tr>
<tr class="even">
<td>StencilFunc</td>
<td>dword</td>
<td>Gli stessi valori di <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> senza il prefisso D3DCMP_. Vedere D3DRS_STENCILFUNC.</td>
</tr>
<tr class="odd">
<td>StencilMask</td>
<td>dword</td>
<td>Stessi valori di D3DRS_STENCILMASK.</td>
</tr>
<tr class="even">
<td>StencilPass</td>
<td>dword</td>
<td>Gli stessi valori di <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> senza il prefisso D3DSTENCILCAP_. Vedere D3DRS_STENCILPASS.</td>
</tr>
<tr class="odd">
<td>StencilRef</td>
<td>INT</td>
<td>Stessi valori di D3DRS_STENCILREF.</td>
</tr>
<tr class="even">
<td>StencilWriteMask</td>
<td>dword</td>
<td>Stessi valori di D3DRS_STENCILWRITEMASK.</td>
</tr>
<tr class="odd">
<td>StencilZFail</td>
<td>dword</td>
<td>Gli stessi valori di <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> senza il prefisso D3DSTENCILCAP_. Vedere D3DRS_STENCILZFAIL.</td>
</tr>
<tr class="even">
<td>TextureFactor</td>
<td>dword</td>
<td>Stessi valori di <a href="d3dcolor.md"><strong>D3DCOLOR</strong></a>. Stessi valori di D3DRS_TEXTUREFACTOR.</td>
</tr>
<tr class="odd">
<td>Wrap0-Wrap15</td>
<td>dword</td>
<td>I valori corrispondono ai valori utilizzati da D3DRS_WRAP0. I valori validi sono:
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
<tr class="even">
<td>ZEnable</td>
<td>dword</td>
<td>Gli stessi valori di <a href="/windows/desktop/direct3d9/d3dzbuffertype"><strong>D3DZBUFFERTYPE</strong></a> senza il prefisso D3DZB_.</td>
</tr>
<tr class="odd">
<td>ZFunc</td>
<td>dword</td>
<td>Gli stessi valori di <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> senza il prefisso D3DCMP_. Vedere D3DRS_ZFUNC.</td>
</tr>
<tr class="even">
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

### <a name="vertex-pipe-render-states"></a>Stati di rendering della pipe del vertice

Gli Stati di rendering dei file degli effetti hanno nomi simili agli Stati della pipeline della funzione fissa, spesso con il prefisso rimosso.



|                          |        |                                                                                                                                               |
|--------------------------|--------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| Stato di rendering             | Tipo   | Valori                                                                                                                                        |
| Di ambiente                  | float4 | Stessi valori dell' \_ ambiente D3DRS.                                                                                                                |
| AmbientMaterialSource    | dword  | Gli stessi valori di [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) senza il \_ prefisso D3DMCS. Vedere D3DRS \_ AMBIENTMATERIALSOURCE.  |
| Ritaglio                 | bool   | Vero o falso. Stessi valori del \_ ritaglio D3DRS.                                                                                                |
| ClipPlaneEnable          | dword  | Combinazione bit per bit di macro D3DCLIPPLANE0-D3DCLIPPLANE5. Vedere [**D3DCLIPPLANEn**](d3dclipplanen.md) e D3DRS \_ CLIPPLANEENABLE.           |
| ColorVertex              | bool   | Vero o falso. Stessi valori di D3DRS \_ COLORVERTEX.                                                                                             |
| CullMode                 | dword  | Gli stessi valori di [**D3DCULL**](./d3dcull.md) senza il \_ prefisso D3DCULL.                                                                 |
| DiffuseMaterialSource    | dword  | Gli stessi valori di [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) senza il \_ prefisso D3DMCS. Vedere D3DRS \_ DIFFUSEMATERIALSOURCE.  |
| EmissiveMaterialSource   | dword  | Gli stessi valori di [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) senza il \_ prefisso D3DMCS. Vedere D3DRS \_ EMISSIVEMATERIALSOURCE. |
| FogColor                 | dword  | Stessi valori di [**D3DCOLOR**](d3dcolor.md). Vedere D3DRS \_ FogColor.                                                                             |
| FogDensity               | float  | Stessi valori di D3DRS \_ FOGDENSITY.                                                                                                             |
| FogEnable                | bool   | Vero o falso. Stessi valori di D3DRS \_ FOGENABLE.                                                                                               |
| FogEnd                   | float  | Stessi valori di D3DRS \_ FOGEND.                                                                                                                 |
| FogStart                 | float  | Stessi valori di D3DRS \_ FOGSTART.                                                                                                               |
| FogTableMode             | dword  | Stessi valori di [**D3DFOGMODE**](./d3dfogmode.md). Vedere D3DRS \_ FOGTABLEMODE in [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md).     |
| FogVertexMode            | dword  | Gli stessi valori di [**D3DFOGMODE**](./d3dfogmode.md) senza il \_ prefisso D3DFOG.                                                            |
| IndexedVertexBlendEnable | bool   | Vero o falso. Stessi valori di D3DRS \_ INDEXEDVERTEXBLENDENABLE.                                                                                |
| Luce                 | bool   | Vero o falso. Stessi valori dell' \_ illuminazione D3DRS.                                                                                                |
| LocalViewer              | bool   | Vero o falso. Stessi valori di D3DRS \_ LOCALVIEWER.                                                                                             |
| MultiSampleAntialias     | bool   | Stessi valori di D3DRS \_ MULTISAMPLEANTIALIAS.                                                                                                   |
| MultiSampleMask          | dword  | Stessi valori di D3DRS \_ MULTISAMPLEMASK.                                                                                                        |
| NormalizeNormals         | bool   | Vero o falso. Stessi valori di D3DRS \_ NORMALIZENORMALS.                                                                                        |
| PatchSegments            | float  | Stessi valori di nSegments in [**SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode).                                                         |
| PointScale \_            | float  | Gli stessi valori di D3DRS \_ POINTSCALE \_ A.                                                                                                          |
| PointScale \_ B            | float  | Stessi valori di D3DRS \_ POINTSCALE \_ B.                                                                                                          |
| PointScale \_ C            | float  | Stessi valori di D3DRS \_ POINTSCALE \_ C.                                                                                                          |
| PointScaleEnable         | bool   | Stessi valori di D3DRS \_ POINTSCALEENABLE.                                                                                                       |
| PointSize                | float  | Stessi valori di D3DRS \_ POINTSIZE.                                                                                                              |
| PointSize \_ min           | float  | Gli stessi valori di D3DRS \_ POINTSIZE \_ min.                                                                                                         |
| PointSize \_ Max           | float  | Gli stessi valori di D3DRS \_ POINTSIZE \_ Max senza il \_ prefisso D3DRS.                                                                              |
| PointSpriteEnable        | bool   | Vero o falso. Stessi valori di D3DRS \_ POINTSPRITEENABLE.                                                                                       |
| RangeFogEnable           | bool   | Vero o falso. Stessi valori di D3DRS \_ RANGEFOGENABLE.                                                                                          |
| SpecularEnable           | bool   | Vero o falso. Stessi valori di D3DRS \_ SPECULARENABLE.                                                                                          |
| SpecularMaterialSource   | dword  | Gli stessi valori di [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) senza il \_ prefisso D3DMCS. Vedere D3DRS \_ SPECULARMATERIALSOURCE. |
| TweenFactor              | float  | Stessi valori di D3DRS \_ TWEENFACTOR.                                                                                                            |
| VertexBlend              | dword  | Gli stessi valori di [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) senza il \_ prefisso D3DVBF. Vedere D3DRS \_ VERTEXBLEND.                  |



 

Esempio:


```
Ambient = float4<0.7f, 0.0f, 0.0f, 1.0f>;
CullMode = CCW;
FogColor = 0xff0000;
```



In questo modo, il colore di ambiente float4<0.7 f, 0,0 f, 0,0 f, 1.0 f>, impostare la modalità di abbattimento della superficie in senso antiorario e impostare il colore di nebbia su rosso.

## <a name="sampler-states"></a>Stati campionatore

Uno stato del campionatore rappresenta un oggetto campionatore.



|         |         |                                     |
|---------|---------|-------------------------------------|
| State   | Tipo    | Valori                              |
| Campionatore | campionatore | **Null** o un blocco di stato del campionatore. |



 

## <a name="sampler-stage-states"></a>Stati fase campionatore

Gli Stati della fase del campionatore vengono usati per campionare le trame. Stato campionatore determina i tipi di filtro e le modalità di indirizzamento della trama.



|                     |                              |                                                                                                                                   |
|---------------------|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| Stato campionatore       | Tipo                         | Valori                                                                                                                            |
| Indirizzo \[ 16\]      | dword                        | Gli stessi valori di [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) senza il \_ prefisso D3DTADDRESS. Vedere D3DSAMP \_ .      |
| AddressV \[ 16\]      | dword                        | Gli stessi valori di [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) senza il \_ prefisso D3DTADDRESS. Vedere D3DSAMP \_ ADDRESSV.      |
| AddressW \[ 16\]      | dword                        | Gli stessi valori di [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) senza il \_ prefisso D3DTADDRESS. Vedere D3DSAMP \_ ADDRESSW.      |
| BorderColor \[ 16\]   | [**D3DCOLOR**](d3dcolor.md) | Gli stessi valori di [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md) senza il \_ prefisso D3DTEXF. Vedere D3DSAMP \_ BorderColor. |
| MagFilter \[ 16\]     | dword                        | Gli stessi valori di [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md) senza il \_ prefisso D3DTEXF. Vedere D3DSAMP \_ MAGFILTER.   |
| MaxAnisotropy \[ 16\] | dword                        | Gli stessi valori di D3DSAMP \_ MAXANISOTROPY senza il \_ prefisso D3DSAMP.                                                               |
| MaxMipLevel \[ 16\]   | INT                          | Gli stessi valori di D3DSAMP \_ MAXMIPLEVEL senza il \_ prefisso D3DSAMP.                                                                 |
| MinFilter \[ 16\]     | dword                        | Gli stessi valori di D3DSAMP \_ MINFILTER senza il \_ prefisso D3DSAMP.                                                                   |
| MipFilter \[ 16\]     | dword                        | Gli stessi valori di D3DSAMP \_ MIPFILTER senza il \_ prefisso D3DSAMP.                                                                   |
| MipMapLodBias \[ 16\] | float                        | Gli stessi valori di D3DSAMP \_ MIPMAPLODBIAS senza il \_ prefisso D3DSAMP.                                                               |
| SRGBTexture         | float                        | Stesso valore di D3DSAMP \_ SRGBTEXTURE senza il \_ prefisso D3DSAMP.                                                                  |



 

Esempio:


```
AddressU[0] = CLAMP;
AddressV[0] = CLAMP;
AddressW[0] = CLAMP;
```



Questo blocca i valori di UVW in modo che siano compresi tra 0 e 1.

## <a name="shader-states"></a>Stati shader

Sono presenti solo due stati Effect shader: uno associato a un oggetto vertex shader e l'altro associato a un oggetto pixel shader.



|              |              |                                                                             |
|--------------|--------------|-----------------------------------------------------------------------------|
| Stato dello shader | Tipo         | Valori                                                                      |
| PixelShader  | PixelShader  | **Null**, un blocco di assembly, una destinazione di compilazione o un parametro pixel shader. |
| VertexShader | vertexshader | **Null**, un blocco di assembly, una destinazione di compilazione o un parametro pixel shader. |



 

Esempio:


```
VertexShader = compile vs_1_1 VSTexture();
PixelShader  = NULL;
```



Questa operazione compilerà VSTexture, un vertex shader definito in precedenza nel file con estensione FX, al vertex shader versione 1,1, quindi imposterà lo shader compilato come vertex shader. Il pixel shader viene assegnato a **null**.

## <a name="shader-constant-states"></a>Stati costanti shader

Gli stati costanti dello shader vengono usati per accedere ai parametri costanti dello shader.



|                       |                 |                                              |
|-----------------------|-----------------|----------------------------------------------|
| Stato costante shader | Tipo            | Valori                                       |
| PixelShaderConstant   | float \[ m \[ n\]\] | matrice m x n di float; m e n sono facoltativi. |
| PixelShaderConstant1  | float4          | Un float 4D.                                |
| PixelShaderConstant2  | float4x2        | Due float 4D.                               |
| PixelShaderConstant3  | float4x3        | Tre float 4D.                             |
| PixelShaderConstant4  | float4x4        | Quattro float 4D.                              |
| PixelShaderConstantB  | bool \[ m \[ n\]\]  | matrice m x n di bool; m e n sono facoltativi.  |
| PixelShaderConstantI  | int \[ m \[ n\]\]   | matrice m x n di int. m e n sono facoltativi.   |
| PixelShaderConstantF  | float \[ m \[ n\]\] | matrice m x n di float. m e n sono facoltativi. |
| VertexShaderConstant  | float \[ m \[ n\]\] | matrice m x n di float. m e n sono facoltativi. |
| VertexShaderConstant1 | float4          | Un float 4D.                                |
| VertexShaderConstant2 | float4x2        | Due float 4D.                               |
| VertexShaderConstant3 | float4x3        | Tre float 4D.                             |
| VertexShaderConstant4 | float4x4        | Quattro float 4D.                              |
| VertexShaderConstantB | bool \[ m \[ n\]\]  | matrice m x n di bool. m e n sono facoltativi.  |
| VertexShaderConstantI | int \[ m \[ n\]\]   | matrice m x n di int. m e n sono facoltativi.   |
| VertexShaderConstantF | float \[ m \[ n\]\] | matrice m x n di float. m e n sono facoltativi. |



 

## <a name="texture-states"></a>Stati di trama

Gli Stati di trama inizializzano le trame usate da multitexture Blender.



|               |         |                                   |
|---------------|---------|-----------------------------------|
| Stato trama | Tipo    | Valori                            |
| Trama \[ 8\]  | trama | **Null** o un parametro texture. |



 

## <a name="texture-stage-states"></a>Stati della fase trama

Gli Stati della fase trama configurano le trame e le fasi di trama in Blender multitexture.



|                            |       |                                                                                                                                                           |
|----------------------------|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Stato della fase trama        | Tipo  | Valori                                                                                                                                                    |
| AlphaOp \[ 8\]               | dword | Uguale a [**D3DTEXTUREOP**](./d3dtextureop.md) senza il \_ prefisso D3DTOP. Vedere D3DTSS \_ ALPHAOP.                                                      |
| AlphaArg0 \[ 8\]             | dword | Uguale a [D3DTA](d3dta.md) senza il \_ prefisso D3DTA. Vedere D3DTSS \_ ALPHAARG0.                                                                             |
| AlphaArg1 \[ 8\]             | dword | Uguale a [D3DTA](d3dta.md) senza il \_ prefisso D3DTA. Vedere D3DTSS \_ ALPHAARG1.                                                                             |
| AlphaArg2 \[ 8\]             | dword | Uguale a [D3DTA](d3dta.md) senza il \_ prefisso D3DTA. Vedere D3DTSS \_ ALPHAARG2.                                                                             |
| ColorArg0 \[ 8\]             | dword | Uguale a [D3DTA](d3dta.md) senza il \_ prefisso D3DTA. Vedere D3DTSS \_ COLORARG0.                                                                             |
| ColorArg1 \[ 8\]             | dword | Uguale a [D3DTA](d3dta.md) senza il \_ prefisso D3DTA. Vedere D3DTSS \_ COLORARG1.                                                                             |
| ColorArg2 \[ 8\]             | dword | Uguale a [D3DTA](d3dta.md) senza il \_ prefisso D3DTA. Vedere D3DTSS \_ COLORARG2.                                                                             |
| ColorOp \[ 8\]               | dword | Uguale a [**D3DTEXTUREOP**](./d3dtextureop.md) senza il \_ prefisso D3DTOP. Vedere D3DTSS \_ COLOROP.                                                      |
| BumpEnvLScale \[ 8\]         | float | Gli stessi valori di D3DTSS \_ BUMPENVLSCALE senza il \_ prefisso D3DTSS TCI.                                                                                      |
| BumpEnvLOffset \[ 8\]        | float | Gli stessi valori di D3DTSS \_ BUMPENVLOFFSET senza il \_ prefisso D3DTSS TCI.                                                                                     |
| BumpEnvMat00 \[ 8\]          | float | Stessi valori di D3DTSS \_ BUMPENVMAT00.                                                                                                                      |
| BumpEnvMat01 \[ 8\]          | float | Stessi valori di D3DTSS \_ BUMPENVMAT01.                                                                                                                      |
| BumpEnvMat10 \[ 8\]          | float | Stessi valori di D3DTSS \_ BUMPENVMAT10.                                                                                                                      |
| BumpEnvMat11 \[ 8\]          | float | Stessi valori di D3DTSS \_ BUMPENVMAT11.                                                                                                                      |
| ResultArg \[ 8\]             | dword | Uguale a [D3DTA](d3dta.md) senza il \_ prefisso D3DTA. Vedere D3DTSS \_ RESULTARG.                                                                             |
| TexCoordIndex \[ 8\]         | dword | Gli stessi valori di D3DTSS \_ TEXCOORDINDEX senza il \_ prefisso D3DTSS TCI.                                                                                      |
| TextureTransformFlags \[ 8\] | dword | Stessi valori dei valori [**D3DTEXTURETRANSFORMFLAGS**](./d3dtexturetransformflags.md) senza il \_ prefisso D3DTTFF. Vedere D3DTSS \_ TEXTURETRANSFORMFLAGS. |



 

## <a name="transform-states"></a>Stati di trasformazione

Impostare gli Stati di trasformazione per inizializzare matrici di trasformazione. Gli effetti utilizzano matrici trasposte per migliorare l'efficienza. È possibile fornire matrici trasposte a un effetto oppure un effetto trasmetterà automaticamente le matrici prima di utilizzarle.



|                       |          |                                                                                                                                 |
|-----------------------|----------|---------------------------------------------------------------------------------------------------------------------------------|
| Stato trasformazione       | Tipo     | Valori                                                                                                                          |
| ProjectionTransform   | float4x4 | Matrice 4x4 di float. Stessi valori della \_ proiezione D3DTS senza il \_ prefisso D3DTS.                                            |
| TextureTransform \[ 8\] | float4x4 | Matrice 4x4 di float. Gli stessi valori di [**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md) senza il \_ prefisso D3DTS. |
| ViewTransform         | float4x4 | Matrice 4x4 di float. Gli stessi valori della \_ vista D3DTS senza il \_ prefisso D3DTS.                                                  |
| WorldTransform        | float4x4 | Matrice 4x4 di float.                                                                                                         |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Formato effetto](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 
