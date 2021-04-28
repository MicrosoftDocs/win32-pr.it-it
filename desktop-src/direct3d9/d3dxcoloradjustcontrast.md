---
description: 'Funzione D3DXColorAdjustContrast (D3dx9math.h): regola il valore di contrasto di un colore.'
ms.assetid: be49c9c7-b625-4cbc-bd63-1d5766ae2dbb
title: Funzione D3DXColorAdjustContrast (D3dx9math.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9dc9bb79d1ebbe536661347d76d13846dead6aa8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115879"
---
# <a name="d3dxcoloradjustcontrast-function-d3dx9mathh"></a><span data-ttu-id="9b459-103">Funzione D3DXColorAdjustContrast (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="9b459-103">D3DXColorAdjustContrast function (D3dx9math.h)</span></span>

<span data-ttu-id="9b459-104">Regola il valore di contrasto di un colore.</span><span class="sxs-lookup"><span data-stu-id="9b459-104">Adjusts the contrast value of a color.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b459-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9b459-105">Syntax</span></span>


```C++
D3DXCOLOR* D3DXColorAdjustContrast(
  _Inout_       D3DXCOLOR *pOut,
  _In_    const D3DXCOLOR *pC,
  _In_          FLOAT     c
);
```



## <a name="parameters"></a><span data-ttu-id="9b459-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9b459-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b459-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="9b459-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="9b459-108">Tipo: **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="9b459-108">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="9b459-109">Puntatore a [**una struttura D3DXCOLOR**](d3dxcolor.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="9b459-109">Pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="9b459-110">*pC* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="9b459-110">*pC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b459-111">Tipo: **const [**D3DXCOLOR**](d3dxcolor.md) \***</span><span class="sxs-lookup"><span data-stu-id="9b459-111">Type: **const [**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="9b459-112">Puntatore a una [**struttura D3DXCOLOR di**](d3dxcolor.md) origine.</span><span class="sxs-lookup"><span data-stu-id="9b459-112">Pointer to a source [**D3DXCOLOR**](d3dxcolor.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="9b459-113">*c* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9b459-113">*c* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b459-114">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9b459-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9b459-115">Valore di contrasto.</span><span class="sxs-lookup"><span data-stu-id="9b459-115">Contrast value.</span></span> <span data-ttu-id="9b459-116">Questo parametro interpola in modo lineare tra il 50% di grigio e il colore, pC.</span><span class="sxs-lookup"><span data-stu-id="9b459-116">This parameter linearly interpolates between fifty percent gray and the color, pC.</span></span> <span data-ttu-id="9b459-117">Non sono previsti limiti per il valore di c.</span><span class="sxs-lookup"><span data-stu-id="9b459-117">There are not limits on the value of c.</span></span> <span data-ttu-id="9b459-118">Se questo parametro è zero, il colore restituito è il 50% grigio.</span><span class="sxs-lookup"><span data-stu-id="9b459-118">If this parameter is zero, then the returned color is fifty percent gray.</span></span> <span data-ttu-id="9b459-119">Se questo parametro è 1, il colore restituito è il colore originale.</span><span class="sxs-lookup"><span data-stu-id="9b459-119">If this parameter is 1, then the returned color is the original color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b459-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9b459-120">Return value</span></span>

<span data-ttu-id="9b459-121">Tipo: **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="9b459-121">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="9b459-122">Questa funzione restituisce un puntatore a [**una struttura D3DXCOLOR**](d3dxcolor.md) che è il risultato della regolazione del contrasto.</span><span class="sxs-lookup"><span data-stu-id="9b459-122">This function returns a pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the result of the contrast adjustment.</span></span>

## <a name="remarks"></a><span data-ttu-id="9b459-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="9b459-123">Remarks</span></span>

<span data-ttu-id="9b459-124">Il canale alfa di input viene copiato, senza modifiche, nel canale alfa di output.</span><span class="sxs-lookup"><span data-stu-id="9b459-124">The input alpha channel is copied, unmodified, to the output alpha channel.</span></span>

<span data-ttu-id="9b459-125">Il valore restituito per questa funzione è lo stesso valore restituito nel parametro pOut.</span><span class="sxs-lookup"><span data-stu-id="9b459-125">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="9b459-126">In questo modo, questa funzione può essere usata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="9b459-126">In this way, this function can be used as a parameter for another function.</span></span>

<span data-ttu-id="9b459-127">Questa funzione interpola i componenti di colore rosso, verde e blu di una struttura [**D3DXCOLOR**](d3dxcolor.md) tra la percentuale di grigio e un valore di contrasto specificato, come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="9b459-127">This function interpolates the red, green, and blue color components of a [**D3DXCOLOR**](d3dxcolor.md) structure between fifty percent gray and a specified contrast value, as shown in the following example.</span></span>


```
pOut->r = 0.5f + c * (pC->r - 0.5f);
```



<span data-ttu-id="9b459-128">Se c è maggiore di 0 e minore di 1, il contrasto viene ridotto.</span><span class="sxs-lookup"><span data-stu-id="9b459-128">If c is greater than 0 and less than 1, the contrast is decreased.</span></span> <span data-ttu-id="9b459-129">Se c è maggiore di 1, il contrasto viene aumentato.</span><span class="sxs-lookup"><span data-stu-id="9b459-129">If c is greater than 1, the contrast is increased.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b459-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9b459-130">Requirements</span></span>



| <span data-ttu-id="9b459-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b459-131">Requirement</span></span> | <span data-ttu-id="9b459-132">Valore</span><span class="sxs-lookup"><span data-stu-id="9b459-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9b459-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9b459-133">Header</span></span><br/>  | <dl> <span data-ttu-id="9b459-134"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="9b459-134"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="9b459-135">Libreria</span><span class="sxs-lookup"><span data-stu-id="9b459-135">Library</span></span><br/> | <dl> <span data-ttu-id="9b459-136"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="9b459-136"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9b459-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9b459-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b459-138">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="9b459-138">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="9b459-139">**D3DXColorAdjustSaturation**</span><span class="sxs-lookup"><span data-stu-id="9b459-139">**D3DXColorAdjustSaturation**</span></span>](d3dxcoloradjustsaturation.md)
</dt> </dl>

 

 
