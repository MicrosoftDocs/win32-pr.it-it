---
title: 'Funzione SampleGrad:: SampleGrad (S, float, float, float, float, uint) per TextureCubeArray'
description: Informazioni sul modo in cui questa funzione esegue il campionamento di una trama, usando una sfumatura per influenzare il modo in cui viene calcolata la posizione di esempio, con un valore facoltativo per bloccare i valori del livello di dettaglio (LOD) di esempio in. Per TextureCubeArray.
ms.assetid: 849FAF04-A133-4E5B-967E-0679AE335CCC
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
ms.openlocfilehash: 00adfb5c7a1a95e5462b1bc524a6c7d86f71c2e8
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "104982646"
---
# <a name="samplegradsamplegradsfloatfloatfloatfloatuint-function-for-texturecubearray"></a><span data-ttu-id="5ec73-105">Funzione SampleGrad:: SampleGrad (S, float, float, float, float, uint) per TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="5ec73-105">SampleGrad::SampleGrad(S,float,float,float,float,uint) function for TextureCubeArray</span></span>

<span data-ttu-id="5ec73-106">Esegue il campionamento di una trama, usando una sfumatura per influenzare il modo in cui viene calcolata la posizione di esempio, con un valore facoltativo per bloccare i valori del livello di dettaglio (LOD) di esempio in.</span><span class="sxs-lookup"><span data-stu-id="5ec73-106">Samples a texture, using a gradient to influence the way the sample location is calculated, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span> <span data-ttu-id="5ec73-107">Restituisce lo stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="5ec73-107">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ec73-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5ec73-108">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="5ec73-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="5ec73-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ec73-110">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5ec73-110">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ec73-111">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="5ec73-111">Type: **SamplerState**</span></span>

