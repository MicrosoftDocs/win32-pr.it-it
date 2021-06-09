---
title: SampleGrad (oggetto Texture HLSL DirectX)
description: Campionare una trama usando una sfumatura per influenzare il modo in cui viene calcolata la posizione del campione. | SampleGrad (oggetto Texture HLSL DirectX)
ms.assetid: f3d73296-23c4-4178-b89e-6f84cfcb48a5
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 959304d36da2b95bdf6289fba1b8c75d6ecfa314
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/09/2021
ms.locfileid: "111825738"
---
# <a name="samplegrad-directx-hlsl-texture-object"></a><span data-ttu-id="3964f-104">SampleGrad (oggetto Texture HLSL DirectX)</span><span class="sxs-lookup"><span data-stu-id="3964f-104">SampleGrad (DirectX HLSL Texture Object)</span></span>

<span data-ttu-id="3964f-105">Campionare una trama usando una sfumatura per influenzare il modo in cui viene calcolata la posizione del campione.</span><span class="sxs-lookup"><span data-stu-id="3964f-105">Samples a texture using a gradient to influence the way the sample location is calculated.</span></span>

<span data-ttu-id="3964f-106">&lt;Template Type &gt; Object.SampleGrad( sampler \_ state S, float Location, float DDX, float DDY \[ , int Offset \] );</span><span class="sxs-lookup"><span data-stu-id="3964f-106">&lt;Template Type&gt; Object.SampleGrad( sampler\_state S, float Location, float DDX, float DDY \[, int Offset\] );</span></span>



 

