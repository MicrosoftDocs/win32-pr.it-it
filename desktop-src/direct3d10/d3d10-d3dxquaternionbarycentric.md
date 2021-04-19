---
description: Restituisce un quaternione nelle coordinate baricentrica.
ms.assetid: 0a8d8d5a-f486-4457-86e9-27e76eaf1bc4
title: Funzione D3DXQuaternionBaryCentric (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionBaryCentric
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: f7cdfcf5b8e7052fcbea72f12123a0ea44422853
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323206"
---
# <a name="d3dxquaternionbarycentric-function-d3dx10mathh"></a><span data-ttu-id="a88aa-103">Funzione D3DXQuaternionBaryCentric (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="a88aa-103">D3DXQuaternionBaryCentric function (D3DX10Math.h)</span></span>

<span data-ttu-id="a88aa-104">Restituisce un quaternione nelle coordinate baricentrica.</span><span class="sxs-lookup"><span data-stu-id="a88aa-104">Returns a quaternion in barycentric coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="a88aa-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a88aa-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionBaryCentric(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ1,
  _In_    const D3DXQUATERNION *pQ2,
  _In_    const D3DXQUATERNION *pQ3,
  _In_          FLOAT          f,
  _In_          FLOAT          g
);
```



## <a name="parameters"></a><span data-ttu-id="a88aa-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a88aa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a88aa-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="a88aa-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a88aa-108">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="a88aa-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="a88aa-109">Puntatore a [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="a88aa-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="a88aa-110">*pQ1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a88aa-110">*pQ1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a88aa-111">Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="a88aa-111">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="a88aa-112">Puntatore a una struttura D3DXQUATERNION di origine.</span><span class="sxs-lookup"><span data-stu-id="a88aa-112">Pointer to a source D3DXQUATERNION structure.</span></span>

</dd> <dt>

<span data-ttu-id="a88aa-113">*pQ2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a88aa-113">*pQ2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a88aa-114">Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="a88aa-114">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="a88aa-115">Puntatore a una struttura D3DXQUATERNION di origine.</span><span class="sxs-lookup"><span data-stu-id="a88aa-115">Pointer to a source D3DXQUATERNION structure.</span></span>

</dd> <dt>

<span data-ttu-id="a88aa-116">*pQ3* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a88aa-116">*pQ3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a88aa-117">Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="a88aa-117">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="a88aa-118">Puntatore a una struttura D3DXQUATERNION di origine.</span><span class="sxs-lookup"><span data-stu-id="a88aa-118">Pointer to a source D3DXQUATERNION structure.</span></span>

</dd> <dt>

<span data-ttu-id="a88aa-119">*f* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a88aa-119">*f* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a88aa-120">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a88aa-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a88aa-121">Fattore di ponderazione.</span><span class="sxs-lookup"><span data-stu-id="a88aa-121">Weighting factor.</span></span> <span data-ttu-id="a88aa-122">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="a88aa-122">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="a88aa-123">*g* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a88aa-123">*g* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a88aa-124">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a88aa-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a88aa-125">Fattore di ponderazione.</span><span class="sxs-lookup"><span data-stu-id="a88aa-125">Weighting factor.</span></span> <span data-ttu-id="a88aa-126">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="a88aa-126">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a88aa-127">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a88aa-127">Return value</span></span>

<span data-ttu-id="a88aa-128">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="a88aa-128">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="a88aa-129">Puntatore a una struttura D3DXQUATERNION nelle coordinate di baricentrica.</span><span class="sxs-lookup"><span data-stu-id="a88aa-129">Pointer to a D3DXQUATERNION structure in Barycentric coordinates.</span></span>

## <a name="remarks"></a><span data-ttu-id="a88aa-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="a88aa-130">Remarks</span></span>

<span data-ttu-id="a88aa-131">Per calcolare le coordinate baricentrica, la funzione D3DXQuaternionBaryCentric implementa la serie seguente di operazioni di interpolazione lineare sferica:</span><span class="sxs-lookup"><span data-stu-id="a88aa-131">To compute the barycentric coordinates, the D3DXQuaternionBaryCentric function implements the following series of spherical linear interpolation operations:</span></span>


```
Slerp(Slerp(Q1, Q2, f+g), Slerp(Q1, Q3, f+g), g/(f+g))
```



<span data-ttu-id="a88aa-132">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro broncio.</span><span class="sxs-lookup"><span data-stu-id="a88aa-132">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="a88aa-133">In questo modo, la funzione D3DXQuaternionBaryCentric può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="a88aa-133">In this way, the D3DXQuaternionBaryCentric function can be used as a parameter for another function.</span></span>

<span data-ttu-id="a88aa-134">Usare [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) per qualsiasi input quaternione non ancora normalizzato.</span><span class="sxs-lookup"><span data-stu-id="a88aa-134">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

<span data-ttu-id="a88aa-135">Le coordinate baricentrica definiscono un punto all'interno di un triangolo in termini di vertici del triangolo.</span><span class="sxs-lookup"><span data-stu-id="a88aa-135">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="a88aa-136">Per una descrizione più approfondita delle coordinate baricentrica, vedere [la descrizione delle coordinate baricentrica di articolo MathWorld](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span><span class="sxs-lookup"><span data-stu-id="a88aa-136">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="a88aa-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a88aa-137">Requirements</span></span>



| <span data-ttu-id="a88aa-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="a88aa-138">Requirement</span></span> | <span data-ttu-id="a88aa-139">Valore</span><span class="sxs-lookup"><span data-stu-id="a88aa-139">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a88aa-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a88aa-140">Header</span></span><br/>  | <dl> <span data-ttu-id="a88aa-141"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="a88aa-141"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="a88aa-142">Libreria</span><span class="sxs-lookup"><span data-stu-id="a88aa-142">Library</span></span><br/> | <dl> <span data-ttu-id="a88aa-143"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a88aa-143"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a88aa-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a88aa-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a88aa-145">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="a88aa-145">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
