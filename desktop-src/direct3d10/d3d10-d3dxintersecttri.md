---
description: "Funzione D3DXIntersectTri (D3DX10math.h): calcola l'intersezione di un raggio e di un triangolo."
ms.assetid: 819f2543-8046-47c9-93b8-7d888264786f
title: Funzione D3DXIntersectTri (D3DX10math.h)
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
ms.openlocfilehash: c8bf502cca48701a7d71a083e515f9988cafe303
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113239"
---
# <a name="d3dxintersecttri-function-d3dx10mathh"></a><span data-ttu-id="cdb88-103">Funzione D3DXIntersectTri (D3DX10math.h)</span><span class="sxs-lookup"><span data-stu-id="cdb88-103">D3DXIntersectTri function (D3DX10math.h)</span></span>

<span data-ttu-id="cdb88-104">Calcola l'intersezione di un raggio e di un triangolo.</span><span class="sxs-lookup"><span data-stu-id="cdb88-104">Computes the intersection of a ray and a triangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="cdb88-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cdb88-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="cdb88-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="cdb88-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cdb88-107">*p0* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="cdb88-107">*p0* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdb88-108">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="cdb88-108">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="cdb88-109">Puntatore a una [**struttura D3DXVECTOR3,**](d3d10-d3dxvector3.md) che descrive la posizione del primo vertice triangolare.</span><span class="sxs-lookup"><span data-stu-id="cdb88-109">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, describing the first triangle vertex position.</span></span>

</dd> <dt>

<span data-ttu-id="cdb88-110">*p1* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="cdb88-110">*p1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdb88-111">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="cdb88-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="cdb88-112">Puntatore a una [**struttura D3DXVECTOR3,**](d3d10-d3dxvector3.md) che descrive la posizione del secondo vertice triangolare.</span><span class="sxs-lookup"><span data-stu-id="cdb88-112">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, describing the second triangle vertex position.</span></span>

</dd> <dt>

<span data-ttu-id="cdb88-113">*p2* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="cdb88-113">*p2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdb88-114">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="cdb88-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="cdb88-115">Puntatore a una [**struttura D3DXVECTOR3,**](d3d10-d3dxvector3.md) che descrive la posizione del terzo vertice triangolare.</span><span class="sxs-lookup"><span data-stu-id="cdb88-115">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, describing the third triangle vertex position.</span></span>

</dd> <dt>

<span data-ttu-id="cdb88-116">*pRayPos* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="cdb88-116">*pRayPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdb88-117">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="cdb88-117">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="cdb88-118">Puntatore a [**una struttura D3DXVECTOR3,**](d3d10-d3dxvector3.md) che specifica il punto in cui inizia il raggio.</span><span class="sxs-lookup"><span data-stu-id="cdb88-118">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, specifying the point where the ray begins.</span></span>

</dd> <dt>

<span data-ttu-id="cdb88-119">*pRayDir* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="cdb88-119">*pRayDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdb88-120">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="cdb88-120">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="cdb88-121">Puntatore a [**una struttura D3DXVECTOR3,**](d3d10-d3dxvector3.md) che specifica la direzione del raggio.</span><span class="sxs-lookup"><span data-stu-id="cdb88-121">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, specifying the direction of the ray.</span></span>

</dd> <dt>

<span data-ttu-id="cdb88-122">*pU* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="cdb88-122">*pU* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cdb88-123">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="cdb88-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="cdb88-124">Coordinate di hit barycentriche, U.</span><span class="sxs-lookup"><span data-stu-id="cdb88-124">Barycentric hit coordinates, U.</span></span>

</dd> <dt>

<span data-ttu-id="cdb88-125">*pV* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="cdb88-125">*pV* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cdb88-126">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="cdb88-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="cdb88-127">Coordinate di hit barycentriche, V.</span><span class="sxs-lookup"><span data-stu-id="cdb88-127">Barycentric hit coordinates, V.</span></span>

</dd> <dt>

<span data-ttu-id="cdb88-128">*pDist* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="cdb88-128">*pDist* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cdb88-129">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="cdb88-129">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="cdb88-130">Distanza dei parametri di intersezione dei raggi.</span><span class="sxs-lookup"><span data-stu-id="cdb88-130">Ray-intersection parameter distance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cdb88-131">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cdb88-131">Return value</span></span>

