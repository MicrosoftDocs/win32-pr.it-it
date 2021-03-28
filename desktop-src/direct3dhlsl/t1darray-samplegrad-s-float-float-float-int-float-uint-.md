---
title: 'Funzione SampleGrad:: SampleGrad (S, float, float, float, int, float, uint) per Texture1DArray'
description: Informazioni su come questa funzione esegue il campionamento di una trama, usando una sfumatura per influenzare il modo in cui viene calcolata la posizione di esempio.
ms.assetid: 8F0D2A4E-37A9-4141-9EE7-2AACBB29E3C2
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
ms.openlocfilehash: 7a0feca232f09da4dc99ff97f68eaab881f1e9ee
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "103762418"
---
# <a name="samplegradsamplegradsfloatfloatfloatintfloatuint-function-for-texture1darray"></a><span data-ttu-id="2dd2f-104">Funzione SampleGrad:: SampleGrad (S, float, float, float, int, float, uint) per Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="2dd2f-104">SampleGrad::SampleGrad(S,float,float,float,int,float,uint) function for Texture1DArray</span></span>

<span data-ttu-id="2dd2f-105">Esegue il campionamento di una trama, usando una sfumatura per influenzare il modo in cui viene calcolata la posizione di esempio, con un valore facoltativo per bloccare i valori del livello di dettaglio (LOD) di esempio in.</span><span class="sxs-lookup"><span data-stu-id="2dd2f-105">Samples a texture, using a gradient to influence the way the sample location is calculated, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span> <span data-ttu-id="2dd2f-106">Restituisce lo stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="2dd2f-106">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="2dd2f-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2dd2f-107">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="2dd2f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="2dd2f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2dd2f-109">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2dd2f-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2dd2f-110">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="2dd2f-110">Type: **SamplerState**</span></span>

