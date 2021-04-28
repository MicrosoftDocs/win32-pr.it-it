---
description: 'Funzione D3DXMatrixOrthoOffCenterRH (D3DX10Math.h): crea una matrice di proiezione ortografica personalizzata con la mano destra.'
ms.assetid: 01d4d61e-de7b-4431-a168-68a50b1d6021
title: Funzione D3DXMatrixOrthoOffCenterRH (D3DX10Math.h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 0b41038021cc34cb02961cb9894415995955404c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113079"
---
# <a name="d3dxmatrixorthooffcenterrh-function-d3dx10mathh"></a><span data-ttu-id="91238-103">Funzione D3DXMatrixOrthoOffCenterRH (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="91238-103">D3DXMatrixOrthoOffCenterRH function (D3DX10Math.h)</span></span>

<span data-ttu-id="91238-104">Compila una matrice di proiezione ortogonale personalizzata con la mano destra.</span><span class="sxs-lookup"><span data-stu-id="91238-104">Builds a customized, right-handed orthographic projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="91238-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="91238-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="91238-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="91238-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91238-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="91238-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="91238-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="91238-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="91238-109">Puntatore all'oggetto [**D3DXMATRIX risultante.**](d3d10-d3dxmatrix.md)</span><span class="sxs-lookup"><span data-stu-id="91238-109">Pointer to the resulting [**D3DXMATRIX**](d3d10-d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="91238-110">*l* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="91238-110">*l* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91238-111">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="91238-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="91238-112">Valore x minimo del volume di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="91238-112">Minimum x-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="91238-113">*r* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="91238-113">*r* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91238-114">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="91238-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="91238-115">Valore x massimo del volume di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="91238-115">Maximum x-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="91238-116">*b* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="91238-116">*b* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91238-117">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="91238-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="91238-118">Valore y minimo del volume della vista.</span><span class="sxs-lookup"><span data-stu-id="91238-118">Minimum y-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="91238-119">*t* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="91238-119">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91238-120">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="91238-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="91238-121">Valore y massimo del volume della vista.</span><span class="sxs-lookup"><span data-stu-id="91238-121">Maximum y-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="91238-122">*zn* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="91238-122">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91238-123">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="91238-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="91238-124">Valore z minimo del volume di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="91238-124">Minimum z-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="91238-125">*zf* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="91238-125">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91238-126">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="91238-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="91238-127">Valore z massimo del volume di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="91238-127">Maximum z-value of the view volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91238-128">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="91238-128">Return value</span></span>

<span data-ttu-id="91238-129">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="91238-129">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="91238-130">Puntatore all'oggetto [**D3DXMATRIX risultante.**](d3d10-d3dxmatrix.md)</span><span class="sxs-lookup"><span data-stu-id="91238-130">Pointer to the resulting [**D3DXMATRIX**](d3d10-d3dxmatrix.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="91238-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="91238-131">Remarks</span></span>

<span data-ttu-id="91238-132">La [**funzione D3DXMatrixOrthoRH**](d3d10-d3dxmatrixorthorh.md) è un caso speciale della funzione D3DXMatrixOrthoOffCenterRH.</span><span class="sxs-lookup"><span data-stu-id="91238-132">The [**D3DXMatrixOrthoRH**](d3d10-d3dxmatrixorthorh.md) function is a special case of the D3DXMatrixOrthoOffCenterRH function.</span></span> <span data-ttu-id="91238-133">Per creare la stessa proiezione usando D3DXMatrixOrthoOffCenterRH, usare i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="91238-133">To create the same projection using D3DXMatrixOrthoOffCenterRH, use the following values:</span></span>

<span data-ttu-id="91238-134">l = -w/2,</span><span class="sxs-lookup"><span data-stu-id="91238-134">l = -w/2,</span></span>

<span data-ttu-id="91238-135">r = w/2,</span><span class="sxs-lookup"><span data-stu-id="91238-135">r = w/2,</span></span>

<span data-ttu-id="91238-136">b = -h/2 e</span><span class="sxs-lookup"><span data-stu-id="91238-136">b = -h/2, and</span></span>

<span data-ttu-id="91238-137">t = h/2.</span><span class="sxs-lookup"><span data-stu-id="91238-137">t = h/2.</span></span>

<span data-ttu-id="91238-138">Tutti i parametri della funzione D3DXMatrixOrthoOffCenterRH sono distanze nello spazio della fotocamera.</span><span class="sxs-lookup"><span data-stu-id="91238-138">All the parameters of the D3DXMatrixOrthoOffCenterRH function are distances in camera space.</span></span> <span data-ttu-id="91238-139">I parametri descrivono le dimensioni del volume di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="91238-139">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="91238-140">Il valore restituito per questa funzione è lo stesso valore restituito nel parametro pOut.</span><span class="sxs-lookup"><span data-stu-id="91238-140">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="91238-141">In questo modo, la funzione D3DXMatrixOrthoOffCenterRH può essere usata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="91238-141">In this way, the D3DXMatrixOrthoOffCenterRH function can be used as a parameter for another function.</span></span>

<span data-ttu-id="91238-142">Questa funzione usa la formula seguente per calcolare la matrice restituita.</span><span class="sxs-lookup"><span data-stu-id="91238-142">This function uses the following formula to compute the returned matrix.</span></span>


```
2/(r-l)      0            0           0
0            2/(t-b)      0           0
0            0            1/(zn-zf)   0
(l+r)/(l-r)  (t+b)/(b-t)  zn/(zn-zf)  1
```



## <a name="requirements"></a><span data-ttu-id="91238-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="91238-143">Requirements</span></span>



| <span data-ttu-id="91238-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="91238-144">Requirement</span></span> | <span data-ttu-id="91238-145">Valore</span><span class="sxs-lookup"><span data-stu-id="91238-145">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="91238-146">Intestazione</span><span class="sxs-lookup"><span data-stu-id="91238-146">Header</span></span><br/>  | <dl> <span data-ttu-id="91238-147"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="91238-147"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="91238-148">Libreria</span><span class="sxs-lookup"><span data-stu-id="91238-148">Library</span></span><br/> | <dl> <span data-ttu-id="91238-149"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="91238-149"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="91238-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="91238-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91238-151">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="91238-151">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
