---
description: 'Funzione D3DXMatrixOrthoOffCenterLH (D3DX10Math.h): compila una matrice di proiezione ortografica personalizzata mancino.'
ms.assetid: 84175c08-5a0b-4183-afe2-8aecafd73897
title: Funzione D3DXMatrixOrthoOffCenterLH (D3DX10Math.h)
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
ms.openlocfilehash: 2eb10963372519827eb544371ebb0df04df2e178
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109139"
---
# <a name="d3dxmatrixorthooffcenterlh-function-d3dx10mathh"></a><span data-ttu-id="eea4f-103">Funzione D3DXMatrixOrthoOffCenterLH (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="eea4f-103">D3DXMatrixOrthoOffCenterLH function (D3DX10Math.h)</span></span>

<span data-ttu-id="eea4f-104">Compila una matrice di proiezione ortografica personalizzata mancino.</span><span class="sxs-lookup"><span data-stu-id="eea4f-104">Builds a customized, left-handed orthographic projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="eea4f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="eea4f-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="eea4f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="eea4f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eea4f-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="eea4f-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="eea4f-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="eea4f-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="eea4f-109">Puntatore all'oggetto [**D3DXMATRIX risultante.**](d3d10-d3dxmatrix.md)</span><span class="sxs-lookup"><span data-stu-id="eea4f-109">Pointer to the resulting [**D3DXMATRIX**](d3d10-d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="eea4f-110">*l* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="eea4f-110">*l* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eea4f-111">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="eea4f-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="eea4f-112">Valore x minimo del volume di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="eea4f-112">Minimum x-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="eea4f-113">*r* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="eea4f-113">*r* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eea4f-114">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="eea4f-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="eea4f-115">Valore x massimo del volume di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="eea4f-115">Maximum x-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="eea4f-116">*b* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="eea4f-116">*b* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eea4f-117">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="eea4f-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="eea4f-118">Valore y minimo del volume della vista.</span><span class="sxs-lookup"><span data-stu-id="eea4f-118">Minimum y-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="eea4f-119">*t* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="eea4f-119">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eea4f-120">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="eea4f-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="eea4f-121">Valore y massimo del volume della vista.</span><span class="sxs-lookup"><span data-stu-id="eea4f-121">Maximum y-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="eea4f-122">*zn* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="eea4f-122">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eea4f-123">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="eea4f-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="eea4f-124">Valore z minimo del volume di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="eea4f-124">Minimum z-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="eea4f-125">*zf* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="eea4f-125">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eea4f-126">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="eea4f-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="eea4f-127">Valore z massimo del volume di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="eea4f-127">Maximum z-value of the view volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eea4f-128">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="eea4f-128">Return value</span></span>

<span data-ttu-id="eea4f-129">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="eea4f-129">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="eea4f-130">Puntatore all'oggetto [**D3DXMATRIX risultante.**](d3d10-d3dxmatrix.md)</span><span class="sxs-lookup"><span data-stu-id="eea4f-130">Pointer to the resulting [**D3DXMATRIX**](d3d10-d3dxmatrix.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="eea4f-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="eea4f-131">Remarks</span></span>

<span data-ttu-id="eea4f-132">[**D3DXMatrixOrthoLH**](d3d10-d3dxmatrixortholh.md) è un caso speciale della funzione D3DXMatrixOrthoOffCenterLH.</span><span class="sxs-lookup"><span data-stu-id="eea4f-132">The [**D3DXMatrixOrthoLH**](d3d10-d3dxmatrixortholh.md) is a special case of the D3DXMatrixOrthoOffCenterLH function.</span></span> <span data-ttu-id="eea4f-133">Per creare la stessa proiezione usando D3DXMatrixOrthoOffCenterLH, usare i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="eea4f-133">To create the same projection using D3DXMatrixOrthoOffCenterLH, use the following values:</span></span>

<span data-ttu-id="eea4f-134">l = -w/2,</span><span class="sxs-lookup"><span data-stu-id="eea4f-134">l = -w/2,</span></span>

<span data-ttu-id="eea4f-135">r = w/2,</span><span class="sxs-lookup"><span data-stu-id="eea4f-135">r = w/2,</span></span>

<span data-ttu-id="eea4f-136">b = -h/2 e</span><span class="sxs-lookup"><span data-stu-id="eea4f-136">b = -h/2, and</span></span>

<span data-ttu-id="eea4f-137">t = h/2.</span><span class="sxs-lookup"><span data-stu-id="eea4f-137">t = h/2.</span></span>

<span data-ttu-id="eea4f-138">Tutti i parametri della funzione D3DXMatrixOrthoOffCenterLH sono distanze nello spazio della fotocamera.</span><span class="sxs-lookup"><span data-stu-id="eea4f-138">All the parameters of the D3DXMatrixOrthoOffCenterLH function are distances in camera space.</span></span> <span data-ttu-id="eea4f-139">I parametri descrivono le dimensioni del volume della vista.</span><span class="sxs-lookup"><span data-stu-id="eea4f-139">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="eea4f-140">Il valore restituito per questa funzione è lo stesso valore restituito nel parametro pOut.</span><span class="sxs-lookup"><span data-stu-id="eea4f-140">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="eea4f-141">In questo modo, la funzione D3DXMatrixOrthoOffCenterLH può essere usata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="eea4f-141">In this way, the D3DXMatrixOrthoOffCenterLH function can be used as a parameter for another function.</span></span>

<span data-ttu-id="eea4f-142">Questa funzione usa la formula seguente per calcolare la matrice restituita.</span><span class="sxs-lookup"><span data-stu-id="eea4f-142">This function uses the following formula to compute the returned matrix.</span></span>


```
2/(r-l)      0            0           0
0            2/(t-b)      0           0
0            0            1/(zf-zn)   0
(l+r)/(l-r)  (t+b)/(b-t)  zn/(zn-zf)  1
```



## <a name="requirements"></a><span data-ttu-id="eea4f-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="eea4f-143">Requirements</span></span>



| <span data-ttu-id="eea4f-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="eea4f-144">Requirement</span></span> | <span data-ttu-id="eea4f-145">Valore</span><span class="sxs-lookup"><span data-stu-id="eea4f-145">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eea4f-146">Intestazione</span><span class="sxs-lookup"><span data-stu-id="eea4f-146">Header</span></span><br/>  | <dl> <span data-ttu-id="eea4f-147"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="eea4f-147"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="eea4f-148">Libreria</span><span class="sxs-lookup"><span data-stu-id="eea4f-148">Library</span></span><br/> | <dl> <span data-ttu-id="eea4f-149"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="eea4f-149"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="eea4f-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="eea4f-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eea4f-151">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="eea4f-151">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
