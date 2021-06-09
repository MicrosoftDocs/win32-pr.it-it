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
# <a name="sample-directx-hlsl-texture-object"></a><span data-ttu-id="de692-104">Esempio (oggetto trama DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="de692-104">Sample (DirectX HLSL Texture Object)</span></span>

<span data-ttu-id="de692-105">Campiota una trama.</span><span class="sxs-lookup"><span data-stu-id="de692-105">Samples a texture.</span></span>

<span data-ttu-id="de692-106">&lt;Tipo di &gt; modello Object.Sample( sampler \_ state S, float Location , int Offset \[ \] );</span><span class="sxs-lookup"><span data-stu-id="de692-106">&lt;Template Type&gt; Object.Sample( sampler\_state S, float Location \[, int Offset\] );</span></span>

## <a name="parameters"></a><span data-ttu-id="de692-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="de692-107">Parameters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="de692-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="de692-108">Item</span></span></th>
<th><span data-ttu-id="de692-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="de692-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="de692-110"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Oggetto</em></span><span class="sxs-lookup"><span data-stu-id="de692-110"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Object</em></span></span><br/></td>
<td><span data-ttu-id="de692-111">Qualsiasi <a href="dx-graphics-hlsl-to-type.md">tipo di oggetto</a> trama (ad eccezione di Texture2DMS e Texture2DMSArray).</span><span class="sxs-lookup"><span data-stu-id="de692-111">Any <a href="dx-graphics-hlsl-to-type.md">texture-object</a> type (except Texture2DMS and Texture2DMSArray).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="de692-112"><span id="S"></span><span id="s"></span><em>S</em></span><span class="sxs-lookup"><span data-stu-id="de692-112"><span id="S"></span><span id="s"></span><em>S</em></span></span><br/></td>
<td><span data-ttu-id="de692-113">[in] Stato <a href="dx-graphics-hlsl-sampler.md">del campionatore.</a></span><span class="sxs-lookup"><span data-stu-id="de692-113">[in] A <a href="dx-graphics-hlsl-sampler.md">Sampler state</a>.</span></span> <span data-ttu-id="de692-114">Si tratta di un oggetto dichiarato in un file di effetti che contiene assegnazioni di stato.</span><span class="sxs-lookup"><span data-stu-id="de692-114">This is an object declared in an effect file that contains state assignments.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="de692-115"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Posizione</em></span><span class="sxs-lookup"><span data-stu-id="de692-115"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Location</em></span></span><br/></td>
<td><span data-ttu-id="de692-116">[in] Coordinate della trama.</span><span class="sxs-lookup"><span data-stu-id="de692-116">[in] The texture coordinates.</span></span> <span data-ttu-id="de692-117">Il tipo di argomento dipende dal tipo texture-object.</span><span class="sxs-lookup"><span data-stu-id="de692-117">The argument type is dependent on the texture-object type.</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="de692-118">Texture-Object tipo</span><span class="sxs-lookup"><span data-stu-id="de692-118">Texture-Object Type</span></span></th>
<th><span data-ttu-id="de692-119">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="de692-119">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="de692-120">Texture1D</span><span class="sxs-lookup"><span data-stu-id="de692-120">Texture1D</span></span></td>
<td><span data-ttu-id="de692-121">float</span><span class="sxs-lookup"><span data-stu-id="de692-121">float</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="de692-122">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="de692-122">Texture1DArray, Texture2D</span></span></td>
<td><span data-ttu-id="de692-123">float2</span><span class="sxs-lookup"><span data-stu-id="de692-123">float2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="de692-124">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="de692-124">Texture2DArray, Texture3D, TextureCube</span></span></td>
<td><span data-ttu-id="de692-125">float3</span><span class="sxs-lookup"><span data-stu-id="de692-125">float3</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="de692-126">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="de692-126">TextureCubeArray</span></span> </td>
<td><span data-ttu-id="de692-127">float4</span><span class="sxs-lookup"><span data-stu-id="de692-127">float4</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="de692-128"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>compensare</em></span><span class="sxs-lookup"><span data-stu-id="de692-128"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Offset</em></span></span></p></td>
<td><p><span data-ttu-id="de692-129">[in] Offset facoltativo delle coordinate della trama, che può essere usato per qualsiasi tipo di oggetto trama. l'offset viene applicato alla posizione prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="de692-129">[in] An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="de692-130">Gli offset di trama devono essere statici.</span><span class="sxs-lookup"><span data-stu-id="de692-130">The texture offsets need to be static.</span></span> <span data-ttu-id="de692-131">Il tipo di argomento dipende dal tipo texture-object.</span><span class="sxs-lookup"><span data-stu-id="de692-131">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="de692-132">Per altre informazioni, vedere <a href="/windows/win32/direct3dhlsl/dx-graphics-hlsl-to-sample#applying-texture-coordinate-offsets">Applicazione degli offset delle coordinate di trama.</a></span><span class="sxs-lookup"><span data-stu-id="de692-132">For more info, see <a href="/windows/win32/direct3dhlsl/dx-graphics-hlsl-to-sample#applying-texture-coordinate-offsets">Applying texture coordinate offsets</a>.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="de692-133">Texture-Object tipo</span><span class="sxs-lookup"><span data-stu-id="de692-133">Texture-Object Type</span></span></th>
<th><span data-ttu-id="de692-134">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="de692-134">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="de692-135">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="de692-135">Texture1D, Texture1DArray</span></span></td>
<td><span data-ttu-id="de692-136">INT</span><span class="sxs-lookup"><span data-stu-id="de692-136">int</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="de692-137">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="de692-137">Texture2D, Texture2DArray</span></span></td>
<td><span data-ttu-id="de692-138">int2</span><span class="sxs-lookup"><span data-stu-id="de692-138">int2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="de692-139">Texture3D</span><span class="sxs-lookup"><span data-stu-id="de692-139">Texture3D</span></span></td>
<td><span data-ttu-id="de692-140">int3</span><span class="sxs-lookup"><span data-stu-id="de692-140">int3</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="de692-141">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="de692-141">TextureCube, TextureCubeArray</span></span> </td>
<td><span data-ttu-id="de692-142">non supportato</span><span class="sxs-lookup"><span data-stu-id="de692-142">not supported</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>

