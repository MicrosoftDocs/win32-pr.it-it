---
title: SampleGrad (oggetto trama di DirectX HLSL)
description: Campiona una trama utilizzando una sfumatura per influenzare il modo in cui viene calcolata la posizione di esempio. | SampleGrad (oggetto trama di DirectX HLSL)
ms.assetid: f3d73296-23c4-4178-b89e-6f84cfcb48a5
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 236c453f3636452cbba8ed6000b2416e5187898d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104234684"
---
# <a name="samplegrad-directx-hlsl-texture-object"></a><span data-ttu-id="10727-104">SampleGrad (oggetto trama di DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="10727-104">SampleGrad (DirectX HLSL Texture Object)</span></span>

<span data-ttu-id="10727-105">Campiona una trama utilizzando una sfumatura per influenzare il modo in cui viene calcolata la posizione di esempio.</span><span class="sxs-lookup"><span data-stu-id="10727-105">Samples a texture using a gradient to influence the way the sample location is calculated.</span></span>



|                                                                                                            |
|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10727-106">&lt;Tipo &gt; di modello Object. SampleGrad ( \_ stato campionatore S, percorso float, DDX float, float ddy \[ , offset int \] );</span><span class="sxs-lookup"><span data-stu-id="10727-106">&lt;Template Type&gt; Object.SampleGrad( sampler\_state S, float Location, float DDX, float DDY \[, int Offset\] );</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="10727-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="10727-107">Parameters</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="10727-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="10727-108">Item</span></span></th>
<th><span data-ttu-id="10727-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="10727-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="10727-110"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Oggetto</em></span><span class="sxs-lookup"><span data-stu-id="10727-110"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Object</em></span></span><br/></td>
<td><span data-ttu-id="10727-111">Qualsiasi tipo <a href="dx-graphics-hlsl-to-type.md">di oggetto trama</a> (ad eccezione di Texture2DMS e Texture2DMSArray).</span><span class="sxs-lookup"><span data-stu-id="10727-111">Any <a href="dx-graphics-hlsl-to-type.md">texture-object</a> type (except Texture2DMS and Texture2DMSArray).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="10727-112"><span id="S"></span><span id="s"></span><em>S</em></span><span class="sxs-lookup"><span data-stu-id="10727-112"><span id="S"></span><span id="s"></span><em>S</em></span></span><br/></td>
<td><span data-ttu-id="10727-113">in <a href="dx-graphics-hlsl-sampler.md">Stato del campionatore</a>.</span><span class="sxs-lookup"><span data-stu-id="10727-113">[in] A <a href="dx-graphics-hlsl-sampler.md">Sampler state</a>.</span></span> <span data-ttu-id="10727-114">Si tratta di un oggetto dichiarato in un file di effetti che contiene le assegnazioni di stato.</span><span class="sxs-lookup"><span data-stu-id="10727-114">This is an object declared in an effect file that contains state assignments.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="10727-115"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Percorso</em></span><span class="sxs-lookup"><span data-stu-id="10727-115"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Location</em></span></span><br/></td>
<td><span data-ttu-id="10727-116">in Coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="10727-116">[in] The Texture coordinates.</span></span> <span data-ttu-id="10727-117">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="10727-117">The argument type is dependent on the texture-object type.</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="10727-118">Tipo di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="10727-118">Texture-Object Type</span></span></th>
<th><span data-ttu-id="10727-119">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="10727-119">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="10727-120">Texture1D</span><span class="sxs-lookup"><span data-stu-id="10727-120">Texture1D</span></span></td>
<td><span data-ttu-id="10727-121">float</span><span class="sxs-lookup"><span data-stu-id="10727-121">float</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="10727-122">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="10727-122">Texture1DArray, Texture2D</span></span></td>
<td><span data-ttu-id="10727-123">float2</span><span class="sxs-lookup"><span data-stu-id="10727-123">float2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="10727-124">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="10727-124">Texture2DArray, Texture3D, TextureCube</span></span></td>
<td><span data-ttu-id="10727-125">float3</span><span class="sxs-lookup"><span data-stu-id="10727-125">float3</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="10727-126">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="10727-126">TextureCubeArray</span></span> </td>
<td><span data-ttu-id="10727-127">float4</span><span class="sxs-lookup"><span data-stu-id="10727-127">float4</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="10727-128">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="10727-128">Texture2DMS, Texture2DMSArray</span></span></td>
<td><span data-ttu-id="10727-129">non supportato</span><span class="sxs-lookup"><span data-stu-id="10727-129">not supported</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10727-130"><span id="DDX"></span><span id="ddx"></span><em>DDX</em></span><span class="sxs-lookup"><span data-stu-id="10727-130"><span id="DDX"></span><span id="ddx"></span><em>DDX</em></span></span></p></td>
<td><p><span data-ttu-id="10727-131">in Frequenza di modifica della geometria della superficie nella direzione x.</span><span class="sxs-lookup"><span data-stu-id="10727-131">[in] The rate of change of the surface geometry in the x direction.</span></span> <span data-ttu-id="10727-132">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="10727-132">The argument type is dependent on the texture-object type.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="10727-133">Tipo di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="10727-133">Texture-Object Type</span></span></th>
<th><span data-ttu-id="10727-134">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="10727-134">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="10727-135">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="10727-135">Texture1D, Texture1DArray</span></span></td>
<td><span data-ttu-id="10727-136">float</span><span class="sxs-lookup"><span data-stu-id="10727-136">float</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="10727-137">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="10727-137">Texture2D, Texture2DArray</span></span></td>
<td><span data-ttu-id="10727-138">float2</span><span class="sxs-lookup"><span data-stu-id="10727-138">float2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="10727-139">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="10727-139">Texture3D, TextureCube, TextureCubeArray</span></span> </td>
<td><span data-ttu-id="10727-140">float3</span><span class="sxs-lookup"><span data-stu-id="10727-140">float3</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="10727-141">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="10727-141">Texture2DMS, Texture2DMSArray</span></span></td>
<td><span data-ttu-id="10727-142">non supportato</span><span class="sxs-lookup"><span data-stu-id="10727-142">not supported</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10727-143"><span id="DDY"></span><span id="ddy"></span><em>DDY</em></span><span class="sxs-lookup"><span data-stu-id="10727-143"><span id="DDY"></span><span id="ddy"></span><em>DDY</em></span></span></p></td>
<td><p><span data-ttu-id="10727-144">in Frequenza di modifica della geometria della superficie nella direzione y.</span><span class="sxs-lookup"><span data-stu-id="10727-144">[in] The rate of change of the surface geometry in the y direction.</span></span> <span data-ttu-id="10727-145">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="10727-145">The argument type is dependent on the texture-object type.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="10727-146">Tipo di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="10727-146">Texture-Object Type</span></span></th>
<th><span data-ttu-id="10727-147">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="10727-147">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="10727-148">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="10727-148">Texture1D, Texture1DArray</span></span></td>
<td><span data-ttu-id="10727-149">float</span><span class="sxs-lookup"><span data-stu-id="10727-149">float</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="10727-150">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="10727-150">Texture2D, Texture2DArray</span></span></td>
<td><span data-ttu-id="10727-151">float2</span><span class="sxs-lookup"><span data-stu-id="10727-151">float2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="10727-152">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="10727-152">Texture3D, TextureCube, TextureCubeArray</span></span> </td>
<td><span data-ttu-id="10727-153">float3</span><span class="sxs-lookup"><span data-stu-id="10727-153">float3</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="10727-154">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="10727-154">Texture2DMS, Texture2DMSArray</span></span></td>
<td><span data-ttu-id="10727-155">non supportato</span><span class="sxs-lookup"><span data-stu-id="10727-155">not supported</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10727-156"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Offset</em></span><span class="sxs-lookup"><span data-stu-id="10727-156"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Offset</em></span></span></p></td>
<td><p><span data-ttu-id="10727-157">in Offset della coordinata di trama facoltativo, che può essere usato per qualsiasi tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="10727-157">[in] An optional texture coordinate offset, which can be used for any texture-object types.</span></span> <span data-ttu-id="10727-158">L'offset viene applicato al percorso prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="10727-158">The offset is applied to the location before sampling.</span></span> <span data-ttu-id="10727-159">Usare un offset solo in un miplevel Integer; in caso contrario, è possibile ottenere risultati che non si traducono correttamente nell'hardware.</span><span class="sxs-lookup"><span data-stu-id="10727-159">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="10727-160">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="10727-160">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="10727-161">Per altre informazioni, vedere<a href="dx-graphics-hlsl-to-sample.md">Applying Integer offsets</a>.</span><span class="sxs-lookup"><span data-stu-id="10727-161">For more info, see<a href="dx-graphics-hlsl-to-sample.md">Applying Integer Offsets</a>.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="10727-162">Tipo di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="10727-162">Texture-Object Type</span></span></th>
<th><span data-ttu-id="10727-163">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="10727-163">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="10727-164">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="10727-164">Texture1D, Texture1DArray</span></span></td>
<td><span data-ttu-id="10727-165">INT</span><span class="sxs-lookup"><span data-stu-id="10727-165">int</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="10727-166">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="10727-166">Texture2D, Texture2DArray</span></span></td>
<td><span data-ttu-id="10727-167">int2</span><span class="sxs-lookup"><span data-stu-id="10727-167">int2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="10727-168">Texture3D</span><span class="sxs-lookup"><span data-stu-id="10727-168">Texture3D</span></span></td>
<td><span data-ttu-id="10727-169">int3</span><span class="sxs-lookup"><span data-stu-id="10727-169">int3</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="10727-170">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="10727-170">TextureCube, TextureCubeArray</span></span> </td>
<td><span data-ttu-id="10727-171">non supportato</span><span class="sxs-lookup"><span data-stu-id="10727-171">not supported</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="10727-172">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="10727-172">Texture2DMS, Texture2DMSArray</span></span></td>
<td><span data-ttu-id="10727-173">non supportato</span><span class="sxs-lookup"><span data-stu-id="10727-173">not supported</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="return-value"></a><span data-ttu-id="10727-174">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="10727-174">Return Value</span></span>

