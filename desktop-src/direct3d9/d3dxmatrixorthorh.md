---
description: 'Funzione D3DXMatrixOrthoRH (D3dx9math.h): crea una matrice di proiezione ortografica con la mano destra.'
ms.assetid: 6b9b50d5-0307-4fc7-a28d-8f42d2a21bf0
title: Funzione D3DXMatrixOrthoRH (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixOrthoRH
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d34a8379851d80ae8734c7f32cc0dc5977af2088
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107439"
---
# <a name="d3dxmatrixorthorh-function-d3dx9mathh"></a><span data-ttu-id="708f5-103">Funzione D3DXMatrixOrthoRH (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="708f5-103">D3DXMatrixOrthoRH function (D3dx9math.h)</span></span>

<span data-ttu-id="708f5-104">Compila una matrice di proiezione ortogonale con la mano destra.</span><span class="sxs-lookup"><span data-stu-id="708f5-104">Builds a right-handed orthographic projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="708f5-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="708f5-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixOrthoRH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      w,
  _In_    FLOAT      h,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="708f5-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="708f5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="708f5-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="708f5-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="708f5-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="708f5-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="708f5-109">Puntatore all'oggetto [**D3DXMATRIX risultante.**](../direct3d10/d3d10-d3dxmatrix.md)</span><span class="sxs-lookup"><span data-stu-id="708f5-109">Pointer to the resulting [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="708f5-110">*w* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="708f5-110">*w* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="708f5-111">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="708f5-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="708f5-112">Larghezza del volume di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="708f5-112">Width of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="708f5-113">*h* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="708f5-113">*h* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="708f5-114">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="708f5-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="708f5-115">Altezza del volume di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="708f5-115">Height of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="708f5-116">*zn* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="708f5-116">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="708f5-117">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="708f5-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="708f5-118">Valore z minimo del volume di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="708f5-118">Minimum z-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="708f5-119">*zf* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="708f5-119">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="708f5-120">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="708f5-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="708f5-121">Valore z massimo del volume di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="708f5-121">Maximum z-value of the view volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="708f5-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="708f5-122">Return value</span></span>

<span data-ttu-id="708f5-123">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="708f5-123">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="708f5-124">Puntatore all'oggetto [**D3DXMATRIX risultante.**](../direct3d10/d3d10-d3dxmatrix.md)</span><span class="sxs-lookup"><span data-stu-id="708f5-124">Pointer to the resulting [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="708f5-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="708f5-125">Remarks</span></span>

<span data-ttu-id="708f5-126">Tutti i parametri della **funzione D3DXMatrixOrthoRH** sono distanze nello spazio della fotocamera.</span><span class="sxs-lookup"><span data-stu-id="708f5-126">All the parameters of the **D3DXMatrixOrthoRH** function are distances in camera space.</span></span> <span data-ttu-id="708f5-127">I parametri descrivono le dimensioni del volume della vista.</span><span class="sxs-lookup"><span data-stu-id="708f5-127">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="708f5-128">Il valore restituito per questa funzione è lo stesso valore restituito nel *parametro pOut.*</span><span class="sxs-lookup"><span data-stu-id="708f5-128">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="708f5-129">In questo modo, la **funzione D3DXMatrixOrthoRH** può essere usata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="708f5-129">In this way, the **D3DXMatrixOrthoRH** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="708f5-130">Questa funzione usa la formula seguente per calcolare la matrice restituita.</span><span class="sxs-lookup"><span data-stu-id="708f5-130">This function uses the following formula to compute the returned matrix.</span></span>


```
2/w  0    0           0
0    2/h  0           0
0    0    1/(zn-zf)   0
0    0    zn/(zn-zf)  1
```



## <a name="requirements"></a><span data-ttu-id="708f5-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="708f5-131">Requirements</span></span>



| <span data-ttu-id="708f5-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="708f5-132">Requirement</span></span> | <span data-ttu-id="708f5-133">Valore</span><span class="sxs-lookup"><span data-stu-id="708f5-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="708f5-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="708f5-134">Header</span></span><br/>  | <dl> <span data-ttu-id="708f5-135"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="708f5-135"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="708f5-136">Libreria</span><span class="sxs-lookup"><span data-stu-id="708f5-136">Library</span></span><br/> | <dl> <span data-ttu-id="708f5-137"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="708f5-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="708f5-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="708f5-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="708f5-139">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="708f5-139">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="708f5-140">**D3DXMatrixOrthoLH**</span><span class="sxs-lookup"><span data-stu-id="708f5-140">**D3DXMatrixOrthoLH**</span></span>](d3dxmatrixortholh.md)
</dt> <dt>

[<span data-ttu-id="708f5-141">**D3DXMatrixOrthoOffCenterRH**</span><span class="sxs-lookup"><span data-stu-id="708f5-141">**D3DXMatrixOrthoOffCenterRH**</span></span>](d3dxmatrixorthooffcenterrh.md)
</dt> <dt>

[<span data-ttu-id="708f5-142">**D3DXMatrixOrthoOffCenterLH**</span><span class="sxs-lookup"><span data-stu-id="708f5-142">**D3DXMatrixOrthoOffCenterLH**</span></span>](d3dxmatrixorthooffcenterlh.md)
</dt> </dl>

 

 
