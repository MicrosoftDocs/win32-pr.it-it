---
title: Funzione D3DX_FLOAT4_to_B8G8R8A8_UNORM
description: Comprime il XMFLOAT4 specificato in un formato DXGI \_ \_ B8G8R8A8 \_ UNORM.
ms.assetid: 5b7452ed-446a-4760-83e6-f3209ac8daf4
keywords:
- Funzione D3DX_FLOAT4_to_B8G8R8A8_UNORM HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT4_to_B8G8R8A8_UNORM
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddec0922218b9770d7a0c4cb4877f6144eded900
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982196"
---
# <a name="d3dx_float4_to_b8g8r8a8_unorm-function"></a><span data-ttu-id="4aef6-104">D3DX \_ float4 \_ to \_ B8G8R8A8 \_ UNORM Function</span><span class="sxs-lookup"><span data-stu-id="4aef6-104">D3DX\_FLOAT4\_to\_B8G8R8A8\_UNORM function</span></span>

<span data-ttu-id="4aef6-105">Comprime il XMFLOAT4 specificato in un formato DXGI \_ \_ B8G8R8A8 \_ UNORM.</span><span class="sxs-lookup"><span data-stu-id="4aef6-105">Packs the given XMFLOAT4 back into a DXGI\_FORMAT\_B8G8R8A8\_UNORM.</span></span>

## <a name="syntax"></a><span data-ttu-id="4aef6-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4aef6-106">Syntax</span></span>

``` syntax
UINT D3DX_FLOAT4_to_B8G8R8A8_UNORM(
   hlsl_precise XMFLOAT4 unpackedInput
);
```

## <a name="parameters"></a><span data-ttu-id="4aef6-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="4aef6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4aef6-108">*unpackedInput*</span><span class="sxs-lookup"><span data-stu-id="4aef6-108">*unpackedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="4aef6-109">Dati dello shader da comprimere.</span><span class="sxs-lookup"><span data-stu-id="4aef6-109">The shader data to pack.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4aef6-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4aef6-110">Return value</span></span>

<span data-ttu-id="4aef6-111">Dati dello shader compressi.</span><span class="sxs-lookup"><span data-stu-id="4aef6-111">The packed shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="4aef6-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4aef6-112">Requirements</span></span>



| <span data-ttu-id="4aef6-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="4aef6-113">Requirement</span></span> | <span data-ttu-id="4aef6-114">Valore</span><span class="sxs-lookup"><span data-stu-id="4aef6-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4aef6-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4aef6-115">Header</span></span><br/> | <dl> <span data-ttu-id="4aef6-116"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="4aef6-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4aef6-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4aef6-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4aef6-118">Funzioni</span><span class="sxs-lookup"><span data-stu-id="4aef6-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="4aef6-119">Decompressione e compressione \_ del formato DXGI per la modifica dell'immagine In-Place</span><span class="sxs-lookup"><span data-stu-id="4aef6-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





