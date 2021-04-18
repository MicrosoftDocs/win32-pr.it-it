---
description: Normalizza i coefficienti del piano in modo che la normale del piano abbia la lunghezza dell'unità.
ms.assetid: 9c595986-e1f8-4153-ba23-1fa6e583a050
title: Funzione D3DXPlaneNormalize (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneNormalize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0f0c87028d3b37f785005725e7510f689cf56d61
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322098"
---
# <a name="d3dxplanenormalize-function-d3dx9mathh"></a><span data-ttu-id="9e0d1-103">Funzione D3DXPlaneNormalize (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="9e0d1-103">D3DXPlaneNormalize function (D3dx9math.h)</span></span>

<span data-ttu-id="9e0d1-104">Normalizza i coefficienti del piano in modo che la normale del piano abbia la lunghezza dell'unità.</span><span class="sxs-lookup"><span data-stu-id="9e0d1-104">Normalizes the plane coefficients so that the plane normal has unit length.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e0d1-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9e0d1-105">Syntax</span></span>


```C++
D3DXPLANE* D3DXPlaneNormalize(
  _Inout_       D3DXPLANE *pOut,
  _In_    const D3DXPLANE *pP
);
```



## <a name="parameters"></a><span data-ttu-id="9e0d1-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9e0d1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e0d1-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="9e0d1-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="9e0d1-108">Tipo: **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="9e0d1-108">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="9e0d1-109">Puntatore alla struttura [**D3DXPLANE**](d3dxplane.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="9e0d1-109">Pointer to the [**D3DXPLANE**](d3dxplane.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="9e0d1-110">*PP* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9e0d1-110">*pP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e0d1-111">Tipo: **const [**D3DXPLANE**](d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="9e0d1-111">Type: **const [**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="9e0d1-112">Puntatore alla struttura [**D3DXPLANE**](d3dxplane.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="9e0d1-112">Pointer to the source [**D3DXPLANE**](d3dxplane.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e0d1-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9e0d1-113">Return value</span></span>

<span data-ttu-id="9e0d1-114">Tipo: **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="9e0d1-114">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="9e0d1-115">Puntatore a una struttura [**D3DXPLANE**](d3dxplane.md) che rappresenta la normale del piano.</span><span class="sxs-lookup"><span data-stu-id="9e0d1-115">Pointer to a [**D3DXPLANE**](d3dxplane.md) structure that represents the normal of the plane.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e0d1-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="9e0d1-116">Remarks</span></span>

<span data-ttu-id="9e0d1-117">Questa funzione normalizza un piano in modo che \| a, b, c \| = = 1.</span><span class="sxs-lookup"><span data-stu-id="9e0d1-117">This function normalizes a plane so that \|a,b,c\| == 1.</span></span>

<span data-ttu-id="9e0d1-118">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro *broncio* .</span><span class="sxs-lookup"><span data-stu-id="9e0d1-118">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="9e0d1-119">In questo modo, questa funzione può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="9e0d1-119">In this way, this function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e0d1-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9e0d1-120">Requirements</span></span>



| <span data-ttu-id="9e0d1-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e0d1-121">Requirement</span></span> | <span data-ttu-id="9e0d1-122">Valore</span><span class="sxs-lookup"><span data-stu-id="9e0d1-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9e0d1-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9e0d1-123">Header</span></span><br/>  | <dl> <span data-ttu-id="9e0d1-124"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e0d1-124"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="9e0d1-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="9e0d1-125">Library</span></span><br/> | <dl> <span data-ttu-id="9e0d1-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9e0d1-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9e0d1-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9e0d1-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e0d1-128">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="9e0d1-128">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




