---
description: Determina il prodotto incrociato in quattro dimensioni.
ms.assetid: 10b965c9-7ed7-450c-86a0-114f068c888f
title: Funzione D3DXVec4Cross (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Cross
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 91e6e5662bff503ba96d96f135f98e60cf15c8fe
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235056"
---
# <a name="d3dxvec4cross-function-d3dx9mathh"></a><span data-ttu-id="350a2-103">Funzione D3DXVec4Cross (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="350a2-103">D3DXVec4Cross function (D3dx9math.h)</span></span>

<span data-ttu-id="350a2-104">Determina il prodotto incrociato in quattro dimensioni.</span><span class="sxs-lookup"><span data-stu-id="350a2-104">Determines the cross-product in four dimensions.</span></span>

## <a name="syntax"></a><span data-ttu-id="350a2-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="350a2-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4Cross(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV1,
  _In_    const D3DXVECTOR4 *pV2,
  _In_    const D3DXVECTOR4 *pV3
);
```



## <a name="parameters"></a><span data-ttu-id="350a2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="350a2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="350a2-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="350a2-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="350a2-108">Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="350a2-108">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="350a2-109">Puntatore alla struttura [**D3DXVECTOR4**](d3dxvector4.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="350a2-109">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="350a2-110">*pV1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="350a2-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="350a2-111">Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="350a2-111">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="350a2-112">Puntatore a una struttura [**D3DXVECTOR4**](d3dxvector4.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="350a2-112">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="350a2-113">*pV2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="350a2-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="350a2-114">Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="350a2-114">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="350a2-115">Puntatore a una struttura [**D3DXVECTOR4**](d3dxvector4.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="350a2-115">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="350a2-116">*pV3* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="350a2-116">*pV3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="350a2-117">Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="350a2-117">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="350a2-118">Puntatore a una struttura [**D3DXVECTOR4**](d3dxvector4.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="350a2-118">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="350a2-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="350a2-119">Return value</span></span>

<span data-ttu-id="350a2-120">Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="350a2-120">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="350a2-121">Puntatore a una struttura [**D3DXVECTOR4**](d3dxvector4.md) che rappresenta il prodotto incrociato.</span><span class="sxs-lookup"><span data-stu-id="350a2-121">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure that is the cross product.</span></span>

## <a name="remarks"></a><span data-ttu-id="350a2-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="350a2-122">Remarks</span></span>

<span data-ttu-id="350a2-123">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro *broncio* .</span><span class="sxs-lookup"><span data-stu-id="350a2-123">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="350a2-124">In questo modo, la funzione **D3DXVec4Cross** può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="350a2-124">In this way, the **D3DXVec4Cross** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="350a2-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="350a2-125">Requirements</span></span>



| <span data-ttu-id="350a2-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="350a2-126">Requirement</span></span> | <span data-ttu-id="350a2-127">Valore</span><span class="sxs-lookup"><span data-stu-id="350a2-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="350a2-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="350a2-128">Header</span></span><br/>  | <dl> <span data-ttu-id="350a2-129"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="350a2-129"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="350a2-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="350a2-130">Library</span></span><br/> | <dl> <span data-ttu-id="350a2-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="350a2-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="350a2-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="350a2-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="350a2-133">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="350a2-133">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="350a2-134">**D3DXVec4Dot**</span><span class="sxs-lookup"><span data-stu-id="350a2-134">**D3DXVec4Dot**</span></span>](d3dxvec4dot.md)
</dt> </dl>

 

 




