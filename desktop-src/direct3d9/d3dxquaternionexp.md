---
description: Calcola l'esponenziale.
ms.assetid: 648aeaf1-ead3-4b21-819f-cd2a70881a13
title: Funzione D3DXQuaternionExp (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionExp
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b9cb5765e01c4fbbc6ab3785363425262ee491ef
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322496"
---
# <a name="d3dxquaternionexp-function-d3dx9mathh"></a><span data-ttu-id="70071-103">Funzione D3DXQuaternionExp (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="70071-103">D3DXQuaternionExp function (D3dx9math.h)</span></span>

<span data-ttu-id="70071-104">Calcola l'esponenziale.</span><span class="sxs-lookup"><span data-stu-id="70071-104">Calculates the exponential.</span></span>

## <a name="syntax"></a><span data-ttu-id="70071-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="70071-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionExp(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="70071-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="70071-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70071-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="70071-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="70071-108">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="70071-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="70071-109">Puntatore alla struttura [**D3DXQUATERNION**](d3dxquaternion.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="70071-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="70071-110">*PQ* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="70071-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70071-111">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="70071-111">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="70071-112">Puntatore alla struttura [**D3DXQUATERNION**](d3dxquaternion.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="70071-112">Pointer to the source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70071-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="70071-113">Return value</span></span>

<span data-ttu-id="70071-114">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="70071-114">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="70071-115">Puntatore a una struttura [**D3DXQUATERNION**](d3dxquaternion.md) che rappresenta l'esponenziale.</span><span class="sxs-lookup"><span data-stu-id="70071-115">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the exponential.</span></span>

## <a name="remarks"></a><span data-ttu-id="70071-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="70071-116">Remarks</span></span>

<span data-ttu-id="70071-117">Questo metodo converte un quaternione puro in un quaternione di unità.</span><span class="sxs-lookup"><span data-stu-id="70071-117">This method converts a pure quaternion to a unit quaternion.</span></span> <span data-ttu-id="70071-118">**D3DXQuaternionExp** prevede un quaternione puro, in cui w viene ignorato nel calcolo (w = = 0).</span><span class="sxs-lookup"><span data-stu-id="70071-118">**D3DXQuaternionExp** expects a pure quaternion, where w is ignored in the calculation (w == 0).</span></span>


```
Given a pure quaternion defined by:
q = (0, theta * v); 
    
This method calculates the exponential result.
exp(Q) = (cos(theta), sin(theta) * v)
```



<span data-ttu-id="70071-119">dove v è la parte di vettore di un quaternione.</span><span class="sxs-lookup"><span data-stu-id="70071-119">where v is the vector portion of a quaternion.</span></span>

<span data-ttu-id="70071-120">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro *broncio* .</span><span class="sxs-lookup"><span data-stu-id="70071-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="70071-121">In questo modo, la funzione **D3DXQuaternionExp** può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="70071-121">In this way, the **D3DXQuaternionExp** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="70071-122">Il metodo [**D3DXQuaternionSquadSetup**](d3dxquaternionsquadsetup.md) può essere usato anche per impostare i punti di controllo di un quaternione.</span><span class="sxs-lookup"><span data-stu-id="70071-122">The [**D3DXQuaternionSquadSetup**](d3dxquaternionsquadsetup.md) method can also be used to set up the control points of a quaternion.</span></span>

<span data-ttu-id="70071-123">Usare [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) per qualsiasi input quaternione non ancora normalizzato.</span><span class="sxs-lookup"><span data-stu-id="70071-123">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="70071-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="70071-124">Requirements</span></span>



| <span data-ttu-id="70071-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="70071-125">Requirement</span></span> | <span data-ttu-id="70071-126">Valore</span><span class="sxs-lookup"><span data-stu-id="70071-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="70071-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="70071-127">Header</span></span><br/>  | <dl> <span data-ttu-id="70071-128"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="70071-128"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="70071-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="70071-129">Library</span></span><br/> | <dl> <span data-ttu-id="70071-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="70071-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="70071-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="70071-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70071-132">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="70071-132">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="70071-133">**D3DXQuaternionLn**</span><span class="sxs-lookup"><span data-stu-id="70071-133">**D3DXQuaternionLn**</span></span>](d3dxquaternionln.md)
</dt> <dt>

[<span data-ttu-id="70071-134">**D3DXQuaternionSquad**</span><span class="sxs-lookup"><span data-stu-id="70071-134">**D3DXQuaternionSquad**</span></span>](d3dxquaternionsquad.md)
</dt> </dl>

 

 




