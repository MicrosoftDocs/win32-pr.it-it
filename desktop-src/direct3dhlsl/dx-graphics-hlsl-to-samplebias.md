---
title: SampleBias (oggetto trama di DirectX HLSL)
description: Esegue il campionamento di una trama, dopo aver applicato la distorsione di input al livello mipmap.
ms.assetid: 1bc03ad8-7b69-4001-81c7-64d8c631d68d
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e710b8a6c7dd2983c6d0c635d16356f95d0b4fe7
ms.sourcegitcommit: 0d6365d4e852b09a9100d9cfb9a5334922ebf478
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/17/2020
ms.locfileid: "104399995"
---
# <a name="samplebias-directx-hlsl-texture-object"></a><span data-ttu-id="1a0cf-103">SampleBias (oggetto trama di DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1a0cf-103">SampleBias (DirectX HLSL Texture Object)</span></span>

<span data-ttu-id="1a0cf-104">Esegue il campionamento di una trama, dopo aver applicato la distorsione di input al livello mipmap.</span><span class="sxs-lookup"><span data-stu-id="1a0cf-104">Samples a texture, after applying the input bias to the mipmap level.</span></span>



|                                                                                                  |
|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a0cf-105">&lt;Tipo &gt; di modello Object. SampleBias (stato campionatore, \_ percorso float, bias float \[ , offset int \] );</span><span class="sxs-lookup"><span data-stu-id="1a0cf-105">&lt;Template Type&gt; Object.SampleBias( sampler\_state S, float Location, float Bias \[, int Offset\] );</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="1a0cf-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1a0cf-106">Parameters</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1a0cf-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="1a0cf-107">Item</span></span></th>
<th><span data-ttu-id="1a0cf-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1a0cf-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1a0cf-109"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Oggetto</em></span><span class="sxs-lookup"><span data-stu-id="1a0cf-109"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Object</em></span></span><br/></td>
<td><span data-ttu-id="1a0cf-110">Qualsiasi tipo <a href="dx-graphics-hlsl-to-type.md">di oggetto trama</a> (ad eccezione di Texture2DMS e Texture2DMSArray).</span><span class="sxs-lookup"><span data-stu-id="1a0cf-110">Any <a href="dx-graphics-hlsl-to-type.md">texture-object</a> type (except Texture2DMS and Texture2DMSArray).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1a0cf-111"><span id="S"></span><span id="s"></span><em>S</em></span><span class="sxs-lookup"><span data-stu-id="1a0cf-111"><span id="S"></span><span id="s"></span><em>S</em></span></span><br/></td>
<td><span data-ttu-id="1a0cf-112">in <a href="dx-graphics-hlsl-sampler.md">Stato del campionatore</a>.</span><span class="sxs-lookup"><span data-stu-id="1a0cf-112">[in] A <a href="dx-graphics-hlsl-sampler.md">Sampler state</a>.</span></span> <span data-ttu-id="1a0cf-113">Si tratta di un oggetto dichiarato in un file di effetti che contiene le assegnazioni di stato.</span><span class="sxs-lookup"><span data-stu-id="1a0cf-113">This is an object declared in an effect file that contains state assignments.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1a0cf-114"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Percorso</em></span><span class="sxs-lookup"><span data-stu-id="1a0cf-114"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Location</em></span></span><br/></td>
<td><span data-ttu-id="1a0cf-115">in Coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="1a0cf-115">[in] The texture coordinates.</span></span> <span data-ttu-id="1a0cf-116">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="1a0cf-116">The argument type is dependent on the texture-object type.</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1a0cf-117">Tipo di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="1a0cf-117">Texture-Object Type</span></span></th>
<th><span data-ttu-id="1a0cf-118">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="1a0cf-118">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1a0cf-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="1a0cf-119">Texture1D</span></span></td>
<td><span data-ttu-id="1a0cf-120">float</span><span class="sxs-lookup"><span data-stu-id="1a0cf-120">float</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1a0cf-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="1a0cf-121">Texture1DArray, Texture2D</span></span></td>
<td><span data-ttu-id="1a0cf-122">float2</span><span class="sxs-lookup"><span data-stu-id="1a0cf-122">float2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1a0cf-123">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="1a0cf-123">Texture2DArray, Texture3D, TextureCube</span></span></td>
<td><span data-ttu-id="1a0cf-124">float3</span><span class="sxs-lookup"><span data-stu-id="1a0cf-124">float3</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1a0cf-125">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="1a0cf-125">TextureCubeArray</span></span> </td>
<td><span data-ttu-id="1a0cf-126">float4</span><span class="sxs-lookup"><span data-stu-id="1a0cf-126">float4</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1a0cf-127"><span id="Bias"></span><span id="bias"></span><span id="BIAS"></span><em>Distorsione</em></span><span class="sxs-lookup"><span data-stu-id="1a0cf-127"><span id="Bias"></span><span id="bias"></span><span id="BIAS"></span><em>Bias</em></span></span></p></td>
<td><p><span data-ttu-id="1a0cf-128">in Il valore di distorsione, che è un numero a virgola mobile compreso tra-16,0 e 15,99, viene applicato a un livello MIP prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="1a0cf-128">[in] The bias value, which is a floating-point number between -16.0 and 15.99, is applied to a mip level before sampling.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1a0cf-129"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Offset</em></span><span class="sxs-lookup"><span data-stu-id="1a0cf-129"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Offset</em></span></span></p></td>
<td><p><span data-ttu-id="1a0cf-130">in Offset della coordinata di trama facoltativo che può essere usato per qualsiasi tipo di oggetto trama. l'offset viene applicato al percorso prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="1a0cf-130">[in] An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="1a0cf-131">Gli offset della trama devono essere statici.</span><span class="sxs-lookup"><span data-stu-id="1a0cf-131">The texture offsets need to be static.</span></span> <span data-ttu-id="1a0cf-132">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="1a0cf-132">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="1a0cf-133">Per altre informazioni, vedere <a href="/windows/win32/direct3dhlsl/dx-graphics-hlsl-to-sample#applying-texture-coordinate-offsets">applicazione degli offset delle coordinate di trama</a>.</span><span class="sxs-lookup"><span data-stu-id="1a0cf-133">For more info, see <a href="/windows/win32/direct3dhlsl/dx-graphics-hlsl-to-sample#applying-texture-coordinate-offsets">Applying texture coordinate offsets</a>.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1a0cf-134">Tipo di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="1a0cf-134">Texture-Object Type</span></span></th>
<th><span data-ttu-id="1a0cf-135">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="1a0cf-135">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1a0cf-136">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="1a0cf-136">Texture1D, Texture1DArray</span></span></td>
<td><span data-ttu-id="1a0cf-137">INT</span><span class="sxs-lookup"><span data-stu-id="1a0cf-137">int</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1a0cf-138">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="1a0cf-138">Texture2D, Texture2DArray</span></span></td>
<td><span data-ttu-id="1a0cf-139">int2</span><span class="sxs-lookup"><span data-stu-id="1a0cf-139">int2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1a0cf-140">Texture3D</span><span class="sxs-lookup"><span data-stu-id="1a0cf-140">Texture3D</span></span></td>
<td><span data-ttu-id="1a0cf-141">int3</span><span class="sxs-lookup"><span data-stu-id="1a0cf-141">int3</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1a0cf-142">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="1a0cf-142">TextureCube, TextureCubeArray</span></span> </td>
<td><span data-ttu-id="1a0cf-143">non supportato</span><span class="sxs-lookup"><span data-stu-id="1a0cf-143">not supported</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="return-value"></a><span data-ttu-id="1a0cf-144">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1a0cf-144">Return Value</span></span>

