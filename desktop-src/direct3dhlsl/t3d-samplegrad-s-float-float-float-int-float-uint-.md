---
title: 'Funzione SampleGrad:: SampleGrad (S, float, float, float, int, float, uint) per Texture3D'
description: Informazioni sul modo in cui questa funzione esegue il campionamento di una trama, usando una sfumatura per influenzare il modo in cui viene calcolata la posizione di esempio, con un valore facoltativo per bloccare i valori del livello di dettaglio (LOD) di esempio in. Per Texture3D.
ms.assetid: 4B02A3B8-8179-497D-BF87-489BF0B9ECC2
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
ms.openlocfilehash: b80b6ddcc2eebecf02416b09256d714bd2b8772f
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "104982662"
---
# <a name="samplegradsamplegradsfloatfloatfloatintfloatuint-function-for-texture3d"></a><span data-ttu-id="d7406-105">Funzione SampleGrad:: SampleGrad (S, float, float, float, int, float, uint) per Texture3D</span><span class="sxs-lookup"><span data-stu-id="d7406-105">SampleGrad::SampleGrad(S,float,float,float,int,float,uint) function for Texture3D</span></span>

<span data-ttu-id="d7406-106">Esegue il campionamento di una trama, usando una sfumatura per influenzare il modo in cui viene calcolata la posizione di esempio, con un valore facoltativo per bloccare i valori del livello di dettaglio (LOD) di esempio in.</span><span class="sxs-lookup"><span data-stu-id="d7406-106">Samples a texture, using a gradient to influence the way the sample location is calculated, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span> <span data-ttu-id="d7406-107">Restituisce lo stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="d7406-107">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7406-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d7406-108">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="d7406-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="d7406-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7406-110">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d7406-110">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7406-111">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="d7406-111">Type: **SamplerState**</span></span>

