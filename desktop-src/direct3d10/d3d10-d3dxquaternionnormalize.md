---
description: Calcola un quaternione di lunghezza dell'unità.
ms.assetid: 6735a632-64d7-4bc1-b63e-d0cd27f5a29b
title: Funzione D3DXQuaternionNormalize (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionNormalize
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: e121ef4892c65a0f04acaa89d44d4a5a9090740e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235128"
---
# <a name="d3dxquaternionnormalize-function-d3dx10mathh"></a><span data-ttu-id="d51ad-103">Funzione D3DXQuaternionNormalize (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="d51ad-103">D3DXQuaternionNormalize function (D3DX10Math.h)</span></span>

<span data-ttu-id="d51ad-104">Calcola un quaternione di lunghezza dell'unità.</span><span class="sxs-lookup"><span data-stu-id="d51ad-104">Computes a unit length quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="d51ad-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d51ad-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionNormalize(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="d51ad-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d51ad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d51ad-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="d51ad-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d51ad-108">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="d51ad-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="d51ad-109">Puntatore a [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="d51ad-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="d51ad-110">*PQ* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d51ad-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d51ad-111">Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="d51ad-111">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="d51ad-112">Puntatore alla struttura D3DXQUATERNION di origine.</span><span class="sxs-lookup"><span data-stu-id="d51ad-112">Pointer to the source D3DXQUATERNION structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d51ad-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d51ad-113">Return value</span></span>

<span data-ttu-id="d51ad-114">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="d51ad-114">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="d51ad-115">Puntatore a una struttura D3DXQUATERNION che corrisponde al normale del quaternione.</span><span class="sxs-lookup"><span data-stu-id="d51ad-115">Pointer to a D3DXQUATERNION structure that is the normal of the quaternion.</span></span>

## <a name="remarks"></a><span data-ttu-id="d51ad-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="d51ad-116">Remarks</span></span>

<span data-ttu-id="d51ad-117">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro broncio.</span><span class="sxs-lookup"><span data-stu-id="d51ad-117">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="d51ad-118">In questo modo, la funzione D3DXQuaternionNormalize può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="d51ad-118">In this way, the D3DXQuaternionNormalize function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="d51ad-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d51ad-119">Requirements</span></span>



| <span data-ttu-id="d51ad-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="d51ad-120">Requirement</span></span> | <span data-ttu-id="d51ad-121">Valore</span><span class="sxs-lookup"><span data-stu-id="d51ad-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d51ad-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d51ad-122">Header</span></span><br/>  | <dl> <span data-ttu-id="d51ad-123"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="d51ad-123"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="d51ad-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="d51ad-124">Library</span></span><br/> | <dl> <span data-ttu-id="d51ad-125"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d51ad-125"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d51ad-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d51ad-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d51ad-127">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="d51ad-127">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
