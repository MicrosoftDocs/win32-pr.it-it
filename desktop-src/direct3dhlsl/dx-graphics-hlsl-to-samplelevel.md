---
title: SampleLevel (oggetto trama di DirectX HLSL)
description: Esegue il campionamento di una trama usando un offset a livello di mipmap.
ms.assetid: d61426c8-e09f-4e88-99f6-fa96c4a2b58d
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 73cf7bc0c13987099540cecd49519de35b4b7de1
ms.sourcegitcommit: 0d6365d4e852b09a9100d9cfb9a5334922ebf478
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/17/2020
ms.locfileid: "104118698"
---
# <a name="samplelevel-directx-hlsl-texture-object"></a>SampleLevel (oggetto trama di DirectX HLSL)

Esegue il campionamento di una trama usando un offset a livello di mipmap.



|                                                                                                  |
|--------------------------------------------------------------------------------------------------|
| &lt;Tipo &gt; di modello Object. SampleLevel (stato del campionatore \_ , percorso float, LOD float \[ , offset int \] ); |



 

Questa funzione è simile a [Sample](dx-graphics-hlsl-to-sample.md) , ad eccezione del fatto che usa il livello LOD (nell'ultimo componente del parametro location) per scegliere il livello mipmap. Ad esempio, una trama 2D USA i primi due componenti per le coordinate UV e il terzo componente per il livello mipmap.

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
<td>Qualsiasi tipo <a href="dx-graphics-hlsl-to-type.md">di oggetto trama</a> (ad eccezione di Texture2DMS e Texture2DMSArray).<br/></td>
</tr>
<tr class="even">
<td><span id="S"></span><span id="s"></span><em>S</em><br/></td>
<td>in <a href="dx-graphics-hlsl-sampler.md">Stato del campionatore</a>. Si tratta di un oggetto dichiarato in un file di effetti che contiene le assegnazioni di stato.<br/></td>
</tr>
<tr class="odd">
<td><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Percorso</em><br/></td>
<td>in Coordinate di trama. Il tipo di argomento dipende dal tipo di oggetto trama. <br/> 
<table>
<thead>
<tr class="header">
<th>Tipo di Texture-Object</th>
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
<td><p><span id="LOD"></span><span id="lod"></span><em>TRAMA</em></p></td>
<td><p>in Numero che specifica il livello mipmap. Se il valore è = 0, viene usato zero'th (mapping più grande). Il valore frazionario (se fornito) viene usato per interpolare tra due livelli di mipmap.</p></td>
</tr>
<tr class="odd">
<td><p><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Offset</em></p></td>
<td><p>in Offset della coordinata di trama facoltativo che può essere usato per qualsiasi tipo di oggetto trama. l'offset viene applicato al percorso prima del campionamento. Gli offset della trama devono essere statici. Il tipo di argomento dipende dal tipo di oggetto trama. Per altre informazioni, vedere <a href="/windows/win32/direct3dhlsl/dx-graphics-hlsl-to-sample#applying-texture-coordinate-offsets">applicazione degli offset delle coordinate di trama</a>.</p>

<table>
<thead>
<tr class="header">
<th>Tipo di Texture-Object</th>
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
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="return-value"></a>Valore restituito

Il tipo di modello della trama, che può essere un vettore a un solo o più componenti. Il formato è basato sul [**\_ formato DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)della trama.

## <a name="minimum-shader-model"></a>Modello Shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| vs \_ 4 \_ 0 | vs \_ 4 \_ 1  | PS \_ 4 \_ 0 | PS \_ 4 \_ 1  | GS \_ 4 \_ 0 | GS \_ 4 \_ 1  |
|----------|-----------|----------|-----------|----------|-----------|
| x        | x         | x        | x         | x        | x         |



 

1.  TextureCubeArray è disponibile nel modello Shader 4,1 o versione successiva.
2.  Il modello di Shader 4,1 è disponibile in Direct3D 10,1 o versione successiva.

## <a name="example"></a>Esempio

Questo esempio di codice parziale si trova nel file Instancing. FX nell' [esempio Instancing10](https://msdn.microsoft.com/library/Ee416415(v=VS.85).aspx).


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

[Texture-oggetto](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