## <a name="parameters"></a><span data-ttu-id="3964f-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="3964f-107">Parameters</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3964f-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="3964f-108">Item</span></span></th>
<th><span data-ttu-id="3964f-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3964f-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3964f-110"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Oggetto</em></span><span class="sxs-lookup"><span data-stu-id="3964f-110"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Object</em></span></span><br/></td>
<td><span data-ttu-id="3964f-111">Qualsiasi <a href="dx-graphics-hlsl-to-type.md">tipo di oggetto</a> trama (ad eccezione di Texture2DMS e Texture2DMSArray).</span><span class="sxs-lookup"><span data-stu-id="3964f-111">Any <a href="dx-graphics-hlsl-to-type.md">texture-object</a> type (except Texture2DMS and Texture2DMSArray).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3964f-112"><span id="S"></span><span id="s"></span><em>S</em></span><span class="sxs-lookup"><span data-stu-id="3964f-112"><span id="S"></span><span id="s"></span><em>S</em></span></span><br/></td>
<td><span data-ttu-id="3964f-113">[in] Stato <a href="dx-graphics-hlsl-sampler.md">del campionatore.</a></span><span class="sxs-lookup"><span data-stu-id="3964f-113">[in] A <a href="dx-graphics-hlsl-sampler.md">Sampler state</a>.</span></span> <span data-ttu-id="3964f-114">Si tratta di un oggetto dichiarato in un file di effetto che contiene assegnazioni di stato.</span><span class="sxs-lookup"><span data-stu-id="3964f-114">This is an object declared in an effect file that contains state assignments.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3964f-115"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Posizione</em></span><span class="sxs-lookup"><span data-stu-id="3964f-115"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Location</em></span></span><br/></td>
<td><span data-ttu-id="3964f-116">[in] Coordinate della trama.</span><span class="sxs-lookup"><span data-stu-id="3964f-116">[in] The Texture coordinates.</span></span> <span data-ttu-id="3964f-117">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="3964f-117">The argument type is dependent on the texture-object type.</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="3964f-118">tipo Texture-Object</span><span class="sxs-lookup"><span data-stu-id="3964f-118">Texture-Object Type</span></span></th>
<th><span data-ttu-id="3964f-119">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="3964f-119">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3964f-120">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3964f-120">Texture1D</span></span></td>
<td><span data-ttu-id="3964f-121">float</span><span class="sxs-lookup"><span data-stu-id="3964f-121">float</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3964f-122">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="3964f-122">Texture1DArray, Texture2D</span></span></td>
<td><span data-ttu-id="3964f-123">float2</span><span class="sxs-lookup"><span data-stu-id="3964f-123">float2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3964f-124">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="3964f-124">Texture2DArray, Texture3D, TextureCube</span></span></td>
<td><span data-ttu-id="3964f-125">float3</span><span class="sxs-lookup"><span data-stu-id="3964f-125">float3</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3964f-126">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="3964f-126">TextureCubeArray</span></span> </td>
<td><span data-ttu-id="3964f-127">float4</span><span class="sxs-lookup"><span data-stu-id="3964f-127">float4</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3964f-128">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="3964f-128">Texture2DMS, Texture2DMSArray</span></span></td>
<td><span data-ttu-id="3964f-129">non supportato</span><span class="sxs-lookup"><span data-stu-id="3964f-129">not supported</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3964f-130"><span id="DDX"></span><span id="ddx"></span><em>Ddx</em></span><span class="sxs-lookup"><span data-stu-id="3964f-130"><span id="DDX"></span><span id="ddx"></span><em>DDX</em></span></span></p></td>
<td><p><span data-ttu-id="3964f-131">[in] Frequenza di modifica della geometria della superficie nella direzione x.</span><span class="sxs-lookup"><span data-stu-id="3964f-131">[in] The rate of change of the surface geometry in the x direction.</span></span> <span data-ttu-id="3964f-132">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="3964f-132">The argument type is dependent on the texture-object type.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="3964f-133">tipo Texture-Object</span><span class="sxs-lookup"><span data-stu-id="3964f-133">Texture-Object Type</span></span></th>
<th><span data-ttu-id="3964f-134">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="3964f-134">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3964f-135">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="3964f-135">Texture1D, Texture1DArray</span></span></td>
<td><span data-ttu-id="3964f-136">float</span><span class="sxs-lookup"><span data-stu-id="3964f-136">float</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3964f-137">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="3964f-137">Texture2D, Texture2DArray</span></span></td>
<td><span data-ttu-id="3964f-138">float2</span><span class="sxs-lookup"><span data-stu-id="3964f-138">float2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3964f-139">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="3964f-139">Texture3D, TextureCube, TextureCubeArray</span></span> </td>
<td><span data-ttu-id="3964f-140">float3</span><span class="sxs-lookup"><span data-stu-id="3964f-140">float3</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3964f-141">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="3964f-141">Texture2DMS, Texture2DMSArray</span></span></td>
<td><span data-ttu-id="3964f-142">non supportato</span><span class="sxs-lookup"><span data-stu-id="3964f-142">not supported</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3964f-143"><span id="DDY"></span><span id="ddy"></span><em>DDY</em></span><span class="sxs-lookup"><span data-stu-id="3964f-143"><span id="DDY"></span><span id="ddy"></span><em>DDY</em></span></span></p></td>
<td><p><span data-ttu-id="3964f-144">[in] Frequenza di modifica della geometria della superficie nella direzione y.</span><span class="sxs-lookup"><span data-stu-id="3964f-144">[in] The rate of change of the surface geometry in the y direction.</span></span> <span data-ttu-id="3964f-145">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="3964f-145">The argument type is dependent on the texture-object type.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="3964f-146">tipo Texture-Object</span><span class="sxs-lookup"><span data-stu-id="3964f-146">Texture-Object Type</span></span></th>
<th><span data-ttu-id="3964f-147">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="3964f-147">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3964f-148">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="3964f-148">Texture1D, Texture1DArray</span></span></td>
<td><span data-ttu-id="3964f-149">float</span><span class="sxs-lookup"><span data-stu-id="3964f-149">float</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3964f-150">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="3964f-150">Texture2D, Texture2DArray</span></span></td>
<td><span data-ttu-id="3964f-151">float2</span><span class="sxs-lookup"><span data-stu-id="3964f-151">float2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3964f-152">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="3964f-152">Texture3D, TextureCube, TextureCubeArray</span></span> </td>
<td><span data-ttu-id="3964f-153">float3</span><span class="sxs-lookup"><span data-stu-id="3964f-153">float3</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3964f-154">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="3964f-154">Texture2DMS, Texture2DMSArray</span></span></td>
<td><span data-ttu-id="3964f-155">non supportato</span><span class="sxs-lookup"><span data-stu-id="3964f-155">not supported</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3964f-156"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>compensare</em></span><span class="sxs-lookup"><span data-stu-id="3964f-156"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Offset</em></span></span></p></td>
<td><p><span data-ttu-id="3964f-157">[in] Offset facoltativo delle coordinate della trama, che può essere usato per qualsiasi tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="3964f-157">[in] An optional texture coordinate offset, which can be used for any texture-object types.</span></span> <span data-ttu-id="3964f-158">L'offset viene applicato alla posizione prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="3964f-158">The offset is applied to the location before sampling.</span></span> <span data-ttu-id="3964f-159">Usare un offset solo in corrispondenza di un valore integer miplevel; In caso contrario, è possibile che si otterrà un risultato che non si traduce bene in hardware.</span><span class="sxs-lookup"><span data-stu-id="3964f-159">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="3964f-160">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="3964f-160">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="3964f-161">Per altre informazioni, vedere<a href="dx-graphics-hlsl-to-sample.md">Applicazione di offset di interi.</a></span><span class="sxs-lookup"><span data-stu-id="3964f-161">For more info, see<a href="dx-graphics-hlsl-to-sample.md">Applying Integer Offsets</a>.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="3964f-162">tipo Texture-Object</span><span class="sxs-lookup"><span data-stu-id="3964f-162">Texture-Object Type</span></span></th>
<th><span data-ttu-id="3964f-163">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="3964f-163">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3964f-164">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="3964f-164">Texture1D, Texture1DArray</span></span></td>
<td><span data-ttu-id="3964f-165">INT</span><span class="sxs-lookup"><span data-stu-id="3964f-165">int</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3964f-166">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="3964f-166">Texture2D, Texture2DArray</span></span></td>
<td><span data-ttu-id="3964f-167">int2</span><span class="sxs-lookup"><span data-stu-id="3964f-167">int2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3964f-168">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3964f-168">Texture3D</span></span></td>
<td><span data-ttu-id="3964f-169">int3</span><span class="sxs-lookup"><span data-stu-id="3964f-169">int3</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3964f-170">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="3964f-170">TextureCube, TextureCubeArray</span></span> </td>
<td><span data-ttu-id="3964f-171">non supportato</span><span class="sxs-lookup"><span data-stu-id="3964f-171">not supported</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3964f-172">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="3964f-172">Texture2DMS, Texture2DMSArray</span></span></td>
<td><span data-ttu-id="3964f-173">non supportato</span><span class="sxs-lookup"><span data-stu-id="3964f-173">not supported</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="return-value"></a><span data-ttu-id="3964f-174">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3964f-174">Return Value</span></span>