<span data-ttu-id="2dd2f-111">[Stato del campionatore](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="2dd2f-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="2dd2f-112">Si tratta di un oggetto dichiarato in un file di effetti che contiene le assegnazioni di stato.</span><span class="sxs-lookup"><span data-stu-id="2dd2f-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="2dd2f-113">*Posizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2dd2f-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2dd2f-114">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="2dd2f-114">Type: **float**</span></span>

<span data-ttu-id="2dd2f-115">Coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="2dd2f-115">The texture coordinates.</span></span> <span data-ttu-id="2dd2f-116">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="2dd2f-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="2dd2f-117">Tipo di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="2dd2f-117">Texture-Object Type</span></span>                    | <span data-ttu-id="2dd2f-118">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="2dd2f-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="2dd2f-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2dd2f-119">Texture1D</span></span>                              | <span data-ttu-id="2dd2f-120">float</span><span class="sxs-lookup"><span data-stu-id="2dd2f-120">float</span></span>          |
| <span data-ttu-id="2dd2f-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="2dd2f-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="2dd2f-122">float2</span><span class="sxs-lookup"><span data-stu-id="2dd2f-122">float2</span></span>         |
| <span data-ttu-id="2dd2f-123">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="2dd2f-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="2dd2f-124">float3</span><span class="sxs-lookup"><span data-stu-id="2dd2f-124">float3</span></span>         |
| <span data-ttu-id="2dd2f-125">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="2dd2f-125">TextureCubeArray</span></span>                       | <span data-ttu-id="2dd2f-126">float4</span><span class="sxs-lookup"><span data-stu-id="2dd2f-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="2dd2f-127">*DDX* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2dd2f-127">*DDX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2dd2f-128">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="2dd2f-128">Type: **float**</span></span>

<span data-ttu-id="2dd2f-129">Frequenza di modifica della geometria della superficie nella direzione x.</span><span class="sxs-lookup"><span data-stu-id="2dd2f-129">The rate of change of the surface geometry in the x direction.</span></span> <span data-ttu-id="2dd2f-130">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="2dd2f-130">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="2dd2f-131">Tipo di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="2dd2f-131">Texture-Object Type</span></span>                      | <span data-ttu-id="2dd2f-132">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="2dd2f-132">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="2dd2f-133">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="2dd2f-133">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="2dd2f-134">float</span><span class="sxs-lookup"><span data-stu-id="2dd2f-134">float</span></span>          |
| <span data-ttu-id="2dd2f-135">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="2dd2f-135">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="2dd2f-136">float2</span><span class="sxs-lookup"><span data-stu-id="2dd2f-136">float2</span></span>         |
| <span data-ttu-id="2dd2f-137">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="2dd2f-137">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="2dd2f-138">float3</span><span class="sxs-lookup"><span data-stu-id="2dd2f-138">float3</span></span>         |
| <span data-ttu-id="2dd2f-139">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="2dd2f-139">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="2dd2f-140">non supportato</span><span class="sxs-lookup"><span data-stu-id="2dd2f-140">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="2dd2f-141">*Ddy* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2dd2f-141">*DDY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2dd2f-142">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="2dd2f-142">Type: **float**</span></span>

<span data-ttu-id="2dd2f-143">Frequenza di modifica della geometria della superficie nella direzione y.</span><span class="sxs-lookup"><span data-stu-id="2dd2f-143">The rate of change of the surface geometry in the y direction.</span></span> <span data-ttu-id="2dd2f-144">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="2dd2f-144">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="2dd2f-145">Tipo di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="2dd2f-145">Texture-Object Type</span></span>                      | <span data-ttu-id="2dd2f-146">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="2dd2f-146">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="2dd2f-147">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="2dd2f-147">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="2dd2f-148">float</span><span class="sxs-lookup"><span data-stu-id="2dd2f-148">float</span></span>          |
| <span data-ttu-id="2dd2f-149">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="2dd2f-149">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="2dd2f-150">float2</span><span class="sxs-lookup"><span data-stu-id="2dd2f-150">float2</span></span>         |
| <span data-ttu-id="2dd2f-151">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="2dd2f-151">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="2dd2f-152">float3</span><span class="sxs-lookup"><span data-stu-id="2dd2f-152">float3</span></span>         |
| <span data-ttu-id="2dd2f-153">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="2dd2f-153">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="2dd2f-154">non supportato</span><span class="sxs-lookup"><span data-stu-id="2dd2f-154">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="2dd2f-155">*Offset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2dd2f-155">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2dd2f-156">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="2dd2f-156">Type: **int**</span></span>

<span data-ttu-id="2dd2f-157">Offset della coordinata di trama facoltativo che può essere usato per qualsiasi tipo di oggetto trama. l'offset viene applicato al percorso prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="2dd2f-157">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="2dd2f-158">Usare un offset solo in un miplevel Integer; in caso contrario, è possibile ottenere risultati che non si traducono correttamente nell'hardware.</span><span class="sxs-lookup"><span data-stu-id="2dd2f-158">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="2dd2f-159">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="2dd2f-159">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="2dd2f-160">Per altre informazioni, vedere [Applying Integer offsets](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="2dd2f-160">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="2dd2f-161">Tipo di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="2dd2f-161">Texture-Object Type</span></span>           | <span data-ttu-id="2dd2f-162">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="2dd2f-162">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="2dd2f-163">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="2dd2f-163">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="2dd2f-164">INT</span><span class="sxs-lookup"><span data-stu-id="2dd2f-164">int</span></span>            |
| <span data-ttu-id="2dd2f-165">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="2dd2f-165">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="2dd2f-166">int2</span><span class="sxs-lookup"><span data-stu-id="2dd2f-166">int2</span></span>           |
| <span data-ttu-id="2dd2f-167">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2dd2f-167">Texture3D</span></span>                     | <span data-ttu-id="2dd2f-168">int3</span><span class="sxs-lookup"><span data-stu-id="2dd2f-168">int3</span></span>           |
| <span data-ttu-id="2dd2f-169">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="2dd2f-169">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="2dd2f-170">non supportato</span><span class="sxs-lookup"><span data-stu-id="2dd2f-170">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="2dd2f-171">*Blocca* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2dd2f-171">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2dd2f-172">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="2dd2f-172">Type: **float**</span></span>

<span data-ttu-id="2dd2f-173">Valore facoltativo a cui bloccare i valori LOD di esempio.</span><span class="sxs-lookup"><span data-stu-id="2dd2f-173">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="2dd2f-174">Se ad esempio si passa 2.0 f per il valore del morsetto, si garantisce che nessun singolo campione acceda a un livello MIP inferiore a 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="2dd2f-174">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="2dd2f-175">*Stato* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="2dd2f-175">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2dd2f-176">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="2dd2f-176">Type: **uint**</span></span>

<span data-ttu-id="2dd2f-177">Stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="2dd2f-177">The status of the operation.</span></span> <span data-ttu-id="2dd2f-178">Non è possibile accedere direttamente allo stato; passare invece lo stato alla funzione intrinseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="2dd2f-178">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="2dd2f-179">**CheckAccessFullyMapped** restituisce **true** se tutti i valori dell'operazione di **campionamento**, **raccolta** o **caricamento** corrispondente hanno eseguito l'accesso ai riquadri mappati in una [risorsa affiancata](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="2dd2f-179">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="2dd2f-180">Se sono stati ricavati valori da un riquadro non mappato, **CheckAccessFullyMapped** restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="2dd2f-180">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2dd2f-181">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2dd2f-181">Return value</span></span>

<span data-ttu-id="2dd2f-182">Tipo: **[ **DXGI \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="2dd2f-182">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="2dd2f-183">Il formato di trama, che è uno dei valori tipizzati elencati [**nel \_ formato DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="2dd2f-183">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="2dd2f-184">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2dd2f-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2dd2f-185">Metodi SampleGrad</span><span class="sxs-lookup"><span data-stu-id="2dd2f-185">SampleGrad methods</span></span>](texture1darray-samplegrad.md)
</dt> </dl>

 

 
