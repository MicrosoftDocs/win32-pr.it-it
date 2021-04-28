---
description: 'Funzione D3DXMatrixOrthoLH (D3dx9math.h): crea una matrice di proiezione ortografica mancino.'
ms.assetid: e42151bd-2302-491b-a211-7d5a4b8e437f
title: Funzione D3DXMatrixOrthoLH (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixOrthoLH
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5492a6caba87025d83562c0327ac0e1f5a76f269
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107499"
---
# <a name="d3dxmatrixortholh-function-d3dx9mathh"></a><span data-ttu-id="e40e2-103">Funzione D3DXMatrixOrthoLH (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="e40e2-103">D3DXMatrixOrthoLH function (D3dx9math.h)</span></span>

<span data-ttu-id="e40e2-104">Compila una matrice di proiezione ortografica mancino.</span><span class="sxs-lookup"><span data-stu-id="e40e2-104">Builds a left-handed orthographic projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="e40e2-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e40e2-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixOrthoLH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      w,
  _In_    FLOAT      h,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="e40e2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e40e2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e40e2-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="e40e2-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e40e2-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="e40e2-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="e40e2-109">Puntatore all'oggetto [**D3DXMATRIX risultante.**](../direct3d10/d3d10-d3dxmatrix.md)</span><span class="sxs-lookup"><span data-stu-id="e40e2-109">Pointer to the resulting [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="e40e2-110">*w* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e40e2-110">*w* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e40e2-111">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e40e2-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e40e2-112">Larghezza del volume di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="e40e2-112">Width of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="e40e2-113">*h* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e40e2-113">*h* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e40e2-114">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e40e2-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e40e2-115">Altezza del volume di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="e40e2-115">Height of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="e40e2-116">*zn* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="e40e2-116">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e40e2-117">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e40e2-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e40e2-118">Valore z minimo del volume di visualizzazione, definito z-near.</span><span class="sxs-lookup"><span data-stu-id="e40e2-118">Minimum z-value of the view volume which is referred to as z-near.</span></span>

</dd> <dt>

<span data-ttu-id="e40e2-119">*zf* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="e40e2-119">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e40e2-120">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e40e2-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e40e2-121">Valore z massimo del volume di visualizzazione, definito z-far.</span><span class="sxs-lookup"><span data-stu-id="e40e2-121">Maximum z-value of the view volume which is referred to as z-far.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e40e2-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e40e2-122">Return value</span></span>

<span data-ttu-id="e40e2-123">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="e40e2-123">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="e40e2-124">Puntatore all'oggetto [**D3DXMATRIX risultante.**](../direct3d10/d3d10-d3dxmatrix.md)</span><span class="sxs-lookup"><span data-stu-id="e40e2-124">Pointer to the resulting [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e40e2-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="e40e2-125">Remarks</span></span>

<span data-ttu-id="e40e2-126">Tutti i parametri della **funzione D3DXMatrixOrthoLH** sono distanze nello spazio della fotocamera.</span><span class="sxs-lookup"><span data-stu-id="e40e2-126">All the parameters of the **D3DXMatrixOrthoLH** function are distances in camera space.</span></span> <span data-ttu-id="e40e2-127">I parametri descrivono le dimensioni del volume della vista.</span><span class="sxs-lookup"><span data-stu-id="e40e2-127">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="e40e2-128">Il valore restituito per questa funzione è lo stesso valore restituito nel *parametro pOut.*</span><span class="sxs-lookup"><span data-stu-id="e40e2-128">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="e40e2-129">In questo modo, la **funzione D3DXMatrixOrthoLH** può essere usata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="e40e2-129">In this way, the **D3DXMatrixOrthoLH** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="e40e2-130">Questa funzione usa la formula seguente per calcolare la matrice restituita.</span><span class="sxs-lookup"><span data-stu-id="e40e2-130">This function uses the following formula to compute the returned matrix.</span></span>


```
2/w  0    0           0
0    2/h  0           0
0    0    1/(zf-zn)   0
0    0   -zn/(zf-zn)  1
```



## <a name="requirements"></a><span data-ttu-id="e40e2-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e40e2-131">Requirements</span></span>



| <span data-ttu-id="e40e2-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="e40e2-132">Requirement</span></span> | <span data-ttu-id="e40e2-133">Valore</span><span class="sxs-lookup"><span data-stu-id="e40e2-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e40e2-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e40e2-134">Header</span></span><br/>  | <dl> <span data-ttu-id="e40e2-135"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="e40e2-135"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="e40e2-136">Libreria</span><span class="sxs-lookup"><span data-stu-id="e40e2-136">Library</span></span><br/> | <dl> <span data-ttu-id="e40e2-137"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="e40e2-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e40e2-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e40e2-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e40e2-139">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="e40e2-139">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="e40e2-140">**D3DXMatrixOrthoRH**</span><span class="sxs-lookup"><span data-stu-id="e40e2-140">**D3DXMatrixOrthoRH**</span></span>](d3dxmatrixorthorh.md)
</dt> <dt>

[<span data-ttu-id="e40e2-141">**D3DXMatrixOrthoOffCenterRH**</span><span class="sxs-lookup"><span data-stu-id="e40e2-141">**D3DXMatrixOrthoOffCenterRH**</span></span>](d3dxmatrixorthooffcenterrh.md)
</dt> <dt>

[<span data-ttu-id="e40e2-142">**D3DXMatrixOrthoOffCenterLH**</span><span class="sxs-lookup"><span data-stu-id="e40e2-142">**D3DXMatrixOrthoOffCenterLH**</span></span>](d3dxmatrixorthooffcenterlh.md)
</dt> </dl>

 

 
