---
description: 'Funzione D3DXQuaternionInverse (D3dx9math.h): coniuga e rinormalizza un quaternione.'
ms.assetid: 25407a60-f7c0-4063-8d1d-2d6d03bdb217
title: Funzione D3DXQuaternionInverse (D3dx9math.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6ebb2520efa3c7c78d98fd8b90ec1ba9615e9927
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094069"
---
# <a name="d3dxquaternioninverse-function-d3dx9mathh"></a><span data-ttu-id="aa986-103">Funzione D3DXQuaternionInverse (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="aa986-103">D3DXQuaternionInverse function (D3dx9math.h)</span></span>

<span data-ttu-id="aa986-104">Coniuga e rinormalizza un quaternione.</span><span class="sxs-lookup"><span data-stu-id="aa986-104">Conjugates and renormalizes a quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa986-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="aa986-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionInverse(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="aa986-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="aa986-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa986-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="aa986-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="aa986-108">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="aa986-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="aa986-109">Puntatore alla [**struttura D3DXQUATERNION**](d3dxquaternion.md) che è il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="aa986-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="aa986-110">*pQ* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="aa986-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa986-111">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="aa986-111">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="aa986-112">Puntatore alla struttura [**D3DXQUATERNION di**](d3dxquaternion.md) origine.</span><span class="sxs-lookup"><span data-stu-id="aa986-112">Pointer to the source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa986-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="aa986-113">Return value</span></span>

<span data-ttu-id="aa986-114">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="aa986-114">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="aa986-115">Puntatore a [**una struttura D3DXQUATERNION**](d3dxquaternion.md) che rappresenta il quaternione inverso del quaternione.</span><span class="sxs-lookup"><span data-stu-id="aa986-115">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the inverse quaternion of the quaternion.</span></span>

## <a name="remarks"></a><span data-ttu-id="aa986-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="aa986-116">Remarks</span></span>


```
A unit quaternion, is defined by:
Q == (cos(theta), sin(theta) * v) where |v| = 1
The natural logarithm of Q is, ln(Q) = (0, theta * v)
```



<span data-ttu-id="aa986-117">Il valore restituito per questa funzione è lo stesso valore restituito nel *parametro pOut.*</span><span class="sxs-lookup"><span data-stu-id="aa986-117">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="aa986-118">In questo modo, la **funzione D3DXQuaternionInverse** può essere usata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="aa986-118">In this way, the **D3DXQuaternionInverse** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="aa986-119">Usare [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) per qualsiasi input quaternione non ancora normalizzato.</span><span class="sxs-lookup"><span data-stu-id="aa986-119">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa986-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aa986-120">Requirements</span></span>



| <span data-ttu-id="aa986-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa986-121">Requirement</span></span> | <span data-ttu-id="aa986-122">Valore</span><span class="sxs-lookup"><span data-stu-id="aa986-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="aa986-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="aa986-123">Header</span></span><br/>  | <dl> <span data-ttu-id="aa986-124"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="aa986-124"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="aa986-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="aa986-125">Library</span></span><br/> | <dl> <span data-ttu-id="aa986-126"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="aa986-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="aa986-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="aa986-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa986-128">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="aa986-128">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="aa986-129">**D3DXQuaternionConjugate**</span><span class="sxs-lookup"><span data-stu-id="aa986-129">**D3DXQuaternionConjugate**</span></span>](d3dxquaternionconjugate.md)
</dt> <dt>

[<span data-ttu-id="aa986-130">**D3DXQuaternionNormalize**</span><span class="sxs-lookup"><span data-stu-id="aa986-130">**D3DXQuaternionNormalize**</span></span>](d3dxquaternionnormalize.md)
</dt> </dl>

 

 




