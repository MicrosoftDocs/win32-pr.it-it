---
description: Descrive la risoluzione del buffer z dell'ombreggiatura che verrà usata nella simulazione di illuminazione diretta PRT (pre-Computed Radiance Transfer) nella GPU.
ms.assetid: 05354328-9b6f-45f5-a913-47ede170b03f
title: Enumerazione D3DXSHGPUSIMOPT (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHGPUSIMOPT
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: a94845faf4c34657f486cfa371c5d41a12dc4336
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323301"
---
# <a name="d3dxshgpusimopt-enumeration"></a><span data-ttu-id="31d7d-103">Enumerazione D3DXSHGPUSIMOPT</span><span class="sxs-lookup"><span data-stu-id="31d7d-103">D3DXSHGPUSIMOPT enumeration</span></span>

<span data-ttu-id="31d7d-104">Descrive la risoluzione del buffer z dell'ombreggiatura che verrà usata nella simulazione di illuminazione diretta PRT (pre-Computed Radiance Transfer) nella GPU.</span><span class="sxs-lookup"><span data-stu-id="31d7d-104">Describes the resolution of the shadow z-buffer that will be used in Precomputed Radiance Transfer (PRT) direct lighting simulation on the GPU.</span></span> <span data-ttu-id="31d7d-105">È anche possibile specificare un buffer z di qualità superiore per ridurre il rumore nei risultati della simulazione di illuminazione diretta, anche se la simulazione sarà più lenta.</span><span class="sxs-lookup"><span data-stu-id="31d7d-105">A higher quality z-buffer can also be specified to reduce noise in the results of the direct lighting simulation, although the simulation will be slower.</span></span>

## <a name="syntax"></a><span data-ttu-id="31d7d-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="31d7d-106">Syntax</span></span>


```C++
typedef enum D3DXSHGPUSIMOPT { 
  D3DXSHGPUSIMOPT_SHADOWRES256   = 1,
  D3DXSHGPUSIMOPT_SHADOWRES512   = 0,
  D3DXSHGPUSIMOPT_SHADOWRES1024  = 2,
  D3DXSHGPUSIMOPT_SHADOWRES2048  = 3,
  D3DXSHGPUSIMOPT_HIGHQUALITY    = 4,
  D3DXSHGPUSIMOPT_FORCE_DWORD    = 0x7fffffff
} D3DXSHGPUSIMOPT, *LPD3DXSHGPUSIMOPT;
```



## <a name="constants"></a><span data-ttu-id="31d7d-107">Costanti</span><span class="sxs-lookup"><span data-stu-id="31d7d-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="31d7d-108"><span id="D3DXSHGPUSIMOPT_SHADOWRES256"></span><span id="d3dxshgpusimopt_shadowres256"></span>**\_SHADOWRES256 D3DXSHGPUSIMOPT**</span><span class="sxs-lookup"><span data-stu-id="31d7d-108"><span id="D3DXSHGPUSIMOPT_SHADOWRES256"></span><span id="d3dxshgpusimopt_shadowres256"></span>**D3DXSHGPUSIMOPT\_SHADOWRES256**</span></span>
</dt> <dd>

<span data-ttu-id="31d7d-109">Simulazione a bassa risoluzione.</span><span class="sxs-lookup"><span data-stu-id="31d7d-109">Low resolution simulation.</span></span> <span data-ttu-id="31d7d-110">Per codificare il buffer z dell'ombreggiatura viene utilizzata una trama con pixel 256 x 256.</span><span class="sxs-lookup"><span data-stu-id="31d7d-110">A 256 x 256 pixel texture is used in the simulation to encode the shadow z-buffer.</span></span>

</dd> <dt>

<span data-ttu-id="31d7d-111"><span id="D3DXSHGPUSIMOPT_SHADOWRES512"></span><span id="d3dxshgpusimopt_shadowres512"></span>**\_SHADOWRES512 D3DXSHGPUSIMOPT**</span><span class="sxs-lookup"><span data-stu-id="31d7d-111"><span id="D3DXSHGPUSIMOPT_SHADOWRES512"></span><span id="d3dxshgpusimopt_shadowres512"></span>**D3DXSHGPUSIMOPT\_SHADOWRES512**</span></span>
</dt> <dd>

<span data-ttu-id="31d7d-112">Simulazione di media risoluzione.</span><span class="sxs-lookup"><span data-stu-id="31d7d-112">Medium resolution simulation.</span></span> <span data-ttu-id="31d7d-113">Per codificare il buffer z dell'ombreggiatura viene utilizzata una trama con pixel 512 x 512.</span><span class="sxs-lookup"><span data-stu-id="31d7d-113">A 512 x 512 pixel texture is used in the simulation to encode the shadow z-buffer.</span></span> <span data-ttu-id="31d7d-114">Si tratta del valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="31d7d-114">This is the default value.</span></span>

</dd> <dt>

<span data-ttu-id="31d7d-115"><span id="D3DXSHGPUSIMOPT_SHADOWRES1024"></span><span id="d3dxshgpusimopt_shadowres1024"></span>**\_SHADOWRES1024 D3DXSHGPUSIMOPT**</span><span class="sxs-lookup"><span data-stu-id="31d7d-115"><span id="D3DXSHGPUSIMOPT_SHADOWRES1024"></span><span id="d3dxshgpusimopt_shadowres1024"></span>**D3DXSHGPUSIMOPT\_SHADOWRES1024**</span></span>
</dt> <dd>

<span data-ttu-id="31d7d-116">Simulazione ad alta risoluzione.</span><span class="sxs-lookup"><span data-stu-id="31d7d-116">High resolution simulation.</span></span> <span data-ttu-id="31d7d-117">Per codificare il buffer z dell'ombreggiatura viene utilizzata una trama con pixel 1024 x 1024.</span><span class="sxs-lookup"><span data-stu-id="31d7d-117">A 1024 x 1024 pixel texture is used in the simulation to encode the shadow z-buffer.</span></span>

</dd> <dt>

<span data-ttu-id="31d7d-118"><span id="D3DXSHGPUSIMOPT_SHADOWRES2048"></span><span id="d3dxshgpusimopt_shadowres2048"></span>**\_SHADOWRES2048 D3DXSHGPUSIMOPT**</span><span class="sxs-lookup"><span data-stu-id="31d7d-118"><span id="D3DXSHGPUSIMOPT_SHADOWRES2048"></span><span id="d3dxshgpusimopt_shadowres2048"></span>**D3DXSHGPUSIMOPT\_SHADOWRES2048**</span></span>
</dt> <dd>

<span data-ttu-id="31d7d-119">Simulazione con la massima risoluzione.</span><span class="sxs-lookup"><span data-stu-id="31d7d-119">Highest resolution simulation.</span></span> <span data-ttu-id="31d7d-120">Per codificare il buffer z dell'ombreggiatura viene utilizzata una trama con pixel 2048 x 2048.</span><span class="sxs-lookup"><span data-stu-id="31d7d-120">A 2048 x 2048 pixel texture is used in the simulation to encode the shadow z-buffer.</span></span>

</dd> <dt>

<span data-ttu-id="31d7d-121"><span id="D3DXSHGPUSIMOPT_HIGHQUALITY"></span><span id="d3dxshgpusimopt_highquality"></span>**\_Highquality D3DXSHGPUSIMOPT**</span><span class="sxs-lookup"><span data-stu-id="31d7d-121"><span id="D3DXSHGPUSIMOPT_HIGHQUALITY"></span><span id="d3dxshgpusimopt_highquality"></span>**D3DXSHGPUSIMOPT\_HIGHQUALITY**</span></span>
</dt> <dd>

<span data-ttu-id="31d7d-122">La simulazione ha una precisione elevata, indipendentemente dalla risoluzione selezionata.</span><span class="sxs-lookup"><span data-stu-id="31d7d-122">The simulation is of high precision, regardless of the selected resolution.</span></span> <span data-ttu-id="31d7d-123">L'impostazione di questo valore ridurrà il rumore nei risultati della simulazione di illuminazione diretta, anche se la simulazione sarà più lenta.</span><span class="sxs-lookup"><span data-stu-id="31d7d-123">Setting this value will reduce noise in the results of the direct lighting simulation, although the simulation will be slower.</span></span> <span data-ttu-id="31d7d-124">Può essere combinato con uno dei valori di risoluzione.</span><span class="sxs-lookup"><span data-stu-id="31d7d-124">May be combined with one of the resolution values.</span></span>

</dd> <dt>

<span data-ttu-id="31d7d-125"><span id="D3DXSHGPUSIMOPT_FORCE_DWORD"></span><span id="d3dxshgpusimopt_force_dword"></span>**D3DXSHGPUSIMOPT \_ Force \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="31d7d-125"><span id="D3DXSHGPUSIMOPT_FORCE_DWORD"></span><span id="d3dxshgpusimopt_force_dword"></span>**D3DXSHGPUSIMOPT\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="31d7d-126">Impone la compilazione di questa enumerazione a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="31d7d-126">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="31d7d-127">Senza questo valore, alcuni compilatori permetterebbero che questa enumerazione venga compilata in una dimensione diversa da 32 bit.</span><span class="sxs-lookup"><span data-stu-id="31d7d-127">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="31d7d-128">Questo valore non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="31d7d-128">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="31d7d-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="31d7d-129">Remarks</span></span>

<span data-ttu-id="31d7d-130">È possibile specificare solo uno dei valori di risoluzione e può essere combinato con il valore di alta qualità.</span><span class="sxs-lookup"><span data-stu-id="31d7d-130">Only one of the resolution values may be specified, and may be combined with the high-quality value.</span></span>

## <a name="requirements"></a><span data-ttu-id="31d7d-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="31d7d-131">Requirements</span></span>



| <span data-ttu-id="31d7d-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="31d7d-132">Requirement</span></span> | <span data-ttu-id="31d7d-133">Valore</span><span class="sxs-lookup"><span data-stu-id="31d7d-133">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="31d7d-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="31d7d-134">Header</span></span><br/> | <dl> <span data-ttu-id="31d7d-135"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="31d7d-135"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31d7d-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="31d7d-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31d7d-137">Enumerazioni D3DX</span><span class="sxs-lookup"><span data-stu-id="31d7d-137">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




