---
title: 'Funzione SampleBias:: SampleBias (S, float, float, float)'
description: 'Esegue il campionamento di una trama, dopo aver applicato il valore di distorsione al livello mipmap, con un valore facoltativo per limitare i valori del livello di dettaglio (LOD) campione a. | Funzione SampleBias:: SampleBias (S, float, float, float)'
ms.assetid: 6683F115-4F81-4C24-B735-67DB4B52455B
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
ms.openlocfilehash: 8d95a1b0341e61853a20d313a04d1cde64dde66d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104132230"
---
# <a name="samplebiassamplebiassfloatfloatfloat-function"></a><span data-ttu-id="ee36a-105">Funzione SampleBias:: SampleBias (S, float, float, float)</span><span class="sxs-lookup"><span data-stu-id="ee36a-105">SampleBias::SampleBias(S,float,float,float) function</span></span>

<span data-ttu-id="ee36a-106">Esegue il campionamento di una trama, dopo aver applicato il valore di distorsione al livello mipmap, con un valore facoltativo per limitare i valori del livello di dettaglio (LOD) campione a.</span><span class="sxs-lookup"><span data-stu-id="ee36a-106">Samples a texture, after applying the bias value to the mipmap level, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee36a-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ee36a-107">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleBias(
  in SamplerState S,
  in float        Location,
  in float        Bias,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="ee36a-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="ee36a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee36a-109">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ee36a-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee36a-110">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="ee36a-110">Type: **SamplerState**</span></span>

<span data-ttu-id="ee36a-111">[Stato del campionatore](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="ee36a-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="ee36a-112">Si tratta di un oggetto dichiarato in un file di effetti che contiene le assegnazioni di stato.</span><span class="sxs-lookup"><span data-stu-id="ee36a-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="ee36a-113">*Posizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ee36a-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee36a-114">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="ee36a-114">Type: **float**</span></span>

<span data-ttu-id="ee36a-115">Coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="ee36a-115">The texture coordinates.</span></span> <span data-ttu-id="ee36a-116">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="ee36a-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="ee36a-117">Tipo di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="ee36a-117">Texture-Object Type</span></span>                    | <span data-ttu-id="ee36a-118">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="ee36a-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="ee36a-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ee36a-119">Texture1D</span></span>                              | <span data-ttu-id="ee36a-120">float</span><span class="sxs-lookup"><span data-stu-id="ee36a-120">float</span></span>          |
| <span data-ttu-id="ee36a-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="ee36a-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="ee36a-122">float2</span><span class="sxs-lookup"><span data-stu-id="ee36a-122">float2</span></span>         |
| <span data-ttu-id="ee36a-123">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="ee36a-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="ee36a-124">float3</span><span class="sxs-lookup"><span data-stu-id="ee36a-124">float3</span></span>         |
| <span data-ttu-id="ee36a-125">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="ee36a-125">TextureCubeArray</span></span>                       | <span data-ttu-id="ee36a-126">float4</span><span class="sxs-lookup"><span data-stu-id="ee36a-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="ee36a-127">*Distorsione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ee36a-127">*Bias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee36a-128">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="ee36a-128">Type: **float**</span></span>

<span data-ttu-id="ee36a-129">Il valore di distorsione, ovvero un numero a virgola mobile compreso tra 0,0 e 1,0 inclusivo, viene applicato a un livello MIP prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="ee36a-129">The bias value, which is a floating-point number between 0.0 and 1.0 inclusive, is applied to a mip level before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="ee36a-130">*Blocca* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ee36a-130">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee36a-131">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="ee36a-131">Type: **float**</span></span>

<span data-ttu-id="ee36a-132">Valore facoltativo a cui bloccare i valori LOD di esempio.</span><span class="sxs-lookup"><span data-stu-id="ee36a-132">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="ee36a-133">Se ad esempio si passa 2.0 f per il valore del morsetto, si garantisce che nessun singolo campione acceda a un livello MIP inferiore a 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="ee36a-133">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee36a-134">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ee36a-134">Return value</span></span>

<span data-ttu-id="ee36a-135">Tipo: **[ **DXGI \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="ee36a-135">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="ee36a-136">Il formato di trama, che è uno dei valori tipizzati elencati [**nel \_ formato DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="ee36a-136">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="ee36a-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ee36a-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee36a-138">Metodi SampleBias</span><span class="sxs-lookup"><span data-stu-id="ee36a-138">SampleBias methods</span></span>](texturecubearray-samplebias.md)
</dt> <dt>

[<span data-ttu-id="ee36a-139">**TextureCubeArray**</span><span class="sxs-lookup"><span data-stu-id="ee36a-139">**TextureCubeArray**</span></span>](texturecubearray.md)
</dt> </dl>

 

 
