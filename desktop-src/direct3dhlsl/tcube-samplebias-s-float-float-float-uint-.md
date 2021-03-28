---
title: 'Funzione SampleBias:: SampleBias (S, float, float, float, uint)'
description: "Esegue il campionamento di una trama, dopo aver applicato il valore di distorsione al livello mipmap, con un valore facoltativo per limitare i valori del livello di dettaglio (LOD) campione a. Restituisce lo stato dell'operazione. | Funzione SampleBias:: SampleBias (S, float, float, float, uint)"
ms.assetid: A2F10B9B-5DF2-4389-83A9-F6A29781BF0A
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
ms.openlocfilehash: 2f3a994d7b0f0c2d55ae3203db9f3205932c1a25
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104234797"
---
# <a name="samplebiassamplebiassfloatfloatfloatuint-function"></a><span data-ttu-id="e99f6-106">Funzione SampleBias:: SampleBias (S, float, float, float, uint)</span><span class="sxs-lookup"><span data-stu-id="e99f6-106">SampleBias::SampleBias(S,float,float,float,uint) function</span></span>

<span data-ttu-id="e99f6-107">Esegue il campionamento di una trama, dopo aver applicato il valore di distorsione al livello mipmap, con un valore facoltativo per limitare i valori del livello di dettaglio (LOD) campione a.</span><span class="sxs-lookup"><span data-stu-id="e99f6-107">Samples a texture, after applying the bias value to the mipmap level, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span> <span data-ttu-id="e99f6-108">Restituisce lo stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="e99f6-108">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="e99f6-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e99f6-109">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleBias(
  in  SamplerState S,
  in  float        Location,
  in  float        Bias,
  in  float        Clamp,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="e99f6-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="e99f6-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e99f6-111">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e99f6-111">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e99f6-112">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="e99f6-112">Type: **SamplerState**</span></span>

<span data-ttu-id="e99f6-113">[Stato del campionatore](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="e99f6-113">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="e99f6-114">Si tratta di un oggetto dichiarato in un file di effetti che contiene le assegnazioni di stato.</span><span class="sxs-lookup"><span data-stu-id="e99f6-114">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="e99f6-115">*Posizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e99f6-115">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e99f6-116">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="e99f6-116">Type: **float**</span></span>

<span data-ttu-id="e99f6-117">Coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="e99f6-117">The texture coordinates.</span></span> <span data-ttu-id="e99f6-118">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="e99f6-118">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="e99f6-119">Tipo di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="e99f6-119">Texture-Object Type</span></span>                    | <span data-ttu-id="e99f6-120">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="e99f6-120">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="e99f6-121">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e99f6-121">Texture1D</span></span>                              | <span data-ttu-id="e99f6-122">float</span><span class="sxs-lookup"><span data-stu-id="e99f6-122">float</span></span>          |
| <span data-ttu-id="e99f6-123">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="e99f6-123">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="e99f6-124">float2</span><span class="sxs-lookup"><span data-stu-id="e99f6-124">float2</span></span>         |
| <span data-ttu-id="e99f6-125">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="e99f6-125">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="e99f6-126">float3</span><span class="sxs-lookup"><span data-stu-id="e99f6-126">float3</span></span>         |
| <span data-ttu-id="e99f6-127">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="e99f6-127">TextureCubeArray</span></span>                       | <span data-ttu-id="e99f6-128">float4</span><span class="sxs-lookup"><span data-stu-id="e99f6-128">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="e99f6-129">*Distorsione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e99f6-129">*Bias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e99f6-130">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="e99f6-130">Type: **float**</span></span>

<span data-ttu-id="e99f6-131">Il valore di distorsione, ovvero un numero a virgola mobile compreso tra 0,0 e 1,0 inclusivo, viene applicato a un livello MIP prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="e99f6-131">The bias value, which is a floating-point number between 0.0 and 1.0 inclusive, is applied to a mip level before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="e99f6-132">*Blocca* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e99f6-132">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e99f6-133">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="e99f6-133">Type: **float**</span></span>

<span data-ttu-id="e99f6-134">Valore facoltativo a cui bloccare i valori LOD di esempio.</span><span class="sxs-lookup"><span data-stu-id="e99f6-134">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="e99f6-135">Se ad esempio si passa 2.0 f per il valore del morsetto, si garantisce che nessun singolo campione acceda a un livello MIP inferiore a 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="e99f6-135">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="e99f6-136">*Stato* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="e99f6-136">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e99f6-137">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="e99f6-137">Type: **uint**</span></span>

<span data-ttu-id="e99f6-138">Stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="e99f6-138">The status of the operation.</span></span> <span data-ttu-id="e99f6-139">Non è possibile accedere direttamente allo stato; passare invece lo stato alla funzione intrinseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="e99f6-139">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="e99f6-140">**CheckAccessFullyMapped** restituisce **true** se tutti i valori dell'operazione di **campionamento**, **raccolta** o **caricamento** corrispondente hanno eseguito l'accesso ai riquadri mappati in una [risorsa affiancata](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="e99f6-140">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="e99f6-141">Se sono stati ricavati valori da un riquadro non mappato, **CheckAccessFullyMapped** restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="e99f6-141">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e99f6-142">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e99f6-142">Return value</span></span>

<span data-ttu-id="e99f6-143">Tipo: **[ **DXGI \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="e99f6-143">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="e99f6-144">Il formato di trama, che è uno dei valori tipizzati elencati [**nel \_ formato DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="e99f6-144">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="e99f6-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e99f6-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e99f6-146">Metodi SampleBias</span><span class="sxs-lookup"><span data-stu-id="e99f6-146">SampleBias methods</span></span>](texturecube-samplebias.md)
</dt> <dt>

[<span data-ttu-id="e99f6-147">**TextureCube**</span><span class="sxs-lookup"><span data-stu-id="e99f6-147">**TextureCube**</span></span>](texturecube.md)
</dt> </dl>

 

 
