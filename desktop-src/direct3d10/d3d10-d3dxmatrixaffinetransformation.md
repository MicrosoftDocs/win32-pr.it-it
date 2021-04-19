---
description: Compila una matrice di trasformazione affine 3D. Gli argomenti NULL vengono considerati come trasformazioni di identità.
ms.assetid: 36044272-a8ce-47db-8f52-30dc680f8174
title: Funzione D3DXMatrixAffineTransformation (D3DX10Math. h)
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
ms.openlocfilehash: 27fee5a620d75c3930b1bc2f8a85415db1320a47
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323415"
---
# <a name="d3dxmatrixaffinetransformation-function-d3dx10mathh"></a><span data-ttu-id="f0faf-104">Funzione D3DXMatrixAffineTransformation (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="f0faf-104">D3DXMatrixAffineTransformation function (D3DX10Math.h)</span></span>

<span data-ttu-id="f0faf-105">Compila una matrice di trasformazione affine 3D.</span><span class="sxs-lookup"><span data-stu-id="f0faf-105">Builds a 3D affine transformation matrix.</span></span> <span data-ttu-id="f0faf-106">Gli argomenti **null** vengono considerati come trasformazioni di identità.</span><span class="sxs-lookup"><span data-stu-id="f0faf-106">**NULL** arguments are treated as identity transformations.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0faf-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f0faf-107">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixAffineTransformation(
  _In_       D3DXMATRIX     *pOut,
  _In_       FLOAT          Scaling,
  _In_ const D3DXVECTOR3    *pRotationCenter,
  _In_ const D3DXQUATERNION *pRotation,
  _In_ const D3DXVECTOR3    *pTranslation
);
```



## <a name="parameters"></a><span data-ttu-id="f0faf-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="f0faf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0faf-109">*broncio* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f0faf-109">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0faf-110">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="f0faf-110">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="f0faf-111">Puntatore a [**D3DXMATRIX**](d3d10-d3dxmatrix.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="f0faf-111">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="f0faf-112">*Ridimensionamento* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f0faf-112">*Scaling* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0faf-113">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f0faf-113">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f0faf-114">Fattore di scala.</span><span class="sxs-lookup"><span data-stu-id="f0faf-114">Scaling factor.</span></span>

</dd> <dt>

<span data-ttu-id="f0faf-115">*pRotationCenter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f0faf-115">*pRotationCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0faf-116">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="f0faf-116">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="f0faf-117">Puntatore a un [**D3DXVECTOR3**](d3d10-d3dxvector3.md), un punto che identifica il centro della rotazione.</span><span class="sxs-lookup"><span data-stu-id="f0faf-117">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md), a point identifying the center of rotation.</span></span> <span data-ttu-id="f0faf-118">Se questo argomento è **null**, una matrice Identity M <sub>RC</sub> viene applicata alla formula nelle osservazioni.</span><span class="sxs-lookup"><span data-stu-id="f0faf-118">If this argument is **NULL**, an identity M<sub>rc</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="f0faf-119">*protazione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f0faf-119">*pRotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0faf-120">Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="f0faf-120">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="f0faf-121">Puntatore a un [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) che specifica la rotazione.</span><span class="sxs-lookup"><span data-stu-id="f0faf-121">Pointer to a [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that specifies the rotation.</span></span> <span data-ttu-id="f0faf-122">Se questo argomento è **null**, una matrice di identità M <sub>r</sub> viene applicata alla formula nei commenti.</span><span class="sxs-lookup"><span data-stu-id="f0faf-122">If this argument is **NULL**, an identity M<sub>r</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="f0faf-123">*pTranslation* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f0faf-123">*pTranslation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0faf-124">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="f0faf-124">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="f0faf-125">Puntatore a una struttura D3DXVECTOR3 che rappresenta la traduzione.</span><span class="sxs-lookup"><span data-stu-id="f0faf-125">Pointer to a D3DXVECTOR3 structure representing the translation.</span></span> <span data-ttu-id="f0faf-126">Se questo argomento è **null**, viene applicata una matrice di valori Identity mt alla formula nei commenti.</span><span class="sxs-lookup"><span data-stu-id="f0faf-126">If this argument is **NULL**, an identity Mₜ matrix is applied to the formula in Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0faf-127">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f0faf-127">Return value</span></span>

<span data-ttu-id="f0faf-128">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="f0faf-128">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="f0faf-129">Puntatore a una struttura D3DXMATRIX che rappresenta una matrice di trasformazione affine.</span><span class="sxs-lookup"><span data-stu-id="f0faf-129">Pointer to a D3DXMATRIX structure that is an affine transformation matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="f0faf-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="f0faf-130">Remarks</span></span>

<span data-ttu-id="f0faf-131">Questa funzione calcola la matrice di trasformazione affine con la formula seguente, con concatenazione di matrici valutata in ordine da sinistra a destra:</span><span class="sxs-lookup"><span data-stu-id="f0faf-131">This function calculates the affine transformation matrix with the following formula, with matrix concatenation evaluated in left-to-right order:</span></span>

<span data-ttu-id="f0faf-132">M<sub>out</sub> = MS \* (m<sub>RC</sub>)-1 \* M<sub>r</sub> \* m<sub>rc</sub> \* mt</span><span class="sxs-lookup"><span data-stu-id="f0faf-132">M<sub>out</sub> = Mₛ \* (M<sub>rc</sub>)-1 \* M<sub>r</sub> \* M<sub>rc</sub> \* Mₜ</span></span>

<span data-ttu-id="f0faf-133">dove:</span><span class="sxs-lookup"><span data-stu-id="f0faf-133">where:</span></span>

<span data-ttu-id="f0faf-134">M<sub>out</sub> = matrice di output (broncio)</span><span class="sxs-lookup"><span data-stu-id="f0faf-134">M<sub>out</sub> = output matrix (pOut)</span></span>

<span data-ttu-id="f0faf-135">MS = scala della matrice (scalabilità)</span><span class="sxs-lookup"><span data-stu-id="f0faf-135">Mₛ = scaling matrix (Scaling)</span></span>

<span data-ttu-id="f0faf-136">M<sub>RC</sub> = matrice Center of rotation (pRotationCenter)</span><span class="sxs-lookup"><span data-stu-id="f0faf-136">M<sub>rc</sub> = center of rotation matrix (pRotationCenter)</span></span>

<span data-ttu-id="f0faf-137">M<sub>r</sub> = matrice di rotazione (protation)</span><span class="sxs-lookup"><span data-stu-id="f0faf-137">M<sub>r</sub> = rotation matrix (pRotation)</span></span>

<span data-ttu-id="f0faf-138">Mt = matrice di traslazione (pTranslation)</span><span class="sxs-lookup"><span data-stu-id="f0faf-138">Mₜ = translation matrix (pTranslation)</span></span>

<span data-ttu-id="f0faf-139">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro broncio.</span><span class="sxs-lookup"><span data-stu-id="f0faf-139">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="f0faf-140">In questo modo, la funzione D3DXMatrixAffineTransformation può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="f0faf-140">In this way, the D3DXMatrixAffineTransformation function can be used as a parameter for another function.</span></span>

<span data-ttu-id="f0faf-141">Per le trasformazioni affini 2D, usare D3DXMatrixAffineTransformation2D.</span><span class="sxs-lookup"><span data-stu-id="f0faf-141">For 2D affine transformations, use D3DXMatrixAffineTransformation2D.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0faf-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f0faf-142">Requirements</span></span>



| <span data-ttu-id="f0faf-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0faf-143">Requirement</span></span> | <span data-ttu-id="f0faf-144">Valore</span><span class="sxs-lookup"><span data-stu-id="f0faf-144">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f0faf-145">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f0faf-145">Header</span></span><br/>  | <dl> <span data-ttu-id="f0faf-146"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0faf-146"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="f0faf-147">Libreria</span><span class="sxs-lookup"><span data-stu-id="f0faf-147">Library</span></span><br/> | <dl> <span data-ttu-id="f0faf-148"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f0faf-148"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f0faf-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f0faf-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0faf-150">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="f0faf-150">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
