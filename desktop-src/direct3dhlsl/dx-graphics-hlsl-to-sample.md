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
# <a name="sample-directx-hlsl-texture-object"></a><span data-ttu-id="ca149-104">Esempio (oggetto trama DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ca149-104">Sample (DirectX HLSL Texture Object)</span></span>

<span data-ttu-id="ca149-105">Campiona una trama.</span><span class="sxs-lookup"><span data-stu-id="ca149-105">Samples a texture.</span></span>

|                                                                                  |
|----------------------------------------------------------------------------------|
| <span data-ttu-id="ca149-106">&lt;Tipo &gt; di modello Object. Sample ( \_ stato campionatore, percorso float \[ , offset int \] );</span><span class="sxs-lookup"><span data-stu-id="ca149-106">&lt;Template Type&gt; Object.Sample( sampler\_state S, float Location \[, int Offset\] );</span></span> |

## <a name="parameters"></a><span data-ttu-id="ca149-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="ca149-107">Parameters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ca149-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="ca149-108">Item</span></span></th>
<th><span data-ttu-id="ca149-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ca149-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ca149-110"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Oggetto</em></span><span class="sxs-lookup"><span data-stu-id="ca149-110"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Object</em></span></span><br/></td>
<td><span data-ttu-id="ca149-111">Qualsiasi tipo <a href="dx-graphics-hlsl-to-type.md">di oggetto trama</a> (ad eccezione di Texture2DMS e Texture2DMSArray).</span><span class="sxs-lookup"><span data-stu-id="ca149-111">Any <a href="dx-graphics-hlsl-to-type.md">texture-object</a> type (except Texture2DMS and Texture2DMSArray).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ca149-112"><span id="S"></span><span id="s"></span><em>S</em></span><span class="sxs-lookup"><span data-stu-id="ca149-112"><span id="S"></span><span id="s"></span><em>S</em></span></span><br/></td>
<td><span data-ttu-id="ca149-113">in <a href="dx-graphics-hlsl-sampler.md">Stato del campionatore</a>.</span><span class="sxs-lookup"><span data-stu-id="ca149-113">[in] A <a href="dx-graphics-hlsl-sampler.md">Sampler state</a>.</span></span> <span data-ttu-id="ca149-114">Si tratta di un oggetto dichiarato in un file di effetti che contiene le assegnazioni di stato.</span><span class="sxs-lookup"><span data-stu-id="ca149-114">This is an object declared in an effect file that contains state assignments.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ca149-115"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Percorso</em></span><span class="sxs-lookup"><span data-stu-id="ca149-115"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Location</em></span></span><br/></td>
<td><span data-ttu-id="ca149-116">in Coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="ca149-116">[in] The texture coordinates.</span></span> <span data-ttu-id="ca149-117">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="ca149-117">The argument type is dependent on the texture-object type.</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="ca149-118">Tipo di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="ca149-118">Texture-Object Type</span></span></th>
<th><span data-ttu-id="ca149-119">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="ca149-119">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ca149-120">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ca149-120">Texture1D</span></span></td>
<td><span data-ttu-id="ca149-121">float</span><span class="sxs-lookup"><span data-stu-id="ca149-121">float</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ca149-122">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="ca149-122">Texture1DArray, Texture2D</span></span></td>
<td><span data-ttu-id="ca149-123">float2</span><span class="sxs-lookup"><span data-stu-id="ca149-123">float2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ca149-124">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="ca149-124">Texture2DArray, Texture3D, TextureCube</span></span></td>
<td><span data-ttu-id="ca149-125">float3</span><span class="sxs-lookup"><span data-stu-id="ca149-125">float3</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ca149-126">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="ca149-126">TextureCubeArray</span></span> </td>
<td><span data-ttu-id="ca149-127">float4</span><span class="sxs-lookup"><span data-stu-id="ca149-127">float4</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ca149-128"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Offset</em></span><span class="sxs-lookup"><span data-stu-id="ca149-128"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Offset</em></span></span></p></td>
<td><p><span data-ttu-id="ca149-129">in Offset della coordinata di trama facoltativo che può essere usato per qualsiasi tipo di oggetto trama. l'offset viene applicato al percorso prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="ca149-129">[in] An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="ca149-130">Gli offset della trama devono essere statici.</span><span class="sxs-lookup"><span data-stu-id="ca149-130">The texture offsets need to be static.</span></span> <span data-ttu-id="ca149-131">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="ca149-131">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="ca149-132">Per altre informazioni, vedere <a href="/windows/win32/direct3dhlsl/dx-graphics-hlsl-to-sample#applying-texture-coordinate-offsets">applicazione degli offset delle coordinate di trama</a>.</span><span class="sxs-lookup"><span data-stu-id="ca149-132">For more info, see <a href="/windows/win32/direct3dhlsl/dx-graphics-hlsl-to-sample#applying-texture-coordinate-offsets">Applying texture coordinate offsets</a>.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="ca149-133">Tipo di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="ca149-133">Texture-Object Type</span></span></th>
<th><span data-ttu-id="ca149-134">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="ca149-134">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ca149-135">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="ca149-135">Texture1D, Texture1DArray</span></span></td>
<td><span data-ttu-id="ca149-136">INT</span><span class="sxs-lookup"><span data-stu-id="ca149-136">int</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ca149-137">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="ca149-137">Texture2D, Texture2DArray</span></span></td>
<td><span data-ttu-id="ca149-138">int2</span><span class="sxs-lookup"><span data-stu-id="ca149-138">int2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ca149-139">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ca149-139">Texture3D</span></span></td>
<td><span data-ttu-id="ca149-140">int3</span><span class="sxs-lookup"><span data-stu-id="ca149-140">int3</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ca149-141">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="ca149-141">TextureCube, TextureCubeArray</span></span> </td>
<td><span data-ttu-id="ca149-142">non supportato</span><span class="sxs-lookup"><span data-stu-id="ca149-142">not supported</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>

