---
description: 'Funzione D3DXMatrixTransformation (D3dx9math.h): compila una matrice di trasformazione. Gli argomenti NULL vengono trattati come trasformazioni di identità.'
ms.assetid: 39042fc6-f489-4e44-ad3f-858ca395575d
title: Funzione D3DXMatrixTransformation (D3dx9math.h)
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
ms.openlocfilehash: dc3b6502a8015564207f208166cec15227d3b18a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098129"
---
# <a name="d3dxmatrixtransformation-function-d3dx9mathh"></a><span data-ttu-id="5190e-104">Funzione D3DXMatrixTransformation (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="5190e-104">D3DXMatrixTransformation function (D3dx9math.h)</span></span>

<span data-ttu-id="5190e-105">Compila una matrice di trasformazione.</span><span class="sxs-lookup"><span data-stu-id="5190e-105">Builds a transformation matrix.</span></span> <span data-ttu-id="5190e-106">**Gli** argomenti NULL vengono trattati come trasformazioni di identità.</span><span class="sxs-lookup"><span data-stu-id="5190e-106">**NULL** arguments are treated as identity transformations.</span></span>

## <a name="syntax"></a><span data-ttu-id="5190e-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5190e-107">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="5190e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="5190e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5190e-109">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="5190e-109">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5190e-110">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="5190e-110">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="5190e-111">Puntatore alla [**struttura D3DXMATRIX**](d3dxmatrix.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="5190e-111">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="5190e-112">*pScalingCenter* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="5190e-112">*pScalingCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5190e-113">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="5190e-113">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="5190e-114">Puntatore a una [**struttura D3DXVECTOR3,**](d3dxvector3.md) che identifica il punto centrale di ridimensionamento.</span><span class="sxs-lookup"><span data-stu-id="5190e-114">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, identifying the scaling center point.</span></span> <span data-ttu-id="5190e-115">Se questo argomento è **NULL,** viene applicata alla formula un'identità M <sub>sc</sub> matrix nelle osservazioni.</span><span class="sxs-lookup"><span data-stu-id="5190e-115">If this argument is **NULL**, an identity M<sub>sc</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="5190e-116">*pScalingRotation* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="5190e-116">*pScalingRotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5190e-117">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="5190e-117">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="5190e-118">Puntatore a una [**struttura D3DXQUATERNION**](d3dxquaternion.md) che specifica la rotazione di ridimensionamento.</span><span class="sxs-lookup"><span data-stu-id="5190e-118">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that specifies the scaling rotation.</span></span> <span data-ttu-id="5190e-119">Se questo argomento è **NULL,** una matrice identity M <sub>sr</sub> viene applicata alla formula nelle osservazioni.</span><span class="sxs-lookup"><span data-stu-id="5190e-119">If this argument is **NULL**, an identity M<sub>sr</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="5190e-120">*pScaling* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="5190e-120">*pScaling* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5190e-121">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="5190e-121">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="5190e-122">Puntatore a una [**struttura D3DXVECTOR3,**](d3dxvector3.md) il vettore di ridimensionamento.</span><span class="sxs-lookup"><span data-stu-id="5190e-122">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, the scaling vector.</span></span> <span data-ttu-id="5190e-123">Se questo argomento è **NULL,** alla formula in Osservazioni viene applicata una matrice Identity Ms.</span><span class="sxs-lookup"><span data-stu-id="5190e-123">If this argument is **NULL**, an identity Mₛ matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="5190e-124">*pRotationCenter* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="5190e-124">*pRotationCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5190e-125">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="5190e-125">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="5190e-126">Puntatore a [**una struttura D3DXVECTOR3,**](d3dxvector3.md) un punto che identifica il centro di rotazione.</span><span class="sxs-lookup"><span data-stu-id="5190e-126">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, a point that identifies the center of rotation.</span></span> <span data-ttu-id="5190e-127">Se questo argomento è **NULL,** alla formula in Osservazioni viene applicata una matrice identity M <sub>rc.</sub></span><span class="sxs-lookup"><span data-stu-id="5190e-127">If this argument is **NULL**, an identity M<sub>rc</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="5190e-128">*pRotation* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="5190e-128">*pRotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5190e-129">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="5190e-129">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="5190e-130">Puntatore a [**una struttura D3DXQUATERNION**](d3dxquaternion.md) che specifica la rotazione.</span><span class="sxs-lookup"><span data-stu-id="5190e-130">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that specifies the rotation.</span></span> <span data-ttu-id="5190e-131">Se questo argomento è **NULL,** alla formula in Osservazioni viene applicata una matrice identity M <sub>r.</sub></span><span class="sxs-lookup"><span data-stu-id="5190e-131">If this argument is **NULL**, an identity M<sub>r</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="5190e-132">*pTranslation* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="5190e-132">*pTranslation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5190e-133">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="5190e-133">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="5190e-134">Puntatore a [**una struttura D3DXVECTOR3,**](d3dxvector3.md) che rappresenta la traslazione.</span><span class="sxs-lookup"><span data-stu-id="5190e-134">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, representing the translation.</span></span> <span data-ttu-id="5190e-135">Se questo argomento è **NULL,** alla formula in Osservazioni viene applicata una matrice Identity Mt.</span><span class="sxs-lookup"><span data-stu-id="5190e-135">If this argument is **NULL**, an identity Mₜ matrix is applied to the formula in Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5190e-136">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5190e-136">Return value</span></span>

