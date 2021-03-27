---
title: Funzione D3DX_FLOAT4_to_R8G8B8A8_UNORM_SRGB
description: Comprime il XMFLOAT4 specificato in un formato DXGI \_ \_ R8G8B8A8 \_ UNORM \_ sRGB.
ms.assetid: 66580428-6f06-4e0c-bf89-01f03c7304ad
keywords:
- Funzione D3DX_FLOAT4_to_R8G8B8A8_UNORM_SRGB HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT4_to_R8G8B8A8_UNORM_SRGB
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06f61e484675b94e1089436ce0b3bd564b3103a4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355769"
---
# <a name="d3dx_float4_to_r8g8b8a8_unorm_srgb-function"></a><span data-ttu-id="93f65-104">D3DX \_ float4 \_ to \_ R8G8B8A8 \_ UNORM \_ sRGB Function</span><span class="sxs-lookup"><span data-stu-id="93f65-104">D3DX\_FLOAT4\_to\_R8G8B8A8\_UNORM\_SRGB function</span></span>

<span data-ttu-id="93f65-105">Comprime il XMFLOAT4 specificato in un formato DXGI \_ \_ R8G8B8A8 \_ UNORM \_ sRGB.</span><span class="sxs-lookup"><span data-stu-id="93f65-105">Packs the given XMFLOAT4 back into a DXGI\_FORMAT\_R8G8B8A8\_UNORM\_SRGB.</span></span>

## <a name="syntax"></a><span data-ttu-id="93f65-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="93f65-106">Syntax</span></span>

``` syntax
UINT D3DX_FLOAT4_to_R8G8B8A8_UNORM_SRGB(
   hlsl_precise XMFLOAT4 unpackedInput
);
```

## <a name="parameters"></a><span data-ttu-id="93f65-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="93f65-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93f65-108">*unpackedInput*</span><span class="sxs-lookup"><span data-stu-id="93f65-108">*unpackedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="93f65-109">Dati dello shader da comprimere.</span><span class="sxs-lookup"><span data-stu-id="93f65-109">The shader data to pack.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93f65-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="93f65-110">Return value</span></span>

<span data-ttu-id="93f65-111">Dati dello shader compressi.</span><span class="sxs-lookup"><span data-stu-id="93f65-111">The packed shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="93f65-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="93f65-112">Requirements</span></span>



| <span data-ttu-id="93f65-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="93f65-113">Requirement</span></span> | <span data-ttu-id="93f65-114">Valore</span><span class="sxs-lookup"><span data-stu-id="93f65-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93f65-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="93f65-115">Header</span></span><br/> | <dl> <span data-ttu-id="93f65-116"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="93f65-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93f65-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="93f65-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93f65-118">Funzioni</span><span class="sxs-lookup"><span data-stu-id="93f65-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="93f65-119">Decompressione e compressione \_ del formato DXGI per la modifica dell'immagine In-Place</span><span class="sxs-lookup"><span data-stu-id="93f65-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





