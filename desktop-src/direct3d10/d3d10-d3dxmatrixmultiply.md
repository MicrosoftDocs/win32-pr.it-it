---
description: 'Funzione D3DXMatrixMultiply (D3DX10Math.h): determina il prodotto di due matrici.'
ms.assetid: d15cd680-0e19-4353-9eee-73933663960e
title: Funzione D3DXMatrixMultiply (D3DX10Math.h)
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
ms.openlocfilehash: 89e103d441648643be0176ca34f72f6175c11213
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113129"
---
# <a name="d3dxmatrixmultiply-function-d3dx10mathh"></a><span data-ttu-id="9ded3-103">Funzione D3DXMatrixMultiply (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="9ded3-103">D3DXMatrixMultiply function (D3DX10Math.h)</span></span>

<span data-ttu-id="9ded3-104">Determina il prodotto di due matrici.</span><span class="sxs-lookup"><span data-stu-id="9ded3-104">Determines the product of two matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ded3-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9ded3-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixMultiply(
  _Inout_       D3DXMATRIX *pOut,
  _In_    const D3DXMATRIX *pM1,
  _In_    const D3DXMATRIX *pM2
);
```



## <a name="parameters"></a><span data-ttu-id="9ded3-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9ded3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ded3-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="9ded3-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="9ded3-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="9ded3-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="9ded3-109">Puntatore alla [**struttura D3DXMATRIX**](d3d10-d3dxmatrix.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="9ded3-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="9ded3-110">*pM1* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="9ded3-110">*pM1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ded3-111">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="9ded3-111">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="9ded3-112">Puntatore a una struttura D3DXMATRIX di origine (lato sinistro).</span><span class="sxs-lookup"><span data-stu-id="9ded3-112">Pointer to a source D3DXMATRIX structure (left hand side).</span></span>

</dd> <dt>

<span data-ttu-id="9ded3-113">*pM2* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="9ded3-113">*pM2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ded3-114">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="9ded3-114">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="9ded3-115">Puntatore a una struttura D3DXMATRIX di origine (lato destro).</span><span class="sxs-lookup"><span data-stu-id="9ded3-115">Pointer to a source D3DXMATRIX structure (right hand side).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ded3-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9ded3-116">Return value</span></span>

<span data-ttu-id="9ded3-117">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="9ded3-117">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="9ded3-118">Puntatore a una struttura D3DXMATRIX che è il prodotto di due matrici.</span><span class="sxs-lookup"><span data-stu-id="9ded3-118">Pointer to a D3DXMATRIX structure that is the product of two matrices.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ded3-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="9ded3-119">Remarks</span></span>

<span data-ttu-id="9ded3-120">Il risultato rappresenta la trasformazione M1 seguita dalla trasformazione M2 (Out = M1 \* M2).</span><span class="sxs-lookup"><span data-stu-id="9ded3-120">The result represents the transformation M1 followed by the transformation M2 (Out = M1 \* M2).</span></span>

<span data-ttu-id="9ded3-121">Il valore restituito per questa funzione è lo stesso valore restituito nel parametro pOut.</span><span class="sxs-lookup"><span data-stu-id="9ded3-121">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="9ded3-122">In questo modo, la funzione D3DXMatrixMultiply può essere usata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="9ded3-122">In this way, the D3DXMatrixMultiply function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ded3-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9ded3-123">Requirements</span></span>



| <span data-ttu-id="9ded3-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ded3-124">Requirement</span></span> | <span data-ttu-id="9ded3-125">Valore</span><span class="sxs-lookup"><span data-stu-id="9ded3-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9ded3-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9ded3-126">Header</span></span><br/>  | <dl> <span data-ttu-id="9ded3-127"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="9ded3-127"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="9ded3-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="9ded3-128">Library</span></span><br/> | <dl> <span data-ttu-id="9ded3-129"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="9ded3-129"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9ded3-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9ded3-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ded3-131">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="9ded3-131">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
