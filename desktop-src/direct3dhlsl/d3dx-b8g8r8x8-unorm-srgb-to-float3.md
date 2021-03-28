---
title: Funzione D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3
description: Decomprime \_ \_ \_ i dati di DXGI Format B8G8R8X8 UNORM \_ sRGB shader in un XMFLOAT3. | Funzione D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3
ms.assetid: 9b3c511c-95c2-454c-95b9-ff6ab0920466
keywords:
- Funzione D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3 HLSL
topic_type:
- apiref
api_name:
- D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 277f10bc574e03a7bd608a333cba65f95a3e0b43
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104995798"
---
# <a name="d3dx_b8g8r8x8_unorm_srgb_to_float3-function"></a><span data-ttu-id="93ef9-105">D3DX \_ B8G8R8X8 \_ UNORM \_ sRGB \_ to \_ FLOAT3 Function</span><span class="sxs-lookup"><span data-stu-id="93ef9-105">D3DX\_B8G8R8X8\_UNORM\_SRGB\_to\_FLOAT3 function</span></span>

<span data-ttu-id="93ef9-106">Decomprime \_ \_ \_ i dati di DXGI Format B8G8R8X8 UNORM \_ sRGB shader in un XMFLOAT3.</span><span class="sxs-lookup"><span data-stu-id="93ef9-106">Unpacks DXGI\_FORMAT\_B8G8R8X8\_UNORM\_SRGB shader data to an XMFLOAT3.</span></span>

## <a name="syntax"></a><span data-ttu-id="93ef9-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="93ef9-107">Syntax</span></span>

``` syntax
XMFLOAT3 D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3(
   UINT packedInput
);
```

## <a name="parameters"></a><span data-ttu-id="93ef9-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="93ef9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93ef9-109">*packedInput*</span><span class="sxs-lookup"><span data-stu-id="93ef9-109">*packedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="93ef9-110">Dati dello shader compressi.</span><span class="sxs-lookup"><span data-stu-id="93ef9-110">The packed shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93ef9-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="93ef9-111">Return value</span></span>

<span data-ttu-id="93ef9-112">Dati dello shader decompressi.</span><span class="sxs-lookup"><span data-stu-id="93ef9-112">The unpacked shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="93ef9-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="93ef9-113">Requirements</span></span>



| <span data-ttu-id="93ef9-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="93ef9-114">Requirement</span></span> | <span data-ttu-id="93ef9-115">Valore</span><span class="sxs-lookup"><span data-stu-id="93ef9-115">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93ef9-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="93ef9-116">Header</span></span><br/> | <dl> <span data-ttu-id="93ef9-117"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="93ef9-117"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93ef9-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="93ef9-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93ef9-119">Funzioni</span><span class="sxs-lookup"><span data-stu-id="93ef9-119">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="93ef9-120">Decompressione e compressione \_ del formato DXGI per la modifica dell'immagine In-Place</span><span class="sxs-lookup"><span data-stu-id="93ef9-120">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





