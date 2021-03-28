---
title: Funzione D3DX_FLOAT3_to_B8G8R8X8_UNORM_SRGB
description: Comprime il XMFLOAT3 specificato in un formato DXGI \_ \_ B8G8R8X8 \_ UNORM \_ sRGB.
ms.assetid: 42d1e8f1-d1b7-4c93-a658-d25790e78830
keywords:
- Funzione D3DX_FLOAT3_to_B8G8R8X8_UNORM_SRGB HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT3_to_B8G8R8X8_UNORM_SRGB
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e74dd5fbc1329d884968d76039061fceb22aafbf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104995855"
---
# <a name="d3dx_float3_to_b8g8r8x8_unorm_srgb-function"></a><span data-ttu-id="d9ee9-104">D3DX \_ FLOAT3 \_ to \_ B8G8R8X8 \_ UNORM \_ sRGB Function</span><span class="sxs-lookup"><span data-stu-id="d9ee9-104">D3DX\_FLOAT3\_to\_B8G8R8X8\_UNORM\_SRGB function</span></span>

<span data-ttu-id="d9ee9-105">Comprime il XMFLOAT3 specificato in un formato DXGI \_ \_ B8G8R8X8 \_ UNORM \_ sRGB.</span><span class="sxs-lookup"><span data-stu-id="d9ee9-105">Packs the given XMFLOAT3 back into a DXGI\_FORMAT\_B8G8R8X8\_UNORM\_SRGB.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9ee9-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d9ee9-106">Syntax</span></span>

``` syntax
UINT D3DX_FLOAT3_to_B8G8R8X8_UNORM_SRGB(
   hlsl_precise XMFLOAT3 unpackedInput
);
```

## <a name="parameters"></a><span data-ttu-id="d9ee9-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="d9ee9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9ee9-108">*unpackedInput*</span><span class="sxs-lookup"><span data-stu-id="d9ee9-108">*unpackedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="d9ee9-109">Dati dello shader da comprimere.</span><span class="sxs-lookup"><span data-stu-id="d9ee9-109">The shader data to pack.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9ee9-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d9ee9-110">Return value</span></span>

<span data-ttu-id="d9ee9-111">Dati dello shader compressi.</span><span class="sxs-lookup"><span data-stu-id="d9ee9-111">The packed shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9ee9-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d9ee9-112">Requirements</span></span>



| <span data-ttu-id="d9ee9-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9ee9-113">Requirement</span></span> | <span data-ttu-id="d9ee9-114">Valore</span><span class="sxs-lookup"><span data-stu-id="d9ee9-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9ee9-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d9ee9-115">Header</span></span><br/> | <dl> <span data-ttu-id="d9ee9-116"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="d9ee9-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9ee9-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d9ee9-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9ee9-118">Funzioni</span><span class="sxs-lookup"><span data-stu-id="d9ee9-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="d9ee9-119">Decompressione e compressione \_ del formato DXGI per la modifica dell'immagine In-Place</span><span class="sxs-lookup"><span data-stu-id="d9ee9-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





