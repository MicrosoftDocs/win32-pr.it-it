---
description: Restituisce il coniugato di un quaternione.
ms.assetid: f690fdd8-7805-4fc1-9064-4f249d5f7c4f
title: Funzione D3DXQuaternionConjugate (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionConjugate
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: bbf288724dbdede9d98ec4ee21afd1bb57dd7a49
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235104"
---
# <a name="d3dxquaternionconjugate-function"></a><span data-ttu-id="5c1c5-103">D3DXQuaternionConjugate (funzione)</span><span class="sxs-lookup"><span data-stu-id="5c1c5-103">D3DXQuaternionConjugate function</span></span>

<span data-ttu-id="5c1c5-104">Restituisce il coniugato di un quaternione.</span><span class="sxs-lookup"><span data-stu-id="5c1c5-104">Returns the conjugate of a quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c1c5-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5c1c5-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionConjugate(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="5c1c5-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5c1c5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c1c5-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="5c1c5-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5c1c5-108">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="5c1c5-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="5c1c5-109">Puntatore alla struttura [**D3DXQUATERNION**](d3dxquaternion.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="5c1c5-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="5c1c5-110">*PQ* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5c1c5-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c1c5-111">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="5c1c5-111">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="5c1c5-112">Puntatore alla struttura [**D3DXQUATERNION**](d3dxquaternion.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="5c1c5-112">Pointer to the source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c1c5-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5c1c5-113">Return value</span></span>

<span data-ttu-id="5c1c5-114">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="5c1c5-114">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="5c1c5-115">Puntatore a una struttura [**D3DXQUATERNION**](d3dxquaternion.md) che rappresenta il coniugato del quaternione.</span><span class="sxs-lookup"><span data-stu-id="5c1c5-115">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the conjugate of the quaternion.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c1c5-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="5c1c5-116">Remarks</span></span>

<span data-ttu-id="5c1c5-117">Dato un quaternione (x, y, z, w), la funzione **D3DXQuaternionConjugate** restituirà il quaternione (-x,-y,-z, w).</span><span class="sxs-lookup"><span data-stu-id="5c1c5-117">Given a quaternion (x, y, z, w), the **D3DXQuaternionConjugate** function will return the quaternion (-x, -y, -z, w).</span></span>

<span data-ttu-id="5c1c5-118">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro *broncio* .</span><span class="sxs-lookup"><span data-stu-id="5c1c5-118">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="5c1c5-119">In questo modo, la funzione **D3DXQuaternionConjugate** può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="5c1c5-119">In this way, the **D3DXQuaternionConjugate** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="5c1c5-120">Usare [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) per qualsiasi input quaternione non ancora normalizzato.</span><span class="sxs-lookup"><span data-stu-id="5c1c5-120">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c1c5-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5c1c5-121">Requirements</span></span>



| <span data-ttu-id="5c1c5-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c1c5-122">Requirement</span></span> | <span data-ttu-id="5c1c5-123">Valore</span><span class="sxs-lookup"><span data-stu-id="5c1c5-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5c1c5-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5c1c5-124">Header</span></span><br/>  | <dl> <span data-ttu-id="5c1c5-125"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c1c5-125"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="5c1c5-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="5c1c5-126">Library</span></span><br/> | <dl> <span data-ttu-id="5c1c5-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5c1c5-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5c1c5-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5c1c5-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c1c5-129">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="5c1c5-129">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="5c1c5-130">**D3DXQuaternionInverse**</span><span class="sxs-lookup"><span data-stu-id="5c1c5-130">**D3DXQuaternionInverse**</span></span>](d3dxquaternioninverse.md)
</dt> </dl>

 

 




