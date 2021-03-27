---
title: 'Funzione TextureCubeArray:: Sample (S, float, float)'
description: 'Esegue il campionamento di una trama con un valore facoltativo per bloccare i valori del livello di dettaglio (LOD) di esempio in. | Funzione TextureCubeArray:: Sample (S, float, float)'
ms.assetid: E3BACA5E-18FC-4BD7-A8D8-C2808BDF1517
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
ms.openlocfilehash: 0f3f822ee334262dc50950064c6b4257aca3dd1f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981482"
---
# <a name="texturecubearraysamplesfloatfloat-function"></a><span data-ttu-id="dba37-105">Funzione TextureCubeArray:: Sample (S, float, float)</span><span class="sxs-lookup"><span data-stu-id="dba37-105">TextureCubeArray::Sample(S,float,float) function</span></span>

<span data-ttu-id="dba37-106">Esegue il campionamento di una trama con un valore facoltativo per bloccare i valori del livello di dettaglio (LOD) di esempio in.</span><span class="sxs-lookup"><span data-stu-id="dba37-106">Samples a texture with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="dba37-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dba37-107">Syntax</span></span>


``` syntax
DXGI_FORMAT Sample(
  in SamplerState S,
  in float        Location,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="dba37-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="dba37-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dba37-109">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dba37-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dba37-110">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="dba37-110">Type: **SamplerState**</span></span>

<span data-ttu-id="dba37-111">[Stato del campionatore](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="dba37-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="dba37-112">Si tratta di un oggetto dichiarato in un file di effetti che contiene le assegnazioni di stato.</span><span class="sxs-lookup"><span data-stu-id="dba37-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="dba37-113">*Posizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dba37-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dba37-114">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="dba37-114">Type: **float**</span></span>

<span data-ttu-id="dba37-115">Coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="dba37-115">The texture coordinates.</span></span> <span data-ttu-id="dba37-116">Il tipo di argomento dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="dba37-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="dba37-117">Tipo di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="dba37-117">Texture-Object Type</span></span>                    | <span data-ttu-id="dba37-118">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="dba37-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="dba37-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="dba37-119">Texture1D</span></span>                              | <span data-ttu-id="dba37-120">float</span><span class="sxs-lookup"><span data-stu-id="dba37-120">float</span></span>          |
| <span data-ttu-id="dba37-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="dba37-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="dba37-122">float2</span><span class="sxs-lookup"><span data-stu-id="dba37-122">float2</span></span>         |
| <span data-ttu-id="dba37-123">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="dba37-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="dba37-124">float3</span><span class="sxs-lookup"><span data-stu-id="dba37-124">float3</span></span>         |
| <span data-ttu-id="dba37-125">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="dba37-125">TextureCubeArray</span></span>                       | <span data-ttu-id="dba37-126">float4</span><span class="sxs-lookup"><span data-stu-id="dba37-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="dba37-127">*Blocca* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dba37-127">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dba37-128">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="dba37-128">Type: **float**</span></span>

<span data-ttu-id="dba37-129">Valore facoltativo a cui bloccare i valori LOD di esempio.</span><span class="sxs-lookup"><span data-stu-id="dba37-129">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="dba37-130">Se ad esempio si passa 2.0 f per il valore del morsetto, si garantisce che nessun singolo campione acceda a un livello MIP inferiore a 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="dba37-130">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dba37-131">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dba37-131">Return value</span></span>

<span data-ttu-id="dba37-132">Tipo: **[ **DXGI \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="dba37-132">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="dba37-133">Il formato di trama, che è uno dei valori tipizzati elencati [**nel \_ formato DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="dba37-133">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="dba37-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dba37-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dba37-135">Metodi di esempio</span><span class="sxs-lookup"><span data-stu-id="dba37-135">Sample methods</span></span>](texturecubearray-sample.md)
</dt> <dt>

[<span data-ttu-id="dba37-136">**TextureCubeArray**</span><span class="sxs-lookup"><span data-stu-id="dba37-136">**TextureCubeArray**</span></span>](texturecubearray.md)
</dt> </dl>

 

 
