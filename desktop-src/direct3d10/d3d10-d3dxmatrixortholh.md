---
description: 'Funzione D3DXMatrixOrthoLH (D3DX10Math.h): compila una matrice di proiezione ortografica mancino.'
ms.assetid: 67bec4a3-2126-4f5a-9301-97faa6dc6e84
title: Funzione D3DXMatrixOrthoLH (D3DX10Math.h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 73cd5d9b809a0eb442db57e91c3788d2548a8c33
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113099"
---
# <a name="d3dxmatrixortholh-function-d3dx10mathh"></a><span data-ttu-id="270ea-103">Funzione D3DXMatrixOrthoLH (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="270ea-103">D3DXMatrixOrthoLH function (D3DX10Math.h)</span></span>

<span data-ttu-id="270ea-104">Compila una matrice di proiezione ortografica mancino.</span><span class="sxs-lookup"><span data-stu-id="270ea-104">Builds a left-handed orthographic projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="270ea-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="270ea-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixOrthoLH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      w,
  _In_    FLOAT      h,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="270ea-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="270ea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="270ea-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="270ea-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="270ea-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="270ea-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="270ea-109">Puntatore all'oggetto [**D3DXMATRIX risultante.**](d3d10-d3dxmatrix.md)</span><span class="sxs-lookup"><span data-stu-id="270ea-109">Pointer to the resulting [**D3DXMATRIX**](d3d10-d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="270ea-110">*w* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="270ea-110">*w* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="270ea-111">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="270ea-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="270ea-112">Larghezza del volume della vista.</span><span class="sxs-lookup"><span data-stu-id="270ea-112">Width of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="270ea-113">*h* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="270ea-113">*h* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="270ea-114">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="270ea-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="270ea-115">Altezza del volume della vista.</span><span class="sxs-lookup"><span data-stu-id="270ea-115">Height of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="270ea-116">*zn* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="270ea-116">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="270ea-117">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="270ea-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="270ea-118">Valore z minimo del volume della vista, definito z-near.</span><span class="sxs-lookup"><span data-stu-id="270ea-118">Minimum z-value of the view volume which is referred to as z-near.</span></span>

</dd> <dt>

<span data-ttu-id="270ea-119">*zf* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="270ea-119">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="270ea-120">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="270ea-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="270ea-121">Valore z massimo del volume della vista, definito z-far.</span><span class="sxs-lookup"><span data-stu-id="270ea-121">Maximum z-value of the view volume which is referred to as z-far.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="270ea-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="270ea-122">Return value</span></span>

<span data-ttu-id="270ea-123">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="270ea-123">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="270ea-124">Puntatore all'oggetto [**D3DXMATRIX risultante.**](d3d10-d3dxmatrix.md)</span><span class="sxs-lookup"><span data-stu-id="270ea-124">Pointer to the resulting [**D3DXMATRIX**](d3d10-d3dxmatrix.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="270ea-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="270ea-125">Remarks</span></span>

<span data-ttu-id="270ea-126">Tutti i parametri della funzione D3DXMatrixOrthoLH sono distanze nello spazio della fotocamera.</span><span class="sxs-lookup"><span data-stu-id="270ea-126">All the parameters of the D3DXMatrixOrthoLH function are distances in camera space.</span></span> <span data-ttu-id="270ea-127">I parametri descrivono le dimensioni del volume di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="270ea-127">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="270ea-128">Il valore restituito per questa funzione è lo stesso valore restituito nel parametro pOut.</span><span class="sxs-lookup"><span data-stu-id="270ea-128">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="270ea-129">In questo modo, la funzione D3DXMatrixOrthoLH può essere usata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="270ea-129">In this way, the D3DXMatrixOrthoLH function can be used as a parameter for another function.</span></span>

<span data-ttu-id="270ea-130">Questa funzione usa la formula seguente per calcolare la matrice restituita.</span><span class="sxs-lookup"><span data-stu-id="270ea-130">This function uses the following formula to compute the returned matrix.</span></span>


```
2/w  0    0           0
0    2/h  0           0
0    0    1/(zf-zn)   0
0    0    zn/(zn-zf)  1
```



## <a name="requirements"></a><span data-ttu-id="270ea-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="270ea-131">Requirements</span></span>



| <span data-ttu-id="270ea-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="270ea-132">Requirement</span></span> | <span data-ttu-id="270ea-133">Valore</span><span class="sxs-lookup"><span data-stu-id="270ea-133">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="270ea-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="270ea-134">Header</span></span><br/>  | <dl> <span data-ttu-id="270ea-135"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="270ea-135"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="270ea-136">Libreria</span><span class="sxs-lookup"><span data-stu-id="270ea-136">Library</span></span><br/> | <dl> <span data-ttu-id="270ea-137"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="270ea-137"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="270ea-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="270ea-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="270ea-139">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="270ea-139">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
