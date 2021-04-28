---
description: 'Funzione D3DXMatrixAffineTransformation (D3dx9math.h): compila una matrice di trasformazione affine 3D. Gli argomenti NULL vengono trattati come trasformazioni di identità.'
ms.assetid: 54eac78f-57be-4a24-8dfb-0b519e97d6ca
title: Funzione D3DXMatrixAffineTransformation (D3dx9math.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7329ffbffe5ffd89ed64e5386246f39699618960
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094169"
---
# <a name="d3dxmatrixaffinetransformation-function-d3dx9mathh"></a><span data-ttu-id="faa11-104">Funzione D3DXMatrixAffineTransformation (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="faa11-104">D3DXMatrixAffineTransformation function (D3dx9math.h)</span></span>

<span data-ttu-id="faa11-105">Compila una matrice di trasformazione affine 3D.</span><span class="sxs-lookup"><span data-stu-id="faa11-105">Builds a 3D affine transformation matrix.</span></span> <span data-ttu-id="faa11-106">**Gli** argomenti NULL vengono trattati come trasformazioni di identità.</span><span class="sxs-lookup"><span data-stu-id="faa11-106">**NULL** arguments are treated as identity transformations.</span></span>

## <a name="syntax"></a><span data-ttu-id="faa11-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="faa11-107">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixAffineTransformation(
  _Inout_       D3DXMATRIX     *pOut,
  _In_          FLOAT          Scaling,
  _In_    const D3DXVECTOR3    *pRotationCenter,
  _In_    const D3DXQUATERNION *pRotation,
  _In_    const D3DXVECTOR3    *pTranslation
);
```



## <a name="parameters"></a><span data-ttu-id="faa11-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="faa11-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="faa11-109">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="faa11-109">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="faa11-110">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="faa11-110">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="faa11-111">Puntatore alla [**struttura D3DXMATRIX**](d3dxmatrix.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="faa11-111">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="faa11-112">*Ridimensionamento* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="faa11-112">*Scaling* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="faa11-113">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="faa11-113">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="faa11-114">Fattore di scala.</span><span class="sxs-lookup"><span data-stu-id="faa11-114">Scaling factor.</span></span>

</dd> <dt>

<span data-ttu-id="faa11-115">*pRotationCenter* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="faa11-115">*pRotationCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="faa11-116">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="faa11-116">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="faa11-117">Puntatore a [**una struttura D3DXVECTOR3,**](d3dxvector3.md) un punto che identifica il centro di rotazione.</span><span class="sxs-lookup"><span data-stu-id="faa11-117">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, a point identifying the center of rotation.</span></span> <span data-ttu-id="faa11-118">Se questo argomento è **NULL,** una matrice identity M <sub>rc</sub> viene applicata alla formula nelle osservazioni.</span><span class="sxs-lookup"><span data-stu-id="faa11-118">If this argument is **NULL**, an identity M<sub>rc</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="faa11-119">*pRotation* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="faa11-119">*pRotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="faa11-120">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="faa11-120">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="faa11-121">Puntatore a [**una struttura D3DXQUATERNION**](d3dxquaternion.md) che specifica la rotazione.</span><span class="sxs-lookup"><span data-stu-id="faa11-121">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that specifies the rotation.</span></span> <span data-ttu-id="faa11-122">Se questo argomento è **NULL,** una matrice di identità M <sub>r</sub> viene applicata alla formula nelle osservazioni.</span><span class="sxs-lookup"><span data-stu-id="faa11-122">If this argument is **NULL**, an identity M<sub>r</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="faa11-123">*pTranslation* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="faa11-123">*pTranslation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="faa11-124">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="faa11-124">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="faa11-125">Puntatore a [**una struttura D3DXVECTOR3**](d3dxvector3.md) che rappresenta la traslazione.</span><span class="sxs-lookup"><span data-stu-id="faa11-125">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure representing the translation.</span></span> <span data-ttu-id="faa11-126">Se questo argomento è **NULL,** alla formula in Osservazioni viene applicata una matrice Identity Mt.</span><span class="sxs-lookup"><span data-stu-id="faa11-126">If this argument is **NULL**, an identity Mₜ matrix is applied to the formula in Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="faa11-127">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="faa11-127">Return value</span></span>

<span data-ttu-id="faa11-128">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="faa11-128">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="faa11-129">Puntatore a [**una struttura D3DXMATRIX**](d3dxmatrix.md) che è una matrice di trasformazione affine.</span><span class="sxs-lookup"><span data-stu-id="faa11-129">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is an affine transformation matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="faa11-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="faa11-130">Remarks</span></span>

<span data-ttu-id="faa11-131">Questa funzione calcola la matrice di trasformazione affine con la formula seguente, con la concatenazione di matrici valutata in ordine da sinistra a destra:</span><span class="sxs-lookup"><span data-stu-id="faa11-131">This function calculates the affine transformation matrix with the following formula, with matrix concatenation evaluated in left-to-right order:</span></span>

<span data-ttu-id="faa11-132">M<sub>out</sub> = Ms \* (M<sub>rc</sub>)⁻¹ \* M<sub>r</sub> \* M<sub>rc</sub> \* Mt</span><span class="sxs-lookup"><span data-stu-id="faa11-132">M<sub>out</sub> = Mₛ \* (M<sub>rc</sub>)⁻¹ \* M<sub>r</sub> \* M<sub>rc</sub> \* Mₜ</span></span>

<span data-ttu-id="faa11-133">dove:</span><span class="sxs-lookup"><span data-stu-id="faa11-133">where:</span></span>

<span data-ttu-id="faa11-134">M <sub>out</sub> = matrice di output (*pOut*)</span><span class="sxs-lookup"><span data-stu-id="faa11-134">M <sub>out</sub> = output matrix (*pOut*)</span></span>

<span data-ttu-id="faa11-135">Ms = matrice di ridimensionamento (*ridimensionamento*)</span><span class="sxs-lookup"><span data-stu-id="faa11-135">Mₛ = scaling matrix (*Scaling*)</span></span>

<span data-ttu-id="faa11-136">M <sub>rc</sub> = centro della matrice di rotazione (*pRotationCenter*)</span><span class="sxs-lookup"><span data-stu-id="faa11-136">M <sub>rc</sub> = center of rotation matrix (*pRotationCenter*)</span></span>

<span data-ttu-id="faa11-137">M <sub>r</sub> = matrice di rotazione (*pRotation*)</span><span class="sxs-lookup"><span data-stu-id="faa11-137">M <sub>r</sub> = rotation matrix (*pRotation*)</span></span>

<span data-ttu-id="faa11-138">Mt = matrice di conversione (*pTranslation*)</span><span class="sxs-lookup"><span data-stu-id="faa11-138">Mₜ = translation matrix (*pTranslation*)</span></span>

<span data-ttu-id="faa11-139">Il valore restituito per questa funzione è lo stesso valore restituito nel parametro pOut.</span><span class="sxs-lookup"><span data-stu-id="faa11-139">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="faa11-140">In questo modo, la **funzione D3DXMatrixAffineTransformation** può essere usata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="faa11-140">In this way, the **D3DXMatrixAffineTransformation** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="faa11-141">Per le trasformazioni affine 2D, usare [**D3DXMatrixAffineTransformation2D**](d3dxmatrixaffinetransformation2d.md).</span><span class="sxs-lookup"><span data-stu-id="faa11-141">For 2D affine transformations, use [**D3DXMatrixAffineTransformation2D**](d3dxmatrixaffinetransformation2d.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="faa11-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="faa11-142">Requirements</span></span>



| <span data-ttu-id="faa11-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="faa11-143">Requirement</span></span> | <span data-ttu-id="faa11-144">Valore</span><span class="sxs-lookup"><span data-stu-id="faa11-144">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="faa11-145">Intestazione</span><span class="sxs-lookup"><span data-stu-id="faa11-145">Header</span></span><br/>  | <dl> <span data-ttu-id="faa11-146"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="faa11-146"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="faa11-147">Libreria</span><span class="sxs-lookup"><span data-stu-id="faa11-147">Library</span></span><br/> | <dl> <span data-ttu-id="faa11-148"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="faa11-148"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="faa11-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="faa11-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="faa11-150">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="faa11-150">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="faa11-151">**D3DXMatrixTransformation**</span><span class="sxs-lookup"><span data-stu-id="faa11-151">**D3DXMatrixTransformation**</span></span>](d3dxmatrixtransformation.md)
</dt> <dt>

[<span data-ttu-id="faa11-152">Trasformazioni (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="faa11-152">Transforms (Direct3D 9)</span></span>](transforms.md)
</dt> </dl>

 

 