<span data-ttu-id="5190e-137">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="5190e-137">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="5190e-138">Puntatore a [**una struttura D3DXMATRIX**](d3dxmatrix.md) che rappresenta la matrice di trasformazione.</span><span class="sxs-lookup"><span data-stu-id="5190e-138">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is the transformation matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="5190e-139">Commenti</span><span class="sxs-lookup"><span data-stu-id="5190e-139">Remarks</span></span>

<span data-ttu-id="5190e-140">Questa funzione calcola la matrice di trasformazione con la formula seguente, con la concatenazione di matrici valutata in ordine da sinistra a destra:</span><span class="sxs-lookup"><span data-stu-id="5190e-140">This function calculates the transformation matrix with the following formula, with matrix concatenation evaluated in left-to-right order:</span></span>

<span data-ttu-id="5190e-141">M<sub>out</sub> = (M<sub>sc</sub>)⁻¹ \* (M<sub>sr</sub>)⁻¹ \* Ms \* M<sub>sr</sub> \* M<sub>sc</sub> \* (M<sub>rc</sub>)⁻¹ \* M<sub>r</sub> \* M<sub>rc</sub> \* Mt</span><span class="sxs-lookup"><span data-stu-id="5190e-141">M<sub>out</sub> = (M<sub>sc</sub>)⁻¹ \* (M<sub>sr</sub>)⁻¹\* Mₛ \* M<sub>sr</sub> \* M<sub>sc</sub> \* (M<sub>rc</sub>)⁻¹\* M<sub>r</sub> \* M<sub>rc</sub> \* Mt</span></span>

<span data-ttu-id="5190e-142">dove:</span><span class="sxs-lookup"><span data-stu-id="5190e-142">where:</span></span>

<span data-ttu-id="5190e-143">M <sub>out</sub> = matrice di output (*pOut*)</span><span class="sxs-lookup"><span data-stu-id="5190e-143">M <sub>out</sub> = output matrix (*pOut*)</span></span>

<span data-ttu-id="5190e-144">M <sub>sc</sub> = scalabilità della matrice centrale (*pScalingCenter*)</span><span class="sxs-lookup"><span data-stu-id="5190e-144">M <sub>sc</sub> = scaling center matrix (*pScalingCenter*)</span></span>

<span data-ttu-id="5190e-145">M <sub>sr</sub> = scalare la matrice di rotazione (*pScalingRotation*)</span><span class="sxs-lookup"><span data-stu-id="5190e-145">M <sub>sr</sub> = scaling rotation matrix (*pScalingRotation*)</span></span>

<span data-ttu-id="5190e-146">Ms = matrice di ridimensionamento (*pScaling*)</span><span class="sxs-lookup"><span data-stu-id="5190e-146">Mₛ = scaling matrix (*pScaling*)</span></span>

<span data-ttu-id="5190e-147">M <sub>rc</sub> = centro della matrice di rotazione (*pRotationCenter*)</span><span class="sxs-lookup"><span data-stu-id="5190e-147">M <sub>rc</sub> = center of rotation matrix (*pRotationCenter*)</span></span>

<span data-ttu-id="5190e-148">M <sub>r</sub> = matrice di rotazione (*pRotation*)</span><span class="sxs-lookup"><span data-stu-id="5190e-148">M <sub>r</sub> = rotation matrix (*pRotation*)</span></span>

<span data-ttu-id="5190e-149">Mt = matrice di traslazione (*pTranslation*)</span><span class="sxs-lookup"><span data-stu-id="5190e-149">Mₜ = translation matrix (*pTranslation*)</span></span>

<span data-ttu-id="5190e-150">Il valore restituito per questa funzione è lo stesso valore restituito nel *parametro pOut.*</span><span class="sxs-lookup"><span data-stu-id="5190e-150">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="5190e-151">In questo modo, la **funzione D3DXMatrixTransformation** può essere usata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="5190e-151">In this way, the **D3DXMatrixTransformation** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="5190e-152">Per le trasformazioni 2D, usare [**D3DXMatrixTransformation2D.**](d3dxmatrixtransformation2d.md)</span><span class="sxs-lookup"><span data-stu-id="5190e-152">For 2D transformations, use [**D3DXMatrixTransformation2D**](d3dxmatrixtransformation2d.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5190e-153">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5190e-153">Requirements</span></span>



| <span data-ttu-id="5190e-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="5190e-154">Requirement</span></span> | <span data-ttu-id="5190e-155">Valore</span><span class="sxs-lookup"><span data-stu-id="5190e-155">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5190e-156">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5190e-156">Header</span></span><br/>  | <dl> <span data-ttu-id="5190e-157"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="5190e-157"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="5190e-158">Libreria</span><span class="sxs-lookup"><span data-stu-id="5190e-158">Library</span></span><br/> | <dl> <span data-ttu-id="5190e-159"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="5190e-159"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5190e-160">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5190e-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5190e-161">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="5190e-161">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="5190e-162">**D3DXMatrixAffineTransformation**</span><span class="sxs-lookup"><span data-stu-id="5190e-162">**D3DXMatrixAffineTransformation**</span></span>](d3dxmatrixaffinetransformation.md)
</dt> <dt>

[<span data-ttu-id="5190e-163">Trasformazioni (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="5190e-163">Transforms (Direct3D 9)</span></span>](transforms.md)
</dt> </dl>

 

 




