---
title: Funzione D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3_inexact
description: Decomprime \_ \_ \_ i dati di DXGI Format B8G8R8X8 UNORM \_ sRGB shader in un XMFLOAT3. | Funzione D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3_inexact
ms.assetid: caa64f89-7b9e-4bc0-82dc-31edfd31d495
keywords:
- Funzione D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3_inexact HLSL
topic_type:
- apiref
api_name:
- D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3_inexact
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ef3f0b97ee3d5e21fef7b0227304fc5b187df2c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982112"
---
# <a name="d3dx_b8g8r8x8_unorm_srgb_to_float3_inexact-function"></a><span data-ttu-id="f0ae6-105">D3DX \_ B8G8R8X8 \_ UNORM \_ sRGB \_ to \_ FLOAT3 \_ unexact Function</span><span class="sxs-lookup"><span data-stu-id="f0ae6-105">D3DX\_B8G8R8X8\_UNORM\_SRGB\_to\_FLOAT3\_inexact function</span></span>

<span data-ttu-id="f0ae6-106">Decomprime \_ \_ \_ i dati di DXGI Format B8G8R8X8 UNORM \_ sRGB shader in un XMFLOAT3.</span><span class="sxs-lookup"><span data-stu-id="f0ae6-106">Unpacks DXGI\_FORMAT\_B8G8R8X8\_UNORM\_SRGB shader data to an XMFLOAT3.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0ae6-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f0ae6-107">Syntax</span></span>

``` syntax
XMFLOAT3 D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3_inexact(
   UINT packedInput
);
```

## <a name="parameters"></a><span data-ttu-id="f0ae6-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="f0ae6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0ae6-109">*packedInput*</span><span class="sxs-lookup"><span data-stu-id="f0ae6-109">*packedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="f0ae6-110">Dati dello shader compressi.</span><span class="sxs-lookup"><span data-stu-id="f0ae6-110">The packed shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0ae6-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f0ae6-111">Return value</span></span>

<span data-ttu-id="f0ae6-112">Dati dello shader decompressi.</span><span class="sxs-lookup"><span data-stu-id="f0ae6-112">The unpacked shader data.</span></span>

## <a name="remarks"></a><span data-ttu-id="f0ae6-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="f0ae6-113">Remarks</span></span>

<span data-ttu-id="f0ae6-114">Questa funzione Usa istruzioni shader che non hanno una precisione sufficientemente elevata per fornire la risposta esatta.</span><span class="sxs-lookup"><span data-stu-id="f0ae6-114">This function uses shader instructions that don't have high enough precision to give the exact answer.</span></span> <span data-ttu-id="f0ae6-115">La funzione alternativa [**D3DX \_ B8G8R8X8 \_ UNORM \_ sRGB \_ a \_ FLOAT3**](d3dx-b8g8r8x8-unorm-srgb-to-float3.md) usa una tabella di ricerca archiviata nello shader per fornire una conversione esattamente da sRGB a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="f0ae6-115">The alternative function [**D3DX\_B8G8R8X8\_UNORM\_SRGB\_to\_FLOAT3**](d3dx-b8g8r8x8-unorm-srgb-to-float3.md) uses a lookup table stored in the shader to give an exact SRGB to float conversion.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0ae6-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f0ae6-116">Requirements</span></span>



| <span data-ttu-id="f0ae6-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0ae6-117">Requirement</span></span> | <span data-ttu-id="f0ae6-118">Valore</span><span class="sxs-lookup"><span data-stu-id="f0ae6-118">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0ae6-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f0ae6-119">Header</span></span><br/> | <dl> <span data-ttu-id="f0ae6-120"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="f0ae6-120"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0ae6-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f0ae6-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0ae6-122">Funzioni</span><span class="sxs-lookup"><span data-stu-id="f0ae6-122">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="f0ae6-123">Decompressione e compressione \_ del formato DXGI per la modifica dell'immagine In-Place</span><span class="sxs-lookup"><span data-stu-id="f0ae6-123">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





