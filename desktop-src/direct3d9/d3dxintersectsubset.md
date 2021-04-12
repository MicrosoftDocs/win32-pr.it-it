---
description: Interseca il raggio specificato con il subset di mesh specificato. Questo fornisce funzionalità simili a D3DXIntersect.
ms.assetid: 4a757b9e-18eb-424e-9f3e-cdf917c23787
title: Funzione D3DXIntersectSubset (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXIntersectSubset
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 621f45d7c2a6d8ff162f539ef62153d3ae70f6e9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235013"
---
# <a name="d3dxintersectsubset-function"></a><span data-ttu-id="f118e-104">D3DXIntersectSubset (funzione)</span><span class="sxs-lookup"><span data-stu-id="f118e-104">D3DXIntersectSubset function</span></span>

<span data-ttu-id="f118e-105">Interseca il raggio specificato con il subset di mesh specificato.</span><span class="sxs-lookup"><span data-stu-id="f118e-105">Intersects the specified ray with the given mesh subset.</span></span> <span data-ttu-id="f118e-106">Questo fornisce funzionalità simili a [**D3DXIntersect**](d3dxintersect.md).</span><span class="sxs-lookup"><span data-stu-id="f118e-106">This provides similar functionality to [**D3DXIntersect**](d3dxintersect.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f118e-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f118e-107">Syntax</span></span>


```C++
HRESULT D3DXIntersectSubset(
  _In_        LPD3DXBASEMESH pMesh,
  _In_        DWORD          AttribId,
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



## <a name="parameters"></a><span data-ttu-id="f118e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="f118e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f118e-109">*pMesh* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f118e-109">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f118e-110">Tipo: **[ **LPD3DXBASEMESH**](id3dxbasemesh.md)**</span><span class="sxs-lookup"><span data-stu-id="f118e-110">Type: **[**LPD3DXBASEMESH**](id3dxbasemesh.md)**</span></span>

<span data-ttu-id="f118e-111">Puntatore a un'interfaccia [**ID3DXBaseMesh**](id3dxbasemesh.md) , che rappresenta la mesh da testare.</span><span class="sxs-lookup"><span data-stu-id="f118e-111">Pointer to an [**ID3DXBaseMesh**](id3dxbasemesh.md) interface, representing the mesh to be tested.</span></span> <span data-ttu-id="f118e-112">La mesh deve essere ordinata come attributo.</span><span class="sxs-lookup"><span data-stu-id="f118e-112">The mesh must be attribute sorted.</span></span>

</dd> <dt>

<span data-ttu-id="f118e-113">*AttribId* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f118e-113">*AttribId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f118e-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f118e-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f118e-115">Identificatore dell'attributo del subset da intersecare con.</span><span class="sxs-lookup"><span data-stu-id="f118e-115">Attribute identifier of the subset to intersect with.</span></span>

</dd> <dt>

<span data-ttu-id="f118e-116">*pRayPos* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f118e-116">*pRayPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f118e-117">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="f118e-117">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="f118e-118">Puntatore a una struttura [**D3DXVECTOR3**](d3dxvector3.md) , che specifica il punto in cui inizia il raggio.</span><span class="sxs-lookup"><span data-stu-id="f118e-118">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the point where the ray begins.</span></span>

</dd> <dt>

<span data-ttu-id="f118e-119">*pRayDir* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f118e-119">*pRayDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f118e-120">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="f118e-120">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="f118e-121">Puntatore a una struttura [**D3DXVECTOR3**](d3dxvector3.md) , che specifica la direzione del raggio.</span><span class="sxs-lookup"><span data-stu-id="f118e-121">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the direction of the ray.</span></span>

</dd> <dt>

<span data-ttu-id="f118e-122">*pHit* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f118e-122">*pHit* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f118e-123">Tipo: **[ **bool**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="f118e-123">Type: **[**BOOL**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="f118e-124">Puntatore a un BOOL.</span><span class="sxs-lookup"><span data-stu-id="f118e-124">Pointer to a BOOL.</span></span> <span data-ttu-id="f118e-125">Se il raggio interseca un quadrante triangolare sulla mesh, questo valore verrà impostato su **true**.</span><span class="sxs-lookup"><span data-stu-id="f118e-125">If the ray intersects a triangular face on the mesh, this value will be set to **TRUE**.</span></span> <span data-ttu-id="f118e-126">In caso contrario, questo valore è impostato su **false**.</span><span class="sxs-lookup"><span data-stu-id="f118e-126">Otherwise, this value is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="f118e-127">*pFaceIndex* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f118e-127">*pFaceIndex* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f118e-128">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="f118e-128">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="f118e-129">Puntatore a un valore di indice della faccia più vicina all'origine del raggio, se pHit è **true**.</span><span class="sxs-lookup"><span data-stu-id="f118e-129">Pointer to an index value of the face closest to the ray origin, if pHit is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="f118e-130">unità di *elaborazione* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f118e-130">*pU* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f118e-131">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="f118e-131">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="f118e-132">Puntatore a una coordinata baricentrica hit, U.</span><span class="sxs-lookup"><span data-stu-id="f118e-132">Pointer to a barycentric hit coordinate, U.</span></span>

</dd> <dt>

<span data-ttu-id="f118e-133">*PV* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f118e-133">*pV* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f118e-134">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="f118e-134">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="f118e-135">Puntatore a una coordinata baricentrica hit, V.</span><span class="sxs-lookup"><span data-stu-id="f118e-135">Pointer to a barycentric hit coordinate, V.</span></span>

</dd> <dt>

<span data-ttu-id="f118e-136">*pDist* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f118e-136">*pDist* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f118e-137">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="f118e-137">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="f118e-138">Puntatore alla distanza del parametro di intersezione del raggio.</span><span class="sxs-lookup"><span data-stu-id="f118e-138">Pointer to a ray intersection parameter distance.</span></span>

</dd> <dt>

<span data-ttu-id="f118e-139">*ppAllHits* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f118e-139">*ppAllHits* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f118e-140">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="f118e-140">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="f118e-141">Matrice di strutture [**D3DXINTERSECTINFO**](d3dxintersectinfo.md) , che rappresenta tutti i riscontri, non solo i riscontri più vicini.</span><span class="sxs-lookup"><span data-stu-id="f118e-141">Array of [**D3DXINTERSECTINFO**](d3dxintersectinfo.md) structures, representing all hits, not just closest hits.</span></span>

</dd> <dt>

<span data-ttu-id="f118e-142">*pCountOfHits* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f118e-142">*pCountOfHits* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f118e-143">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="f118e-143">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="f118e-144">Numero di elementi nella matrice restituiti da ppAllHits.</span><span class="sxs-lookup"><span data-stu-id="f118e-144">Number of elements in the array returned from ppAllHits.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f118e-145">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f118e-145">Return value</span></span>

<span data-ttu-id="f118e-146">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f118e-146">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f118e-147">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f118e-147">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="f118e-148">Se la funzione ha esito negativo, il valore restituito può essere il valore seguente: E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="f118e-148">If the function fails, the return value can be the following value: E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="f118e-149">Commenti</span><span class="sxs-lookup"><span data-stu-id="f118e-149">Remarks</span></span>

<span data-ttu-id="f118e-150">La funzione **D3DXIntersectSubset** fornisce un modo per comprendere i punti in e intorno a un triangolo, indipendentemente dalla posizione in cui si trova effettivamente il triangolo.</span><span class="sxs-lookup"><span data-stu-id="f118e-150">The **D3DXIntersectSubset** function provides a way to understand points in and around a triangle, independent of where the triangle is actually located.</span></span> <span data-ttu-id="f118e-151">Questa funzione restituisce il punto risultante utilizzando l'equazione seguente: V1 + U (v2-v1) + V (V3-V1).</span><span class="sxs-lookup"><span data-stu-id="f118e-151">This function returns the resulting point by using the following equation: V1 + U(V2 - V1) + V(V3 - V1).</span></span>

<span data-ttu-id="f118e-152">Qualsiasi punto nel V1V2V3 del piano può essere rappresentato dalla coordinata baricentrica (U, V).</span><span class="sxs-lookup"><span data-stu-id="f118e-152">Any point in the plane V1V2V3 can be represented by the barycentric coordinate (U,V).</span></span> <span data-ttu-id="f118e-153">Il parametro U controlla la quantità di V2 che viene ponderata nel risultato e il parametro V controlla la quantità di V3 che viene ponderata nel risultato.</span><span class="sxs-lookup"><span data-stu-id="f118e-153">The parameter U controls how much V2 gets weighted into the result and the parameter V controls how much V3 gets weighted into the result.</span></span> <span data-ttu-id="f118e-154">Infine, il valore \[ 1-(U + V) controlla la \] quantità di V1 che viene ponderata nel risultato.</span><span class="sxs-lookup"><span data-stu-id="f118e-154">Lastly, the value of \[1 - (U + V)\] controls how much V1 gets weighted into the result.</span></span>

<span data-ttu-id="f118e-155">Le coordinate baricentrica sono costituite da coordinate generali.</span><span class="sxs-lookup"><span data-stu-id="f118e-155">Barycentric coordinates are a form of general coordinates.</span></span> <span data-ttu-id="f118e-156">In questo contesto, l'utilizzo delle coordinate baricentrica rappresenta una modifica nei sistemi di coordinate.</span><span class="sxs-lookup"><span data-stu-id="f118e-156">In this context, using barycentric coordinates represents a change in coordinate systems.</span></span> <span data-ttu-id="f118e-157">Ciò che è valido per le coordinate cartesiane è valido per le coordinate baricentrica.</span><span class="sxs-lookup"><span data-stu-id="f118e-157">What holds true for Cartesian coordinates holds true for barycentric coordinates.</span></span>

<span data-ttu-id="f118e-158">Le coordinate baricentrica definiscono un punto all'interno di un triangolo in termini di vertici del triangolo.</span><span class="sxs-lookup"><span data-stu-id="f118e-158">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="f118e-159">Per una descrizione più approfondita delle coordinate baricentrica, vedere [la descrizione delle coordinate baricentrica di articolo MathWorld](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span><span class="sxs-lookup"><span data-stu-id="f118e-159">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="f118e-160">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f118e-160">Requirements</span></span>



| <span data-ttu-id="f118e-161">Requisito</span><span class="sxs-lookup"><span data-stu-id="f118e-161">Requirement</span></span> | <span data-ttu-id="f118e-162">Valore</span><span class="sxs-lookup"><span data-stu-id="f118e-162">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f118e-163">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f118e-163">Header</span></span><br/>  | <dl> <span data-ttu-id="f118e-164"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="f118e-164"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="f118e-165">Libreria</span><span class="sxs-lookup"><span data-stu-id="f118e-165">Library</span></span><br/> | <dl> <span data-ttu-id="f118e-166"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f118e-166"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f118e-167">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f118e-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f118e-168">Funzioni mesh</span><span class="sxs-lookup"><span data-stu-id="f118e-168">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
