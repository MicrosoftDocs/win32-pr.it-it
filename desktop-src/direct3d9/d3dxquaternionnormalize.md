---
description: Calcola un quaternione di lunghezza dell'unità.
ms.assetid: 31f56c2b-96b0-4110-a5b9-ce09983779b6
title: Funzione D3DXQuaternionNormalize (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d052d4dfc88feb2a00237392071f63d724070b3d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530889"
---
# <a name="d3dxquaternionnormalize-function-d3dx9mathh"></a><span data-ttu-id="113fe-103">Funzione D3DXQuaternionNormalize (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="113fe-103">D3DXQuaternionNormalize function (D3dx9math.h)</span></span>

<span data-ttu-id="113fe-104">Calcola un quaternione di lunghezza dell'unità.</span><span class="sxs-lookup"><span data-stu-id="113fe-104">Computes a unit length quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="113fe-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="113fe-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionNormalize(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="113fe-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="113fe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="113fe-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="113fe-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="113fe-108">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="113fe-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="113fe-109">Puntatore alla struttura [**D3DXQUATERNION**](d3dxquaternion.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="113fe-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="113fe-110">*PQ* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="113fe-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="113fe-111">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="113fe-111">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="113fe-112">Puntatore alla struttura [**D3DXQUATERNION**](d3dxquaternion.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="113fe-112">Pointer to the source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="113fe-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="113fe-113">Return value</span></span>

<span data-ttu-id="113fe-114">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="113fe-114">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="113fe-115">Puntatore a una struttura [**D3DXQUATERNION**](d3dxquaternion.md) che corrisponde al normale del quaternione.</span><span class="sxs-lookup"><span data-stu-id="113fe-115">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the normal of the quaternion.</span></span>

## <a name="remarks"></a><span data-ttu-id="113fe-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="113fe-116">Remarks</span></span>

<span data-ttu-id="113fe-117">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro *broncio* .</span><span class="sxs-lookup"><span data-stu-id="113fe-117">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="113fe-118">In questo modo, la funzione **D3DXQuaternionNormalize** può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="113fe-118">In this way, the **D3DXQuaternionNormalize** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="113fe-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="113fe-119">Requirements</span></span>



| <span data-ttu-id="113fe-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="113fe-120">Requirement</span></span> | <span data-ttu-id="113fe-121">Valore</span><span class="sxs-lookup"><span data-stu-id="113fe-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="113fe-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="113fe-122">Header</span></span><br/>  | <dl> <span data-ttu-id="113fe-123"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="113fe-123"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="113fe-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="113fe-124">Library</span></span><br/> | <dl> <span data-ttu-id="113fe-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="113fe-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="113fe-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="113fe-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="113fe-127">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="113fe-127">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="113fe-128">**D3DXQuaternionInverse**</span><span class="sxs-lookup"><span data-stu-id="113fe-128">**D3DXQuaternionInverse**</span></span>](d3dxquaternioninverse.md)
</dt> </dl>

 

 




