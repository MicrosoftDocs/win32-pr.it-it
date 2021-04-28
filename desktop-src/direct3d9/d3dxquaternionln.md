---
description: 'Funzione D3DXQuaternionLn (D3dx9math.h): calcola il logaritmo naturale.'
ms.assetid: 73ca7d13-1e20-48fc-b0ed-0d3127d094a7
title: Funzione D3DXQuaternionLn (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionLn
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d1a529c1c6ca4d7f81bf4d41fcdb4a7c7179874b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094059"
---
# <a name="d3dxquaternionln-function-d3dx9mathh"></a><span data-ttu-id="4e00e-103">Funzione D3DXQuaternionLn (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="4e00e-103">D3DXQuaternionLn function (D3dx9math.h)</span></span>

<span data-ttu-id="4e00e-104">Calcola il logaritmo naturale.</span><span class="sxs-lookup"><span data-stu-id="4e00e-104">Calculates the natural logarithm.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e00e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4e00e-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionLn(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="4e00e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4e00e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e00e-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="4e00e-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4e00e-108">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="4e00e-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="4e00e-109">Puntatore alla [**struttura D3DXQUATERNION**](d3dxquaternion.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="4e00e-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="4e00e-110">*pQ* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="4e00e-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e00e-111">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="4e00e-111">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="4e00e-112">Puntatore alla struttura [**D3DXQUATERNION di**](d3dxquaternion.md) origine.</span><span class="sxs-lookup"><span data-stu-id="4e00e-112">Pointer to the source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e00e-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4e00e-113">Return value</span></span>

<span data-ttu-id="4e00e-114">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="4e00e-114">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="4e00e-115">Puntatore a [**una struttura D3DXQUATERNION**](d3dxquaternion.md) che rappresenta il logaritmo naturale.</span><span class="sxs-lookup"><span data-stu-id="4e00e-115">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the natural logarithm.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e00e-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="4e00e-116">Remarks</span></span>

<span data-ttu-id="4e00e-117">La **funzione D3DXQuaternionLn** funziona solo per quaternioni unità.</span><span class="sxs-lookup"><span data-stu-id="4e00e-117">The **D3DXQuaternionLn** function works only for unit quaternions.</span></span>


```
A unit quaternion, is defined by:
Q == (cos(theta), sin(theta) * v) where |v| = 1
The natural logarithm of Q is, ln(Q) = (0, theta * v)
```



<span data-ttu-id="4e00e-118">Il valore restituito per questa funzione è lo stesso valore restituito nel *parametro pOut.*</span><span class="sxs-lookup"><span data-stu-id="4e00e-118">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="4e00e-119">In questo modo, la **funzione D3DXQuaternionLn** può essere usata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="4e00e-119">In this way, the **D3DXQuaternionLn** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="4e00e-120">Usare [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) per qualsiasi input quaternione non ancora normalizzato.</span><span class="sxs-lookup"><span data-stu-id="4e00e-120">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e00e-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4e00e-121">Requirements</span></span>



| <span data-ttu-id="4e00e-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e00e-122">Requirement</span></span> | <span data-ttu-id="4e00e-123">Valore</span><span class="sxs-lookup"><span data-stu-id="4e00e-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4e00e-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4e00e-124">Header</span></span><br/>  | <dl> <span data-ttu-id="4e00e-125"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="4e00e-125"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="4e00e-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="4e00e-126">Library</span></span><br/> | <dl> <span data-ttu-id="4e00e-127"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="4e00e-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4e00e-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4e00e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e00e-129">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="4e00e-129">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="4e00e-130">**D3DXQuaternionExp**</span><span class="sxs-lookup"><span data-stu-id="4e00e-130">**D3DXQuaternionExp**</span></span>](d3dxquaternionexp.md)
</dt> <dt>

[<span data-ttu-id="4e00e-131">**D3DXQuaternionSquad**</span><span class="sxs-lookup"><span data-stu-id="4e00e-131">**D3DXQuaternionSquad**</span></span>](d3dxquaternionsquad.md)
</dt> </dl>

 

 




