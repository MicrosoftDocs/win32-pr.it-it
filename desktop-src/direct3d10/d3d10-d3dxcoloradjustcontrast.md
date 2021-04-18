---
description: Regola il valore di contrasto di un colore.
ms.assetid: c111d3c7-19c6-4a6b-af0d-a9e1bc0bb7d9
title: Funzione D3DXColorAdjustContrast (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXColorAdjustContrast
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 24586b2a8d2206d6818e00af9ea86e4c5e9758fa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323270"
---
# <a name="d3dxcoloradjustcontrast-function-d3dx10mathh"></a><span data-ttu-id="4d44d-103">Funzione D3DXColorAdjustContrast (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="4d44d-103">D3DXColorAdjustContrast function (D3DX10Math.h)</span></span>

<span data-ttu-id="4d44d-104">Regola il valore di contrasto di un colore.</span><span class="sxs-lookup"><span data-stu-id="4d44d-104">Adjusts the contrast value of a color.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d44d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4d44d-105">Syntax</span></span>


```C++
D3DXCOLOR* D3DXColorAdjustContrast(
  _In_       D3DXCOLOR *pOut,
  _In_ const D3DXCOLOR *pC,
  _In_       FLOAT     c
);
```



## <a name="parameters"></a><span data-ttu-id="4d44d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4d44d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d44d-107">*broncio* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4d44d-107">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d44d-108">Tipo: **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="4d44d-108">Type: **[**D3DXCOLOR**](../direct3d9/d3dxcolor.md)\***</span></span>

<span data-ttu-id="4d44d-109">\[in, out \] puntatore a un [**D3DXCOLOR**](d3d10-d3dxcolor.md) che è il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="4d44d-109">\[in, out\] Pointer to a [**D3DXCOLOR**](d3d10-d3dxcolor.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="4d44d-110">*computer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4d44d-110">*pC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d44d-111">Tipo: **const [**D3DXCOLOR**](../direct3d9/d3dxcolor.md) \***</span><span class="sxs-lookup"><span data-stu-id="4d44d-111">Type: **const [**D3DXCOLOR**](../direct3d9/d3dxcolor.md)\***</span></span>

<span data-ttu-id="4d44d-112">Puntatore a una struttura D3DXCOLOR di origine.</span><span class="sxs-lookup"><span data-stu-id="4d44d-112">Pointer to a source D3DXCOLOR structure.</span></span>

</dd> <dt>

<span data-ttu-id="4d44d-113">*c* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4d44d-113">*c* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d44d-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4d44d-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4d44d-115">Valore di contrasto.</span><span class="sxs-lookup"><span data-stu-id="4d44d-115">Contrast value.</span></span> <span data-ttu-id="4d44d-116">Questo parametro esegue l'interpolazione lineare tra il 50% di grigio e il colore, pC.</span><span class="sxs-lookup"><span data-stu-id="4d44d-116">This parameter linearly interpolates between fifty percent gray and the color, pC.</span></span> <span data-ttu-id="4d44d-117">Non sono previsti limiti per il valore di c.</span><span class="sxs-lookup"><span data-stu-id="4d44d-117">There are no limits on the value of c.</span></span> <span data-ttu-id="4d44d-118">Se questo parametro è zero, il colore restituito è il 50% di grigio.</span><span class="sxs-lookup"><span data-stu-id="4d44d-118">If this parameter is zero, then the returned color is fifty percent gray.</span></span> <span data-ttu-id="4d44d-119">Se questo parametro è 1, il colore restituito è quello originale.</span><span class="sxs-lookup"><span data-stu-id="4d44d-119">If this parameter is 1, then the returned color is the original color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d44d-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4d44d-120">Return value</span></span>

<span data-ttu-id="4d44d-121">Tipo: **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="4d44d-121">Type: **[**D3DXCOLOR**](../direct3d9/d3dxcolor.md)\***</span></span>

<span data-ttu-id="4d44d-122">Questa funzione restituisce un puntatore a una struttura D3DXCOLOR che è il risultato della regolazione del contrasto.</span><span class="sxs-lookup"><span data-stu-id="4d44d-122">This function returns a pointer to a D3DXCOLOR structure that is the result of the contrast adjustment.</span></span>

## <a name="remarks"></a><span data-ttu-id="4d44d-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="4d44d-123">Remarks</span></span>

<span data-ttu-id="4d44d-124">Il canale alfa di input viene copiato, non modificato, nel canale alfa di output.</span><span class="sxs-lookup"><span data-stu-id="4d44d-124">The input alpha channel is copied, unmodified, to the output alpha channel.</span></span>

<span data-ttu-id="4d44d-125">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro broncio.</span><span class="sxs-lookup"><span data-stu-id="4d44d-125">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="4d44d-126">In questo modo, questa funzione può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="4d44d-126">In this way, this function can be used as a parameter for another function.</span></span>

<span data-ttu-id="4d44d-127">Questa funzione interpola i componenti di colore rosso, verde e blu di una struttura D3DXCOLOR tra il 50% di grigio e un valore di contrasto specificato, come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="4d44d-127">This function interpolates the red, green, and blue color components of a D3DXCOLOR structure between fifty percent gray and a specified contrast value, as shown in the following example.</span></span>


```
pOut->r = 0.5f + c * (pC->r - 0.5f);
```



<span data-ttu-id="4d44d-128">Se c è maggiore di 0 e minore di 1, il contrasto viene ridotto.</span><span class="sxs-lookup"><span data-stu-id="4d44d-128">If c is greater than 0 and less than 1, the contrast is decreased.</span></span> <span data-ttu-id="4d44d-129">Se c è maggiore di 1, il contrasto viene aumentato.</span><span class="sxs-lookup"><span data-stu-id="4d44d-129">If c is greater than 1, the contrast is increased.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d44d-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4d44d-130">Requirements</span></span>



| <span data-ttu-id="4d44d-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d44d-131">Requirement</span></span> | <span data-ttu-id="4d44d-132">Valore</span><span class="sxs-lookup"><span data-stu-id="4d44d-132">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4d44d-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4d44d-133">Header</span></span><br/>  | <dl> <span data-ttu-id="4d44d-134"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="4d44d-134"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="4d44d-135">Libreria</span><span class="sxs-lookup"><span data-stu-id="4d44d-135">Library</span></span><br/> | <dl> <span data-ttu-id="4d44d-136"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4d44d-136"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4d44d-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4d44d-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d44d-138">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="4d44d-138">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