## <a name="return-value"></a><span data-ttu-id="ca149-143">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ca149-143">Return value</span></span>

<span data-ttu-id="ca149-144">Il tipo di modello della trama, che può essere un vettore a un solo o più componenti.</span><span class="sxs-lookup"><span data-stu-id="ca149-144">The texture's template type, which may be a single- or multi-component vector.</span></span> <span data-ttu-id="ca149-145">Il formato è basato sul [**\_ formato DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)della trama.</span><span class="sxs-lookup"><span data-stu-id="ca149-145">The format is based on the texture's [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="ca149-146">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="ca149-146">Minimum Shader Model</span></span>

<span data-ttu-id="ca149-147">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="ca149-147">This function is supported in the following shader models.</span></span>

| <span data-ttu-id="ca149-148">vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="ca149-148">vs\_4\_0</span></span> | <span data-ttu-id="ca149-149">vs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="ca149-149">vs\_4\_1</span></span>  | <span data-ttu-id="ca149-150">PS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="ca149-150">ps\_4\_0</span></span> | <span data-ttu-id="ca149-151">PS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="ca149-151">ps\_4\_1</span></span>  | <span data-ttu-id="ca149-152">GS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="ca149-152">gs\_4\_0</span></span> | <span data-ttu-id="ca149-153">GS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="ca149-153">gs\_4\_1</span></span>  |
|----------|-----------|----------|-----------|----------|-----------|
|          |           | <span data-ttu-id="ca149-154">x</span><span class="sxs-lookup"><span data-stu-id="ca149-154">x</span></span>        | <span data-ttu-id="ca149-155">x</span><span class="sxs-lookup"><span data-stu-id="ca149-155">x</span></span>         |          |           |

1.  <span data-ttu-id="ca149-156">TextureCubeArray è disponibile nel modello Shader 4,1 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="ca149-156">TextureCubeArray is available in Shader Model 4.1 or higher.</span></span>
2.  <span data-ttu-id="ca149-157">Il modello di Shader 4,1 è disponibile in Direct3D 10,1 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="ca149-157">Shader Model 4.1 is available in Direct3D 10.1 or higher.</span></span>

## <a name="example"></a><span data-ttu-id="ca149-158">Esempio</span><span class="sxs-lookup"><span data-stu-id="ca149-158">Example</span></span>

<span data-ttu-id="ca149-159">Questo esempio di codice parziale è basato sul file BasicHLSL11. FX nell' [esempio BasicHLSL11](https://github.com/microsoftarchive/msdn-code-gallery-community-a-c/tree/master/Basic%20DXUT%20Win32%20Samples/%5BC%2B%2B%5D-Basic%20DXUT%20Win32%20Samples/C%2B%2B/BasicHLSL11).</span><span class="sxs-lookup"><span data-stu-id="ca149-159">This partial code example is based on the BasicHLSL11.fx file in the [BasicHLSL11 Sample](https://github.com/microsoftarchive/msdn-code-gallery-community-a-c/tree/master/Basic%20DXUT%20Win32%20Samples/%5BC%2B%2B%5D-Basic%20DXUT%20Win32%20Samples/C%2B%2B/BasicHLSL11).</span></span>

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

## <a name="remarks"></a><span data-ttu-id="ca149-160">Commenti</span><span class="sxs-lookup"><span data-stu-id="ca149-160">Remarks</span></span>

<span data-ttu-id="ca149-161">Il campionamento della trama usa la posizione di Texel per cercare un valore di Texel.</span><span class="sxs-lookup"><span data-stu-id="ca149-161">Texture sampling uses the texel position to look up a texel value.</span></span> <span data-ttu-id="ca149-162">Un offset può essere applicato alla posizione prima della ricerca.</span><span class="sxs-lookup"><span data-stu-id="ca149-162">An offset can be applied to the position before lookup.</span></span> <span data-ttu-id="ca149-163">Lo stato del campionatore contiene le opzioni di campionamento e filtro.</span><span class="sxs-lookup"><span data-stu-id="ca149-163">The sampler state contains the sampling and filtering options.</span></span> <span data-ttu-id="ca149-164">Questo metodo può essere richiamato all'interno di una pixel shader, ma non è supportato in un vertex shader o in un geometry shader.</span><span class="sxs-lookup"><span data-stu-id="ca149-164">This method can be invoked within a pixel shader, but it is not supported in a vertex shader or a geometry shader.</span></span>

<span data-ttu-id="ca149-165">Usare un offset solo in un miplevel Integer; in caso contrario, è possibile ottenere risultati diversi a seconda dell'implementazione dell'hardware o delle impostazioni del driver.</span><span class="sxs-lookup"><span data-stu-id="ca149-165">Use an offset only at an integer miplevel; otherwise, you may get different results depending on hardware implementation or driver settings.</span></span>

### <a name="calculating-texel-positions"></a><span data-ttu-id="ca149-166">Calcolo delle posizioni di Texel</span><span class="sxs-lookup"><span data-stu-id="ca149-166">Calculating texel positions</span></span>

<span data-ttu-id="ca149-167">Le coordinate di trama sono valori a virgola mobile che fanno riferimento a dati di trama, noti anche come spazio di trama normalizzato.</span><span class="sxs-lookup"><span data-stu-id="ca149-167">Texture coordinates are floating-point values that reference texture data, which is also known as normalized texture space.</span></span> <span data-ttu-id="ca149-168">Le modalità di wrapping degli indirizzi vengono applicate in questo ordine (coordinate di trama + offset + modalità a capo) per modificare le coordinate di trama al di fuori dell' \[ intervallo 0... 1 \] .</span><span class="sxs-lookup"><span data-stu-id="ca149-168">Address wrapping modes are applied in this order (texture coordinates + offsets + wrap mode) to modify texture coordinates outside the \[0...1\] range.</span></span>

<span data-ttu-id="ca149-169">Per le matrici di trama, un valore aggiuntivo nel parametro location specifica un indice in una matrice di trame.</span><span class="sxs-lookup"><span data-stu-id="ca149-169">For texture arrays, an additional value in the location parameter specifies an index into a texture array.</span></span> <span data-ttu-id="ca149-170">Questo indice viene considerato come valore float scalato, invece dello spazio normalizzato per le coordinate di trama standard.</span><span class="sxs-lookup"><span data-stu-id="ca149-170">This index is treated as a scaled float value (instead of the normalized space for standard texture coordinates).</span></span> <span data-ttu-id="ca149-171">La conversione in un indice Integer viene eseguita nell'ordine seguente (float + round-to-more-even integer + Clamp nell'intervallo di matrici).</span><span class="sxs-lookup"><span data-stu-id="ca149-171">The conversion to an integer index is done in the following order (float + round-to-nearest-even integer + clamp to the array range).</span></span>

