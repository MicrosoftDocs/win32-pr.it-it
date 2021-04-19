---
description: Calcola l'intersezione tra un raggio e un triangolo.
ms.assetid: 819f2543-8046-47c9-93b8-7d888264786f
title: Funzione D3DXIntersectTri (D3DX10math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXIntersectTri
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: af96d25b4f13995d60e7926ec5da2d15ff86f282
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322781"
---
# <a name="d3dxintersecttri-function-d3dx10mathh"></a><span data-ttu-id="4cfc6-103">Funzione D3DXIntersectTri (D3DX10math. h)</span><span class="sxs-lookup"><span data-stu-id="4cfc6-103">D3DXIntersectTri function (D3DX10math.h)</span></span>

<span data-ttu-id="4cfc6-104">Calcola l'intersezione tra un raggio e un triangolo.</span><span class="sxs-lookup"><span data-stu-id="4cfc6-104">Computes the intersection of a ray and a triangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="4cfc6-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4cfc6-105">Syntax</span></span>


```C++
BOOL D3DXIntersectTri(
  _In_  const D3DXVECTOR3 *p0,
  _In_  const D3DXVECTOR3 *p1,
  _In_  const D3DXVECTOR3 *p2,
  _In_  const D3DXVECTOR3 *pRayPos,
  _In_  const D3DXVECTOR3 *pRayDir,
  _Out_       FLOAT       *pU,
  _Out_       FLOAT       *pV,
  _Out_       FLOAT       *pDist
);
```



## <a name="parameters"></a><span data-ttu-id="4cfc6-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4cfc6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4cfc6-107">*P0* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4cfc6-107">*p0* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4cfc6-108">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="4cfc6-108">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="4cfc6-109">Puntatore a una struttura [**D3DXVECTOR3**](d3d10-d3dxvector3.md) che descrive la prima posizione del vertice del triangolo.</span><span class="sxs-lookup"><span data-stu-id="4cfc6-109">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, describing the first triangle vertex position.</span></span>

</dd> <dt>

<span data-ttu-id="4cfc6-110">*P1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4cfc6-110">*p1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4cfc6-111">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="4cfc6-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="4cfc6-112">Puntatore a una struttura [**D3DXVECTOR3**](d3d10-d3dxvector3.md) che descrive la seconda posizione del vertice del triangolo.</span><span class="sxs-lookup"><span data-stu-id="4cfc6-112">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, describing the second triangle vertex position.</span></span>

</dd> <dt>

<span data-ttu-id="4cfc6-113">*P2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4cfc6-113">*p2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4cfc6-114">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="4cfc6-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="4cfc6-115">Puntatore a una struttura [**D3DXVECTOR3**](d3d10-d3dxvector3.md) che descrive la posizione del vertice del terzo triangolo.</span><span class="sxs-lookup"><span data-stu-id="4cfc6-115">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, describing the third triangle vertex position.</span></span>

</dd> <dt>

<span data-ttu-id="4cfc6-116">*pRayPos* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4cfc6-116">*pRayPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4cfc6-117">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="4cfc6-117">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="4cfc6-118">Puntatore a una struttura [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , che specifica il punto in cui inizia il raggio.</span><span class="sxs-lookup"><span data-stu-id="4cfc6-118">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, specifying the point where the ray begins.</span></span>

</dd> <dt>

<span data-ttu-id="4cfc6-119">*pRayDir* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4cfc6-119">*pRayDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4cfc6-120">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="4cfc6-120">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="4cfc6-121">Puntatore a una struttura [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , che specifica la direzione del raggio.</span><span class="sxs-lookup"><span data-stu-id="4cfc6-121">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, specifying the direction of the ray.</span></span>

</dd> <dt>

<span data-ttu-id="4cfc6-122">unità di *elaborazione* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="4cfc6-122">*pU* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4cfc6-123">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="4cfc6-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="4cfc6-124">Coordinate baricentrica hit, U.</span><span class="sxs-lookup"><span data-stu-id="4cfc6-124">Barycentric hit coordinates, U.</span></span>

</dd> <dt>

<span data-ttu-id="4cfc6-125">*PV* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="4cfc6-125">*pV* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4cfc6-126">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="4cfc6-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="4cfc6-127">Coordinate baricentrica hit, V.</span><span class="sxs-lookup"><span data-stu-id="4cfc6-127">Barycentric hit coordinates, V.</span></span>

</dd> <dt>

<span data-ttu-id="4cfc6-128">*pDist* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="4cfc6-128">*pDist* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4cfc6-129">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="4cfc6-129">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="4cfc6-130">Distanza del parametro di intersezione tra Ray.</span><span class="sxs-lookup"><span data-stu-id="4cfc6-130">Ray-intersection parameter distance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4cfc6-131">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4cfc6-131">Return value</span></span>

<span data-ttu-id="4cfc6-132">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4cfc6-132">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4cfc6-133">Restituisce **true** se il raggio interseca l'area del triangolo.</span><span class="sxs-lookup"><span data-stu-id="4cfc6-133">Returns **TRUE** if the ray intersects the area of the triangle.</span></span> <span data-ttu-id="4cfc6-134">In caso contrario, restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="4cfc6-134">Otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="4cfc6-135">Commenti</span><span class="sxs-lookup"><span data-stu-id="4cfc6-135">Remarks</span></span>

<span data-ttu-id="4cfc6-136">Qualsiasi punto nel V1V2V3 del piano può essere rappresentato dalla coordinata baricentrica (U, V).</span><span class="sxs-lookup"><span data-stu-id="4cfc6-136">Any point in the plane V1V2V3 can be represented by the barycentric coordinate (U,V).</span></span> <span data-ttu-id="4cfc6-137">Il parametro U controlla la quantità di V2 che viene ponderata nel risultato e il parametro V controlla la quantità di V3 che viene ponderata nel risultato.</span><span class="sxs-lookup"><span data-stu-id="4cfc6-137">The parameter U controls how much V2 gets weighted into the result, and the parameter V controls how much V3 gets weighted into the result.</span></span> <span data-ttu-id="4cfc6-138">Infine, il valore \[ 1-(U + V) controlla la \] quantità di V1 che viene ponderata nel risultato.</span><span class="sxs-lookup"><span data-stu-id="4cfc6-138">Lastly, the value of \[1 - (U + V)\] controls how much V1 gets weighted into the result.</span></span>

<span data-ttu-id="4cfc6-139">Le coordinate baricentrica sono costituite da coordinate generali.</span><span class="sxs-lookup"><span data-stu-id="4cfc6-139">Barycentric coordinates are a form of general coordinates.</span></span> <span data-ttu-id="4cfc6-140">In questo contesto, l'utilizzo delle coordinate baricentrica rappresenta una modifica nei sistemi di coordinate.</span><span class="sxs-lookup"><span data-stu-id="4cfc6-140">In this context, using barycentric coordinates represents a change in coordinate systems.</span></span> <span data-ttu-id="4cfc6-141">Ciò che è valido per le coordinate cartesiane è valido per le coordinate baricentrica.</span><span class="sxs-lookup"><span data-stu-id="4cfc6-141">What holds true for Cartesian coordinates holds true for barycentric coordinates.</span></span>

<span data-ttu-id="4cfc6-142">Le coordinate baricentrica definiscono un punto all'interno di un triangolo in termini di vertici del triangolo.</span><span class="sxs-lookup"><span data-stu-id="4cfc6-142">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="4cfc6-143">Per una descrizione più approfondita delle coordinate baricentrica, vedere [la descrizione delle coordinate baricentrica di articolo MathWorld](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span><span class="sxs-lookup"><span data-stu-id="4cfc6-143">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="4cfc6-144">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4cfc6-144">Requirements</span></span>



| <span data-ttu-id="4cfc6-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="4cfc6-145">Requirement</span></span> | <span data-ttu-id="4cfc6-146">Valore</span><span class="sxs-lookup"><span data-stu-id="4cfc6-146">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4cfc6-147">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4cfc6-147">Header</span></span><br/>  | <dl> <span data-ttu-id="4cfc6-148"><dt>D3DX10math. h</dt></span><span class="sxs-lookup"><span data-stu-id="4cfc6-148"><dt>D3DX10math.h</dt></span></span> </dl> |
| <span data-ttu-id="4cfc6-149">Libreria</span><span class="sxs-lookup"><span data-stu-id="4cfc6-149">Library</span></span><br/> | <dl> <span data-ttu-id="4cfc6-150"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4cfc6-150"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4cfc6-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4cfc6-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cfc6-152">Funzioni mesh</span><span class="sxs-lookup"><span data-stu-id="4cfc6-152">Mesh Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> </dl>

 

 
