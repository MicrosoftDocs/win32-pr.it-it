---
description: 'Funzione D3DXMatrixTransformation2D (D3DX10Math.h): compila una matrice di trasformazione 2D che rappresenta le trasformazioni nel piano xy. Gli argomenti NULL vengono considerati trasformazioni di identità.'
ms.assetid: 5b894c3b-a532-458a-bcbc-48fcd5c73c34
title: Funzione D3DXMatrixTransformation2D (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixTransformation2D
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 4ef112c346fd222f5e25935740e47ab62273628f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103359"
---
# <a name="d3dxmatrixtransformation2d-function-d3dx10mathh"></a><span data-ttu-id="54a15-104">Funzione D3DXMatrixTransformation2D (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="54a15-104">D3DXMatrixTransformation2D function (D3DX10Math.h)</span></span>

<span data-ttu-id="54a15-105">Compila una matrice di trasformazione 2D che rappresenta le trasformazioni nel piano xy.</span><span class="sxs-lookup"><span data-stu-id="54a15-105">Builds a 2D transformation matrix that represents transformations in the xy plane.</span></span> <span data-ttu-id="54a15-106">**Gli** argomenti NULL vengono considerati trasformazioni di identità.</span><span class="sxs-lookup"><span data-stu-id="54a15-106">**NULL** arguments are treated as identity transformations.</span></span>

## <a name="syntax"></a><span data-ttu-id="54a15-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="54a15-107">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixTransformation2D(
  _Inout_       D3DXMATRIX  *pOut,
  _In_    const D3DXVECTOR2 *pScalingCenter,
  _In_          FLOAT       ScalingRotation,
  _In_    const D3DXVECTOR2 *pScaling,
  _In_    const D3DXVECTOR2 *pRotationCenter,
  _In_          FLOAT       Rotation,
  _In_    const D3DXVECTOR2 *pTranslation
);
```



## <a name="parameters"></a><span data-ttu-id="54a15-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="54a15-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54a15-109">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="54a15-109">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="54a15-110">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="54a15-110">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="54a15-111">Puntatore alla [**struttura D3DXMATRIX**](d3d10-d3dxmatrix.md) che contiene il risultato delle trasformazioni.</span><span class="sxs-lookup"><span data-stu-id="54a15-111">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that contains the result of the transformations.</span></span>

</dd> <dt>

<span data-ttu-id="54a15-112">*pScalingCenter* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="54a15-112">*pScalingCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54a15-113">Tipo: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="54a15-113">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="54a15-114">Puntatore a [**un oggetto D3DXVECTOR2,**](d3d10-d3dxvector2.md)un punto che identifica il centro di ridimensionamento.</span><span class="sxs-lookup"><span data-stu-id="54a15-114">Pointer to a [**D3DXVECTOR2**](d3d10-d3dxvector2.md), a point identifying the scaling center.</span></span> <span data-ttu-id="54a15-115">Se questo argomento è **NULL,** alla formula in Osservazioni viene applicata una matrice identity M <sub>sc.</sub></span><span class="sxs-lookup"><span data-stu-id="54a15-115">If this argument is **NULL**, an identity M<sub>sc</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="54a15-116">*ScalingRotation* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="54a15-116">*ScalingRotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54a15-117">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="54a15-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="54a15-118">Puntatore al fattore di rotazione di ridimensionamento.</span><span class="sxs-lookup"><span data-stu-id="54a15-118">Pointer to the scaling rotation factor.</span></span>

</dd> <dt>

<span data-ttu-id="54a15-119">*pScaling* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="54a15-119">*pScaling* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54a15-120">Tipo: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="54a15-120">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="54a15-121">Puntatore a una struttura D3DXVECTOR2, un punto che identifica la scala.</span><span class="sxs-lookup"><span data-stu-id="54a15-121">Pointer to a D3DXVECTOR2 structure, a point identifying the scale.</span></span> <span data-ttu-id="54a15-122">Se questo argomento è **NULL,** alla formula in Osservazioni viene applicata una matrice Identity Ms.</span><span class="sxs-lookup"><span data-stu-id="54a15-122">If this argument is **NULL**, an identity Mₛ matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="54a15-123">*pRotationCenter* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="54a15-123">*pRotationCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54a15-124">Tipo: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="54a15-124">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="54a15-125">Puntatore a una struttura D3DXVECTOR2, un punto che identifica il centro di rotazione.</span><span class="sxs-lookup"><span data-stu-id="54a15-125">Pointer to a D3DXVECTOR2 structure, a point identifying the rotation center.</span></span> <span data-ttu-id="54a15-126">Se questo argomento è **NULL,** una matrice identity M <sub>rc</sub> viene applicata alla formula nelle osservazioni.</span><span class="sxs-lookup"><span data-stu-id="54a15-126">If this argument is **NULL**, an identity M<sub>rc</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="54a15-127">*Rotazione* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="54a15-127">*Rotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54a15-128">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="54a15-128">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="54a15-129">Angolo di rotazione in radianti.</span><span class="sxs-lookup"><span data-stu-id="54a15-129">The angle of rotation in radians.</span></span>

</dd> <dt>

<span data-ttu-id="54a15-130">*pTranslation* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="54a15-130">*pTranslation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54a15-131">Tipo: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="54a15-131">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="54a15-132">Puntatore a una struttura D3DXVECTOR2 che identifica la traslazione.</span><span class="sxs-lookup"><span data-stu-id="54a15-132">Pointer to a D3DXVECTOR2 structure, identifying the translation.</span></span> <span data-ttu-id="54a15-133">Se questo argomento è **NULL,** viene applicata una matrice Identity Mt alla formula in Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="54a15-133">If this argument is **NULL**, an identity Mₜ matrix is applied to the formula in Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54a15-134">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="54a15-134">Return value</span></span>

<span data-ttu-id="54a15-135">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="54a15-135">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="54a15-136">Puntatore a una struttura D3DXMATRIX che contiene la matrice di trasformazione.</span><span class="sxs-lookup"><span data-stu-id="54a15-136">Pointer to a D3DXMATRIX structure that contains the transformation matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="54a15-137">Commenti</span><span class="sxs-lookup"><span data-stu-id="54a15-137">Remarks</span></span>

<span data-ttu-id="54a15-138">Questa funzione calcola la matrice di trasformazione con la formula seguente, con la concatenazione di matrici valutata nell'ordine da sinistra a destra:</span><span class="sxs-lookup"><span data-stu-id="54a15-138">This function calculates the transformation matrix with the following formula, with matrix concatenation evaluated in left-to-right order:</span></span>

<span data-ttu-id="54a15-139">M<sub>out</sub> = (M<sub>sc</sub>)⁻ più \* (M<sub>sr</sub>)⁻ ms \* M \* <sub>sr</sub> \* M<sub>sc</sub> \* (M<sub>rc</sub>)⁻⁻ \* M<sub>r</sub> \* M<sub>rc</sub> \* Mt</span><span class="sxs-lookup"><span data-stu-id="54a15-139">M<sub>out</sub> = (M<sub>sc</sub>)⁻¹\* (M<sub>sr</sub>)⁻¹\* Mₛ \* M<sub>sr</sub> \* M<sub>sc</sub> \* (M<sub>rc</sub>)⁻¹\* M<sub>r</sub> \* M<sub>rc</sub> \* Mₜ</span></span>

<span data-ttu-id="54a15-140">dove:</span><span class="sxs-lookup"><span data-stu-id="54a15-140">where:</span></span>

<span data-ttu-id="54a15-141">M<sub>out</sub> = matrice di output (pOut)</span><span class="sxs-lookup"><span data-stu-id="54a15-141">M<sub>out</sub> = output matrix (pOut)</span></span>

<span data-ttu-id="54a15-142">M<sub>sc</sub> = matrice del centro di ridimensionamento (pScalingCenter)</span><span class="sxs-lookup"><span data-stu-id="54a15-142">M<sub>sc</sub> = scaling center matrix (pScalingCenter)</span></span>

<span data-ttu-id="54a15-143">M<sub>sr</sub> = matrice di rotazione di ridimensionamento (pScalingRotation)</span><span class="sxs-lookup"><span data-stu-id="54a15-143">M<sub>sr</sub> = scaling rotation matrix (pScalingRotation)</span></span>

<span data-ttu-id="54a15-144">Ms = matrice di ridimensionamento (pScaling)</span><span class="sxs-lookup"><span data-stu-id="54a15-144">Mₛ = scaling matrix (pScaling)</span></span>

<span data-ttu-id="54a15-145">M<sub>rc</sub> = centro della matrice di rotazione (pRotationCenter)</span><span class="sxs-lookup"><span data-stu-id="54a15-145">M<sub>rc</sub> = center of rotation matrix (pRotationCenter)</span></span>

<span data-ttu-id="54a15-146">M<sub>r</sub> = matrice di rotazione (rotazione)</span><span class="sxs-lookup"><span data-stu-id="54a15-146">M<sub>r</sub> = rotation matrix (Rotation)</span></span>

<span data-ttu-id="54a15-147">Mt = matrice di conversione (pTranslation)</span><span class="sxs-lookup"><span data-stu-id="54a15-147">Mₜ = translation matrix (pTranslation)</span></span>

<span data-ttu-id="54a15-148">Il valore restituito per questa funzione è lo stesso valore restituito nel parametro pOut.</span><span class="sxs-lookup"><span data-stu-id="54a15-148">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="54a15-149">In questo modo, la funzione D3DXMatrixTransformation2D può essere usata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="54a15-149">In this way, the D3DXMatrixTransformation2D function can be used as a parameter for another function.</span></span>

<span data-ttu-id="54a15-150">Per le trasformazioni 3D, usare [**D3DXMatrixTransformation**](d3d10-d3dxmatrixtransformation.md).</span><span class="sxs-lookup"><span data-stu-id="54a15-150">For 3D transformations, use [**D3DXMatrixTransformation**](d3d10-d3dxmatrixtransformation.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="54a15-151">Requisiti</span><span class="sxs-lookup"><span data-stu-id="54a15-151">Requirements</span></span>



| <span data-ttu-id="54a15-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="54a15-152">Requirement</span></span> | <span data-ttu-id="54a15-153">Valore</span><span class="sxs-lookup"><span data-stu-id="54a15-153">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="54a15-154">Intestazione</span><span class="sxs-lookup"><span data-stu-id="54a15-154">Header</span></span><br/>  | <dl> <span data-ttu-id="54a15-155"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="54a15-155"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="54a15-156">Libreria</span><span class="sxs-lookup"><span data-stu-id="54a15-156">Library</span></span><br/> | <dl> <span data-ttu-id="54a15-157"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="54a15-157"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="54a15-158">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="54a15-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54a15-159">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="54a15-159">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