<span data-ttu-id="1a0cf-145">Il tipo di modello della trama, che può essere un vettore a un solo o più componenti.</span><span class="sxs-lookup"><span data-stu-id="1a0cf-145">The texture's template type, which may be a single- or multi-component vector.</span></span> <span data-ttu-id="1a0cf-146">Il formato è basato sul [**\_ formato DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)della trama.</span><span class="sxs-lookup"><span data-stu-id="1a0cf-146">The format is based on the texture's [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="1a0cf-147">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="1a0cf-147">Minimum Shader Model</span></span>

<span data-ttu-id="1a0cf-148">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="1a0cf-148">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="1a0cf-149">vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="1a0cf-149">vs\_4\_0</span></span> | <span data-ttu-id="1a0cf-150">vs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="1a0cf-150">vs\_4\_1</span></span>  | <span data-ttu-id="1a0cf-151">PS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="1a0cf-151">ps\_4\_0</span></span> | <span data-ttu-id="1a0cf-152">PS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="1a0cf-152">ps\_4\_1</span></span>  | <span data-ttu-id="1a0cf-153">GS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="1a0cf-153">gs\_4\_0</span></span> | <span data-ttu-id="1a0cf-154">GS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="1a0cf-154">gs\_4\_1</span></span>  |
|----------|-----------|----------|-----------|----------|-----------|
|          |           | <span data-ttu-id="1a0cf-155">x</span><span class="sxs-lookup"><span data-stu-id="1a0cf-155">x</span></span>        | <span data-ttu-id="1a0cf-156">x</span><span class="sxs-lookup"><span data-stu-id="1a0cf-156">x</span></span>         |          |           |



 

1.  <span data-ttu-id="1a0cf-157">TextureCubeArray è disponibile nel modello Shader 4,1 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="1a0cf-157">TextureCubeArray is available in Shader Model 4.1 or higher.</span></span>
2.  <span data-ttu-id="1a0cf-158">Il modello di Shader 4,1 è disponibile in Direct3D 10,1 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="1a0cf-158">Shader Model 4.1 is available in Direct3D 10.1 or higher.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1a0cf-159">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1a0cf-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1a0cf-160">Texture-oggetto</span><span class="sxs-lookup"><span data-stu-id="1a0cf-160">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

