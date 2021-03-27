---
title: 'Funzione SampleCmpLevelZero:: SampleCmpLevelZero (S, float, float, uint) per TextureCubeArray'
description: Esegue il campionamento di una trama solo sul livello 0 di mipmap e confronta il risultato con un valore di confronto, quindi restituisce lo stato dell'operazione. Per TextureCubeArray.
ms.assetid: D73447C6-E77C-4027-B265-24F96C679357
keywords:
- Funzione SampleCmpLevelZero HLSL
topic_type:
- apiref
api_name:
- SampleCmpLevelZero
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ac042bd2856aa69bbba1293fb91ff74d95c0de53
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "103762400"
---
# <a name="samplecmplevelzerosamplecmplevelzerosfloatfloatuint-function-for-texturecubearray"></a><span data-ttu-id="3d4e1-105">Funzione SampleCmpLevelZero:: SampleCmpLevelZero (S, float, float, uint) per TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="3d4e1-105">SampleCmpLevelZero::SampleCmpLevelZero(S,float,float,uint) function for TextureCubeArray</span></span>

<span data-ttu-id="3d4e1-106">Esegue il campionamento di una trama solo sul livello 0 di mipmap e confronta il risultato con un valore di confronto.</span><span class="sxs-lookup"><span data-stu-id="3d4e1-106">Samples a texture on mipmap level 0 only and compares the result to a comparison value.</span></span> <span data-ttu-id="3d4e1-107">Restituisce lo stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="3d4e1-107">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d4e1-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3d4e1-108">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleCmpLevelZero(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="3d4e1-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="3d4e1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d4e1-110">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3d4e1-110">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d4e1-111">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="3d4e1-111">Type: **SamplerState**</span></span>

<span data-ttu-id="3d4e1-112">[Stato del campionatore](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="3d4e1-112">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="3d4e1-113">Si tratta di un oggetto dichiarato in un file di effetti che contiene le assegnazioni di stato.</span><span class="sxs-lookup"><span data-stu-id="3d4e1-113">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="3d4e1-114">*Posizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3d4e1-114">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d4e1-115">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="3d4e1-115">Type: **float**</span></span>

<span data-ttu-id="3d4e1-116">Coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="3d4e1-116">The texture coordinates.</span></span> <span data-ttu-id="3d4e1-117">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="3d4e1-117">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="3d4e1-118">Tipo di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="3d4e1-118">Texture-Object Type</span></span>                    | <span data-ttu-id="3d4e1-119">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="3d4e1-119">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="3d4e1-120">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3d4e1-120">Texture1D</span></span>                              | <span data-ttu-id="3d4e1-121">float</span><span class="sxs-lookup"><span data-stu-id="3d4e1-121">float</span></span>          |
| <span data-ttu-id="3d4e1-122">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="3d4e1-122">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="3d4e1-123">float2</span><span class="sxs-lookup"><span data-stu-id="3d4e1-123">float2</span></span>         |
| <span data-ttu-id="3d4e1-124">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="3d4e1-124">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="3d4e1-125">float3</span><span class="sxs-lookup"><span data-stu-id="3d4e1-125">float3</span></span>         |
| <span data-ttu-id="3d4e1-126">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="3d4e1-126">TextureCubeArray</span></span>                       | <span data-ttu-id="3d4e1-127">float4</span><span class="sxs-lookup"><span data-stu-id="3d4e1-127">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="3d4e1-128">*CompareValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3d4e1-128">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d4e1-129">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="3d4e1-129">Type: **float**</span></span>

<span data-ttu-id="3d4e1-130">Valore a virgola mobile da utilizzare come valore di confronto.</span><span class="sxs-lookup"><span data-stu-id="3d4e1-130">A floating-point value to use as a comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="3d4e1-131">*Stato* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="3d4e1-131">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3d4e1-132">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="3d4e1-132">Type: **uint**</span></span>

<span data-ttu-id="3d4e1-133">Stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="3d4e1-133">The status of the operation.</span></span> <span data-ttu-id="3d4e1-134">Non è possibile accedere direttamente allo stato; passare invece lo stato alla funzione intrinseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="3d4e1-134">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="3d4e1-135">**CheckAccessFullyMapped** restituisce **true** se tutti i valori dell'operazione di **campionamento**, **raccolta** o **caricamento** corrispondente hanno eseguito l'accesso ai riquadri mappati in una [risorsa affiancata](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="3d4e1-135">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="3d4e1-136">Se sono stati ricavati valori da un riquadro non mappato, **CheckAccessFullyMapped** restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="3d4e1-136">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d4e1-137">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3d4e1-137">Return value</span></span>

<span data-ttu-id="3d4e1-138">Tipo: **[ **DXGI \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="3d4e1-138">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="3d4e1-139">Il formato di trama, che è uno dei valori tipizzati elencati [**nel \_ formato DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="3d4e1-139">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="3d4e1-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3d4e1-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d4e1-141">Metodi SampleCmpLevelZero</span><span class="sxs-lookup"><span data-stu-id="3d4e1-141">SampleCmpLevelZero methods</span></span>](texturecubearray-samplecmplevelzero.md)
</dt> <dt>

[<span data-ttu-id="3d4e1-142">**TextureCubeArray**</span><span class="sxs-lookup"><span data-stu-id="3d4e1-142">**TextureCubeArray**</span></span>](texturecubearray.md)
</dt> </dl>

 

 
