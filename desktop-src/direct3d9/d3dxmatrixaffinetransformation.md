---
description: Compila una matrice di trasformazione affine 3D. Gli argomenti NULL vengono considerati come trasformazioni di identità.
ms.assetid: 54eac78f-57be-4a24-8dfb-0b519e97d6ca
title: Funzione D3DXMatrixAffineTransformation (D3dx9math. h)
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
ms.openlocfilehash: 025485f0015e6f2d85851c8f0919f5462b2bdc3e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355439"
---
# <a name="d3dxmatrixaffinetransformation-function-d3dx9mathh"></a><span data-ttu-id="a0df9-104">Funzione D3DXMatrixAffineTransformation (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="a0df9-104">D3DXMatrixAffineTransformation function (D3dx9math.h)</span></span>

<span data-ttu-id="a0df9-105">Compila una matrice di trasformazione affine 3D.</span><span class="sxs-lookup"><span data-stu-id="a0df9-105">Builds a 3D affine transformation matrix.</span></span> <span data-ttu-id="a0df9-106">Gli argomenti **null** vengono considerati come trasformazioni di identità.</span><span class="sxs-lookup"><span data-stu-id="a0df9-106">**NULL** arguments are treated as identity transformations.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0df9-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a0df9-107">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixAffineTransformation(
  _Inout_       D3DXMATRIX     *pOut,
  _In_          FLOAT          Scaling,
  _In_    const D3DXVECTOR3    *pRotationCenter,
  _In_    const D3DXQUATERNION *pRotation,
  _In_    const D3DXVECTOR3    *pTranslation
);
```



## <a name="parameters"></a><span data-ttu-id="a0df9-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="a0df9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0df9-109">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="a0df9-109">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a0df9-110">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="a0df9-110">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="a0df9-111">Puntatore alla struttura [**D3DXMATRIX**](d3dxmatrix.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="a0df9-111">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="a0df9-112">*Ridimensionamento* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a0df9-112">*Scaling* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0df9-113">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a0df9-113">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a0df9-114">Fattore di scala.</span><span class="sxs-lookup"><span data-stu-id="a0df9-114">Scaling factor.</span></span>

</dd> <dt>

<span data-ttu-id="a0df9-115">*pRotationCenter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a0df9-115">*pRotationCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0df9-116">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="a0df9-116">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="a0df9-117">Puntatore a una struttura [**D3DXVECTOR3**](d3dxvector3.md) , un punto che identifica il centro della rotazione.</span><span class="sxs-lookup"><span data-stu-id="a0df9-117">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, a point identifying the center of rotation.</span></span> <span data-ttu-id="a0df9-118">Se questo argomento è **null**, una matrice Identity M <sub>RC</sub> viene applicata alla formula nelle osservazioni.</span><span class="sxs-lookup"><span data-stu-id="a0df9-118">If this argument is **NULL**, an identity M<sub>rc</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="a0df9-119">*protazione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a0df9-119">*pRotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0df9-120">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="a0df9-120">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="a0df9-121">Puntatore a una struttura [**D3DXQUATERNION**](d3dxquaternion.md) che specifica la rotazione.</span><span class="sxs-lookup"><span data-stu-id="a0df9-121">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that specifies the rotation.</span></span> <span data-ttu-id="a0df9-122">Se questo argomento è **null**, una matrice di identità M <sub>r</sub> viene applicata alla formula nei commenti.</span><span class="sxs-lookup"><span data-stu-id="a0df9-122">If this argument is **NULL**, an identity M<sub>r</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="a0df9-123">*pTranslation* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a0df9-123">*pTranslation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0df9-124">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="a0df9-124">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="a0df9-125">Puntatore a una struttura [**D3DXVECTOR3**](d3dxvector3.md) che rappresenta la traduzione.</span><span class="sxs-lookup"><span data-stu-id="a0df9-125">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure representing the translation.</span></span> <span data-ttu-id="a0df9-126">Se questo argomento è **null**, viene applicata una matrice di valori Identity mt alla formula nei commenti.</span><span class="sxs-lookup"><span data-stu-id="a0df9-126">If this argument is **NULL**, an identity Mₜ matrix is applied to the formula in Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0df9-127">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a0df9-127">Return value</span></span>

<span data-ttu-id="a0df9-128">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="a0df9-128">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="a0df9-129">Puntatore a una struttura [**D3DXMATRIX**](d3dxmatrix.md) che rappresenta una matrice di trasformazione affine.</span><span class="sxs-lookup"><span data-stu-id="a0df9-129">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is an affine transformation matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0df9-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="a0df9-130">Remarks</span></span>

<span data-ttu-id="a0df9-131">Questa funzione calcola la matrice di trasformazione affine con la formula seguente, con concatenazione di matrici valutata in ordine da sinistra a destra:</span><span class="sxs-lookup"><span data-stu-id="a0df9-131">This function calculates the affine transformation matrix with the following formula, with matrix concatenation evaluated in left-to-right order:</span></span>

<span data-ttu-id="a0df9-132">M<sub>out</sub> = MS \* (M<sub>RC</sub>) ⁻ ¹ \* m<sub>r</sub> \* m<sub>rc</sub> \* mt</span><span class="sxs-lookup"><span data-stu-id="a0df9-132">M<sub>out</sub> = Mₛ \* (M<sub>rc</sub>)⁻¹ \* M<sub>r</sub> \* M<sub>rc</sub> \* Mₜ</span></span>

<span data-ttu-id="a0df9-133">dove:</span><span class="sxs-lookup"><span data-stu-id="a0df9-133">where:</span></span>

<span data-ttu-id="a0df9-134">M <sub>out</sub> = matrice di output (*broncio*)</span><span class="sxs-lookup"><span data-stu-id="a0df9-134">M <sub>out</sub> = output matrix (*pOut*)</span></span>

<span data-ttu-id="a0df9-135">MS = scala della matrice (*scalabilità*)</span><span class="sxs-lookup"><span data-stu-id="a0df9-135">Mₛ = scaling matrix (*Scaling*)</span></span>

<span data-ttu-id="a0df9-136">M <sub>RC</sub> = matrice Center of rotation (*pRotationCenter*)</span><span class="sxs-lookup"><span data-stu-id="a0df9-136">M <sub>rc</sub> = center of rotation matrix (*pRotationCenter*)</span></span>

<span data-ttu-id="a0df9-137">M <sub>r</sub> = matrice di rotazione (*protation*)</span><span class="sxs-lookup"><span data-stu-id="a0df9-137">M <sub>r</sub> = rotation matrix (*pRotation*)</span></span>

<span data-ttu-id="a0df9-138">Mt = matrice di traslazione (*pTranslation*)</span><span class="sxs-lookup"><span data-stu-id="a0df9-138">Mₜ = translation matrix (*pTranslation*)</span></span>

<span data-ttu-id="a0df9-139">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro broncio.</span><span class="sxs-lookup"><span data-stu-id="a0df9-139">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="a0df9-140">In questo modo, la funzione **D3DXMatrixAffineTransformation** può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="a0df9-140">In this way, the **D3DXMatrixAffineTransformation** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="a0df9-141">Per le trasformazioni affini 2D, usare [**D3DXMatrixAffineTransformation2D**](d3dxmatrixaffinetransformation2d.md).</span><span class="sxs-lookup"><span data-stu-id="a0df9-141">For 2D affine transformations, use [**D3DXMatrixAffineTransformation2D**](d3dxmatrixaffinetransformation2d.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a0df9-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a0df9-142">Requirements</span></span>



| <span data-ttu-id="a0df9-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0df9-143">Requirement</span></span> | <span data-ttu-id="a0df9-144">Valore</span><span class="sxs-lookup"><span data-stu-id="a0df9-144">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a0df9-145">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a0df9-145">Header</span></span><br/>  | <dl> <span data-ttu-id="a0df9-146"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0df9-146"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="a0df9-147">Libreria</span><span class="sxs-lookup"><span data-stu-id="a0df9-147">Library</span></span><br/> | <dl> <span data-ttu-id="a0df9-148"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a0df9-148"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a0df9-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a0df9-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0df9-150">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="a0df9-150">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="a0df9-151">**D3DXMatrixTransformation**</span><span class="sxs-lookup"><span data-stu-id="a0df9-151">**D3DXMatrixTransformation**</span></span>](d3dxmatrixtransformation.md)
</dt> <dt>

[<span data-ttu-id="a0df9-152">Trasformazioni (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="a0df9-152">Transforms (Direct3D 9)</span></span>](transforms.md)
</dt> </dl>

 

 
