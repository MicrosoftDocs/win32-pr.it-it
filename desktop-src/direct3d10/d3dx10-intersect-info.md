---
description: Descrive un'intersezione tra i triangoli.
ms.assetid: 21658b74-6f1d-4a16-a8b3-0c7bb6edf899
title: Struttura D3DX10_INTERSECT_INFO (D3DX10. h)
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
ms.openlocfilehash: 87490e734299cba57952bb43d1ee4ffad8e014c8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762113"
---
# <a name="d3dx10_intersect_info-structure"></a><span data-ttu-id="cc249-103">\_ \_ Struttura info Intersect d3dx10</span><span class="sxs-lookup"><span data-stu-id="cc249-103">D3DX10\_INTERSECT\_INFO structure</span></span>

<span data-ttu-id="cc249-104">Descrive un'intersezione tra i triangoli.</span><span class="sxs-lookup"><span data-stu-id="cc249-104">Describes a ray-triangle intersection.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc249-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cc249-105">Syntax</span></span>


```C++
typedef struct D3DX10_INTERSECT_INFO {
  UINT  FaceIndex;
  FLOAT U;
  FLOAT V;
  FLOAT Dist;
} D3DX10_INTERSECT_INFO, *LPD3DX10_INTERSECT_INFO;
```



## <a name="members"></a><span data-ttu-id="cc249-106">Members</span><span class="sxs-lookup"><span data-stu-id="cc249-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="cc249-107">**FaceIndex**</span><span class="sxs-lookup"><span data-stu-id="cc249-107">**FaceIndex**</span></span>
</dt> <dd>

<span data-ttu-id="cc249-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cc249-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="cc249-109">Indice del triangolo che raggiunge il raggio.</span><span class="sxs-lookup"><span data-stu-id="cc249-109">Index of the triangle that hit the ray.</span></span>

</dd> <dt>

<span data-ttu-id="cc249-110">**U**</span><span class="sxs-lookup"><span data-stu-id="cc249-110">**U**</span></span>
</dt> <dd>

<span data-ttu-id="cc249-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cc249-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="cc249-112">Coordinata baricentrica all'interno del triangolo in cui si interseca il raggio.</span><span class="sxs-lookup"><span data-stu-id="cc249-112">Barycentric coordinate within the triangle where the ray intersects.</span></span>

</dd> <dt>

<span data-ttu-id="cc249-113">**V**</span><span class="sxs-lookup"><span data-stu-id="cc249-113">**V**</span></span>
</dt> <dd>

<span data-ttu-id="cc249-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cc249-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="cc249-115">Coordinata baricentrica all'interno del triangolo in cui si interseca il raggio.</span><span class="sxs-lookup"><span data-stu-id="cc249-115">Barycentric coordinate within the triangle where the ray intersects.</span></span>

</dd> <dt>

<span data-ttu-id="cc249-116">**Dist**</span><span class="sxs-lookup"><span data-stu-id="cc249-116">**Dist**</span></span>
</dt> <dd>

<span data-ttu-id="cc249-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cc249-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="cc249-118">Distanza lungo il raggio in cui si è verificata l'intersezione.</span><span class="sxs-lookup"><span data-stu-id="cc249-118">Distance along the ray where the intersection occurred.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cc249-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="cc249-119">Remarks</span></span>

<span data-ttu-id="cc249-120">Le coordinate baricentrica definiscono un punto all'interno di un triangolo in termini di vertici del triangolo.</span><span class="sxs-lookup"><span data-stu-id="cc249-120">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="cc249-121">Per una descrizione più approfondita delle coordinate baricentrica, vedere [la descrizione delle coordinate baricentrica di articolo MathWorld](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span><span class="sxs-lookup"><span data-stu-id="cc249-121">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="cc249-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cc249-122">Requirements</span></span>



| <span data-ttu-id="cc249-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc249-123">Requirement</span></span> | <span data-ttu-id="cc249-124">Valore</span><span class="sxs-lookup"><span data-stu-id="cc249-124">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="cc249-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cc249-125">Header</span></span><br/> | <dl> <span data-ttu-id="cc249-126"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc249-126"><dt>D3DX10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc249-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cc249-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc249-128">Strutture D3DX</span><span class="sxs-lookup"><span data-stu-id="cc249-128">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