## <a name="return-value"></a><span data-ttu-id="de692-143">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="de692-143">Return value</span></span>

<span data-ttu-id="de692-144">Tipo di modello della trama, che può essere un vettore singolo o multi-componente.</span><span class="sxs-lookup"><span data-stu-id="de692-144">The texture's template type, which may be a single- or multi-component vector.</span></span> <span data-ttu-id="de692-145">Il formato è basato sul formato [**DXGI \_ della trama.**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)</span><span class="sxs-lookup"><span data-stu-id="de692-145">The format is based on the texture's [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="de692-146">Modello di shader minimo</span><span class="sxs-lookup"><span data-stu-id="de692-146">Minimum Shader Model</span></span>

<span data-ttu-id="de692-147">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="de692-147">This function is supported in the following shader models.</span></span>

| <span data-ttu-id="de692-148">vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="de692-148">vs\_4\_0</span></span> | <span data-ttu-id="de692-149">vs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="de692-149">vs\_4\_1</span></span>  | <span data-ttu-id="de692-150">ps \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="de692-150">ps\_4\_0</span></span> | <span data-ttu-id="de692-151">ps \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="de692-151">ps\_4\_1</span></span>  | <span data-ttu-id="de692-152">gs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="de692-152">gs\_4\_0</span></span> | <span data-ttu-id="de692-153">gs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="de692-153">gs\_4\_1</span></span>  |
|----------|-----------|----------|-----------|----------|-----------|
|          |           | <span data-ttu-id="de692-154">x</span><span class="sxs-lookup"><span data-stu-id="de692-154">x</span></span>        | <span data-ttu-id="de692-155">x</span><span class="sxs-lookup"><span data-stu-id="de692-155">x</span></span>         |          |           |

1.  <span data-ttu-id="de692-156">TextureCubeArray è disponibile in Shader Model 4.1 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="de692-156">TextureCubeArray is available in Shader Model 4.1 or higher.</span></span>
2.  <span data-ttu-id="de692-157">Shader Model 4.1 è disponibile in Direct3D 10.1 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="de692-157">Shader Model 4.1 is available in Direct3D 10.1 or higher.</span></span>

## <a name="example"></a><span data-ttu-id="de692-158">Esempio</span><span class="sxs-lookup"><span data-stu-id="de692-158">Example</span></span>

<span data-ttu-id="de692-159">Questo esempio di codice parziale è basato sul file BasicHLSL11.fx nell'esempio [BasicHLSL11.](https://github.com/microsoftarchive/msdn-code-gallery-community-a-c/tree/master/Basic%20DXUT%20Win32%20Samples/%5BC%2B%2B%5D-Basic%20DXUT%20Win32%20Samples/C%2B%2B/BasicHLSL11)</span><span class="sxs-lookup"><span data-stu-id="de692-159">This partial code example is based on the BasicHLSL11.fx file in the [BasicHLSL11 Sample](https://github.com/microsoftarchive/msdn-code-gallery-community-a-c/tree/master/Basic%20DXUT%20Win32%20Samples/%5BC%2B%2B%5D-Basic%20DXUT%20Win32%20Samples/C%2B%2B/BasicHLSL11).</span></span>

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

## <a name="remarks"></a><span data-ttu-id="de692-160">Commenti</span><span class="sxs-lookup"><span data-stu-id="de692-160">Remarks</span></span>

<span data-ttu-id="de692-161">Il campionamento trame usa la posizione texel per cercare un valore texel.</span><span class="sxs-lookup"><span data-stu-id="de692-161">Texture sampling uses the texel position to look up a texel value.</span></span> <span data-ttu-id="de692-162">È possibile applicare un offset alla posizione prima della ricerca.</span><span class="sxs-lookup"><span data-stu-id="de692-162">An offset can be applied to the position before lookup.</span></span> <span data-ttu-id="de692-163">Lo stato del campionatore contiene le opzioni di campionamento e filtro.</span><span class="sxs-lookup"><span data-stu-id="de692-163">The sampler state contains the sampling and filtering options.</span></span> <span data-ttu-id="de692-164">Questo metodo può essere richiamato all'interno di un pixel shader, ma non è supportato in un vertex shader o geometry shader.</span><span class="sxs-lookup"><span data-stu-id="de692-164">This method can be invoked within a pixel shader, but it is not supported in a vertex shader or a geometry shader.</span></span>

<span data-ttu-id="de692-165">Usare un offset solo in corrispondenza di un valore integer miplevel. In caso contrario, è possibile ottenere risultati diversi a seconda dell'implementazione dell'hardware o delle impostazioni del driver.</span><span class="sxs-lookup"><span data-stu-id="de692-165">Use an offset only at an integer miplevel; otherwise, you may get different results depending on hardware implementation or driver settings.</span></span>

### <a name="calculating-texel-positions"></a><span data-ttu-id="de692-166">Calcolo delle posizioni texel</span><span class="sxs-lookup"><span data-stu-id="de692-166">Calculating texel positions</span></span>

<span data-ttu-id="de692-167">Le coordinate di trama sono valori a virgola mobile che fanno riferimento ai dati della trama, noto anche come spazio trame normalizzato.</span><span class="sxs-lookup"><span data-stu-id="de692-167">Texture coordinates are floating-point values that reference texture data, which is also known as normalized texture space.</span></span> <span data-ttu-id="de692-168">Le modalità di ritorno a capo degli indirizzi vengono applicate in questo ordine (coordinate trama + offset + modalità di ritorno a capo) per modificare le coordinate di trama al di fuori dell'intervallo \[ 0...1. \]</span><span class="sxs-lookup"><span data-stu-id="de692-168">Address wrapping modes are applied in this order (texture coordinates + offsets + wrap mode) to modify texture coordinates outside the \[0...1\] range.</span></span>

<span data-ttu-id="de692-169">Per le matrici di trame, un valore aggiuntivo nel parametro location specifica un indice in una matrice di trame.</span><span class="sxs-lookup"><span data-stu-id="de692-169">For texture arrays, an additional value in the location parameter specifies an index into a texture array.</span></span> <span data-ttu-id="de692-170">Questo indice viene considerato come un valore float ridimensionato anziché come spazio normalizzato per le coordinate di trama standard.</span><span class="sxs-lookup"><span data-stu-id="de692-170">This index is treated as a scaled float value (instead of the normalized space for standard texture coordinates).</span></span> <span data-ttu-id="de692-171">La conversione in un indice integer viene eseguita nell'ordine seguente (float + round-to-nearest-even integer + clamp all'intervallo di matrici).</span><span class="sxs-lookup"><span data-stu-id="de692-171">The conversion to an integer index is done in the following order (float + round-to-nearest-even integer + clamp to the array range).</span></span>

