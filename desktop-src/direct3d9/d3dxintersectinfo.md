---
description: "Struttura D3DXINTERSECTINFO: descrive un'intersezione di un triangolo a raggi."
ms.assetid: b6f50fc0-2c8a-4efa-a144-bd0851f8b0ca
title: Struttura D3DXINTERSECTINFO (D3dx9mesh.h)
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
ms.openlocfilehash: f4a63c7f4a479bfbe9dcb49f485ce0acb8db6486
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098289"
---
# <a name="d3dxintersectinfo-structure"></a><span data-ttu-id="2c82d-103">Struttura D3DXINTERSECTINFO</span><span class="sxs-lookup"><span data-stu-id="2c82d-103">D3DXINTERSECTINFO structure</span></span>

<span data-ttu-id="2c82d-104">Descrive un'intersezione a triangolo di raggi.</span><span class="sxs-lookup"><span data-stu-id="2c82d-104">Describes a ray-triangle intersection.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c82d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2c82d-105">Syntax</span></span>


```C++
typedef struct D3DXINTERSECTINFO {
  DWORD FaceIndex;
  FLOAT U;
  FLOAT V;
  FLOAT Dist;
} D3DXINTERSECTINFO, *LPD3DXINTERSECTINFO;
```



## <a name="members"></a><span data-ttu-id="2c82d-106">Members</span><span class="sxs-lookup"><span data-stu-id="2c82d-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="2c82d-107">**FaceIndex**</span><span class="sxs-lookup"><span data-stu-id="2c82d-107">**FaceIndex**</span></span>
</dt> <dd>

<span data-ttu-id="2c82d-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2c82d-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2c82d-109">Indice del triangolo che ha raggiunto il raggio.</span><span class="sxs-lookup"><span data-stu-id="2c82d-109">Index of the triangle that hit the ray.</span></span>

</dd> <dt>

<span data-ttu-id="2c82d-110">**U**</span><span class="sxs-lookup"><span data-stu-id="2c82d-110">**U**</span></span>
</dt> <dd>

<span data-ttu-id="2c82d-111">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2c82d-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2c82d-112">Coordinata barycentrica all'interno del triangolo in cui si interseca il raggio.</span><span class="sxs-lookup"><span data-stu-id="2c82d-112">Barycentric coordinate within the triangle where the ray intersects.</span></span>

</dd> <dt>

<span data-ttu-id="2c82d-113">**V**</span><span class="sxs-lookup"><span data-stu-id="2c82d-113">**V**</span></span>
</dt> <dd>

<span data-ttu-id="2c82d-114">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2c82d-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2c82d-115">Coordinata barycentrica all'interno del triangolo in cui si interseca il raggio.</span><span class="sxs-lookup"><span data-stu-id="2c82d-115">Barycentric coordinate within the triangle where the ray intersects.</span></span>

</dd> <dt>

<span data-ttu-id="2c82d-116">**Dist**</span><span class="sxs-lookup"><span data-stu-id="2c82d-116">**Dist**</span></span>
</dt> <dd>

<span data-ttu-id="2c82d-117">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2c82d-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2c82d-118">Distanza lungo il raggio in cui si è verificata l'intersezione.</span><span class="sxs-lookup"><span data-stu-id="2c82d-118">Distance along the ray where the intersection occurred.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2c82d-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="2c82d-119">Remarks</span></span>

<span data-ttu-id="2c82d-120">Le coordinate barycentriche definiscono un punto all'interno di un triangolo in termini di vertici del triangolo.</span><span class="sxs-lookup"><span data-stu-id="2c82d-120">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="2c82d-121">Per una descrizione più approfondita delle coordinate barycentriche, vedere Descrizione delle coordinate [barycentriche di Mathworld.](https://mathworld.wolfram.com/BarycentricCoordinates.html)</span><span class="sxs-lookup"><span data-stu-id="2c82d-121">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="2c82d-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2c82d-122">Requirements</span></span>



| <span data-ttu-id="2c82d-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c82d-123">Requirement</span></span> | <span data-ttu-id="2c82d-124">Valore</span><span class="sxs-lookup"><span data-stu-id="2c82d-124">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2c82d-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2c82d-125">Header</span></span><br/> | <dl> <span data-ttu-id="2c82d-126"><dt>D3dx9mesh.h</dt></span><span class="sxs-lookup"><span data-stu-id="2c82d-126"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c82d-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2c82d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c82d-128">Strutture D3DX</span><span class="sxs-lookup"><span data-stu-id="2c82d-128">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
