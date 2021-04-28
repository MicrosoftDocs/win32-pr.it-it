---
description: 'Funzione D3DXMatrixAffineTransformation (D3DX10Math.h): compila una matrice di trasformazione affine 3D. Gli argomenti NULL vengono considerati trasformazioni di identità.'
ms.assetid: 36044272-a8ce-47db-8f52-30dc680f8174
title: Funzione D3DXMatrixAffineTransformation (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixAffineTransformation
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 01c6b3c3ffe2de9b7c7003b78f1b07a0f35cc3a1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113179"
---
# <a name="d3dxmatrixaffinetransformation-function-d3dx10mathh"></a><span data-ttu-id="e74c3-104">Funzione D3DXMatrixAffineTransformation (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="e74c3-104">D3DXMatrixAffineTransformation function (D3DX10Math.h)</span></span>

<span data-ttu-id="e74c3-105">Compila una matrice di trasformazione affine 3D.</span><span class="sxs-lookup"><span data-stu-id="e74c3-105">Builds a 3D affine transformation matrix.</span></span> <span data-ttu-id="e74c3-106">**Gli** argomenti NULL vengono considerati trasformazioni di identità.</span><span class="sxs-lookup"><span data-stu-id="e74c3-106">**NULL** arguments are treated as identity transformations.</span></span>

## <a name="syntax"></a><span data-ttu-id="e74c3-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e74c3-107">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixAffineTransformation(
  _In_       D3DXMATRIX     *pOut,
  _In_       FLOAT          Scaling,
  _In_ const D3DXVECTOR3    *pRotationCenter,
  _In_ const D3DXQUATERNION *pRotation,
  _In_ const D3DXVECTOR3    *pTranslation
);
```



## <a name="parameters"></a><span data-ttu-id="e74c3-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e74c3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e74c3-109">*pOut* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="e74c3-109">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e74c3-110">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="e74c3-110">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="e74c3-111">Puntatore [**all'oggetto D3DXMATRIX**](d3d10-d3dxmatrix.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="e74c3-111">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="e74c3-112">*Ridimensionamento* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="e74c3-112">*Scaling* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e74c3-113">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e74c3-113">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e74c3-114">Fattore di scala.</span><span class="sxs-lookup"><span data-stu-id="e74c3-114">Scaling factor.</span></span>

</dd> <dt>

<span data-ttu-id="e74c3-115">*pRotationCenter* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="e74c3-115">*pRotationCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e74c3-116">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="e74c3-116">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="e74c3-117">Puntatore a [**un oggetto D3DXVECTOR3,**](d3d10-d3dxvector3.md)un punto che identifica il centro di rotazione.</span><span class="sxs-lookup"><span data-stu-id="e74c3-117">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md), a point identifying the center of rotation.</span></span> <span data-ttu-id="e74c3-118">Se questo argomento è **NULL,** alla formula in Osservazioni viene applicata una matrice identity M <sub>rc.</sub></span><span class="sxs-lookup"><span data-stu-id="e74c3-118">If this argument is **NULL**, an identity M<sub>rc</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="e74c3-119">*pRotation* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="e74c3-119">*pRotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e74c3-120">Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="e74c3-120">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="e74c3-121">Puntatore a [**un oggetto D3DXQUATERNION**](d3d10-d3dxquaternion.md) che specifica la rotazione.</span><span class="sxs-lookup"><span data-stu-id="e74c3-121">Pointer to a [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that specifies the rotation.</span></span> <span data-ttu-id="e74c3-122">Se questo argomento è **NULL,** alla formula in Osservazioni viene applicata una matrice identity M <sub>r.</sub></span><span class="sxs-lookup"><span data-stu-id="e74c3-122">If this argument is **NULL**, an identity M<sub>r</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="e74c3-123">*pTranslation* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="e74c3-123">*pTranslation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e74c3-124">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="e74c3-124">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="e74c3-125">Puntatore a una struttura D3DXVECTOR3 che rappresenta la traslazione.</span><span class="sxs-lookup"><span data-stu-id="e74c3-125">Pointer to a D3DXVECTOR3 structure representing the translation.</span></span> <span data-ttu-id="e74c3-126">Se questo argomento è **NULL,** viene applicata una matrice Identity Mt alla formula in Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="e74c3-126">If this argument is **NULL**, an identity Mₜ matrix is applied to the formula in Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e74c3-127">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e74c3-127">Return value</span></span>

<span data-ttu-id="e74c3-128">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="e74c3-128">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="e74c3-129">Puntatore a una struttura D3DXMATRIX che è una matrice di trasformazione affine.</span><span class="sxs-lookup"><span data-stu-id="e74c3-129">Pointer to a D3DXMATRIX structure that is an affine transformation matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="e74c3-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="e74c3-130">Remarks</span></span>

<span data-ttu-id="e74c3-131">Questa funzione calcola la matrice di trasformazione affine con la formula seguente, con la concatenazione di matrici valutata in ordine da sinistra a destra:</span><span class="sxs-lookup"><span data-stu-id="e74c3-131">This function calculates the affine transformation matrix with the following formula, with matrix concatenation evaluated in left-to-right order:</span></span>

<span data-ttu-id="e74c3-132">M<sub>out</sub> = Ms \* (M<sub>rc</sub>)-1 \* M<sub>r</sub> \* M<sub>rc</sub> \* Mt</span><span class="sxs-lookup"><span data-stu-id="e74c3-132">M<sub>out</sub> = Mₛ \* (M<sub>rc</sub>)-1 \* M<sub>r</sub> \* M<sub>rc</sub> \* Mₜ</span></span>

<span data-ttu-id="e74c3-133">dove:</span><span class="sxs-lookup"><span data-stu-id="e74c3-133">where:</span></span>

<span data-ttu-id="e74c3-134">M<sub>out</sub> = matrice di output (pOut)</span><span class="sxs-lookup"><span data-stu-id="e74c3-134">M<sub>out</sub> = output matrix (pOut)</span></span>

<span data-ttu-id="e74c3-135">Ms = matrice di ridimensionamento (ridimensionamento)</span><span class="sxs-lookup"><span data-stu-id="e74c3-135">Mₛ = scaling matrix (Scaling)</span></span>

<span data-ttu-id="e74c3-136">M<sub>rc</sub> = centro della matrice di rotazione (pRotationCenter)</span><span class="sxs-lookup"><span data-stu-id="e74c3-136">M<sub>rc</sub> = center of rotation matrix (pRotationCenter)</span></span>

<span data-ttu-id="e74c3-137">M<sub>r</sub> = matrice di rotazione (pRotation)</span><span class="sxs-lookup"><span data-stu-id="e74c3-137">M<sub>r</sub> = rotation matrix (pRotation)</span></span>

<span data-ttu-id="e74c3-138">Mt = matrice di traslazione (pTranslation)</span><span class="sxs-lookup"><span data-stu-id="e74c3-138">Mₜ = translation matrix (pTranslation)</span></span>

<span data-ttu-id="e74c3-139">Il valore restituito per questa funzione è lo stesso valore restituito nel parametro pOut.</span><span class="sxs-lookup"><span data-stu-id="e74c3-139">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="e74c3-140">In questo modo, la funzione D3DXMatrixAffineTransformation può essere usata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="e74c3-140">In this way, the D3DXMatrixAffineTransformation function can be used as a parameter for another function.</span></span>

<span data-ttu-id="e74c3-141">Per le trasformazioni affine 2D, usare D3DXMatrixAffineTransformation2D.</span><span class="sxs-lookup"><span data-stu-id="e74c3-141">For 2D affine transformations, use D3DXMatrixAffineTransformation2D.</span></span>

## <a name="requirements"></a><span data-ttu-id="e74c3-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e74c3-142">Requirements</span></span>



| <span data-ttu-id="e74c3-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="e74c3-143">Requirement</span></span> | <span data-ttu-id="e74c3-144">Valore</span><span class="sxs-lookup"><span data-stu-id="e74c3-144">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e74c3-145">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e74c3-145">Header</span></span><br/>  | <dl> <span data-ttu-id="e74c3-146"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="e74c3-146"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="e74c3-147">Libreria</span><span class="sxs-lookup"><span data-stu-id="e74c3-147">Library</span></span><br/> | <dl> <span data-ttu-id="e74c3-148"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="e74c3-148"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e74c3-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e74c3-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e74c3-150">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="e74c3-150">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
