---
description: Determina se un raggio si interseca con una mesh.
ms.assetid: 325f5b40-80ba-4400-a143-bae41146ab07
title: Funzione D3DXIntersect (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXIntersect
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: dc877fb1301e01b05184625ba2e92a2c680cfa9f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322648"
---
# <a name="d3dxintersect-function"></a><span data-ttu-id="92109-103">D3DXIntersect (funzione)</span><span class="sxs-lookup"><span data-stu-id="92109-103">D3DXIntersect function</span></span>

<span data-ttu-id="92109-104">Determina se un raggio si interseca con una mesh.</span><span class="sxs-lookup"><span data-stu-id="92109-104">Determines if a ray intersects with a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="92109-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="92109-105">Syntax</span></span>


```C++
HRESULT D3DXIntersect(
  _In_        LPD3DXBASEMESH pMesh,
  _In_  const D3DXVECTOR3    *pRayPos,
  _In_  const D3DXVECTOR3    *pRayDir,
  _Out_       BOOL           *pHit,
  _Out_       DWORD          *pFaceIndex,
  _Out_       FLOAT          *pU,
  _Out_       FLOAT          *pV,
  _Out_       FLOAT          *pDist,
  _Out_       LPD3DXBUFFER   *ppAllHits,
  _Out_       DWORD          *pCountOfHits
);
```



## <a name="parameters"></a><span data-ttu-id="92109-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="92109-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92109-107">*pMesh* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="92109-107">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92109-108">Tipo: **[ **LPD3DXBASEMESH**](id3dxbasemesh.md)**</span><span class="sxs-lookup"><span data-stu-id="92109-108">Type: **[**LPD3DXBASEMESH**](id3dxbasemesh.md)**</span></span>

<span data-ttu-id="92109-109">Puntatore a un'interfaccia [**ID3DXBaseMesh**](id3dxbasemesh.md) , che rappresenta la mesh da testare.</span><span class="sxs-lookup"><span data-stu-id="92109-109">Pointer to an [**ID3DXBaseMesh**](id3dxbasemesh.md) interface, representing the mesh to be tested.</span></span>

</dd> <dt>

<span data-ttu-id="92109-110">*pRayPos* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="92109-110">*pRayPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92109-111">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="92109-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="92109-112">Puntatore a una struttura [**D3DXVECTOR3**](d3dxvector3.md) , che specifica il punto in cui inizia il raggio.</span><span class="sxs-lookup"><span data-stu-id="92109-112">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the point where the ray begins.</span></span>

</dd> <dt>

<span data-ttu-id="92109-113">*pRayDir* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="92109-113">*pRayDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92109-114">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="92109-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="92109-115">Puntatore a una struttura [**D3DXVECTOR3**](d3dxvector3.md) , che specifica la direzione del raggio.</span><span class="sxs-lookup"><span data-stu-id="92109-115">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the direction of the ray.</span></span>

</dd> <dt>

<span data-ttu-id="92109-116">*pHit* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="92109-116">*pHit* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="92109-117">Tipo: **[ **bool**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="92109-117">Type: **[**BOOL**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="92109-118">Puntatore a un BOOL.</span><span class="sxs-lookup"><span data-stu-id="92109-118">Pointer to a BOOL.</span></span> <span data-ttu-id="92109-119">Se il raggio interseca un quadrante triangolare sulla mesh, questo valore verrà impostato su **true**.</span><span class="sxs-lookup"><span data-stu-id="92109-119">If the ray intersects a triangular face on the mesh, this value will be set to **TRUE**.</span></span> <span data-ttu-id="92109-120">In caso contrario, questo valore è impostato su **false**.</span><span class="sxs-lookup"><span data-stu-id="92109-120">Otherwise, this value is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="92109-121">*pFaceIndex* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="92109-121">*pFaceIndex* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="92109-122">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="92109-122">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="92109-123">Puntatore a un valore di indice della faccia più vicina all'origine del raggio, se pHit è **true**.</span><span class="sxs-lookup"><span data-stu-id="92109-123">Pointer to an index value of the face closest to the ray origin, if pHit is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="92109-124">unità di *elaborazione* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="92109-124">*pU* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="92109-125">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="92109-125">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="92109-126">Puntatore a una coordinata baricentrica hit, U.</span><span class="sxs-lookup"><span data-stu-id="92109-126">Pointer to a barycentric hit coordinate, U.</span></span>

</dd> <dt>

<span data-ttu-id="92109-127">*PV* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="92109-127">*pV* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="92109-128">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="92109-128">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="92109-129">Puntatore a una coordinata baricentrica hit, V.</span><span class="sxs-lookup"><span data-stu-id="92109-129">Pointer to a barycentric hit coordinate, V.</span></span>

</dd> <dt>

<span data-ttu-id="92109-130">*pDist* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="92109-130">*pDist* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="92109-131">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="92109-131">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="92109-132">Puntatore alla distanza del parametro di intersezione del raggio.</span><span class="sxs-lookup"><span data-stu-id="92109-132">Pointer to a ray intersection parameter distance.</span></span>

</dd> <dt>

<span data-ttu-id="92109-133">*ppAllHits* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="92109-133">*ppAllHits* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="92109-134">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="92109-134">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="92109-135">Puntatore a un oggetto [**ID3DXBuffer**](id3dxbuffer.md) che contiene una matrice di strutture [**D3DXINTERSECTINFO**](d3dxintersectinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="92109-135">Pointer to an [**ID3DXBuffer**](id3dxbuffer.md) object, containing an array of [**D3DXINTERSECTINFO**](d3dxintersectinfo.md) structures.</span></span>

</dd> <dt>

<span data-ttu-id="92109-136">*pCountOfHits* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="92109-136">*pCountOfHits* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="92109-137">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="92109-137">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="92109-138">Puntatore a un valore DWORD che contiene il numero di voci nella matrice ppAllHits.</span><span class="sxs-lookup"><span data-stu-id="92109-138">Pointer to a DWORD that contains the number of entries in the ppAllHits array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92109-139">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="92109-139">Return value</span></span>

<span data-ttu-id="92109-140">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="92109-140">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="92109-141">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="92109-141">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="92109-142">Se la funzione ha esito negativo, il valore restituito può essere: E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="92109-142">If the function fails, the return value can be: E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="92109-143">Commenti</span><span class="sxs-lookup"><span data-stu-id="92109-143">Remarks</span></span>

<span data-ttu-id="92109-144">La funzione **D3DXIntersect** fornisce un modo per comprendere i punti in e intorno a un triangolo, indipendentemente dalla posizione in cui si trova effettivamente il triangolo.</span><span class="sxs-lookup"><span data-stu-id="92109-144">The **D3DXIntersect** function provides a way to understand points in and around a triangle, independent of where the triangle is actually located.</span></span> <span data-ttu-id="92109-145">Questa funzione restituisce il punto risultante utilizzando l'equazione seguente: V1 + U (v2-v1) + V (V3-V1).</span><span class="sxs-lookup"><span data-stu-id="92109-145">This function returns the resulting point by using the following equation: V1 + U(V2 - V1) + V(V3 - V1).</span></span>

<span data-ttu-id="92109-146">Qualsiasi punto nel V1V2V3 del piano può essere rappresentato dalla coordinata baricentrica (U, V).</span><span class="sxs-lookup"><span data-stu-id="92109-146">Any point in the plane V1V2V3 can be represented by the barycentric coordinate (U,V).</span></span> <span data-ttu-id="92109-147">Il parametro U controlla la quantità di V2 che viene ponderata nel risultato e il parametro V controlla la quantità di V3 che viene ponderata nel risultato.</span><span class="sxs-lookup"><span data-stu-id="92109-147">The parameter U controls how much V2 gets weighted into the result, and the parameter V controls how much V3 gets weighted into the result.</span></span> <span data-ttu-id="92109-148">Infine, il valore \[ 1-(U + V) controlla la \] quantità di V1 che viene ponderata nel risultato.</span><span class="sxs-lookup"><span data-stu-id="92109-148">Lastly, the value of \[1 - (U + V)\] controls how much V1 gets weighted into the result.</span></span>

<span data-ttu-id="92109-149">Le coordinate baricentrica sono costituite da coordinate generali.</span><span class="sxs-lookup"><span data-stu-id="92109-149">Barycentric coordinates are a form of general coordinates.</span></span> <span data-ttu-id="92109-150">In questo contesto, l'utilizzo delle coordinate baricentrica rappresenta una modifica nei sistemi di coordinate.</span><span class="sxs-lookup"><span data-stu-id="92109-150">In this context, using barycentric coordinates represents a change in coordinate systems.</span></span> <span data-ttu-id="92109-151">Ciò che è valido per le coordinate cartesiane è valido per le coordinate baricentrica.</span><span class="sxs-lookup"><span data-stu-id="92109-151">What holds true for Cartesian coordinates holds true for barycentric coordinates.</span></span>

<span data-ttu-id="92109-152">Le coordinate baricentrica definiscono un punto all'interno di un triangolo in termini di vertici del triangolo.</span><span class="sxs-lookup"><span data-stu-id="92109-152">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="92109-153">Per una descrizione più approfondita delle coordinate baricentrica, vedere [la descrizione delle coordinate baricentrica di articolo MathWorld](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span><span class="sxs-lookup"><span data-stu-id="92109-153">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="92109-154">Requisiti</span><span class="sxs-lookup"><span data-stu-id="92109-154">Requirements</span></span>



| <span data-ttu-id="92109-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="92109-155">Requirement</span></span> | <span data-ttu-id="92109-156">Valore</span><span class="sxs-lookup"><span data-stu-id="92109-156">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="92109-157">Intestazione</span><span class="sxs-lookup"><span data-stu-id="92109-157">Header</span></span><br/>  | <dl> <span data-ttu-id="92109-158"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="92109-158"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="92109-159">Libreria</span><span class="sxs-lookup"><span data-stu-id="92109-159">Library</span></span><br/> | <dl> <span data-ttu-id="92109-160"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="92109-160"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="92109-161">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="92109-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92109-162">Funzioni mesh</span><span class="sxs-lookup"><span data-stu-id="92109-162">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
