---
description: "D3DX10_INTERSECT_INFO struttura : descrive l'intersezione di un triangolo di raggio."
ms.assetid: 21658b74-6f1d-4a16-a8b3-0c7bb6edf899
title: D3DX10_INTERSECT_INFO struttura (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_INTERSECT_INFO
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: 203daa48e766edd545bf232c4f8d94c4f17b5b2a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105459"
---
# <a name="d3dx10_intersect_info-structure"></a><span data-ttu-id="767ef-103">Struttura D3DX10 \_ INTERSECT \_ INFO</span><span class="sxs-lookup"><span data-stu-id="767ef-103">D3DX10\_INTERSECT\_INFO structure</span></span>

<span data-ttu-id="767ef-104">Descrive l'intersezione di un triangolo di raggio.</span><span class="sxs-lookup"><span data-stu-id="767ef-104">Describes a ray-triangle intersection.</span></span>

## <a name="syntax"></a><span data-ttu-id="767ef-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="767ef-105">Syntax</span></span>


```C++
typedef struct D3DX10_INTERSECT_INFO {
  UINT  FaceIndex;
  FLOAT U;
  FLOAT V;
  FLOAT Dist;
} D3DX10_INTERSECT_INFO, *LPD3DX10_INTERSECT_INFO;
```



## <a name="members"></a><span data-ttu-id="767ef-106">Members</span><span class="sxs-lookup"><span data-stu-id="767ef-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="767ef-107">**FaceIndex**</span><span class="sxs-lookup"><span data-stu-id="767ef-107">**FaceIndex**</span></span>
</dt> <dd>

<span data-ttu-id="767ef-108">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="767ef-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="767ef-109">Indice del triangolo che ha raggiunto il raggio.</span><span class="sxs-lookup"><span data-stu-id="767ef-109">Index of the triangle that hit the ray.</span></span>

</dd> <dt>

<span data-ttu-id="767ef-110">**U**</span><span class="sxs-lookup"><span data-stu-id="767ef-110">**U**</span></span>
</dt> <dd>

<span data-ttu-id="767ef-111">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="767ef-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="767ef-112">Coordinata barycentrica all'interno del triangolo in cui si interseca il raggio.</span><span class="sxs-lookup"><span data-stu-id="767ef-112">Barycentric coordinate within the triangle where the ray intersects.</span></span>

</dd> <dt>

<span data-ttu-id="767ef-113">**V**</span><span class="sxs-lookup"><span data-stu-id="767ef-113">**V**</span></span>
</dt> <dd>

<span data-ttu-id="767ef-114">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="767ef-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="767ef-115">Coordinata barycentrica all'interno del triangolo in cui si interseca il raggio.</span><span class="sxs-lookup"><span data-stu-id="767ef-115">Barycentric coordinate within the triangle where the ray intersects.</span></span>

</dd> <dt>

<span data-ttu-id="767ef-116">**Dist**</span><span class="sxs-lookup"><span data-stu-id="767ef-116">**Dist**</span></span>
</dt> <dd>

<span data-ttu-id="767ef-117">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="767ef-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="767ef-118">Distanza lungo il raggio in cui si è verificata l'intersezione.</span><span class="sxs-lookup"><span data-stu-id="767ef-118">Distance along the ray where the intersection occurred.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="767ef-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="767ef-119">Remarks</span></span>

<span data-ttu-id="767ef-120">Le coordinate barycentriche definiscono un punto all'interno di un triangolo in termini di vertici del triangolo.</span><span class="sxs-lookup"><span data-stu-id="767ef-120">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="767ef-121">Per una descrizione più dettagliata delle coordinate barycentric, vedere Descrizione delle [coordinate barycentriche di Mathworld.](https://mathworld.wolfram.com/BarycentricCoordinates.html)</span><span class="sxs-lookup"><span data-stu-id="767ef-121">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="767ef-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="767ef-122">Requirements</span></span>



| <span data-ttu-id="767ef-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="767ef-123">Requirement</span></span> | <span data-ttu-id="767ef-124">Valore</span><span class="sxs-lookup"><span data-stu-id="767ef-124">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="767ef-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="767ef-125">Header</span></span><br/> | <dl> <span data-ttu-id="767ef-126"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="767ef-126"><dt>D3DX10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="767ef-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="767ef-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="767ef-128">Strutture D3DX</span><span class="sxs-lookup"><span data-stu-id="767ef-128">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
