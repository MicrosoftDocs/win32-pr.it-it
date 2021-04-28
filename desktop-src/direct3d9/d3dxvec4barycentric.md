---
description: 'Funzione D3DXVec4BaryCentric (D3dx9math.h): restituisce un punto in coordinate barycentriche, usando i vettori 4D specificati.'
ms.assetid: 80d73232-76bf-4f40-add2-dd1bdcc5cd98
title: Funzione D3DXVec4BaryCentric (D3dx9math.h)
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
ms.openlocfilehash: 643773fe2be45bbae5709dcd7efaeae5fd4b86d5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097709"
---
# <a name="d3dxvec4barycentric-function-d3dx9mathh"></a><span data-ttu-id="1cfea-103">Funzione D3DXVec4BaryCentric (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="1cfea-103">D3DXVec4BaryCentric function (D3dx9math.h)</span></span>

<span data-ttu-id="1cfea-104">Restituisce un punto in coordinate barycentriche, usando i vettori 4D specificati.</span><span class="sxs-lookup"><span data-stu-id="1cfea-104">Returns a point in Barycentric coordinates, using the specified 4D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="1cfea-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1cfea-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="1cfea-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1cfea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1cfea-107">*pOut* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="1cfea-107">*pOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1cfea-108">Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="1cfea-108">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="1cfea-109">Puntatore alla [**struttura D3DXVECTOR4**](d3dxvector4.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="1cfea-109">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="1cfea-110">*pV1* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="1cfea-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cfea-111">Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="1cfea-111">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="1cfea-112">Puntatore a una [**struttura D3DXVECTOR4 di**](d3dxvector4.md) origine.</span><span class="sxs-lookup"><span data-stu-id="1cfea-112">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="1cfea-113">*pV2* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="1cfea-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cfea-114">Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="1cfea-114">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="1cfea-115">Puntatore a una [**struttura D3DXVECTOR4 di**](d3dxvector4.md) origine.</span><span class="sxs-lookup"><span data-stu-id="1cfea-115">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="1cfea-116">*pV3* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="1cfea-116">*pV3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cfea-117">Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="1cfea-117">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="1cfea-118">Puntatore a una [**struttura D3DXVECTOR4 di**](d3dxvector4.md) origine.</span><span class="sxs-lookup"><span data-stu-id="1cfea-118">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="1cfea-119">*f* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1cfea-119">*f* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cfea-120">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1cfea-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1cfea-121">Fattore di ponderazione.</span><span class="sxs-lookup"><span data-stu-id="1cfea-121">Weighting factor.</span></span> <span data-ttu-id="1cfea-122">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="1cfea-122">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="1cfea-123">*g* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1cfea-123">*g* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cfea-124">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1cfea-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1cfea-125">Fattore di ponderazione.</span><span class="sxs-lookup"><span data-stu-id="1cfea-125">Weighting factor.</span></span> <span data-ttu-id="1cfea-126">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="1cfea-126">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1cfea-127">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1cfea-127">Return value</span></span>

<span data-ttu-id="1cfea-128">Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="1cfea-128">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="1cfea-129">Puntatore a [**una struttura D3DXVECTOR4**](d3dxvector4.md) in coordinate barycentriche.</span><span class="sxs-lookup"><span data-stu-id="1cfea-129">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure in Barycentric coordinates.</span></span>

## <a name="remarks"></a><span data-ttu-id="1cfea-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="1cfea-130">Remarks</span></span>

<span data-ttu-id="1cfea-131">La **funzione D3DXVec4BaryCentric** consente di comprendere i punti all'interno e intorno a un triangolo, indipendentemente dalla posizione in cui si trova effettivamente il triangolo.</span><span class="sxs-lookup"><span data-stu-id="1cfea-131">The **D3DXVec4BaryCentric** function provides a way to understand points in and around a triangle, independent of where the triangle is actually located.</span></span> <span data-ttu-id="1cfea-132">Questa funzione restituisce il punto risultante usando l'equazione seguente: V1 + f(V2-V1) + g(V3-V1).</span><span class="sxs-lookup"><span data-stu-id="1cfea-132">This function returns the resulting point by using the following equation: V1 + f(V2-V1) + g(V3-V1).</span></span>

<span data-ttu-id="1cfea-133">Qualsiasi punto nel piano V1V2V3 può essere rappresentato dalla coordinata barycentric (f,g). Il parametro *f* controlla quanto V2 viene ponderato nel risultato e il parametro *g* controlla quanto V3 viene ponderato nel risultato.</span><span class="sxs-lookup"><span data-stu-id="1cfea-133">Any point in the plane V1V2V3 can be represented by the Barycentric coordinate (f,g).The parameter *f* controls how much V2 gets weighted into the result and the parameter *g* controls how much V3 gets weighted into the result.</span></span> <span data-ttu-id="1cfea-134">Infine, 1-f-g controlla quanto V1 viene ponderato nel risultato.</span><span class="sxs-lookup"><span data-stu-id="1cfea-134">Lastly, 1-f-g controls how much V1 gets weighted into the result.</span></span>

<span data-ttu-id="1cfea-135">Si notino le relazioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="1cfea-135">Note the following relations.</span></span>

-   <span data-ttu-id="1cfea-136">Se (f>=0 &, & g>=0 &, & 1-f-g>=0), il punto si trova all'interno del triangolo V1V2V3.</span><span class="sxs-lookup"><span data-stu-id="1cfea-136">If (f>=0 &, & g>=0 &, & 1-f-g>=0), the point is inside the triangle V1V2V3.</span></span>
-   <span data-ttu-id="1cfea-137">Se (f==0 &, & g>=0 &, & 1-f-g>=0), il punto si trova sulla riga V1V3.</span><span class="sxs-lookup"><span data-stu-id="1cfea-137">If (f==0 &, & g>=0 &, & 1-f-g>=0), the point is on the line V1V3.</span></span>
-   <span data-ttu-id="1cfea-138">Se (f>=0 &, & g==0 &, & 1-f-g>=0), il punto si trova sulla riga V1V2.</span><span class="sxs-lookup"><span data-stu-id="1cfea-138">If (f>=0 &, & g==0 &, & 1-f-g>=0), the point is on the line V1V2.</span></span>
-   <span data-ttu-id="1cfea-139">Se (f>=0 &, & g>=0 &, & 1-f-g==0), il punto si trova sulla riga V2V3.</span><span class="sxs-lookup"><span data-stu-id="1cfea-139">If (f>=0 &, & g>=0 &, & 1-f-g==0), the point is on the line V2V3.</span></span>

<span data-ttu-id="1cfea-140">Le coordinate barycentriche sono una forma di coordinate generali.</span><span class="sxs-lookup"><span data-stu-id="1cfea-140">Barycentric coordinates are a form of general coordinates.</span></span> <span data-ttu-id="1cfea-141">In questo contesto, l'uso di coordinate barycentric rappresenta una modifica nei sistemi di coordinate.</span><span class="sxs-lookup"><span data-stu-id="1cfea-141">In this context, using Barycentric coordinates represents a change in coordinate systems.</span></span> <span data-ttu-id="1cfea-142">Ciò che vale per le coordinate cartesiane è vero per le coordinate barycentriche.</span><span class="sxs-lookup"><span data-stu-id="1cfea-142">What holds true for Cartesian coordinates holds true for Barycentric coordinates.</span></span>

<span data-ttu-id="1cfea-143">Il valore restituito per questa funzione è lo stesso valore restituito nel *parametro pOut.*</span><span class="sxs-lookup"><span data-stu-id="1cfea-143">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="1cfea-144">In questo modo, la **funzione D3DXVec4BaryCentric** può essere usata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="1cfea-144">In this way, the **D3DXVec4BaryCentric** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="1cfea-145">Le coordinate barycentriche definiscono un punto all'interno di un triangolo in termini di vertici del triangolo.</span><span class="sxs-lookup"><span data-stu-id="1cfea-145">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="1cfea-146">Per una descrizione più dettagliata delle coordinate barycentric, vedere Descrizione delle [coordinate barycentriche di Mathworld.](https://mathworld.wolfram.com/BarycentricCoordinates.html)</span><span class="sxs-lookup"><span data-stu-id="1cfea-146">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="1cfea-147">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1cfea-147">Requirements</span></span>



| <span data-ttu-id="1cfea-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="1cfea-148">Requirement</span></span> | <span data-ttu-id="1cfea-149">Valore</span><span class="sxs-lookup"><span data-stu-id="1cfea-149">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1cfea-150">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1cfea-150">Header</span></span><br/>  | <dl> <span data-ttu-id="1cfea-151"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="1cfea-151"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="1cfea-152">Libreria</span><span class="sxs-lookup"><span data-stu-id="1cfea-152">Library</span></span><br/> | <dl> <span data-ttu-id="1cfea-153"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="1cfea-153"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1cfea-154">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1cfea-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cfea-155">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="1cfea-155">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
