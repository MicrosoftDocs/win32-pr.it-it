---
title: 'Funzione SampleBias:: SampleBias (S, float, float, float, uint)'
description: "Esegue il campionamento di una trama, dopo aver applicato il valore di distorsione al livello mipmap, con un valore facoltativo per limitare i valori del livello di dettaglio (LOD) campione a. Restituisce lo stato dell'operazione. | Funzione SampleBias:: SampleBias (S, float, float, float, uint)"
ms.assetid: 376F11E6-4FFF-4685-9285-9D6143C77F2D
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
ms.openlocfilehash: b91491b6ff43862a8dbbdb55120f5af8f80bec85
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981474"
---
# <a name="samplebiassamplebiassfloatfloatfloatuint-function"></a><span data-ttu-id="101fd-106">Funzione SampleBias:: SampleBias (S, float, float, float, uint)</span><span class="sxs-lookup"><span data-stu-id="101fd-106">SampleBias::SampleBias(S,float,float,float,uint) function</span></span>

<span data-ttu-id="101fd-107">Esegue il campionamento di una trama, dopo aver applicato il valore di distorsione al livello mipmap, con un valore facoltativo per limitare i valori del livello di dettaglio (LOD) campione a.</span><span class="sxs-lookup"><span data-stu-id="101fd-107">Samples a texture, after applying the bias value to the mipmap level, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span> <span data-ttu-id="101fd-108">Restituisce lo stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="101fd-108">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="101fd-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="101fd-109">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleBias(
  in  SamplerState S,
  in  float        Location,
  in  float        Bias,
  in  float        Clamp,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="101fd-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="101fd-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="101fd-111">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="101fd-111">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="101fd-112">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="101fd-112">Type: **SamplerState**</span></span>

<span data-ttu-id="101fd-113">[Stato del campionatore](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="101fd-113">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="101fd-114">Si tratta di un oggetto dichiarato in un file di effetti che contiene le assegnazioni di stato.</span><span class="sxs-lookup"><span data-stu-id="101fd-114">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="101fd-115">*Posizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="101fd-115">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="101fd-116">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="101fd-116">Type: **float**</span></span>

<span data-ttu-id="101fd-117">Coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="101fd-117">The texture coordinates.</span></span> <span data-ttu-id="101fd-118">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="101fd-118">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="101fd-119">Tipo di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="101fd-119">Texture-Object Type</span></span>                    | <span data-ttu-id="101fd-120">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="101fd-120">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="101fd-121">Texture1D</span><span class="sxs-lookup"><span data-stu-id="101fd-121">Texture1D</span></span>                              | <span data-ttu-id="101fd-122">float</span><span class="sxs-lookup"><span data-stu-id="101fd-122">float</span></span>          |
| <span data-ttu-id="101fd-123">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="101fd-123">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="101fd-124">float2</span><span class="sxs-lookup"><span data-stu-id="101fd-124">float2</span></span>         |
| <span data-ttu-id="101fd-125">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="101fd-125">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="101fd-126">float3</span><span class="sxs-lookup"><span data-stu-id="101fd-126">float3</span></span>         |
| <span data-ttu-id="101fd-127">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="101fd-127">TextureCubeArray</span></span>                       | <span data-ttu-id="101fd-128">float4</span><span class="sxs-lookup"><span data-stu-id="101fd-128">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="101fd-129">*Distorsione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="101fd-129">*Bias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="101fd-130">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="101fd-130">Type: **float**</span></span>

<span data-ttu-id="101fd-131">Il valore di distorsione, ovvero un numero a virgola mobile compreso tra 0,0 e 1,0 inclusivo, viene applicato a un livello MIP prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="101fd-131">The bias value, which is a floating-point number between 0.0 and 1.0 inclusive, is applied to a mip level before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="101fd-132">*Blocca* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="101fd-132">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="101fd-133">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="101fd-133">Type: **float**</span></span>

<span data-ttu-id="101fd-134">Valore facoltativo a cui bloccare i valori LOD di esempio.</span><span class="sxs-lookup"><span data-stu-id="101fd-134">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="101fd-135">Se ad esempio si passa 2.0 f per il valore del morsetto, si garantisce che nessun singolo campione acceda a un livello MIP inferiore a 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="101fd-135">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="101fd-136">*Stato* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="101fd-136">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="101fd-137">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="101fd-137">Type: **uint**</span></span>

<span data-ttu-id="101fd-138">Stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="101fd-138">The status of the operation.</span></span> <span data-ttu-id="101fd-139">Non è possibile accedere direttamente allo stato; passare invece lo stato alla funzione intrinseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="101fd-139">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="101fd-140">**CheckAccessFullyMapped** restituisce **true** se tutti i valori dell'operazione di **campionamento**, **raccolta** o **caricamento** corrispondente hanno eseguito l'accesso ai riquadri mappati in una [risorsa affiancata](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="101fd-140">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="101fd-141">Se sono stati ricavati valori da un riquadro non mappato, **CheckAccessFullyMapped** restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="101fd-141">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="101fd-142">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="101fd-142">Return value</span></span>

<span data-ttu-id="101fd-143">Tipo: **[ **DXGI \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="101fd-143">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="101fd-144">Il formato di trama, che è uno dei valori tipizzati elencati [**nel \_ formato DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="101fd-144">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="101fd-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="101fd-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="101fd-146">Metodi SampleBias</span><span class="sxs-lookup"><span data-stu-id="101fd-146">SampleBias methods</span></span>](texturecubearray-samplebias.md)
</dt> <dt>

[<span data-ttu-id="101fd-147">**TextureCubeArray**</span><span class="sxs-lookup"><span data-stu-id="101fd-147">**TextureCubeArray**</span></span>](texturecubearray.md)
</dt> </dl>

 

 
