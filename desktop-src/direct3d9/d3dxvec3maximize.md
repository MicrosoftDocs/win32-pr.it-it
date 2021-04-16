---
description: Restituisce un vettore 3D costituito dai componenti più grandi di due vettori 3D.
ms.assetid: 8d3a5310-bee9-4dbd-bef3-8a0e1586f365
title: Funzione D3DXVec3Maximize (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Maximize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7d86f3e54a6399693e37cc0c8970439558d82c9c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530871"
---
# <a name="d3dxvec3maximize-function"></a><span data-ttu-id="89467-103">D3DXVec3Maximize (funzione)</span><span class="sxs-lookup"><span data-stu-id="89467-103">D3DXVec3Maximize function</span></span>

<span data-ttu-id="89467-104">Restituisce un vettore 3D costituito dai componenti più grandi di due vettori 3D.</span><span class="sxs-lookup"><span data-stu-id="89467-104">Returns a 3D vector that is made up of the largest components of two 3D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="89467-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="89467-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3Maximize(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV1,
  _In_    const D3DXVECTOR3 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="89467-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="89467-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89467-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="89467-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="89467-108">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="89467-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="89467-109">Puntatore alla struttura [**D3DXVECTOR3**](d3dxvector3.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="89467-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="89467-110">*pV1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="89467-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89467-111">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="89467-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="89467-112">Puntatore a una struttura [**D3DXVECTOR3**](d3dxvector3.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="89467-112">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="89467-113">*pV2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="89467-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89467-114">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="89467-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="89467-115">Puntatore a una struttura [**D3DXVECTOR3**](d3dxvector3.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="89467-115">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89467-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="89467-116">Return value</span></span>

<span data-ttu-id="89467-117">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="89467-117">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="89467-118">Puntatore a una struttura [**D3DXVECTOR3**](d3dxvector3.md) costituita dai componenti più grandi dei due vettori.</span><span class="sxs-lookup"><span data-stu-id="89467-118">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is made up of the largest components of the two vectors.</span></span>

## <a name="remarks"></a><span data-ttu-id="89467-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="89467-119">Remarks</span></span>

<span data-ttu-id="89467-120">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro *broncio* .</span><span class="sxs-lookup"><span data-stu-id="89467-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="89467-121">In questo modo, la funzione **D3DXVec3Maximize** può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="89467-121">In this way, the **D3DXVec3Maximize** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="89467-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="89467-122">Requirements</span></span>



| <span data-ttu-id="89467-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="89467-123">Requirement</span></span> | <span data-ttu-id="89467-124">Valore</span><span class="sxs-lookup"><span data-stu-id="89467-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="89467-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="89467-125">Header</span></span><br/>  | <dl> <span data-ttu-id="89467-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="89467-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="89467-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="89467-127">Library</span></span><br/> | <dl> <span data-ttu-id="89467-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="89467-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="89467-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="89467-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89467-130">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="89467-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="89467-131">**D3DXVec3Minimize**</span><span class="sxs-lookup"><span data-stu-id="89467-131">**D3DXVec3Minimize**</span></span>](d3dxvec3minimize.md)
</dt> </dl>

 

 




