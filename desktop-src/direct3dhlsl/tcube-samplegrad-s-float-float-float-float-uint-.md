---
title: 'Funzione SampleGrad:: SampleGrad (S, float, float, float, float, uint) per TextureCube'
description: Esegue il campionamento di una trama, usando una sfumatura per influenzare il modo in cui viene calcolata la posizione di esempio, con un valore facoltativo per bloccare i valori del livello di dettaglio (LOD) di esempio in. Per TextureCube.
ms.assetid: 36DF7846-416A-4F2F-A7F8-44EE768CDEE1
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
ms.openlocfilehash: 3e75bccaeac28aefc50620a5dea31fa62b880332
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "104531093"
---
# <a name="samplegradsamplegradsfloatfloatfloatfloatuint-function-for-texturecube"></a><span data-ttu-id="c4eb0-105">Funzione SampleGrad:: SampleGrad (S, float, float, float, float, uint) per TextureCube</span><span class="sxs-lookup"><span data-stu-id="c4eb0-105">SampleGrad::SampleGrad(S,float,float,float,float,uint) function for TextureCube</span></span>

<span data-ttu-id="c4eb0-106">Esegue il campionamento di una trama, usando una sfumatura per influenzare il modo in cui viene calcolata la posizione di esempio, con un valore facoltativo per bloccare i valori del livello di dettaglio (LOD) di esempio in.</span><span class="sxs-lookup"><span data-stu-id="c4eb0-106">Samples a texture, using a gradient to influence the way the sample location is calculated, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span> <span data-ttu-id="c4eb0-107">Restituisce lo stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="c4eb0-107">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4eb0-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c4eb0-108">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleGrad(
  in  SamplerState S,
  in  float        Location,
  in  float        DDX,
  in  float        DDY,
  in  float        Clamp,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="c4eb0-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="c4eb0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4eb0-110">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c4eb0-110">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4eb0-111">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="c4eb0-111">Type: **SamplerState**</span></span>

