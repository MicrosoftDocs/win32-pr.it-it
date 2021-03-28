---
title: 'Funzione SampleCmp:: SampleCmp (S, float, float, float, uint) per TextureCubeArray'
description: 'Esegue il campionamento di una trama, usando un valore di confronto per rifiutare esempi, con un valore facoltativo per bloccare i valori del livello di dettaglio (LOD) di esempio in. | Funzione SampleCmp:: SampleCmp (S, float, float, float, uint) per TextureCubeArray'
ms.assetid: 5596D341-C057-414D-B1EC-7AA78693D32C
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
ms.openlocfilehash: 20626fe9d209ef4bfb64805f1a12561fd324f5a2
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "104996353"
---
# <a name="samplecmpsamplecmpsfloatfloatfloatuint-function-for-texturecubearray"></a><span data-ttu-id="53f9b-105">Funzione SampleCmp:: SampleCmp (S, float, float, float, uint) per TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="53f9b-105">SampleCmp::SampleCmp(S,float,float,float,uint) function for TextureCubeArray</span></span>

<span data-ttu-id="53f9b-106">Esegue il campionamento di una trama, usando un valore di confronto per rifiutare esempi, con un valore facoltativo per bloccare i valori del livello di dettaglio (LOD) di esempio in.</span><span class="sxs-lookup"><span data-stu-id="53f9b-106">Samples a texture, using a comparison value to reject samples, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span> <span data-ttu-id="53f9b-107">Restituisce lo stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="53f9b-107">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="53f9b-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="53f9b-108">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleCmp(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  in  float        Clamp,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="53f9b-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="53f9b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53f9b-110">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="53f9b-110">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53f9b-111">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="53f9b-111">Type: **SamplerState**</span></span>

<span data-ttu-id="53f9b-112">[Stato del campionatore](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="53f9b-112">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="53f9b-113">Si tratta di un oggetto dichiarato in un file di effetti che contiene le assegnazioni di stato.</span><span class="sxs-lookup"><span data-stu-id="53f9b-113">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="53f9b-114">*Posizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="53f9b-114">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53f9b-115">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="53f9b-115">Type: **float**</span></span>

<span data-ttu-id="53f9b-116">Coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="53f9b-116">The texture coordinates.</span></span> <span data-ttu-id="53f9b-117">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="53f9b-117">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="53f9b-118">Tipo di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="53f9b-118">Texture-Object Type</span></span>                    | <span data-ttu-id="53f9b-119">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="53f9b-119">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="53f9b-120">Texture1D</span><span class="sxs-lookup"><span data-stu-id="53f9b-120">Texture1D</span></span>                              | <span data-ttu-id="53f9b-121">float</span><span class="sxs-lookup"><span data-stu-id="53f9b-121">float</span></span>          |
| <span data-ttu-id="53f9b-122">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="53f9b-122">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="53f9b-123">float2</span><span class="sxs-lookup"><span data-stu-id="53f9b-123">float2</span></span>         |
| <span data-ttu-id="53f9b-124">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="53f9b-124">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="53f9b-125">float3</span><span class="sxs-lookup"><span data-stu-id="53f9b-125">float3</span></span>         |
| <span data-ttu-id="53f9b-126">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="53f9b-126">TextureCubeArray</span></span>                       | <span data-ttu-id="53f9b-127">float4</span><span class="sxs-lookup"><span data-stu-id="53f9b-127">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="53f9b-128">*CompareValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="53f9b-128">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53f9b-129">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="53f9b-129">Type: **float**</span></span>

<span data-ttu-id="53f9b-130">Valore a virgola mobile da utilizzare come valore di confronto.</span><span class="sxs-lookup"><span data-stu-id="53f9b-130">A floating-point value to use as a comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="53f9b-131">*Blocca* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="53f9b-131">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53f9b-132">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="53f9b-132">Type: **float**</span></span>

<span data-ttu-id="53f9b-133">Valore facoltativo a cui bloccare i valori LOD di esempio.</span><span class="sxs-lookup"><span data-stu-id="53f9b-133">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="53f9b-134">Se ad esempio si passa 2.0 f per il valore del morsetto, si garantisce che nessun singolo campione acceda a un livello MIP inferiore a 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="53f9b-134">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="53f9b-135">*Stato* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="53f9b-135">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="53f9b-136">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="53f9b-136">Type: **uint**</span></span>

<span data-ttu-id="53f9b-137">Stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="53f9b-137">The status of the operation.</span></span> <span data-ttu-id="53f9b-138">Non è possibile accedere direttamente allo stato; passare invece lo stato alla funzione intrinseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="53f9b-138">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="53f9b-139">**CheckAccessFullyMapped** restituisce **true** se tutti i valori dell'operazione di **campionamento**, **raccolta** o **caricamento** corrispondente hanno eseguito l'accesso ai riquadri mappati in una [risorsa affiancata](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="53f9b-139">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="53f9b-140">Se sono stati ricavati valori da un riquadro non mappato, **CheckAccessFullyMapped** restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="53f9b-140">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53f9b-141">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="53f9b-141">Return value</span></span>

<span data-ttu-id="53f9b-142">Tipo: **[ **DXGI \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="53f9b-142">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="53f9b-143">Il formato di trama, che è uno dei valori tipizzati elencati [**nel \_ formato DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="53f9b-143">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="53f9b-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="53f9b-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53f9b-145">Metodi SampleCmp</span><span class="sxs-lookup"><span data-stu-id="53f9b-145">SampleCmp methods</span></span>](texturecubearray-samplecmp.md)
</dt> <dt>

[<span data-ttu-id="53f9b-146">**TextureCubeArray**</span><span class="sxs-lookup"><span data-stu-id="53f9b-146">**TextureCubeArray**</span></span>](texturecubearray.md)
</dt> </dl>

 

 
