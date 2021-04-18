---
title: 'Funzione SampleBias:: SampleBias (S, float, float, float, uint) per TextureCube'
description: "La funzione SampleBias:: SampleBias (S, float, float, float, uint) per TextureCube campiona una trama dopo l'applicazione del valore di distorsione al livello mipmap."
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
ms.openlocfilehash: 116749acdc23bb8ac2fd057139bf8ef7c8f5ddcc
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/02/2021
ms.locfileid: "106334322"
---
# <a name="samplebiassamplebiassfloatfloatfloatuint-function-for-texturecube"></a><span data-ttu-id="c1ae6-104">Funzione SampleBias:: SampleBias (S, float, float, float, uint) per TextureCube</span><span class="sxs-lookup"><span data-stu-id="c1ae6-104">SampleBias::SampleBias(S,float,float,float,uint) function for TextureCube</span></span>

<span data-ttu-id="c1ae6-105">Esegue il campionamento di una trama, dopo aver applicato il valore di distorsione al livello mipmap, con un valore facoltativo per limitare i valori del livello di dettaglio (LOD) campione a.</span><span class="sxs-lookup"><span data-stu-id="c1ae6-105">Samples a texture, after applying the bias value to the mipmap level, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span> <span data-ttu-id="c1ae6-106">Restituisce lo stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="c1ae6-106">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1ae6-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c1ae6-107">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleBias(
  in  SamplerState S,
  in  float        Location,
  in  float        Bias,
  in  float        Clamp,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="c1ae6-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="c1ae6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1ae6-109">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c1ae6-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1ae6-110">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="c1ae6-110">Type: **SamplerState**</span></span>

<span data-ttu-id="c1ae6-111">[Stato del campionatore](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="c1ae6-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="c1ae6-112">Si tratta di un oggetto dichiarato in un file di effetti che contiene le assegnazioni di stato.</span><span class="sxs-lookup"><span data-stu-id="c1ae6-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="c1ae6-113">*Posizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c1ae6-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1ae6-114">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="c1ae6-114">Type: **float**</span></span>

<span data-ttu-id="c1ae6-115">Coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="c1ae6-115">The texture coordinates.</span></span> <span data-ttu-id="c1ae6-116">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="c1ae6-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="c1ae6-117">Tipo di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="c1ae6-117">Texture-Object Type</span></span>                    | <span data-ttu-id="c1ae6-118">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="c1ae6-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="c1ae6-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="c1ae6-119">Texture1D</span></span>                              | <span data-ttu-id="c1ae6-120">float</span><span class="sxs-lookup"><span data-stu-id="c1ae6-120">float</span></span>          |
| <span data-ttu-id="c1ae6-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="c1ae6-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="c1ae6-122">float2</span><span class="sxs-lookup"><span data-stu-id="c1ae6-122">float2</span></span>         |
| <span data-ttu-id="c1ae6-123">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="c1ae6-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="c1ae6-124">float3</span><span class="sxs-lookup"><span data-stu-id="c1ae6-124">float3</span></span>         |
| <span data-ttu-id="c1ae6-125">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="c1ae6-125">TextureCubeArray</span></span>                       | <span data-ttu-id="c1ae6-126">float4</span><span class="sxs-lookup"><span data-stu-id="c1ae6-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="c1ae6-127">*Distorsione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c1ae6-127">*Bias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1ae6-128">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="c1ae6-128">Type: **float**</span></span>

<span data-ttu-id="c1ae6-129">Il valore di distorsione, ovvero un numero a virgola mobile compreso tra 0,0 e 1,0 inclusivo, viene applicato a un livello MIP prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="c1ae6-129">The bias value, which is a floating-point number between 0.0 and 1.0 inclusive, is applied to a mip level before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="c1ae6-130">*Blocca* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c1ae6-130">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1ae6-131">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="c1ae6-131">Type: **float**</span></span>

<span data-ttu-id="c1ae6-132">Valore facoltativo a cui bloccare i valori LOD di esempio.</span><span class="sxs-lookup"><span data-stu-id="c1ae6-132">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="c1ae6-133">Se ad esempio si passa 2.0 f per il valore del morsetto, si garantisce che nessun singolo campione acceda a un livello MIP inferiore a 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="c1ae6-133">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="c1ae6-134">*Stato* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="c1ae6-134">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c1ae6-135">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="c1ae6-135">Type: **uint**</span></span>

<span data-ttu-id="c1ae6-136">Stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="c1ae6-136">The status of the operation.</span></span> <span data-ttu-id="c1ae6-137">Non è possibile accedere direttamente allo stato; passare invece lo stato alla funzione intrinseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="c1ae6-137">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="c1ae6-138">**CheckAccessFullyMapped** restituisce **true** se tutti i valori dell'operazione di **campionamento**, **raccolta** o **caricamento** corrispondente hanno eseguito l'accesso ai riquadri mappati in una [risorsa affiancata](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="c1ae6-138">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="c1ae6-139">Se sono stati ricavati valori da un riquadro non mappato, **CheckAccessFullyMapped** restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="c1ae6-139">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1ae6-140">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c1ae6-140">Return value</span></span>

<span data-ttu-id="c1ae6-141">Tipo: **[ **DXGI \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="c1ae6-141">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="c1ae6-142">Il formato di trama, che è uno dei valori tipizzati elencati [**nel \_ formato DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="c1ae6-142">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="c1ae6-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c1ae6-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1ae6-144">Metodi SampleBias</span><span class="sxs-lookup"><span data-stu-id="c1ae6-144">SampleBias methods</span></span>](texturecube-samplebias.md)
</dt> <dt>

[<span data-ttu-id="c1ae6-145">**TextureCube**</span><span class="sxs-lookup"><span data-stu-id="c1ae6-145">**TextureCube**</span></span>](texturecube.md)
</dt> </dl>

 

 
