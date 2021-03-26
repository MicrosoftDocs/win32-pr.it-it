---
title: 'Funzione SampleGrad:: SampleGrad (S, float, float, float, int, float) per Texture2DArray'
description: Informazioni sul modo in cui questa funzione esegue il campionamento di una trama, usando una sfumatura per influenzare il modo in cui viene calcolata la posizione di esempio, con un valore facoltativo per bloccare i valori del livello di dettaglio (LOD) di esempio in. Per Texture2DArray.
ms.assetid: CBC940D5-FC09-498D-9C7A-3CBAB2EC2D4D
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
ms.openlocfilehash: 032d2b228800ffca654704c85a72d5ada76e65ef
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "104982763"
---
# <a name="samplegradsamplegradsfloatfloatfloatintfloat-function-for-texture2darray"></a><span data-ttu-id="f5649-105">Funzione SampleGrad:: SampleGrad (S, float, float, float, int, float) per Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="f5649-105">SampleGrad::SampleGrad(S,float,float,float,int,float) function for Texture2DArray</span></span>

<span data-ttu-id="f5649-106">Esegue il campionamento di una trama, usando una sfumatura per influenzare il modo in cui viene calcolata la posizione di esempio, con un valore facoltativo per bloccare i valori del livello di dettaglio (LOD) di esempio in.</span><span class="sxs-lookup"><span data-stu-id="f5649-106">Samples a texture, using a gradient to influence the way the sample location is calculated, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5649-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f5649-107">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="f5649-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="f5649-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5649-109">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f5649-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5649-110">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="f5649-110">Type: **SamplerState**</span></span>

