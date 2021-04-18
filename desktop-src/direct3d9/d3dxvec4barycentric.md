---
description: Restituisce un punto nelle coordinate baricentrica, usando i vettori 4D specificati.
ms.assetid: 80d73232-76bf-4f40-add2-dd1bdcc5cd98
title: Funzione D3DXVec4BaryCentric (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4BaryCentric
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 75f0d068d1545f1b8b55dc3b976d3585e6f9bc88
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322862"
---
# <a name="d3dxvec4barycentric-function-d3dx9mathh"></a><span data-ttu-id="a70ef-103">Funzione D3DXVec4BaryCentric (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="a70ef-103">D3DXVec4BaryCentric function (D3dx9math.h)</span></span>

<span data-ttu-id="a70ef-104">Restituisce un punto nelle coordinate baricentrica, usando i vettori 4D specificati.</span><span class="sxs-lookup"><span data-stu-id="a70ef-104">Returns a point in Barycentric coordinates, using the specified 4D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="a70ef-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a70ef-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4BaryCentric(
  _Out_       D3DXVECTOR4 *pOut,
  _In_  const D3DXVECTOR4 *pV1,
  _In_  const D3DXVECTOR4 *pV2,
  _In_  const D3DXVECTOR4 *pV3,
  _In_        FLOAT       f,
  _In_        FLOAT       g
);
```



## <a name="parameters"></a><span data-ttu-id="a70ef-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a70ef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a70ef-107">*broncio* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a70ef-107">*pOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a70ef-108">Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="a70ef-108">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="a70ef-109">Puntatore alla struttura [**D3DXVECTOR4**](d3dxvector4.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="a70ef-109">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="a70ef-110">*pV1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a70ef-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a70ef-111">Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="a70ef-111">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="a70ef-112">Puntatore a una struttura [**D3DXVECTOR4**](d3dxvector4.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="a70ef-112">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="a70ef-113">*pV2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a70ef-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a70ef-114">Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="a70ef-114">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="a70ef-115">Puntatore a una struttura [**D3DXVECTOR4**](d3dxvector4.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="a70ef-115">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="a70ef-116">*pV3* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a70ef-116">*pV3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a70ef-117">Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="a70ef-117">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="a70ef-118">Puntatore a una struttura [**D3DXVECTOR4**](d3dxvector4.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="a70ef-118">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="a70ef-119">*f* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a70ef-119">*f* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a70ef-120">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a70ef-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a70ef-121">Fattore di ponderazione.</span><span class="sxs-lookup"><span data-stu-id="a70ef-121">Weighting factor.</span></span> <span data-ttu-id="a70ef-122">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="a70ef-122">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="a70ef-123">*g* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a70ef-123">*g* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a70ef-124">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a70ef-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a70ef-125">Fattore di ponderazione.</span><span class="sxs-lookup"><span data-stu-id="a70ef-125">Weighting factor.</span></span> <span data-ttu-id="a70ef-126">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="a70ef-126">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a70ef-127">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a70ef-127">Return value</span></span>

<span data-ttu-id="a70ef-128">Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="a70ef-128">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="a70ef-129">Puntatore a una struttura [**D3DXVECTOR4**](d3dxvector4.md) nelle coordinate di baricentrica.</span><span class="sxs-lookup"><span data-stu-id="a70ef-129">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure in Barycentric coordinates.</span></span>

## <a name="remarks"></a><span data-ttu-id="a70ef-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="a70ef-130">Remarks</span></span>

<span data-ttu-id="a70ef-131">La funzione **D3DXVec4BaryCentric** fornisce un modo per comprendere i punti in e intorno a un triangolo, indipendentemente dalla posizione in cui si trova effettivamente il triangolo.</span><span class="sxs-lookup"><span data-stu-id="a70ef-131">The **D3DXVec4BaryCentric** function provides a way to understand points in and around a triangle, independent of where the triangle is actually located.</span></span> <span data-ttu-id="a70ef-132">Questa funzione restituisce il punto risultante utilizzando l'equazione seguente: V1 + f (v2-v1) + g (V3-V1).</span><span class="sxs-lookup"><span data-stu-id="a70ef-132">This function returns the resulting point by using the following equation: V1 + f(V2-V1) + g(V3-V1).</span></span>

<span data-ttu-id="a70ef-133">Qualsiasi punto nel V1V2V3 del piano può essere rappresentato dalla coordinata baricentrica (f, g). Il parametro *f* controlla la quantità di V2 che viene ponderata nel risultato e il parametro *g* controlla la quantità di V3 che viene ponderata nel risultato.</span><span class="sxs-lookup"><span data-stu-id="a70ef-133">Any point in the plane V1V2V3 can be represented by the Barycentric coordinate (f,g).The parameter *f* controls how much V2 gets weighted into the result and the parameter *g* controls how much V3 gets weighted into the result.</span></span> <span data-ttu-id="a70ef-134">Infine, 1-f-g controlla la quantità di V1 che viene ponderata nel risultato.</span><span class="sxs-lookup"><span data-stu-id="a70ef-134">Lastly, 1-f-g controls how much V1 gets weighted into the result.</span></span>

<span data-ttu-id="a70ef-135">Si notino le relazioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="a70ef-135">Note the following relations.</span></span>

-   <span data-ttu-id="a70ef-136">Se (f>= 0 &, & g>= 0 &, & 1-f-g>= 0), il punto si trova all'interno del triangolo V1V2V3.</span><span class="sxs-lookup"><span data-stu-id="a70ef-136">If (f>=0 &, & g>=0 &, & 1-f-g>=0), the point is inside the triangle V1V2V3.</span></span>
-   <span data-ttu-id="a70ef-137">Se (f = = 0 &, & g>= 0 &, & 1-f-g>= 0), il punto si trova nella riga V1V3.</span><span class="sxs-lookup"><span data-stu-id="a70ef-137">If (f==0 &, & g>=0 &, & 1-f-g>=0), the point is on the line V1V3.</span></span>
-   <span data-ttu-id="a70ef-138">Se (f>= 0 &, & g = = 0 &, & 1-f-g>= 0), il punto si trova nella riga V1V2.</span><span class="sxs-lookup"><span data-stu-id="a70ef-138">If (f>=0 &, & g==0 &, & 1-f-g>=0), the point is on the line V1V2.</span></span>
-   <span data-ttu-id="a70ef-139">Se (f>= 0 &, & g>= 0 &, & 1-f-g = = 0), il punto si trova nella riga V2V3.</span><span class="sxs-lookup"><span data-stu-id="a70ef-139">If (f>=0 &, & g>=0 &, & 1-f-g==0), the point is on the line V2V3.</span></span>

<span data-ttu-id="a70ef-140">Le coordinate baricentrica sono costituite da coordinate generali.</span><span class="sxs-lookup"><span data-stu-id="a70ef-140">Barycentric coordinates are a form of general coordinates.</span></span> <span data-ttu-id="a70ef-141">In questo contesto, l'utilizzo delle coordinate baricentrica rappresenta una modifica nei sistemi di coordinate.</span><span class="sxs-lookup"><span data-stu-id="a70ef-141">In this context, using Barycentric coordinates represents a change in coordinate systems.</span></span> <span data-ttu-id="a70ef-142">Ciò che è valido per le coordinate cartesiane è valido per le coordinate baricentrica.</span><span class="sxs-lookup"><span data-stu-id="a70ef-142">What holds true for Cartesian coordinates holds true for Barycentric coordinates.</span></span>

<span data-ttu-id="a70ef-143">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro *broncio* .</span><span class="sxs-lookup"><span data-stu-id="a70ef-143">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="a70ef-144">In questo modo, la funzione **D3DXVec4BaryCentric** può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="a70ef-144">In this way, the **D3DXVec4BaryCentric** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="a70ef-145">Le coordinate baricentrica definiscono un punto all'interno di un triangolo in termini di vertici del triangolo.</span><span class="sxs-lookup"><span data-stu-id="a70ef-145">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="a70ef-146">Per una descrizione più approfondita delle coordinate baricentrica, vedere [la descrizione delle coordinate baricentrica di articolo MathWorld](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span><span class="sxs-lookup"><span data-stu-id="a70ef-146">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="a70ef-147">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a70ef-147">Requirements</span></span>



| <span data-ttu-id="a70ef-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="a70ef-148">Requirement</span></span> | <span data-ttu-id="a70ef-149">Valore</span><span class="sxs-lookup"><span data-stu-id="a70ef-149">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a70ef-150">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a70ef-150">Header</span></span><br/>  | <dl> <span data-ttu-id="a70ef-151"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="a70ef-151"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="a70ef-152">Libreria</span><span class="sxs-lookup"><span data-stu-id="a70ef-152">Library</span></span><br/> | <dl> <span data-ttu-id="a70ef-153"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a70ef-153"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a70ef-154">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a70ef-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a70ef-155">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="a70ef-155">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
