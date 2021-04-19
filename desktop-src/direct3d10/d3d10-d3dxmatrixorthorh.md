---
description: Compila una matrice di proiezione ortogonale a destra.
ms.assetid: e6673ff4-06a2-4a16-b72e-5ca69ddf2438
title: Funzione D3DXMatrixOrthoRH (D3DX10Math. h)
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
ms.openlocfilehash: 2a8883f2690fa5a5f0bfa1bb1570163b714974b3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323212"
---
# <a name="d3dxmatrixorthorh-function-d3dx10mathh"></a><span data-ttu-id="b753e-103">Funzione D3DXMatrixOrthoRH (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="b753e-103">D3DXMatrixOrthoRH function (D3DX10Math.h)</span></span>

<span data-ttu-id="b753e-104">Compila una matrice di proiezione ortogonale a destra.</span><span class="sxs-lookup"><span data-stu-id="b753e-104">Builds a right-handed orthographic projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="b753e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b753e-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixOrthoRH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      w,
  _In_    FLOAT      h,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="b753e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b753e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b753e-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="b753e-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b753e-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="b753e-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="b753e-109">Puntatore al [**D3DXMATRIX**](d3d10-d3dxmatrix.md)risultante.</span><span class="sxs-lookup"><span data-stu-id="b753e-109">Pointer to the resulting [**D3DXMATRIX**](d3d10-d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="b753e-110">*w* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b753e-110">*w* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b753e-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b753e-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b753e-112">Larghezza del volume di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="b753e-112">Width of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="b753e-113">*h* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b753e-113">*h* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b753e-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b753e-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b753e-115">Altezza del volume di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="b753e-115">Height of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="b753e-116">*Zn* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b753e-116">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b753e-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b753e-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b753e-118">Valore z minimo del volume di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="b753e-118">Minimum z-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="b753e-119">*ZF* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b753e-119">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b753e-120">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b753e-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b753e-121">Valore z massimo del volume di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="b753e-121">Maximum z-value of the view volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b753e-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b753e-122">Return value</span></span>

<span data-ttu-id="b753e-123">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="b753e-123">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="b753e-124">Puntatore al [**D3DXMATRIX**](d3d10-d3dxmatrix.md)risultante.</span><span class="sxs-lookup"><span data-stu-id="b753e-124">Pointer to the resulting [**D3DXMATRIX**](d3d10-d3dxmatrix.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b753e-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="b753e-125">Remarks</span></span>

<span data-ttu-id="b753e-126">Tutti i parametri della funzione D3DXMatrixOrthoRH sono distanze nello spazio della fotocamera.</span><span class="sxs-lookup"><span data-stu-id="b753e-126">All the parameters of the D3DXMatrixOrthoRH function are distances in camera space.</span></span> <span data-ttu-id="b753e-127">I parametri descrivono le dimensioni del volume di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="b753e-127">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="b753e-128">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro broncio.</span><span class="sxs-lookup"><span data-stu-id="b753e-128">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="b753e-129">In questo modo, la funzione D3DXMatrixOrthoRH può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="b753e-129">In this way, the D3DXMatrixOrthoRH function can be used as a parameter for another function.</span></span>

<span data-ttu-id="b753e-130">Questa funzione usa la formula seguente per calcolare la matrice restituita.</span><span class="sxs-lookup"><span data-stu-id="b753e-130">This function uses the following formula to compute the returned matrix.</span></span>


```
2/w  0    0           0
0    2/h  0           0
0    0    1/(zn-zf)   0
0    0    zn/(zn-zf)  1
```



## <a name="requirements"></a><span data-ttu-id="b753e-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b753e-131">Requirements</span></span>



| <span data-ttu-id="b753e-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="b753e-132">Requirement</span></span> | <span data-ttu-id="b753e-133">Valore</span><span class="sxs-lookup"><span data-stu-id="b753e-133">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b753e-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b753e-134">Header</span></span><br/>  | <dl> <span data-ttu-id="b753e-135"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="b753e-135"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="b753e-136">Libreria</span><span class="sxs-lookup"><span data-stu-id="b753e-136">Library</span></span><br/> | <dl> <span data-ttu-id="b753e-137"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b753e-137"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b753e-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b753e-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b753e-139">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="b753e-139">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