### <a name="applying-texture-coordinate-offsets"></a><span data-ttu-id="de692-172">Applicazione degli offset delle coordinate di trama</span><span class="sxs-lookup"><span data-stu-id="de692-172">Applying texture coordinate offsets</span></span>

<span data-ttu-id="de692-173">Il parametro offset modifica le coordinate della trama, nello spazio texel.</span><span class="sxs-lookup"><span data-stu-id="de692-173">The offset parameter modifies the texture coordinates, in texel space.</span></span> <span data-ttu-id="de692-174">Anche se le coordinate della trama sono numeri a virgola mobile normalizzati, l'offset applica un offset intero.</span><span class="sxs-lookup"><span data-stu-id="de692-174">Even though texture coordinates are normalized floating-point numbers, the offset applies an integer offset.</span></span> <span data-ttu-id="de692-175">Si noti anche che gli offset trame devono essere statici.</span><span class="sxs-lookup"><span data-stu-id="de692-175">Also note that the texture offsets need to be static.</span></span>

<span data-ttu-id="de692-176">Il formato dei dati restituito è determinato dal formato della trama.</span><span class="sxs-lookup"><span data-stu-id="de692-176">The data format returned is determined by the texture format.</span></span> <span data-ttu-id="de692-177">Ad esempio, se la risorsa trama è stata definita con il formato DXGI \_ FORMAT A8B8G8R8 UNORM SRGB, l'operazione di campionamento converte i texel campionati da \_ \_ gamma 2.0 a 1.0, filtra e scrive il risultato come valore a virgola mobile nell'intervallo \_ \[ 0,.1 \] .</span><span class="sxs-lookup"><span data-stu-id="de692-177">For example, if the texture resource was defined with the DXGI\_FORMAT\_A8B8G8R8\_UNORM\_SRGB format, the sampling operation converts sampled texels from gamma 2.0 to 1.0, filter, and writes the result as a floating-point value in the range \[0..1\].</span></span>

## <a name="related-topics"></a><span data-ttu-id="de692-178">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="de692-178">Related topics</span></span>

[<span data-ttu-id="de692-179">Oggetto texture</span><span class="sxs-lookup"><span data-stu-id="de692-179">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