<span data-ttu-id="f5649-111">[Stato del campionatore](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="f5649-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="f5649-112">Si tratta di un oggetto dichiarato in un file di effetti che contiene le assegnazioni di stato.</span><span class="sxs-lookup"><span data-stu-id="f5649-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="f5649-113">*Posizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f5649-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5649-114">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="f5649-114">Type: **float**</span></span>

<span data-ttu-id="f5649-115">Coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="f5649-115">The texture coordinates.</span></span> <span data-ttu-id="f5649-116">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="f5649-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="f5649-117">Tipo di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="f5649-117">Texture-Object Type</span></span>                    | <span data-ttu-id="f5649-118">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="f5649-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="f5649-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f5649-119">Texture1D</span></span>                              | <span data-ttu-id="f5649-120">float</span><span class="sxs-lookup"><span data-stu-id="f5649-120">float</span></span>          |
| <span data-ttu-id="f5649-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="f5649-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="f5649-122">float2</span><span class="sxs-lookup"><span data-stu-id="f5649-122">float2</span></span>         |
| <span data-ttu-id="f5649-123">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="f5649-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="f5649-124">float3</span><span class="sxs-lookup"><span data-stu-id="f5649-124">float3</span></span>         |
| <span data-ttu-id="f5649-125">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="f5649-125">TextureCubeArray</span></span>                       | <span data-ttu-id="f5649-126">float4</span><span class="sxs-lookup"><span data-stu-id="f5649-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="f5649-127">*DDX* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f5649-127">*DDX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5649-128">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="f5649-128">Type: **float**</span></span>

<span data-ttu-id="f5649-129">Frequenza di modifica della geometria della superficie nella direzione x.</span><span class="sxs-lookup"><span data-stu-id="f5649-129">The rate of change of the surface geometry in the x direction.</span></span> <span data-ttu-id="f5649-130">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="f5649-130">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="f5649-131">Tipo di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="f5649-131">Texture-Object Type</span></span>                      | <span data-ttu-id="f5649-132">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="f5649-132">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="f5649-133">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="f5649-133">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="f5649-134">float</span><span class="sxs-lookup"><span data-stu-id="f5649-134">float</span></span>          |
| <span data-ttu-id="f5649-135">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="f5649-135">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="f5649-136">float2</span><span class="sxs-lookup"><span data-stu-id="f5649-136">float2</span></span>         |
| <span data-ttu-id="f5649-137">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="f5649-137">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="f5649-138">float3</span><span class="sxs-lookup"><span data-stu-id="f5649-138">float3</span></span>         |
| <span data-ttu-id="f5649-139">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="f5649-139">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="f5649-140">non supportato</span><span class="sxs-lookup"><span data-stu-id="f5649-140">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="f5649-141">*Ddy* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f5649-141">*DDY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5649-142">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="f5649-142">Type: **float**</span></span>

<span data-ttu-id="f5649-143">Frequenza di modifica della geometria della superficie nella direzione y.</span><span class="sxs-lookup"><span data-stu-id="f5649-143">The rate of change of the surface geometry in the y direction.</span></span> <span data-ttu-id="f5649-144">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="f5649-144">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="f5649-145">Tipo di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="f5649-145">Texture-Object Type</span></span>                      | <span data-ttu-id="f5649-146">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="f5649-146">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="f5649-147">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="f5649-147">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="f5649-148">float</span><span class="sxs-lookup"><span data-stu-id="f5649-148">float</span></span>          |
| <span data-ttu-id="f5649-149">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="f5649-149">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="f5649-150">float2</span><span class="sxs-lookup"><span data-stu-id="f5649-150">float2</span></span>         |
| <span data-ttu-id="f5649-151">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="f5649-151">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="f5649-152">float3</span><span class="sxs-lookup"><span data-stu-id="f5649-152">float3</span></span>         |
| <span data-ttu-id="f5649-153">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="f5649-153">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="f5649-154">non supportato</span><span class="sxs-lookup"><span data-stu-id="f5649-154">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="f5649-155">*Offset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f5649-155">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5649-156">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="f5649-156">Type: **int**</span></span>

<span data-ttu-id="f5649-157">Offset della coordinata di trama facoltativo che può essere usato per qualsiasi tipo di oggetto trama. l'offset viene applicato al percorso prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="f5649-157">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="f5649-158">Usare un offset solo in un miplevel Integer; in caso contrario, è possibile ottenere risultati che non si traducono correttamente nell'hardware.</span><span class="sxs-lookup"><span data-stu-id="f5649-158">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="f5649-159">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="f5649-159">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="f5649-160">Per altre informazioni, vedere [Applying Integer offsets](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="f5649-160">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="f5649-161">Tipo di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="f5649-161">Texture-Object Type</span></span>           | <span data-ttu-id="f5649-162">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="f5649-162">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="f5649-163">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="f5649-163">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="f5649-164">INT</span><span class="sxs-lookup"><span data-stu-id="f5649-164">int</span></span>            |
| <span data-ttu-id="f5649-165">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="f5649-165">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="f5649-166">int2</span><span class="sxs-lookup"><span data-stu-id="f5649-166">int2</span></span>           |
| <span data-ttu-id="f5649-167">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f5649-167">Texture3D</span></span>                     | <span data-ttu-id="f5649-168">int3</span><span class="sxs-lookup"><span data-stu-id="f5649-168">int3</span></span>           |
| <span data-ttu-id="f5649-169">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="f5649-169">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="f5649-170">non supportato</span><span class="sxs-lookup"><span data-stu-id="f5649-170">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="f5649-171">*Blocca* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f5649-171">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5649-172">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="f5649-172">Type: **float**</span></span>

<span data-ttu-id="f5649-173">Valore facoltativo a cui bloccare i valori LOD di esempio.</span><span class="sxs-lookup"><span data-stu-id="f5649-173">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="f5649-174">Se ad esempio si passa 2.0 f per il valore del morsetto, si garantisce che nessun singolo campione acceda a un livello MIP inferiore a 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="f5649-174">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5649-175">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f5649-175">Return value</span></span>

<span data-ttu-id="f5649-176">Tipo: **[ **DXGI \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="f5649-176">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="f5649-177">Il formato di trama, che è uno dei valori tipizzati elencati [**nel \_ formato DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="f5649-177">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="f5649-178">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f5649-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5649-179">Metodi SampleGrad</span><span class="sxs-lookup"><span data-stu-id="f5649-179">SampleGrad methods</span></span>](texture2darray-samplegrad.md)
</dt> <dt>

[<span data-ttu-id="f5649-180">**Texture2DArray**</span><span class="sxs-lookup"><span data-stu-id="f5649-180">**Texture2DArray**</span></span>](sm5-object-texture2darray.md)
</dt> </dl>

 

 
