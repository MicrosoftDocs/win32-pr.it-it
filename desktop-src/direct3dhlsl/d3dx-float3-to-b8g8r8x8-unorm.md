---
title: Funzione D3DX_FLOAT3_to_B8G8R8X8_UNORM
description: Comprime il XMFLOAT3 specificato in un \_ formato DXGI \_ B8G8R8X8 \_ UNORM uint.
ms.assetid: 9492578b-e3c3-4856-b6d2-49f776a21d77
keywords:
- Funzione D3DX_FLOAT3_to_B8G8R8X8_UNORM HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT3_to_B8G8R8X8_UNORM
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29d922264c62526b79aec5d3e36bb477e6a62987
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104995903"
---
# <a name="d3dx_float3_to_b8g8r8x8_unorm-function"></a><span data-ttu-id="4e4a1-104">D3DX \_ FLOAT3 \_ to \_ B8G8R8X8 \_ UNORM Function</span><span class="sxs-lookup"><span data-stu-id="4e4a1-104">D3DX\_FLOAT3\_to\_B8G8R8X8\_UNORM function</span></span>

<span data-ttu-id="4e4a1-105">Comprime il XMFLOAT3 specificato in un \_ formato DXGI \_ B8G8R8X8 \_ UNORM uint.</span><span class="sxs-lookup"><span data-stu-id="4e4a1-105">Packs the given XMFLOAT3 into a DXGI\_FORMAT\_B8G8R8X8\_UNORM UINT.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e4a1-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4e4a1-106">Syntax</span></span>

``` syntax
UINT D3DX_FLOAT3_to_B8G8R8X8_UNORM(
   hlsl_precise XMFLOAT3 unpackedInput
);
```

## <a name="parameters"></a><span data-ttu-id="4e4a1-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="4e4a1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e4a1-108">*unpackedInput*</span><span class="sxs-lookup"><span data-stu-id="4e4a1-108">*unpackedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="4e4a1-109">Dati dello shader decompressi.</span><span class="sxs-lookup"><span data-stu-id="4e4a1-109">The unpacked shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e4a1-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4e4a1-110">Return value</span></span>

<span data-ttu-id="4e4a1-111">Dati dello shader compressi.</span><span class="sxs-lookup"><span data-stu-id="4e4a1-111">The packed shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e4a1-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4e4a1-112">Requirements</span></span>



| <span data-ttu-id="4e4a1-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e4a1-113">Requirement</span></span> | <span data-ttu-id="4e4a1-114">Valore</span><span class="sxs-lookup"><span data-stu-id="4e4a1-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e4a1-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4e4a1-115">Header</span></span><br/> | <dl> <span data-ttu-id="4e4a1-116"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="4e4a1-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e4a1-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4e4a1-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e4a1-118">Funzioni</span><span class="sxs-lookup"><span data-stu-id="4e4a1-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="4e4a1-119">Decompressione e compressione \_ del formato DXGI per la modifica dell'immagine In-Place</span><span class="sxs-lookup"><span data-stu-id="4e4a1-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





