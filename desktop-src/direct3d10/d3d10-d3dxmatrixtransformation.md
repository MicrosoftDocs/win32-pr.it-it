---
description: Compila una matrice di trasformazione. Gli argomenti NULL vengono considerati come trasformazioni di identità.
ms.assetid: 99c75ce9-3683-4753-b635-760eb8aaf46e
title: Funzione D3DXMatrixTransformation (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixTransformation
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: db1d88ad04e4aaa51232cfdba3168779805b22c3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323401"
---
# <a name="d3dxmatrixtransformation-function-d3dx10mathh"></a><span data-ttu-id="29ae7-104">Funzione D3DXMatrixTransformation (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="29ae7-104">D3DXMatrixTransformation function (D3DX10Math.h)</span></span>

<span data-ttu-id="29ae7-105">Compila una matrice di trasformazione.</span><span class="sxs-lookup"><span data-stu-id="29ae7-105">Builds a transformation matrix.</span></span> <span data-ttu-id="29ae7-106">Gli argomenti **null** vengono considerati come trasformazioni di identità.</span><span class="sxs-lookup"><span data-stu-id="29ae7-106">**NULL** arguments are treated as identity transformations.</span></span>

## <a name="syntax"></a><span data-ttu-id="29ae7-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="29ae7-107">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixTransformation(
  _Inout_       D3DXMATRIX     *pOut,
  _In_    const D3DXVECTOR3    *pScalingCenter,
  _In_    const D3DXQUATERNION *pScalingRotation,
  _In_    const D3DXVECTOR3    *pScaling,
  _In_    const D3DXVECTOR3    *pRotationCenter,
  _In_    const D3DXQUATERNION *pRotation,
  _In_    const D3DXVECTOR3    *pTranslation
);
```



## <a name="parameters"></a><span data-ttu-id="29ae7-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="29ae7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29ae7-109">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="29ae7-109">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="29ae7-110">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="29ae7-110">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="29ae7-111">Puntatore alla struttura [**D3DXMATRIX**](d3d10-d3dxmatrix.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="29ae7-111">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="29ae7-112">*pScalingCenter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="29ae7-112">*pScalingCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29ae7-113">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="29ae7-113">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="29ae7-114">Puntatore a un [**D3DXVECTOR3**](d3d10-d3dxvector3.md), che identifica il punto centrale di ridimensionamento.</span><span class="sxs-lookup"><span data-stu-id="29ae7-114">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md), identifying the scaling center point.</span></span> <span data-ttu-id="29ae7-115">Se questo argomento è **null**, una matrice Identity M <sub>SC</sub> viene applicata alla formula nei commenti.</span><span class="sxs-lookup"><span data-stu-id="29ae7-115">If this argument is **NULL**, an identity M<sub>sc</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="29ae7-116">*pScalingRotation* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="29ae7-116">*pScalingRotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29ae7-117">Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="29ae7-117">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="29ae7-118">Puntatore a un [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) che specifica la rotazione di ridimensionamento.</span><span class="sxs-lookup"><span data-stu-id="29ae7-118">Pointer to a [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that specifies the scaling rotation.</span></span> <span data-ttu-id="29ae7-119">Se questo argomento è **null**, una matrice Identity M <sub>SR</sub> viene applicata alla formula nei commenti.</span><span class="sxs-lookup"><span data-stu-id="29ae7-119">If this argument is **NULL**, an identity M<sub>sr</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="29ae7-120">*pScaling* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="29ae7-120">*pScaling* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29ae7-121">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="29ae7-121">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="29ae7-122">Puntatore a una struttura D3DXVECTOR3, il vettore di ridimensionamento.</span><span class="sxs-lookup"><span data-stu-id="29ae7-122">Pointer to a D3DXVECTOR3 structure, the scaling vector.</span></span> <span data-ttu-id="29ae7-123">Se questo argomento è **null**, una matrice di identità MS viene applicata alla formula nei commenti.</span><span class="sxs-lookup"><span data-stu-id="29ae7-123">If this argument is **NULL**, an identity Mₛ matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="29ae7-124">*pRotationCenter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="29ae7-124">*pRotationCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29ae7-125">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="29ae7-125">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="29ae7-126">Puntatore a una struttura D3DXVECTOR3, un punto che identifica il centro della rotazione.</span><span class="sxs-lookup"><span data-stu-id="29ae7-126">Pointer to a D3DXVECTOR3 structure, a point that identifies the center of rotation.</span></span> <span data-ttu-id="29ae7-127">Se questo argomento è **null**, una matrice Identity M <sub>RC</sub> viene applicata alla formula nelle osservazioni.</span><span class="sxs-lookup"><span data-stu-id="29ae7-127">If this argument is **NULL**, an identity M<sub>rc</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="29ae7-128">*protazione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="29ae7-128">*pRotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29ae7-129">Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="29ae7-129">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="29ae7-130">Puntatore a una struttura D3DXQUATERNION che specifica la rotazione.</span><span class="sxs-lookup"><span data-stu-id="29ae7-130">Pointer to a D3DXQUATERNION structure that specifies the rotation.</span></span> <span data-ttu-id="29ae7-131">Se questo argomento è **null**, una matrice di identità M <sub>r</sub> viene applicata alla formula nei commenti.</span><span class="sxs-lookup"><span data-stu-id="29ae7-131">If this argument is **NULL**, an identity M<sub>r</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="29ae7-132">*pTranslation* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="29ae7-132">*pTranslation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29ae7-133">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="29ae7-133">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="29ae7-134">Puntatore a una struttura D3DXVECTOR3, che rappresenta la traduzione.</span><span class="sxs-lookup"><span data-stu-id="29ae7-134">Pointer to a D3DXVECTOR3 structure, representing the translation.</span></span> <span data-ttu-id="29ae7-135">Se questo argomento è **null**, viene applicata una matrice di valori Identity mt alla formula nei commenti.</span><span class="sxs-lookup"><span data-stu-id="29ae7-135">If this argument is **NULL**, an identity Mₜ matrix is applied to the formula in Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29ae7-136">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="29ae7-136">Return value</span></span>

<span data-ttu-id="29ae7-137">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="29ae7-137">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="29ae7-138">Puntatore a una struttura D3DXMATRIX che rappresenta la matrice di trasformazione.</span><span class="sxs-lookup"><span data-stu-id="29ae7-138">Pointer to a D3DXMATRIX structure that is the transformation matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="29ae7-139">Commenti</span><span class="sxs-lookup"><span data-stu-id="29ae7-139">Remarks</span></span>

<span data-ttu-id="29ae7-140">Questa funzione calcola la matrice di trasformazione con la formula seguente, con concatenazione di matrici valutata in ordine da sinistra a destra:</span><span class="sxs-lookup"><span data-stu-id="29ae7-140">This function calculates the transformation matrix with the following formula, with matrix concatenation evaluated in left-to-right order:</span></span>

<span data-ttu-id="29ae7-141">M<sub>out</sub> = (m<sub>SC</sub>) ⁻ ¹ \* (m<sub>SR</sub>) ⁻ ¹ \* MS \* m<sub>SR</sub> \* m<sub>SC</sub> \* (m<sub>RC</sub>) ⁻ ¹ \* M<sub>r</sub> \* m<sub>RC</sub> \* mt</span><span class="sxs-lookup"><span data-stu-id="29ae7-141">M<sub>out</sub> = (M<sub>sc</sub>)⁻¹ \* (M<sub>sr</sub>)⁻¹\* Mₛ \* M<sub>sr</sub> \* M<sub>sc</sub> \* (M<sub>rc</sub>)⁻¹\* M<sub>r</sub> \* M<sub>rc</sub> \* Mt</span></span>

<span data-ttu-id="29ae7-142">dove:</span><span class="sxs-lookup"><span data-stu-id="29ae7-142">where:</span></span>

<span data-ttu-id="29ae7-143">M<sub>out</sub> = matrice di output (broncio)</span><span class="sxs-lookup"><span data-stu-id="29ae7-143">M<sub>out</sub> = output matrix (pOut)</span></span>

<span data-ttu-id="29ae7-144">M<sub>SC</sub> = scala Center Matrix (pScalingCenter)</span><span class="sxs-lookup"><span data-stu-id="29ae7-144">M<sub>sc</sub> = scaling center matrix (pScalingCenter)</span></span>

<span data-ttu-id="29ae7-145">M<sub>Sr</sub> = scala della matrice di rotazione (pScalingRotation)</span><span class="sxs-lookup"><span data-stu-id="29ae7-145">M<sub>sr</sub> = scaling rotation matrix (pScalingRotation)</span></span>

<span data-ttu-id="29ae7-146">MS = scala Matrix (pScaling)</span><span class="sxs-lookup"><span data-stu-id="29ae7-146">Mₛ = scaling matrix (pScaling)</span></span>

<span data-ttu-id="29ae7-147">M<sub>RC</sub> = matrice Center of rotation (pRotationCenter)</span><span class="sxs-lookup"><span data-stu-id="29ae7-147">M<sub>rc</sub> = center of rotation matrix (pRotationCenter)</span></span>

<span data-ttu-id="29ae7-148">M<sub>r</sub> = matrice di rotazione (protation)</span><span class="sxs-lookup"><span data-stu-id="29ae7-148">M<sub>r</sub> = rotation matrix (pRotation)</span></span>

<span data-ttu-id="29ae7-149">Mt = matrice di traslazione (pTranslation)</span><span class="sxs-lookup"><span data-stu-id="29ae7-149">Mₜ = translation matrix (pTranslation)</span></span>

<span data-ttu-id="29ae7-150">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro broncio.</span><span class="sxs-lookup"><span data-stu-id="29ae7-150">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="29ae7-151">In questo modo, la funzione D3DXMatrixTransformation può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="29ae7-151">In this way, the D3DXMatrixTransformation function can be used as a parameter for another function.</span></span>

<span data-ttu-id="29ae7-152">Per le trasformazioni 2D, usare [**D3DXMatrixTransformation2D**](d3d10-d3dxmatrixtransformation2d.md).</span><span class="sxs-lookup"><span data-stu-id="29ae7-152">For 2D transformations, use [**D3DXMatrixTransformation2D**](d3d10-d3dxmatrixtransformation2d.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="29ae7-153">Requisiti</span><span class="sxs-lookup"><span data-stu-id="29ae7-153">Requirements</span></span>



| <span data-ttu-id="29ae7-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="29ae7-154">Requirement</span></span> | <span data-ttu-id="29ae7-155">Valore</span><span class="sxs-lookup"><span data-stu-id="29ae7-155">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="29ae7-156">Intestazione</span><span class="sxs-lookup"><span data-stu-id="29ae7-156">Header</span></span><br/>  | <dl> <span data-ttu-id="29ae7-157"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="29ae7-157"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="29ae7-158">Libreria</span><span class="sxs-lookup"><span data-stu-id="29ae7-158">Library</span></span><br/> | <dl> <span data-ttu-id="29ae7-159"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="29ae7-159"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="29ae7-160">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="29ae7-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29ae7-161">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="29ae7-161">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
