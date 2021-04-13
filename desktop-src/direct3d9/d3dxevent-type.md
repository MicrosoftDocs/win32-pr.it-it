---
description: Descrive il tipo di eventi che possono essere codificati dal controller animazione.
ms.assetid: d98b398e-29e1-41b5-84eb-37983bac8d0a
title: Enumerazione D3DXEVENT_TYPE (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXEVENT_TYPE
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 97219478b898dc47e385e8e00a5cc9b5484730ce
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354879"
---
# <a name="d3dxevent_type-enumeration"></a><span data-ttu-id="48392-103">\_Enumerazione del tipo D3DXEVENT</span><span class="sxs-lookup"><span data-stu-id="48392-103">D3DXEVENT\_TYPE enumeration</span></span>

<span data-ttu-id="48392-104">Descrive il tipo di eventi che possono essere codificati dal controller animazione.</span><span class="sxs-lookup"><span data-stu-id="48392-104">Describes the type of events that can be keyed by the animation controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="48392-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="48392-105">Syntax</span></span>


```C++
typedef enum D3DXEVENT_TYPE { 
  D3DXEVENT_TRACKSPEED     = 0,
  D3DXEVENT_TRACKWEIGHT    = 1,
  D3DXEVENT_TRACKPOSITION  = 2,
  D3DXEVENT_TRACKENABLE    = 3,
  D3DXEVENT_PRIORITYBLEND  = 4,
  D3DXEVENT_FORCE_DWORD    = 0x7fffffff
} D3DXEVENT_TYPE, *LPD3DXEVENT_TYPE;
```



## <a name="constants"></a><span data-ttu-id="48392-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="48392-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="48392-107"><span id="D3DXEVENT_TRACKSPEED"></span><span id="d3dxevent_trackspeed"></span>**\_TRACKSPEED D3DXEVENT**</span><span class="sxs-lookup"><span data-stu-id="48392-107"><span id="D3DXEVENT_TRACKSPEED"></span><span id="d3dxevent_trackspeed"></span>**D3DXEVENT\_TRACKSPEED**</span></span>
</dt> <dd>

<span data-ttu-id="48392-108">Rileva velocità.</span><span class="sxs-lookup"><span data-stu-id="48392-108">Track speed.</span></span>

</dd> <dt>

<span data-ttu-id="48392-109"><span id="D3DXEVENT_TRACKWEIGHT"></span><span id="d3dxevent_trackweight"></span>**\_TRACKWEIGHT D3DXEVENT**</span><span class="sxs-lookup"><span data-stu-id="48392-109"><span id="D3DXEVENT_TRACKWEIGHT"></span><span id="d3dxevent_trackweight"></span>**D3DXEVENT\_TRACKWEIGHT**</span></span>
</dt> <dd>

<span data-ttu-id="48392-110">Tenere traccia del peso.</span><span class="sxs-lookup"><span data-stu-id="48392-110">Track weight.</span></span>

</dd> <dt>

<span data-ttu-id="48392-111"><span id="D3DXEVENT_TRACKPOSITION"></span><span id="d3dxevent_trackposition"></span>**\_TRACKPOSITION D3DXEVENT**</span><span class="sxs-lookup"><span data-stu-id="48392-111"><span id="D3DXEVENT_TRACKPOSITION"></span><span id="d3dxevent_trackposition"></span>**D3DXEVENT\_TRACKPOSITION**</span></span>
</dt> <dd>

<span data-ttu-id="48392-112">Rilevare la posizione.</span><span class="sxs-lookup"><span data-stu-id="48392-112">Track position.</span></span>

</dd> <dt>

<span data-ttu-id="48392-113"><span id="D3DXEVENT_TRACKENABLE"></span><span id="d3dxevent_trackenable"></span>**\_TRACKENABLE D3DXEVENT**</span><span class="sxs-lookup"><span data-stu-id="48392-113"><span id="D3DXEVENT_TRACKENABLE"></span><span id="d3dxevent_trackenable"></span>**D3DXEVENT\_TRACKENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="48392-114">Abilita flag.</span><span class="sxs-lookup"><span data-stu-id="48392-114">Enable flag.</span></span>

</dd> <dt>

<span data-ttu-id="48392-115"><span id="D3DXEVENT_PRIORITYBLEND"></span><span id="d3dxevent_priorityblend"></span>**\_PRIORITYBLEND D3DXEVENT**</span><span class="sxs-lookup"><span data-stu-id="48392-115"><span id="D3DXEVENT_PRIORITYBLEND"></span><span id="d3dxevent_priorityblend"></span>**D3DXEVENT\_PRIORITYBLEND**</span></span>
</dt> <dd>

<span data-ttu-id="48392-116">Valore di Blend di priorità.</span><span class="sxs-lookup"><span data-stu-id="48392-116">Priority blend value.</span></span>

</dd> <dt>

<span data-ttu-id="48392-117"><span id="D3DXEVENT_FORCE_DWORD"></span><span id="d3dxevent_force_dword"></span>**D3DXEVENT \_ Force \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="48392-117"><span id="D3DXEVENT_FORCE_DWORD"></span><span id="d3dxevent_force_dword"></span>**D3DXEVENT\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="48392-118">Impone la compilazione di questa enumerazione a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="48392-118">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="48392-119">Senza questo valore, alcuni compilatori permetterebbero che questa enumerazione venga compilata in una dimensione diversa da 32 bit.</span><span class="sxs-lookup"><span data-stu-id="48392-119">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="48392-120">Questo valore non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="48392-120">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="48392-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="48392-121">Requirements</span></span>



| <span data-ttu-id="48392-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="48392-122">Requirement</span></span> | <span data-ttu-id="48392-123">Valore</span><span class="sxs-lookup"><span data-stu-id="48392-123">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="48392-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="48392-124">Header</span></span><br/> | <dl> <span data-ttu-id="48392-125"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="48392-125"><dt>D3dx9anim.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48392-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="48392-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48392-127">Enumerazioni D3DX</span><span class="sxs-lookup"><span data-stu-id="48392-127">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




