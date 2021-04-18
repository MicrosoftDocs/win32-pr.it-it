---
description: Calcola il prodotto trasposto di due matrici.
ms.assetid: 3db4138c-407c-47b5-b8b9-04af8771e98e
title: Funzione D3DXMatrixMultiplyTranspose (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixMultiplyTranspose
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 187912a4117ab502ea7b0b1b3fc1ea105ecbc3e7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323409"
---
# <a name="d3dxmatrixmultiplytranspose-function-d3dx10mathh"></a><span data-ttu-id="5ee54-103">Funzione D3DXMatrixMultiplyTranspose (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="5ee54-103">D3DXMatrixMultiplyTranspose function (D3DX10Math.h)</span></span>

<span data-ttu-id="5ee54-104">Calcola il prodotto trasposto di due matrici.</span><span class="sxs-lookup"><span data-stu-id="5ee54-104">Calculates the transposed product of two matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ee54-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5ee54-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixMultiplyTranspose(
  _Inout_       D3DXMATRIX *pOut,
  _In_    const D3DXMATRIX *pM1,
  _In_    const D3DXMATRIX *pM2
);
```



## <a name="parameters"></a><span data-ttu-id="5ee54-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5ee54-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ee54-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="5ee54-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5ee54-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="5ee54-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="5ee54-109">Puntatore alla struttura [**D3DXMATRIX**](d3d10-d3dxmatrix.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="5ee54-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="5ee54-110">*pM1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5ee54-110">*pM1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ee54-111">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="5ee54-111">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="5ee54-112">Puntatore a una struttura D3DXMATRIX di origine (lato sinistro).</span><span class="sxs-lookup"><span data-stu-id="5ee54-112">Pointer to a source D3DXMATRIX structure (left hand side).</span></span>

</dd> <dt>

<span data-ttu-id="5ee54-113">*pM2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5ee54-113">*pM2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ee54-114">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="5ee54-114">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="5ee54-115">Puntatore a una struttura D3DXMATRIX di origine (lato destro).</span><span class="sxs-lookup"><span data-stu-id="5ee54-115">Pointer to a source D3DXMATRIX structure (right hand side).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ee54-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5ee54-116">Return value</span></span>

<span data-ttu-id="5ee54-117">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="5ee54-117">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="5ee54-118">Puntatore a una struttura D3DXMATRIX che è il prodotto di due matrici.</span><span class="sxs-lookup"><span data-stu-id="5ee54-118">Pointer to a D3DXMATRIX structure that is the product of two matrices.</span></span>

## <a name="remarks"></a><span data-ttu-id="5ee54-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="5ee54-119">Remarks</span></span>

<span data-ttu-id="5ee54-120">Il risultato è l'oggetto trasposto dal prodotto di due matrici di trasformazione, out = T (M1 \* m2).</span><span class="sxs-lookup"><span data-stu-id="5ee54-120">The result is the transposed of the product of two transformation matrices, Out = T(M1\*M2).</span></span>

<span data-ttu-id="5ee54-121">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro broncio.</span><span class="sxs-lookup"><span data-stu-id="5ee54-121">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="5ee54-122">In questo modo, la funzione D3DXMatrixMultiplyTranspose può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="5ee54-122">In this way, the D3DXMatrixMultiplyTranspose function can be used as a parameter for another function.</span></span>

<span data-ttu-id="5ee54-123">Questa funzione è utile per impostare matrici come costanti per i vertex e i pixel shader.</span><span class="sxs-lookup"><span data-stu-id="5ee54-123">This function is useful to set matrices as constants for vertex and pixel shaders.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ee54-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5ee54-124">Requirements</span></span>



| <span data-ttu-id="5ee54-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ee54-125">Requirement</span></span> | <span data-ttu-id="5ee54-126">Valore</span><span class="sxs-lookup"><span data-stu-id="5ee54-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ee54-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5ee54-127">Header</span></span><br/>  | <dl> <span data-ttu-id="5ee54-128"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ee54-128"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="5ee54-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="5ee54-129">Library</span></span><br/> | <dl> <span data-ttu-id="5ee54-130"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5ee54-130"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5ee54-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5ee54-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ee54-132">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="5ee54-132">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
