---
description: Determina se un raggio si interseca con la mesh.
ms.assetid: 74565d4a-94e6-4faa-bf70-9c1b35e5e5d8
title: Metodo ID3DX10Mesh::Intersect (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.Intersect
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 8ceed03ab21debf61371da9e53b5150d2dc83e4a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322747"
---
# <a name="id3dx10meshintersect-method"></a><span data-ttu-id="c76c6-103">Metodo ID3DX10Mesh:: Intersect</span><span class="sxs-lookup"><span data-stu-id="c76c6-103">ID3DX10Mesh::Intersect method</span></span>

<span data-ttu-id="c76c6-104">Determina se un raggio si interseca con la mesh.</span><span class="sxs-lookup"><span data-stu-id="c76c6-104">Determines if a ray intersects with this mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="c76c6-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c76c6-105">Syntax</span></span>


```C++
HRESULT Intersect(
  [in]  D3DXVECTOR3 *pRayPos,
  [in]  D3DXVECTOR3 *pRayDir,
  [in]  UINT        *pHitCount,
  [in]  UINT        *pFaceIndex,
  [in]  float       *pU,
  [in]  float       *pV,
  [in]  float       *pDist,
  [out] ID3D10Blob  **ppAllHits
);
```



## <a name="parameters"></a><span data-ttu-id="c76c6-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c76c6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c76c6-107">*pRayPos* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c76c6-107">*pRayPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c76c6-108">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="c76c6-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="c76c6-109">Puntatore a una struttura [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , che specifica il punto in cui inizia il raggio.</span><span class="sxs-lookup"><span data-stu-id="c76c6-109">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, specifying the point where the ray begins.</span></span>

</dd> <dt>

<span data-ttu-id="c76c6-110">*pRayDir* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c76c6-110">*pRayDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c76c6-111">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="c76c6-111">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="c76c6-112">Puntatore a una struttura [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , che specifica la direzione del raggio.</span><span class="sxs-lookup"><span data-stu-id="c76c6-112">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, specifying the direction of the ray.</span></span>

</dd> <dt>

<span data-ttu-id="c76c6-113">*pHitCount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c76c6-113">*pHitCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c76c6-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="c76c6-114">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="c76c6-115">Numero di volte in cui il raggio è stato intersecato con la mesh.</span><span class="sxs-lookup"><span data-stu-id="c76c6-115">The number of times the ray intersected with the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="c76c6-116">*pFaceIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c76c6-116">*pFaceIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c76c6-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="c76c6-117">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="c76c6-118">Puntatore a un valore di indice della faccia più vicina all'origine del raggio, se pHit è **true**.</span><span class="sxs-lookup"><span data-stu-id="c76c6-118">Pointer to an index value of the face closest to the ray origin, if pHit is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="c76c6-119">unità di *elaborazione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c76c6-119">*pU* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c76c6-120">Tipo: **float \***</span><span class="sxs-lookup"><span data-stu-id="c76c6-120">Type: **float\***</span></span>

<span data-ttu-id="c76c6-121">Puntatore a una coordinata baricentrica hit, U.</span><span class="sxs-lookup"><span data-stu-id="c76c6-121">Pointer to a barycentric hit coordinate, U.</span></span>

</dd> <dt>

<span data-ttu-id="c76c6-122">*PV* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c76c6-122">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c76c6-123">Tipo: **float \***</span><span class="sxs-lookup"><span data-stu-id="c76c6-123">Type: **float\***</span></span>

<span data-ttu-id="c76c6-124">Puntatore a una coordinata baricentrica hit, V.</span><span class="sxs-lookup"><span data-stu-id="c76c6-124">Pointer to a barycentric hit coordinate, V.</span></span>

</dd> <dt>

<span data-ttu-id="c76c6-125">*pDist* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c76c6-125">*pDist* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c76c6-126">Tipo: **float \***</span><span class="sxs-lookup"><span data-stu-id="c76c6-126">Type: **float\***</span></span>

<span data-ttu-id="c76c6-127">Puntatore alla distanza del parametro di intersezione del raggio.</span><span class="sxs-lookup"><span data-stu-id="c76c6-127">Pointer to a ray intersection parameter distance.</span></span>

</dd> <dt>

<span data-ttu-id="c76c6-128">*ppAllHits* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="c76c6-128">*ppAllHits* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c76c6-129">Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="c76c6-129">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="c76c6-130">Puntatore a un' [**interfaccia ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)contenente una matrice di strutture [**di \_ \_ informazioni di intersezione d3dx10**](d3dx10-intersect-info.md) .</span><span class="sxs-lookup"><span data-stu-id="c76c6-130">Pointer to an [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob), containing an array of [**D3DX10\_INTERSECT\_INFO**](d3dx10-intersect-info.md) structures.</span></span> <span data-ttu-id="c76c6-131">Si tratta di un elenco di tutti i riscontri che si sono verificati nel test di intersezione.</span><span class="sxs-lookup"><span data-stu-id="c76c6-131">This is a list of all the hits that occurred in the intersection test.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c76c6-132">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c76c6-132">Return value</span></span>

<span data-ttu-id="c76c6-133">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c76c6-133">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c76c6-134">Il valore restituito è uno dei valori elencati in [codici restituiti Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="c76c6-134">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c76c6-135">Commenti</span><span class="sxs-lookup"><span data-stu-id="c76c6-135">Remarks</span></span>

<span data-ttu-id="c76c6-136">Questa API fornisce un modo per comprendere i punti in e intorno a un triangolo, indipendentemente dalla posizione in cui si trova effettivamente il triangolo.</span><span class="sxs-lookup"><span data-stu-id="c76c6-136">This API provides a way to understand points in and around a triangle, independent of where the triangle is actually located.</span></span> <span data-ttu-id="c76c6-137">Questa funzione restituisce il punto risultante utilizzando l'equazione seguente: V1 + U (v2-v1) + V (V3-V1).</span><span class="sxs-lookup"><span data-stu-id="c76c6-137">This function returns the resulting point by using the following equation: V1 + U(V2 - V1) + V(V3 - V1).</span></span>

<span data-ttu-id="c76c6-138">Qualsiasi punto nel V1V2V3 del piano può essere rappresentato dalla coordinata baricentrica (U, V).</span><span class="sxs-lookup"><span data-stu-id="c76c6-138">Any point in the plane V1V2V3 can be represented by the barycentric coordinate (U,V).</span></span> <span data-ttu-id="c76c6-139">Il parametro U controlla la quantità di V2 che viene ponderata nel risultato e il parametro V controlla la quantità di V3 che viene ponderata nel risultato.</span><span class="sxs-lookup"><span data-stu-id="c76c6-139">The parameter U controls how much V2 gets weighted into the result, and the parameter V controls how much V3 gets weighted into the result.</span></span> <span data-ttu-id="c76c6-140">Infine, il valore \[ 1-(U + V) controlla la \] quantità di V1 che viene ponderata nel risultato.</span><span class="sxs-lookup"><span data-stu-id="c76c6-140">Lastly, the value of \[1 - (U + V)\] controls how much V1 gets weighted into the result.</span></span>

<span data-ttu-id="c76c6-141">Le coordinate baricentrica sono costituite da coordinate generali.</span><span class="sxs-lookup"><span data-stu-id="c76c6-141">Barycentric coordinates are a form of general coordinates.</span></span> <span data-ttu-id="c76c6-142">In questo contesto, l'utilizzo delle coordinate baricentrica rappresenta una modifica nei sistemi di coordinate.</span><span class="sxs-lookup"><span data-stu-id="c76c6-142">In this context, using barycentric coordinates represents a change in coordinate systems.</span></span> <span data-ttu-id="c76c6-143">Ciò che è valido per le coordinate cartesiane è valido per le coordinate baricentrica.</span><span class="sxs-lookup"><span data-stu-id="c76c6-143">What holds true for Cartesian coordinates holds true for barycentric coordinates.</span></span>

<span data-ttu-id="c76c6-144">Le coordinate baricentrica definiscono un punto all'interno di un triangolo in termini di vertici del triangolo.</span><span class="sxs-lookup"><span data-stu-id="c76c6-144">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="c76c6-145">Per una descrizione più approfondita delle coordinate baricentrica, vedere [la descrizione delle coordinate baricentrica di articolo MathWorld](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span><span class="sxs-lookup"><span data-stu-id="c76c6-145">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="c76c6-146">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c76c6-146">Requirements</span></span>



| <span data-ttu-id="c76c6-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="c76c6-147">Requirement</span></span> | <span data-ttu-id="c76c6-148">Valore</span><span class="sxs-lookup"><span data-stu-id="c76c6-148">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c76c6-149">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c76c6-149">Header</span></span><br/>  | <dl> <span data-ttu-id="c76c6-150"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="c76c6-150"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="c76c6-151">Libreria</span><span class="sxs-lookup"><span data-stu-id="c76c6-151">Library</span></span><br/> | <dl> <span data-ttu-id="c76c6-152"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c76c6-152"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c76c6-153">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c76c6-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c76c6-154">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="c76c6-154">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="c76c6-155">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="c76c6-155">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
