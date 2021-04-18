---
description: Questa struttura contiene i dati per la segnalazione di utilizzo intensivo della memoria.
ms.assetid: 42cf0922-53cc-48b9-8359-b88583ef5f1c
title: Struttura D3DMEMORYPRESSURE (D3d9types. h) per Microsoft Media Foundation
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
ms.openlocfilehash: 7400c4822b61a84ab288f0424cfa84e825e69dc9
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/02/2021
ms.locfileid: "106334396"
---
# <a name="d3dmemorypressure-structure-d3d9typesh-for-microsoft-media-foundation"></a><span data-ttu-id="76192-103">Struttura D3DMEMORYPRESSURE (D3d9types. h) per Microsoft Media Foundation</span><span class="sxs-lookup"><span data-stu-id="76192-103">D3DMEMORYPRESSURE structure (D3d9types.h) for Microsoft Media Foundation</span></span>

<span data-ttu-id="76192-104">Contiene i dati per la segnalazione di richieste di memoria.</span><span class="sxs-lookup"><span data-stu-id="76192-104">Contains data for memory pressure reporting.</span></span>

## <a name="syntax"></a><span data-ttu-id="76192-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="76192-105">Syntax</span></span>


```C++
typedef struct _D3DMEMORYPRESSURE {
  UINT64 BytesEvictedFromProcess;
  UINT64 SizeOfInefficientAllocation;
  DWORD  LevelOfEfficiency;
} D3DMEMORYPRESSURE;
```



## <a name="members"></a><span data-ttu-id="76192-106">Members</span><span class="sxs-lookup"><span data-stu-id="76192-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="76192-107">**BytesEvictedFromProcess**</span><span class="sxs-lookup"><span data-stu-id="76192-107">**BytesEvictedFromProcess**</span></span>
</dt> <dd>

<span data-ttu-id="76192-108">Numero di byte rimossi dal processo durante la durata della query.</span><span class="sxs-lookup"><span data-stu-id="76192-108">The number of bytes that were evicted by the process during the duration of the query.</span></span>

</dd> <dt>

<span data-ttu-id="76192-109">**SizeOfInefficientAllocation**</span><span class="sxs-lookup"><span data-stu-id="76192-109">**SizeOfInefficientAllocation**</span></span>
</dt> <dd>

<span data-ttu-id="76192-110">Numero totale di byte posizionati in segmenti di memoria non ottimali a causa di uno spazio inadeguato nei segmenti di memoria preferiti.</span><span class="sxs-lookup"><span data-stu-id="76192-110">The total number of bytes placed in nonoptimal memory segments, due to inadequate space within the preferred memory segments.</span></span>

</dd> <dt>

<span data-ttu-id="76192-111">**LevelOfEfficiency**</span><span class="sxs-lookup"><span data-stu-id="76192-111">**LevelOfEfficiency**</span></span>
</dt> <dd>

<span data-ttu-id="76192-112">Efficienza complessiva delle allocazioni di memoria posizionate nella memoria non ottimale.</span><span class="sxs-lookup"><span data-stu-id="76192-112">The overall efficiency of the memory allocations that were placed in nonoptimal memory.</span></span> <span data-ttu-id="76192-113">Il valore è espresso come percentuale.</span><span class="sxs-lookup"><span data-stu-id="76192-113">The value is expressed as a percentage.</span></span> <span data-ttu-id="76192-114">Ad esempio, il valore 95 indica che le allocazioni posizionate nei segmenti di memoria non preferiti sono efficienti al 95%.</span><span class="sxs-lookup"><span data-stu-id="76192-114">For example, the value 95 indicates that the allocations placed in nonpreferred memory segments are 95% efficient.</span></span> <span data-ttu-id="76192-115">Questo numero non deve essere considerato una misura esatta.</span><span class="sxs-lookup"><span data-stu-id="76192-115">This number should not be considered an exact measurement.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="76192-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="76192-116">Requirements</span></span>



| <span data-ttu-id="76192-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="76192-117">Requirement</span></span> | <span data-ttu-id="76192-118">Valore</span><span class="sxs-lookup"><span data-stu-id="76192-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76192-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="76192-119">Minimum supported client</span></span> | <span data-ttu-id="76192-120">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="76192-120">Windows 7 \[desktop apps only\]</span></span>                                                              |
| <span data-ttu-id="76192-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="76192-121">Minimum supported server</span></span> | <span data-ttu-id="76192-122">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="76192-122">Windows Server 2008 R2 \[desktop apps only\]</span></span>                                                 |
| <span data-ttu-id="76192-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="76192-123">Header</span></span>                  | <span data-ttu-id="76192-124">D3d9types. h (include d3d9. h)</span><span class="sxs-lookup"><span data-stu-id="76192-124">D3d9types.h (include D3d9.h)</span></span> |



## <a name="see-also"></a><span data-ttu-id="76192-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="76192-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76192-126">Strutture video Direct3D</span><span class="sxs-lookup"><span data-stu-id="76192-126">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="76192-127">Segnalazione di utilizzo intensivo della memoria</span><span class="sxs-lookup"><span data-stu-id="76192-127">Memory Pressure Reporting</span></span>](memory-pressure-reporting.md)
</dt> </dl>

 

 




