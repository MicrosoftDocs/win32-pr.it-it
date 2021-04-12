---
description: Usa un'analisi efficiente del raggio nelle simulazioni del trasferimento di luminosità pre-calcolate (PRT) per determinare se un raggio interseca una mesh.
ms.assetid: e506aed3-bf14-4f29-845b-2091f5b00950
title: 'Metodo ID3DXPRTEngine:: ClosestRayIntersects (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ClosestRayIntersects
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4fd802f636077c9ec2a9f0f1060ffd43493aabf1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235177"
---
# <a name="id3dxprtengineclosestrayintersects-method"></a><span data-ttu-id="15fb7-103">Metodo ID3DXPRTEngine:: ClosestRayIntersects</span><span class="sxs-lookup"><span data-stu-id="15fb7-103">ID3DXPRTEngine::ClosestRayIntersects method</span></span>

<span data-ttu-id="15fb7-104">Usa un'analisi efficiente del raggio nelle simulazioni del trasferimento di luminosità pre-calcolate (PRT) per determinare se un raggio interseca una mesh.</span><span class="sxs-lookup"><span data-stu-id="15fb7-104">Uses efficient ray-tracing in precomputed radiance transfer (PRT) simulations to determine whether a ray intersects a mesh.</span></span> <span data-ttu-id="15fb7-105">Se viene rilevata un'intersezione, il metodo restituisce l'indice della faccia mesh più vicina raggiunta dal raggio e dalle coordinate baricentrica del punto di intersezione.</span><span class="sxs-lookup"><span data-stu-id="15fb7-105">If an intersection is found, the method returns the index of the closest mesh face hit by the ray and the barycentric coordinates of the intersection point.</span></span>

## <a name="syntax"></a><span data-ttu-id="15fb7-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="15fb7-106">Syntax</span></span>


```C++
BOOL ClosestRayIntersects(
  [in]  const D3DXVECTOR3 *pRayPos,
  [in]  const D3DXVECTOR3 *pRayDir,
  [in]        DWORD       *pFaceIndex,
  [out]       FLOAT       *pU,
  [out]       FLOAT       *pV,
  [out]       FLOAT       *pDist
);
```



## <a name="parameters"></a><span data-ttu-id="15fb7-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="15fb7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15fb7-108">*pRayPos* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="15fb7-108">*pRayPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15fb7-109">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="15fb7-109">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="15fb7-110">Puntatore a una struttura [**D3DXVECTOR3**](d3dxvector3.md) , che specifica il punto in cui inizia il raggio.</span><span class="sxs-lookup"><span data-stu-id="15fb7-110">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the point where the ray begins.</span></span>

</dd> <dt>

<span data-ttu-id="15fb7-111">*pRayDir* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="15fb7-111">*pRayDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15fb7-112">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="15fb7-112">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="15fb7-113">Puntatore a una struttura [**D3DXVECTOR3**](d3dxvector3.md) , che specifica la direzione normalizzata del raggio.</span><span class="sxs-lookup"><span data-stu-id="15fb7-113">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the normalized direction of the ray.</span></span>

</dd> <dt>

<span data-ttu-id="15fb7-114">*pFaceIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="15fb7-114">*pFaceIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15fb7-115">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="15fb7-115">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="15fb7-116">Puntatore all'indice della faccia mesh corrente che viene raggiunto prima dal raggio specificato, in base allo stack di tutti i visi della mesh di blocco davanti alla mesh corrente.</span><span class="sxs-lookup"><span data-stu-id="15fb7-116">Pointer to the index of the current mesh face that is first hit by the given ray, based upon stacking all blocker mesh faces in front of the current mesh.</span></span>

</dd> <dt>

<span data-ttu-id="15fb7-117">unità di *elaborazione* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="15fb7-117">*pU* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="15fb7-118">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="15fb7-118">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="15fb7-119">Puntatore a una coordinata di hit baricentrica, U, per il vertice 0 del triangolo.</span><span class="sxs-lookup"><span data-stu-id="15fb7-119">Pointer to a barycentric hit coordinate, U, for vertex 0 of the triangle.</span></span>

</dd> <dt>

<span data-ttu-id="15fb7-120">*PV* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="15fb7-120">*pV* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="15fb7-121">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="15fb7-121">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="15fb7-122">Puntatore a una coordinata baricentrica hit, V, per il vertice 1 del triangolo.</span><span class="sxs-lookup"><span data-stu-id="15fb7-122">Pointer to a barycentric hit coordinate, V, for vertex 1 of the triangle.</span></span>

