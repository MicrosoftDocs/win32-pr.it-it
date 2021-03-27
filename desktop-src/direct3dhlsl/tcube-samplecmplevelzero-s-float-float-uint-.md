---
title: 'Funzione SampleCmpLevelZero:: SampleCmpLevelZero (S, float, float, uint) per TextureCube'
description: Esegue il campionamento di una trama solo sul livello 0 di mipmap e confronta il risultato con un valore di confronto. Restituisce lo stato dell'operazione. Per TextureCube.
ms.assetid: FE40307D-B9BE-434F-A6EF-7CA3C5BC7D70
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
ms.openlocfilehash: ff58c51919e575260c71f7b58d8f3d0fda6c1dd1
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "104982702"
---
# <a name="samplecmplevelzerosamplecmplevelzerosfloatfloatuint-function-for-texturecube"></a><span data-ttu-id="4eee5-106">Funzione SampleCmpLevelZero:: SampleCmpLevelZero (S, float, float, uint) per TextureCube</span><span class="sxs-lookup"><span data-stu-id="4eee5-106">SampleCmpLevelZero::SampleCmpLevelZero(S,float,float,uint) function for TextureCube</span></span>

<span data-ttu-id="4eee5-107">Esegue il campionamento di una trama solo sul livello 0 di mipmap e confronta il risultato con un valore di confronto.</span><span class="sxs-lookup"><span data-stu-id="4eee5-107">Samples a texture on mipmap level 0 only and compares the result to a comparison value.</span></span> <span data-ttu-id="4eee5-108">Restituisce lo stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="4eee5-108">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="4eee5-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4eee5-109">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleCmpLevelZero(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="4eee5-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="4eee5-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4eee5-111">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4eee5-111">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4eee5-112">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="4eee5-112">Type: **SamplerState**</span></span>

<span data-ttu-id="4eee5-113">[Stato del campionatore](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="4eee5-113">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="4eee5-114">Si tratta di un oggetto dichiarato in un file di effetti che contiene le assegnazioni di stato.</span><span class="sxs-lookup"><span data-stu-id="4eee5-114">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="4eee5-115">*Posizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4eee5-115">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4eee5-116">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="4eee5-116">Type: **float**</span></span>

<span data-ttu-id="4eee5-117">Coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="4eee5-117">The texture coordinates.</span></span> <span data-ttu-id="4eee5-118">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="4eee5-118">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="4eee5-119">Tipo di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="4eee5-119">Texture-Object Type</span></span>                    | <span data-ttu-id="4eee5-120">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="4eee5-120">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="4eee5-121">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4eee5-121">Texture1D</span></span>                              | <span data-ttu-id="4eee5-122">float</span><span class="sxs-lookup"><span data-stu-id="4eee5-122">float</span></span>          |
| <span data-ttu-id="4eee5-123">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="4eee5-123">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="4eee5-124">float2</span><span class="sxs-lookup"><span data-stu-id="4eee5-124">float2</span></span>         |
| <span data-ttu-id="4eee5-125">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="4eee5-125">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="4eee5-126">float3</span><span class="sxs-lookup"><span data-stu-id="4eee5-126">float3</span></span>         |
| <span data-ttu-id="4eee5-127">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="4eee5-127">TextureCubeArray</span></span>                       | <span data-ttu-id="4eee5-128">float4</span><span class="sxs-lookup"><span data-stu-id="4eee5-128">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="4eee5-129">*CompareValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4eee5-129">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4eee5-130">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="4eee5-130">Type: **float**</span></span>

<span data-ttu-id="4eee5-131">Valore a virgola mobile da utilizzare come valore di confronto.</span><span class="sxs-lookup"><span data-stu-id="4eee5-131">A floating-point value to use as a comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="4eee5-132">*Stato* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="4eee5-132">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4eee5-133">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="4eee5-133">Type: **uint**</span></span>

<span data-ttu-id="4eee5-134">Stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="4eee5-134">The status of the operation.</span></span> <span data-ttu-id="4eee5-135">Non è possibile accedere direttamente allo stato; passare invece lo stato alla funzione intrinseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="4eee5-135">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="4eee5-136">**CheckAccessFullyMapped** restituisce **true** se tutti i valori dell'operazione di **campionamento**, **raccolta** o **caricamento** corrispondente hanno eseguito l'accesso ai riquadri mappati in una [risorsa affiancata](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="4eee5-136">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="4eee5-137">Se sono stati ricavati valori da un riquadro non mappato, **CheckAccessFullyMapped** restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="4eee5-137">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4eee5-138">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4eee5-138">Return value</span></span>

<span data-ttu-id="4eee5-139">Tipo: **[ **DXGI \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="4eee5-139">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="4eee5-140">Il formato di trama, che è uno dei valori tipizzati elencati [**nel \_ formato DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="4eee5-140">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="4eee5-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4eee5-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4eee5-142">Metodi SampleCmpLevelZero</span><span class="sxs-lookup"><span data-stu-id="4eee5-142">SampleCmpLevelZero methods</span></span>](texturecube-samplecmplevelzero.md)
</dt> <dt>

[<span data-ttu-id="4eee5-143">**TextureCube**</span><span class="sxs-lookup"><span data-stu-id="4eee5-143">**TextureCube**</span></span>](texturecube.md)
</dt> </dl>

 

 
