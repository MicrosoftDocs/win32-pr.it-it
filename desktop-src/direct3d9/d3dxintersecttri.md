---
description: "Funzione D3DXIntersectTri (D3DX9Mesh.h): calcola l'intersezione di un raggio e di un triangolo."
ms.assetid: f335a71d-7203-4ea1-a6bf-407b28c712e6
title: Funzione D3DXIntersectTri (D3DX9Mesh.h)
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
ms.openlocfilehash: 33d45beda51a7a2c80debafbab864c2accb33653
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098269"
---
# <a name="d3dxintersecttri-function-d3dx9meshh"></a><span data-ttu-id="87909-103">Funzione D3DXIntersectTri (D3DX9Mesh.h)</span><span class="sxs-lookup"><span data-stu-id="87909-103">D3DXIntersectTri function (D3DX9Mesh.h)</span></span>

<span data-ttu-id="87909-104">Calcola l'intersezione di un raggio e di un triangolo.</span><span class="sxs-lookup"><span data-stu-id="87909-104">Computes the intersection of a ray and a triangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="87909-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="87909-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="87909-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="87909-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87909-107">*p0* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="87909-107">*p0* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87909-108">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="87909-108">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="87909-109">Puntatore a una [**struttura D3DXVECTOR3,**](d3dxvector3.md) che descrive la prima posizione del vertice del triangolo.</span><span class="sxs-lookup"><span data-stu-id="87909-109">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, describing the first triangle vertex position.</span></span>

</dd> <dt>

<span data-ttu-id="87909-110">*p1* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="87909-110">*p1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87909-111">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="87909-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="87909-112">Puntatore a una [**struttura D3DXVECTOR3,**](d3dxvector3.md) che descrive la seconda posizione del vertice del triangolo.</span><span class="sxs-lookup"><span data-stu-id="87909-112">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, describing the second triangle vertex position.</span></span>

</dd> <dt>

<span data-ttu-id="87909-113">*p2* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="87909-113">*p2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87909-114">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="87909-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="87909-115">Puntatore a una [**struttura D3DXVECTOR3,**](d3dxvector3.md) che descrive la posizione del terzo vertice del triangolo.</span><span class="sxs-lookup"><span data-stu-id="87909-115">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, describing the third triangle vertex position.</span></span>

</dd> <dt>

<span data-ttu-id="87909-116">*pRayPos* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="87909-116">*pRayPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87909-117">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="87909-117">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="87909-118">Puntatore a [**una struttura D3DXVECTOR3,**](d3dxvector3.md) che specifica il punto in cui inizia il raggio.</span><span class="sxs-lookup"><span data-stu-id="87909-118">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the point where the ray begins.</span></span>

</dd> <dt>

<span data-ttu-id="87909-119">*pRayDir* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="87909-119">*pRayDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87909-120">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="87909-120">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="87909-121">Puntatore a [**una struttura D3DXVECTOR3,**](d3dxvector3.md) che specifica la direzione del raggio.</span><span class="sxs-lookup"><span data-stu-id="87909-121">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the direction of the ray.</span></span>

</dd> <dt>

<span data-ttu-id="87909-122">*pU* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="87909-122">*pU* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="87909-123">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="87909-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="87909-124">Coordinate di hit barycentriche, U.</span><span class="sxs-lookup"><span data-stu-id="87909-124">Barycentric hit coordinates, U.</span></span>

</dd> <dt>

<span data-ttu-id="87909-125">*pV* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="87909-125">*pV* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="87909-126">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="87909-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="87909-127">Coordinate di hit barycentriche, V.</span><span class="sxs-lookup"><span data-stu-id="87909-127">Barycentric hit coordinates, V.</span></span>

</dd> <dt>

<span data-ttu-id="87909-128">*pDist* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="87909-128">*pDist* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="87909-129">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="87909-129">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="87909-130">Distanza dei parametri di intersezione dei raggi.</span><span class="sxs-lookup"><span data-stu-id="87909-130">Ray-intersection parameter distance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87909-131">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="87909-131">Return value</span></span>

