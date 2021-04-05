---
description: Compila una matrice di proiezione ortogonale personalizzata, a sinistra.
ms.assetid: e4f087e5-63d9-49ca-9d8e-3a25070e1a51
title: Funzione D3DXMatrixOrthoOffCenterLH (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1e286197233b2abb2b19138b8fc9d154df355a6a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969446"
---
# <a name="d3dxmatrixorthooffcenterlh-function-d3dx9mathh"></a><span data-ttu-id="8c825-103">Funzione D3DXMatrixOrthoOffCenterLH (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="8c825-103">D3DXMatrixOrthoOffCenterLH function (D3dx9math.h)</span></span>

<span data-ttu-id="8c825-104">Compila una matrice di proiezione ortogonale personalizzata, a sinistra.</span><span class="sxs-lookup"><span data-stu-id="8c825-104">Builds a customized, left-handed orthographic projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c825-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8c825-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="8c825-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8c825-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c825-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="8c825-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8c825-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="8c825-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="8c825-109">Puntatore al [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md)risultante.</span><span class="sxs-lookup"><span data-stu-id="8c825-109">Pointer to the resulting [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="8c825-110">*l* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8c825-110">*l* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c825-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8c825-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8c825-112">Valore x minimo del volume di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="8c825-112">Minimum x-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="8c825-113">*r* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8c825-113">*r* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c825-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8c825-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8c825-115">Valore x massimo del volume di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="8c825-115">Maximum x-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="8c825-116">*b* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8c825-116">*b* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c825-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8c825-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8c825-118">Valore y minimo del volume di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="8c825-118">Minimum y-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="8c825-119">*t* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8c825-119">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c825-120">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8c825-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8c825-121">Valore y massimo del volume di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="8c825-121">Maximum y-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="8c825-122">*Zn* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8c825-122">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c825-123">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8c825-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8c825-124">Valore z minimo del volume di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="8c825-124">Minimum z-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="8c825-125">*ZF* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8c825-125">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c825-126">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8c825-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8c825-127">Valore z massimo del volume di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="8c825-127">Maximum z-value of the view volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c825-128">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8c825-128">Return value</span></span>

<span data-ttu-id="8c825-129">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="8c825-129">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="8c825-130">Puntatore al [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md)risultante.</span><span class="sxs-lookup"><span data-stu-id="8c825-130">Pointer to the resulting [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="8c825-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="8c825-131">Remarks</span></span>

<span data-ttu-id="8c825-132">La funzione [**D3DXMatrixOrthoLH**](d3dxmatrixortholh.md) è un caso speciale della funzione **D3DXMatrixOrthoOffCenterLH** .</span><span class="sxs-lookup"><span data-stu-id="8c825-132">The [**D3DXMatrixOrthoLH**](d3dxmatrixortholh.md) function is a special case of the **D3DXMatrixOrthoOffCenterLH** function.</span></span> <span data-ttu-id="8c825-133">Per creare la stessa proiezione usando **D3DXMatrixOrthoOffCenterLH**, usare i valori seguenti: l =-w/2, r = w/2, b =-h/2 e t = h/2.</span><span class="sxs-lookup"><span data-stu-id="8c825-133">To create the same projection using **D3DXMatrixOrthoOffCenterLH**, use the following values: l = -w/2, r = w/2, b = -h/2, and t = h/2.</span></span>

<span data-ttu-id="8c825-134">Tutti i parametri della funzione **D3DXMatrixOrthoOffCenterLH** sono distanze nello spazio della fotocamera.</span><span class="sxs-lookup"><span data-stu-id="8c825-134">All the parameters of the **D3DXMatrixOrthoOffCenterLH** function are distances in camera space.</span></span> <span data-ttu-id="8c825-135">I parametri descrivono le dimensioni del volume di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="8c825-135">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="8c825-136">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro *broncio* .</span><span class="sxs-lookup"><span data-stu-id="8c825-136">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="8c825-137">In questo modo, la funzione **D3DXMatrixOrthoOffCenterLH** può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="8c825-137">In this way, the **D3DXMatrixOrthoOffCenterLH** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="8c825-138">Questa funzione usa la formula seguente per calcolare la matrice restituita.</span><span class="sxs-lookup"><span data-stu-id="8c825-138">This function uses the following formula to compute the returned matrix.</span></span>


```
2/(r-l)      0            0           0
0            2/(t-b)      0           0
0            0            1/(zf-zn)   0
(l+r)/(l-r)  (t+b)/(b-t)  zn/(zn-zf)  1
```



## <a name="requirements"></a><span data-ttu-id="8c825-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8c825-139">Requirements</span></span>



| <span data-ttu-id="8c825-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c825-140">Requirement</span></span> | <span data-ttu-id="8c825-141">Valore</span><span class="sxs-lookup"><span data-stu-id="8c825-141">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8c825-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8c825-142">Header</span></span><br/>  | <dl> <span data-ttu-id="8c825-143"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c825-143"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="8c825-144">Libreria</span><span class="sxs-lookup"><span data-stu-id="8c825-144">Library</span></span><br/> | <dl> <span data-ttu-id="8c825-145"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8c825-145"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8c825-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8c825-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c825-147">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="8c825-147">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="8c825-148">**D3DXMatrixOrthoRH**</span><span class="sxs-lookup"><span data-stu-id="8c825-148">**D3DXMatrixOrthoRH**</span></span>](d3dxmatrixorthorh.md)
</dt> <dt>

[<span data-ttu-id="8c825-149">**D3DXMatrixOrthoLH**</span><span class="sxs-lookup"><span data-stu-id="8c825-149">**D3DXMatrixOrthoLH**</span></span>](d3dxmatrixortholh.md)
</dt> <dt>

[<span data-ttu-id="8c825-150">**D3DXMatrixOrthoOffCenterRH**</span><span class="sxs-lookup"><span data-stu-id="8c825-150">**D3DXMatrixOrthoOffCenterRH**</span></span>](d3dxmatrixorthooffcenterrh.md)
</dt> </dl>

 

 
