---
description: Descrive una traccia di animazione e specifica il peso, la velocità e la posizione della traccia in un determinato momento.
ms.assetid: f1469b6f-861f-4b7d-a187-933092a5d257
title: Struttura D3DXTRACK_DESC (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTRACK_DESC
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 12f1604cf954bcdd6a2a898fec5410804112e498
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322574"
---
# <a name="d3dxtrack_desc-structure"></a><span data-ttu-id="b81e1-103">\_Struttura D3DXTRACK DESC</span><span class="sxs-lookup"><span data-stu-id="b81e1-103">D3DXTRACK\_DESC structure</span></span>

<span data-ttu-id="b81e1-104">Descrive una traccia di animazione e specifica il peso, la velocità e la posizione della traccia in un determinato momento.</span><span class="sxs-lookup"><span data-stu-id="b81e1-104">Describes an animation track and specifies blending weight, speed, and position for the track at a given time.</span></span>

## <a name="syntax"></a><span data-ttu-id="b81e1-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b81e1-105">Syntax</span></span>


```C++
typedef struct D3DXTRACK_DESC {
  D3DXPRIORITY_TYPE Priority;
  FLOAT             Weight;
  FLOAT             Speed;
  DOUBLE            Position;
  BOOL              Enable;
} D3DXTRACK_DESC, *LPD3DXTRACK_DESC;
```



## <a name="members"></a><span data-ttu-id="b81e1-106">Members</span><span class="sxs-lookup"><span data-stu-id="b81e1-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="b81e1-107">**Priorità**</span><span class="sxs-lookup"><span data-stu-id="b81e1-107">**Priority**</span></span>
</dt> <dd>

<span data-ttu-id="b81e1-108">Tipo: **[ **D3DXPRIORITY \_**](./d3dxpriority-type.md)**</span><span class="sxs-lookup"><span data-stu-id="b81e1-108">Type: **[**D3DXPRIORITY\_TYPE**](./d3dxpriority-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b81e1-109">Tipo di priorità, come definito [**nel \_ tipo D3DXPRIORITY**](./d3dxpriority-type.md).</span><span class="sxs-lookup"><span data-stu-id="b81e1-109">Priority type, as defined in [**D3DXPRIORITY\_TYPE**](./d3dxpriority-type.md).</span></span>

</dd> <dt>

<span data-ttu-id="b81e1-110">**Weight**</span><span class="sxs-lookup"><span data-stu-id="b81e1-110">**Weight**</span></span>
</dt> <dd>

<span data-ttu-id="b81e1-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b81e1-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b81e1-112">Valore del peso.</span><span class="sxs-lookup"><span data-stu-id="b81e1-112">Weight value.</span></span> <span data-ttu-id="b81e1-113">Il peso determina la percentuale di questa traccia da unire con altre tracce.</span><span class="sxs-lookup"><span data-stu-id="b81e1-113">The weight determines the proportion of this track to blend with other tracks.</span></span>

</dd> <dt>

<span data-ttu-id="b81e1-114">**Velocità**</span><span class="sxs-lookup"><span data-stu-id="b81e1-114">**Speed**</span></span>
</dt> <dd>

<span data-ttu-id="b81e1-115">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b81e1-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b81e1-116">Valore della velocità.</span><span class="sxs-lookup"><span data-stu-id="b81e1-116">Speed value.</span></span> <span data-ttu-id="b81e1-117">Viene usato in modo analogo a un moltiplicatore per ridimensionare il periodo della traccia.</span><span class="sxs-lookup"><span data-stu-id="b81e1-117">This is used similarly to a multiplier to scale the period of the track.</span></span>

</dd> <dt>

<span data-ttu-id="b81e1-118">**Position**</span><span class="sxs-lookup"><span data-stu-id="b81e1-118">**Position**</span></span>
</dt> <dd>

<span data-ttu-id="b81e1-119">Tipo: **[ **Double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b81e1-119">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b81e1-120">Posizione temporale della traccia nell'intervallo di tempo locale del set di animazioni corrente.</span><span class="sxs-lookup"><span data-stu-id="b81e1-120">Time position of the track, in the local timeframe of its current animation set.</span></span>

</dd> <dt>

<span data-ttu-id="b81e1-121">**Attiva**</span><span class="sxs-lookup"><span data-stu-id="b81e1-121">**Enable**</span></span>
</dt> <dd>

<span data-ttu-id="b81e1-122">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b81e1-122">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b81e1-123">Tenere traccia dell'abilitazione o disabilitazione.</span><span class="sxs-lookup"><span data-stu-id="b81e1-123">Track enable/disable.</span></span> <span data-ttu-id="b81e1-124">Per abilitare, impostare su **true**.</span><span class="sxs-lookup"><span data-stu-id="b81e1-124">To enable, set to **TRUE**.</span></span> <span data-ttu-id="b81e1-125">Per disabilitare, impostare su **false**.</span><span class="sxs-lookup"><span data-stu-id="b81e1-125">To disable, set to **FALSE**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b81e1-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="b81e1-126">Remarks</span></span>

<span data-ttu-id="b81e1-127">Le tracce con la stessa priorità vengono combinate insieme e i due valori risultanti vengono combinati utilizzando il fattore di sfumatura della priorità.</span><span class="sxs-lookup"><span data-stu-id="b81e1-127">Tracks with the same priority are blended together, and the two resulting values are then blended using the priority blend factor.</span></span> <span data-ttu-id="b81e1-128">A una traccia deve essere associato un set di animazioni (archiviato separatamente).</span><span class="sxs-lookup"><span data-stu-id="b81e1-128">A track must have an animation set (stored separately) associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="b81e1-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b81e1-129">Requirements</span></span>



| <span data-ttu-id="b81e1-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="b81e1-130">Requirement</span></span> | <span data-ttu-id="b81e1-131">Valore</span><span class="sxs-lookup"><span data-stu-id="b81e1-131">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b81e1-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b81e1-132">Header</span></span><br/> | <dl> <span data-ttu-id="b81e1-133"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="b81e1-133"><dt>D3dx9anim.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b81e1-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b81e1-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b81e1-135">Strutture D3DX</span><span class="sxs-lookup"><span data-stu-id="b81e1-135">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