<span data-ttu-id="d7406-112">[Stato del campionatore](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="d7406-112">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="d7406-113">Si tratta di un oggetto dichiarato in un file di effetti che contiene le assegnazioni di stato.</span><span class="sxs-lookup"><span data-stu-id="d7406-113">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="d7406-114">*Posizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d7406-114">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7406-115">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="d7406-115">Type: **float**</span></span>

<span data-ttu-id="d7406-116">Coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="d7406-116">The texture coordinates.</span></span> <span data-ttu-id="d7406-117">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="d7406-117">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="d7406-118">Tipo di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="d7406-118">Texture-Object Type</span></span>                    | <span data-ttu-id="d7406-119">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="d7406-119">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="d7406-120">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d7406-120">Texture1D</span></span>                              | <span data-ttu-id="d7406-121">float</span><span class="sxs-lookup"><span data-stu-id="d7406-121">float</span></span>          |
| <span data-ttu-id="d7406-122">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="d7406-122">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="d7406-123">float2</span><span class="sxs-lookup"><span data-stu-id="d7406-123">float2</span></span>         |
| <span data-ttu-id="d7406-124">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="d7406-124">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="d7406-125">float3</span><span class="sxs-lookup"><span data-stu-id="d7406-125">float3</span></span>         |
| <span data-ttu-id="d7406-126">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="d7406-126">TextureCubeArray</span></span>                       | <span data-ttu-id="d7406-127">float4</span><span class="sxs-lookup"><span data-stu-id="d7406-127">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="d7406-128">*DDX* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d7406-128">*DDX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7406-129">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="d7406-129">Type: **float**</span></span>

<span data-ttu-id="d7406-130">Frequenza di modifica della geometria della superficie nella direzione x.</span><span class="sxs-lookup"><span data-stu-id="d7406-130">The rate of change of the surface geometry in the x direction.</span></span> <span data-ttu-id="d7406-131">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="d7406-131">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="d7406-132">Tipo di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="d7406-132">Texture-Object Type</span></span>                      | <span data-ttu-id="d7406-133">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="d7406-133">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="d7406-134">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="d7406-134">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="d7406-135">float</span><span class="sxs-lookup"><span data-stu-id="d7406-135">float</span></span>          |
| <span data-ttu-id="d7406-136">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="d7406-136">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="d7406-137">float2</span><span class="sxs-lookup"><span data-stu-id="d7406-137">float2</span></span>         |
| <span data-ttu-id="d7406-138">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="d7406-138">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="d7406-139">float3</span><span class="sxs-lookup"><span data-stu-id="d7406-139">float3</span></span>         |
| <span data-ttu-id="d7406-140">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="d7406-140">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="d7406-141">non supportato</span><span class="sxs-lookup"><span data-stu-id="d7406-141">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="d7406-142">*Ddy* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d7406-142">*DDY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7406-143">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="d7406-143">Type: **float**</span></span>

<span data-ttu-id="d7406-144">Frequenza di modifica della geometria della superficie nella direzione y.</span><span class="sxs-lookup"><span data-stu-id="d7406-144">The rate of change of the surface geometry in the y direction.</span></span> <span data-ttu-id="d7406-145">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="d7406-145">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="d7406-146">Tipo di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="d7406-146">Texture-Object Type</span></span>                      | <span data-ttu-id="d7406-147">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="d7406-147">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="d7406-148">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="d7406-148">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="d7406-149">float</span><span class="sxs-lookup"><span data-stu-id="d7406-149">float</span></span>          |
| <span data-ttu-id="d7406-150">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="d7406-150">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="d7406-151">float2</span><span class="sxs-lookup"><span data-stu-id="d7406-151">float2</span></span>         |
| <span data-ttu-id="d7406-152">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="d7406-152">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="d7406-153">float3</span><span class="sxs-lookup"><span data-stu-id="d7406-153">float3</span></span>         |
| <span data-ttu-id="d7406-154">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="d7406-154">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="d7406-155">non supportato</span><span class="sxs-lookup"><span data-stu-id="d7406-155">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="d7406-156">*Offset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d7406-156">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7406-157">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="d7406-157">Type: **int**</span></span>

<span data-ttu-id="d7406-158">Offset della coordinata di trama facoltativo che può essere usato per qualsiasi tipo di oggetto trama. l'offset viene applicato al percorso prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="d7406-158">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="d7406-159">Usare un offset solo in un miplevel Integer; in caso contrario, è possibile ottenere risultati che non si traducono correttamente nell'hardware.</span><span class="sxs-lookup"><span data-stu-id="d7406-159">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="d7406-160">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="d7406-160">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="d7406-161">Per altre informazioni, vedere [Applying Integer offsets](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="d7406-161">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="d7406-162">Tipo di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="d7406-162">Texture-Object Type</span></span>           | <span data-ttu-id="d7406-163">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="d7406-163">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="d7406-164">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="d7406-164">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="d7406-165">INT</span><span class="sxs-lookup"><span data-stu-id="d7406-165">int</span></span>            |
| <span data-ttu-id="d7406-166">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="d7406-166">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="d7406-167">int2</span><span class="sxs-lookup"><span data-stu-id="d7406-167">int2</span></span>           |
| <span data-ttu-id="d7406-168">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d7406-168">Texture3D</span></span>                     | <span data-ttu-id="d7406-169">int3</span><span class="sxs-lookup"><span data-stu-id="d7406-169">int3</span></span>           |
| <span data-ttu-id="d7406-170">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="d7406-170">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="d7406-171">non supportato</span><span class="sxs-lookup"><span data-stu-id="d7406-171">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="d7406-172">*Blocca* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d7406-172">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7406-173">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="d7406-173">Type: **float**</span></span>

<span data-ttu-id="d7406-174">Valore facoltativo a cui bloccare i valori LOD di esempio.</span><span class="sxs-lookup"><span data-stu-id="d7406-174">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="d7406-175">Se ad esempio si passa 2.0 f per il valore del morsetto, si garantisce che nessun singolo campione acceda a un livello MIP inferiore a 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="d7406-175">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="d7406-176">*Stato* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="d7406-176">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d7406-177">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="d7406-177">Type: **uint**</span></span>

<span data-ttu-id="d7406-178">Stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="d7406-178">The status of the operation.</span></span> <span data-ttu-id="d7406-179">Non è possibile accedere direttamente allo stato; passare invece lo stato alla funzione intrinseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="d7406-179">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="d7406-180">**CheckAccessFullyMapped** restituisce **true** se tutti i valori dell'operazione di **campionamento**, **raccolta** o **caricamento** corrispondente hanno eseguito l'accesso ai riquadri mappati in una [risorsa affiancata](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="d7406-180">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="d7406-181">Se sono stati ricavati valori da un riquadro non mappato, **CheckAccessFullyMapped** restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="d7406-181">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7406-182">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d7406-182">Return value</span></span>

<span data-ttu-id="d7406-183">Tipo: **[ **DXGI \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="d7406-183">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="d7406-184">Il formato di trama, che è uno dei valori tipizzati elencati [**nel \_ formato DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="d7406-184">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="d7406-185">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d7406-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7406-186">Metodi SampleGrad</span><span class="sxs-lookup"><span data-stu-id="d7406-186">SampleGrad methods</span></span>](texture3d-samplegrad.md)
</dt> <dt>

[<span data-ttu-id="d7406-187">**Texture3D**</span><span class="sxs-lookup"><span data-stu-id="d7406-187">**Texture3D**</span></span>](sm5-object-texture3d.md)
</dt> </dl>

 

 
