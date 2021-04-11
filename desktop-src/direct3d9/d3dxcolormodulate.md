---
description: Combina due colori.
ms.assetid: deff70c7-2359-48b2-ab40-8c418acf5a07
title: Funzione D3DXColorModulate (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXColorModulate
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: cf9b202da786f6ec87ceca9816c2a4fc86776577
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235090"
---
# <a name="d3dxcolormodulate-function"></a><span data-ttu-id="b5000-103">D3DXColorModulate (funzione)</span><span class="sxs-lookup"><span data-stu-id="b5000-103">D3DXColorModulate function</span></span>

<span data-ttu-id="b5000-104">Combina due colori.</span><span class="sxs-lookup"><span data-stu-id="b5000-104">Blends two colors.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5000-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b5000-105">Syntax</span></span>


```C++
D3DXCOLOR* D3DXColorModulate(
  _Inout_       D3DXCOLOR *pOut,
  _In_    const D3DXCOLOR *pC1,
  _In_    const D3DXCOLOR *pC2
);
```



## <a name="parameters"></a><span data-ttu-id="b5000-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b5000-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5000-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="b5000-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b5000-108">Tipo: **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="b5000-108">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="b5000-109">Puntatore a una struttura [**D3DXCOLOR**](d3dxcolor.md) che è il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="b5000-109">Pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="b5000-110">*pC1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b5000-110">*pC1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5000-111">Tipo: **const [**D3DXCOLOR**](d3dxcolor.md) \***</span><span class="sxs-lookup"><span data-stu-id="b5000-111">Type: **const [**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="b5000-112">Puntatore a una struttura [**D3DXCOLOR**](d3dxcolor.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="b5000-112">Pointer to a source [**D3DXCOLOR**](d3dxcolor.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="b5000-113">*pC2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b5000-113">*pC2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5000-114">Tipo: **const [**D3DXCOLOR**](d3dxcolor.md) \***</span><span class="sxs-lookup"><span data-stu-id="b5000-114">Type: **const [**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="b5000-115">Puntatore a una struttura [**D3DXCOLOR**](d3dxcolor.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="b5000-115">Pointer to a source [**D3DXCOLOR**](d3dxcolor.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5000-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b5000-116">Return value</span></span>

<span data-ttu-id="b5000-117">Tipo: **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="b5000-117">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="b5000-118">Questa funzione restituisce un puntatore a una struttura [**D3DXCOLOR**](d3dxcolor.md) che è il risultato dell'operazione di fusione.</span><span class="sxs-lookup"><span data-stu-id="b5000-118">This function returns a pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the result of the blending operation.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5000-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="b5000-119">Remarks</span></span>

<span data-ttu-id="b5000-120">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro broncio.</span><span class="sxs-lookup"><span data-stu-id="b5000-120">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="b5000-121">In questo modo, la funzione **D3DXColorModulate** può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="b5000-121">In this way, the **D3DXColorModulate** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="b5000-122">Questa funzione unisce due colori moltiplicando i componenti di colore corrispondenti, come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="b5000-122">This function blends together two colors by multiplying matching color components, as shown in the following example.</span></span>


```
pOut->r = pC1->r * pC2->r;
```



## <a name="requirements"></a><span data-ttu-id="b5000-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b5000-123">Requirements</span></span>



| <span data-ttu-id="b5000-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5000-124">Requirement</span></span> | <span data-ttu-id="b5000-125">Valore</span><span class="sxs-lookup"><span data-stu-id="b5000-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b5000-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b5000-126">Header</span></span><br/>  | <dl> <span data-ttu-id="b5000-127"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5000-127"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="b5000-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="b5000-128">Library</span></span><br/> | <dl> <span data-ttu-id="b5000-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b5000-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b5000-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b5000-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5000-131">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="b5000-131">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="b5000-132">**D3DXColorLerp**</span><span class="sxs-lookup"><span data-stu-id="b5000-132">**D3DXColorLerp**</span></span>](d3dxcolorlerp.md)
</dt> <dt>

[<span data-ttu-id="b5000-133">**D3DXColorNegative**</span><span class="sxs-lookup"><span data-stu-id="b5000-133">**D3DXColorNegative**</span></span>](d3dxcolornegative.md)
</dt> <dt>

[<span data-ttu-id="b5000-134">**D3DXColorScale**</span><span class="sxs-lookup"><span data-stu-id="b5000-134">**D3DXColorScale**</span></span>](d3dxcolorscale.md)
</dt> </dl>

 

 




