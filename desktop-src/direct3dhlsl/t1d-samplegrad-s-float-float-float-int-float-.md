---
title: 'Funzione SampleGrad:: SampleGrad (S, float, float, float, int, float) per Texture1D'
description: La funzione esegue il campionamento di una trama, usando una sfumatura per influenzare il modo in cui viene calcolata la posizione di esempio, con un valore facoltativo per bloccare i valori del livello di dettaglio (LOD) di esempio in.
ms.assetid: 34A79CB6-0C45-40ED-845C-77C08F1DEC57
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
ms.openlocfilehash: 8c6222d8fa9548e3154abf7605fc5032dd67235a
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "104982747"
---
# <a name="samplegradsamplegradsfloatfloatfloatintfloat-function-for-texture1d"></a><span data-ttu-id="f2eb3-104">Funzione SampleGrad:: SampleGrad (S, float, float, float, int, float) per Texture1D</span><span class="sxs-lookup"><span data-stu-id="f2eb3-104">SampleGrad::SampleGrad(S,float,float,float,int,float) function for Texture1D</span></span>

<span data-ttu-id="f2eb3-105">Esegue il campionamento di una trama, usando una sfumatura per influenzare il modo in cui viene calcolata la posizione di esempio, con un valore facoltativo per bloccare i valori del livello di dettaglio (LOD) di esempio in.</span><span class="sxs-lookup"><span data-stu-id="f2eb3-105">Samples a texture, using a gradient to influence the way the sample location is calculated, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2eb3-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f2eb3-106">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="f2eb3-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="f2eb3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2eb3-108">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f2eb3-108">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2eb3-109">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="f2eb3-109">Type: **SamplerState**</span></span>

