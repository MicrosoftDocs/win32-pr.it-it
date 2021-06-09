---
title: SampleGrad (oggetto Texture HLSL DirectX)
description: Campionare una trama usando una sfumatura per influenzare il modo in cui viene calcolata la posizione del campione. | SampleGrad (oggetto Texture HLSL DirectX)
ms.assetid: f3d73296-23c4-4178-b89e-6f84cfcb48a5
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 959304d36da2b95bdf6289fba1b8c75d6ecfa314
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/09/2021
ms.locfileid: "111825738"
---
# <a name="samplegrad-directx-hlsl-texture-object"></a>SampleGrad (oggetto Texture HLSL DirectX)

Campionare una trama usando una sfumatura per influenzare il modo in cui viene calcolata la posizione del campione.

&lt;Template Type &gt; Object.SampleGrad( sampler \_ state S, float Location, float DDX, float DDY \[ , int Offset \] );



 

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
<td><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Oggetto</em><br/></td>
<td>Qualsiasi <a href="dx-graphics-hlsl-to-type.md">tipo di oggetto</a> trama (ad eccezione di Texture2DMS e Texture2DMSArray).<br/></td>
</tr>
<tr class="even">
<td><span id="S"></span><span id="s"></span><em>S</em><br/></td>
<td>[in] Stato <a href="dx-graphics-hlsl-sampler.md">del campionatore.</a> Si tratta di un oggetto dichiarato in un file di effetto che contiene assegnazioni di stato.<br/></td>
</tr>
<tr class="odd">
<td><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Posizione</em><br/></td>
<td>[in] Coordinate della trama. Il tipo di argomento dipende dal tipo di oggetto trama. <br/> 
<table>
<thead>
<tr class="header">
<th>tipo Texture-Object</th>
<th>Tipo di parametro</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Texture1D</td>
<td>float</td>
</tr>
<tr class="even">
<td>Texture1DArray, Texture2D</td>
<td>float2</td>
</tr>
<tr class="odd">
<td>Texture2DArray, Texture3D, TextureCube</td>
<td>float3</td>
</tr>
<tr class="even">
<td>TextureCubeArray </td>
<td>float4</td>
</tr>
<tr class="odd">
<td>Texture2DMS, Texture2DMSArray</td>
<td>non supportato</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><p><span id="DDX"></span><span id="ddx"></span><em>Ddx</em></p></td>
<td><p>[in] Frequenza di modifica della geometria della superficie nella direzione x. Il tipo di argomento dipende dal tipo di oggetto trama.</p>

<table>
<thead>
<tr class="header">
<th>tipo Texture-Object</th>
<th>Tipo di parametro</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Texture1D, Texture1DArray</td>
<td>float</td>
</tr>
<tr class="even">
<td>Texture2D, Texture2DArray</td>
<td>float2</td>
</tr>
<tr class="odd">
<td>Texture3D, TextureCube, TextureCubeArray </td>
<td>float3</td>
</tr>
<tr class="even">
<td>Texture2DMS, Texture2DMSArray</td>
<td>non supportato</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><p><span id="DDY"></span><span id="ddy"></span><em>DDY</em></p></td>
<td><p>[in] Frequenza di modifica della geometria della superficie nella direzione y. Il tipo di argomento dipende dal tipo di oggetto trama.</p>

<table>
<thead>
<tr class="header">
<th>tipo Texture-Object</th>
<th>Tipo di parametro</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Texture1D, Texture1DArray</td>
<td>float</td>
</tr>
<tr class="even">
<td>Texture2D, Texture2DArray</td>
<td>float2</td>
</tr>
<tr class="odd">
<td>Texture3D, TextureCube, TextureCubeArray </td>
<td>float3</td>
</tr>
<tr class="even">
<td>Texture2DMS, Texture2DMSArray</td>
<td>non supportato</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><p><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>compensare</em></p></td>
<td><p>[in] Offset facoltativo delle coordinate della trama, che può essere usato per qualsiasi tipo di oggetto trama. L'offset viene applicato alla posizione prima del campionamento. Usare un offset solo in corrispondenza di un valore integer miplevel; In caso contrario, è possibile che si otterrà un risultato che non si traduce bene in hardware. Il tipo di argomento dipende dal tipo di oggetto trama. Per altre informazioni, vedere<a href="dx-graphics-hlsl-to-sample.md">Applicazione di offset di interi.</a></p>

<table>
<thead>
<tr class="header">
<th>tipo Texture-Object</th>
<th>Tipo di parametro</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Texture1D, Texture1DArray</td>
<td>INT</td>
</tr>
<tr class="even">
<td>Texture2D, Texture2DArray</td>
<td>int2</td>
</tr>
<tr class="odd">
<td>Texture3D</td>
<td>int3</td>
</tr>
<tr class="even">
<td>TextureCube, TextureCubeArray </td>
<td>non supportato</td>
</tr>
<tr class="odd">
<td>Texture2DMS, Texture2DMSArray</td>
<td>non supportato</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="return-value"></a>Valore restituito

Tipo di modello della trama, che può essere un vettore a uno o più componenti. Il formato è basato sul formato [**DXGI \_ della trama.**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)

## <a name="minimum-shader-model"></a>Modello di shader minimo

Questa funzione è supportata nei modelli di shader seguenti.



| vs \_ 4 \_ 0 | vs \_ 4 \_ 1  | ps \_ 4 \_ 0 | ps \_ 4 \_ 1  | gs \_ 4 \_ 0 | gs \_ 4 \_ 1  |
|----------|-----------|----------|-----------|----------|-----------|
| x        | x         | x        | x         | x        | x         |



 

1.  TextureCubeArray è disponibile in Shader Model 4.1 o versione successiva.
2.  Il modello shader 4.1 è disponibile in Direct3D 10.1 o versione successiva.

## <a name="example"></a>Esempio

Questo esempio di codice parziale è dal file MotionBlur.fx in [MotionBlur10 Sample](https://msdn.microsoft.com/library/Ee416417(v=VS.85).aspx).


```
// Object Declarations
Texture2D g_txDiffuse;

SamplerState g_samLinear
{
    Filter = ANISOTROPIC;
    MaxAnisotropy = 8;
    AddressU = Wrap;
    AddressV = Wrap;
};

struct VSSceneOut
{
    float4 Pos : SV_POSITION;
    float4 Color : COLOR0;
    float2 Tex : TEXCOORD;
    float2 Aniso : ANISOTROPY;
};

float4 PSSceneMain( VSSceneOut Input ) : SV_TARGET
{
    float2 ddx = Input.Aniso;
    float2 ddy = Input.Aniso;
    
    // Shader body calling the intrinsic function
    float4 diff = g_txDiffuse.SampleGrad( g_samLinear, Input.Tex, ddx, ddy);
    
    ...
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Oggetto Texture](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

