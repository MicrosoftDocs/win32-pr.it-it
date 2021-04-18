---
title: 'Funzione SampleBias:: SampleBias (S, float, float, float) per TextureCube'
description: 'La funzione SampleBias:: SampleBias (S, float, float, float) per TextureCube campiona una trama, dopo aver applicato il valore di distorsione al livello mipmap.'
ms.assetid: BCDDADD9-D8B0-47C9-A312-5E6AF9C3C07B
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
ms.openlocfilehash: 55404f2e32f45e5b19e7b0cd4c109a6d5a8bcc13
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/02/2021
ms.locfileid: "106334321"
---
# <a name="samplebiassamplebiassfloatfloatfloat-function-for-texturecube"></a><span data-ttu-id="3563f-104">Funzione SampleBias:: SampleBias (S, float, float, float) per TextureCube</span><span class="sxs-lookup"><span data-stu-id="3563f-104">SampleBias::SampleBias(S,float,float,float) function for TextureCube</span></span>

<span data-ttu-id="3563f-105">Esegue il campionamento di una trama, dopo aver applicato il valore di distorsione al livello mipmap, con un valore facoltativo per limitare i valori del livello di dettaglio (LOD) campione a.</span><span class="sxs-lookup"><span data-stu-id="3563f-105">Samples a texture, after applying the bias value to the mipmap level, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="3563f-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3563f-106">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleBias(
  in SamplerState S,
  in float        Location,
  in float        Bias,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="3563f-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="3563f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3563f-108">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3563f-108">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3563f-109">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="3563f-109">Type: **SamplerState**</span></span>

<span data-ttu-id="3563f-110">[Stato del campionatore](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="3563f-110">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="3563f-111">Si tratta di un oggetto dichiarato in un file di effetti che contiene le assegnazioni di stato.</span><span class="sxs-lookup"><span data-stu-id="3563f-111">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="3563f-112">*Posizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3563f-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3563f-113">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="3563f-113">Type: **float**</span></span>

<span data-ttu-id="3563f-114">Coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="3563f-114">The texture coordinates.</span></span> <span data-ttu-id="3563f-115">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="3563f-115">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="3563f-116">Tipo di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="3563f-116">Texture-Object Type</span></span>                    | <span data-ttu-id="3563f-117">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="3563f-117">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="3563f-118">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3563f-118">Texture1D</span></span>                              | <span data-ttu-id="3563f-119">float</span><span class="sxs-lookup"><span data-stu-id="3563f-119">float</span></span>          |
| <span data-ttu-id="3563f-120">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="3563f-120">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="3563f-121">float2</span><span class="sxs-lookup"><span data-stu-id="3563f-121">float2</span></span>         |
| <span data-ttu-id="3563f-122">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="3563f-122">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="3563f-123">float3</span><span class="sxs-lookup"><span data-stu-id="3563f-123">float3</span></span>         |
| <span data-ttu-id="3563f-124">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="3563f-124">TextureCubeArray</span></span>                       | <span data-ttu-id="3563f-125">float4</span><span class="sxs-lookup"><span data-stu-id="3563f-125">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="3563f-126">*Distorsione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3563f-126">*Bias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3563f-127">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="3563f-127">Type: **float**</span></span>

<span data-ttu-id="3563f-128">Il valore di distorsione, ovvero un numero a virgola mobile compreso tra 0,0 e 1,0 inclusivo, viene applicato a un livello MIP prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="3563f-128">The bias value, which is a floating-point number between 0.0 and 1.0 inclusive, is applied to a mip level before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="3563f-129">*Blocca* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3563f-129">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3563f-130">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="3563f-130">Type: **float**</span></span>

<span data-ttu-id="3563f-131">Valore facoltativo a cui bloccare i valori LOD di esempio.</span><span class="sxs-lookup"><span data-stu-id="3563f-131">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="3563f-132">Se ad esempio si passa 2.0 f per il valore del morsetto, si garantisce che nessun singolo campione acceda a un livello MIP inferiore a 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="3563f-132">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3563f-133">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3563f-133">Return value</span></span>

<span data-ttu-id="3563f-134">Tipo: **[ **DXGI \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="3563f-134">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="3563f-135">Il formato di trama, che è uno dei valori tipizzati elencati [**nel \_ formato DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="3563f-135">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="3563f-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3563f-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3563f-137">Metodi SampleBias</span><span class="sxs-lookup"><span data-stu-id="3563f-137">SampleBias methods</span></span>](texturecube-samplebias.md)
</dt> <dt>

[<span data-ttu-id="3563f-138">**TextureCube**</span><span class="sxs-lookup"><span data-stu-id="3563f-138">**TextureCube**</span></span>](texturecube.md)
</dt> </dl>

 

 
