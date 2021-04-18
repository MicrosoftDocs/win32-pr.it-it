---
description: Compila una matrice di trasformazione affine 2D nel piano XY. Gli argomenti NULL vengono considerati come trasformazioni di identità.
ms.assetid: 335de919-ae4d-405d-b6bb-ca6bdc2d568a
title: Funzione D3DXMatrixAffineTransformation2D (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a6edd0658eb80ec53d19b6c136a672cb78a2087b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322506"
---
# <a name="d3dxmatrixaffinetransformation2d-function-d3dx9mathh"></a><span data-ttu-id="ab18c-104">Funzione D3DXMatrixAffineTransformation2D (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="ab18c-104">D3DXMatrixAffineTransformation2D function (D3dx9math.h)</span></span>

<span data-ttu-id="ab18c-105">Compila una matrice di trasformazione affine 2D nel piano XY.</span><span class="sxs-lookup"><span data-stu-id="ab18c-105">Builds a 2D affine transformation matrix in the xy plane.</span></span> <span data-ttu-id="ab18c-106">Gli argomenti **null** vengono considerati come trasformazioni di identità.</span><span class="sxs-lookup"><span data-stu-id="ab18c-106">**NULL** arguments are treated as identity transformations.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab18c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ab18c-107">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixAffineTransformation2D(
  _Inout_       D3DXMATRIX  *pOut,
  _In_          FLOAT       Scaling,
  _In_    const D3DXVECTOR2 *pRotationCenter,
  _In_          FLOAT       Rotation,
  _In_    const D3DXVECTOR2 *pTranslation
);
```



## <a name="parameters"></a><span data-ttu-id="ab18c-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="ab18c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab18c-109">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="ab18c-109">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ab18c-110">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="ab18c-110">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="ab18c-111">Puntatore alla struttura [**D3DXMATRIX**](d3dxmatrix.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="ab18c-111">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="ab18c-112">*Ridimensionamento* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ab18c-112">*Scaling* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab18c-113">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ab18c-113">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ab18c-114">Fattore di scala.</span><span class="sxs-lookup"><span data-stu-id="ab18c-114">Scaling factor.</span></span>

</dd> <dt>

<span data-ttu-id="ab18c-115">*pRotationCenter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ab18c-115">*pRotationCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab18c-116">Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="ab18c-116">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="ab18c-117">Puntatore a una struttura [**D3DXVECTOR2**](d3dxvector2.md) , un punto che identifica il centro della rotazione.</span><span class="sxs-lookup"><span data-stu-id="ab18c-117">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure, a point identifying the center of rotation.</span></span> <span data-ttu-id="ab18c-118">Se questo argomento è **null**, una matrice Identity M <sub>RC</sub> viene applicata alla formula nelle osservazioni.</span><span class="sxs-lookup"><span data-stu-id="ab18c-118">If this argument is **NULL**, an identity M<sub>rc</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="ab18c-119">*Rotazione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ab18c-119">*Rotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab18c-120">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ab18c-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ab18c-121">Angolo di rotazione.</span><span class="sxs-lookup"><span data-stu-id="ab18c-121">The angle of rotation.</span></span>

</dd> <dt>

<span data-ttu-id="ab18c-122">*pTranslation* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ab18c-122">*pTranslation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab18c-123">Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="ab18c-123">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="ab18c-124">Puntatore a una struttura [**D3DXVECTOR2**](d3dxvector2.md) , che rappresenta la traduzione.</span><span class="sxs-lookup"><span data-stu-id="ab18c-124">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure, representing the translation.</span></span> <span data-ttu-id="ab18c-125">Se questo argomento è **null**, viene applicata una matrice di valori Identity mt alla formula nei commenti.</span><span class="sxs-lookup"><span data-stu-id="ab18c-125">If this argument is **NULL**, an identity Mₜ matrix is applied to the formula in Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab18c-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ab18c-126">Return value</span></span>

<span data-ttu-id="ab18c-127">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="ab18c-127">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="ab18c-128">Puntatore a una struttura [**D3DXMATRIX**](d3dxmatrix.md) che rappresenta una matrice di trasformazione affine.</span><span class="sxs-lookup"><span data-stu-id="ab18c-128">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is an affine transformation matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab18c-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="ab18c-129">Remarks</span></span>

<span data-ttu-id="ab18c-130">Questa funzione calcola la matrice di trasformazione affine con la formula seguente, con concatenazione di matrici valutata in ordine da sinistra a destra:</span><span class="sxs-lookup"><span data-stu-id="ab18c-130">This function calculates the affine transformation matrix with the following formula, with matrix concatenation evaluated in left-to-right order:</span></span>

<span data-ttu-id="ab18c-131">M<sub>out</sub> = MS \* (M<sub>RC</sub>) ⁻ ¹ \* m<sub>r</sub> \* m<sub>rc</sub> \* mt</span><span class="sxs-lookup"><span data-stu-id="ab18c-131">M<sub>out</sub> = Mₛ \* (M<sub>rc</sub>)⁻¹ \* M<sub>r</sub> \* M<sub>rc</sub> \* Mₜ</span></span>

<span data-ttu-id="ab18c-132">dove:</span><span class="sxs-lookup"><span data-stu-id="ab18c-132">where:</span></span>

<span data-ttu-id="ab18c-133">M <sub>out</sub> = matrice di output (*broncio*)</span><span class="sxs-lookup"><span data-stu-id="ab18c-133">M <sub>out</sub> = output matrix (*pOut*)</span></span>

<span data-ttu-id="ab18c-134">MS = scala della matrice (*scalabilità*)</span><span class="sxs-lookup"><span data-stu-id="ab18c-134">Mₛ = scaling matrix (*Scaling*)</span></span>

<span data-ttu-id="ab18c-135">M <sub>RC</sub> = matrice Center of rotation (*pRotationCenter*)</span><span class="sxs-lookup"><span data-stu-id="ab18c-135">M <sub>rc</sub> = center of rotation matrix (*pRotationCenter*)</span></span>

<span data-ttu-id="ab18c-136">M <sub>r</sub> = matrice di rotazione (*rotazione*)</span><span class="sxs-lookup"><span data-stu-id="ab18c-136">M <sub>r</sub> = rotation matrix (*Rotation*)</span></span>

<span data-ttu-id="ab18c-137">Mt = matrice di traslazione (*pTranslation*)</span><span class="sxs-lookup"><span data-stu-id="ab18c-137">Mₜ = translation matrix (*pTranslation*)</span></span>

<span data-ttu-id="ab18c-138">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro broncio.</span><span class="sxs-lookup"><span data-stu-id="ab18c-138">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="ab18c-139">In questo modo, la funzione **D3DXMatrixAffineTransformation2D** può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="ab18c-139">In this way, the **D3DXMatrixAffineTransformation2D** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="ab18c-140">Per le trasformazioni affini 3D, usare [**D3DXMatrixAffineTransformation**](d3dxmatrixaffinetransformation.md).</span><span class="sxs-lookup"><span data-stu-id="ab18c-140">For 3D affine transformations, use [**D3DXMatrixAffineTransformation**](d3dxmatrixaffinetransformation.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ab18c-141">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ab18c-141">Requirements</span></span>



| <span data-ttu-id="ab18c-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab18c-142">Requirement</span></span> | <span data-ttu-id="ab18c-143">Valore</span><span class="sxs-lookup"><span data-stu-id="ab18c-143">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ab18c-144">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ab18c-144">Header</span></span><br/>  | <dl> <span data-ttu-id="ab18c-145"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="ab18c-145"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="ab18c-146">Libreria</span><span class="sxs-lookup"><span data-stu-id="ab18c-146">Library</span></span><br/> | <dl> <span data-ttu-id="ab18c-147"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ab18c-147"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ab18c-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ab18c-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab18c-149">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="ab18c-149">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="ab18c-150">**D3DXMatrixTransformation2D**</span><span class="sxs-lookup"><span data-stu-id="ab18c-150">**D3DXMatrixTransformation2D**</span></span>](d3dxmatrixtransformation2d.md)
</dt> <dt>

[<span data-ttu-id="ab18c-151">Trasformazioni (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="ab18c-151">Transforms (Direct3D 9)</span></span>](transforms.md)
</dt> </dl>

 

 
