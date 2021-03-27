---
title: 'Funzione SampleGrad:: SampleGrad (S, float, float, float, float) per TextureCubeArray'
description: Informazioni su come questa funzione esegue il campionamento di una trama, usando una sfumatura per influenzare il modo in cui viene calcolata la posizione di esempio. Per TextureCubeArray.
ms.assetid: 0C7DC9AA-3F0A-47E4-852F-7AE25CF67EA3
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
ms.openlocfilehash: 5320f47a5ae4db5bd96232dfa0a1d55b54f29c25
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "103762401"
---
# <a name="samplegradsamplegradsfloatfloatfloatfloat-function-for-texturecubearray"></a><span data-ttu-id="499be-105">Funzione SampleGrad:: SampleGrad (S, float, float, float, float) per TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="499be-105">SampleGrad::SampleGrad(S,float,float,float,float) function for TextureCubeArray</span></span>

<span data-ttu-id="499be-106">Esegue il campionamento di una trama, usando una sfumatura per influenzare il modo in cui viene calcolata la posizione di esempio, con un valore facoltativo per bloccare i valori del livello di dettaglio (LOD) di esempio in.</span><span class="sxs-lookup"><span data-stu-id="499be-106">Samples a texture, using a gradient to influence the way the sample location is calculated, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="499be-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="499be-107">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleGrad(
  in SamplerState S,
  in float        Location,
  in float        DDX,
  in float        DDY,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="499be-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="499be-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="499be-109">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="499be-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="499be-110">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="499be-110">Type: **SamplerState**</span></span>

<span data-ttu-id="499be-111">[Stato del campionatore](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="499be-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="499be-112">Si tratta di un oggetto dichiarato in un file di effetti che contiene le assegnazioni di stato.</span><span class="sxs-lookup"><span data-stu-id="499be-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="499be-113">*Posizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="499be-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="499be-114">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="499be-114">Type: **float**</span></span>

<span data-ttu-id="499be-115">Coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="499be-115">The texture coordinates.</span></span> <span data-ttu-id="499be-116">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="499be-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="499be-117">Tipo di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="499be-117">Texture-Object Type</span></span>                    | <span data-ttu-id="499be-118">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="499be-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="499be-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="499be-119">Texture1D</span></span>                              | <span data-ttu-id="499be-120">float</span><span class="sxs-lookup"><span data-stu-id="499be-120">float</span></span>          |
| <span data-ttu-id="499be-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="499be-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="499be-122">float2</span><span class="sxs-lookup"><span data-stu-id="499be-122">float2</span></span>         |
| <span data-ttu-id="499be-123">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="499be-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="499be-124">float3</span><span class="sxs-lookup"><span data-stu-id="499be-124">float3</span></span>         |
| <span data-ttu-id="499be-125">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="499be-125">TextureCubeArray</span></span>                       | <span data-ttu-id="499be-126">float4</span><span class="sxs-lookup"><span data-stu-id="499be-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="499be-127">*DDX* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="499be-127">*DDX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="499be-128">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="499be-128">Type: **float**</span></span>

<span data-ttu-id="499be-129">Frequenza di modifica della geometria della superficie nella direzione x.</span><span class="sxs-lookup"><span data-stu-id="499be-129">The rate of change of the surface geometry in the x direction.</span></span> <span data-ttu-id="499be-130">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="499be-130">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="499be-131">Tipo di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="499be-131">Texture-Object Type</span></span>                      | <span data-ttu-id="499be-132">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="499be-132">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="499be-133">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="499be-133">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="499be-134">float</span><span class="sxs-lookup"><span data-stu-id="499be-134">float</span></span>          |
| <span data-ttu-id="499be-135">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="499be-135">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="499be-136">float2</span><span class="sxs-lookup"><span data-stu-id="499be-136">float2</span></span>         |
| <span data-ttu-id="499be-137">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="499be-137">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="499be-138">float3</span><span class="sxs-lookup"><span data-stu-id="499be-138">float3</span></span>         |
| <span data-ttu-id="499be-139">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="499be-139">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="499be-140">non supportato</span><span class="sxs-lookup"><span data-stu-id="499be-140">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="499be-141">*Ddy* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="499be-141">*DDY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="499be-142">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="499be-142">Type: **float**</span></span>

<span data-ttu-id="499be-143">Frequenza di modifica della geometria della superficie nella direzione y.</span><span class="sxs-lookup"><span data-stu-id="499be-143">The rate of change of the surface geometry in the y direction.</span></span> <span data-ttu-id="499be-144">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="499be-144">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="499be-145">Tipo di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="499be-145">Texture-Object Type</span></span>                      | <span data-ttu-id="499be-146">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="499be-146">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="499be-147">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="499be-147">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="499be-148">float</span><span class="sxs-lookup"><span data-stu-id="499be-148">float</span></span>          |
| <span data-ttu-id="499be-149">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="499be-149">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="499be-150">float2</span><span class="sxs-lookup"><span data-stu-id="499be-150">float2</span></span>         |
| <span data-ttu-id="499be-151">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="499be-151">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="499be-152">float3</span><span class="sxs-lookup"><span data-stu-id="499be-152">float3</span></span>         |
| <span data-ttu-id="499be-153">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="499be-153">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="499be-154">non supportato</span><span class="sxs-lookup"><span data-stu-id="499be-154">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="499be-155">*Blocca* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="499be-155">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="499be-156">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="499be-156">Type: **float**</span></span>

<span data-ttu-id="499be-157">Valore facoltativo a cui bloccare i valori LOD di esempio.</span><span class="sxs-lookup"><span data-stu-id="499be-157">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="499be-158">Se ad esempio si passa 2.0 f per il valore del morsetto, si garantisce che nessun singolo campione acceda a un livello MIP inferiore a 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="499be-158">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="499be-159">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="499be-159">Return value</span></span>

<span data-ttu-id="499be-160">Tipo: **[ **DXGI \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="499be-160">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="499be-161">Il formato di trama, che è uno dei valori tipizzati elencati [**nel \_ formato DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="499be-161">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="499be-162">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="499be-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="499be-163">Metodi SampleGrad</span><span class="sxs-lookup"><span data-stu-id="499be-163">SampleGrad methods</span></span>](texturecubearray-samplegrad.md)
</dt> <dt>

[<span data-ttu-id="499be-164">**TextureCubeArray**</span><span class="sxs-lookup"><span data-stu-id="499be-164">**TextureCubeArray**</span></span>](texturecubearray.md)
</dt> </dl>

 

 
