---
description: Descrive un evento di animazione.
ms.assetid: ddcdd143-bcbd-450c-a4df-914797a562e6
title: Struttura D3DXEVENT_DESC (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXEVENT_DESC
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 32e02e75d3d73569b60c466f45dace2c074a6b3e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322706"
---
# <a name="d3dxevent_desc-structure"></a><span data-ttu-id="bfeea-103">\_Struttura D3DXEVENT DESC</span><span class="sxs-lookup"><span data-stu-id="bfeea-103">D3DXEVENT\_DESC structure</span></span>

<span data-ttu-id="bfeea-104">Descrive un evento di animazione.</span><span class="sxs-lookup"><span data-stu-id="bfeea-104">Describes an animation event.</span></span>

## <a name="syntax"></a><span data-ttu-id="bfeea-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bfeea-105">Syntax</span></span>


```C++
typedef struct D3DXEVENT_DESC {
  D3DXEVENT_TYPE      Type;
  UINT                Track;
  DOUBLE              StartTime;
  DOUBLE              Duration;
  D3DXTRANSITION_TYPE Transition;
  union {
    FLOAT  Weight;
    FLOAT  Speed;
    DOUBLE Position;
    BOOL   Enable;
  };
} D3DXEVENT_DESC, *LPD3DXEVENT_DESC;
```



## <a name="members"></a><span data-ttu-id="bfeea-106">Members</span><span class="sxs-lookup"><span data-stu-id="bfeea-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="bfeea-107">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="bfeea-107">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="bfeea-108">Tipo: **[ **D3DXEVENT \_**](./d3dxevent-type.md)**</span><span class="sxs-lookup"><span data-stu-id="bfeea-108">Type: **[**D3DXEVENT\_TYPE**](./d3dxevent-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="bfeea-109">Tipo di evento, come definito [**nel \_ tipo D3DXEVENT**](./d3dxevent-type.md).</span><span class="sxs-lookup"><span data-stu-id="bfeea-109">Event type, as defined in [**D3DXEVENT\_TYPE**](./d3dxevent-type.md).</span></span>

</dd> <dt>

<span data-ttu-id="bfeea-110">**Track**</span><span class="sxs-lookup"><span data-stu-id="bfeea-110">**Track**</span></span>
</dt> <dd>

<span data-ttu-id="bfeea-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bfeea-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="bfeea-112">Identificatore di traccia eventi.</span><span class="sxs-lookup"><span data-stu-id="bfeea-112">Event track identifier.</span></span>

</dd> <dt>

<span data-ttu-id="bfeea-113">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="bfeea-113">**StartTime**</span></span>
</dt> <dd>

<span data-ttu-id="bfeea-114">Tipo: **[ **Double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bfeea-114">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="bfeea-115">Ora di inizio dell'evento nell'ora globale.</span><span class="sxs-lookup"><span data-stu-id="bfeea-115">Start time of the event in global time.</span></span>

</dd> <dt>

<span data-ttu-id="bfeea-116">**Duration**</span><span class="sxs-lookup"><span data-stu-id="bfeea-116">**Duration**</span></span>
</dt> <dd>

<span data-ttu-id="bfeea-117">Tipo: **[ **Double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bfeea-117">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="bfeea-118">Durata dell'evento nell'ora globale.</span><span class="sxs-lookup"><span data-stu-id="bfeea-118">Duration of the event in global time.</span></span>

</dd> <dt>

<span data-ttu-id="bfeea-119">**Transizione**</span><span class="sxs-lookup"><span data-stu-id="bfeea-119">**Transition**</span></span>
</dt> <dd>

<span data-ttu-id="bfeea-120">Tipo: **[ **D3DXTRANSITION \_**](./d3dxtransition-type.md)**</span><span class="sxs-lookup"><span data-stu-id="bfeea-120">Type: **[**D3DXTRANSITION\_TYPE**](./d3dxtransition-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="bfeea-121">Stile di transizione dell'evento, come definito nel [**\_ tipo D3DXTRANSITION**](./d3dxtransition-type.md).</span><span class="sxs-lookup"><span data-stu-id="bfeea-121">Transition style of the event, as defined in [**D3DXTRANSITION\_TYPE**](./d3dxtransition-type.md).</span></span>

</dd> <dt>

<span data-ttu-id="bfeea-122">**Weight**</span><span class="sxs-lookup"><span data-stu-id="bfeea-122">**Weight**</span></span>
</dt> <dd>

<span data-ttu-id="bfeea-123">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bfeea-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="bfeea-124">Tenere traccia del peso dell'evento.</span><span class="sxs-lookup"><span data-stu-id="bfeea-124">Track weight for the event.</span></span>

</dd> <dt>

<span data-ttu-id="bfeea-125">**Velocità**</span><span class="sxs-lookup"><span data-stu-id="bfeea-125">**Speed**</span></span>
</dt> <dd>

<span data-ttu-id="bfeea-126">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bfeea-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="bfeea-127">Rilevare la velocità per l'evento.</span><span class="sxs-lookup"><span data-stu-id="bfeea-127">Track speed for the event.</span></span>

</dd> <dt>

<span data-ttu-id="bfeea-128">**Position**</span><span class="sxs-lookup"><span data-stu-id="bfeea-128">**Position**</span></span>
</dt> <dd>

<span data-ttu-id="bfeea-129">Tipo: **[ **Double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bfeea-129">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="bfeea-130">Rilevare la posizione per l'evento.</span><span class="sxs-lookup"><span data-stu-id="bfeea-130">Track position for the event.</span></span>

</dd> <dt>

<span data-ttu-id="bfeea-131">**Attiva**</span><span class="sxs-lookup"><span data-stu-id="bfeea-131">**Enable**</span></span>
</dt> <dd>

<span data-ttu-id="bfeea-132">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bfeea-132">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="bfeea-133">Abilita flag.</span><span class="sxs-lookup"><span data-stu-id="bfeea-133">Enable flag.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bfeea-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bfeea-134">Requirements</span></span>



| <span data-ttu-id="bfeea-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="bfeea-135">Requirement</span></span> | <span data-ttu-id="bfeea-136">Valore</span><span class="sxs-lookup"><span data-stu-id="bfeea-136">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bfeea-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bfeea-137">Header</span></span><br/> | <dl> <span data-ttu-id="bfeea-138"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="bfeea-138"><dt>D3dx9anim.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bfeea-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bfeea-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfeea-140">Strutture D3DX</span><span class="sxs-lookup"><span data-stu-id="bfeea-140">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
