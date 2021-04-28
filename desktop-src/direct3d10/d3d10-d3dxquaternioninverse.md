---
description: 'Funzione D3DXQuaternionInverse (D3DX10Math.h): coniuga e rinormalizza un quaternione.'
ms.assetid: 8e1bba91-8895-43a2-805b-1368050f8e82
title: Funzione D3DXQuaternionInverse (D3DX10Math.h)
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
ms.openlocfilehash: 84816ac72841dcda0aef726535b7f5219d5467e4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103199"
---
# <a name="d3dxquaternioninverse-function-d3dx10mathh"></a><span data-ttu-id="8de33-103">Funzione D3DXQuaternionInverse (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="8de33-103">D3DXQuaternionInverse function (D3DX10Math.h)</span></span>

<span data-ttu-id="8de33-104">Coniuga e rinormalizza un quaternione.</span><span class="sxs-lookup"><span data-stu-id="8de33-104">Conjugates and renormalizes a quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="8de33-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8de33-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionInverse(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="8de33-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8de33-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8de33-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="8de33-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8de33-108">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="8de33-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="8de33-109">Puntatore [**all'oggetto D3DXQUATERNION**](d3d10-d3dxquaternion.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="8de33-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="8de33-110">*pQ* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="8de33-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8de33-111">Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="8de33-111">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="8de33-112">Puntatore alla struttura D3DXQUATERNION di origine.</span><span class="sxs-lookup"><span data-stu-id="8de33-112">Pointer to the source D3DXQUATERNION structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8de33-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8de33-113">Return value</span></span>

<span data-ttu-id="8de33-114">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="8de33-114">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="8de33-115">Puntatore a una struttura D3DXQUATERNION che rappresenta il quaternione inverso del quaternione.</span><span class="sxs-lookup"><span data-stu-id="8de33-115">Pointer to a D3DXQUATERNION structure that is the inverse quaternion of the quaternion.</span></span>

## <a name="remarks"></a><span data-ttu-id="8de33-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="8de33-116">Remarks</span></span>


```
A unit quaternion, is defined by:
Q == (cos(theta), sin(theta) * v) where |v| = 1
The natural logarithm of Q is, ln(Q) = (0, theta * v)
```



<span data-ttu-id="8de33-117">Il valore restituito per questa funzione è lo stesso valore restituito nel parametro pOut.</span><span class="sxs-lookup"><span data-stu-id="8de33-117">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="8de33-118">In questo modo, la funzione D3DXQuaternionInverse può essere usata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="8de33-118">In this way, the D3DXQuaternionInverse function can be used as a parameter for another function.</span></span>

<span data-ttu-id="8de33-119">Usare [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) per qualsiasi input quaternione non ancora normalizzato.</span><span class="sxs-lookup"><span data-stu-id="8de33-119">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="8de33-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8de33-120">Requirements</span></span>



| <span data-ttu-id="8de33-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="8de33-121">Requirement</span></span> | <span data-ttu-id="8de33-122">Valore</span><span class="sxs-lookup"><span data-stu-id="8de33-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8de33-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8de33-123">Header</span></span><br/>  | <dl> <span data-ttu-id="8de33-124"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="8de33-124"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="8de33-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="8de33-125">Library</span></span><br/> | <dl> <span data-ttu-id="8de33-126"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="8de33-126"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8de33-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8de33-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8de33-128">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="8de33-128">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
