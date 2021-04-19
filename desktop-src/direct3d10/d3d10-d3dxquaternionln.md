---
description: Calcola il logaritmo naturale.
ms.assetid: 576cf676-bb42-45ec-8e45-4612a7cdb167
title: Funzione D3DXQuaternionLn (D3DX10Math. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 07b081e0e2063d18ab8f2bb010e2b436c38df097
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323203"
---
# <a name="d3dxquaternionln-function-d3dx10mathh"></a><span data-ttu-id="cd66d-103">Funzione D3DXQuaternionLn (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="cd66d-103">D3DXQuaternionLn function (D3DX10Math.h)</span></span>

<span data-ttu-id="cd66d-104">Calcola il logaritmo naturale.</span><span class="sxs-lookup"><span data-stu-id="cd66d-104">Calculates the natural logarithm.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd66d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cd66d-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionLn(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="cd66d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="cd66d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd66d-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="cd66d-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="cd66d-108">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="cd66d-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="cd66d-109">Puntatore a [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="cd66d-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="cd66d-110">*PQ* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cd66d-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd66d-111">Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="cd66d-111">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="cd66d-112">Puntatore alla struttura D3DXQUATERNION di origine.</span><span class="sxs-lookup"><span data-stu-id="cd66d-112">Pointer to the source D3DXQUATERNION structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd66d-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cd66d-113">Return value</span></span>

<span data-ttu-id="cd66d-114">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="cd66d-114">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="cd66d-115">Puntatore a una struttura D3DXQUATERNION che rappresenta il logaritmo naturale.</span><span class="sxs-lookup"><span data-stu-id="cd66d-115">Pointer to a D3DXQUATERNION structure that is the natural logarithm.</span></span>

## <a name="remarks"></a><span data-ttu-id="cd66d-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="cd66d-116">Remarks</span></span>

<span data-ttu-id="cd66d-117">La funzione D3DXQuaternionLn funziona solo per i quaternioni dell'unità.</span><span class="sxs-lookup"><span data-stu-id="cd66d-117">The D3DXQuaternionLn function works only for unit quaternions.</span></span>


```
A unit quaternion, is defined by:
Q == (cos(theta), sin(theta) * v) where |v| = 1
The natural logarithm of Q is, ln(Q) = (0, theta * v)
```



<span data-ttu-id="cd66d-118">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro broncio.</span><span class="sxs-lookup"><span data-stu-id="cd66d-118">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="cd66d-119">In questo modo, la funzione D3DXQuaternionLn può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="cd66d-119">In this way, the D3DXQuaternionLn function can be used as a parameter for another function.</span></span>

<span data-ttu-id="cd66d-120">Usare [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) per qualsiasi input quaternione non ancora normalizzato.</span><span class="sxs-lookup"><span data-stu-id="cd66d-120">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd66d-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cd66d-121">Requirements</span></span>



| <span data-ttu-id="cd66d-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd66d-122">Requirement</span></span> | <span data-ttu-id="cd66d-123">Valore</span><span class="sxs-lookup"><span data-stu-id="cd66d-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cd66d-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cd66d-124">Header</span></span><br/>  | <dl> <span data-ttu-id="cd66d-125"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="cd66d-125"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="cd66d-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="cd66d-126">Library</span></span><br/> | <dl> <span data-ttu-id="cd66d-127"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cd66d-127"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="cd66d-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cd66d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd66d-129">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="cd66d-129">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