<span data-ttu-id="87909-132">Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="87909-132">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="87909-133">Restituisce **TRUE** se il raggio interseca l'area del triangolo.</span><span class="sxs-lookup"><span data-stu-id="87909-133">Returns **TRUE** if the ray intersects the area of the triangle.</span></span> <span data-ttu-id="87909-134">In caso contrario, **restituisce FALSE.**</span><span class="sxs-lookup"><span data-stu-id="87909-134">Otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="87909-135">Commenti</span><span class="sxs-lookup"><span data-stu-id="87909-135">Remarks</span></span>

<span data-ttu-id="87909-136">La [**funzione D3DXIntersect**](d3dxintersect.md) consente di comprendere i punti all'interno e intorno a un triangolo, indipendentemente dalla posizione in cui si trova effettivamente il triangolo.</span><span class="sxs-lookup"><span data-stu-id="87909-136">The [**D3DXIntersect**](d3dxintersect.md) function provides a way to understand points in and around a triangle, independent of where the triangle is actually located.</span></span> <span data-ttu-id="87909-137">Questa funzione restituisce il punto risultante usando l'equazione seguente: V1 + U(V2 - V1) + V(V3 - V1).</span><span class="sxs-lookup"><span data-stu-id="87909-137">This function returns the resulting point by using the following equation: V1 + U(V2 - V1) + V(V3 - V1).</span></span>

<span data-ttu-id="87909-138">Qualsiasi punto nel piano V1V2V3 può essere rappresentato dalla coordinata barycentric (U,V).</span><span class="sxs-lookup"><span data-stu-id="87909-138">Any point in the plane V1V2V3 can be represented by the barycentric coordinate (U,V).</span></span> <span data-ttu-id="87909-139">Il parametro U controlla quanto V2 viene ponderato nel risultato e il parametro V controlla quanto V3 viene ponderato nel risultato.</span><span class="sxs-lookup"><span data-stu-id="87909-139">The parameter U controls how much V2 gets weighted into the result, and the parameter V controls how much V3 gets weighted into the result.</span></span> <span data-ttu-id="87909-140">Infine, il valore 1 - (U + V) controlla quanto \[ \] V1 viene ponderato nel risultato.</span><span class="sxs-lookup"><span data-stu-id="87909-140">Lastly, the value of \[1 - (U + V)\] controls how much V1 gets weighted into the result.</span></span>

<span data-ttu-id="87909-141">Le coordinate barycentriche sono una forma di coordinate generali.</span><span class="sxs-lookup"><span data-stu-id="87909-141">Barycentric coordinates are a form of general coordinates.</span></span> <span data-ttu-id="87909-142">In questo contesto, l'uso di coordinate barycentrice rappresenta una modifica nei sistemi di coordinate.</span><span class="sxs-lookup"><span data-stu-id="87909-142">In this context, using barycentric coordinates represents a change in coordinate systems.</span></span> <span data-ttu-id="87909-143">Ciò che vale per le coordinate cartesiane è vero per le coordinate barycentriche.</span><span class="sxs-lookup"><span data-stu-id="87909-143">What holds true for Cartesian coordinates holds true for barycentric coordinates.</span></span>

<span data-ttu-id="87909-144">Le coordinate barycentriche definiscono un punto all'interno di un triangolo in termini di vertici del triangolo.</span><span class="sxs-lookup"><span data-stu-id="87909-144">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="87909-145">Per una descrizione più approfondita delle coordinate barycentriche, vedere Descrizione delle coordinate [barycentriche di Mathworld.](https://mathworld.wolfram.com/BarycentricCoordinates.html)</span><span class="sxs-lookup"><span data-stu-id="87909-145">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="87909-146">Requisiti</span><span class="sxs-lookup"><span data-stu-id="87909-146">Requirements</span></span>



| <span data-ttu-id="87909-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="87909-147">Requirement</span></span> | <span data-ttu-id="87909-148">Valore</span><span class="sxs-lookup"><span data-stu-id="87909-148">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="87909-149">Intestazione</span><span class="sxs-lookup"><span data-stu-id="87909-149">Header</span></span><br/>  | <dl> <span data-ttu-id="87909-150"><dt>D3DX9Mesh.h</dt></span><span class="sxs-lookup"><span data-stu-id="87909-150"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="87909-151">Libreria</span><span class="sxs-lookup"><span data-stu-id="87909-151">Library</span></span><br/> | <dl> <span data-ttu-id="87909-152"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="87909-152"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="87909-153">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="87909-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87909-154">Funzioni mesh</span><span class="sxs-lookup"><span data-stu-id="87909-154">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
