---
description: Compila una matrice che riflette il sistema di coordinate su un piano.
ms.assetid: bd2c5905-780e-4fac-a848-d7dbcfc390c6
title: Funzione D3DXMatrixReflect (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixReflect
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: d8c8f0fc8529730a46c403432ec0b5b5a86c8afa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323343"
---
# <a name="d3dxmatrixreflect-function-d3dx10mathh"></a><span data-ttu-id="782c3-103">Funzione D3DXMatrixReflect (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="782c3-103">D3DXMatrixReflect function (D3DX10Math.h)</span></span>

<span data-ttu-id="782c3-104">Compila una matrice che riflette il sistema di coordinate su un piano.</span><span class="sxs-lookup"><span data-stu-id="782c3-104">Builds a matrix that reflects the coordinate system about a plane.</span></span>

## <a name="syntax"></a><span data-ttu-id="782c3-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="782c3-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixReflect(
  _Inout_       D3DXMATRIX *pOut,
  _In_    const D3DXPLANE  *pPlane
);
```



## <a name="parameters"></a><span data-ttu-id="782c3-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="782c3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="782c3-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="782c3-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="782c3-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="782c3-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="782c3-109">Puntatore alla struttura [**D3DXMATRIX**](d3d10-d3dxmatrix.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="782c3-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="782c3-110">*pPlane* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="782c3-110">*pPlane* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="782c3-111">Tipo: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="782c3-111">Type: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="782c3-112">Puntatore all'origine [**D3DXPLANE**](d3d10-d3dxplane.md).</span><span class="sxs-lookup"><span data-stu-id="782c3-112">Pointer to the source [**D3DXPLANE**](d3d10-d3dxplane.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="782c3-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="782c3-113">Return value</span></span>

<span data-ttu-id="782c3-114">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="782c3-114">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="782c3-115">Puntatore a una struttura D3DXMATRIX che riflette il sistema di coordinate del piano di origine.</span><span class="sxs-lookup"><span data-stu-id="782c3-115">Pointer to a D3DXMATRIX structure that reflects the coordinate system about the source plane.</span></span>

## <a name="remarks"></a><span data-ttu-id="782c3-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="782c3-116">Remarks</span></span>

<span data-ttu-id="782c3-117">Questa funzione normalizza l'equazione del piano prima di creare la matrice riflesso.</span><span class="sxs-lookup"><span data-stu-id="782c3-117">This function normalizes the plane equation before it creates the reflected matrix.</span></span>

<span data-ttu-id="782c3-118">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro broncio.</span><span class="sxs-lookup"><span data-stu-id="782c3-118">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="782c3-119">In questo modo, la funzione D3DXMatrixReflect può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="782c3-119">In this way, the D3DXMatrixReflect function can be used as a parameter for another function.</span></span>

<span data-ttu-id="782c3-120">Questa funzione usa la formula seguente per calcolare la matrice restituita.</span><span class="sxs-lookup"><span data-stu-id="782c3-120">This function uses the following formula to compute the returned matrix.</span></span>


```
P = normalize(Plane);
    
-2 * P.a * P.a + 1  -2 * P.b * P.a      -2 * P.c * P.a        0
-2 * P.a * P.b      -2 * P.b * P.b + 1  -2 * P.c * P.b        0
-2 * P.a * P.c      -2 * P.b * P.c      -2 * P.c * P.c + 1    0
-2 * P.a * P.d      -2 * P.b * P.d      -2 * P.c * P.d        1
```



## <a name="requirements"></a><span data-ttu-id="782c3-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="782c3-121">Requirements</span></span>



| <span data-ttu-id="782c3-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="782c3-122">Requirement</span></span> | <span data-ttu-id="782c3-123">Valore</span><span class="sxs-lookup"><span data-stu-id="782c3-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="782c3-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="782c3-124">Header</span></span><br/>  | <dl> <span data-ttu-id="782c3-125"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="782c3-125"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="782c3-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="782c3-126">Library</span></span><br/> | <dl> <span data-ttu-id="782c3-127"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="782c3-127"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="782c3-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="782c3-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="782c3-129">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="782c3-129">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
