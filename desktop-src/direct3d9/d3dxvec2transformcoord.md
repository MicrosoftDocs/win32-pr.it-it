---
description: Trasforma un vettore 2D in base a una matrice specificata, proiettando il risultato in w = 1.
ms.assetid: 0c0efdf8-77df-4f4a-86ce-89e11555f4dc
title: Funzione D3DXVec2TransformCoord (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7bc047075cd2f9f6aba6903f85ea6960e78e0ba1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322865"
---
# <a name="d3dxvec2transformcoord-function-d3dx9mathh"></a><span data-ttu-id="138a4-103">Funzione D3DXVec2TransformCoord (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="138a4-103">D3DXVec2TransformCoord function (D3dx9math.h)</span></span>

<span data-ttu-id="138a4-104">Trasforma un vettore 2D in base a una matrice specificata, proiettando il risultato in w = 1.</span><span class="sxs-lookup"><span data-stu-id="138a4-104">Transforms a 2D vector by a given matrix, projecting the result back into w = 1.</span></span>

## <a name="syntax"></a><span data-ttu-id="138a4-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="138a4-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2TransformCoord(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="138a4-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="138a4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="138a4-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="138a4-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="138a4-108">Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="138a4-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="138a4-109">Puntatore alla struttura [**D3DXVECTOR2**](d3dxvector2.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="138a4-109">Pointer to the [**D3DXVECTOR2**](d3dxvector2.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="138a4-110">*PV* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="138a4-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="138a4-111">Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="138a4-111">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="138a4-112">Puntatore alla struttura [**D3DXVECTOR2**](d3dxvector2.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="138a4-112">Pointer to the source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="138a4-113">*PM* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="138a4-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="138a4-114">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="138a4-114">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="138a4-115">Puntatore alla struttura [**D3DXMATRIX**](d3dxmatrix.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="138a4-115">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="138a4-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="138a4-116">Return value</span></span>

<span data-ttu-id="138a4-117">Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="138a4-117">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="138a4-118">Puntatore a una struttura [**D3DXVECTOR2**](d3dxvector2.md) che rappresenta il vettore trasformato.</span><span class="sxs-lookup"><span data-stu-id="138a4-118">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure that is the transformed vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="138a4-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="138a4-119">Remarks</span></span>

<span data-ttu-id="138a4-120">Questa funzione trasforma il vettore, *PV* (x, y, 0, 1), dalla matrice, *PM*, proiettando il risultato in w = 1.</span><span class="sxs-lookup"><span data-stu-id="138a4-120">This function transforms the vector, *pV* (x, y, 0, 1), by the matrix, *pM*, projecting the result back into w=1.</span></span>

<span data-ttu-id="138a4-121">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro *broncio* .</span><span class="sxs-lookup"><span data-stu-id="138a4-121">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="138a4-122">In questo modo, la funzione **D3DXVec2TransformCoord** può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="138a4-122">In this way, the **D3DXVec2TransformCoord** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="138a4-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="138a4-123">Requirements</span></span>



| <span data-ttu-id="138a4-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="138a4-124">Requirement</span></span> | <span data-ttu-id="138a4-125">Valore</span><span class="sxs-lookup"><span data-stu-id="138a4-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="138a4-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="138a4-126">Header</span></span><br/>  | <dl> <span data-ttu-id="138a4-127"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="138a4-127"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="138a4-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="138a4-128">Library</span></span><br/> | <dl> <span data-ttu-id="138a4-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="138a4-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="138a4-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="138a4-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="138a4-131">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="138a4-131">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="138a4-132">**D3DXVec2Transform**</span><span class="sxs-lookup"><span data-stu-id="138a4-132">**D3DXVec2Transform**</span></span>](d3dxvec2transform.md)
</dt> <dt>

[<span data-ttu-id="138a4-133">**D3DXVec2TransformNormal**</span><span class="sxs-lookup"><span data-stu-id="138a4-133">**D3DXVec2TransformNormal**</span></span>](d3dxvec2transformnormal.md)
</dt> </dl>

 

 