<span data-ttu-id="5ec73-112">[Stato del campionatore](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="5ec73-112">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="5ec73-113">Si tratta di un oggetto dichiarato in un file di effetti che contiene le assegnazioni di stato.</span><span class="sxs-lookup"><span data-stu-id="5ec73-113">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="5ec73-114">*Posizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5ec73-114">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ec73-115">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="5ec73-115">Type: **float**</span></span>

<span data-ttu-id="5ec73-116">Coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="5ec73-116">The texture coordinates.</span></span> <span data-ttu-id="5ec73-117">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="5ec73-117">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="5ec73-118">Tipo di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="5ec73-118">Texture-Object Type</span></span>                    | <span data-ttu-id="5ec73-119">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="5ec73-119">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="5ec73-120">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5ec73-120">Texture1D</span></span>                              | <span data-ttu-id="5ec73-121">float</span><span class="sxs-lookup"><span data-stu-id="5ec73-121">float</span></span>          |
| <span data-ttu-id="5ec73-122">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="5ec73-122">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="5ec73-123">float2</span><span class="sxs-lookup"><span data-stu-id="5ec73-123">float2</span></span>         |
| <span data-ttu-id="5ec73-124">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="5ec73-124">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="5ec73-125">float3</span><span class="sxs-lookup"><span data-stu-id="5ec73-125">float3</span></span>         |
| <span data-ttu-id="5ec73-126">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="5ec73-126">TextureCubeArray</span></span>                       | <span data-ttu-id="5ec73-127">float4</span><span class="sxs-lookup"><span data-stu-id="5ec73-127">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="5ec73-128">*DDX* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5ec73-128">*DDX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ec73-129">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="5ec73-129">Type: **float**</span></span>

<span data-ttu-id="5ec73-130">Frequenza di modifica della geometria della superficie nella direzione x.</span><span class="sxs-lookup"><span data-stu-id="5ec73-130">The rate of change of the surface geometry in the x direction.</span></span> <span data-ttu-id="5ec73-131">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="5ec73-131">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="5ec73-132">Tipo di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="5ec73-132">Texture-Object Type</span></span>                      | <span data-ttu-id="5ec73-133">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="5ec73-133">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="5ec73-134">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="5ec73-134">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="5ec73-135">float</span><span class="sxs-lookup"><span data-stu-id="5ec73-135">float</span></span>          |
| <span data-ttu-id="5ec73-136">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="5ec73-136">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="5ec73-137">float2</span><span class="sxs-lookup"><span data-stu-id="5ec73-137">float2</span></span>         |
| <span data-ttu-id="5ec73-138">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="5ec73-138">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="5ec73-139">float3</span><span class="sxs-lookup"><span data-stu-id="5ec73-139">float3</span></span>         |
| <span data-ttu-id="5ec73-140">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="5ec73-140">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="5ec73-141">non supportato</span><span class="sxs-lookup"><span data-stu-id="5ec73-141">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="5ec73-142">*Ddy* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5ec73-142">*DDY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ec73-143">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="5ec73-143">Type: **float**</span></span>

<span data-ttu-id="5ec73-144">Frequenza di modifica della geometria della superficie nella direzione y.</span><span class="sxs-lookup"><span data-stu-id="5ec73-144">The rate of change of the surface geometry in the y direction.</span></span> <span data-ttu-id="5ec73-145">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="5ec73-145">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="5ec73-146">Tipo di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="5ec73-146">Texture-Object Type</span></span>                      | <span data-ttu-id="5ec73-147">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="5ec73-147">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="5ec73-148">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="5ec73-148">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="5ec73-149">float</span><span class="sxs-lookup"><span data-stu-id="5ec73-149">float</span></span>          |
| <span data-ttu-id="5ec73-150">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="5ec73-150">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="5ec73-151">float2</span><span class="sxs-lookup"><span data-stu-id="5ec73-151">float2</span></span>         |
| <span data-ttu-id="5ec73-152">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="5ec73-152">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="5ec73-153">float3</span><span class="sxs-lookup"><span data-stu-id="5ec73-153">float3</span></span>         |
| <span data-ttu-id="5ec73-154">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="5ec73-154">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="5ec73-155">non supportato</span><span class="sxs-lookup"><span data-stu-id="5ec73-155">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="5ec73-156">*Blocca* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5ec73-156">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ec73-157">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="5ec73-157">Type: **float**</span></span>

<span data-ttu-id="5ec73-158">Valore facoltativo a cui bloccare i valori LOD di esempio.</span><span class="sxs-lookup"><span data-stu-id="5ec73-158">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="5ec73-159">Se ad esempio si passa 2.0 f per il valore del morsetto, si garantisce che nessun singolo campione acceda a un livello MIP inferiore a 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="5ec73-159">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="5ec73-160">*Stato* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="5ec73-160">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5ec73-161">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="5ec73-161">Type: **uint**</span></span>

<span data-ttu-id="5ec73-162">Stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="5ec73-162">The status of the operation.</span></span> <span data-ttu-id="5ec73-163">Non è possibile accedere direttamente allo stato; passare invece lo stato alla funzione intrinseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="5ec73-163">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="5ec73-164">**CheckAccessFullyMapped** restituisce **true** se tutti i valori dell'operazione di **campionamento**, **raccolta** o **caricamento** corrispondente hanno eseguito l'accesso ai riquadri mappati in una [risorsa affiancata](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="5ec73-164">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="5ec73-165">Se sono stati ricavati valori da un riquadro non mappato, **CheckAccessFullyMapped** restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="5ec73-165">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ec73-166">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5ec73-166">Return value</span></span>

<span data-ttu-id="5ec73-167">Tipo: **[ **DXGI \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="5ec73-167">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="5ec73-168">Il formato di trama, che è uno dei valori tipizzati elencati [**nel \_ formato DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="5ec73-168">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="5ec73-169">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5ec73-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ec73-170">Metodi SampleGrad</span><span class="sxs-lookup"><span data-stu-id="5ec73-170">SampleGrad methods</span></span>](texturecubearray-samplegrad.md)
</dt> <dt>

[<span data-ttu-id="5ec73-171">**TextureCubeArray**</span><span class="sxs-lookup"><span data-stu-id="5ec73-171">**TextureCubeArray**</span></span>](texturecubearray.md)
</dt> </dl>

 

 
