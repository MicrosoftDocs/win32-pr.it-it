---
title: Funzione D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4_inexact
description: Decomprime \_ \_ \_ i dati di DXGI Format R8G8B8A8 UNORM \_ sRGB shader in un XMFLOAT4. | Funzione D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4_inexact
ms.assetid: ca7c2bf8-30fd-48fa-b4d9-e69c28c7f603
keywords:
- Funzione D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4_inexact HLSL
topic_type:
- apiref
api_name:
- D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4_inexact
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74d3d4a9d47eb520d151fe2e3388e99f401fc0a4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969400"
---
# <a name="d3dx_r8g8b8a8_unorm_srgb_to_float4_inexact-function"></a><span data-ttu-id="41353-105">D3DX \_ R8G8B8A8 \_ UNORM \_ sRGB \_ to \_ float4 \_ unexact Function</span><span class="sxs-lookup"><span data-stu-id="41353-105">D3DX\_R8G8B8A8\_UNORM\_SRGB\_to\_FLOAT4\_inexact function</span></span>

<span data-ttu-id="41353-106">Decomprime \_ \_ \_ i dati di DXGI Format R8G8B8A8 UNORM \_ sRGB shader in un XMFLOAT4.</span><span class="sxs-lookup"><span data-stu-id="41353-106">Unpacks DXGI\_FORMAT\_R8G8B8A8\_UNORM\_SRGB shader data to an XMFLOAT4.</span></span>

## <a name="syntax"></a><span data-ttu-id="41353-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="41353-107">Syntax</span></span>

``` syntax
XMFLOAT4 D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4_inexact(
   UINT packedInput
);
```

## <a name="parameters"></a><span data-ttu-id="41353-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="41353-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41353-109">*packedInput*</span><span class="sxs-lookup"><span data-stu-id="41353-109">*packedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="41353-110">Dati dello shader compressi.</span><span class="sxs-lookup"><span data-stu-id="41353-110">The packed shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41353-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="41353-111">Return value</span></span>

<span data-ttu-id="41353-112">Dati dello shader decompressi.</span><span class="sxs-lookup"><span data-stu-id="41353-112">The unpacked shader data.</span></span>

## <a name="remarks"></a><span data-ttu-id="41353-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="41353-113">Remarks</span></span>

<span data-ttu-id="41353-114">Questa funzione Usa istruzioni shader che non hanno una precisione sufficientemente elevata per fornire la risposta esatta.</span><span class="sxs-lookup"><span data-stu-id="41353-114">This function uses shader instructions that don't have high enough precision to give the exact answer.</span></span> <span data-ttu-id="41353-115">La funzione alternativa [**D3DX \_ R8G8B8A8 \_ UNORM \_ sRGB \_ a \_ float4**](d3dx-r8g8b8a8-unorm-srgb-to-float4.md) usa una tabella di ricerca archiviata nello shader per fornire una conversione esattamente da sRGB a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="41353-115">The alternative function [**D3DX\_R8G8B8A8\_UNORM\_SRGB\_to\_FLOAT4**](d3dx-r8g8b8a8-unorm-srgb-to-float4.md) uses a lookup table stored in the shader to give an exact SRGB to float conversion.</span></span>

## <a name="requirements"></a><span data-ttu-id="41353-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="41353-116">Requirements</span></span>



| <span data-ttu-id="41353-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="41353-117">Requirement</span></span> | <span data-ttu-id="41353-118">Valore</span><span class="sxs-lookup"><span data-stu-id="41353-118">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41353-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="41353-119">Header</span></span><br/> | <dl> <span data-ttu-id="41353-120"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="41353-120"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41353-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="41353-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41353-122">Funzioni</span><span class="sxs-lookup"><span data-stu-id="41353-122">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="41353-123">Decompressione e compressione \_ del formato DXGI per la modifica dell'immagine In-Place</span><span class="sxs-lookup"><span data-stu-id="41353-123">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





