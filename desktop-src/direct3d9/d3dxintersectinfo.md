---
description: Descrive un'intersezione tra i triangoli.
ms.assetid: b6f50fc0-2c8a-4efa-a144-bd0851f8b0ca
title: Struttura D3DXINTERSECTINFO (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXINTERSECTINFO
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 31a98e9a7095e81e962b2996dedb9bdf5871533d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322647"
---
# <a name="d3dxintersectinfo-structure"></a><span data-ttu-id="588f1-103">Struttura D3DXINTERSECTINFO</span><span class="sxs-lookup"><span data-stu-id="588f1-103">D3DXINTERSECTINFO structure</span></span>

<span data-ttu-id="588f1-104">Descrive un'intersezione tra i triangoli.</span><span class="sxs-lookup"><span data-stu-id="588f1-104">Describes a ray-triangle intersection.</span></span>

## <a name="syntax"></a><span data-ttu-id="588f1-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="588f1-105">Syntax</span></span>


```C++
typedef struct D3DXINTERSECTINFO {
  DWORD FaceIndex;
  FLOAT U;
  FLOAT V;
  FLOAT Dist;
} D3DXINTERSECTINFO, *LPD3DXINTERSECTINFO;
```



## <a name="members"></a><span data-ttu-id="588f1-106">Members</span><span class="sxs-lookup"><span data-stu-id="588f1-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="588f1-107">**FaceIndex**</span><span class="sxs-lookup"><span data-stu-id="588f1-107">**FaceIndex**</span></span>
</dt> <dd>

<span data-ttu-id="588f1-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="588f1-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="588f1-109">Indice del triangolo che raggiunge il raggio.</span><span class="sxs-lookup"><span data-stu-id="588f1-109">Index of the triangle that hit the ray.</span></span>

</dd> <dt>

<span data-ttu-id="588f1-110">**U**</span><span class="sxs-lookup"><span data-stu-id="588f1-110">**U**</span></span>
</dt> <dd>

<span data-ttu-id="588f1-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="588f1-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="588f1-112">Coordinata baricentrica all'interno del triangolo in cui si interseca il raggio.</span><span class="sxs-lookup"><span data-stu-id="588f1-112">Barycentric coordinate within the triangle where the ray intersects.</span></span>

</dd> <dt>

<span data-ttu-id="588f1-113">**V**</span><span class="sxs-lookup"><span data-stu-id="588f1-113">**V**</span></span>
</dt> <dd>

<span data-ttu-id="588f1-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="588f1-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="588f1-115">Coordinata baricentrica all'interno del triangolo in cui si interseca il raggio.</span><span class="sxs-lookup"><span data-stu-id="588f1-115">Barycentric coordinate within the triangle where the ray intersects.</span></span>

</dd> <dt>

<span data-ttu-id="588f1-116">**Dist**</span><span class="sxs-lookup"><span data-stu-id="588f1-116">**Dist**</span></span>
</dt> <dd>

<span data-ttu-id="588f1-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="588f1-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="588f1-118">Distanza lungo il raggio in cui si è verificata l'intersezione.</span><span class="sxs-lookup"><span data-stu-id="588f1-118">Distance along the ray where the intersection occurred.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="588f1-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="588f1-119">Remarks</span></span>

<span data-ttu-id="588f1-120">Le coordinate baricentrica definiscono un punto all'interno di un triangolo in termini di vertici del triangolo.</span><span class="sxs-lookup"><span data-stu-id="588f1-120">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="588f1-121">Per una descrizione più approfondita delle coordinate baricentrica, vedere [la descrizione delle coordinate baricentrica di articolo MathWorld](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span><span class="sxs-lookup"><span data-stu-id="588f1-121">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="588f1-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="588f1-122">Requirements</span></span>



| <span data-ttu-id="588f1-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="588f1-123">Requirement</span></span> | <span data-ttu-id="588f1-124">Valore</span><span class="sxs-lookup"><span data-stu-id="588f1-124">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="588f1-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="588f1-125">Header</span></span><br/> | <dl> <span data-ttu-id="588f1-126"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="588f1-126"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="588f1-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="588f1-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="588f1-128">Strutture D3DX</span><span class="sxs-lookup"><span data-stu-id="588f1-128">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
