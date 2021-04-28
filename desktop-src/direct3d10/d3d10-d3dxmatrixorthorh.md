---
description: 'Funzione D3DXMatrixOrthoRH (D3DX10Math.h): compila una matrice di proiezione ortografica con la mano destra.'
ms.assetid: e6673ff4-06a2-4a16-b72e-5ca69ddf2438
title: Funzione D3DXMatrixOrthoRH (D3DX10Math.h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: f1ab6069890bdffdedbd3e36caed1a93984fc2c2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109149"
---
# <a name="d3dxmatrixorthorh-function-d3dx10mathh"></a><span data-ttu-id="b5743-103">Funzione D3DXMatrixOrthoRH (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="b5743-103">D3DXMatrixOrthoRH function (D3DX10Math.h)</span></span>

<span data-ttu-id="b5743-104">Compila una matrice di proiezione ortografica con la mano destra.</span><span class="sxs-lookup"><span data-stu-id="b5743-104">Builds a right-handed orthographic projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5743-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b5743-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixOrthoRH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      w,
  _In_    FLOAT      h,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="b5743-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b5743-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5743-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="b5743-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b5743-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="b5743-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="b5743-109">Puntatore all'oggetto [**D3DXMATRIX risultante.**](d3d10-d3dxmatrix.md)</span><span class="sxs-lookup"><span data-stu-id="b5743-109">Pointer to the resulting [**D3DXMATRIX**](d3d10-d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="b5743-110">*w* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b5743-110">*w* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5743-111">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b5743-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b5743-112">Larghezza del volume della vista.</span><span class="sxs-lookup"><span data-stu-id="b5743-112">Width of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="b5743-113">*h* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b5743-113">*h* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5743-114">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b5743-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b5743-115">Altezza del volume della vista.</span><span class="sxs-lookup"><span data-stu-id="b5743-115">Height of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="b5743-116">*zn* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="b5743-116">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5743-117">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b5743-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b5743-118">Valore z minimo del volume di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="b5743-118">Minimum z-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="b5743-119">*zf* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="b5743-119">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5743-120">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b5743-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b5743-121">Valore z massimo del volume di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="b5743-121">Maximum z-value of the view volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5743-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b5743-122">Return value</span></span>

<span data-ttu-id="b5743-123">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="b5743-123">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="b5743-124">Puntatore all'oggetto [**D3DXMATRIX risultante.**](d3d10-d3dxmatrix.md)</span><span class="sxs-lookup"><span data-stu-id="b5743-124">Pointer to the resulting [**D3DXMATRIX**](d3d10-d3dxmatrix.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b5743-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="b5743-125">Remarks</span></span>

<span data-ttu-id="b5743-126">Tutti i parametri della funzione D3DXMatrixOrthoRH sono distanze nello spazio della fotocamera.</span><span class="sxs-lookup"><span data-stu-id="b5743-126">All the parameters of the D3DXMatrixOrthoRH function are distances in camera space.</span></span> <span data-ttu-id="b5743-127">I parametri descrivono le dimensioni del volume di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="b5743-127">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="b5743-128">Il valore restituito per questa funzione è lo stesso valore restituito nel parametro pOut.</span><span class="sxs-lookup"><span data-stu-id="b5743-128">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="b5743-129">In questo modo, la funzione D3DXMatrixOrthoRH può essere usata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="b5743-129">In this way, the D3DXMatrixOrthoRH function can be used as a parameter for another function.</span></span>

<span data-ttu-id="b5743-130">Questa funzione usa la formula seguente per calcolare la matrice restituita.</span><span class="sxs-lookup"><span data-stu-id="b5743-130">This function uses the following formula to compute the returned matrix.</span></span>


```
2/w  0    0           0
0    2/h  0           0
0    0    1/(zn-zf)   0
0    0    zn/(zn-zf)  1
```



## <a name="requirements"></a><span data-ttu-id="b5743-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b5743-131">Requirements</span></span>



| <span data-ttu-id="b5743-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5743-132">Requirement</span></span> | <span data-ttu-id="b5743-133">Valore</span><span class="sxs-lookup"><span data-stu-id="b5743-133">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b5743-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b5743-134">Header</span></span><br/>  | <dl> <span data-ttu-id="b5743-135"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="b5743-135"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="b5743-136">Libreria</span><span class="sxs-lookup"><span data-stu-id="b5743-136">Library</span></span><br/> | <dl> <span data-ttu-id="b5743-137"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="b5743-137"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b5743-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b5743-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5743-139">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="b5743-139">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
