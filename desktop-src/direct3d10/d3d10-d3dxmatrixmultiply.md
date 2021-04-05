---
description: Determina il prodotto di due matrici.
ms.assetid: d15cd680-0e19-4353-9eee-73933663960e
title: Funzione D3DXMatrixMultiply (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixMultiply
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 5f07130c25ce9ef1c588309460e4e12e67bb2485
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969484"
---
# <a name="d3dxmatrixmultiply-function-d3dx10mathh"></a><span data-ttu-id="761a2-103">Funzione D3DXMatrixMultiply (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="761a2-103">D3DXMatrixMultiply function (D3DX10Math.h)</span></span>

<span data-ttu-id="761a2-104">Determina il prodotto di due matrici.</span><span class="sxs-lookup"><span data-stu-id="761a2-104">Determines the product of two matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="761a2-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="761a2-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixMultiply(
  _Inout_       D3DXMATRIX *pOut,
  _In_    const D3DXMATRIX *pM1,
  _In_    const D3DXMATRIX *pM2
);
```



## <a name="parameters"></a><span data-ttu-id="761a2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="761a2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="761a2-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="761a2-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="761a2-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="761a2-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="761a2-109">Puntatore alla struttura [**D3DXMATRIX**](d3d10-d3dxmatrix.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="761a2-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="761a2-110">*pM1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="761a2-110">*pM1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="761a2-111">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="761a2-111">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="761a2-112">Puntatore a una struttura D3DXMATRIX di origine (lato sinistro).</span><span class="sxs-lookup"><span data-stu-id="761a2-112">Pointer to a source D3DXMATRIX structure (left hand side).</span></span>

</dd> <dt>

<span data-ttu-id="761a2-113">*pM2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="761a2-113">*pM2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="761a2-114">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="761a2-114">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="761a2-115">Puntatore a una struttura D3DXMATRIX di origine (lato destro).</span><span class="sxs-lookup"><span data-stu-id="761a2-115">Pointer to a source D3DXMATRIX structure (right hand side).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="761a2-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="761a2-116">Return value</span></span>

<span data-ttu-id="761a2-117">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="761a2-117">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="761a2-118">Puntatore a una struttura D3DXMATRIX che è il prodotto di due matrici.</span><span class="sxs-lookup"><span data-stu-id="761a2-118">Pointer to a D3DXMATRIX structure that is the product of two matrices.</span></span>

## <a name="remarks"></a><span data-ttu-id="761a2-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="761a2-119">Remarks</span></span>

<span data-ttu-id="761a2-120">Il risultato rappresenta la trasformazione M1 seguita dalla trasformazione m2 (out = M1 \* m2).</span><span class="sxs-lookup"><span data-stu-id="761a2-120">The result represents the transformation M1 followed by the transformation M2 (Out = M1 \* M2).</span></span>

<span data-ttu-id="761a2-121">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro broncio.</span><span class="sxs-lookup"><span data-stu-id="761a2-121">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="761a2-122">In questo modo, la funzione D3DXMatrixMultiply può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="761a2-122">In this way, the D3DXMatrixMultiply function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="761a2-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="761a2-123">Requirements</span></span>



| <span data-ttu-id="761a2-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="761a2-124">Requirement</span></span> | <span data-ttu-id="761a2-125">Valore</span><span class="sxs-lookup"><span data-stu-id="761a2-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="761a2-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="761a2-126">Header</span></span><br/>  | <dl> <span data-ttu-id="761a2-127"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="761a2-127"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="761a2-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="761a2-128">Library</span></span><br/> | <dl> <span data-ttu-id="761a2-129"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="761a2-129"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="761a2-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="761a2-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="761a2-131">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="761a2-131">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
