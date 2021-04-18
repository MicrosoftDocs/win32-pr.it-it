---
description: Compila una matrice di proiezione ortogonale personalizzata, a sinistra.
ms.assetid: 84175c08-5a0b-4183-afe2-8aecafd73897
title: Funzione D3DXMatrixOrthoOffCenterLH (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixOrthoOffCenterLH
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 4292f2996b4a19b71531094e5bf39bf7c213b972
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323214"
---
# <a name="d3dxmatrixorthooffcenterlh-function-d3dx10mathh"></a><span data-ttu-id="f20ab-103">Funzione D3DXMatrixOrthoOffCenterLH (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="f20ab-103">D3DXMatrixOrthoOffCenterLH function (D3DX10Math.h)</span></span>

<span data-ttu-id="f20ab-104">Compila una matrice di proiezione ortogonale personalizzata, a sinistra.</span><span class="sxs-lookup"><span data-stu-id="f20ab-104">Builds a customized, left-handed orthographic projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="f20ab-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f20ab-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixOrthoOffCenterLH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      l,
  _In_    FLOAT      r,
  _In_    FLOAT      b,
  _In_    FLOAT      t,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="f20ab-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f20ab-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f20ab-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="f20ab-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f20ab-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="f20ab-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="f20ab-109">Puntatore al [**D3DXMATRIX**](d3d10-d3dxmatrix.md)risultante.</span><span class="sxs-lookup"><span data-stu-id="f20ab-109">Pointer to the resulting [**D3DXMATRIX**](d3d10-d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="f20ab-110">*l* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f20ab-110">*l* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f20ab-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f20ab-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f20ab-112">Valore x minimo del volume di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="f20ab-112">Minimum x-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="f20ab-113">*r* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f20ab-113">*r* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f20ab-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f20ab-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f20ab-115">Valore x massimo del volume di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="f20ab-115">Maximum x-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="f20ab-116">*b* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f20ab-116">*b* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f20ab-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f20ab-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f20ab-118">Valore y minimo del volume di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="f20ab-118">Minimum y-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="f20ab-119">*t* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f20ab-119">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f20ab-120">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f20ab-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f20ab-121">Valore y massimo del volume di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="f20ab-121">Maximum y-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="f20ab-122">*Zn* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f20ab-122">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f20ab-123">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f20ab-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f20ab-124">Valore z minimo del volume di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="f20ab-124">Minimum z-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="f20ab-125">*ZF* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f20ab-125">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f20ab-126">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f20ab-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f20ab-127">Valore z massimo del volume di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="f20ab-127">Maximum z-value of the view volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f20ab-128">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f20ab-128">Return value</span></span>

<span data-ttu-id="f20ab-129">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="f20ab-129">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="f20ab-130">Puntatore al [**D3DXMATRIX**](d3d10-d3dxmatrix.md)risultante.</span><span class="sxs-lookup"><span data-stu-id="f20ab-130">Pointer to the resulting [**D3DXMATRIX**](d3d10-d3dxmatrix.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f20ab-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="f20ab-131">Remarks</span></span>

<span data-ttu-id="f20ab-132">[**D3DXMatrixOrthoLH**](d3d10-d3dxmatrixortholh.md) è un caso speciale della funzione D3DXMatrixOrthoOffCenterLH.</span><span class="sxs-lookup"><span data-stu-id="f20ab-132">The [**D3DXMatrixOrthoLH**](d3d10-d3dxmatrixortholh.md) is a special case of the D3DXMatrixOrthoOffCenterLH function.</span></span> <span data-ttu-id="f20ab-133">Per creare la stessa proiezione usando D3DXMatrixOrthoOffCenterLH, usare i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="f20ab-133">To create the same projection using D3DXMatrixOrthoOffCenterLH, use the following values:</span></span>

<span data-ttu-id="f20ab-134">l =-w/2,</span><span class="sxs-lookup"><span data-stu-id="f20ab-134">l = -w/2,</span></span>

<span data-ttu-id="f20ab-135">r = w/2,</span><span class="sxs-lookup"><span data-stu-id="f20ab-135">r = w/2,</span></span>

<span data-ttu-id="f20ab-136">b =-h/2 e</span><span class="sxs-lookup"><span data-stu-id="f20ab-136">b = -h/2, and</span></span>

<span data-ttu-id="f20ab-137">t = h/2.</span><span class="sxs-lookup"><span data-stu-id="f20ab-137">t = h/2.</span></span>

<span data-ttu-id="f20ab-138">Tutti i parametri della funzione D3DXMatrixOrthoOffCenterLH sono distanze nello spazio della fotocamera.</span><span class="sxs-lookup"><span data-stu-id="f20ab-138">All the parameters of the D3DXMatrixOrthoOffCenterLH function are distances in camera space.</span></span> <span data-ttu-id="f20ab-139">I parametri descrivono le dimensioni del volume di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="f20ab-139">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="f20ab-140">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro broncio.</span><span class="sxs-lookup"><span data-stu-id="f20ab-140">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="f20ab-141">In questo modo, la funzione D3DXMatrixOrthoOffCenterLH può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="f20ab-141">In this way, the D3DXMatrixOrthoOffCenterLH function can be used as a parameter for another function.</span></span>

<span data-ttu-id="f20ab-142">Questa funzione usa la formula seguente per calcolare la matrice restituita.</span><span class="sxs-lookup"><span data-stu-id="f20ab-142">This function uses the following formula to compute the returned matrix.</span></span>


```
2/(r-l)      0            0           0
0            2/(t-b)      0           0
0            0            1/(zf-zn)   0
(l+r)/(l-r)  (t+b)/(b-t)  zn/(zn-zf)  1
```



## <a name="requirements"></a><span data-ttu-id="f20ab-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f20ab-143">Requirements</span></span>



| <span data-ttu-id="f20ab-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="f20ab-144">Requirement</span></span> | <span data-ttu-id="f20ab-145">Valore</span><span class="sxs-lookup"><span data-stu-id="f20ab-145">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f20ab-146">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f20ab-146">Header</span></span><br/>  | <dl> <span data-ttu-id="f20ab-147"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="f20ab-147"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="f20ab-148">Libreria</span><span class="sxs-lookup"><span data-stu-id="f20ab-148">Library</span></span><br/> | <dl> <span data-ttu-id="f20ab-149"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f20ab-149"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f20ab-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f20ab-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f20ab-151">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="f20ab-151">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
