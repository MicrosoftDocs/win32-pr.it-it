---
description: Contiene i dati per la segnalazione di richieste di memoria.
ms.assetid: bdf65d35-281f-4795-a2c1-0d4e91bfa7bc
title: Struttura D3DMEMORYPRESSURE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DMEMORYPRESSURE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 5917d1e61817f401106ae14aa5a0f98cd75b0d42
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322925"
---
# <a name="d3dmemorypressure-structure-d3d9typesh"></a><span data-ttu-id="670fc-103">Struttura D3DMEMORYPRESSURE (D3d9types. h)</span><span class="sxs-lookup"><span data-stu-id="670fc-103">D3DMEMORYPRESSURE structure (D3d9types.h)</span></span>

<span data-ttu-id="670fc-104">Contiene i dati per la segnalazione di richieste di memoria.</span><span class="sxs-lookup"><span data-stu-id="670fc-104">Contains data for memory pressure reporting.</span></span>

## <a name="syntax"></a><span data-ttu-id="670fc-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="670fc-105">Syntax</span></span>


```C++
typedef struct _D3DMEMORYPRESSURE {
  UINT64 BytesEvictedFromProcess;
  UINT64 SizeOfInefficientAllocation;
  DWORD  LevelOfEfficiency;
} D3DMEMORYPRESSURE;
```



## <a name="members"></a><span data-ttu-id="670fc-106">Members</span><span class="sxs-lookup"><span data-stu-id="670fc-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="670fc-107">**BytesEvictedFromProcess**</span><span class="sxs-lookup"><span data-stu-id="670fc-107">**BytesEvictedFromProcess**</span></span>
</dt> <dd>

<span data-ttu-id="670fc-108">Tipo: **[ **UInt64**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="670fc-108">Type: **[**UINT64**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="670fc-109">Numero di byte rimossi dal processo durante la durata della query.</span><span class="sxs-lookup"><span data-stu-id="670fc-109">The number of bytes that were evicted by the process during the duration of the query.</span></span>

</dd> <dt>

<span data-ttu-id="670fc-110">**SizeOfInefficientAllocation**</span><span class="sxs-lookup"><span data-stu-id="670fc-110">**SizeOfInefficientAllocation**</span></span>
</dt> <dd>

<span data-ttu-id="670fc-111">Tipo: **[ **UInt64**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="670fc-111">Type: **[**UINT64**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="670fc-112">Numero totale di byte posizionati in segmenti di memoria non ottimali a causa di uno spazio inadeguato nei segmenti di memoria preferiti.</span><span class="sxs-lookup"><span data-stu-id="670fc-112">The total number of bytes placed in nonoptimal memory segments, due to inadequate space within the preferred memory segments.</span></span>

</dd> <dt>

<span data-ttu-id="670fc-113">**LevelOfEfficiency**</span><span class="sxs-lookup"><span data-stu-id="670fc-113">**LevelOfEfficiency**</span></span>
</dt> <dd>

<span data-ttu-id="670fc-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="670fc-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="670fc-115">Efficienza complessiva delle allocazioni di memoria posizionate nella memoria non ottimale.</span><span class="sxs-lookup"><span data-stu-id="670fc-115">The overall efficiency of the memory allocations that were placed in nonoptimal memory.</span></span> <span data-ttu-id="670fc-116">Il valore è espresso come percentuale.</span><span class="sxs-lookup"><span data-stu-id="670fc-116">The value is expressed as a percentage.</span></span> <span data-ttu-id="670fc-117">Ad esempio, il valore 95 indica che le allocazioni posizionate nei segmenti di memoria non preferiti sono efficienti al 95%.</span><span class="sxs-lookup"><span data-stu-id="670fc-117">For example, the value 95 indicates that the allocations placed in nonpreferred memory segments are 95% efficient.</span></span> <span data-ttu-id="670fc-118">Questo numero non deve essere considerato una misura esatta.</span><span class="sxs-lookup"><span data-stu-id="670fc-118">This number should not be considered an exact measurement.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="670fc-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="670fc-119">Requirements</span></span>



| <span data-ttu-id="670fc-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="670fc-120">Requirement</span></span> | <span data-ttu-id="670fc-121">Valore</span><span class="sxs-lookup"><span data-stu-id="670fc-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="670fc-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="670fc-122">Header</span></span><br/> | <dl> <span data-ttu-id="670fc-123"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="670fc-123"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="670fc-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="670fc-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="670fc-125">Strutture Direct3D</span><span class="sxs-lookup"><span data-stu-id="670fc-125">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
