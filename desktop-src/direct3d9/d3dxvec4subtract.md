---
description: Sottrae due vettori 4D.
ms.assetid: 3bc55b38-818e-40eb-859e-495ee28fc4ae
title: Funzione D3DXVec4Subtract (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Subtract
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1110930d8e37cf04f7de5129c2a72db4ecc4ac8d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104356134"
---
# <a name="d3dxvec4subtract-function"></a><span data-ttu-id="1eafb-103">D3DXVec4Subtract (funzione)</span><span class="sxs-lookup"><span data-stu-id="1eafb-103">D3DXVec4Subtract function</span></span>

<span data-ttu-id="1eafb-104">Sottrae due vettori 4D.</span><span class="sxs-lookup"><span data-stu-id="1eafb-104">Subtracts two 4D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="1eafb-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1eafb-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4Subtract(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV1,
  _In_    const D3DXVECTOR4 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="1eafb-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1eafb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1eafb-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="1eafb-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1eafb-108">Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="1eafb-108">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="1eafb-109">Puntatore alla struttura [**D3DXVECTOR4**](d3dxvector4.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="1eafb-109">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="1eafb-110">*pV1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1eafb-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1eafb-111">Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="1eafb-111">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="1eafb-112">Puntatore a una struttura [**D3DXVECTOR4**](d3dxvector4.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="1eafb-112">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="1eafb-113">*pV2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1eafb-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1eafb-114">Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="1eafb-114">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="1eafb-115">Puntatore a una struttura [**D3DXVECTOR4**](d3dxvector4.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="1eafb-115">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1eafb-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1eafb-116">Return value</span></span>

<span data-ttu-id="1eafb-117">Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="1eafb-117">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="1eafb-118">Puntatore a una struttura [**D3DXVECTOR4**](d3dxvector4.md) che rappresenta la differenza di due vettori.</span><span class="sxs-lookup"><span data-stu-id="1eafb-118">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure that is the difference of two vectors.</span></span>

## <a name="remarks"></a><span data-ttu-id="1eafb-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="1eafb-119">Remarks</span></span>

<span data-ttu-id="1eafb-120">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro *broncio* .</span><span class="sxs-lookup"><span data-stu-id="1eafb-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="1eafb-121">In questo modo, la funzione **D3DXVec4Subtract** può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="1eafb-121">In this way, the **D3DXVec4Subtract** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="1eafb-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1eafb-122">Requirements</span></span>



| <span data-ttu-id="1eafb-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="1eafb-123">Requirement</span></span> | <span data-ttu-id="1eafb-124">Valore</span><span class="sxs-lookup"><span data-stu-id="1eafb-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1eafb-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1eafb-125">Header</span></span><br/>  | <dl> <span data-ttu-id="1eafb-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="1eafb-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="1eafb-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="1eafb-127">Library</span></span><br/> | <dl> <span data-ttu-id="1eafb-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1eafb-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1eafb-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1eafb-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1eafb-130">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="1eafb-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="1eafb-131">**D3DXVec3Add**</span><span class="sxs-lookup"><span data-stu-id="1eafb-131">**D3DXVec3Add**</span></span>](d3dxvec3add.md)
</dt> <dt>

[<span data-ttu-id="1eafb-132">**D3DXVec3Scale**</span><span class="sxs-lookup"><span data-stu-id="1eafb-132">**D3DXVec3Scale**</span></span>](d3dxvec3scale.md)
</dt> </dl>

 

 




