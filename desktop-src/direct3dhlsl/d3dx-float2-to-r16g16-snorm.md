---
title: Funzione D3DX_FLOAT2_to_R16G16_SNORM
description: Comprime di nuovo il XMFLOAT2 specificato in un \_ formato DXGI \_ R16G16 \_ russar.
ms.assetid: 7c5c6aae-b750-435a-9582-18b7689bc2d9
keywords:
- Funzione D3DX_FLOAT2_to_R16G16_SNORM HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT2_to_R16G16_SNORM
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba63d7d7f03988e416d06b645e5c15163e431a7e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969388"
---
# <a name="d3dx_float2_to_r16g16_snorm-function"></a><span data-ttu-id="fc890-104">D3DX \_ FLOAT2 \_ to \_ R16G16 \_ russat Function</span><span class="sxs-lookup"><span data-stu-id="fc890-104">D3DX\_FLOAT2\_to\_R16G16\_SNORM function</span></span>

<span data-ttu-id="fc890-105">Comprime di nuovo il XMFLOAT2 specificato in un \_ formato DXGI \_ R16G16 \_ russar.</span><span class="sxs-lookup"><span data-stu-id="fc890-105">Packs the given XMFLOAT2 back into a DXGI\_FORMAT\_R16G16\_SNORM.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc890-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fc890-106">Syntax</span></span>

``` syntax
UINT D3DX_FLOAT2_to_R16G16_SNORM(
   hlsl_precise XMFLOAT2 unpackedInput
);
```

## <a name="parameters"></a><span data-ttu-id="fc890-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="fc890-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc890-108">*unpackedInput*</span><span class="sxs-lookup"><span data-stu-id="fc890-108">*unpackedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="fc890-109">Dati dello shader decompressi.</span><span class="sxs-lookup"><span data-stu-id="fc890-109">The unpacked shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc890-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fc890-110">Return value</span></span>

<span data-ttu-id="fc890-111">Dati dello shader compressi.</span><span class="sxs-lookup"><span data-stu-id="fc890-111">The packed shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc890-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fc890-112">Requirements</span></span>



| <span data-ttu-id="fc890-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc890-113">Requirement</span></span> | <span data-ttu-id="fc890-114">Valore</span><span class="sxs-lookup"><span data-stu-id="fc890-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc890-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fc890-115">Header</span></span><br/> | <dl> <span data-ttu-id="fc890-116"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="fc890-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc890-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fc890-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc890-118">Funzioni</span><span class="sxs-lookup"><span data-stu-id="fc890-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="fc890-119">Decompressione e compressione \_ del formato DXGI per la modifica dell'immagine In-Place</span><span class="sxs-lookup"><span data-stu-id="fc890-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





