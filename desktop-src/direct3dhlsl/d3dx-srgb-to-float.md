---
title: Funzione D3DX_SRGB_to_FLOAT
description: Converte un valore SRGB in FLOAT. | Funzione D3DX_SRGB_to_FLOAT
ms.assetid: 03e2ea09-3dd7-48cb-81b3-e11f7a9cf0ee
keywords:
- Funzione D3DX_SRGB_to_FLOAT HLSL
topic_type:
- apiref
api_name:
- D3DX_SRGB_to_FLOAT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32e1b5dc6224a06881e227b82e74436c4820aaf3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969387"
---
# <a name="d3dx_srgb_to_float-function"></a><span data-ttu-id="0906f-105">D3DX \_ sRGB \_ to \_ float-funzione</span><span class="sxs-lookup"><span data-stu-id="0906f-105">D3DX\_SRGB\_to\_FLOAT function</span></span>

<span data-ttu-id="0906f-106">Converte un valore SRGB in FLOAT.</span><span class="sxs-lookup"><span data-stu-id="0906f-106">Converts an SRGB value to FLOAT.</span></span>

## <a name="syntax"></a><span data-ttu-id="0906f-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0906f-107">Syntax</span></span>

``` syntax
FLOAT D3DX_SRGB_to_FLOAT(
   UINT val
);
```

## <a name="parameters"></a><span data-ttu-id="0906f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="0906f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0906f-109">*Val*</span><span class="sxs-lookup"><span data-stu-id="0906f-109">*val*</span></span> 
</dt> <dd>

<span data-ttu-id="0906f-110">Valore SRGB da convertire.</span><span class="sxs-lookup"><span data-stu-id="0906f-110">SRGB value to convert.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0906f-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0906f-111">Return value</span></span>

<span data-ttu-id="0906f-112">Valore SRGB convertito.</span><span class="sxs-lookup"><span data-stu-id="0906f-112">The converted SRGB value.</span></span>

## <a name="requirements"></a><span data-ttu-id="0906f-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0906f-113">Requirements</span></span>



| <span data-ttu-id="0906f-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="0906f-114">Requirement</span></span> | <span data-ttu-id="0906f-115">Valore</span><span class="sxs-lookup"><span data-stu-id="0906f-115">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0906f-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0906f-116">Header</span></span><br/> | <dl> <span data-ttu-id="0906f-117"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="0906f-117"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0906f-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0906f-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0906f-119">Funzioni</span><span class="sxs-lookup"><span data-stu-id="0906f-119">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="0906f-120">Decompressione e compressione \_ del formato DXGI per la modifica dell'immagine In-Place</span><span class="sxs-lookup"><span data-stu-id="0906f-120">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





