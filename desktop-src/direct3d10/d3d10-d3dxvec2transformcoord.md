---
description: 'Funzione D3DXVec2TransformCoord (D3DX10Math.h): trasforma un vettore 2D in base a una determinata matrice, proiettando di nuovo il risultato in w = 1.'
ms.assetid: bb24204f-0c8e-4dc5-bcae-12e3033d1a39
title: Funzione D3DXVec2TransformCoord (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2TransformCoord
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 95321d377ad5af29075764e2c2d9386abf5b1441
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108339"
---
# <a name="d3dxvec2transformcoord-function-d3dx10mathh"></a><span data-ttu-id="a4454-103">Funzione D3DXVec2TransformCoord (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="a4454-103">D3DXVec2TransformCoord function (D3DX10Math.h)</span></span>

<span data-ttu-id="a4454-104">Trasforma un vettore 2D in base a una determinata matrice, proiettando il risultato in w = 1.</span><span class="sxs-lookup"><span data-stu-id="a4454-104">Transforms a 2D vector by a given matrix, projecting the result back into w = 1.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4454-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a4454-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2TransformCoord(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="a4454-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a4454-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4454-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="a4454-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a4454-108">Tipo: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="a4454-108">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="a4454-109">Puntatore [**all'oggetto D3DXVECTOR2**](d3d10-d3dxvector2.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="a4454-109">Pointer to the [**D3DXVECTOR2**](d3d10-d3dxvector2.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="a4454-110">*pV* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="a4454-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4454-111">Tipo: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="a4454-111">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="a4454-112">Puntatore alla struttura D3DXVECTOR2 di origine.</span><span class="sxs-lookup"><span data-stu-id="a4454-112">Pointer to the source D3DXVECTOR2 structure.</span></span>

</dd> <dt>

<span data-ttu-id="a4454-113">*pM* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="a4454-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4454-114">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="a4454-114">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="a4454-115">Puntatore alla struttura [**D3DXMATRIX di**](d3d10-d3dxmatrix.md) origine.</span><span class="sxs-lookup"><span data-stu-id="a4454-115">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4454-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a4454-116">Return value</span></span>

<span data-ttu-id="a4454-117">Tipo: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="a4454-117">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="a4454-118">Puntatore a una struttura D3DXVECTOR2 che rappresenta il vettore trasformato.</span><span class="sxs-lookup"><span data-stu-id="a4454-118">Pointer to a D3DXVECTOR2 structure that is the transformed vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="a4454-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="a4454-119">Remarks</span></span>

<span data-ttu-id="a4454-120">Questa funzione trasforma il vettore, pV (x, y, 0, 1), dalla matrice, pM, proiettando di nuovo il risultato in w=1.</span><span class="sxs-lookup"><span data-stu-id="a4454-120">This function transforms the vector, pV (x, y, 0, 1), by the matrix, pM, projecting the result back into w=1.</span></span>

<span data-ttu-id="a4454-121">Il valore restituito per questa funzione è lo stesso valore restituito nel parametro pOut.</span><span class="sxs-lookup"><span data-stu-id="a4454-121">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="a4454-122">In questo modo, la funzione D3DXVec2TransformCoord può essere usata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="a4454-122">In this way, the D3DXVec2TransformCoord function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4454-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a4454-123">Requirements</span></span>



| <span data-ttu-id="a4454-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="a4454-124">Requirement</span></span> | <span data-ttu-id="a4454-125">Valore</span><span class="sxs-lookup"><span data-stu-id="a4454-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a4454-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a4454-126">Header</span></span><br/>  | <dl> <span data-ttu-id="a4454-127"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="a4454-127"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="a4454-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="a4454-128">Library</span></span><br/> | <dl> <span data-ttu-id="a4454-129"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="a4454-129"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a4454-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a4454-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4454-131">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="a4454-131">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
