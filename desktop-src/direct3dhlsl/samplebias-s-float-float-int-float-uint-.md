---
title: 'Funzione SampleBias:: SampleBias (S, float, float, int, float, uint) per Texture2D'
description: 'La funzione SampleBias:: SampleBias (S, float, float, int, float, uint) esegue il campionamento di un Texture2D, dopo aver applicato il valore di distorsione al livello mipmap.'
ms.assetid: ACABF551-1DBF-4979-B0B1-D025E04EC08C
keywords:
- Funzione SampleBias HLSL
topic_type:
- apiref
api_name:
- SampleBias
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 86840748d12a92eca24b8d0d2bfba26eee69cff5
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "104982787"
---
# <a name="samplebiassamplebiassfloatfloatintfloatuint-function-for-texture2d"></a><span data-ttu-id="fa03f-104">Funzione SampleBias:: SampleBias (S, float, float, int, float, uint) per Texture2D</span><span class="sxs-lookup"><span data-stu-id="fa03f-104">SampleBias::SampleBias(S,float,float,int,float,uint) function for Texture2D</span></span>

<span data-ttu-id="fa03f-105">Esegue il campionamento di un [**Texture2D**](sm5-object-texture2d.md), dopo aver applicato il valore di distorsione al livello mipmap, con un valore facoltativo per bloccare i valori del livello di dettaglio (LOD) campione su.</span><span class="sxs-lookup"><span data-stu-id="fa03f-105">Samples a [**Texture2D**](sm5-object-texture2d.md), after applying the bias value to the mipmap level, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span> <span data-ttu-id="fa03f-106">Restituisce lo stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="fa03f-106">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa03f-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fa03f-107">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleBias(
  in  SamplerState S,
  in  float        Location,
  in  float        Bias,
  in  int          Offset,
  in  float        Clamp,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="fa03f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="fa03f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa03f-109">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fa03f-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa03f-110">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="fa03f-110">Type: **SamplerState**</span></span>

<span data-ttu-id="fa03f-111">[Stato del campionatore](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="fa03f-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="fa03f-112">Si tratta di un oggetto dichiarato in un file di effetti che contiene le assegnazioni di stato.</span><span class="sxs-lookup"><span data-stu-id="fa03f-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="fa03f-113">*Posizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fa03f-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa03f-114">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="fa03f-114">Type: **float**</span></span>

<span data-ttu-id="fa03f-115">Coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="fa03f-115">The texture coordinates.</span></span> <span data-ttu-id="fa03f-116">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="fa03f-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="fa03f-117">Tipo di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="fa03f-117">Texture-Object Type</span></span>                    | <span data-ttu-id="fa03f-118">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="fa03f-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="fa03f-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fa03f-119">Texture1D</span></span>                              | <span data-ttu-id="fa03f-120">float</span><span class="sxs-lookup"><span data-stu-id="fa03f-120">float</span></span>          |
| <span data-ttu-id="fa03f-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="fa03f-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="fa03f-122">float2</span><span class="sxs-lookup"><span data-stu-id="fa03f-122">float2</span></span>         |
| <span data-ttu-id="fa03f-123">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="fa03f-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="fa03f-124">float3</span><span class="sxs-lookup"><span data-stu-id="fa03f-124">float3</span></span>         |
| <span data-ttu-id="fa03f-125">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="fa03f-125">TextureCubeArray</span></span>                       | <span data-ttu-id="fa03f-126">float4</span><span class="sxs-lookup"><span data-stu-id="fa03f-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="fa03f-127">*Distorsione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fa03f-127">*Bias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa03f-128">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="fa03f-128">Type: **float**</span></span>

<span data-ttu-id="fa03f-129">Il valore di distorsione, ovvero un numero a virgola mobile compreso tra 0,0 e 1,0 inclusivo, viene applicato a un livello MIP prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="fa03f-129">The bias value, which is a floating-point number between 0.0 and 1.0 inclusive, is applied to a mip level before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="fa03f-130">*Offset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fa03f-130">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa03f-131">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="fa03f-131">Type: **int**</span></span>

<span data-ttu-id="fa03f-132">Offset della coordinata di trama facoltativo che può essere usato per qualsiasi tipo di oggetto trama. l'offset viene applicato al percorso prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="fa03f-132">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="fa03f-133">Usare un offset solo in un miplevel Integer; in caso contrario, è possibile ottenere risultati che non si traducono correttamente nell'hardware.</span><span class="sxs-lookup"><span data-stu-id="fa03f-133">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="fa03f-134">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="fa03f-134">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="fa03f-135">Per altre informazioni, vedere [Applying Integer offsets](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="fa03f-135">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="fa03f-136">Tipo di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="fa03f-136">Texture-Object Type</span></span>           | <span data-ttu-id="fa03f-137">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="fa03f-137">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="fa03f-138">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="fa03f-138">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="fa03f-139">INT</span><span class="sxs-lookup"><span data-stu-id="fa03f-139">int</span></span>            |
| <span data-ttu-id="fa03f-140">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="fa03f-140">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="fa03f-141">int2</span><span class="sxs-lookup"><span data-stu-id="fa03f-141">int2</span></span>           |
| <span data-ttu-id="fa03f-142">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fa03f-142">Texture3D</span></span>                     | <span data-ttu-id="fa03f-143">int3</span><span class="sxs-lookup"><span data-stu-id="fa03f-143">int3</span></span>           |
| <span data-ttu-id="fa03f-144">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="fa03f-144">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="fa03f-145">non supportato</span><span class="sxs-lookup"><span data-stu-id="fa03f-145">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="fa03f-146">*Blocca* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fa03f-146">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa03f-147">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="fa03f-147">Type: **float**</span></span>

<span data-ttu-id="fa03f-148">Valore facoltativo a cui bloccare i valori LOD di esempio.</span><span class="sxs-lookup"><span data-stu-id="fa03f-148">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="fa03f-149">Se ad esempio si passa 2.0 f per il valore del morsetto, si garantisce che nessun singolo campione acceda a un livello MIP inferiore a 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="fa03f-149">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="fa03f-150">*Stato* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="fa03f-150">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fa03f-151">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="fa03f-151">Type: **uint**</span></span>

<span data-ttu-id="fa03f-152">Stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="fa03f-152">The status of the operation.</span></span> <span data-ttu-id="fa03f-153">Non è possibile accedere direttamente allo stato; passare invece lo stato alla funzione intrinseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="fa03f-153">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="fa03f-154">**CheckAccessFullyMapped** restituisce **true** se tutti i valori dell'operazione di **campionamento**, **raccolta** o **caricamento** corrispondente hanno eseguito l'accesso ai riquadri mappati in una [risorsa affiancata](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="fa03f-154">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="fa03f-155">Se sono stati ricavati valori da un riquadro non mappato, **CheckAccessFullyMapped** restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="fa03f-155">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa03f-156">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fa03f-156">Return value</span></span>

<span data-ttu-id="fa03f-157">Tipo: **[ **DXGI \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="fa03f-157">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="fa03f-158">Il formato di trama, che è uno dei valori tipizzati elencati [**nel \_ formato DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="fa03f-158">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="fa03f-159">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fa03f-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa03f-160">Metodi SampleBias</span><span class="sxs-lookup"><span data-stu-id="fa03f-160">SampleBias methods</span></span>](texture2d-samplebias.md)
</dt> </dl>

 

 
