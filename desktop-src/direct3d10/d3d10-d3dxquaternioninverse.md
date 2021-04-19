---
description: Coniuga e rinormalizza un quaternione.
ms.assetid: 8e1bba91-8895-43a2-805b-1368050f8e82
title: Funzione D3DXQuaternionInverse (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionInverse
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: d58231c076dd44f77c7082a755d92ae997515ffb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323205"
---
# <a name="d3dxquaternioninverse-function-d3dx10mathh"></a><span data-ttu-id="7cc97-103">Funzione D3DXQuaternionInverse (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="7cc97-103">D3DXQuaternionInverse function (D3DX10Math.h)</span></span>

<span data-ttu-id="7cc97-104">Coniuga e rinormalizza un quaternione.</span><span class="sxs-lookup"><span data-stu-id="7cc97-104">Conjugates and renormalizes a quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="7cc97-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7cc97-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionInverse(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="7cc97-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7cc97-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7cc97-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="7cc97-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7cc97-108">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="7cc97-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="7cc97-109">Puntatore a [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="7cc97-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="7cc97-110">*PQ* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7cc97-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7cc97-111">Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="7cc97-111">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="7cc97-112">Puntatore alla struttura D3DXQUATERNION di origine.</span><span class="sxs-lookup"><span data-stu-id="7cc97-112">Pointer to the source D3DXQUATERNION structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7cc97-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7cc97-113">Return value</span></span>

<span data-ttu-id="7cc97-114">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="7cc97-114">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="7cc97-115">Puntatore a una struttura D3DXQUATERNION che rappresenta il quaternione inverso del quaternione.</span><span class="sxs-lookup"><span data-stu-id="7cc97-115">Pointer to a D3DXQUATERNION structure that is the inverse quaternion of the quaternion.</span></span>

## <a name="remarks"></a><span data-ttu-id="7cc97-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="7cc97-116">Remarks</span></span>


```
A unit quaternion, is defined by:
Q == (cos(theta), sin(theta) * v) where |v| = 1
The natural logarithm of Q is, ln(Q) = (0, theta * v)
```



<span data-ttu-id="7cc97-117">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro broncio.</span><span class="sxs-lookup"><span data-stu-id="7cc97-117">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="7cc97-118">In questo modo, la funzione D3DXQuaternionInverse può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="7cc97-118">In this way, the D3DXQuaternionInverse function can be used as a parameter for another function.</span></span>

<span data-ttu-id="7cc97-119">Usare [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) per qualsiasi input quaternione non ancora normalizzato.</span><span class="sxs-lookup"><span data-stu-id="7cc97-119">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="7cc97-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7cc97-120">Requirements</span></span>



| <span data-ttu-id="7cc97-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="7cc97-121">Requirement</span></span> | <span data-ttu-id="7cc97-122">Valore</span><span class="sxs-lookup"><span data-stu-id="7cc97-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7cc97-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7cc97-123">Header</span></span><br/>  | <dl> <span data-ttu-id="7cc97-124"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="7cc97-124"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="7cc97-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="7cc97-125">Library</span></span><br/> | <dl> <span data-ttu-id="7cc97-126"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7cc97-126"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7cc97-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7cc97-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7cc97-128">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="7cc97-128">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
