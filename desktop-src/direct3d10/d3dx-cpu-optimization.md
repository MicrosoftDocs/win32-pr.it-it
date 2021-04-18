---
description: Specifica il set di istruzioni D3DX attualmente ottimizzato per.
ms.assetid: 5fc97028-4a9d-4bc7-9c90-236a70e570e1
title: Enumerazione D3DX_CPU_OPTIMIZATION (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX_CPU_OPTIMIZATION
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 208422604e79b3ef7a87b548e7d71eceedd9fb78
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322386"
---
# <a name="d3dx_cpu_optimization-enumeration"></a><span data-ttu-id="5f293-103">\_ \_ Enumerazione ottimizzazione CPU D3DX</span><span class="sxs-lookup"><span data-stu-id="5f293-103">D3DX\_CPU\_OPTIMIZATION enumeration</span></span>

<span data-ttu-id="5f293-104">Specifica il set di istruzioni D3DX attualmente ottimizzato per.</span><span class="sxs-lookup"><span data-stu-id="5f293-104">Specifies the instruction set D3DX is currently optimized for.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f293-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5f293-105">Syntax</span></span>


```C++
typedef enum _D3DX_CPU_OPTIMIZATION { 
  D3DX_NOT_OPTIMIZED    = 0,
  D3DX_3DNOW_OPTIMIZED  = 1,
  D3DX_SSE2_OPTIMIZED   = 2,
  D3DX_SSE_OPTIMIZED    = 3
} D3DX_CPU_OPTIMIZATION;
```



## <a name="constants"></a><span data-ttu-id="5f293-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="5f293-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="5f293-107"><span id="D3DX_NOT_OPTIMIZED"></span><span id="d3dx_not_optimized"></span>**D3DX \_ non \_ ottimizzato**</span><span class="sxs-lookup"><span data-stu-id="5f293-107"><span id="D3DX_NOT_OPTIMIZED"></span><span id="d3dx_not_optimized"></span>**D3DX\_NOT\_OPTIMIZED**</span></span>
</dt> <dd>

<span data-ttu-id="5f293-108">Non ottimizzare.</span><span class="sxs-lookup"><span data-stu-id="5f293-108">Do not optimize.</span></span>

</dd> <dt>

<span data-ttu-id="5f293-109"><span id="D3DX_3DNOW_OPTIMIZED"></span><span id="d3dx_3dnow_optimized"></span>**D3DX \_ 3DNOW \_ ottimizzato**</span><span class="sxs-lookup"><span data-stu-id="5f293-109"><span id="D3DX_3DNOW_OPTIMIZED"></span><span id="d3dx_3dnow_optimized"></span>**D3DX\_3DNOW\_OPTIMIZED**</span></span>
</dt> <dd>

<span data-ttu-id="5f293-110">Ottimizza per un 3DNow!</span><span class="sxs-lookup"><span data-stu-id="5f293-110">Optimize for a 3DNow!</span></span> <span data-ttu-id="5f293-111">set di istruzioni.</span><span class="sxs-lookup"><span data-stu-id="5f293-111">instruction set.</span></span>

</dd> <dt>

<span data-ttu-id="5f293-112"><span id="D3DX_SSE2_OPTIMIZED"></span><span id="d3dx_sse2_optimized"></span>**D3DX \_ SSE2 \_ ottimizzato**</span><span class="sxs-lookup"><span data-stu-id="5f293-112"><span id="D3DX_SSE2_OPTIMIZED"></span><span id="d3dx_sse2_optimized"></span>**D3DX\_SSE2\_OPTIMIZED**</span></span>
</dt> <dd>

<span data-ttu-id="5f293-113">Ottimizza per un set di istruzioni SSE2.</span><span class="sxs-lookup"><span data-stu-id="5f293-113">Optimize for an SSE2 instruction set.</span></span>

</dd> <dt>

<span data-ttu-id="5f293-114"><span id="D3DX_SSE_OPTIMIZED"></span><span id="d3dx_sse_optimized"></span>**D3DX \_ SSE \_ ottimizzato**</span><span class="sxs-lookup"><span data-stu-id="5f293-114"><span id="D3DX_SSE_OPTIMIZED"></span><span id="d3dx_sse_optimized"></span>**D3DX\_SSE\_OPTIMIZED**</span></span>
</dt> <dd>

<span data-ttu-id="5f293-115">Ottimizza per un set di istruzioni SSE.</span><span class="sxs-lookup"><span data-stu-id="5f293-115">Optimize for an SSE instruction set.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5f293-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5f293-116">Requirements</span></span>



| <span data-ttu-id="5f293-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f293-117">Requirement</span></span> | <span data-ttu-id="5f293-118">Valore</span><span class="sxs-lookup"><span data-stu-id="5f293-118">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5f293-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5f293-119">Header</span></span><br/> | <dl> <span data-ttu-id="5f293-120"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f293-120"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f293-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5f293-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f293-122">Enumerazioni D3DX</span><span class="sxs-lookup"><span data-stu-id="5f293-122">D3DX Enumerations</span></span>](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