### <a name="applying-texture-coordinate-offsets"></a><span data-ttu-id="ca149-172">Applicazione degli offset delle coordinate di trama</span><span class="sxs-lookup"><span data-stu-id="ca149-172">Applying texture coordinate offsets</span></span>

<span data-ttu-id="ca149-173">Il parametro offset modifica le coordinate di trama, nello spazio Texel.</span><span class="sxs-lookup"><span data-stu-id="ca149-173">The offset parameter modifies the texture coordinates, in texel space.</span></span> <span data-ttu-id="ca149-174">Anche se le coordinate di trama sono numeri a virgola mobile normalizzati, l'offset applica un offset intero.</span><span class="sxs-lookup"><span data-stu-id="ca149-174">Even though texture coordinates are normalized floating-point numbers, the offset applies an integer offset.</span></span> <span data-ttu-id="ca149-175">Si noti inoltre che gli offset della trama devono essere statici.</span><span class="sxs-lookup"><span data-stu-id="ca149-175">Also note that the texture offsets need to be static.</span></span>

<span data-ttu-id="ca149-176">Il formato di dati restituito è determinato dal formato di trama.</span><span class="sxs-lookup"><span data-stu-id="ca149-176">The data format returned is determined by the texture format.</span></span> <span data-ttu-id="ca149-177">Se, ad esempio, la risorsa di trama è stata definita con il formato DXGI \_ \_ A8B8G8R8 \_ UNORM \_ sRGB format, l'operazione di campionamento converte i Texel campionati da gamma 2,0 a 1,0, filtra e scrive il risultato come valore a virgola mobile nell'intervallo \[ 0.. 1 \] .</span><span class="sxs-lookup"><span data-stu-id="ca149-177">For example, if the texture resource was defined with the DXGI\_FORMAT\_A8B8G8R8\_UNORM\_SRGB format, the sampling operation converts sampled texels from gamma 2.0 to 1.0, filter, and writes the result as a floating-point value in the range \[0..1\].</span></span>

## <a name="related-topics"></a><span data-ttu-id="ca149-178">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ca149-178">Related topics</span></span>

[<span data-ttu-id="ca149-179">Texture-oggetto</span><span class="sxs-lookup"><span data-stu-id="ca149-179">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
