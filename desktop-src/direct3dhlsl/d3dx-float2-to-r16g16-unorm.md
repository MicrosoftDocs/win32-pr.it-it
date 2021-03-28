---
title: Funzione D3DX_FLOAT2_to_R16G16_UNORM
description: Comprime il XMFLOAT2 specificato in un formato DXGI \_ \_ R16G16 \_ UNORM.
ms.assetid: 5a1bd034-262f-4f55-8f38-d2fda42bb13b
keywords:
- Funzione D3DX_FLOAT2_to_R16G16_UNORM HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT2_to_R16G16_UNORM
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f0a6ffe3081955db79765d80278394eb89ab188
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104995906"
---
# <a name="d3dx_float2_to_r16g16_unorm-function"></a><span data-ttu-id="8b67f-104">D3DX \_ FLOAT2 \_ to \_ R16G16 \_ UNORM Function</span><span class="sxs-lookup"><span data-stu-id="8b67f-104">D3DX\_FLOAT2\_to\_R16G16\_UNORM function</span></span>

<span data-ttu-id="8b67f-105">Comprime il XMFLOAT2 specificato in un formato DXGI \_ \_ R16G16 \_ UNORM.</span><span class="sxs-lookup"><span data-stu-id="8b67f-105">Packs the given XMFLOAT2 back into a DXGI\_FORMAT\_R16G16\_UNORM.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b67f-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8b67f-106">Syntax</span></span>

``` syntax
UINT D3DX_FLOAT2_to_R16G16_UNORM(
   XMFLOAT2 unpackedInput
);
```

## <a name="parameters"></a><span data-ttu-id="8b67f-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="8b67f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b67f-108">*unpackedInput*</span><span class="sxs-lookup"><span data-stu-id="8b67f-108">*unpackedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="8b67f-109">Dati dello shader decompressi.</span><span class="sxs-lookup"><span data-stu-id="8b67f-109">The unpacked shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b67f-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8b67f-110">Return value</span></span>

<span data-ttu-id="8b67f-111">Dati dello shader compressi.</span><span class="sxs-lookup"><span data-stu-id="8b67f-111">The packed shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b67f-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8b67f-112">Requirements</span></span>



| <span data-ttu-id="8b67f-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b67f-113">Requirement</span></span> | <span data-ttu-id="8b67f-114">Valore</span><span class="sxs-lookup"><span data-stu-id="8b67f-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b67f-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8b67f-115">Header</span></span><br/> | <dl> <span data-ttu-id="8b67f-116"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="8b67f-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b67f-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8b67f-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b67f-118">Funzioni</span><span class="sxs-lookup"><span data-stu-id="8b67f-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="8b67f-119">Decompressione e compressione \_ del formato DXGI per la modifica dell'immagine In-Place</span><span class="sxs-lookup"><span data-stu-id="8b67f-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





