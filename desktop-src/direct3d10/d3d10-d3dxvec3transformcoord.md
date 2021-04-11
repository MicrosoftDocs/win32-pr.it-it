---
description: Trasforma un vettore 3D in base a una matrice specificata, proiettando il risultato in w = 1.
ms.assetid: e138fdc0-6999-45ab-8bcf-54f53bd9b1bf
title: Funzione D3DXVec3TransformCoord (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3TransformCoord
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: a8fc7c7a00133e036921eabaa145dca01a12f042
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354969"
---
# <a name="d3dxvec3transformcoord-function-d3dx10mathh"></a><span data-ttu-id="e6039-103">Funzione D3DXVec3TransformCoord (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="e6039-103">D3DXVec3TransformCoord function (D3DX10Math.h)</span></span>

<span data-ttu-id="e6039-104">Trasforma un vettore 3D in base a una matrice specificata, proiettando il risultato in w = 1.</span><span class="sxs-lookup"><span data-stu-id="e6039-104">Transforms a 3D vector by a given matrix, projecting the result back into w = 1.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6039-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e6039-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3TransformCoord(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="e6039-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e6039-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6039-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="e6039-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e6039-108">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="e6039-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="e6039-109">Puntatore a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="e6039-109">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="e6039-110">*PV* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e6039-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6039-111">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="e6039-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="e6039-112">Puntatore alla struttura D3DXVECTOR3 di origine.</span><span class="sxs-lookup"><span data-stu-id="e6039-112">Pointer to the source D3DXVECTOR3 structure.</span></span>

</dd> <dt>

<span data-ttu-id="e6039-113">*PM* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e6039-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6039-114">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="e6039-114">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="e6039-115">Puntatore alla struttura [**D3DXMATRIX**](d3d10-d3dxmatrix.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="e6039-115">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6039-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e6039-116">Return value</span></span>

<span data-ttu-id="e6039-117">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="e6039-117">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="e6039-118">Puntatore a una struttura D3DXVECTOR3 che rappresenta il vettore trasformato.</span><span class="sxs-lookup"><span data-stu-id="e6039-118">Pointer to a D3DXVECTOR3 structure that is the transformed vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6039-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="e6039-119">Remarks</span></span>

<span data-ttu-id="e6039-120">Questa funzione trasforma il vettore, pV (x, y, z, 1), dalla matrice, pM, proiettando il risultato in w = 1.</span><span class="sxs-lookup"><span data-stu-id="e6039-120">This function transforms the vector, pV (x, y, z, 1), by the matrix, pM, projecting the result back into w=1.</span></span>

<span data-ttu-id="e6039-121">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro broncio.</span><span class="sxs-lookup"><span data-stu-id="e6039-121">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="e6039-122">In questo modo, la funzione D3DXVec3TransformCoord può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="e6039-122">In this way, the D3DXVec3TransformCoord function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6039-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e6039-123">Requirements</span></span>



| <span data-ttu-id="e6039-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6039-124">Requirement</span></span> | <span data-ttu-id="e6039-125">Valore</span><span class="sxs-lookup"><span data-stu-id="e6039-125">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e6039-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e6039-126">Header</span></span><br/> | <dl> <span data-ttu-id="e6039-127"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="e6039-127"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6039-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e6039-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6039-129">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="e6039-129">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
