---
title: 'Funzione SampleGrad:: SampleGrad (S, float, float, float, int, float) per Texture2D'
description: Esegue il campionamento di un Texture2D, utilizzando una sfumatura per influenzare il modo in cui viene calcolata la posizione di esempio, con un valore facoltativo per bloccare i valori del livello di dettaglio (LOD) di esempio in. Per Texture2D.
ms.assetid: 1216B02A-4F70-4804-9B04-37E83DFC1CE8
keywords:
- Funzione SampleGrad HLSL
topic_type:
- apiref
api_name:
- SampleGrad
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0b309eb9bc0ce7cbd968be81fa05eee91ee577b4
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "104996417"
---
# <a name="samplegradsamplegradsfloatfloatfloatintfloat-function-for-texture2d"></a><span data-ttu-id="1648a-105">Funzione SampleGrad:: SampleGrad (S, float, float, float, int, float) per Texture2D</span><span class="sxs-lookup"><span data-stu-id="1648a-105">SampleGrad::SampleGrad(S,float,float,float,int,float) function for Texture2D</span></span>

<span data-ttu-id="1648a-106">Esegue il campionamento di un [**Texture2D**](sm5-object-texture2d.md), utilizzando una sfumatura per influenzare il modo in cui viene calcolata la posizione di esempio, con un valore facoltativo per bloccare i valori del livello di dettaglio (LOD) di esempio in.</span><span class="sxs-lookup"><span data-stu-id="1648a-106">Samples a [**Texture2D**](sm5-object-texture2d.md), using a gradient to influence the way the sample location is calculated, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="1648a-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1648a-107">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleGrad(
  in SamplerState S,
  in float        Location,
  in float        DDX,
  in float        DDY,
  in int          Offset,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="1648a-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="1648a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1648a-109">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1648a-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1648a-110">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="1648a-110">Type: **SamplerState**</span></span>

<span data-ttu-id="1648a-111">[Stato del campionatore](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="1648a-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="1648a-112">Si tratta di un oggetto dichiarato in un file di effetti che contiene le assegnazioni di stato.</span><span class="sxs-lookup"><span data-stu-id="1648a-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="1648a-113">*Posizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1648a-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1648a-114">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="1648a-114">Type: **float**</span></span>

<span data-ttu-id="1648a-115">Coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="1648a-115">The texture coordinates.</span></span> <span data-ttu-id="1648a-116">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="1648a-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="1648a-117">Tipo di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="1648a-117">Texture-Object Type</span></span>                    | <span data-ttu-id="1648a-118">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="1648a-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="1648a-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="1648a-119">Texture1D</span></span>                              | <span data-ttu-id="1648a-120">float</span><span class="sxs-lookup"><span data-stu-id="1648a-120">float</span></span>          |
| <span data-ttu-id="1648a-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="1648a-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="1648a-122">float2</span><span class="sxs-lookup"><span data-stu-id="1648a-122">float2</span></span>         |
| <span data-ttu-id="1648a-123">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="1648a-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="1648a-124">float3</span><span class="sxs-lookup"><span data-stu-id="1648a-124">float3</span></span>         |
| <span data-ttu-id="1648a-125">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="1648a-125">TextureCubeArray</span></span>                       | <span data-ttu-id="1648a-126">float4</span><span class="sxs-lookup"><span data-stu-id="1648a-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="1648a-127">*DDX* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1648a-127">*DDX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1648a-128">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="1648a-128">Type: **float**</span></span>

<span data-ttu-id="1648a-129">Frequenza di modifica della geometria della superficie nella direzione x.</span><span class="sxs-lookup"><span data-stu-id="1648a-129">The rate of change of the surface geometry in the x direction.</span></span> <span data-ttu-id="1648a-130">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="1648a-130">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="1648a-131">Tipo di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="1648a-131">Texture-Object Type</span></span>                      | <span data-ttu-id="1648a-132">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="1648a-132">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="1648a-133">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="1648a-133">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="1648a-134">float</span><span class="sxs-lookup"><span data-stu-id="1648a-134">float</span></span>          |
| <span data-ttu-id="1648a-135">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="1648a-135">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="1648a-136">float2</span><span class="sxs-lookup"><span data-stu-id="1648a-136">float2</span></span>         |
| <span data-ttu-id="1648a-137">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="1648a-137">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="1648a-138">float3</span><span class="sxs-lookup"><span data-stu-id="1648a-138">float3</span></span>         |
| <span data-ttu-id="1648a-139">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="1648a-139">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="1648a-140">non supportato</span><span class="sxs-lookup"><span data-stu-id="1648a-140">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="1648a-141">*Ddy* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1648a-141">*DDY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1648a-142">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="1648a-142">Type: **float**</span></span>

<span data-ttu-id="1648a-143">Frequenza di modifica della geometria della superficie nella direzione y.</span><span class="sxs-lookup"><span data-stu-id="1648a-143">The rate of change of the surface geometry in the y direction.</span></span> <span data-ttu-id="1648a-144">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="1648a-144">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="1648a-145">Tipo di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="1648a-145">Texture-Object Type</span></span>                      | <span data-ttu-id="1648a-146">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="1648a-146">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="1648a-147">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="1648a-147">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="1648a-148">float</span><span class="sxs-lookup"><span data-stu-id="1648a-148">float</span></span>          |
| <span data-ttu-id="1648a-149">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="1648a-149">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="1648a-150">float2</span><span class="sxs-lookup"><span data-stu-id="1648a-150">float2</span></span>         |
| <span data-ttu-id="1648a-151">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="1648a-151">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="1648a-152">float3</span><span class="sxs-lookup"><span data-stu-id="1648a-152">float3</span></span>         |
| <span data-ttu-id="1648a-153">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="1648a-153">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="1648a-154">non supportato</span><span class="sxs-lookup"><span data-stu-id="1648a-154">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="1648a-155">*Offset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1648a-155">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1648a-156">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="1648a-156">Type: **int**</span></span>

<span data-ttu-id="1648a-157">Offset della coordinata di trama facoltativo che può essere usato per qualsiasi tipo di oggetto trama. l'offset viene applicato al percorso prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="1648a-157">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="1648a-158">Usare un offset solo in un miplevel Integer; in caso contrario, è possibile ottenere risultati che non si traducono correttamente nell'hardware.</span><span class="sxs-lookup"><span data-stu-id="1648a-158">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="1648a-159">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="1648a-159">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="1648a-160">Per altre informazioni, vedere [Applying Integer offsets](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="1648a-160">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="1648a-161">Tipo di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="1648a-161">Texture-Object Type</span></span>           | <span data-ttu-id="1648a-162">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="1648a-162">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="1648a-163">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="1648a-163">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="1648a-164">INT</span><span class="sxs-lookup"><span data-stu-id="1648a-164">int</span></span>            |
| <span data-ttu-id="1648a-165">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="1648a-165">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="1648a-166">int2</span><span class="sxs-lookup"><span data-stu-id="1648a-166">int2</span></span>           |
| <span data-ttu-id="1648a-167">Texture3D</span><span class="sxs-lookup"><span data-stu-id="1648a-167">Texture3D</span></span>                     | <span data-ttu-id="1648a-168">int3</span><span class="sxs-lookup"><span data-stu-id="1648a-168">int3</span></span>           |
| <span data-ttu-id="1648a-169">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="1648a-169">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="1648a-170">non supportato</span><span class="sxs-lookup"><span data-stu-id="1648a-170">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="1648a-171">*Blocca* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1648a-171">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1648a-172">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="1648a-172">Type: **float**</span></span>

<span data-ttu-id="1648a-173">Valore facoltativo a cui bloccare i valori LOD di esempio.</span><span class="sxs-lookup"><span data-stu-id="1648a-173">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="1648a-174">Se ad esempio si passa 2.0 f per il valore del morsetto, si garantisce che nessun singolo campione acceda a un livello MIP inferiore a 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="1648a-174">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1648a-175">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1648a-175">Return value</span></span>

<span data-ttu-id="1648a-176">Tipo: **[ **DXGI \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="1648a-176">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="1648a-177">Il formato di trama, che è uno dei valori tipizzati elencati [**nel \_ formato DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="1648a-177">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="1648a-178">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1648a-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1648a-179">Metodi SampleGrad</span><span class="sxs-lookup"><span data-stu-id="1648a-179">SampleGrad methods</span></span>](texture2d-samplegrad.md)
</dt> </dl>

 

 
