---
description: 'Funzione D3DXMatrixOrthoOffCenterRH (D3dx9math.h): crea una matrice di proiezione ortografica personalizzata e con la mano destra.'
ms.assetid: d6171e28-b138-4ccf-9f12-fb977a30aca1
title: Funzione D3DXMatrixOrthoOffCenterRH (D3dx9math.h)
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
ms.openlocfilehash: 8519dca07a4475ff043491802ae173ecc61c0bd3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107459"
---
# <a name="d3dxmatrixorthooffcenterrh-function-d3dx9mathh"></a><span data-ttu-id="d8be6-103">Funzione D3DXMatrixOrthoOffCenterRH (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="d8be6-103">D3DXMatrixOrthoOffCenterRH function (D3dx9math.h)</span></span>

<span data-ttu-id="d8be6-104">Compila una matrice di proiezione ortogonale personalizzata con la mano destra.</span><span class="sxs-lookup"><span data-stu-id="d8be6-104">Builds a customized, right-handed orthographic projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8be6-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d8be6-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="d8be6-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d8be6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8be6-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="d8be6-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d8be6-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="d8be6-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="d8be6-109">Puntatore all'oggetto [**D3DXMATRIX risultante.**](../direct3d10/d3d10-d3dxmatrix.md)</span><span class="sxs-lookup"><span data-stu-id="d8be6-109">Pointer to the resulting [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="d8be6-110">*l* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d8be6-110">*l* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8be6-111">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d8be6-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d8be6-112">Valore x minimo del volume di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="d8be6-112">Minimum x-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="d8be6-113">*r* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d8be6-113">*r* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8be6-114">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d8be6-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d8be6-115">Valore x massimo del volume di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="d8be6-115">Maximum x-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="d8be6-116">*b* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d8be6-116">*b* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8be6-117">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d8be6-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d8be6-118">Valore y minimo del volume di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="d8be6-118">Minimum y-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="d8be6-119">*t* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d8be6-119">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8be6-120">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d8be6-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d8be6-121">Valore y massimo del volume di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="d8be6-121">Maximum y-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="d8be6-122">*zn* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="d8be6-122">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8be6-123">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d8be6-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d8be6-124">Valore z minimo del volume di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="d8be6-124">Minimum z-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="d8be6-125">*zf* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="d8be6-125">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8be6-126">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d8be6-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d8be6-127">Valore z massimo del volume di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="d8be6-127">Maximum z-value of the view volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8be6-128">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d8be6-128">Return value</span></span>

<span data-ttu-id="d8be6-129">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="d8be6-129">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="d8be6-130">Puntatore all'oggetto [**D3DXMATRIX risultante.**](../direct3d10/d3d10-d3dxmatrix.md)</span><span class="sxs-lookup"><span data-stu-id="d8be6-130">Pointer to the resulting [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d8be6-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="d8be6-131">Remarks</span></span>

<span data-ttu-id="d8be6-132">La [**funzione D3DXMatrixOrthoRH**](d3dxmatrixorthorh.md) è un caso speciale della **funzione D3DXMatrixOrthoOffCenterRH.**</span><span class="sxs-lookup"><span data-stu-id="d8be6-132">The [**D3DXMatrixOrthoRH**](d3dxmatrixorthorh.md) function is a special case of the **D3DXMatrixOrthoOffCenterRH** function.</span></span> <span data-ttu-id="d8be6-133">Per creare la stessa proiezione **usando D3DXMatrixOrthoOffCenterRH,** usare i valori seguenti: l = -w/2, r = w/2, b = -h/2 e t = h/2.</span><span class="sxs-lookup"><span data-stu-id="d8be6-133">To create the same projection using **D3DXMatrixOrthoOffCenterRH**, use the following values: l = -w/2, r = w/2, b = -h/2, and t = h/2.</span></span>

<span data-ttu-id="d8be6-134">Tutti i parametri della **funzione D3DXMatrixOrthoOffCenterRH** sono distanze nello spazio della fotocamera.</span><span class="sxs-lookup"><span data-stu-id="d8be6-134">All the parameters of the **D3DXMatrixOrthoOffCenterRH** function are distances in camera space.</span></span> <span data-ttu-id="d8be6-135">I parametri descrivono le dimensioni del volume della vista.</span><span class="sxs-lookup"><span data-stu-id="d8be6-135">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="d8be6-136">Il valore restituito per questa funzione è lo stesso valore restituito nel *parametro pOut.*</span><span class="sxs-lookup"><span data-stu-id="d8be6-136">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="d8be6-137">In questo modo, la **funzione D3DXMatrixOrthoOffCenterRH** può essere usata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="d8be6-137">In this way, the **D3DXMatrixOrthoOffCenterRH** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="d8be6-138">Questa funzione usa la formula seguente per calcolare la matrice restituita.</span><span class="sxs-lookup"><span data-stu-id="d8be6-138">This function uses the following formula to compute the returned matrix.</span></span>


```
2/(r-l)      0            0           0
0            2/(t-b)      0           0
0            0            1/(zn-zf)   0
(l+r)/(l-r)  (t+b)/(b-t)  zn/(zn-zf)  1
```



## <a name="requirements"></a><span data-ttu-id="d8be6-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d8be6-139">Requirements</span></span>



| <span data-ttu-id="d8be6-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8be6-140">Requirement</span></span> | <span data-ttu-id="d8be6-141">Valore</span><span class="sxs-lookup"><span data-stu-id="d8be6-141">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d8be6-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d8be6-142">Header</span></span><br/>  | <dl> <span data-ttu-id="d8be6-143"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="d8be6-143"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="d8be6-144">Libreria</span><span class="sxs-lookup"><span data-stu-id="d8be6-144">Library</span></span><br/> | <dl> <span data-ttu-id="d8be6-145"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="d8be6-145"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d8be6-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d8be6-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8be6-147">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="d8be6-147">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="d8be6-148">**D3DXMatrixOrthoRH**</span><span class="sxs-lookup"><span data-stu-id="d8be6-148">**D3DXMatrixOrthoRH**</span></span>](d3dxmatrixorthorh.md)
</dt> <dt>

[<span data-ttu-id="d8be6-149">**D3DXMatrixOrthoLH**</span><span class="sxs-lookup"><span data-stu-id="d8be6-149">**D3DXMatrixOrthoLH**</span></span>](d3dxmatrixortholh.md)
</dt> <dt>

[<span data-ttu-id="d8be6-150">**D3DXMatrixOrthoOffCenterLH**</span><span class="sxs-lookup"><span data-stu-id="d8be6-150">**D3DXMatrixOrthoOffCenterLH**</span></span>](d3dxmatrixorthooffcenterlh.md)
</dt> </dl>

 

 
