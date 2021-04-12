---
description: Trasforma un vettore 3D in base a una matrice specificata, proiettando il risultato in w = 1.
ms.assetid: 4075b067-1e64-46c9-be73-5fa765c9cb9d
title: Funzione D3DXVec3TransformCoord (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3TransformCoord
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4bcf1a78f9da4cf5fb2a5f67360a1659182c7ffb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355959"
---
# <a name="d3dxvec3transformcoord-function-d3dx9mathh"></a><span data-ttu-id="2cfc3-103">Funzione D3DXVec3TransformCoord (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="2cfc3-103">D3DXVec3TransformCoord function (D3dx9math.h)</span></span>

<span data-ttu-id="2cfc3-104">Trasforma un vettore 3D in base a una matrice specificata, proiettando il risultato in w = 1.</span><span class="sxs-lookup"><span data-stu-id="2cfc3-104">Transforms a 3D vector by a given matrix, projecting the result back into w = 1.</span></span>

## <a name="syntax"></a><span data-ttu-id="2cfc3-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2cfc3-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3TransformCoord(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="2cfc3-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2cfc3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2cfc3-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="2cfc3-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2cfc3-108">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="2cfc3-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="2cfc3-109">Puntatore alla struttura [**D3DXVECTOR3**](d3dxvector3.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="2cfc3-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="2cfc3-110">*PV* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2cfc3-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2cfc3-111">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="2cfc3-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="2cfc3-112">Puntatore alla struttura [**D3DXVECTOR3**](d3dxvector3.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="2cfc3-112">Pointer to the source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="2cfc3-113">*PM* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2cfc3-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2cfc3-114">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="2cfc3-114">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="2cfc3-115">Puntatore alla struttura [**D3DXMATRIX**](d3dxmatrix.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="2cfc3-115">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2cfc3-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2cfc3-116">Return value</span></span>

<span data-ttu-id="2cfc3-117">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="2cfc3-117">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="2cfc3-118">Puntatore a una struttura [**D3DXVECTOR3**](d3dxvector3.md) che rappresenta il vettore trasformato.</span><span class="sxs-lookup"><span data-stu-id="2cfc3-118">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the transformed vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="2cfc3-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="2cfc3-119">Remarks</span></span>

<span data-ttu-id="2cfc3-120">Questa funzione trasforma il vettore, *PV* (x, y, z, 1), dalla matrice, *PM*, proiettando il risultato in w = 1.</span><span class="sxs-lookup"><span data-stu-id="2cfc3-120">This function transforms the vector, *pV* (x, y, z, 1), by the matrix, *pM*, projecting the result back into w=1.</span></span>

<span data-ttu-id="2cfc3-121">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro *broncio* .</span><span class="sxs-lookup"><span data-stu-id="2cfc3-121">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="2cfc3-122">In questo modo, la funzione **D3DXVec3TransformCoord** può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="2cfc3-122">In this way, the **D3DXVec3TransformCoord** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="2cfc3-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2cfc3-123">Requirements</span></span>



| <span data-ttu-id="2cfc3-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="2cfc3-124">Requirement</span></span> | <span data-ttu-id="2cfc3-125">Valore</span><span class="sxs-lookup"><span data-stu-id="2cfc3-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2cfc3-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2cfc3-126">Header</span></span><br/>  | <dl> <span data-ttu-id="2cfc3-127"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="2cfc3-127"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="2cfc3-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="2cfc3-128">Library</span></span><br/> | <dl> <span data-ttu-id="2cfc3-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2cfc3-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2cfc3-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2cfc3-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2cfc3-131">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="2cfc3-131">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="2cfc3-132">**D3DXVec3Transform**</span><span class="sxs-lookup"><span data-stu-id="2cfc3-132">**D3DXVec3Transform**</span></span>](d3dxvec3transform.md)
</dt> <dt>

[<span data-ttu-id="2cfc3-133">**D3DXVec3TransformNormal**</span><span class="sxs-lookup"><span data-stu-id="2cfc3-133">**D3DXVec3TransformNormal**</span></span>](d3dxvec3transformnormal.md)
</dt> </dl>

 

 




