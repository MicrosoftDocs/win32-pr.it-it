---
description: Calcola l'intersezione tra un raggio e un triangolo.
ms.assetid: f335a71d-7203-4ea1-a6bf-407b28c712e6
title: Funzione D3DXIntersectTri (D3DX9Mesh. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 41c7012cea0a533dc447db0575def6b418d0e59e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322644"
---
# <a name="d3dxintersecttri-function-d3dx9meshh"></a><span data-ttu-id="8df8e-103">Funzione D3DXIntersectTri (D3DX9Mesh. h)</span><span class="sxs-lookup"><span data-stu-id="8df8e-103">D3DXIntersectTri function (D3DX9Mesh.h)</span></span>

<span data-ttu-id="8df8e-104">Calcola l'intersezione tra un raggio e un triangolo.</span><span class="sxs-lookup"><span data-stu-id="8df8e-104">Computes the intersection of a ray and a triangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="8df8e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8df8e-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="8df8e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8df8e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8df8e-107">*P0* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8df8e-107">*p0* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8df8e-108">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="8df8e-108">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="8df8e-109">Puntatore a una struttura [**D3DXVECTOR3**](d3dxvector3.md) che descrive la prima posizione del vertice del triangolo.</span><span class="sxs-lookup"><span data-stu-id="8df8e-109">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, describing the first triangle vertex position.</span></span>

</dd> <dt>

<span data-ttu-id="8df8e-110">*P1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8df8e-110">*p1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8df8e-111">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="8df8e-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="8df8e-112">Puntatore a una struttura [**D3DXVECTOR3**](d3dxvector3.md) che descrive la seconda posizione del vertice del triangolo.</span><span class="sxs-lookup"><span data-stu-id="8df8e-112">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, describing the second triangle vertex position.</span></span>

</dd> <dt>

<span data-ttu-id="8df8e-113">*P2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8df8e-113">*p2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8df8e-114">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="8df8e-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="8df8e-115">Puntatore a una struttura [**D3DXVECTOR3**](d3dxvector3.md) che descrive la posizione del vertice del terzo triangolo.</span><span class="sxs-lookup"><span data-stu-id="8df8e-115">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, describing the third triangle vertex position.</span></span>

</dd> <dt>

<span data-ttu-id="8df8e-116">*pRayPos* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8df8e-116">*pRayPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8df8e-117">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="8df8e-117">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="8df8e-118">Puntatore a una struttura [**D3DXVECTOR3**](d3dxvector3.md) , che specifica il punto in cui inizia il raggio.</span><span class="sxs-lookup"><span data-stu-id="8df8e-118">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the point where the ray begins.</span></span>

</dd> <dt>

<span data-ttu-id="8df8e-119">*pRayDir* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8df8e-119">*pRayDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8df8e-120">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="8df8e-120">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="8df8e-121">Puntatore a una struttura [**D3DXVECTOR3**](d3dxvector3.md) , che specifica la direzione del raggio.</span><span class="sxs-lookup"><span data-stu-id="8df8e-121">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the direction of the ray.</span></span>

</dd> <dt>

<span data-ttu-id="8df8e-122">unità di *elaborazione* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="8df8e-122">*pU* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8df8e-123">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="8df8e-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="8df8e-124">Coordinate baricentrica hit, U.</span><span class="sxs-lookup"><span data-stu-id="8df8e-124">Barycentric hit coordinates, U.</span></span>

</dd> <dt>

<span data-ttu-id="8df8e-125">*PV* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="8df8e-125">*pV* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8df8e-126">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="8df8e-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="8df8e-127">Coordinate baricentrica hit, V.</span><span class="sxs-lookup"><span data-stu-id="8df8e-127">Barycentric hit coordinates, V.</span></span>

</dd> <dt>

<span data-ttu-id="8df8e-128">*pDist* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="8df8e-128">*pDist* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8df8e-129">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="8df8e-129">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="8df8e-130">Distanza del parametro di intersezione tra Ray.</span><span class="sxs-lookup"><span data-stu-id="8df8e-130">Ray-intersection parameter distance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8df8e-131">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8df8e-131">Return value</span></span>

<span data-ttu-id="8df8e-132">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8df8e-132">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8df8e-133">Restituisce **true** se il raggio interseca l'area del triangolo.</span><span class="sxs-lookup"><span data-stu-id="8df8e-133">Returns **TRUE** if the ray intersects the area of the triangle.</span></span> <span data-ttu-id="8df8e-134">In caso contrario, restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="8df8e-134">Otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="8df8e-135">Commenti</span><span class="sxs-lookup"><span data-stu-id="8df8e-135">Remarks</span></span>

<span data-ttu-id="8df8e-136">La funzione [**D3DXIntersect**](d3dxintersect.md) fornisce un modo per comprendere i punti in e intorno a un triangolo, indipendentemente dalla posizione in cui si trova effettivamente il triangolo.</span><span class="sxs-lookup"><span data-stu-id="8df8e-136">The [**D3DXIntersect**](d3dxintersect.md) function provides a way to understand points in and around a triangle, independent of where the triangle is actually located.</span></span> <span data-ttu-id="8df8e-137">Questa funzione restituisce il punto risultante utilizzando l'equazione seguente: V1 + U (v2-v1) + V (V3-V1).</span><span class="sxs-lookup"><span data-stu-id="8df8e-137">This function returns the resulting point by using the following equation: V1 + U(V2 - V1) + V(V3 - V1).</span></span>

<span data-ttu-id="8df8e-138">Qualsiasi punto nel V1V2V3 del piano può essere rappresentato dalla coordinata baricentrica (U, V).</span><span class="sxs-lookup"><span data-stu-id="8df8e-138">Any point in the plane V1V2V3 can be represented by the barycentric coordinate (U,V).</span></span> <span data-ttu-id="8df8e-139">Il parametro U controlla la quantità di V2 che viene ponderata nel risultato e il parametro V controlla la quantità di V3 che viene ponderata nel risultato.</span><span class="sxs-lookup"><span data-stu-id="8df8e-139">The parameter U controls how much V2 gets weighted into the result, and the parameter V controls how much V3 gets weighted into the result.</span></span> <span data-ttu-id="8df8e-140">Infine, il valore \[ 1-(U + V) controlla la \] quantità di V1 che viene ponderata nel risultato.</span><span class="sxs-lookup"><span data-stu-id="8df8e-140">Lastly, the value of \[1 - (U + V)\] controls how much V1 gets weighted into the result.</span></span>

<span data-ttu-id="8df8e-141">Le coordinate baricentrica sono costituite da coordinate generali.</span><span class="sxs-lookup"><span data-stu-id="8df8e-141">Barycentric coordinates are a form of general coordinates.</span></span> <span data-ttu-id="8df8e-142">In questo contesto, l'utilizzo delle coordinate baricentrica rappresenta una modifica nei sistemi di coordinate.</span><span class="sxs-lookup"><span data-stu-id="8df8e-142">In this context, using barycentric coordinates represents a change in coordinate systems.</span></span> <span data-ttu-id="8df8e-143">Ciò che è valido per le coordinate cartesiane è valido per le coordinate baricentrica.</span><span class="sxs-lookup"><span data-stu-id="8df8e-143">What holds true for Cartesian coordinates holds true for barycentric coordinates.</span></span>

<span data-ttu-id="8df8e-144">Le coordinate baricentrica definiscono un punto all'interno di un triangolo in termini di vertici del triangolo.</span><span class="sxs-lookup"><span data-stu-id="8df8e-144">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="8df8e-145">Per una descrizione più approfondita delle coordinate baricentrica, vedere [la descrizione delle coordinate baricentrica di articolo MathWorld](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span><span class="sxs-lookup"><span data-stu-id="8df8e-145">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="8df8e-146">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8df8e-146">Requirements</span></span>



| <span data-ttu-id="8df8e-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="8df8e-147">Requirement</span></span> | <span data-ttu-id="8df8e-148">Valore</span><span class="sxs-lookup"><span data-stu-id="8df8e-148">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8df8e-149">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8df8e-149">Header</span></span><br/>  | <dl> <span data-ttu-id="8df8e-150"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="8df8e-150"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="8df8e-151">Libreria</span><span class="sxs-lookup"><span data-stu-id="8df8e-151">Library</span></span><br/> | <dl> <span data-ttu-id="8df8e-152"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8df8e-152"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8df8e-153">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8df8e-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8df8e-154">Funzioni mesh</span><span class="sxs-lookup"><span data-stu-id="8df8e-154">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
