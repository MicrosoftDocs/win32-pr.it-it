---
description: Ridimensiona un valore di colore.
ms.assetid: 35e8adee-7ce5-4db5-8276-f0e408748e78
title: Funzione D3DXColorScale (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXColorScale
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 74020f302a26162df1e42cb4c9f020af3f64e59c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323012"
---
# <a name="d3dxcolorscale-function"></a><span data-ttu-id="e2ed9-103">D3DXColorScale (funzione)</span><span class="sxs-lookup"><span data-stu-id="e2ed9-103">D3DXColorScale function</span></span>

<span data-ttu-id="e2ed9-104">Ridimensiona un valore di colore.</span><span class="sxs-lookup"><span data-stu-id="e2ed9-104">Scales a color value.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2ed9-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e2ed9-105">Syntax</span></span>


```C++
D3DXCOLOR* D3DXColorScale(
  _Inout_       D3DXCOLOR *pOut,
  _In_    const D3DXCOLOR *pC,
  _In_          FLOAT     s
);
```



## <a name="parameters"></a><span data-ttu-id="e2ed9-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e2ed9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2ed9-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="e2ed9-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e2ed9-108">Tipo: **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="e2ed9-108">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="e2ed9-109">Puntatore a una struttura [**D3DXCOLOR**](d3dxcolor.md) che è il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="e2ed9-109">Pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="e2ed9-110">*computer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e2ed9-110">*pC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2ed9-111">Tipo: **const [**D3DXCOLOR**](d3dxcolor.md) \***</span><span class="sxs-lookup"><span data-stu-id="e2ed9-111">Type: **const [**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="e2ed9-112">Puntatore a una struttura [**D3DXCOLOR**](d3dxcolor.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="e2ed9-112">Pointer to a source [**D3DXCOLOR**](d3dxcolor.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="e2ed9-113">*s* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e2ed9-113">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2ed9-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e2ed9-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e2ed9-115">Fattore di scala.</span><span class="sxs-lookup"><span data-stu-id="e2ed9-115">Scale factor.</span></span> <span data-ttu-id="e2ed9-116">Ridimensiona il colore, considerandolo come un vettore 4D.</span><span class="sxs-lookup"><span data-stu-id="e2ed9-116">It scales the color, treating it like a 4D vector.</span></span> <span data-ttu-id="e2ed9-117">Non sono previsti limiti per il valore di s.</span><span class="sxs-lookup"><span data-stu-id="e2ed9-117">There are no limits on the value of s.</span></span> <span data-ttu-id="e2ed9-118">Se s è 1, il colore risultante è quello originale.</span><span class="sxs-lookup"><span data-stu-id="e2ed9-118">If s is 1, the resulting color is the original color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2ed9-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e2ed9-119">Return value</span></span>

<span data-ttu-id="e2ed9-120">Tipo: **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="e2ed9-120">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="e2ed9-121">Questa funzione restituisce un puntatore a una struttura [**D3DXCOLOR**](d3dxcolor.md) che corrisponde al valore di colore ridimensionato.</span><span class="sxs-lookup"><span data-stu-id="e2ed9-121">This function returns a pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the scaled color value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2ed9-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="e2ed9-122">Remarks</span></span>

<span data-ttu-id="e2ed9-123">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro broncio.</span><span class="sxs-lookup"><span data-stu-id="e2ed9-123">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="e2ed9-124">In questo modo, la funzione **D3DXColorScale** può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="e2ed9-124">In this way, the **D3DXColorScale** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="e2ed9-125">Questa funzione calcola il valore del colore scalato moltiplicando i componenti del colore della struttura [**D3DXCOLOR**](d3dxcolor.md) in base al fattore di scala specificato, come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="e2ed9-125">This function computes the scaled color value by multiplying the color components of the [**D3DXCOLOR**](d3dxcolor.md) structure by the specified scale factor, as shown in the following example.</span></span>


```
pOut->r = pC->r * s;
```



## <a name="requirements"></a><span data-ttu-id="e2ed9-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e2ed9-126">Requirements</span></span>



| <span data-ttu-id="e2ed9-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2ed9-127">Requirement</span></span> | <span data-ttu-id="e2ed9-128">Valore</span><span class="sxs-lookup"><span data-stu-id="e2ed9-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e2ed9-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e2ed9-129">Header</span></span><br/>  | <dl> <span data-ttu-id="e2ed9-130"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2ed9-130"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="e2ed9-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="e2ed9-131">Library</span></span><br/> | <dl> <span data-ttu-id="e2ed9-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e2ed9-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e2ed9-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e2ed9-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2ed9-134">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="e2ed9-134">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="e2ed9-135">**D3DXColorLerp**</span><span class="sxs-lookup"><span data-stu-id="e2ed9-135">**D3DXColorLerp**</span></span>](d3dxcolorlerp.md)
</dt> <dt>

[<span data-ttu-id="e2ed9-136">**D3DXColorModulate**</span><span class="sxs-lookup"><span data-stu-id="e2ed9-136">**D3DXColorModulate**</span></span>](d3dxcolormodulate.md)
</dt> <dt>

[<span data-ttu-id="e2ed9-137">**D3DXColorNegative**</span><span class="sxs-lookup"><span data-stu-id="e2ed9-137">**D3DXColorNegative**</span></span>](d3dxcolornegative.md)
</dt> </dl>

 

 