<span data-ttu-id="c4eb0-112">[Stato del campionatore](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="c4eb0-112">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="c4eb0-113">Si tratta di un oggetto dichiarato in un file di effetti che contiene le assegnazioni di stato.</span><span class="sxs-lookup"><span data-stu-id="c4eb0-113">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="c4eb0-114">*Posizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c4eb0-114">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4eb0-115">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="c4eb0-115">Type: **float**</span></span>

<span data-ttu-id="c4eb0-116">Coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="c4eb0-116">The texture coordinates.</span></span> <span data-ttu-id="c4eb0-117">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="c4eb0-117">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="c4eb0-118">Tipo di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="c4eb0-118">Texture-Object Type</span></span>                    | <span data-ttu-id="c4eb0-119">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="c4eb0-119">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="c4eb0-120">Texture1D</span><span class="sxs-lookup"><span data-stu-id="c4eb0-120">Texture1D</span></span>                              | <span data-ttu-id="c4eb0-121">float</span><span class="sxs-lookup"><span data-stu-id="c4eb0-121">float</span></span>          |
| <span data-ttu-id="c4eb0-122">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="c4eb0-122">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="c4eb0-123">float2</span><span class="sxs-lookup"><span data-stu-id="c4eb0-123">float2</span></span>         |
| <span data-ttu-id="c4eb0-124">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="c4eb0-124">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="c4eb0-125">float3</span><span class="sxs-lookup"><span data-stu-id="c4eb0-125">float3</span></span>         |
| <span data-ttu-id="c4eb0-126">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="c4eb0-126">TextureCubeArray</span></span>                       | <span data-ttu-id="c4eb0-127">float4</span><span class="sxs-lookup"><span data-stu-id="c4eb0-127">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="c4eb0-128">*DDX* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c4eb0-128">*DDX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4eb0-129">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="c4eb0-129">Type: **float**</span></span>

<span data-ttu-id="c4eb0-130">Frequenza di modifica della geometria della superficie nella direzione x.</span><span class="sxs-lookup"><span data-stu-id="c4eb0-130">The rate of change of the surface geometry in the x direction.</span></span> <span data-ttu-id="c4eb0-131">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="c4eb0-131">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="c4eb0-132">Tipo di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="c4eb0-132">Texture-Object Type</span></span>                      | <span data-ttu-id="c4eb0-133">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="c4eb0-133">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="c4eb0-134">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="c4eb0-134">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="c4eb0-135">float</span><span class="sxs-lookup"><span data-stu-id="c4eb0-135">float</span></span>          |
| <span data-ttu-id="c4eb0-136">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="c4eb0-136">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="c4eb0-137">float2</span><span class="sxs-lookup"><span data-stu-id="c4eb0-137">float2</span></span>         |
| <span data-ttu-id="c4eb0-138">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="c4eb0-138">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="c4eb0-139">float3</span><span class="sxs-lookup"><span data-stu-id="c4eb0-139">float3</span></span>         |
| <span data-ttu-id="c4eb0-140">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="c4eb0-140">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="c4eb0-141">non supportato</span><span class="sxs-lookup"><span data-stu-id="c4eb0-141">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="c4eb0-142">*Ddy* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c4eb0-142">*DDY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4eb0-143">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="c4eb0-143">Type: **float**</span></span>

<span data-ttu-id="c4eb0-144">Frequenza di modifica della geometria della superficie nella direzione y.</span><span class="sxs-lookup"><span data-stu-id="c4eb0-144">The rate of change of the surface geometry in the y direction.</span></span> <span data-ttu-id="c4eb0-145">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="c4eb0-145">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="c4eb0-146">Tipo di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="c4eb0-146">Texture-Object Type</span></span>                      | <span data-ttu-id="c4eb0-147">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="c4eb0-147">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="c4eb0-148">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="c4eb0-148">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="c4eb0-149">float</span><span class="sxs-lookup"><span data-stu-id="c4eb0-149">float</span></span>          |
| <span data-ttu-id="c4eb0-150">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="c4eb0-150">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="c4eb0-151">float2</span><span class="sxs-lookup"><span data-stu-id="c4eb0-151">float2</span></span>         |
| <span data-ttu-id="c4eb0-152">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="c4eb0-152">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="c4eb0-153">float3</span><span class="sxs-lookup"><span data-stu-id="c4eb0-153">float3</span></span>         |
| <span data-ttu-id="c4eb0-154">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="c4eb0-154">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="c4eb0-155">non supportato</span><span class="sxs-lookup"><span data-stu-id="c4eb0-155">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="c4eb0-156">*Blocca* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c4eb0-156">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4eb0-157">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="c4eb0-157">Type: **float**</span></span>

<span data-ttu-id="c4eb0-158">Valore facoltativo a cui bloccare i valori LOD di esempio.</span><span class="sxs-lookup"><span data-stu-id="c4eb0-158">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="c4eb0-159">Se ad esempio si passa 2.0 f per il valore del morsetto, si garantisce che nessun singolo campione acceda a un livello MIP inferiore a 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="c4eb0-159">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="c4eb0-160">*Stato* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="c4eb0-160">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c4eb0-161">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="c4eb0-161">Type: **uint**</span></span>

<span data-ttu-id="c4eb0-162">Stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="c4eb0-162">The status of the operation.</span></span> <span data-ttu-id="c4eb0-163">Non è possibile accedere direttamente allo stato; passare invece lo stato alla funzione intrinseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="c4eb0-163">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="c4eb0-164">**CheckAccessFullyMapped** restituisce **true** se tutti i valori dell'operazione di **campionamento**, **raccolta** o **caricamento** corrispondente hanno eseguito l'accesso ai riquadri mappati in una [risorsa affiancata](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="c4eb0-164">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="c4eb0-165">Se sono stati ricavati valori da un riquadro non mappato, **CheckAccessFullyMapped** restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="c4eb0-165">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4eb0-166">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c4eb0-166">Return value</span></span>

<span data-ttu-id="c4eb0-167">Tipo: **[ **DXGI \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="c4eb0-167">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="c4eb0-168">Il formato di trama, che è uno dei valori tipizzati elencati [**nel \_ formato DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="c4eb0-168">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="c4eb0-169">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c4eb0-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4eb0-170">Metodi SampleGrad</span><span class="sxs-lookup"><span data-stu-id="c4eb0-170">SampleGrad methods</span></span>](texturecube-samplegrad.md)
</dt> <dt>

[<span data-ttu-id="c4eb0-171">**TextureCube**</span><span class="sxs-lookup"><span data-stu-id="c4eb0-171">**TextureCube**</span></span>](texturecube.md)
</dt> </dl>

 

 
