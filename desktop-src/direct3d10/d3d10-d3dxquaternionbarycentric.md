---
description: 'Funzione D3DXQuaternionBaryCentric (D3DX10Math.h): restituisce un quaternione in coordinate barycentriche.'
ms.assetid: 0a8d8d5a-f486-4457-86e9-27e76eaf1bc4
title: Funzione D3DXQuaternionBaryCentric (D3DX10Math.h)
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
ms.openlocfilehash: 00d8e41a0173b7b26083f38beb82417365ef7067
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108779"
---
# <a name="d3dxquaternionbarycentric-function-d3dx10mathh"></a><span data-ttu-id="1c2f7-103">Funzione D3DXQuaternionBaryCentric (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="1c2f7-103">D3DXQuaternionBaryCentric function (D3DX10Math.h)</span></span>

<span data-ttu-id="1c2f7-104">Restituisce un quaternione in coordinate barycentriche.</span><span class="sxs-lookup"><span data-stu-id="1c2f7-104">Returns a quaternion in barycentric coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c2f7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1c2f7-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="1c2f7-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1c2f7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c2f7-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="1c2f7-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1c2f7-108">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="1c2f7-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="1c2f7-109">Puntatore [**all'oggetto D3DXQUATERNION**](d3d10-d3dxquaternion.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="1c2f7-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="1c2f7-110">*pQ1* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="1c2f7-110">*pQ1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c2f7-111">Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="1c2f7-111">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="1c2f7-112">Puntatore a una struttura D3DXQUATERNION di origine.</span><span class="sxs-lookup"><span data-stu-id="1c2f7-112">Pointer to a source D3DXQUATERNION structure.</span></span>

</dd> <dt>

<span data-ttu-id="1c2f7-113">*pQ2* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="1c2f7-113">*pQ2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c2f7-114">Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="1c2f7-114">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="1c2f7-115">Puntatore a una struttura D3DXQUATERNION di origine.</span><span class="sxs-lookup"><span data-stu-id="1c2f7-115">Pointer to a source D3DXQUATERNION structure.</span></span>

</dd> <dt>

<span data-ttu-id="1c2f7-116">*pQ3* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="1c2f7-116">*pQ3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c2f7-117">Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="1c2f7-117">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="1c2f7-118">Puntatore a una struttura D3DXQUATERNION di origine.</span><span class="sxs-lookup"><span data-stu-id="1c2f7-118">Pointer to a source D3DXQUATERNION structure.</span></span>

</dd> <dt>

<span data-ttu-id="1c2f7-119">*f* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1c2f7-119">*f* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c2f7-120">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1c2f7-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1c2f7-121">Fattore di ponderazione.</span><span class="sxs-lookup"><span data-stu-id="1c2f7-121">Weighting factor.</span></span> <span data-ttu-id="1c2f7-122">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="1c2f7-122">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="1c2f7-123">*g* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1c2f7-123">*g* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c2f7-124">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1c2f7-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1c2f7-125">Fattore di ponderazione.</span><span class="sxs-lookup"><span data-stu-id="1c2f7-125">Weighting factor.</span></span> <span data-ttu-id="1c2f7-126">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="1c2f7-126">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c2f7-127">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1c2f7-127">Return value</span></span>

<span data-ttu-id="1c2f7-128">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="1c2f7-128">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="1c2f7-129">Puntatore a una struttura D3DXQUATERNION in coordinate barycentriche.</span><span class="sxs-lookup"><span data-stu-id="1c2f7-129">Pointer to a D3DXQUATERNION structure in Barycentric coordinates.</span></span>

## <a name="remarks"></a><span data-ttu-id="1c2f7-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="1c2f7-130">Remarks</span></span>

<span data-ttu-id="1c2f7-131">Per calcolare le coordinate barycentric, la funzione D3DXQuaternionBaryCentric implementa la serie seguente di operazioni di interpolazione lineare sferica:</span><span class="sxs-lookup"><span data-stu-id="1c2f7-131">To compute the barycentric coordinates, the D3DXQuaternionBaryCentric function implements the following series of spherical linear interpolation operations:</span></span>


```
Slerp(Slerp(Q1, Q2, f+g), Slerp(Q1, Q3, f+g), g/(f+g))
```



<span data-ttu-id="1c2f7-132">Il valore restituito per questa funzione è lo stesso valore restituito nel parametro pOut.</span><span class="sxs-lookup"><span data-stu-id="1c2f7-132">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="1c2f7-133">In questo modo, la funzione D3DXQuaternionBaryCentric può essere usata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="1c2f7-133">In this way, the D3DXQuaternionBaryCentric function can be used as a parameter for another function.</span></span>

<span data-ttu-id="1c2f7-134">Usare [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) per qualsiasi input quaternione non ancora normalizzato.</span><span class="sxs-lookup"><span data-stu-id="1c2f7-134">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

<span data-ttu-id="1c2f7-135">Le coordinate barycentriche definiscono un punto all'interno di un triangolo in termini di vertici del triangolo.</span><span class="sxs-lookup"><span data-stu-id="1c2f7-135">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="1c2f7-136">Per una descrizione più dettagliata delle coordinate barycentric, vedere Descrizione delle [coordinate barycentriche di Mathworld.](https://mathworld.wolfram.com/BarycentricCoordinates.html)</span><span class="sxs-lookup"><span data-stu-id="1c2f7-136">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="1c2f7-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1c2f7-137">Requirements</span></span>



| <span data-ttu-id="1c2f7-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c2f7-138">Requirement</span></span> | <span data-ttu-id="1c2f7-139">Valore</span><span class="sxs-lookup"><span data-stu-id="1c2f7-139">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1c2f7-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1c2f7-140">Header</span></span><br/>  | <dl> <span data-ttu-id="1c2f7-141"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="1c2f7-141"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="1c2f7-142">Libreria</span><span class="sxs-lookup"><span data-stu-id="1c2f7-142">Library</span></span><br/> | <dl> <span data-ttu-id="1c2f7-143"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="1c2f7-143"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1c2f7-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1c2f7-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c2f7-145">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="1c2f7-145">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
