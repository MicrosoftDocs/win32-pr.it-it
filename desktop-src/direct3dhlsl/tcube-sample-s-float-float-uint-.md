---
title: 'Funzione TextureCube:: Sample (S, float, float, uint)'
description: "Esegue il campionamento di una trama con un valore facoltativo per bloccare i valori del livello di dettaglio (LOD) di esempio in e restituisce lo stato dell'operazione. | Funzione TextureCube:: Sample (S, float, float, uint)"
ms.assetid: 8FA17583-9002-4DEC-A6D5-85B25DEA19B7
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
ms.openlocfilehash: 9a91e9a3dcc2df617f50175eb0872398bc564103
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981762"
---
# <a name="texturecubesamplesfloatfloatuint-function"></a><span data-ttu-id="fa639-105">Funzione TextureCube:: Sample (S, float, float, uint)</span><span class="sxs-lookup"><span data-stu-id="fa639-105">TextureCube::Sample(S,float,float,uint) function</span></span>

<span data-ttu-id="fa639-106">Esegue il campionamento di una trama con un valore facoltativo per bloccare i valori del livello di dettaglio (LOD) di esempio in e restituisce lo stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="fa639-106">Samples a texture with an optional value to clamp sample level-of-detail (LOD) values to, and returns status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa639-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fa639-107">Syntax</span></span>


``` syntax
DXGI_FORMAT Sample(
  in  SamplerState S,
  in  float        Location,
  in  float        Clamp,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="fa639-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="fa639-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa639-109">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fa639-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa639-110">[Stato del campionatore](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="fa639-110">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="fa639-111">Si tratta di un oggetto dichiarato in un file di effetti che contiene le assegnazioni di stato.</span><span class="sxs-lookup"><span data-stu-id="fa639-111">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="fa639-112">*Posizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fa639-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa639-113">Coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="fa639-113">The texture coordinates.</span></span> <span data-ttu-id="fa639-114">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="fa639-114">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="fa639-115">Tipo di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="fa639-115">Texture-Object Type</span></span>                    | <span data-ttu-id="fa639-116">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="fa639-116">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="fa639-117">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fa639-117">Texture1D</span></span>                              | <span data-ttu-id="fa639-118">float</span><span class="sxs-lookup"><span data-stu-id="fa639-118">float</span></span>          |
| <span data-ttu-id="fa639-119">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="fa639-119">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="fa639-120">float2</span><span class="sxs-lookup"><span data-stu-id="fa639-120">float2</span></span>         |
| <span data-ttu-id="fa639-121">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="fa639-121">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="fa639-122">float3</span><span class="sxs-lookup"><span data-stu-id="fa639-122">float3</span></span>         |
| <span data-ttu-id="fa639-123">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="fa639-123">TextureCubeArray</span></span>                       | <span data-ttu-id="fa639-124">float4</span><span class="sxs-lookup"><span data-stu-id="fa639-124">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="fa639-125">*Blocca* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fa639-125">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa639-126">Valore facoltativo a cui bloccare i valori LOD di esempio.</span><span class="sxs-lookup"><span data-stu-id="fa639-126">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="fa639-127">Se ad esempio si passa 2.0 f per il valore del morsetto, si garantisce che nessun singolo campione acceda a un livello MIP inferiore a 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="fa639-127">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="fa639-128">*Stato* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="fa639-128">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fa639-129">Stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="fa639-129">The status of the operation.</span></span> <span data-ttu-id="fa639-130">Non è possibile accedere direttamente allo stato; passare invece lo stato alla funzione intrinseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="fa639-130">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="fa639-131">**CheckAccessFullyMapped** restituisce **true** se tutti i valori dell'operazione di **campionamento**, **raccolta** o **caricamento** corrispondente hanno eseguito l'accesso ai riquadri mappati in una [risorsa affiancata](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="fa639-131">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="fa639-132">Se sono stati ricavati valori da un riquadro non mappato, **CheckAccessFullyMapped** restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="fa639-132">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa639-133">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fa639-133">Return value</span></span>

<span data-ttu-id="fa639-134">Il formato di trama, che è uno dei valori tipizzati elencati [**nel \_ formato DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="fa639-134">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="fa639-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fa639-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa639-136">Metodi di esempio</span><span class="sxs-lookup"><span data-stu-id="fa639-136">Sample methods</span></span>](texturecube-sample.md)
</dt> <dt>

[<span data-ttu-id="fa639-137">**TextureCube**</span><span class="sxs-lookup"><span data-stu-id="fa639-137">**TextureCube**</span></span>](texturecube.md)
</dt> </dl>

 

 