</dd> <dt>

<span data-ttu-id="15fb7-123">*pDist* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="15fb7-123">*pDist* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="15fb7-124">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="15fb7-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="15fb7-125">Puntatore alla distanza del punto di intersezione lungo il raggio.</span><span class="sxs-lookup"><span data-stu-id="15fb7-125">Pointer to the distance of the intersection point along the ray.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15fb7-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="15fb7-126">Return value</span></span>

<span data-ttu-id="15fb7-127">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="15fb7-127">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="15fb7-128">Restituisce **true** se il raggio interseca la mesh corrente; in caso contrario, restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="15fb7-128">Returns **TRUE** if the ray intersects the current mesh; otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="15fb7-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="15fb7-129">Remarks</span></span>

<span data-ttu-id="15fb7-130">Usare [**ID3DXPRTEngine:: SetMinMaxIntersection**](id3dxprtengine--setminmaxintersection.md) per impostare le distanze minime e massime dell'intersezione con il raggio.</span><span class="sxs-lookup"><span data-stu-id="15fb7-130">Use [**ID3DXPRTEngine::SetMinMaxIntersection**](id3dxprtengine--setminmaxintersection.md) to set minimum and maximum distances of intersection with the ray.</span></span>

<span data-ttu-id="15fb7-131">La coordinata baricentrica del terzo vertice (vertice 2) del triangolo è 1-(U + V).</span><span class="sxs-lookup"><span data-stu-id="15fb7-131">The barycentric coordinate of the third vertex (vertex 2) of the triangle is 1 - ( U + V ).</span></span>

<span data-ttu-id="15fb7-132">Questo metodo viene eseguito più lentamente di [**ID3DXPRTEngine:: ShadowRayIntersects**](id3dxprtengine--shadowrayintersects.md).</span><span class="sxs-lookup"><span data-stu-id="15fb7-132">This method executes slower than [**ID3DXPRTEngine::ShadowRayIntersects**](id3dxprtengine--shadowrayintersects.md).</span></span> <span data-ttu-id="15fb7-133">Usare **ID3DXPRTEngine:: ShadowRayIntersects** se il percorso del punto di intersezione non è necessario.</span><span class="sxs-lookup"><span data-stu-id="15fb7-133">Use **ID3DXPRTEngine::ShadowRayIntersects** if the location of the intersection point is not needed.</span></span>

<span data-ttu-id="15fb7-134">Le coordinate baricentrica definiscono un punto all'interno di un triangolo in termini di vertici del triangolo.</span><span class="sxs-lookup"><span data-stu-id="15fb7-134">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="15fb7-135">Per una descrizione più approfondita delle coordinate baricentrica, vedere [la descrizione delle coordinate baricentrica di articolo MathWorld](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span><span class="sxs-lookup"><span data-stu-id="15fb7-135">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="15fb7-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="15fb7-136">Requirements</span></span>



| <span data-ttu-id="15fb7-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="15fb7-137">Requirement</span></span> | <span data-ttu-id="15fb7-138">Valore</span><span class="sxs-lookup"><span data-stu-id="15fb7-138">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="15fb7-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="15fb7-139">Header</span></span><br/>  | <dl> <span data-ttu-id="15fb7-140"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="15fb7-140"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="15fb7-141">Libreria</span><span class="sxs-lookup"><span data-stu-id="15fb7-141">Library</span></span><br/> | <dl> <span data-ttu-id="15fb7-142"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="15fb7-142"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="15fb7-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="15fb7-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15fb7-144">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="15fb7-144">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> <dt>

[<span data-ttu-id="15fb7-145">**ID3DXPRTEngine::ShadowRayIntersects**</span><span class="sxs-lookup"><span data-stu-id="15fb7-145">**ID3DXPRTEngine::ShadowRayIntersects**</span></span>](id3dxprtengine--shadowrayintersects.md)
</dt> <dt>

[<span data-ttu-id="15fb7-146">**ID3DXPRTEngine::SetMinMaxIntersection**</span><span class="sxs-lookup"><span data-stu-id="15fb7-146">**ID3DXPRTEngine::SetMinMaxIntersection**</span></span>](id3dxprtengine--setminmaxintersection.md)
</dt> </dl>

 

 
