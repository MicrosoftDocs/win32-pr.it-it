---
title: SampleLevel (oggetto Texture HLSL DirectX)
description: Campio una trama usando un offset a livello di mipmap.
ms.assetid: d61426c8-e09f-4e88-99f6-fa96c4a2b58d
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4249d094f142af8a9015f4e8a3b32d4e39cd42fb
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2021
ms.locfileid: "122629554"
---
# <a name="samplelevel-directx-hlsl-texture-object"></a>SampleLevel (oggetto Texture HLSL DirectX)

Campio una trama usando un offset a livello di mipmap.

&lt;Tipo di &gt; modello Object.SampleLevel( sampler \_ state S, float Location, float LOD \[ , int Offset \] );



 

Questa funzione è simile a [Sample,](dx-graphics-hlsl-to-sample.md) ad eccezione del fatto che usa il livello LOD (nell'ultimo componente del parametro location) per scegliere il livello mipmap. Ad esempio, una trama 2D usa i primi due componenti per le coordinate uv e il terzo componente per il livello mipmap.

## <a name="parameters"></a>Parametri



<table>
<colgroup>
<col  />
<col  />
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
<td>[in] Stato <a href="dx-graphics-hlsl-sampler.md">del campionatore.</a> Si tratta di un oggetto dichiarato in un file degli effetti che contiene assegnazioni di stato.<br/></td>
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
</tbody>
</table>

<p> </p>
<p>Se l'oggetto trama è una matrice, l'ultimo componente è l'indice della matrice.</p></td>
</tr>
<tr class="even">
<td><p><span id="LOD"></span><span id="lod"></span><em>LOD</em></p></td>
<td><p>[in] Numero che specifica il livello mipmap. Se il valore è = 0, viene usato lo zero (mappa principale). Il valore frazionario (se specificato) viene usato per eseguire l'interpolazione tra due livelli mipmap.</p></td>
</tr>
<tr class="odd">
<td><p><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Compensare</em></p></td>
<td><p>[in] Offset facoltativo delle coordinate della trama, che può essere usato per qualsiasi tipo di oggetto trama. L'offset viene applicato alla posizione prima del campionamento. Gli offset di trama devono essere statici. Il tipo di argomento dipende dal tipo di oggetto trama. Per altre informazioni, vedere <a href="/windows/win32/direct3dhlsl/dx-graphics-hlsl-to-sample#applying-texture-coordinate-offsets">Applicazione degli offset delle coordinate di trama.</a></p>

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
<td>int</td>
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

Questo esempio di codice parziale deriva dal file Instancing.fx in [Instancing10 Sample](https://msdn.microsoft.com/library/Ee416415(v=VS.85).aspx).


```
// Object Declarations
Texture1D g_txRandom;

SamplerState g_samPoint
{
    Filter = MIN_MAG_MIP_POINT;
    AddressU = Wrap;
    AddressV = Wrap;
};

    
// Shader body calling the intrinsic function
float3 RandomDir(float fOffset)
{   
    float tCoord = (fOffset) / 300.0;
    return g_txRandom.SampleLevel( g_samPoint, tCoord, 0 );
   ...

```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Oggetto Texture](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

