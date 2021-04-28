---
description: 'Funzione D3DXVec3BaryCentric (D3dx9math.h): restituisce un punto in coordinate barycentriche, usando i vettori 3D specificati.'
ms.assetid: ecbabc76-9936-4f31-adec-1ec807984787
title: Funzione D3DXVec3BaryCentric (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3BaryCentric
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c966eeabe78deabefb2877405f649f3d162f9d73
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097895"
---
# <a name="d3dxvec3barycentric-function-d3dx9mathh"></a><span data-ttu-id="66c02-103">Funzione D3DXVec3BaryCentric (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="66c02-103">D3DXVec3BaryCentric function (D3dx9math.h)</span></span>

<span data-ttu-id="66c02-104">Restituisce un punto nelle coordinate barycentriche, usando i vettori 3D specificati.</span><span class="sxs-lookup"><span data-stu-id="66c02-104">Returns a point in Barycentric coordinates, using the specified 3D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="66c02-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="66c02-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3BaryCentric(
  _Out_       D3DXVECTOR3 *pOut,
  _In_  const D3DXVECTOR3 *pV1,
  _In_  const D3DXVECTOR3 *pV2,
  _In_  const D3DXVECTOR3 *pV3,
  _In_        FLOAT       f,
  _In_        FLOAT       g
);
```



## <a name="parameters"></a><span data-ttu-id="66c02-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="66c02-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66c02-107">*pOut* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="66c02-107">*pOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="66c02-108">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="66c02-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="66c02-109">Puntatore alla [**struttura D3DXVECTOR3**](d3dxvector3.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="66c02-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="66c02-110">*pV1* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="66c02-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66c02-111">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="66c02-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="66c02-112">Puntatore a una [**struttura D3DXVECTOR3 di**](d3dxvector3.md) origine.</span><span class="sxs-lookup"><span data-stu-id="66c02-112">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="66c02-113">*pV2* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="66c02-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66c02-114">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="66c02-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="66c02-115">Puntatore a una [**struttura D3DXVECTOR3 di**](d3dxvector3.md) origine.</span><span class="sxs-lookup"><span data-stu-id="66c02-115">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="66c02-116">*pV3* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="66c02-116">*pV3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66c02-117">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="66c02-117">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="66c02-118">Puntatore a una [**struttura D3DXVECTOR3 di**](d3dxvector3.md) origine.</span><span class="sxs-lookup"><span data-stu-id="66c02-118">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="66c02-119">*f* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="66c02-119">*f* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66c02-120">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="66c02-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="66c02-121">Fattore di ponderazione.</span><span class="sxs-lookup"><span data-stu-id="66c02-121">Weighting factor.</span></span> <span data-ttu-id="66c02-122">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="66c02-122">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="66c02-123">*g* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="66c02-123">*g* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66c02-124">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="66c02-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="66c02-125">Fattore di ponderazione.</span><span class="sxs-lookup"><span data-stu-id="66c02-125">Weighting factor.</span></span> <span data-ttu-id="66c02-126">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="66c02-126">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66c02-127">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="66c02-127">Return value</span></span>

<span data-ttu-id="66c02-128">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="66c02-128">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="66c02-129">Puntatore a [**una struttura D3DXVECTOR3**](d3dxvector3.md) in coordinate barycentriche.</span><span class="sxs-lookup"><span data-stu-id="66c02-129">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure in Barycentric coordinates.</span></span>

## <a name="remarks"></a><span data-ttu-id="66c02-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="66c02-130">Remarks</span></span>

<span data-ttu-id="66c02-131">La **funzione D3DXVec3BaryCentric** consente di comprendere i punti all'interno e intorno a un triangolo, indipendentemente dalla posizione in cui si trova effettivamente il triangolo.</span><span class="sxs-lookup"><span data-stu-id="66c02-131">The **D3DXVec3BaryCentric** function provides a way to understand points in and around a triangle, independent of where the triangle is actually located.</span></span> <span data-ttu-id="66c02-132">Questa funzione restituisce il punto risultante usando l'equazione seguente: V1 + f(V2-V1) + g(V3-V1).</span><span class="sxs-lookup"><span data-stu-id="66c02-132">This function returns the resulting point by using the following equation: V1 + f(V2-V1) + g(V3-V1).</span></span>

<span data-ttu-id="66c02-133">Qualsiasi punto nel piano V1V2V3 può essere rappresentato dalla coordinata barycentric (f,g). Il parametro *f* controlla quanto V2 viene ponderato nel risultato e il parametro *g* controlla quanto V3 viene ponderato nel risultato.</span><span class="sxs-lookup"><span data-stu-id="66c02-133">Any point in the plane V1V2V3 can be represented by the Barycentric coordinate (f,g).The parameter *f* controls how much V2 gets weighted into the result and the parameter *g* controls how much V3 gets weighted into the result.</span></span> <span data-ttu-id="66c02-134">Infine, 1-f-g controlla quanto V1 viene ponderato nel risultato.</span><span class="sxs-lookup"><span data-stu-id="66c02-134">Lastly, 1-f-g controls how much V1 gets weighted into the result.</span></span>

<span data-ttu-id="66c02-135">Si notino le relazioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="66c02-135">Note the following relations.</span></span>

-   <span data-ttu-id="66c02-136">Se (f>=0 &, & g>=0 &, & 1-f-g>=0), il punto si trova all'interno del triangolo V1V2V3.</span><span class="sxs-lookup"><span data-stu-id="66c02-136">If (f>=0 &, & g>=0 &, & 1-f-g>=0), the point is inside the triangle V1V2V3.</span></span>
-   <span data-ttu-id="66c02-137">Se (f==0 &, & g>=0 &, & 1-f-g>=0), il punto si trova sulla riga V1V3.</span><span class="sxs-lookup"><span data-stu-id="66c02-137">If (f==0 &, & g>=0 &, & 1-f-g>=0), the point is on the line V1V3.</span></span>
-   <span data-ttu-id="66c02-138">Se (f>=0 &, & g==0 &, & 1-f-g>=0), il punto si trova sulla riga V1V2.</span><span class="sxs-lookup"><span data-stu-id="66c02-138">If (f>=0 &, & g==0 &, & 1-f-g>=0), the point is on the line V1V2.</span></span>
-   <span data-ttu-id="66c02-139">Se (f>=0 &, & g>=0 &, & 1-f-g==0), il punto si trova sulla riga V2V3.</span><span class="sxs-lookup"><span data-stu-id="66c02-139">If (f>=0 &, & g>=0 &, & 1-f-g==0), the point is on the line V2V3.</span></span>

<span data-ttu-id="66c02-140">Le coordinate barycentriche sono una forma di coordinate generali.</span><span class="sxs-lookup"><span data-stu-id="66c02-140">Barycentric coordinates are a form of general coordinates.</span></span> <span data-ttu-id="66c02-141">In questo contesto, l'uso di coordinate barycentric rappresenta una modifica nei sistemi di coordinate.</span><span class="sxs-lookup"><span data-stu-id="66c02-141">In this context, using Barycentric coordinates represents a change in coordinate systems.</span></span> <span data-ttu-id="66c02-142">Ciò che vale per le coordinate cartesiane è vero per le coordinate barycentriche.</span><span class="sxs-lookup"><span data-stu-id="66c02-142">What holds true for Cartesian coordinates holds true for Barycentric coordinates.</span></span>

<span data-ttu-id="66c02-143">Il valore restituito per questa funzione è lo stesso valore restituito nel *parametro pOut.*</span><span class="sxs-lookup"><span data-stu-id="66c02-143">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="66c02-144">In questo modo, la **funzione D3DXVec3BaryCentric** può essere usata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="66c02-144">In this way, the **D3DXVec3BaryCentric** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="66c02-145">Le coordinate barycentriche definiscono un punto all'interno di un triangolo in termini di vertici del triangolo.</span><span class="sxs-lookup"><span data-stu-id="66c02-145">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="66c02-146">Per una descrizione più dettagliata delle coordinate barycentric, vedere Descrizione delle [coordinate barycentriche di Mathworld.](https://mathworld.wolfram.com/BarycentricCoordinates.html)</span><span class="sxs-lookup"><span data-stu-id="66c02-146">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="66c02-147">Requisiti</span><span class="sxs-lookup"><span data-stu-id="66c02-147">Requirements</span></span>



| <span data-ttu-id="66c02-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="66c02-148">Requirement</span></span> | <span data-ttu-id="66c02-149">Valore</span><span class="sxs-lookup"><span data-stu-id="66c02-149">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="66c02-150">Intestazione</span><span class="sxs-lookup"><span data-stu-id="66c02-150">Header</span></span><br/>  | <dl> <span data-ttu-id="66c02-151"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="66c02-151"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="66c02-152">Libreria</span><span class="sxs-lookup"><span data-stu-id="66c02-152">Library</span></span><br/> | <dl> <span data-ttu-id="66c02-153"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="66c02-153"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="66c02-154">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="66c02-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66c02-155">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="66c02-155">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
