---
description: 'Funzione D3DXColorAdjustSaturation (D3DX10Math.h): regola il valore di saturazione di un colore.'
ms.assetid: a7ca64b4-2198-4116-8e9f-79d6c922fd09
title: Funzione D3DXColorAdjustSaturation (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXColorAdjustSaturation
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 9e9ae91f5c898dae8ff922616bc02846732c760a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103539"
---
# <a name="d3dxcoloradjustsaturation-function-d3dx10mathh"></a><span data-ttu-id="af3cf-103">Funzione D3DXColorAdjustSaturation (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="af3cf-103">D3DXColorAdjustSaturation function (D3DX10Math.h)</span></span>

<span data-ttu-id="af3cf-104">Regola il valore di saturazione di un colore.</span><span class="sxs-lookup"><span data-stu-id="af3cf-104">Adjusts the saturation value of a color.</span></span>

## <a name="syntax"></a><span data-ttu-id="af3cf-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="af3cf-105">Syntax</span></span>


```C++
D3DXCOLOR* D3DXColorAdjustSaturation(
  _In_       D3DXCOLOR *pOut,
  _In_ const D3DXCOLOR *pC,
  _In_       FLOAT     s
);
```



## <a name="parameters"></a><span data-ttu-id="af3cf-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="af3cf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af3cf-107">*pOut* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="af3cf-107">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af3cf-108">Tipo: **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="af3cf-108">Type: **[**D3DXCOLOR**](../direct3d9/d3dxcolor.md)\***</span></span>

<span data-ttu-id="af3cf-109">Puntatore a [**un oggetto D3DXCOLOR**](d3d10-d3dxcolor.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="af3cf-109">Pointer to a [**D3DXCOLOR**](d3d10-d3dxcolor.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="af3cf-110">*pC* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="af3cf-110">*pC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af3cf-111">Tipo: **const [**D3DXCOLOR**](../direct3d9/d3dxcolor.md) \***</span><span class="sxs-lookup"><span data-stu-id="af3cf-111">Type: **const [**D3DXCOLOR**](../direct3d9/d3dxcolor.md)\***</span></span>

<span data-ttu-id="af3cf-112">Puntatore a una struttura D3DXCOLOR di origine.</span><span class="sxs-lookup"><span data-stu-id="af3cf-112">Pointer to a source D3DXCOLOR structure.</span></span>

</dd> <dt>

<span data-ttu-id="af3cf-113">*s* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="af3cf-113">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af3cf-114">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="af3cf-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="af3cf-115">Valore di saturazione.</span><span class="sxs-lookup"><span data-stu-id="af3cf-115">Saturation value.</span></span> <span data-ttu-id="af3cf-116">Questo parametro interpola in modo lineare tra il colore convertito in gradazioni di grigio e il colore originale, pC.</span><span class="sxs-lookup"><span data-stu-id="af3cf-116">This parameter linearly interpolates between the color converted to grayscale and the original color, pC.</span></span> <span data-ttu-id="af3cf-117">Non sono previsti limiti al valore di .</span><span class="sxs-lookup"><span data-stu-id="af3cf-117">There are no limits on the value of s.</span></span> <span data-ttu-id="af3cf-118">Se s è 0, il colore restituito è il colore in scala di grigi.</span><span class="sxs-lookup"><span data-stu-id="af3cf-118">If s is 0, the returned color is the grayscale color.</span></span> <span data-ttu-id="af3cf-119">Se s è 1, il colore restituito è il colore originale.</span><span class="sxs-lookup"><span data-stu-id="af3cf-119">If s is 1, the returned color is the original color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af3cf-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="af3cf-120">Return value</span></span>

<span data-ttu-id="af3cf-121">Tipo: **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="af3cf-121">Type: **[**D3DXCOLOR**](../direct3d9/d3dxcolor.md)\***</span></span>

<span data-ttu-id="af3cf-122">Questa funzione restituisce un puntatore a una struttura D3DXCOLOR che è il risultato della regolazione della saturazione.</span><span class="sxs-lookup"><span data-stu-id="af3cf-122">This function returns a pointer to a D3DXCOLOR structure that is the result of the saturation adjustment.</span></span>

## <a name="remarks"></a><span data-ttu-id="af3cf-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="af3cf-123">Remarks</span></span>

<span data-ttu-id="af3cf-124">Il canale alfa di input viene copiato, senza modifiche, nel canale alfa di output.</span><span class="sxs-lookup"><span data-stu-id="af3cf-124">The input alpha channel is copied, unmodified, to the output alpha channel.</span></span>

<span data-ttu-id="af3cf-125">Il valore restituito per questa funzione è lo stesso valore restituito nel parametro pOut.</span><span class="sxs-lookup"><span data-stu-id="af3cf-125">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="af3cf-126">In questo modo, questa funzione può essere usata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="af3cf-126">In this way, this function can be used as a parameter for another function.</span></span>

<span data-ttu-id="af3cf-127">Questa funzione interpola i componenti di colore rosso, verde e blu di una struttura D3DXCOLOR tra un colore non saturo e un colore, come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="af3cf-127">This function interpolates the red, green, and blue color components of a D3DXCOLOR structure between an unsaturated color and a color, as shown in the following example.</span></span>


```
//Approximate values for each component's contribution to luminance.
//Based upon the NTSC standard described in ITU-R Recommendation BT.709.
FLOAT grey = pC->r * 0.2125f + pC->g * 0.7154f + pC->b * 0.0721f;

pOut->r = grey + s * (pC->r - grey);
```



<span data-ttu-id="af3cf-128">Se s è maggiore di 0 e minore di 1, la saturazione viene ridotta.</span><span class="sxs-lookup"><span data-stu-id="af3cf-128">If s is greater than 0 and less than 1, the saturation is decreased.</span></span> <span data-ttu-id="af3cf-129">Se s è maggiore di 1, la saturazione viene aumentata.</span><span class="sxs-lookup"><span data-stu-id="af3cf-129">If s is greater than 1, the saturation is increased.</span></span>

<span data-ttu-id="af3cf-130">Il colore in scala di grigi viene calcolato come:</span><span class="sxs-lookup"><span data-stu-id="af3cf-130">The grayscale color is computed as:</span></span>


```
r = g = b = 0.2125*r + 0.7154*g + 0.0721*b;
```



## <a name="requirements"></a><span data-ttu-id="af3cf-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="af3cf-131">Requirements</span></span>



| <span data-ttu-id="af3cf-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="af3cf-132">Requirement</span></span> | <span data-ttu-id="af3cf-133">Valore</span><span class="sxs-lookup"><span data-stu-id="af3cf-133">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="af3cf-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="af3cf-134">Header</span></span><br/>  | <dl> <span data-ttu-id="af3cf-135"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="af3cf-135"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="af3cf-136">Libreria</span><span class="sxs-lookup"><span data-stu-id="af3cf-136">Library</span></span><br/> | <dl> <span data-ttu-id="af3cf-137"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="af3cf-137"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="af3cf-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="af3cf-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af3cf-139">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="af3cf-139">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
