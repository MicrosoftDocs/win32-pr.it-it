---
title: 'Funzione SampleGrad:: SampleGrad (S, float, float, float, int, float, uint) per Texture1D'
description: Esegue il campionamento di una trama, usando una sfumatura per influenzare il modo in cui viene calcolata la posizione di esempio, con un valore facoltativo per bloccare i valori del livello di dettaglio (LOD) di esempio in. Per Texture1D.
ms.assetid: E2B131AC-99E6-493A-91EE-EB0D3EE7FA8B
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
ms.openlocfilehash: 3a5f95a87f46e94c971dd19989ffa670e6993e8f
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "103969536"
---
# <a name="samplegradsamplegradsfloatfloatfloatintfloatuint-function-for-texture1d"></a><span data-ttu-id="0bc3e-105">Funzione SampleGrad:: SampleGrad (S, float, float, float, int, float, uint) per Texture1D</span><span class="sxs-lookup"><span data-stu-id="0bc3e-105">SampleGrad::SampleGrad(S,float,float,float,int,float,uint) function for Texture1D</span></span>

<span data-ttu-id="0bc3e-106">Esegue il campionamento di una trama, usando una sfumatura per influenzare il modo in cui viene calcolata la posizione di esempio, con un valore facoltativo per bloccare i valori del livello di dettaglio (LOD) di esempio in.</span><span class="sxs-lookup"><span data-stu-id="0bc3e-106">Samples a texture, using a gradient to influence the way the sample location is calculated, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span> <span data-ttu-id="0bc3e-107">Restituisce lo stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="0bc3e-107">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="0bc3e-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0bc3e-108">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleGrad(
  in  SamplerState S,
  in  float        Location,
  in  float        DDX,
  in  float        DDY,
  in  int          Offset,
  in  float        Clamp,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="0bc3e-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="0bc3e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0bc3e-110">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0bc3e-110">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0bc3e-111">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="0bc3e-111">Type: **SamplerState**</span></span>

<span data-ttu-id="0bc3e-112">[Stato del campionatore](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="0bc3e-112">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="0bc3e-113">Si tratta di un oggetto dichiarato in un file di effetti che contiene le assegnazioni di stato.</span><span class="sxs-lookup"><span data-stu-id="0bc3e-113">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="0bc3e-114">*Posizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0bc3e-114">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0bc3e-115">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="0bc3e-115">Type: **float**</span></span>

<span data-ttu-id="0bc3e-116">Coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="0bc3e-116">The texture coordinates.</span></span> <span data-ttu-id="0bc3e-117">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="0bc3e-117">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="0bc3e-118">Tipo di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="0bc3e-118">Texture-Object Type</span></span>                    | <span data-ttu-id="0bc3e-119">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="0bc3e-119">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="0bc3e-120">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0bc3e-120">Texture1D</span></span>                              | <span data-ttu-id="0bc3e-121">float</span><span class="sxs-lookup"><span data-stu-id="0bc3e-121">float</span></span>          |
| <span data-ttu-id="0bc3e-122">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="0bc3e-122">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="0bc3e-123">float2</span><span class="sxs-lookup"><span data-stu-id="0bc3e-123">float2</span></span>         |
| <span data-ttu-id="0bc3e-124">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="0bc3e-124">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="0bc3e-125">float3</span><span class="sxs-lookup"><span data-stu-id="0bc3e-125">float3</span></span>         |
| <span data-ttu-id="0bc3e-126">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="0bc3e-126">TextureCubeArray</span></span>                       | <span data-ttu-id="0bc3e-127">float4</span><span class="sxs-lookup"><span data-stu-id="0bc3e-127">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="0bc3e-128">*DDX* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0bc3e-128">*DDX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0bc3e-129">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="0bc3e-129">Type: **float**</span></span>

<span data-ttu-id="0bc3e-130">Frequenza di modifica della geometria della superficie nella direzione x.</span><span class="sxs-lookup"><span data-stu-id="0bc3e-130">The rate of change of the surface geometry in the x direction.</span></span> <span data-ttu-id="0bc3e-131">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="0bc3e-131">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="0bc3e-132">Tipo di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="0bc3e-132">Texture-Object Type</span></span>                      | <span data-ttu-id="0bc3e-133">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="0bc3e-133">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="0bc3e-134">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="0bc3e-134">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="0bc3e-135">float</span><span class="sxs-lookup"><span data-stu-id="0bc3e-135">float</span></span>          |
| <span data-ttu-id="0bc3e-136">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="0bc3e-136">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="0bc3e-137">float2</span><span class="sxs-lookup"><span data-stu-id="0bc3e-137">float2</span></span>         |
| <span data-ttu-id="0bc3e-138">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="0bc3e-138">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="0bc3e-139">float3</span><span class="sxs-lookup"><span data-stu-id="0bc3e-139">float3</span></span>         |
| <span data-ttu-id="0bc3e-140">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="0bc3e-140">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="0bc3e-141">non supportato</span><span class="sxs-lookup"><span data-stu-id="0bc3e-141">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="0bc3e-142">*Ddy* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0bc3e-142">*DDY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0bc3e-143">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="0bc3e-143">Type: **float**</span></span>

<span data-ttu-id="0bc3e-144">Frequenza di modifica della geometria della superficie nella direzione y.</span><span class="sxs-lookup"><span data-stu-id="0bc3e-144">The rate of change of the surface geometry in the y direction.</span></span> <span data-ttu-id="0bc3e-145">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="0bc3e-145">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="0bc3e-146">Tipo di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="0bc3e-146">Texture-Object Type</span></span>                      | <span data-ttu-id="0bc3e-147">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="0bc3e-147">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="0bc3e-148">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="0bc3e-148">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="0bc3e-149">float</span><span class="sxs-lookup"><span data-stu-id="0bc3e-149">float</span></span>          |
| <span data-ttu-id="0bc3e-150">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="0bc3e-150">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="0bc3e-151">float2</span><span class="sxs-lookup"><span data-stu-id="0bc3e-151">float2</span></span>         |
| <span data-ttu-id="0bc3e-152">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="0bc3e-152">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="0bc3e-153">float3</span><span class="sxs-lookup"><span data-stu-id="0bc3e-153">float3</span></span>         |
| <span data-ttu-id="0bc3e-154">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="0bc3e-154">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="0bc3e-155">non supportato</span><span class="sxs-lookup"><span data-stu-id="0bc3e-155">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="0bc3e-156">*Offset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0bc3e-156">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0bc3e-157">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="0bc3e-157">Type: **int**</span></span>

<span data-ttu-id="0bc3e-158">Offset della coordinata di trama facoltativo che può essere usato per qualsiasi tipo di oggetto trama. l'offset viene applicato al percorso prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="0bc3e-158">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="0bc3e-159">Usare un offset solo in un miplevel Integer; in caso contrario, è possibile ottenere risultati che non si traducono correttamente nell'hardware.</span><span class="sxs-lookup"><span data-stu-id="0bc3e-159">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="0bc3e-160">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="0bc3e-160">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="0bc3e-161">Per altre informazioni, vedere [Applying Integer offsets](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="0bc3e-161">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="0bc3e-162">Tipo di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="0bc3e-162">Texture-Object Type</span></span>           | <span data-ttu-id="0bc3e-163">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="0bc3e-163">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="0bc3e-164">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="0bc3e-164">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="0bc3e-165">INT</span><span class="sxs-lookup"><span data-stu-id="0bc3e-165">int</span></span>            |
| <span data-ttu-id="0bc3e-166">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="0bc3e-166">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="0bc3e-167">int2</span><span class="sxs-lookup"><span data-stu-id="0bc3e-167">int2</span></span>           |
| <span data-ttu-id="0bc3e-168">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0bc3e-168">Texture3D</span></span>                     | <span data-ttu-id="0bc3e-169">int3</span><span class="sxs-lookup"><span data-stu-id="0bc3e-169">int3</span></span>           |
| <span data-ttu-id="0bc3e-170">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="0bc3e-170">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="0bc3e-171">non supportato</span><span class="sxs-lookup"><span data-stu-id="0bc3e-171">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="0bc3e-172">*Blocca* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0bc3e-172">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0bc3e-173">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="0bc3e-173">Type: **float**</span></span>

<span data-ttu-id="0bc3e-174">Valore facoltativo a cui bloccare i valori LOD di esempio.</span><span class="sxs-lookup"><span data-stu-id="0bc3e-174">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="0bc3e-175">Se ad esempio si passa 2.0 f per il valore del morsetto, si garantisce che nessun singolo campione acceda a un livello MIP inferiore a 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="0bc3e-175">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="0bc3e-176">*Stato* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="0bc3e-176">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0bc3e-177">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="0bc3e-177">Type: **uint**</span></span>

<span data-ttu-id="0bc3e-178">Stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="0bc3e-178">The status of the operation.</span></span> <span data-ttu-id="0bc3e-179">Non è possibile accedere direttamente allo stato; passare invece lo stato alla funzione intrinseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="0bc3e-179">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="0bc3e-180">**CheckAccessFullyMapped** restituisce **true** se tutti i valori dell'operazione di **campionamento**, **raccolta** o **caricamento** corrispondente hanno eseguito l'accesso ai riquadri mappati in una [risorsa affiancata](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="0bc3e-180">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="0bc3e-181">Se sono stati ricavati valori da un riquadro non mappato, **CheckAccessFullyMapped** restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="0bc3e-181">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0bc3e-182">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0bc3e-182">Return value</span></span>

<span data-ttu-id="0bc3e-183">Tipo: **[ **DXGI \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="0bc3e-183">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="0bc3e-184">Il formato di trama, che è uno dei valori tipizzati elencati [**nel \_ formato DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="0bc3e-184">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="0bc3e-185">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0bc3e-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0bc3e-186">Metodi SampleGrad</span><span class="sxs-lookup"><span data-stu-id="0bc3e-186">SampleGrad methods</span></span>](texture1d-samplegrad.md)
</dt> </dl>

 

 
