---
description: Crea il valore del colore negativo di un valore di colore.
ms.assetid: 74143126-93f8-49fa-abe3-fd730b644d87
title: Funzione D3DXColorNegative (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXColorNegative
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a6d4d8559e64580897aec5261c450dc739496e75
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322881"
---
# <a name="d3dxcolornegative-function"></a><span data-ttu-id="6a23b-103">D3DXColorNegative (funzione)</span><span class="sxs-lookup"><span data-stu-id="6a23b-103">D3DXColorNegative function</span></span>

<span data-ttu-id="6a23b-104">Crea il valore del colore negativo di un valore di colore.</span><span class="sxs-lookup"><span data-stu-id="6a23b-104">Creates the negative color value of a color value.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a23b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6a23b-105">Syntax</span></span>


```C++
D3DXCOLOR* D3DXColorNegative(
  _Inout_       D3DXCOLOR *pOut,
  _In_    const D3DXCOLOR *pC
);
```



## <a name="parameters"></a><span data-ttu-id="6a23b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6a23b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a23b-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="6a23b-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6a23b-108">Tipo: **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="6a23b-108">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="6a23b-109">Puntatore a una struttura [**D3DXCOLOR**](d3dxcolor.md) che è il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="6a23b-109">Pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="6a23b-110">*computer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6a23b-110">*pC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a23b-111">Tipo: **const [**D3DXCOLOR**](d3dxcolor.md) \***</span><span class="sxs-lookup"><span data-stu-id="6a23b-111">Type: **const [**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="6a23b-112">Puntatore a una struttura [**D3DXCOLOR**](d3dxcolor.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="6a23b-112">Pointer to a source [**D3DXCOLOR**](d3dxcolor.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a23b-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6a23b-113">Return value</span></span>

<span data-ttu-id="6a23b-114">Tipo: **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="6a23b-114">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="6a23b-115">Questa funzione restituisce un puntatore a una struttura [**D3DXCOLOR**](d3dxcolor.md) che corrisponde al valore di colore negativo del valore del colore.</span><span class="sxs-lookup"><span data-stu-id="6a23b-115">This function returns a pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the negative color value of the color value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a23b-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="6a23b-116">Remarks</span></span>

<span data-ttu-id="6a23b-117">Il canale alfa di input viene copiato, non modificato, nel canale alfa di output.</span><span class="sxs-lookup"><span data-stu-id="6a23b-117">The input alpha channel is copied, unmodified, to the output alpha channel.</span></span>

<span data-ttu-id="6a23b-118">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro broncio.</span><span class="sxs-lookup"><span data-stu-id="6a23b-118">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="6a23b-119">In questo modo, la funzione **D3DXColorNegative** può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="6a23b-119">In this way, the **D3DXColorNegative** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="6a23b-120">Questa funzione restituisce il valore di colore negativo sottraendo 1,0 dai componenti colore della struttura [**D3DXCOLOR**](d3dxcolor.md) , come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="6a23b-120">This function returns the negative color value by subtracting 1.0 from the color components of the [**D3DXCOLOR**](d3dxcolor.md) structure, as shown in the following example.</span></span>


```
pOut->r = 1.0f - pC->r;
```



## <a name="requirements"></a><span data-ttu-id="6a23b-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6a23b-121">Requirements</span></span>



| <span data-ttu-id="6a23b-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a23b-122">Requirement</span></span> | <span data-ttu-id="6a23b-123">Valore</span><span class="sxs-lookup"><span data-stu-id="6a23b-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6a23b-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6a23b-124">Header</span></span><br/>  | <dl> <span data-ttu-id="6a23b-125"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="6a23b-125"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="6a23b-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="6a23b-126">Library</span></span><br/> | <dl> <span data-ttu-id="6a23b-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6a23b-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6a23b-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6a23b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a23b-129">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="6a23b-129">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="6a23b-130">**D3DXColorLerp**</span><span class="sxs-lookup"><span data-stu-id="6a23b-130">**D3DXColorLerp**</span></span>](d3dxcolorlerp.md)
</dt> <dt>

[<span data-ttu-id="6a23b-131">**D3DXColorModulate**</span><span class="sxs-lookup"><span data-stu-id="6a23b-131">**D3DXColorModulate**</span></span>](d3dxcolormodulate.md)
</dt> <dt>

[<span data-ttu-id="6a23b-132">**D3DXColorScale**</span><span class="sxs-lookup"><span data-stu-id="6a23b-132">**D3DXColorScale**</span></span>](d3dxcolorscale.md)
</dt> </dl>

 

 