<span data-ttu-id="3964f-175">Tipo di modello della trama, che può essere un vettore a uno o più componenti.</span><span class="sxs-lookup"><span data-stu-id="3964f-175">The texture's template type, which may be a single- or multi-component vector.</span></span> <span data-ttu-id="3964f-176">Il formato è basato sul formato [**DXGI \_ della trama.**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)</span><span class="sxs-lookup"><span data-stu-id="3964f-176">The format is based on the texture's [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="3964f-177">Modello di shader minimo</span><span class="sxs-lookup"><span data-stu-id="3964f-177">Minimum Shader Model</span></span>

<span data-ttu-id="3964f-178">Questa funzione è supportata nei modelli di shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="3964f-178">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="3964f-179">vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3964f-179">vs\_4\_0</span></span> | <span data-ttu-id="3964f-180">vs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="3964f-180">vs\_4\_1</span></span>  | <span data-ttu-id="3964f-181">ps \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3964f-181">ps\_4\_0</span></span> | <span data-ttu-id="3964f-182">ps \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="3964f-182">ps\_4\_1</span></span>  | <span data-ttu-id="3964f-183">gs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3964f-183">gs\_4\_0</span></span> | <span data-ttu-id="3964f-184">gs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="3964f-184">gs\_4\_1</span></span>  |
|----------|-----------|----------|-----------|----------|-----------|
| <span data-ttu-id="3964f-185">x</span><span class="sxs-lookup"><span data-stu-id="3964f-185">x</span></span>        | <span data-ttu-id="3964f-186">x</span><span class="sxs-lookup"><span data-stu-id="3964f-186">x</span></span>         | <span data-ttu-id="3964f-187">x</span><span class="sxs-lookup"><span data-stu-id="3964f-187">x</span></span>        | <span data-ttu-id="3964f-188">x</span><span class="sxs-lookup"><span data-stu-id="3964f-188">x</span></span>         | <span data-ttu-id="3964f-189">x</span><span class="sxs-lookup"><span data-stu-id="3964f-189">x</span></span>        | <span data-ttu-id="3964f-190">x</span><span class="sxs-lookup"><span data-stu-id="3964f-190">x</span></span>         |



 

1.  <span data-ttu-id="3964f-191">TextureCubeArray è disponibile in Shader Model 4.1 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="3964f-191">TextureCubeArray is available in Shader Model 4.1 or higher.</span></span>
2.  <span data-ttu-id="3964f-192">Il modello shader 4.1 è disponibile in Direct3D 10.1 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="3964f-192">Shader Model 4.1 is available in Direct3D 10.1 or higher.</span></span>

## <a name="example"></a><span data-ttu-id="3964f-193">Esempio</span><span class="sxs-lookup"><span data-stu-id="3964f-193">Example</span></span>

<span data-ttu-id="3964f-194">Questo esempio di codice parziale è dal file MotionBlur.fx in [MotionBlur10 Sample](https://msdn.microsoft.com/library/Ee416417(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="3964f-194">This partial code example is from the MotionBlur.fx file in the [MotionBlur10 Sample](https://msdn.microsoft.com/library/Ee416417(v=VS.85).aspx).</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="3964f-195">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3964f-195">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3964f-196">Oggetto Texture</span><span class="sxs-lookup"><span data-stu-id="3964f-196">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

