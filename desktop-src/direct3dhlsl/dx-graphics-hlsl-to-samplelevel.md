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
ms.openlocfilehash: bc3a074641ce5b15a3d837e8bd91dfdae09fe627
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826685"
---
# <a name="samplelevel-directx-hlsl-texture-object"></a><span data-ttu-id="9ee5a-103">SampleLevel (oggetto Texture HLSL DirectX)</span><span class="sxs-lookup"><span data-stu-id="9ee5a-103">SampleLevel (DirectX HLSL Texture Object)</span></span>

<span data-ttu-id="9ee5a-104">Campio una trama usando un offset a livello di mipmap.</span><span class="sxs-lookup"><span data-stu-id="9ee5a-104">Samples a texture using a mipmap-level offset.</span></span>

<span data-ttu-id="9ee5a-105">&lt;Tipo di &gt; modello Object.SampleLevel( sampler \_ state S, float Location, float LOD \[ , int Offset \] );</span><span class="sxs-lookup"><span data-stu-id="9ee5a-105">&lt;Template Type&gt; Object.SampleLevel( sampler\_state S, float Location, float LOD \[, int Offset\] );</span></span>



 

<span data-ttu-id="9ee5a-106">Questa funzione è simile a [Sample,](dx-graphics-hlsl-to-sample.md) ad eccezione del fatto che usa il livello LOD (nell'ultimo componente del parametro location) per scegliere il livello mipmap.</span><span class="sxs-lookup"><span data-stu-id="9ee5a-106">This function is similar to [Sample](dx-graphics-hlsl-to-sample.md) except that it uses the LOD level (in the last component of the location parameter) to choose the mipmap level.</span></span> <span data-ttu-id="9ee5a-107">Ad esempio, una trama 2D usa i primi due componenti per le coordinate uv e il terzo componente per il livello mipmap.</span><span class="sxs-lookup"><span data-stu-id="9ee5a-107">For example, a 2D texture uses the first two components for uv coordinates and the third component for the mipmap level.</span></span>

## <a name="parameters"></a><span data-ttu-id="9ee5a-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="9ee5a-108">Parameters</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9ee5a-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="9ee5a-109">Item</span></span></th>
<th><span data-ttu-id="9ee5a-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9ee5a-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9ee5a-111"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Oggetto</em></span><span class="sxs-lookup"><span data-stu-id="9ee5a-111"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Object</em></span></span><br/></td>
<td><span data-ttu-id="9ee5a-112">Qualsiasi <a href="dx-graphics-hlsl-to-type.md">tipo di oggetto</a> trama (ad eccezione di Texture2DMS e Texture2DMSArray).</span><span class="sxs-lookup"><span data-stu-id="9ee5a-112">Any <a href="dx-graphics-hlsl-to-type.md">texture-object</a> type (except Texture2DMS and Texture2DMSArray).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ee5a-113"><span id="S"></span><span id="s"></span><em>S</em></span><span class="sxs-lookup"><span data-stu-id="9ee5a-113"><span id="S"></span><span id="s"></span><em>S</em></span></span><br/></td>
<td><span data-ttu-id="9ee5a-114">[in] Stato <a href="dx-graphics-hlsl-sampler.md">del campionatore.</a></span><span class="sxs-lookup"><span data-stu-id="9ee5a-114">[in] A <a href="dx-graphics-hlsl-sampler.md">Sampler state</a>.</span></span> <span data-ttu-id="9ee5a-115">Si tratta di un oggetto dichiarato in un file di effetto che contiene assegnazioni di stato.</span><span class="sxs-lookup"><span data-stu-id="9ee5a-115">This is an object declared in an effect file that contains state assignments.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ee5a-116"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Posizione</em></span><span class="sxs-lookup"><span data-stu-id="9ee5a-116"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Location</em></span></span><br/></td>
<td><span data-ttu-id="9ee5a-117">[in] Coordinate della trama.</span><span class="sxs-lookup"><span data-stu-id="9ee5a-117">[in] The texture coordinates.</span></span> <span data-ttu-id="9ee5a-118">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="9ee5a-118">The argument type is dependent on the texture-object type.</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="9ee5a-119">tipo Texture-Object</span><span class="sxs-lookup"><span data-stu-id="9ee5a-119">Texture-Object Type</span></span></th>
<th><span data-ttu-id="9ee5a-120">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="9ee5a-120">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9ee5a-121">Texture1D</span><span class="sxs-lookup"><span data-stu-id="9ee5a-121">Texture1D</span></span></td>
<td><span data-ttu-id="9ee5a-122">float</span><span class="sxs-lookup"><span data-stu-id="9ee5a-122">float</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ee5a-123">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="9ee5a-123">Texture1DArray, Texture2D</span></span></td>
<td><span data-ttu-id="9ee5a-124">float2</span><span class="sxs-lookup"><span data-stu-id="9ee5a-124">float2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ee5a-125">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="9ee5a-125">Texture2DArray, Texture3D, TextureCube</span></span></td>
<td><span data-ttu-id="9ee5a-126">float3</span><span class="sxs-lookup"><span data-stu-id="9ee5a-126">float3</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ee5a-127">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="9ee5a-127">TextureCubeArray</span></span> </td>
<td><span data-ttu-id="9ee5a-128">float4</span><span class="sxs-lookup"><span data-stu-id="9ee5a-128">float4</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="9ee5a-129">Se l'oggetto trama è una matrice, l'ultimo componente è l'indice della matrice.</span><span class="sxs-lookup"><span data-stu-id="9ee5a-129">If the texture object is an array, the last component is the array index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ee5a-130"><span id="LOD"></span><span id="lod"></span><em>Lod</em></span><span class="sxs-lookup"><span data-stu-id="9ee5a-130"><span id="LOD"></span><span id="lod"></span><em>LOD</em></span></span></p></td>
<td><p><span data-ttu-id="9ee5a-131">[in] Numero che specifica il livello mipmap.</span><span class="sxs-lookup"><span data-stu-id="9ee5a-131">[in] A number that specifies the mipmap level.</span></span> <span data-ttu-id="9ee5a-132">Se il valore è = 0, viene usato lo zero (mappa principale).</span><span class="sxs-lookup"><span data-stu-id="9ee5a-132">If the value is = 0, the zero'th (biggest map) is used.</span></span> <span data-ttu-id="9ee5a-133">Il valore frazionario (se specificato) viene usato per eseguire l'interpolazione tra due livelli mipmap.</span><span class="sxs-lookup"><span data-stu-id="9ee5a-133">The fractional value (if supplied) is used to interpolate between two mipmap levels.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ee5a-134"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>compensare</em></span><span class="sxs-lookup"><span data-stu-id="9ee5a-134"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Offset</em></span></span></p></td>
<td><p><span data-ttu-id="9ee5a-135">[in] Offset facoltativo delle coordinate della trama, che può essere usato per qualsiasi tipo di oggetto trama. L'offset viene applicato alla posizione prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="9ee5a-135">[in] An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="9ee5a-136">Gli offset di trama devono essere statici.</span><span class="sxs-lookup"><span data-stu-id="9ee5a-136">The texture offsets need to be static.</span></span> <span data-ttu-id="9ee5a-137">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="9ee5a-137">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="9ee5a-138">Per altre informazioni, vedere <a href="/windows/win32/direct3dhlsl/dx-graphics-hlsl-to-sample#applying-texture-coordinate-offsets">Applicazione degli offset delle coordinate di trama.</a></span><span class="sxs-lookup"><span data-stu-id="9ee5a-138">For more info, see <a href="/windows/win32/direct3dhlsl/dx-graphics-hlsl-to-sample#applying-texture-coordinate-offsets">Applying texture coordinate offsets</a>.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="9ee5a-139">tipo Texture-Object</span><span class="sxs-lookup"><span data-stu-id="9ee5a-139">Texture-Object Type</span></span></th>
<th><span data-ttu-id="9ee5a-140">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="9ee5a-140">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9ee5a-141">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="9ee5a-141">Texture1D, Texture1DArray</span></span></td>
<td><span data-ttu-id="9ee5a-142">INT</span><span class="sxs-lookup"><span data-stu-id="9ee5a-142">int</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ee5a-143">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="9ee5a-143">Texture2D, Texture2DArray</span></span></td>
<td><span data-ttu-id="9ee5a-144">int2</span><span class="sxs-lookup"><span data-stu-id="9ee5a-144">int2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ee5a-145">Texture3D</span><span class="sxs-lookup"><span data-stu-id="9ee5a-145">Texture3D</span></span></td>
<td><span data-ttu-id="9ee5a-146">int3</span><span class="sxs-lookup"><span data-stu-id="9ee5a-146">int3</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ee5a-147">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="9ee5a-147">TextureCube, TextureCubeArray</span></span> </td>
<td><span data-ttu-id="9ee5a-148">non supportato</span><span class="sxs-lookup"><span data-stu-id="9ee5a-148">not supported</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="return-value"></a><span data-ttu-id="9ee5a-149">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9ee5a-149">Return Value</span></span>

<span data-ttu-id="9ee5a-150">Tipo di modello della trama, che può essere un vettore a uno o più componenti.</span><span class="sxs-lookup"><span data-stu-id="9ee5a-150">The texture's template type, which may be a single- or multi-component vector.</span></span> <span data-ttu-id="9ee5a-151">Il formato è basato sul formato [**DXGI \_ della trama.**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)</span><span class="sxs-lookup"><span data-stu-id="9ee5a-151">The format is based on the texture's [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="9ee5a-152">Modello di shader minimo</span><span class="sxs-lookup"><span data-stu-id="9ee5a-152">Minimum Shader Model</span></span>

<span data-ttu-id="9ee5a-153">Questa funzione è supportata nei modelli di shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="9ee5a-153">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="9ee5a-154">vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="9ee5a-154">vs\_4\_0</span></span> | <span data-ttu-id="9ee5a-155">vs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="9ee5a-155">vs\_4\_1</span></span>  | <span data-ttu-id="9ee5a-156">ps \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="9ee5a-156">ps\_4\_0</span></span> | <span data-ttu-id="9ee5a-157">ps \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="9ee5a-157">ps\_4\_1</span></span>  | <span data-ttu-id="9ee5a-158">gs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="9ee5a-158">gs\_4\_0</span></span> | <span data-ttu-id="9ee5a-159">gs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="9ee5a-159">gs\_4\_1</span></span>  |
|----------|-----------|----------|-----------|----------|-----------|
| <span data-ttu-id="9ee5a-160">x</span><span class="sxs-lookup"><span data-stu-id="9ee5a-160">x</span></span>        | <span data-ttu-id="9ee5a-161">x</span><span class="sxs-lookup"><span data-stu-id="9ee5a-161">x</span></span>         | <span data-ttu-id="9ee5a-162">x</span><span class="sxs-lookup"><span data-stu-id="9ee5a-162">x</span></span>        | <span data-ttu-id="9ee5a-163">x</span><span class="sxs-lookup"><span data-stu-id="9ee5a-163">x</span></span>         | <span data-ttu-id="9ee5a-164">x</span><span class="sxs-lookup"><span data-stu-id="9ee5a-164">x</span></span>        | <span data-ttu-id="9ee5a-165">x</span><span class="sxs-lookup"><span data-stu-id="9ee5a-165">x</span></span>         |



 

1.  <span data-ttu-id="9ee5a-166">TextureCubeArray è disponibile in Shader Model 4.1 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="9ee5a-166">TextureCubeArray is available in Shader Model 4.1 or higher.</span></span>
2.  <span data-ttu-id="9ee5a-167">Il modello shader 4.1 è disponibile in Direct3D 10.1 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="9ee5a-167">Shader Model 4.1 is available in Direct3D 10.1 or higher.</span></span>

## <a name="example"></a><span data-ttu-id="9ee5a-168">Esempio</span><span class="sxs-lookup"><span data-stu-id="9ee5a-168">Example</span></span>

<span data-ttu-id="9ee5a-169">Questo esempio di codice parziale deriva dal file Instancing.fx in [Instancing10 Sample](https://msdn.microsoft.com/library/Ee416415(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="9ee5a-169">This partial code example is from the Instancing.fx file in the [Instancing10 Sample](https://msdn.microsoft.com/library/Ee416415(v=VS.85).aspx).</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="9ee5a-170">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9ee5a-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9ee5a-171">Oggetto Texture</span><span class="sxs-lookup"><span data-stu-id="9ee5a-171">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

