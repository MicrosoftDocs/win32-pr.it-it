---
description: Compila una matrice di trasformazione. Gli argomenti NULL vengono considerati come trasformazioni di identità.
ms.assetid: 39042fc6-f489-4e44-ad3f-858ca395575d
title: Funzione D3DXMatrixTransformation (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f2174329e01e3e624ef27608ca56b33181b770db
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104058586"
---
# <a name="d3dxmatrixtransformation-function-d3dx9mathh"></a><span data-ttu-id="ecd8d-104">Funzione D3DXMatrixTransformation (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="ecd8d-104">D3DXMatrixTransformation function (D3dx9math.h)</span></span>

<span data-ttu-id="ecd8d-105">Compila una matrice di trasformazione.</span><span class="sxs-lookup"><span data-stu-id="ecd8d-105">Builds a transformation matrix.</span></span> <span data-ttu-id="ecd8d-106">Gli argomenti **null** vengono considerati come trasformazioni di identità.</span><span class="sxs-lookup"><span data-stu-id="ecd8d-106">**NULL** arguments are treated as identity transformations.</span></span>

## <a name="syntax"></a><span data-ttu-id="ecd8d-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ecd8d-107">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="ecd8d-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="ecd8d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ecd8d-109">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="ecd8d-109">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ecd8d-110">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="ecd8d-110">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="ecd8d-111">Puntatore alla struttura [**D3DXMATRIX**](d3dxmatrix.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="ecd8d-111">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="ecd8d-112">*pScalingCenter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ecd8d-112">*pScalingCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ecd8d-113">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="ecd8d-113">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="ecd8d-114">Puntatore a una struttura [**D3DXVECTOR3**](d3dxvector3.md) , che identifica il punto centrale di ridimensionamento.</span><span class="sxs-lookup"><span data-stu-id="ecd8d-114">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, identifying the scaling center point.</span></span> <span data-ttu-id="ecd8d-115">Se questo argomento è **null**, una matrice Identity M <sub>SC</sub> viene applicata alla formula nei commenti.</span><span class="sxs-lookup"><span data-stu-id="ecd8d-115">If this argument is **NULL**, an identity M<sub>sc</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="ecd8d-116">*pScalingRotation* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ecd8d-116">*pScalingRotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ecd8d-117">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="ecd8d-117">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="ecd8d-118">Puntatore a una struttura [**D3DXQUATERNION**](d3dxquaternion.md) che specifica la rotazione di ridimensionamento.</span><span class="sxs-lookup"><span data-stu-id="ecd8d-118">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that specifies the scaling rotation.</span></span> <span data-ttu-id="ecd8d-119">Se questo argomento è **null**, una matrice Identity M <sub>SR</sub> viene applicata alla formula nei commenti.</span><span class="sxs-lookup"><span data-stu-id="ecd8d-119">If this argument is **NULL**, an identity M<sub>sr</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="ecd8d-120">*pScaling* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ecd8d-120">*pScaling* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ecd8d-121">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="ecd8d-121">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="ecd8d-122">Puntatore a una struttura [**D3DXVECTOR3**](d3dxvector3.md) , il vettore di ridimensionamento.</span><span class="sxs-lookup"><span data-stu-id="ecd8d-122">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, the scaling vector.</span></span> <span data-ttu-id="ecd8d-123">Se questo argomento è **null**, una matrice di identità MS viene applicata alla formula nei commenti.</span><span class="sxs-lookup"><span data-stu-id="ecd8d-123">If this argument is **NULL**, an identity Mₛ matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="ecd8d-124">*pRotationCenter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ecd8d-124">*pRotationCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ecd8d-125">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="ecd8d-125">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="ecd8d-126">Puntatore a una struttura [**D3DXVECTOR3**](d3dxvector3.md) , un punto che identifica il centro della rotazione.</span><span class="sxs-lookup"><span data-stu-id="ecd8d-126">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, a point that identifies the center of rotation.</span></span> <span data-ttu-id="ecd8d-127">Se questo argomento è **null**, una matrice Identity M <sub>RC</sub> viene applicata alla formula nelle osservazioni.</span><span class="sxs-lookup"><span data-stu-id="ecd8d-127">If this argument is **NULL**, an identity M<sub>rc</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="ecd8d-128">*protazione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ecd8d-128">*pRotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ecd8d-129">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="ecd8d-129">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="ecd8d-130">Puntatore a una struttura [**D3DXQUATERNION**](d3dxquaternion.md) che specifica la rotazione.</span><span class="sxs-lookup"><span data-stu-id="ecd8d-130">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that specifies the rotation.</span></span> <span data-ttu-id="ecd8d-131">Se questo argomento è **null**, una matrice di identità M <sub>r</sub> viene applicata alla formula nei commenti.</span><span class="sxs-lookup"><span data-stu-id="ecd8d-131">If this argument is **NULL**, an identity M<sub>r</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="ecd8d-132">*pTranslation* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ecd8d-132">*pTranslation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ecd8d-133">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="ecd8d-133">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="ecd8d-134">Puntatore a una struttura [**D3DXVECTOR3**](d3dxvector3.md) , che rappresenta la traduzione.</span><span class="sxs-lookup"><span data-stu-id="ecd8d-134">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, representing the translation.</span></span> <span data-ttu-id="ecd8d-135">Se questo argomento è **null**, viene applicata una matrice di valori Identity mt alla formula nei commenti.</span><span class="sxs-lookup"><span data-stu-id="ecd8d-135">If this argument is **NULL**, an identity Mₜ matrix is applied to the formula in Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ecd8d-136">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ecd8d-136">Return value</span></span>

<span data-ttu-id="ecd8d-137">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="ecd8d-137">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="ecd8d-138">Puntatore a una struttura [**D3DXMATRIX**](d3dxmatrix.md) che rappresenta la matrice di trasformazione.</span><span class="sxs-lookup"><span data-stu-id="ecd8d-138">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is the transformation matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="ecd8d-139">Commenti</span><span class="sxs-lookup"><span data-stu-id="ecd8d-139">Remarks</span></span>

<span data-ttu-id="ecd8d-140">Questa funzione calcola la matrice di trasformazione con la formula seguente, con concatenazione di matrici valutata in ordine da sinistra a destra:</span><span class="sxs-lookup"><span data-stu-id="ecd8d-140">This function calculates the transformation matrix with the following formula, with matrix concatenation evaluated in left-to-right order:</span></span>

<span data-ttu-id="ecd8d-141">M<sub>out</sub> = (m<sub>SC</sub>) ⁻ ¹ \* (m<sub>SR</sub>) ⁻ ¹ \* MS \* m<sub>SR</sub> \* m<sub>SC</sub> \* (m<sub>RC</sub>) ⁻ ¹ \* M<sub>r</sub> \* m<sub>RC</sub> \* mt</span><span class="sxs-lookup"><span data-stu-id="ecd8d-141">M<sub>out</sub> = (M<sub>sc</sub>)⁻¹ \* (M<sub>sr</sub>)⁻¹\* Mₛ \* M<sub>sr</sub> \* M<sub>sc</sub> \* (M<sub>rc</sub>)⁻¹\* M<sub>r</sub> \* M<sub>rc</sub> \* Mt</span></span>

<span data-ttu-id="ecd8d-142">dove:</span><span class="sxs-lookup"><span data-stu-id="ecd8d-142">where:</span></span>

<span data-ttu-id="ecd8d-143">M <sub>out</sub> = matrice di output (*broncio*)</span><span class="sxs-lookup"><span data-stu-id="ecd8d-143">M <sub>out</sub> = output matrix (*pOut*)</span></span>

<span data-ttu-id="ecd8d-144">M <sub>SC</sub> = scala Center Matrix (*pScalingCenter*)</span><span class="sxs-lookup"><span data-stu-id="ecd8d-144">M <sub>sc</sub> = scaling center matrix (*pScalingCenter*)</span></span>

<span data-ttu-id="ecd8d-145">M <sub>Sr</sub> = scala della matrice di rotazione (*pScalingRotation*)</span><span class="sxs-lookup"><span data-stu-id="ecd8d-145">M <sub>sr</sub> = scaling rotation matrix (*pScalingRotation*)</span></span>

<span data-ttu-id="ecd8d-146">MS = scala Matrix (*pScaling*)</span><span class="sxs-lookup"><span data-stu-id="ecd8d-146">Mₛ = scaling matrix (*pScaling*)</span></span>

<span data-ttu-id="ecd8d-147">M <sub>RC</sub> = matrice Center of rotation (*pRotationCenter*)</span><span class="sxs-lookup"><span data-stu-id="ecd8d-147">M <sub>rc</sub> = center of rotation matrix (*pRotationCenter*)</span></span>

<span data-ttu-id="ecd8d-148">M <sub>r</sub> = matrice di rotazione (*protation*)</span><span class="sxs-lookup"><span data-stu-id="ecd8d-148">M <sub>r</sub> = rotation matrix (*pRotation*)</span></span>

<span data-ttu-id="ecd8d-149">Mt = matrice di traslazione (*pTranslation*)</span><span class="sxs-lookup"><span data-stu-id="ecd8d-149">Mₜ = translation matrix (*pTranslation*)</span></span>

<span data-ttu-id="ecd8d-150">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro *broncio* .</span><span class="sxs-lookup"><span data-stu-id="ecd8d-150">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="ecd8d-151">In questo modo, la funzione **D3DXMatrixTransformation** può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="ecd8d-151">In this way, the **D3DXMatrixTransformation** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="ecd8d-152">Per le trasformazioni 2D, usare [**D3DXMatrixTransformation2D**](d3dxmatrixtransformation2d.md).</span><span class="sxs-lookup"><span data-stu-id="ecd8d-152">For 2D transformations, use [**D3DXMatrixTransformation2D**](d3dxmatrixtransformation2d.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ecd8d-153">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ecd8d-153">Requirements</span></span>



| <span data-ttu-id="ecd8d-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="ecd8d-154">Requirement</span></span> | <span data-ttu-id="ecd8d-155">Valore</span><span class="sxs-lookup"><span data-stu-id="ecd8d-155">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ecd8d-156">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ecd8d-156">Header</span></span><br/>  | <dl> <span data-ttu-id="ecd8d-157"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="ecd8d-157"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="ecd8d-158">Libreria</span><span class="sxs-lookup"><span data-stu-id="ecd8d-158">Library</span></span><br/> | <dl> <span data-ttu-id="ecd8d-159"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ecd8d-159"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ecd8d-160">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ecd8d-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecd8d-161">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="ecd8d-161">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="ecd8d-162">**D3DXMatrixAffineTransformation**</span><span class="sxs-lookup"><span data-stu-id="ecd8d-162">**D3DXMatrixAffineTransformation**</span></span>](d3dxmatrixaffinetransformation.md)
</dt> <dt>

[<span data-ttu-id="ecd8d-163">Trasformazioni (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="ecd8d-163">Transforms (Direct3D 9)</span></span>](transforms.md)
</dt> </dl>

 

 




