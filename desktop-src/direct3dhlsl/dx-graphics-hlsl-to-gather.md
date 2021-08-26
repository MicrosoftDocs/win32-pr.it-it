---
title: Gather (oggetto Texture HLSL DirectX)
description: Ottiene i quattro campioni (solo componente rosso) che verrebbero usati per l'interpolazione bilineare durante il campionamento di una trama.
ms.assetid: a394d8c2-99cc-4a38-9ac9-34afc666ebe0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bf364bc9d8feac199235319639ab5be8b851de4b
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2021
ms.locfileid: "122626957"
---
# <a name="gather-directx-hlsl-texture-object"></a>Gather (oggetto Texture HLSL DirectX)

Ottiene i quattro campioni (solo componente rosso) che verrebbero usati per l'interpolazione bilineare durante il campionamento di una trama.

&lt;Template Type &gt; 4 Object.Gather( sampler \_ state S, float2 \| 3 \| 4 Location \[ , int2 Offset \] );



 

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
<td>Sono supportati <a href="dx-graphics-hlsl-to-type.md">i tipi di oggetto</a> trama seguenti: Texture2D, Texture2DArray, TextureCube, TextureCubeArray.<br/></td>
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
<td>Texture2D</td>
<td>float2</td>
</tr>
<tr class="even">
<td>Texture2DArray, TextureCube</td>
<td>float3</td>
</tr>
<tr class="odd">
<td>TextureCubeArray </td>
<td>float4</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><p><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Compensare</em></p></td>
<td><p>[in] Offset facoltativo delle coordinate della trama, che può essere usato per qualsiasi tipo di oggetto trama. L'offset viene applicato alla posizione prima del campionamento. Il tipo di argomento dipende dal tipo di oggetto trama. Per gli shader che hanno come destinazione il modello shader 5.0 e versione superiore, i 6 bit meno significativi di ogni valore di offset vengono rispettati come valore con segno, producendo un intervallo [-32..31]. Per gli shader del modello di shader precedente, gli offset devono essere numeri interi immediati compresi tra -8 e 7.</p>

<table>
<thead>
<tr class="header">
<th>tipo Texture-Object</th>
<th>Tipo di parametro</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Texture2D, Texture2DArray</td>
<td>int2</td>
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

Vettore a quattro componenti, con quattro componenti di dati rossi, il cui tipo è uguale al tipo di modello della trama.

## <a name="minimum-shader-model"></a>Modello di shader minimo

Questa funzione è supportata nei modelli di shader seguenti.



| vs \_ 4 \_ 0 | vs \_ 4 \_ 1  | ps \_ 4 \_ 0 | ps \_ 4 \_ 1  | gs \_ 4 \_ 0 | gs \_ 4 \_ 1  |
|----------|-----------|----------|-----------|----------|-----------|
|          | x         |          | x         |          | x         |



 

1.  TextureCubeArray è disponibile in Shader Model 4.1 o versione successiva.
2.  Il modello shader 4.1 è disponibile in Direct3D 10.1 o versione successiva.

## <a name="example"></a>Esempio


```
Texture2D<int1> Tex2d;
Texture2DArray<int2> Tex2dArray;
TextureCube<int3> TexCube;
TextureCubeArray<float2> TexCubeArray;

SamplerState s;

int4 main (float4 f : SV_Position) : SV_Target
{
    int2 iOffset = int2(2,3);

    int4 i1 = Tex2d.Gather(s, f.xy);
    int4 i2 = Tex2d.Gather(s, f.xy, iOffset);

    int4 i3 = Tex2dArray.Gather(s, f.xyz);
    int4 i4 = Tex2dArray.Gather(s, f.xyz, iOffset);

    int4 i5 = TexCube.Gather(s, f.xyzw);

    float4 f6 = TexCubeArray.Gather(s, f.xyzw);

    return i1+i2+i3+i4+i5+int4(i6);
}
  
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Oggetto Texture](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 





