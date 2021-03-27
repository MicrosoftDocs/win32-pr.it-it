---
title: Funzione D3DX_R8G8B8A8_SNORM_to_FLOAT4
description: Decomprime \_ \_ \_ i dati di DXGI Format R8G8B8A8 russar shader in un XMFLOAT4.
ms.assetid: 2f2b9d5e-f4d0-470a-a4bb-b333d57f03e7
keywords:
- Funzione D3DX_R8G8B8A8_SNORM_to_FLOAT4 HLSL
topic_type:
- apiref
api_name:
- D3DX_R8G8B8A8_SNORM_to_FLOAT4
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1a4153fa30f2792008ccc45bc3e16f5d404f33a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982217"
---
# <a name="d3dx_r8g8b8a8_snorm_to_float4-function"></a><span data-ttu-id="e03a3-104">D3DX \_ R8G8B8A8 \_ russa \_ to \_ float4 Function</span><span class="sxs-lookup"><span data-stu-id="e03a3-104">D3DX\_R8G8B8A8\_SNORM\_to\_FLOAT4 function</span></span>

<span data-ttu-id="e03a3-105">Decomprime \_ \_ \_ i dati di DXGI Format R8G8B8A8 russar shader in un XMFLOAT4.</span><span class="sxs-lookup"><span data-stu-id="e03a3-105">Unpacks DXGI\_FORMAT\_R8G8B8A8\_SNORM shader data to an XMFLOAT4.</span></span>

## <a name="syntax"></a><span data-ttu-id="e03a3-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e03a3-106">Syntax</span></span>

``` syntax
XMFLOAT4 D3DX_R8G8B8A8_SNORM_to_FLOAT4(
   UINT packedInput
);
```

## <a name="parameters"></a><span data-ttu-id="e03a3-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="e03a3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e03a3-108">*packedInput*</span><span class="sxs-lookup"><span data-stu-id="e03a3-108">*packedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="e03a3-109">Dati dello shader compressi.</span><span class="sxs-lookup"><span data-stu-id="e03a3-109">The packed shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e03a3-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e03a3-110">Return value</span></span>

<span data-ttu-id="e03a3-111">Dati dello shader decompressi.</span><span class="sxs-lookup"><span data-stu-id="e03a3-111">The unpacked shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="e03a3-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e03a3-112">Requirements</span></span>



| <span data-ttu-id="e03a3-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="e03a3-113">Requirement</span></span> | <span data-ttu-id="e03a3-114">Valore</span><span class="sxs-lookup"><span data-stu-id="e03a3-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e03a3-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e03a3-115">Header</span></span><br/> | <dl> <span data-ttu-id="e03a3-116"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="e03a3-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e03a3-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e03a3-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e03a3-118">Funzioni</span><span class="sxs-lookup"><span data-stu-id="e03a3-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="e03a3-119">Decompressione e compressione \_ del formato DXGI per la modifica dell'immagine In-Place</span><span class="sxs-lookup"><span data-stu-id="e03a3-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





