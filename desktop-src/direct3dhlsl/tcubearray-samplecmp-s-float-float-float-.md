---
title: 'Funzione SampleCmp:: SampleCmp (S, float, float, float) per TextureCubeArray'
description: 'Esegue il campionamento di una trama, usando un valore di confronto per rifiutare esempi, con un valore facoltativo per bloccare i valori del livello di dettaglio (LOD) di esempio in. | Funzione SampleCmp:: SampleCmp (S, float, float, float) per TextureCubeArray'
ms.assetid: A8824A82-A3FD-4FEE-BC10-56843997BBCE
keywords:
- Funzione SampleCmp HLSL
topic_type:
- apiref
api_name:
- SampleCmp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e65b1747d03b3a0555267f7b57e95a4d5aba54da
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "104982643"
---
# <a name="samplecmpsamplecmpsfloatfloatfloat-function-for-texturecubearray"></a><span data-ttu-id="a522c-105">Funzione SampleCmp:: SampleCmp (S, float, float, float) per TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="a522c-105">SampleCmp::SampleCmp(S,float,float,float) function for TextureCubeArray</span></span>

<span data-ttu-id="a522c-106">Esegue il campionamento di una trama, usando un valore di confronto per rifiutare esempi, con un valore facoltativo per bloccare i valori del livello di dettaglio (LOD) di esempio in.</span><span class="sxs-lookup"><span data-stu-id="a522c-106">Samples a texture, using a comparison value to reject samples, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="a522c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a522c-107">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleCmp(
  in SamplerState S,
  in float        Location,
  in float        CompareValue,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="a522c-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="a522c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a522c-109">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a522c-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a522c-110">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="a522c-110">Type: **SamplerState**</span></span>

<span data-ttu-id="a522c-111">[Stato del campionatore](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="a522c-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="a522c-112">Si tratta di un oggetto dichiarato in un file di effetti che contiene le assegnazioni di stato.</span><span class="sxs-lookup"><span data-stu-id="a522c-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="a522c-113">*Posizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a522c-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a522c-114">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="a522c-114">Type: **float**</span></span>

<span data-ttu-id="a522c-115">Coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="a522c-115">The texture coordinates.</span></span> <span data-ttu-id="a522c-116">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="a522c-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="a522c-117">Tipo di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="a522c-117">Texture-Object Type</span></span>                    | <span data-ttu-id="a522c-118">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="a522c-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="a522c-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a522c-119">Texture1D</span></span>                              | <span data-ttu-id="a522c-120">float</span><span class="sxs-lookup"><span data-stu-id="a522c-120">float</span></span>          |
| <span data-ttu-id="a522c-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="a522c-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="a522c-122">float2</span><span class="sxs-lookup"><span data-stu-id="a522c-122">float2</span></span>         |
| <span data-ttu-id="a522c-123">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="a522c-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="a522c-124">float3</span><span class="sxs-lookup"><span data-stu-id="a522c-124">float3</span></span>         |
| <span data-ttu-id="a522c-125">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="a522c-125">TextureCubeArray</span></span>                       | <span data-ttu-id="a522c-126">float4</span><span class="sxs-lookup"><span data-stu-id="a522c-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="a522c-127">*CompareValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a522c-127">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a522c-128">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="a522c-128">Type: **float**</span></span>

<span data-ttu-id="a522c-129">Valore a virgola mobile da utilizzare come valore di confronto.</span><span class="sxs-lookup"><span data-stu-id="a522c-129">A floating-point value to use as a comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="a522c-130">*Blocca* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a522c-130">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a522c-131">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="a522c-131">Type: **float**</span></span>

<span data-ttu-id="a522c-132">Valore facoltativo a cui bloccare i valori LOD di esempio.</span><span class="sxs-lookup"><span data-stu-id="a522c-132">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="a522c-133">Se ad esempio si passa 2.0 f per il valore del morsetto, si garantisce che nessun singolo campione acceda a un livello MIP inferiore a 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="a522c-133">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a522c-134">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a522c-134">Return value</span></span>

<span data-ttu-id="a522c-135">Tipo: **[ **DXGI \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="a522c-135">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="a522c-136">Il formato di trama, che è uno dei valori tipizzati elencati [**nel \_ formato DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="a522c-136">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="a522c-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a522c-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a522c-138">Metodi SampleCmp</span><span class="sxs-lookup"><span data-stu-id="a522c-138">SampleCmp methods</span></span>](texturecubearray-samplecmp.md)
</dt> <dt>

[<span data-ttu-id="a522c-139">**TextureCubeArray**</span><span class="sxs-lookup"><span data-stu-id="a522c-139">**TextureCubeArray**</span></span>](texturecubearray.md)
</dt> </dl>

 

 
