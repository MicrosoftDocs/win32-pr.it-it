---
description: 'Funzione D3DXVec4BaryCentric (D3DX10Math.h): restituisce un punto nelle coordinate barycentriche, usando i vettori 4D specificati.'
ms.assetid: 44406135-3270-4f2e-bb53-29affb2510f2
title: Funzione D3DXVec4BaryCentric (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4BaryCentric
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 935432d1634a7fd35401d92471b1f366075ac8b7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102989"
---
# <a name="d3dxvec4barycentric-function-d3dx10mathh"></a><span data-ttu-id="fbc53-103">Funzione D3DXVec4BaryCentric (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="fbc53-103">D3DXVec4BaryCentric function (D3DX10Math.h)</span></span>

<span data-ttu-id="fbc53-104">Restituisce un punto nelle coordinate barycentriche, usando i vettori 4D specificati.</span><span class="sxs-lookup"><span data-stu-id="fbc53-104">Returns a point in Barycentric coordinates, using the specified 4D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbc53-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fbc53-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4BaryCentric(
  _In_       D3DXVECTOR4 *pOut,
  _In_ const D3DXVECTOR4 *pV1,
  _In_ const D3DXVECTOR4 *pV2,
  _In_ const D3DXVECTOR4 *pV3,
  _In_       FLOAT       f,
  _In_       FLOAT       g
);
```



## <a name="parameters"></a><span data-ttu-id="fbc53-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="fbc53-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fbc53-107">*pOut* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="fbc53-107">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fbc53-108">Tipo: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="fbc53-108">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="fbc53-109">Puntatore a [**D3DXVECTOR4**](d3d10-d3dxvector4.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="fbc53-109">Pointer to the [**D3DXVECTOR4**](d3d10-d3dxvector4.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="fbc53-110">*pV1* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="fbc53-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fbc53-111">Tipo: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="fbc53-111">Type: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="fbc53-112">Puntatore a una struttura D3DXVECTOR4 di origine.</span><span class="sxs-lookup"><span data-stu-id="fbc53-112">Pointer to a source D3DXVECTOR4 structure.</span></span>

</dd> <dt>

<span data-ttu-id="fbc53-113">*pV2* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="fbc53-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fbc53-114">Tipo: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="fbc53-114">Type: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="fbc53-115">Puntatore a una struttura D3DXVECTOR4 di origine.</span><span class="sxs-lookup"><span data-stu-id="fbc53-115">Pointer to a source D3DXVECTOR4 structure.</span></span>

</dd> <dt>

<span data-ttu-id="fbc53-116">*pV3* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="fbc53-116">*pV3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fbc53-117">Tipo: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="fbc53-117">Type: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="fbc53-118">Puntatore a una struttura D3DXVECTOR4 di origine.</span><span class="sxs-lookup"><span data-stu-id="fbc53-118">Pointer to a source D3DXVECTOR4 structure.</span></span>

</dd> <dt>

<span data-ttu-id="fbc53-119">*f* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fbc53-119">*f* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fbc53-120">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fbc53-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fbc53-121">Fattore di ponderazione.</span><span class="sxs-lookup"><span data-stu-id="fbc53-121">Weighting factor.</span></span> <span data-ttu-id="fbc53-122">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="fbc53-122">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="fbc53-123">*g* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fbc53-123">*g* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fbc53-124">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fbc53-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fbc53-125">Fattore di ponderazione.</span><span class="sxs-lookup"><span data-stu-id="fbc53-125">Weighting factor.</span></span> <span data-ttu-id="fbc53-126">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="fbc53-126">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fbc53-127">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fbc53-127">Return value</span></span>

<span data-ttu-id="fbc53-128">Tipo: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="fbc53-128">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="fbc53-129">Puntatore a una struttura D3DXVECTOR4 in coordinate barycentriche.</span><span class="sxs-lookup"><span data-stu-id="fbc53-129">Pointer to a D3DXVECTOR4 structure in Barycentric coordinates.</span></span>

## <a name="remarks"></a><span data-ttu-id="fbc53-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="fbc53-130">Remarks</span></span>

<span data-ttu-id="fbc53-131">La funzione D3DXVec4BaryCentric consente di comprendere i punti all'interno e intorno a un triangolo, indipendentemente dalla posizione in cui si trova effettivamente il triangolo.</span><span class="sxs-lookup"><span data-stu-id="fbc53-131">The D3DXVec4BaryCentric function provides a way to understand points in and around a triangle, independent of where the triangle is actually located.</span></span> <span data-ttu-id="fbc53-132">Questa funzione restituisce il punto risultante usando l'equazione seguente: V1 + f(V2-V1) + g(V3-V1).</span><span class="sxs-lookup"><span data-stu-id="fbc53-132">This function returns the resulting point by using the following equation: V1 + f(V2-V1) + g(V3-V1).</span></span>

<span data-ttu-id="fbc53-133">Qualsiasi punto nel piano V1V2V3 può essere rappresentato dalla coordinata barycentrica (f,g). Il parametro f controlla quanto V2 viene ponderato nel risultato e il parametro g controlla la quantità di V3 ponderata nel risultato.</span><span class="sxs-lookup"><span data-stu-id="fbc53-133">Any point in the plane V1V2V3 can be represented by the Barycentric coordinate (f,g).The parameter f controls how much V2 gets weighted into the result and the parameter g controls how much V3 gets weighted into the result.</span></span> <span data-ttu-id="fbc53-134">Infine, 1-f-g controlla la quantità di V1 ponderata nel risultato.</span><span class="sxs-lookup"><span data-stu-id="fbc53-134">Lastly, 1-f-g controls how much V1 gets weighted into the result.</span></span>

<span data-ttu-id="fbc53-135">Si notino le relazioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="fbc53-135">Note the following relations.</span></span>

-   <span data-ttu-id="fbc53-136">Se (f>=0 &, & g>=0 &, & 1-f-g>=0), il punto si trova all'interno del triangolo V1V2V3.</span><span class="sxs-lookup"><span data-stu-id="fbc53-136">If (f>=0 &, & g>=0 &, & 1-f-g>=0), the point is inside the triangle V1V2V3.</span></span>
-   <span data-ttu-id="fbc53-137">Se (f===0 &, & g>=0 &, & 1-f-g>=0), il punto si trova sulla riga V1V3.</span><span class="sxs-lookup"><span data-stu-id="fbc53-137">If (f==0 &, & g>=0 &, & 1-f-g>=0), the point is on the line V1V3.</span></span>
-   <span data-ttu-id="fbc53-138">Se (f>=0 &, & g==0 &, & 1-f-g>=0), il punto si trova sulla riga V1V2.</span><span class="sxs-lookup"><span data-stu-id="fbc53-138">If (f>=0 &, & g==0 &, & 1-f-g>=0), the point is on the line V1V2.</span></span>
-   <span data-ttu-id="fbc53-139">Se (f>=0 &, & g>=0 &, & 1-f-g==0), il punto si trova sulla riga V2V3.</span><span class="sxs-lookup"><span data-stu-id="fbc53-139">If (f>=0 &, & g>=0 &, & 1-f-g==0), the point is on the line V2V3.</span></span>

<span data-ttu-id="fbc53-140">Le coordinate barycentriche sono una forma di coordinate generali.</span><span class="sxs-lookup"><span data-stu-id="fbc53-140">Barycentric coordinates are a form of general coordinates.</span></span> <span data-ttu-id="fbc53-141">In questo contesto, l'uso delle coordinate barycentriche rappresenta una modifica nei sistemi di coordinate.</span><span class="sxs-lookup"><span data-stu-id="fbc53-141">In this context, using Barycentric coordinates represents a change in coordinate systems.</span></span> <span data-ttu-id="fbc53-142">Ciò che vale per le coordinate cartesiane è vero per le coordinate barycentriche.</span><span class="sxs-lookup"><span data-stu-id="fbc53-142">What holds true for Cartesian coordinates holds true for Barycentric coordinates.</span></span>

<span data-ttu-id="fbc53-143">Il valore restituito per questa funzione è lo stesso valore restituito nel parametro pOut.</span><span class="sxs-lookup"><span data-stu-id="fbc53-143">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="fbc53-144">In questo modo, la funzione D3DXVec4BaryCentric può essere usata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="fbc53-144">In this way, the D3DXVec4BaryCentric function can be used as a parameter for another function.</span></span>

<span data-ttu-id="fbc53-145">Le coordinate barycentriche definiscono un punto all'interno di un triangolo in termini di vertici del triangolo.</span><span class="sxs-lookup"><span data-stu-id="fbc53-145">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="fbc53-146">Per una descrizione più approfondita delle coordinate barycentriche, vedere Descrizione delle coordinate [barycentriche di Mathworld.](https://mathworld.wolfram.com/BarycentricCoordinates.html)</span><span class="sxs-lookup"><span data-stu-id="fbc53-146">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="fbc53-147">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fbc53-147">Requirements</span></span>



| <span data-ttu-id="fbc53-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="fbc53-148">Requirement</span></span> | <span data-ttu-id="fbc53-149">Valore</span><span class="sxs-lookup"><span data-stu-id="fbc53-149">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fbc53-150">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fbc53-150">Header</span></span><br/> | <dl> <span data-ttu-id="fbc53-151"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="fbc53-151"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fbc53-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fbc53-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbc53-153">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="fbc53-153">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
