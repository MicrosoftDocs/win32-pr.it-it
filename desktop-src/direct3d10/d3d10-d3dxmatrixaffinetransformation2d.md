---
description: Compila una matrice di trasformazione affine 2D nel piano x-y. Gli argomenti NULL vengono considerati come trasformazioni di identità.
ms.assetid: f46a307c-4566-42c8-8def-fb189116144e
title: Funzione D3DXMatrixAffineTransformation2D (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixAffineTransformation2D
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 223ef5d2d9a68c993553d52f5d4cf63e8b95dd3b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323414"
---
# <a name="d3dxmatrixaffinetransformation2d-function-d3dx10mathh"></a><span data-ttu-id="1564b-104">Funzione D3DXMatrixAffineTransformation2D (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="1564b-104">D3DXMatrixAffineTransformation2D function (D3DX10Math.h)</span></span>

<span data-ttu-id="1564b-105">Compila una matrice di trasformazione affine 2D nel piano x-y.</span><span class="sxs-lookup"><span data-stu-id="1564b-105">Builds a 2D affine transformation matrix in the x-y plane.</span></span> <span data-ttu-id="1564b-106">Gli argomenti **null** vengono considerati come trasformazioni di identità.</span><span class="sxs-lookup"><span data-stu-id="1564b-106">**NULL** arguments are treated as identity transformations.</span></span>

## <a name="syntax"></a><span data-ttu-id="1564b-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1564b-107">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixAffineTransformation2D(
  _In_       D3DXMATRIX  *pOut,
  _In_       FLOAT       Scaling,
  _In_ const D3DXVECTOR2 *pRotationCenter,
  _In_       FLOAT       Rotation,
  _In_ const D3DXVECTOR2 *pTranslation
);
```



## <a name="parameters"></a><span data-ttu-id="1564b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="1564b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1564b-109">*broncio* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1564b-109">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1564b-110">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="1564b-110">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="1564b-111">Puntatore a [**D3DXMATRIX**](d3d10-d3dxmatrix.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="1564b-111">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="1564b-112">*Ridimensionamento* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1564b-112">*Scaling* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1564b-113">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1564b-113">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1564b-114">Fattore di scala.</span><span class="sxs-lookup"><span data-stu-id="1564b-114">Scaling factor.</span></span>

</dd> <dt>

<span data-ttu-id="1564b-115">*pRotationCenter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1564b-115">*pRotationCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1564b-116">Tipo: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="1564b-116">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="1564b-117">Puntatore a un [**D3DXVECTOR2**](d3d10-d3dxvector2.md), un punto che identifica il centro della rotazione.</span><span class="sxs-lookup"><span data-stu-id="1564b-117">Pointer to a [**D3DXVECTOR2**](d3d10-d3dxvector2.md), a point identifying the center of rotation.</span></span> <span data-ttu-id="1564b-118">Se questo argomento è **null**, una matrice Identity M <sub>RC</sub> viene applicata alla formula nelle osservazioni.</span><span class="sxs-lookup"><span data-stu-id="1564b-118">If this argument is **NULL**, an identity M<sub>rc</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="1564b-119">*Rotazione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1564b-119">*Rotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1564b-120">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1564b-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1564b-121">Angolo di rotazione.</span><span class="sxs-lookup"><span data-stu-id="1564b-121">The angle of rotation.</span></span>

</dd> <dt>

<span data-ttu-id="1564b-122">*pTranslation* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1564b-122">*pTranslation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1564b-123">Tipo: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="1564b-123">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="1564b-124">Puntatore a un [**D3DXVECTOR2**](d3d10-d3dxvector2.md)che rappresenta la traduzione.</span><span class="sxs-lookup"><span data-stu-id="1564b-124">Pointer to a [**D3DXVECTOR2**](d3d10-d3dxvector2.md), representing the translation.</span></span> <span data-ttu-id="1564b-125">Se questo argomento è **null**, viene applicata una matrice di valori Identity mt alla formula nei commenti.</span><span class="sxs-lookup"><span data-stu-id="1564b-125">If this argument is **NULL**, an identity Mₜ matrix is applied to the formula in Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1564b-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1564b-126">Return value</span></span>

<span data-ttu-id="1564b-127">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="1564b-127">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="1564b-128">Puntatore a una struttura D3DXMATRIX che rappresenta una matrice di trasformazione affine.</span><span class="sxs-lookup"><span data-stu-id="1564b-128">Pointer to a D3DXMATRIX structure that is an affine transformation matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="1564b-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="1564b-129">Remarks</span></span>

<span data-ttu-id="1564b-130">Questa funzione calcola la matrice di trasformazione affine con la formula seguente, con concatenazione di matrici valutata in ordine da sinistra a destra:</span><span class="sxs-lookup"><span data-stu-id="1564b-130">This function calculates the affine transformation matrix with the following formula, with matrix concatenation evaluated in left-to-right order:</span></span>

<span data-ttu-id="1564b-131">M<sub>out</sub> = MS \* (m<sub>RC</sub>)-1 \* M<sub>r</sub> \* m<sub>rc</sub> \* mt</span><span class="sxs-lookup"><span data-stu-id="1564b-131">M<sub>out</sub> = Mₛ \* (M<sub>rc</sub>)-1 \* M<sub>r</sub> \* M<sub>rc</sub> \* Mₜ</span></span>

<span data-ttu-id="1564b-132">dove:</span><span class="sxs-lookup"><span data-stu-id="1564b-132">where:</span></span>

<span data-ttu-id="1564b-133">M<sub>out</sub> = matrice di output (broncio)</span><span class="sxs-lookup"><span data-stu-id="1564b-133">M<sub>out</sub> = output matrix (pOut)</span></span>

<span data-ttu-id="1564b-134">MS = scala della matrice (scalabilità)</span><span class="sxs-lookup"><span data-stu-id="1564b-134">Mₛ = scaling matrix (Scaling)</span></span>

<span data-ttu-id="1564b-135">M<sub>RC</sub> = matrice Center of rotation (pRotationCenter)</span><span class="sxs-lookup"><span data-stu-id="1564b-135">M<sub>rc</sub> = center of rotation matrix (pRotationCenter)</span></span>

<span data-ttu-id="1564b-136">M<sub>r</sub> = matrice di rotazione (rotazione)</span><span class="sxs-lookup"><span data-stu-id="1564b-136">M<sub>r</sub> = rotation matrix (Rotation)</span></span>

<span data-ttu-id="1564b-137">Mt = matrice di traslazione (pTranslation)</span><span class="sxs-lookup"><span data-stu-id="1564b-137">Mₜ = translation matrix (pTranslation)</span></span>

<span data-ttu-id="1564b-138">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro broncio.</span><span class="sxs-lookup"><span data-stu-id="1564b-138">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="1564b-139">In questo modo, la funzione D3DXMatrixAffineTransformation2D può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="1564b-139">In this way, the D3DXMatrixAffineTransformation2D function can be used as a parameter for another function.</span></span>

<span data-ttu-id="1564b-140">Per le trasformazioni affini 3D, usare D3DXMatrixAffineTransformation.</span><span class="sxs-lookup"><span data-stu-id="1564b-140">For 3D affine transformations, use D3DXMatrixAffineTransformation.</span></span>

## <a name="requirements"></a><span data-ttu-id="1564b-141">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1564b-141">Requirements</span></span>



| <span data-ttu-id="1564b-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="1564b-142">Requirement</span></span> | <span data-ttu-id="1564b-143">Valore</span><span class="sxs-lookup"><span data-stu-id="1564b-143">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1564b-144">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1564b-144">Header</span></span><br/>  | <dl> <span data-ttu-id="1564b-145"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="1564b-145"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="1564b-146">Libreria</span><span class="sxs-lookup"><span data-stu-id="1564b-146">Library</span></span><br/> | <dl> <span data-ttu-id="1564b-147"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1564b-147"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1564b-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1564b-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1564b-149">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="1564b-149">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
