---
title: 'Funzione TextureCube:: Sample (S, float, float)'
description: 'Esegue il campionamento di una trama con un valore facoltativo per bloccare i valori del livello di dettaglio (LOD) di esempio in. | Funzione TextureCube:: Sample (S, float, float)'
ms.assetid: 7DB25135-46B5-48E2-91D0-A45D355179D6
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
ms.openlocfilehash: 2ce841eb68e426fc76032d45353f2b439f0f3e4b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104234637"
---
# <a name="texturecubesamplesfloatfloat-function"></a><span data-ttu-id="a0f6f-105">Funzione TextureCube:: Sample (S, float, float)</span><span class="sxs-lookup"><span data-stu-id="a0f6f-105">TextureCube::Sample(S,float,float) function</span></span>

<span data-ttu-id="a0f6f-106">Esegue il campionamento di una trama con un valore facoltativo per bloccare i valori del livello di dettaglio (LOD) di esempio in.</span><span class="sxs-lookup"><span data-stu-id="a0f6f-106">Samples a texture with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0f6f-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a0f6f-107">Syntax</span></span>


``` syntax
DXGI_FORMAT Sample(
  in SamplerState S,
  in float        Location,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="a0f6f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="a0f6f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0f6f-109">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a0f6f-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0f6f-110">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="a0f6f-110">Type: **SamplerState**</span></span>

<span data-ttu-id="a0f6f-111">[Stato del campionatore](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="a0f6f-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="a0f6f-112">Si tratta di un oggetto dichiarato in un file di effetti che contiene le assegnazioni di stato.</span><span class="sxs-lookup"><span data-stu-id="a0f6f-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="a0f6f-113">*Posizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a0f6f-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0f6f-114">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="a0f6f-114">Type: **float**</span></span>

<span data-ttu-id="a0f6f-115">Coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="a0f6f-115">The texture coordinates.</span></span> <span data-ttu-id="a0f6f-116">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="a0f6f-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="a0f6f-117">Tipo di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="a0f6f-117">Texture-Object Type</span></span>                    | <span data-ttu-id="a0f6f-118">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="a0f6f-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="a0f6f-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a0f6f-119">Texture1D</span></span>                              | <span data-ttu-id="a0f6f-120">float</span><span class="sxs-lookup"><span data-stu-id="a0f6f-120">float</span></span>          |
| <span data-ttu-id="a0f6f-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="a0f6f-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="a0f6f-122">float2</span><span class="sxs-lookup"><span data-stu-id="a0f6f-122">float2</span></span>         |
| <span data-ttu-id="a0f6f-123">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="a0f6f-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="a0f6f-124">float3</span><span class="sxs-lookup"><span data-stu-id="a0f6f-124">float3</span></span>         |
| <span data-ttu-id="a0f6f-125">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="a0f6f-125">TextureCubeArray</span></span>                       | <span data-ttu-id="a0f6f-126">float4</span><span class="sxs-lookup"><span data-stu-id="a0f6f-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="a0f6f-127">*Blocca* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a0f6f-127">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0f6f-128">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="a0f6f-128">Type: **float**</span></span>

<span data-ttu-id="a0f6f-129">Valore facoltativo a cui bloccare i valori LOD di esempio.</span><span class="sxs-lookup"><span data-stu-id="a0f6f-129">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="a0f6f-130">Se ad esempio si passa 2.0 f per il valore del morsetto, si garantisce che nessun singolo campione acceda a un livello MIP inferiore a 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="a0f6f-130">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0f6f-131">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a0f6f-131">Return value</span></span>

<span data-ttu-id="a0f6f-132">Tipo: **[ **DXGI \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="a0f6f-132">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="a0f6f-133">Il formato di trama, che è uno dei valori tipizzati elencati [**nel \_ formato DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="a0f6f-133">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="a0f6f-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a0f6f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0f6f-135">Metodi di esempio</span><span class="sxs-lookup"><span data-stu-id="a0f6f-135">Sample methods</span></span>](texturecube-sample.md)
</dt> <dt>

[<span data-ttu-id="a0f6f-136">**TextureCube**</span><span class="sxs-lookup"><span data-stu-id="a0f6f-136">**TextureCube**</span></span>](texturecube.md)
</dt> </dl>

 

 
