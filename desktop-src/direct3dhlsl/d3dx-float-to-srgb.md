---
title: Funzione D3DX_FLOAT_to_SRGB
description: Converte un valore FLOAT in un valore SRGB.
ms.assetid: 734a0837-98da-45ba-bb0b-1e930ba78a7d
keywords:
- Funzione D3DX_FLOAT_to_SRGB HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT_to_SRGB
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a71afb0c4e601be70c1ec04bd7bcd5e76c6cc573
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996177"
---
# <a name="d3dx_float_to_srgb-function"></a><span data-ttu-id="09447-104">\_Funzione float D3DX \_ a \_ sRGB</span><span class="sxs-lookup"><span data-stu-id="09447-104">D3DX\_FLOAT\_to\_SRGB function</span></span>

<span data-ttu-id="09447-105">Converte un valore FLOAT in un valore SRGB.</span><span class="sxs-lookup"><span data-stu-id="09447-105">Converts a FLOAT value to an SRGB.</span></span>

## <a name="syntax"></a><span data-ttu-id="09447-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="09447-106">Syntax</span></span>

``` syntax
FLOAT D3DX_FLOAT_to_SRGB(
   FLOAT val
);
```

## <a name="parameters"></a><span data-ttu-id="09447-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="09447-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09447-108">*Val*</span><span class="sxs-lookup"><span data-stu-id="09447-108">*val*</span></span> 
</dt> <dd>

<span data-ttu-id="09447-109">Valore FLOAT da convertire.</span><span class="sxs-lookup"><span data-stu-id="09447-109">FLOAT value to convert.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09447-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="09447-110">Return value</span></span>

<span data-ttu-id="09447-111">Valore SRGB convertito.</span><span class="sxs-lookup"><span data-stu-id="09447-111">The converted SRGB value.</span></span>

## <a name="requirements"></a><span data-ttu-id="09447-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="09447-112">Requirements</span></span>



| <span data-ttu-id="09447-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="09447-113">Requirement</span></span> | <span data-ttu-id="09447-114">Valore</span><span class="sxs-lookup"><span data-stu-id="09447-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09447-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="09447-115">Header</span></span><br/> | <dl> <span data-ttu-id="09447-116"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="09447-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09447-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="09447-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09447-118">Funzioni</span><span class="sxs-lookup"><span data-stu-id="09447-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="09447-119">Decompressione e compressione \_ del formato DXGI per la modifica dell'immagine In-Place</span><span class="sxs-lookup"><span data-stu-id="09447-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





