---
title: 'Funzione TextureCubeArray:: Sample (S, float, float, uint)'
description: "Esegue il campionamento di una trama con un valore facoltativo per bloccare i valori del livello di dettaglio (LOD) di esempio in e restituisce lo stato dell'operazione. | Funzione TextureCubeArray:: Sample (S, float, float, uint)"
ms.assetid: 5645841D-A32E-452E-873C-E070CF6A4C00
keywords:
- Funzione di esempio HLSL
topic_type:
- apiref
api_name:
- Sample
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 24e6d77698507f0d1673b66954db8e78466ac728
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "103761704"
---
# <a name="texturecubearraysamplesfloatfloatuint-function"></a><span data-ttu-id="ec2a7-105">Funzione TextureCubeArray:: Sample (S, float, float, uint)</span><span class="sxs-lookup"><span data-stu-id="ec2a7-105">TextureCubeArray::Sample(S,float,float,uint) function</span></span>

<span data-ttu-id="ec2a7-106">Esegue il campionamento di una trama con un valore facoltativo per bloccare i valori del livello di dettaglio (LOD) di esempio in e restituisce lo stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="ec2a7-106">Samples a texture with an optional value to clamp sample level-of-detail (LOD) values to, and returns status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec2a7-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ec2a7-107">Syntax</span></span>


``` syntax
DXGI_FORMAT Sample(
  in  SamplerState S,
  in  float        Location,
  in  float        Clamp,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="ec2a7-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="ec2a7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec2a7-109">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ec2a7-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec2a7-110">[Stato del campionatore](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="ec2a7-110">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="ec2a7-111">Si tratta di un oggetto dichiarato in un file di effetti che contiene le assegnazioni di stato.</span><span class="sxs-lookup"><span data-stu-id="ec2a7-111">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="ec2a7-112">*Posizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ec2a7-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec2a7-113">Coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="ec2a7-113">The texture coordinates.</span></span> <span data-ttu-id="ec2a7-114">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="ec2a7-114">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="ec2a7-115">Tipo di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="ec2a7-115">Texture-Object Type</span></span>                    | <span data-ttu-id="ec2a7-116">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="ec2a7-116">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="ec2a7-117">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ec2a7-117">Texture1D</span></span>                              | <span data-ttu-id="ec2a7-118">float</span><span class="sxs-lookup"><span data-stu-id="ec2a7-118">float</span></span>          |
| <span data-ttu-id="ec2a7-119">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="ec2a7-119">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="ec2a7-120">float2</span><span class="sxs-lookup"><span data-stu-id="ec2a7-120">float2</span></span>         |
| <span data-ttu-id="ec2a7-121">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="ec2a7-121">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="ec2a7-122">float3</span><span class="sxs-lookup"><span data-stu-id="ec2a7-122">float3</span></span>         |
| <span data-ttu-id="ec2a7-123">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="ec2a7-123">TextureCubeArray</span></span>                       | <span data-ttu-id="ec2a7-124">float4</span><span class="sxs-lookup"><span data-stu-id="ec2a7-124">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="ec2a7-125">*Blocca* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ec2a7-125">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec2a7-126">Valore facoltativo a cui bloccare i valori LOD di esempio.</span><span class="sxs-lookup"><span data-stu-id="ec2a7-126">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="ec2a7-127">Se ad esempio si passa 2.0 f per il valore del morsetto, si garantisce che nessun singolo campione acceda a un livello MIP inferiore a 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="ec2a7-127">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="ec2a7-128">*Stato* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="ec2a7-128">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ec2a7-129">Stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="ec2a7-129">The status of the operation.</span></span> <span data-ttu-id="ec2a7-130">Non è possibile accedere direttamente allo stato; passare invece lo stato alla funzione intrinseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="ec2a7-130">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="ec2a7-131">**CheckAccessFullyMapped** restituisce **true** se tutti i valori dell'operazione di **campionamento**, **raccolta** o **caricamento** corrispondente hanno eseguito l'accesso ai riquadri mappati in una [risorsa affiancata](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="ec2a7-131">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="ec2a7-132">Se sono stati ricavati valori da un riquadro non mappato, **CheckAccessFullyMapped** restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="ec2a7-132">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec2a7-133">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ec2a7-133">Return value</span></span>

<span data-ttu-id="ec2a7-134">Il formato di trama, che è uno dei valori tipizzati elencati [**nel \_ formato DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="ec2a7-134">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="ec2a7-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ec2a7-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec2a7-136">Metodi di esempio</span><span class="sxs-lookup"><span data-stu-id="ec2a7-136">Sample methods</span></span>](texturecubearray-sample.md)
</dt> <dt>

[<span data-ttu-id="ec2a7-137">**TextureCubeArray**</span><span class="sxs-lookup"><span data-stu-id="ec2a7-137">**TextureCubeArray**</span></span>](texturecubearray.md)
</dt> </dl>

 

 
