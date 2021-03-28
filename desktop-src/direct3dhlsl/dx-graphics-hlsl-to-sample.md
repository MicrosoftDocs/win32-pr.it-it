---
title: Esempio (oggetto trama DirectX HLSL)
description: Campiona una trama. | Esempio (oggetto trama DirectX HLSL)
ms.assetid: 788ba4b4-8013-411f-9a19-fb9983386fa0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ec80d296025684c1bb67642661a31d8cdc119a53
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995296"
---
# <a name="sample-directx-hlsl-texture-object"></a>Esempio (oggetto trama DirectX HLSL)

Campiona una trama.

|                                                                                  |
|----------------------------------------------------------------------------------|
| &lt;Tipo &gt; di modello Object. Sample ( \_ stato campionatore, percorso float \[ , offset int \] ); |

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

<p> </p></td>
</tr>
<tr class="even">
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
|          |           | x        | x         |          |           |

1.  TextureCubeArray è disponibile nel modello Shader 4,1 o versione successiva.
2.  Il modello di Shader 4,1 è disponibile in Direct3D 10,1 o versione successiva.

## <a name="example"></a>Esempio

Questo esempio di codice parziale è basato sul file BasicHLSL11. FX nell' [esempio BasicHLSL11](https://github.com/microsoftarchive/msdn-code-gallery-community-a-c/tree/master/Basic%20DXUT%20Win32%20Samples/%5BC%2B%2B%5D-Basic%20DXUT%20Win32%20Samples/C%2B%2B/BasicHLSL11).

```
// Object Declarations
Texture2D g_MeshTexture;            // Color texture for mesh

SamplerState MeshTextureSampler
{
    Filter = MIN_MAG_MIP_LINEAR;
    AddressU = Wrap;
    AddressV = Wrap;
};

struct VS_OUTPUT
{
    float4 Position   : SV_POSITION; // vertex position 
    float4 Diffuse    : COLOR0;      // vertex diffuse color (note that COLOR0 is clamped from 0..1)
    float2 TextureUV  : TEXCOORD0;   // vertex texture coords 
};

VS_OUTPUT In;

// Shader body calling the intrinsic function
   ...
        Output.RGBColor = g_MeshTexture.Sample(MeshTextureSampler, In.TextureUV) * In.Diffuse;
```

## <a name="remarks"></a>Commenti

Il campionamento della trama usa la posizione di Texel per cercare un valore di Texel. Un offset può essere applicato alla posizione prima della ricerca. Lo stato del campionatore contiene le opzioni di campionamento e filtro. Questo metodo può essere richiamato all'interno di una pixel shader, ma non è supportato in un vertex shader o in un geometry shader.

Usare un offset solo in un miplevel Integer; in caso contrario, è possibile ottenere risultati diversi a seconda dell'implementazione dell'hardware o delle impostazioni del driver.

### <a name="calculating-texel-positions"></a>Calcolo delle posizioni di Texel

Le coordinate di trama sono valori a virgola mobile che fanno riferimento a dati di trama, noti anche come spazio di trama normalizzato. Le modalità di wrapping degli indirizzi vengono applicate in questo ordine (coordinate di trama + offset + modalità a capo) per modificare le coordinate di trama al di fuori dell' \[ intervallo 0... 1 \] .

Per le matrici di trama, un valore aggiuntivo nel parametro location specifica un indice in una matrice di trame. Questo indice viene considerato come valore float scalato, invece dello spazio normalizzato per le coordinate di trama standard. La conversione in un indice Integer viene eseguita nell'ordine seguente (float + round-to-more-even integer + Clamp nell'intervallo di matrici).

### <a name="applying-texture-coordinate-offsets"></a>Applicazione degli offset delle coordinate di trama

Il parametro offset modifica le coordinate di trama, nello spazio Texel. Anche se le coordinate di trama sono numeri a virgola mobile normalizzati, l'offset applica un offset intero. Si noti inoltre che gli offset della trama devono essere statici.

Il formato di dati restituito è determinato dal formato di trama. Se, ad esempio, la risorsa di trama è stata definita con il formato DXGI \_ \_ A8B8G8R8 \_ UNORM \_ sRGB format, l'operazione di campionamento converte i Texel campionati da gamma 2,0 a 1,0, filtra e scrive il risultato come valore a virgola mobile nell'intervallo \[ 0.. 1 \] .

## <a name="related-topics"></a>Argomenti correlati

[Texture-oggetto](dx-graphics-hlsl-to-type.md)