<span data-ttu-id="10727-175">Il tipo di modello della trama, che può essere un vettore a un solo o più componenti.</span><span class="sxs-lookup"><span data-stu-id="10727-175">The texture's template type, which may be a single- or multi-component vector.</span></span> <span data-ttu-id="10727-176">Il formato è basato sul [**\_ formato DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)della trama.</span><span class="sxs-lookup"><span data-stu-id="10727-176">The format is based on the texture's [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="10727-177">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="10727-177">Minimum Shader Model</span></span>

<span data-ttu-id="10727-178">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="10727-178">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="10727-179">vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="10727-179">vs\_4\_0</span></span> | <span data-ttu-id="10727-180">vs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="10727-180">vs\_4\_1</span></span>  | <span data-ttu-id="10727-181">PS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="10727-181">ps\_4\_0</span></span> | <span data-ttu-id="10727-182">PS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="10727-182">ps\_4\_1</span></span>  | <span data-ttu-id="10727-183">GS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="10727-183">gs\_4\_0</span></span> | <span data-ttu-id="10727-184">GS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="10727-184">gs\_4\_1</span></span>  |
|----------|-----------|----------|-----------|----------|-----------|
| <span data-ttu-id="10727-185">x</span><span class="sxs-lookup"><span data-stu-id="10727-185">x</span></span>        | <span data-ttu-id="10727-186">x</span><span class="sxs-lookup"><span data-stu-id="10727-186">x</span></span>         | <span data-ttu-id="10727-187">x</span><span class="sxs-lookup"><span data-stu-id="10727-187">x</span></span>        | <span data-ttu-id="10727-188">x</span><span class="sxs-lookup"><span data-stu-id="10727-188">x</span></span>         | <span data-ttu-id="10727-189">x</span><span class="sxs-lookup"><span data-stu-id="10727-189">x</span></span>        | <span data-ttu-id="10727-190">x</span><span class="sxs-lookup"><span data-stu-id="10727-190">x</span></span>         |



 

1.  <span data-ttu-id="10727-191">TextureCubeArray è disponibile nel modello Shader 4,1 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="10727-191">TextureCubeArray is available in Shader Model 4.1 or higher.</span></span>
2.  <span data-ttu-id="10727-192">Il modello di Shader 4,1 è disponibile in Direct3D 10,1 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="10727-192">Shader Model 4.1 is available in Direct3D 10.1 or higher.</span></span>

## <a name="example"></a><span data-ttu-id="10727-193">Esempio</span><span class="sxs-lookup"><span data-stu-id="10727-193">Example</span></span>

<span data-ttu-id="10727-194">Questo esempio di codice parziale viene dal file MotionBlur. FX nell' [esempio MotionBlur10](https://msdn.microsoft.com/library/Ee416417(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="10727-194">This partial code example is from the MotionBlur.fx file in the [MotionBlur10 Sample](https://msdn.microsoft.com/library/Ee416417(v=VS.85).aspx).</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="10727-195">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="10727-195">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="10727-196">Texture-oggetto</span><span class="sxs-lookup"><span data-stu-id="10727-196">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