<span data-ttu-id="f2eb3-110">[Stato del campionatore](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="f2eb3-110">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="f2eb3-111">Si tratta di un oggetto dichiarato in un file di effetti che contiene le assegnazioni di stato.</span><span class="sxs-lookup"><span data-stu-id="f2eb3-111">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="f2eb3-112">*Posizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f2eb3-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2eb3-113">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="f2eb3-113">Type: **float**</span></span>

<span data-ttu-id="f2eb3-114">Coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="f2eb3-114">The texture coordinates.</span></span> <span data-ttu-id="f2eb3-115">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="f2eb3-115">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="f2eb3-116">Tipo di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="f2eb3-116">Texture-Object Type</span></span>                    | <span data-ttu-id="f2eb3-117">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="f2eb3-117">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="f2eb3-118">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f2eb3-118">Texture1D</span></span>                              | <span data-ttu-id="f2eb3-119">float</span><span class="sxs-lookup"><span data-stu-id="f2eb3-119">float</span></span>          |
| <span data-ttu-id="f2eb3-120">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="f2eb3-120">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="f2eb3-121">float2</span><span class="sxs-lookup"><span data-stu-id="f2eb3-121">float2</span></span>         |
| <span data-ttu-id="f2eb3-122">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="f2eb3-122">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="f2eb3-123">float3</span><span class="sxs-lookup"><span data-stu-id="f2eb3-123">float3</span></span>         |
| <span data-ttu-id="f2eb3-124">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="f2eb3-124">TextureCubeArray</span></span>                       | <span data-ttu-id="f2eb3-125">float4</span><span class="sxs-lookup"><span data-stu-id="f2eb3-125">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="f2eb3-126">*DDX* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f2eb3-126">*DDX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2eb3-127">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="f2eb3-127">Type: **float**</span></span>

<span data-ttu-id="f2eb3-128">Frequenza di modifica della geometria della superficie nella direzione x.</span><span class="sxs-lookup"><span data-stu-id="f2eb3-128">The rate of change of the surface geometry in the x direction.</span></span> <span data-ttu-id="f2eb3-129">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="f2eb3-129">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="f2eb3-130">Tipo di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="f2eb3-130">Texture-Object Type</span></span>                      | <span data-ttu-id="f2eb3-131">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="f2eb3-131">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="f2eb3-132">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="f2eb3-132">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="f2eb3-133">float</span><span class="sxs-lookup"><span data-stu-id="f2eb3-133">float</span></span>          |
| <span data-ttu-id="f2eb3-134">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="f2eb3-134">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="f2eb3-135">float2</span><span class="sxs-lookup"><span data-stu-id="f2eb3-135">float2</span></span>         |
| <span data-ttu-id="f2eb3-136">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="f2eb3-136">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="f2eb3-137">float3</span><span class="sxs-lookup"><span data-stu-id="f2eb3-137">float3</span></span>         |
| <span data-ttu-id="f2eb3-138">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="f2eb3-138">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="f2eb3-139">non supportato</span><span class="sxs-lookup"><span data-stu-id="f2eb3-139">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="f2eb3-140">*Ddy* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f2eb3-140">*DDY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2eb3-141">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="f2eb3-141">Type: **float**</span></span>

<span data-ttu-id="f2eb3-142">Frequenza di modifica della geometria della superficie nella direzione y.</span><span class="sxs-lookup"><span data-stu-id="f2eb3-142">The rate of change of the surface geometry in the y direction.</span></span> <span data-ttu-id="f2eb3-143">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="f2eb3-143">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="f2eb3-144">Tipo di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="f2eb3-144">Texture-Object Type</span></span>                      | <span data-ttu-id="f2eb3-145">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="f2eb3-145">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="f2eb3-146">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="f2eb3-146">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="f2eb3-147">float</span><span class="sxs-lookup"><span data-stu-id="f2eb3-147">float</span></span>          |
| <span data-ttu-id="f2eb3-148">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="f2eb3-148">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="f2eb3-149">float2</span><span class="sxs-lookup"><span data-stu-id="f2eb3-149">float2</span></span>         |
| <span data-ttu-id="f2eb3-150">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="f2eb3-150">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="f2eb3-151">float3</span><span class="sxs-lookup"><span data-stu-id="f2eb3-151">float3</span></span>         |
| <span data-ttu-id="f2eb3-152">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="f2eb3-152">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="f2eb3-153">non supportato</span><span class="sxs-lookup"><span data-stu-id="f2eb3-153">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="f2eb3-154">*Offset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f2eb3-154">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2eb3-155">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="f2eb3-155">Type: **int**</span></span>

<span data-ttu-id="f2eb3-156">Offset della coordinata di trama facoltativo che può essere usato per qualsiasi tipo di oggetto trama. l'offset viene applicato al percorso prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="f2eb3-156">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="f2eb3-157">Usare un offset solo in un miplevel Integer; in caso contrario, è possibile ottenere risultati che non si traducono correttamente nell'hardware.</span><span class="sxs-lookup"><span data-stu-id="f2eb3-157">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="f2eb3-158">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="f2eb3-158">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="f2eb3-159">Per altre informazioni, vedere [Applying Integer offsets](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="f2eb3-159">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="f2eb3-160">Tipo di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="f2eb3-160">Texture-Object Type</span></span>           | <span data-ttu-id="f2eb3-161">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="f2eb3-161">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="f2eb3-162">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="f2eb3-162">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="f2eb3-163">INT</span><span class="sxs-lookup"><span data-stu-id="f2eb3-163">int</span></span>            |
| <span data-ttu-id="f2eb3-164">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="f2eb3-164">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="f2eb3-165">int2</span><span class="sxs-lookup"><span data-stu-id="f2eb3-165">int2</span></span>           |
| <span data-ttu-id="f2eb3-166">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f2eb3-166">Texture3D</span></span>                     | <span data-ttu-id="f2eb3-167">int3</span><span class="sxs-lookup"><span data-stu-id="f2eb3-167">int3</span></span>           |
| <span data-ttu-id="f2eb3-168">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="f2eb3-168">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="f2eb3-169">non supportato</span><span class="sxs-lookup"><span data-stu-id="f2eb3-169">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="f2eb3-170">*Blocca* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f2eb3-170">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2eb3-171">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="f2eb3-171">Type: **float**</span></span>

<span data-ttu-id="f2eb3-172">Valore facoltativo a cui bloccare i valori LOD di esempio.</span><span class="sxs-lookup"><span data-stu-id="f2eb3-172">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="f2eb3-173">Se ad esempio si passa 2.0 f per il valore del morsetto, si garantisce che nessun singolo campione acceda a un livello MIP inferiore a 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="f2eb3-173">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2eb3-174">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f2eb3-174">Return value</span></span>

<span data-ttu-id="f2eb3-175">Tipo: **[ **DXGI \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="f2eb3-175">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="f2eb3-176">Il formato di trama, che è uno dei valori tipizzati elencati [**nel \_ formato DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="f2eb3-176">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="f2eb3-177">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f2eb3-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2eb3-178">Metodi SampleGrad</span><span class="sxs-lookup"><span data-stu-id="f2eb3-178">SampleGrad methods</span></span>](texture1d-samplegrad.md)
</dt> </dl>

 

 
