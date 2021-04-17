---
description: Calcola il logaritmo naturale.
ms.assetid: 73ca7d13-1e20-48fc-b0ed-0d3127d094a7
title: Funzione D3DXQuaternionLn (D3dx9math. h)
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
ms.openlocfilehash: b51fcc77da29216acd2bfc1c011a063014da5d69
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104531015"
---
# <a name="d3dxquaternionln-function-d3dx9mathh"></a><span data-ttu-id="ded5f-103">Funzione D3DXQuaternionLn (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="ded5f-103">D3DXQuaternionLn function (D3dx9math.h)</span></span>

<span data-ttu-id="ded5f-104">Calcola il logaritmo naturale.</span><span class="sxs-lookup"><span data-stu-id="ded5f-104">Calculates the natural logarithm.</span></span>

## <a name="syntax"></a><span data-ttu-id="ded5f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ded5f-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionLn(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="ded5f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ded5f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ded5f-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="ded5f-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ded5f-108">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="ded5f-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="ded5f-109">Puntatore alla struttura [**D3DXQUATERNION**](d3dxquaternion.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="ded5f-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="ded5f-110">*PQ* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ded5f-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ded5f-111">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="ded5f-111">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="ded5f-112">Puntatore alla struttura [**D3DXQUATERNION**](d3dxquaternion.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="ded5f-112">Pointer to the source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ded5f-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ded5f-113">Return value</span></span>

<span data-ttu-id="ded5f-114">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="ded5f-114">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="ded5f-115">Puntatore a una struttura [**D3DXQUATERNION**](d3dxquaternion.md) che rappresenta il logaritmo naturale.</span><span class="sxs-lookup"><span data-stu-id="ded5f-115">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the natural logarithm.</span></span>

## <a name="remarks"></a><span data-ttu-id="ded5f-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="ded5f-116">Remarks</span></span>

<span data-ttu-id="ded5f-117">La funzione **D3DXQuaternionLn** funziona solo per i quaternioni dell'unità.</span><span class="sxs-lookup"><span data-stu-id="ded5f-117">The **D3DXQuaternionLn** function works only for unit quaternions.</span></span>


```
A unit quaternion, is defined by:
Q == (cos(theta), sin(theta) * v) where |v| = 1
The natural logarithm of Q is, ln(Q) = (0, theta * v)
```



<span data-ttu-id="ded5f-118">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro *broncio* .</span><span class="sxs-lookup"><span data-stu-id="ded5f-118">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="ded5f-119">In questo modo, la funzione **D3DXQuaternionLn** può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="ded5f-119">In this way, the **D3DXQuaternionLn** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="ded5f-120">Usare [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) per qualsiasi input quaternione non ancora normalizzato.</span><span class="sxs-lookup"><span data-stu-id="ded5f-120">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="ded5f-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ded5f-121">Requirements</span></span>



| <span data-ttu-id="ded5f-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="ded5f-122">Requirement</span></span> | <span data-ttu-id="ded5f-123">Valore</span><span class="sxs-lookup"><span data-stu-id="ded5f-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ded5f-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ded5f-124">Header</span></span><br/>  | <dl> <span data-ttu-id="ded5f-125"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="ded5f-125"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="ded5f-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="ded5f-126">Library</span></span><br/> | <dl> <span data-ttu-id="ded5f-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ded5f-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ded5f-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ded5f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ded5f-129">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="ded5f-129">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="ded5f-130">**D3DXQuaternionExp**</span><span class="sxs-lookup"><span data-stu-id="ded5f-130">**D3DXQuaternionExp**</span></span>](d3dxquaternionexp.md)
</dt> <dt>

[<span data-ttu-id="ded5f-131">**D3DXQuaternionSquad**</span><span class="sxs-lookup"><span data-stu-id="ded5f-131">**D3DXQuaternionSquad**</span></span>](d3dxquaternionsquad.md)
</dt> </dl>

 

 




