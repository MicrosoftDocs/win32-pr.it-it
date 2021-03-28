---
title: 'Funzione SampleCmp:: SampleCmp (S, float, float, int, float) per Texture2D'
description: Questa funzione esegue il campionamento di un Texture2D usando un valore di confronto per rifiutare esempi, con un valore facoltativo per bloccare i valori del livello di dettaglio (LOD) di esempio in.
ms.assetid: 1B5E6559-2524-4557-8F43-7AF258C39FB2
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
ms.openlocfilehash: 9df6a84fff7c6988ed9333584a7196fa06ad30ec
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "104982782"
---
# <a name="samplecmpsamplecmpsfloatfloatintfloat-function-for-texture2d"></a><span data-ttu-id="012fa-104">Funzione SampleCmp:: SampleCmp (S, float, float, int, float) per Texture2D</span><span class="sxs-lookup"><span data-stu-id="012fa-104">SampleCmp::SampleCmp(S,float,float,int,float) function for Texture2D</span></span>

<span data-ttu-id="012fa-105">Esegue il campionamento di un [**Texture2D**](sm5-object-texture2d.md), usando un valore di confronto per rifiutare esempi, con un valore facoltativo per bloccare i valori del livello di dettaglio (LOD) di esempio in.</span><span class="sxs-lookup"><span data-stu-id="012fa-105">Samples a [**Texture2D**](sm5-object-texture2d.md), using a comparison value to reject samples, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="012fa-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="012fa-106">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleCmp(
  in SamplerState S,
  in float        Location,
  in float        CompareValue,
  in int          Offset,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="012fa-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="012fa-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="012fa-108">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="012fa-108">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="012fa-109">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="012fa-109">Type: **SamplerState**</span></span>

<span data-ttu-id="012fa-110">[Stato del campionatore](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="012fa-110">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="012fa-111">Si tratta di un oggetto dichiarato in un file di effetti che contiene le assegnazioni di stato.</span><span class="sxs-lookup"><span data-stu-id="012fa-111">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="012fa-112">*Posizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="012fa-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="012fa-113">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="012fa-113">Type: **float**</span></span>

<span data-ttu-id="012fa-114">Coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="012fa-114">The texture coordinates.</span></span> <span data-ttu-id="012fa-115">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="012fa-115">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="012fa-116">Tipo di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="012fa-116">Texture-Object Type</span></span>                    | <span data-ttu-id="012fa-117">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="012fa-117">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="012fa-118">Texture1D</span><span class="sxs-lookup"><span data-stu-id="012fa-118">Texture1D</span></span>                              | <span data-ttu-id="012fa-119">float</span><span class="sxs-lookup"><span data-stu-id="012fa-119">float</span></span>          |
| <span data-ttu-id="012fa-120">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="012fa-120">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="012fa-121">float2</span><span class="sxs-lookup"><span data-stu-id="012fa-121">float2</span></span>         |
| <span data-ttu-id="012fa-122">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="012fa-122">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="012fa-123">float3</span><span class="sxs-lookup"><span data-stu-id="012fa-123">float3</span></span>         |
| <span data-ttu-id="012fa-124">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="012fa-124">TextureCubeArray</span></span>                       | <span data-ttu-id="012fa-125">float4</span><span class="sxs-lookup"><span data-stu-id="012fa-125">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="012fa-126">*CompareValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="012fa-126">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="012fa-127">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="012fa-127">Type: **float**</span></span>

<span data-ttu-id="012fa-128">Valore a virgola mobile da utilizzare come valore di confronto.</span><span class="sxs-lookup"><span data-stu-id="012fa-128">A floating-point value to use as a comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="012fa-129">*Offset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="012fa-129">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="012fa-130">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="012fa-130">Type: **int**</span></span>

<span data-ttu-id="012fa-131">Offset della coordinata di trama facoltativo che può essere usato per qualsiasi tipo di oggetto trama. l'offset viene applicato al percorso prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="012fa-131">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="012fa-132">Usare un offset solo in un miplevel Integer; in caso contrario, è possibile ottenere risultati che non si traducono correttamente nell'hardware.</span><span class="sxs-lookup"><span data-stu-id="012fa-132">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="012fa-133">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="012fa-133">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="012fa-134">Per altre informazioni, vedere [Applying Integer offsets](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="012fa-134">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="012fa-135">Tipo di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="012fa-135">Texture-Object Type</span></span>           | <span data-ttu-id="012fa-136">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="012fa-136">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="012fa-137">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="012fa-137">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="012fa-138">INT</span><span class="sxs-lookup"><span data-stu-id="012fa-138">int</span></span>            |
| <span data-ttu-id="012fa-139">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="012fa-139">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="012fa-140">int2</span><span class="sxs-lookup"><span data-stu-id="012fa-140">int2</span></span>           |
| <span data-ttu-id="012fa-141">Texture3D</span><span class="sxs-lookup"><span data-stu-id="012fa-141">Texture3D</span></span>                     | <span data-ttu-id="012fa-142">int3</span><span class="sxs-lookup"><span data-stu-id="012fa-142">int3</span></span>           |
| <span data-ttu-id="012fa-143">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="012fa-143">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="012fa-144">non supportato</span><span class="sxs-lookup"><span data-stu-id="012fa-144">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="012fa-145">*Blocca* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="012fa-145">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="012fa-146">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="012fa-146">Type: **float**</span></span>

<span data-ttu-id="012fa-147">Valore facoltativo a cui bloccare i valori LOD di esempio.</span><span class="sxs-lookup"><span data-stu-id="012fa-147">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="012fa-148">Se ad esempio si passa 2.0 f per il valore del morsetto, si garantisce che nessun singolo campione acceda a un livello MIP inferiore a 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="012fa-148">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="012fa-149">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="012fa-149">Return value</span></span>

<span data-ttu-id="012fa-150">Tipo: **[ **DXGI \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="012fa-150">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="012fa-151">Il formato di trama, che è uno dei valori tipizzati elencati [**nel \_ formato DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="012fa-151">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="012fa-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="012fa-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="012fa-153">Metodi SampleCmp</span><span class="sxs-lookup"><span data-stu-id="012fa-153">SampleCmp methods</span></span>](texture2d-samplecmp.md)
</dt> </dl>

 

 
