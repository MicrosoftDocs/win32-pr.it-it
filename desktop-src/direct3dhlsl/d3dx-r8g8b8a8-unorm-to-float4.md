---
title: Funzione D3DX_R8G8B8A8_UNORM_to_FLOAT4
description: Decomprime \_ \_ \_ i dati di DXGI Format R8G8B8A8 UNORM shader in un XMFLOAT4. | Funzione D3DX_R8G8B8A8_UNORM_to_FLOAT4
ms.assetid: 94430f29-4872-4ecd-99b9-72f3b77c47f2
keywords:
- Funzione D3DX_R8G8B8A8_UNORM_to_FLOAT4 HLSL
topic_type:
- apiref
api_name:
- D3DX_R8G8B8A8_UNORM_to_FLOAT4
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8e24b9f29d2e54f62582407e8ad40488032f8a2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354549"
---
# <a name="d3dx_r8g8b8a8_unorm_to_float4-function"></a><span data-ttu-id="58860-105">D3DX \_ R8G8B8A8 \_ UNORM \_ to \_ float4 Function</span><span class="sxs-lookup"><span data-stu-id="58860-105">D3DX\_R8G8B8A8\_UNORM\_to\_FLOAT4 function</span></span>

<span data-ttu-id="58860-106">Decomprime \_ \_ \_ i dati di DXGI Format R8G8B8A8 UNORM shader in un XMFLOAT4.</span><span class="sxs-lookup"><span data-stu-id="58860-106">Unpacks DXGI\_FORMAT\_R8G8B8A8\_UNORM shader data to an XMFLOAT4.</span></span>

## <a name="syntax"></a><span data-ttu-id="58860-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="58860-107">Syntax</span></span>

``` syntax
XMFLOAT4 D3DX_R8G8B8A8_UNORM_to_FLOAT4(
   UINT packedInput
);
```

## <a name="parameters"></a><span data-ttu-id="58860-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="58860-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58860-109">*packedInput*</span><span class="sxs-lookup"><span data-stu-id="58860-109">*packedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="58860-110">Dati dello shader compressi.</span><span class="sxs-lookup"><span data-stu-id="58860-110">The packed shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58860-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="58860-111">Return value</span></span>

<span data-ttu-id="58860-112">Dati dello shader decompressi.</span><span class="sxs-lookup"><span data-stu-id="58860-112">The unpacked shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="58860-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="58860-113">Requirements</span></span>



| <span data-ttu-id="58860-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="58860-114">Requirement</span></span> | <span data-ttu-id="58860-115">Valore</span><span class="sxs-lookup"><span data-stu-id="58860-115">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58860-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="58860-116">Header</span></span><br/> | <dl> <span data-ttu-id="58860-117"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="58860-117"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58860-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="58860-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58860-119">Funzioni</span><span class="sxs-lookup"><span data-stu-id="58860-119">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="58860-120">Decompressione e compressione \_ del formato DXGI per la modifica dell'immagine In-Place</span><span class="sxs-lookup"><span data-stu-id="58860-120">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