<span data-ttu-id="cdb88-132">Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cdb88-132">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cdb88-133">Restituisce **TRUE** se il raggio interseca l'area del triangolo.</span><span class="sxs-lookup"><span data-stu-id="cdb88-133">Returns **TRUE** if the ray intersects the area of the triangle.</span></span> <span data-ttu-id="cdb88-134">In caso contrario, **restituisce FALSE.**</span><span class="sxs-lookup"><span data-stu-id="cdb88-134">Otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="cdb88-135">Commenti</span><span class="sxs-lookup"><span data-stu-id="cdb88-135">Remarks</span></span>

<span data-ttu-id="cdb88-136">Qualsiasi punto nel piano V1V2V3 può essere rappresentato dalla coordinata barycentric (U,V).</span><span class="sxs-lookup"><span data-stu-id="cdb88-136">Any point in the plane V1V2V3 can be represented by the barycentric coordinate (U,V).</span></span> <span data-ttu-id="cdb88-137">Il parametro U controlla quanto V2 viene ponderato nel risultato e il parametro V controlla quanto V3 viene ponderato nel risultato.</span><span class="sxs-lookup"><span data-stu-id="cdb88-137">The parameter U controls how much V2 gets weighted into the result, and the parameter V controls how much V3 gets weighted into the result.</span></span> <span data-ttu-id="cdb88-138">Infine, il valore 1 - (U + V) controlla quanto \[ \] V1 viene ponderato nel risultato.</span><span class="sxs-lookup"><span data-stu-id="cdb88-138">Lastly, the value of \[1 - (U + V)\] controls how much V1 gets weighted into the result.</span></span>

<span data-ttu-id="cdb88-139">Le coordinate barycentriche sono una forma di coordinate generali.</span><span class="sxs-lookup"><span data-stu-id="cdb88-139">Barycentric coordinates are a form of general coordinates.</span></span> <span data-ttu-id="cdb88-140">In questo contesto, l'uso di coordinate barycentrice rappresenta una modifica nei sistemi di coordinate.</span><span class="sxs-lookup"><span data-stu-id="cdb88-140">In this context, using barycentric coordinates represents a change in coordinate systems.</span></span> <span data-ttu-id="cdb88-141">Ciò che vale per le coordinate cartesiane è vero per le coordinate barycentriche.</span><span class="sxs-lookup"><span data-stu-id="cdb88-141">What holds true for Cartesian coordinates holds true for barycentric coordinates.</span></span>

<span data-ttu-id="cdb88-142">Le coordinate barycentriche definiscono un punto all'interno di un triangolo in termini di vertici del triangolo.</span><span class="sxs-lookup"><span data-stu-id="cdb88-142">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="cdb88-143">Per una descrizione più dettagliata delle coordinate barycentric, vedere Descrizione delle [coordinate barycentriche di Mathworld.](https://mathworld.wolfram.com/BarycentricCoordinates.html)</span><span class="sxs-lookup"><span data-stu-id="cdb88-143">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="cdb88-144">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cdb88-144">Requirements</span></span>



| <span data-ttu-id="cdb88-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="cdb88-145">Requirement</span></span> | <span data-ttu-id="cdb88-146">Valore</span><span class="sxs-lookup"><span data-stu-id="cdb88-146">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cdb88-147">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cdb88-147">Header</span></span><br/>  | <dl> <span data-ttu-id="cdb88-148"><dt>D3DX10math.h</dt></span><span class="sxs-lookup"><span data-stu-id="cdb88-148"><dt>D3DX10math.h</dt></span></span> </dl> |
| <span data-ttu-id="cdb88-149">Libreria</span><span class="sxs-lookup"><span data-stu-id="cdb88-149">Library</span></span><br/> | <dl> <span data-ttu-id="cdb88-150"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="cdb88-150"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="cdb88-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cdb88-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cdb88-152">Funzioni mesh</span><span class="sxs-lookup"><span data-stu-id="cdb88-152">Mesh Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> </dl>

 

 
