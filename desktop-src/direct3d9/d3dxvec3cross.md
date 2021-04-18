---
description: Determina il prodotto incrociato di due vettori 3D.
ms.assetid: c9623f35-c8fc-4fbe-87b6-0e5bb8ebd5e8
title: Funzione D3DXVec3Cross (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Cross
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ba0d8a80690f43d5f8e9f6df55aa3b2e0db23dc2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322626"
---
# <a name="d3dxvec3cross-function"></a><span data-ttu-id="e635c-103">D3DXVec3Cross (funzione)</span><span class="sxs-lookup"><span data-stu-id="e635c-103">D3DXVec3Cross function</span></span>

<span data-ttu-id="e635c-104">Determina il prodotto incrociato di due vettori 3D.</span><span class="sxs-lookup"><span data-stu-id="e635c-104">Determines the cross-product of two 3D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="e635c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e635c-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3Cross(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV1,
  _In_    const D3DXVECTOR3 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="e635c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e635c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e635c-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="e635c-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e635c-108">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="e635c-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="e635c-109">Puntatore alla struttura [**D3DXVECTOR3**](d3dxvector3.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="e635c-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="e635c-110">*pV1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e635c-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e635c-111">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="e635c-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="e635c-112">Puntatore a una struttura [**D3DXVECTOR3**](d3dxvector3.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="e635c-112">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="e635c-113">*pV2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e635c-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e635c-114">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="e635c-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="e635c-115">Puntatore a una struttura [**D3DXVECTOR3**](d3dxvector3.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="e635c-115">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e635c-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e635c-116">Return value</span></span>

<span data-ttu-id="e635c-117">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="e635c-117">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="e635c-118">Puntatore a una struttura [**D3DXVECTOR3**](d3dxvector3.md) che rappresenta il prodotto incrociato di due vettori 3D.</span><span class="sxs-lookup"><span data-stu-id="e635c-118">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the cross product of two 3D vectors.</span></span>

## <a name="remarks"></a><span data-ttu-id="e635c-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="e635c-119">Remarks</span></span>

<span data-ttu-id="e635c-120">Questa funzione determina il prodotto incrociato con il codice seguente.</span><span class="sxs-lookup"><span data-stu-id="e635c-120">This function determines the cross-product with the following code.</span></span>


```
D3DXVECTOR3 v;
    
v.x = pV1->y * pV2->z - pV1->z * pV2->y;
v.y = pV1->z * pV2->x - pV1->x * pV2->z;
v.z = pV1->x * pV2->y - pV1->y * pV2->x;
    
*pOut = v;
```



<span data-ttu-id="e635c-121">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro *broncio* .</span><span class="sxs-lookup"><span data-stu-id="e635c-121">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="e635c-122">In questo modo, la funzione **D3DXVec3Cross** può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="e635c-122">In this way, the **D3DXVec3Cross** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="e635c-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e635c-123">Requirements</span></span>



| <span data-ttu-id="e635c-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="e635c-124">Requirement</span></span> | <span data-ttu-id="e635c-125">Valore</span><span class="sxs-lookup"><span data-stu-id="e635c-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e635c-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e635c-126">Header</span></span><br/>  | <dl> <span data-ttu-id="e635c-127"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="e635c-127"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="e635c-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="e635c-128">Library</span></span><br/> | <dl> <span data-ttu-id="e635c-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e635c-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e635c-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e635c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e635c-131">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="e635c-131">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="e635c-132">**D3DXVec3Dot**</span><span class="sxs-lookup"><span data-stu-id="e635c-132">**D3DXVec3Dot**</span></span>](d3dxvec3dot.md)
</dt> </dl>

 

 




