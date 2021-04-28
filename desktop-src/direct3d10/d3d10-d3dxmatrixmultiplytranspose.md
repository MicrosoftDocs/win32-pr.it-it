---
description: 'Funzione D3DXMatrixMultiplyTranspose (D3DX10Math.h): calcola il prodotto trasposto di due matrici.'
ms.assetid: 3db4138c-407c-47b5-b8b9-04af8771e98e
title: Funzione D3DXMatrixMultiplyTranspose (D3DX10Math.h)
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
ms.openlocfilehash: fcf3d5578aa6e2ad13bd3f91dfd2206d6eaf0b13
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103418"
---
# <a name="d3dxmatrixmultiplytranspose-function-d3dx10mathh"></a><span data-ttu-id="b40e9-103">Funzione D3DXMatrixMultiplyTranspose (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="b40e9-103">D3DXMatrixMultiplyTranspose function (D3DX10Math.h)</span></span>

<span data-ttu-id="b40e9-104">Calcola il prodotto trasposto di due matrici.</span><span class="sxs-lookup"><span data-stu-id="b40e9-104">Calculates the transposed product of two matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="b40e9-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b40e9-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixMultiplyTranspose(
  _Inout_       D3DXMATRIX *pOut,
  _In_    const D3DXMATRIX *pM1,
  _In_    const D3DXMATRIX *pM2
);
```



## <a name="parameters"></a><span data-ttu-id="b40e9-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b40e9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b40e9-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="b40e9-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b40e9-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="b40e9-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="b40e9-109">Puntatore alla [**struttura D3DXMATRIX**](d3d10-d3dxmatrix.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="b40e9-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="b40e9-110">*pM1* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="b40e9-110">*pM1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b40e9-111">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="b40e9-111">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="b40e9-112">Puntatore a una struttura D3DXMATRIX di origine (lato sinistro).</span><span class="sxs-lookup"><span data-stu-id="b40e9-112">Pointer to a source D3DXMATRIX structure (left hand side).</span></span>

</dd> <dt>

<span data-ttu-id="b40e9-113">*pM2* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="b40e9-113">*pM2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b40e9-114">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="b40e9-114">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="b40e9-115">Puntatore a una struttura D3DXMATRIX di origine (lato destro).</span><span class="sxs-lookup"><span data-stu-id="b40e9-115">Pointer to a source D3DXMATRIX structure (right hand side).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b40e9-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b40e9-116">Return value</span></span>

<span data-ttu-id="b40e9-117">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="b40e9-117">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="b40e9-118">Puntatore a una struttura D3DXMATRIX che è il prodotto di due matrici.</span><span class="sxs-lookup"><span data-stu-id="b40e9-118">Pointer to a D3DXMATRIX structure that is the product of two matrices.</span></span>

## <a name="remarks"></a><span data-ttu-id="b40e9-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="b40e9-119">Remarks</span></span>

<span data-ttu-id="b40e9-120">Il risultato è il prodotto trasposto di due matrici di trasformazione, Out = T(M1 \* M2).</span><span class="sxs-lookup"><span data-stu-id="b40e9-120">The result is the transposed of the product of two transformation matrices, Out = T(M1\*M2).</span></span>

<span data-ttu-id="b40e9-121">Il valore restituito per questa funzione è lo stesso valore restituito nel parametro pOut.</span><span class="sxs-lookup"><span data-stu-id="b40e9-121">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="b40e9-122">In questo modo, la funzione D3DXMatrixMultiplyTranspose può essere usata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="b40e9-122">In this way, the D3DXMatrixMultiplyTranspose function can be used as a parameter for another function.</span></span>

<span data-ttu-id="b40e9-123">Questa funzione è utile per impostare le matrici come costanti per vertici e pixel shader.</span><span class="sxs-lookup"><span data-stu-id="b40e9-123">This function is useful to set matrices as constants for vertex and pixel shaders.</span></span>

## <a name="requirements"></a><span data-ttu-id="b40e9-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b40e9-124">Requirements</span></span>



| <span data-ttu-id="b40e9-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="b40e9-125">Requirement</span></span> | <span data-ttu-id="b40e9-126">Valore</span><span class="sxs-lookup"><span data-stu-id="b40e9-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b40e9-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b40e9-127">Header</span></span><br/>  | <dl> <span data-ttu-id="b40e9-128"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="b40e9-128"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="b40e9-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="b40e9-129">Library</span></span><br/> | <dl> <span data-ttu-id="b40e9-130"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="b40e9-130"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b40e9-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b40e9-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b40e9-132">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="b40e9-132">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
