---
title: Funzione D3DX_SRGB_to_FLOAT_inexact
description: Converte un valore SRGB in FLOAT. | Funzione D3DX_SRGB_to_FLOAT_inexact
ms.assetid: 6eadda6d-ff99-4a8e-9e30-ae455732438e
keywords:
- Funzione D3DX_SRGB_to_FLOAT_inexact HLSL
topic_type:
- apiref
api_name:
- D3DX_SRGB_to_FLOAT_inexact
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44804ad73ab49ce4f62274c870d8487501c44361
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982208"
---
# <a name="d3dx_srgb_to_float_inexact-function"></a><span data-ttu-id="c517c-105">D3DX \_ sRGB \_ per \_ float- \_ funzione inesatta</span><span class="sxs-lookup"><span data-stu-id="c517c-105">D3DX\_SRGB\_to\_FLOAT\_inexact function</span></span>

<span data-ttu-id="c517c-106">Converte un valore SRGB in FLOAT.</span><span class="sxs-lookup"><span data-stu-id="c517c-106">Converts an SRGB value to FLOAT.</span></span>

## <a name="syntax"></a><span data-ttu-id="c517c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c517c-107">Syntax</span></span>

``` syntax
FLOAT D3DX_SRGB_to_FLOAT_inexact(
   hlsl_precise FLOAT val
);
```

## <a name="parameters"></a><span data-ttu-id="c517c-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="c517c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c517c-109">*Val*</span><span class="sxs-lookup"><span data-stu-id="c517c-109">*val*</span></span> 
</dt> <dd>

<span data-ttu-id="c517c-110">Valore SRGB da convertire.</span><span class="sxs-lookup"><span data-stu-id="c517c-110">SRGB value to convert.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c517c-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c517c-111">Return value</span></span>

<span data-ttu-id="c517c-112">Valore SRGB convertito.</span><span class="sxs-lookup"><span data-stu-id="c517c-112">The converted SRGB value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c517c-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="c517c-113">Remarks</span></span>

<span data-ttu-id="c517c-114">Questa funzione non ha una precisione sufficientemente elevata per fornire la risposta esatta.</span><span class="sxs-lookup"><span data-stu-id="c517c-114">This function doesn't have a high enough precision to give the exact answer.</span></span> <span data-ttu-id="c517c-115">La funzione alternativa [**D3DX \_ sRGB \_ per \_ float**](d3dx-srgb-to-float.md) usa una tabella di ricerca per ottenere una conversione esattamente da sRGB a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="c517c-115">The alternative function [**D3DX\_SRGB\_to\_FLOAT**](d3dx-srgb-to-float.md) uses a lookup table to give an exact SRGB to float conversion.</span></span>

## <a name="requirements"></a><span data-ttu-id="c517c-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c517c-116">Requirements</span></span>



| <span data-ttu-id="c517c-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="c517c-117">Requirement</span></span> | <span data-ttu-id="c517c-118">Valore</span><span class="sxs-lookup"><span data-stu-id="c517c-118">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c517c-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c517c-119">Header</span></span><br/> | <dl> <span data-ttu-id="c517c-120"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="c517c-120"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c517c-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c517c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c517c-122">Funzioni</span><span class="sxs-lookup"><span data-stu-id="c517c-122">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="c517c-123">Decompressione e compressione \_ del formato DXGI per la modifica dell'immagine In-Place</span><span class="sxs-lookup"><span data-stu-id="c517c-123">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





