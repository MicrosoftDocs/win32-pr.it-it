---
title: Esempio (oggetto trama DirectX HLSL)
description: Campiota una trama. | Esempio (oggetto trama DirectX HLSL)
ms.assetid: 788ba4b4-8013-411f-9a19-fb9983386fa0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2374063d222d06576f720fed2aa7fb714bcccf04
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/09/2021
ms.locfileid: "111825748"
---
# <a name="sample-directx-hlsl-texture-object"></a>Esempio (oggetto trama DirectX HLSL)

Campiota una trama.

&lt;Tipo di &gt; modello Object.Sample( sampler \_ state S, float Location , int Offset \[ \] );

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
<td>[in] Stato <a href="dx-graphics-hlsl-sampler.md">del campionatore.</a> Si tratta di un oggetto dichiarato in un file di effetti che contiene assegnazioni di stato.<br/></td>
</tr>
<tr class="odd">
<td><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Posizione</em><br/></td>
<td>[in] Coordinate della trama. Il tipo di argomento dipende dal tipo texture-object. <br/> 
<table>
<thead>
<tr class="header">
<th>Texture-Object tipo</th>
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
<td><p><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>compensare</em></p></td>
<td><p>[in] Offset facoltativo delle coordinate della trama, che può essere usato per qualsiasi tipo di oggetto trama. l'offset viene applicato alla posizione prima del campionamento. Gli offset di trama devono essere statici. Il tipo di argomento dipende dal tipo texture-object. Per altre informazioni, vedere <a href="/windows/win32/direct3dhlsl/dx-graphics-hlsl-to-sample#applying-texture-coordinate-offsets">Applicazione degli offset delle coordinate di trama.</a></p>

<table>
<thead>
<tr class="header">
<th>Texture-Object tipo</th>
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

Tipo di modello della trama, che può essere un vettore singolo o multi-componente. Il formato è basato sul formato [**DXGI \_ della trama.**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)

## <a name="minimum-shader-model"></a>Modello di shader minimo

Questa funzione è supportata nei modelli shader seguenti.

| vs \_ 4 \_ 0 | vs \_ 4 \_ 1  | ps \_ 4 \_ 0 | ps \_ 4 \_ 1  | gs \_ 4 \_ 0 | gs \_ 4 \_ 1  |
|----------|-----------|----------|-----------|----------|-----------|
|          |           | x        | x         |          |           |

1.  TextureCubeArray è disponibile in Shader Model 4.1 o versione successiva.
2.  Shader Model 4.1 è disponibile in Direct3D 10.1 o versione successiva.

## <a name="example"></a>Esempio

Questo esempio di codice parziale è basato sul file BasicHLSL11.fx nell'esempio [BasicHLSL11.](https://github.com/microsoftarchive/msdn-code-gallery-community-a-c/tree/master/Basic%20DXUT%20Win32%20Samples/%5BC%2B%2B%5D-Basic%20DXUT%20Win32%20Samples/C%2B%2B/BasicHLSL11)

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

Il campionamento trame usa la posizione texel per cercare un valore texel. È possibile applicare un offset alla posizione prima della ricerca. Lo stato del campionatore contiene le opzioni di campionamento e filtro. Questo metodo può essere richiamato all'interno di un pixel shader, ma non è supportato in un vertex shader o geometry shader.

Usare un offset solo in corrispondenza di un valore integer miplevel. In caso contrario, è possibile ottenere risultati diversi a seconda dell'implementazione dell'hardware o delle impostazioni del driver.

### <a name="calculating-texel-positions"></a>Calcolo delle posizioni texel

Le coordinate di trama sono valori a virgola mobile che fanno riferimento ai dati della trama, noto anche come spazio trame normalizzato. Le modalità di ritorno a capo degli indirizzi vengono applicate in questo ordine (coordinate trama + offset + modalità di ritorno a capo) per modificare le coordinate di trama al di fuori dell'intervallo \[ 0...1. \]

Per le matrici di trame, un valore aggiuntivo nel parametro location specifica un indice in una matrice di trame. Questo indice viene considerato come un valore float ridimensionato anziché come spazio normalizzato per le coordinate di trama standard. La conversione in un indice integer viene eseguita nell'ordine seguente (float + round-to-nearest-even integer + clamp all'intervallo di matrici).

### <a name="applying-texture-coordinate-offsets"></a>Applicazione degli offset delle coordinate di trama

Il parametro offset modifica le coordinate della trama, nello spazio texel. Anche se le coordinate della trama sono numeri a virgola mobile normalizzati, l'offset applica un offset intero. Si noti anche che gli offset trame devono essere statici.

Il formato dei dati restituito è determinato dal formato della trama. Ad esempio, se la risorsa trama è stata definita con il formato DXGI \_ FORMAT A8B8G8R8 UNORM SRGB, l'operazione di campionamento converte i texel campionati da \_ \_ gamma 2.0 a 1.0, filtra e scrive il risultato come valore a virgola mobile nell'intervallo \_ \[ 0,.1 \] .

## <a name="related-topics"></a>Argomenti correlati

[Oggetto texture](dx-graphics-hlsl-to-type.md)
