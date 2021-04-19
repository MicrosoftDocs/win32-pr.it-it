---
description: Compila una matrice di proiezione ortogonale personalizzata, a destra.
ms.assetid: d6171e28-b138-4ccf-9f12-fb977a30aca1
title: Funzione D3DXMatrixOrthoOffCenterRH (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixOrthoOffCenterRH
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7de5e4b3a872ea7466840e511fc0a57448861b55
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323241"
---
# <a name="d3dxmatrixorthooffcenterrh-function-d3dx9mathh"></a><span data-ttu-id="d0170-103">Funzione D3DXMatrixOrthoOffCenterRH (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="d0170-103">D3DXMatrixOrthoOffCenterRH function (D3dx9math.h)</span></span>

<span data-ttu-id="d0170-104">Compila una matrice di proiezione ortogonale personalizzata, a destra.</span><span class="sxs-lookup"><span data-stu-id="d0170-104">Builds a customized, right-handed orthographic projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0170-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d0170-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixOrthoOffCenterRH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      l,
  _In_    FLOAT      r,
  _In_    FLOAT      b,
  _In_    FLOAT      t,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="d0170-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d0170-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0170-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="d0170-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d0170-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="d0170-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="d0170-109">Puntatore al [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md)risultante.</span><span class="sxs-lookup"><span data-stu-id="d0170-109">Pointer to the resulting [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="d0170-110">*l* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d0170-110">*l* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0170-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d0170-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d0170-112">Valore x minimo del volume di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="d0170-112">Minimum x-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="d0170-113">*r* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d0170-113">*r* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0170-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d0170-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d0170-115">Valore x massimo del volume di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="d0170-115">Maximum x-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="d0170-116">*b* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d0170-116">*b* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0170-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d0170-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d0170-118">Valore y minimo del volume di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="d0170-118">Minimum y-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="d0170-119">*t* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d0170-119">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0170-120">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d0170-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d0170-121">Valore y massimo del volume di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="d0170-121">Maximum y-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="d0170-122">*Zn* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d0170-122">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0170-123">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d0170-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d0170-124">Valore z minimo del volume di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="d0170-124">Minimum z-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="d0170-125">*ZF* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d0170-125">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0170-126">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d0170-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d0170-127">Valore z massimo del volume di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="d0170-127">Maximum z-value of the view volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0170-128">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d0170-128">Return value</span></span>

<span data-ttu-id="d0170-129">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="d0170-129">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="d0170-130">Puntatore al [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md)risultante.</span><span class="sxs-lookup"><span data-stu-id="d0170-130">Pointer to the resulting [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d0170-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="d0170-131">Remarks</span></span>

<span data-ttu-id="d0170-132">La funzione [**D3DXMatrixOrthoRH**](d3dxmatrixorthorh.md) è un caso speciale della funzione **D3DXMatrixOrthoOffCenterRH** .</span><span class="sxs-lookup"><span data-stu-id="d0170-132">The [**D3DXMatrixOrthoRH**](d3dxmatrixorthorh.md) function is a special case of the **D3DXMatrixOrthoOffCenterRH** function.</span></span> <span data-ttu-id="d0170-133">Per creare la stessa proiezione usando **D3DXMatrixOrthoOffCenterRH**, usare i valori seguenti: l =-w/2, r = w/2, b =-h/2 e t = h/2.</span><span class="sxs-lookup"><span data-stu-id="d0170-133">To create the same projection using **D3DXMatrixOrthoOffCenterRH**, use the following values: l = -w/2, r = w/2, b = -h/2, and t = h/2.</span></span>

<span data-ttu-id="d0170-134">Tutti i parametri della funzione **D3DXMatrixOrthoOffCenterRH** sono distanze nello spazio della fotocamera.</span><span class="sxs-lookup"><span data-stu-id="d0170-134">All the parameters of the **D3DXMatrixOrthoOffCenterRH** function are distances in camera space.</span></span> <span data-ttu-id="d0170-135">I parametri descrivono le dimensioni del volume di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="d0170-135">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="d0170-136">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro *broncio* .</span><span class="sxs-lookup"><span data-stu-id="d0170-136">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="d0170-137">In questo modo, la funzione **D3DXMatrixOrthoOffCenterRH** può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="d0170-137">In this way, the **D3DXMatrixOrthoOffCenterRH** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="d0170-138">Questa funzione usa la formula seguente per calcolare la matrice restituita.</span><span class="sxs-lookup"><span data-stu-id="d0170-138">This function uses the following formula to compute the returned matrix.</span></span>


```
2/(r-l)      0            0           0
0            2/(t-b)      0           0
0            0            1/(zn-zf)   0
(l+r)/(l-r)  (t+b)/(b-t)  zn/(zn-zf)  1
```



## <a name="requirements"></a><span data-ttu-id="d0170-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d0170-139">Requirements</span></span>



| <span data-ttu-id="d0170-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0170-140">Requirement</span></span> | <span data-ttu-id="d0170-141">Valore</span><span class="sxs-lookup"><span data-stu-id="d0170-141">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d0170-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d0170-142">Header</span></span><br/>  | <dl> <span data-ttu-id="d0170-143"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="d0170-143"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="d0170-144">Libreria</span><span class="sxs-lookup"><span data-stu-id="d0170-144">Library</span></span><br/> | <dl> <span data-ttu-id="d0170-145"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d0170-145"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d0170-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d0170-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0170-147">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="d0170-147">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="d0170-148">**D3DXMatrixOrthoRH**</span><span class="sxs-lookup"><span data-stu-id="d0170-148">**D3DXMatrixOrthoRH**</span></span>](d3dxmatrixorthorh.md)
</dt> <dt>

[<span data-ttu-id="d0170-149">**D3DXMatrixOrthoLH**</span><span class="sxs-lookup"><span data-stu-id="d0170-149">**D3DXMatrixOrthoLH**</span></span>](d3dxmatrixortholh.md)
</dt> <dt>

[<span data-ttu-id="d0170-150">**D3DXMatrixOrthoOffCenterLH**</span><span class="sxs-lookup"><span data-stu-id="d0170-150">**D3DXMatrixOrthoOffCenterLH**</span></span>](d3dxmatrixorthooffcenterlh.md)
</dt> </dl>

 

 
