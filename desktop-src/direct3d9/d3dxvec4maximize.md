---
description: Restituisce un vettore 4D costituito dai componenti più grandi di due vettori 4D.
ms.assetid: a08ceba0-938c-42af-8f32-b1fd8c12d926
title: Funzione D3DXVec4Maximize (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Maximize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c145094deec5bdfdca123e6e494b18bbee01ce5b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235227"
---
# <a name="d3dxvec4maximize-function"></a><span data-ttu-id="62c0c-103">D3DXVec4Maximize (funzione)</span><span class="sxs-lookup"><span data-stu-id="62c0c-103">D3DXVec4Maximize function</span></span>

<span data-ttu-id="62c0c-104">Restituisce un vettore 4D costituito dai componenti più grandi di due vettori 4D.</span><span class="sxs-lookup"><span data-stu-id="62c0c-104">Returns a 4D vector that is made up of the largest components of two 4D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="62c0c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="62c0c-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4Maximize(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV1,
  _In_    const D3DXVECTOR4 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="62c0c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="62c0c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62c0c-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="62c0c-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="62c0c-108">Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="62c0c-108">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="62c0c-109">Puntatore alla struttura [**D3DXVECTOR4**](d3dxvector4.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="62c0c-109">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="62c0c-110">*pV1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="62c0c-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62c0c-111">Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="62c0c-111">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="62c0c-112">Puntatore a una struttura [**D3DXVECTOR4**](d3dxvector4.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="62c0c-112">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="62c0c-113">*pV2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="62c0c-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62c0c-114">Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="62c0c-114">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="62c0c-115">Puntatore a una struttura [**D3DXVECTOR4**](d3dxvector4.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="62c0c-115">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62c0c-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="62c0c-116">Return value</span></span>

<span data-ttu-id="62c0c-117">Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="62c0c-117">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="62c0c-118">Puntatore a una struttura [**D3DXVECTOR4**](d3dxvector4.md) costituita dai componenti più grandi dei due vettori.</span><span class="sxs-lookup"><span data-stu-id="62c0c-118">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure that is made up of the largest components of the two vectors.</span></span>

## <a name="remarks"></a><span data-ttu-id="62c0c-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="62c0c-119">Remarks</span></span>

<span data-ttu-id="62c0c-120">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro *broncio* .</span><span class="sxs-lookup"><span data-stu-id="62c0c-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="62c0c-121">In questo modo, la funzione **D3DXVec4Maximize** può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="62c0c-121">In this way, the **D3DXVec4Maximize** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="62c0c-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="62c0c-122">Requirements</span></span>



| <span data-ttu-id="62c0c-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="62c0c-123">Requirement</span></span> | <span data-ttu-id="62c0c-124">Valore</span><span class="sxs-lookup"><span data-stu-id="62c0c-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="62c0c-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="62c0c-125">Header</span></span><br/>  | <dl> <span data-ttu-id="62c0c-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="62c0c-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="62c0c-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="62c0c-127">Library</span></span><br/> | <dl> <span data-ttu-id="62c0c-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="62c0c-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="62c0c-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="62c0c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62c0c-130">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="62c0c-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="62c0c-131">**D3DXVec4Minimize**</span><span class="sxs-lookup"><span data-stu-id="62c0c-131">**D3DXVec4Minimize**</span></span>](d3dxvec4minimize.md)
</dt> </dl>

 

 




