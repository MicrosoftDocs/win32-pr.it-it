---
description: Sottrae due valori di colore per creare un nuovo valore di colore.
ms.assetid: c21f8402-c1c2-4909-896f-2872ef518537
title: Funzione D3DXColorSubtract (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXColorSubtract
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 47f28ea3a3fb6d1556e699fed3820e228faf6604
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322878"
---
# <a name="d3dxcolorsubtract-function"></a><span data-ttu-id="391bd-103">D3DXColorSubtract (funzione)</span><span class="sxs-lookup"><span data-stu-id="391bd-103">D3DXColorSubtract function</span></span>

<span data-ttu-id="391bd-104">Sottrae due valori di colore per creare un nuovo valore di colore.</span><span class="sxs-lookup"><span data-stu-id="391bd-104">Subtracts two color values to create a new color value.</span></span>

## <a name="syntax"></a><span data-ttu-id="391bd-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="391bd-105">Syntax</span></span>


```C++
D3DXCOLOR* D3DXColorSubtract(
  _Inout_       D3DXCOLOR *pOut,
  _In_    const D3DXCOLOR *pC1,
  _In_    const D3DXCOLOR *pC2
);
```



## <a name="parameters"></a><span data-ttu-id="391bd-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="391bd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="391bd-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="391bd-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="391bd-108">Tipo: **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="391bd-108">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="391bd-109">Puntatore a una struttura [**D3DXCOLOR**](d3dxcolor.md) che è il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="391bd-109">Pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="391bd-110">*pC1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="391bd-110">*pC1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="391bd-111">Tipo: **const [**D3DXCOLOR**](d3dxcolor.md) \***</span><span class="sxs-lookup"><span data-stu-id="391bd-111">Type: **const [**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="391bd-112">Puntatore a una struttura [**D3DXCOLOR**](d3dxcolor.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="391bd-112">Pointer to a source [**D3DXCOLOR**](d3dxcolor.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="391bd-113">*pC2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="391bd-113">*pC2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="391bd-114">Tipo: **const [**D3DXCOLOR**](d3dxcolor.md) \***</span><span class="sxs-lookup"><span data-stu-id="391bd-114">Type: **const [**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="391bd-115">Puntatore a una struttura [**D3DXCOLOR**](d3dxcolor.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="391bd-115">Pointer to a source [**D3DXCOLOR**](d3dxcolor.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="391bd-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="391bd-116">Return value</span></span>

<span data-ttu-id="391bd-117">Tipo: **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="391bd-117">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="391bd-118">Questa funzione restituisce un puntatore a una struttura [**D3DXCOLOR**](d3dxcolor.md) che rappresenta la differenza tra due valori di colore.</span><span class="sxs-lookup"><span data-stu-id="391bd-118">This function returns a pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the difference between two color values.</span></span>

## <a name="remarks"></a><span data-ttu-id="391bd-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="391bd-119">Remarks</span></span>

<span data-ttu-id="391bd-120">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro broncio.</span><span class="sxs-lookup"><span data-stu-id="391bd-120">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="391bd-121">In questo modo, la funzione **D3DXColorSubtract** può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="391bd-121">In this way, the **D3DXColorSubtract** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="391bd-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="391bd-122">Requirements</span></span>



| <span data-ttu-id="391bd-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="391bd-123">Requirement</span></span> | <span data-ttu-id="391bd-124">Valore</span><span class="sxs-lookup"><span data-stu-id="391bd-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="391bd-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="391bd-125">Header</span></span><br/>  | <dl> <span data-ttu-id="391bd-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="391bd-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="391bd-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="391bd-127">Library</span></span><br/> | <dl> <span data-ttu-id="391bd-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="391bd-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="391bd-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="391bd-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="391bd-130">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="391bd-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="391bd-131">**D3DXColorAdd**</span><span class="sxs-lookup"><span data-stu-id="391bd-131">**D3DXColorAdd**</span></span>](d3dxcoloradd.md)
</dt> </dl>

 

 




