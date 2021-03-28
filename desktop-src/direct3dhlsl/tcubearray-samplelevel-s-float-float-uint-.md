---
title: 'Funzione SampleLevel:: SampleLevel (S, float, float, uint)'
description: "Esegue il campionamento di una trama sul livello mipmap specificato e restituisce lo stato dell'operazione. | Funzione SampleLevel:: SampleLevel (S, float, float, uint)"
ms.assetid: 3794D17F-BC70-4D3A-9F2C-ADF900983D2C
keywords:
- Funzione SampleLevel HLSL
topic_type:
- apiref
api_name:
- SampleLevel
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 356e2779d82e886946e93d2071ae693279c07eb8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104234770"
---
# <a name="samplelevelsamplelevelsfloatfloatuint-function"></a><span data-ttu-id="8bae0-105">Funzione SampleLevel:: SampleLevel (S, float, float, uint)</span><span class="sxs-lookup"><span data-stu-id="8bae0-105">SampleLevel::SampleLevel(S,float,float,uint) function</span></span>

<span data-ttu-id="8bae0-106">Esegue il campionamento di una trama sul livello mipmap specificato e restituisce lo stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="8bae0-106">Samples a texture on the specified mipmap level and returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="8bae0-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8bae0-107">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleLevel(
  in  SamplerState S,
  in  float        Location,
  in  float        LOD,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="8bae0-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="8bae0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8bae0-109">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8bae0-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8bae0-110">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="8bae0-110">Type: **SamplerState**</span></span>

<span data-ttu-id="8bae0-111">[Stato del campionatore](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="8bae0-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="8bae0-112">Si tratta di un oggetto dichiarato in un file di effetti che contiene le assegnazioni di stato.</span><span class="sxs-lookup"><span data-stu-id="8bae0-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="8bae0-113">*Posizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8bae0-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8bae0-114">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="8bae0-114">Type: **float**</span></span>

<span data-ttu-id="8bae0-115">Coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="8bae0-115">The texture coordinates.</span></span> <span data-ttu-id="8bae0-116">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="8bae0-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="8bae0-117">Tipo di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="8bae0-117">Texture-Object Type</span></span>                    | <span data-ttu-id="8bae0-118">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="8bae0-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="8bae0-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="8bae0-119">Texture1D</span></span>                              | <span data-ttu-id="8bae0-120">float</span><span class="sxs-lookup"><span data-stu-id="8bae0-120">float</span></span>          |
| <span data-ttu-id="8bae0-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="8bae0-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="8bae0-122">float2</span><span class="sxs-lookup"><span data-stu-id="8bae0-122">float2</span></span>         |
| <span data-ttu-id="8bae0-123">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="8bae0-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="8bae0-124">float3</span><span class="sxs-lookup"><span data-stu-id="8bae0-124">float3</span></span>         |
| <span data-ttu-id="8bae0-125">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="8bae0-125">TextureCubeArray</span></span>                       | <span data-ttu-id="8bae0-126">float4</span><span class="sxs-lookup"><span data-stu-id="8bae0-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="8bae0-127">*LOD* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8bae0-127">*LOD* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8bae0-128">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="8bae0-128">Type: **float**</span></span>

<span data-ttu-id="8bae0-129">\[in \] un numero che specifica il livello mipmap.</span><span class="sxs-lookup"><span data-stu-id="8bae0-129">\[in\] A number that specifies the mipmap level.</span></span> <span data-ttu-id="8bae0-130">Se il valore è ≤ 0, viene usato il livello mipmap 0 (mapping più grande).</span><span class="sxs-lookup"><span data-stu-id="8bae0-130">If the value is ≤ 0, mipmap level 0 (biggest map) is used.</span></span> <span data-ttu-id="8bae0-131">Il valore frazionario (se fornito) viene usato per interpolare tra due livelli di mipmap.</span><span class="sxs-lookup"><span data-stu-id="8bae0-131">The fractional value (if supplied) is used to interpolate between two mipmap levels.</span></span>

</dd> <dt>

<span data-ttu-id="8bae0-132">*Stato* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="8bae0-132">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8bae0-133">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="8bae0-133">Type: **uint**</span></span>

<span data-ttu-id="8bae0-134">Stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="8bae0-134">The status of the operation.</span></span> <span data-ttu-id="8bae0-135">Non è possibile accedere direttamente allo stato; passare invece lo stato alla funzione intrinseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="8bae0-135">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="8bae0-136">**CheckAccessFullyMapped** restituisce **true** se tutti i valori dell'operazione di **campionamento**, **raccolta** o **caricamento** corrispondente hanno eseguito l'accesso ai riquadri mappati in una [risorsa affiancata](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="8bae0-136">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="8bae0-137">Se sono stati ricavati valori da un riquadro non mappato, **CheckAccessFullyMapped** restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="8bae0-137">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8bae0-138">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8bae0-138">Return value</span></span>

<span data-ttu-id="8bae0-139">Tipo: **[ **DXGI \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="8bae0-139">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="8bae0-140">Il formato di trama, che è uno dei valori tipizzati elencati [**nel \_ formato DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="8bae0-140">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="8bae0-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8bae0-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8bae0-142">Metodi SampleLevel</span><span class="sxs-lookup"><span data-stu-id="8bae0-142">SampleLevel methods</span></span>](texturecubearray-samplelevel.md)
</dt> <dt>

[<span data-ttu-id="8bae0-143">**TextureCubeArray**</span><span class="sxs-lookup"><span data-stu-id="8bae0-143">**TextureCubeArray**</span></span>](texturecubearray.md)
</dt> </dl>

 

 
